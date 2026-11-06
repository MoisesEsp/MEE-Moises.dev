# MEMORY.md — Diario de Estudio
Memoria entre sesiones. Máximo ~50 líneas; resume o elimina lo que ya no aporte.
## Estado actual
- Esqueleto completo: `index.html` (hero + secciones 01–07 + footer) y `css/styles.css`.
- Contenido real de `InfPersonal.md`, foto `assets/img/profile.webp` en el hero.
- Escala tipográfica revisada: cuerpo 16–18 px, textos `--muted` pequeños subidos (nav, hero intro, captions, footer, metadatos).
- Verificado con Chrome DevTools a 1440, 820 y 375 px; consola limpia; Lighthouse 100 en accesibilidad, SEO y buenas prácticas.
## Decisiones (y por qué)
- Repositorio Git inicializado en rama `main`. `.agents/` y las imágenes sin usar (`profile.jpg`, `profile-original.jpeg`) van en `.gitignore`; `skills-lock.json` se versiona para reinstalar skills.
- `origin` apunta al repo `MoisesEsp/MEE-Moises.dev`: fetch por HTTPS y push por SSH (el entorno no tiene credenciales HTTPS).
- Paleta del tema Omarchy `wallhaven`: negro, texto `#FCF900`, acento `#5874ab`, muted `#9a9287` (más claro que el muted del tema para legibilidad).
- Tamaño mínimo de texto legible: 0.75rem para etiquetas y 1rem para cuerpo; el mono a 12 px se leía fino.
- Separación de secciones: banda con borde superior, título con índice, etiqueta y número gigante de fondo (`section__watermark`). Evita que los bloques se mezclen sin usar fondos distintos.
- Nav sticky con scroll horizontal en móvil (7 enlaces no caben); sin estado activo para no añadir JS.
- Animación de entrada solo con `animation-timeline: view()` dentro de `@supports` y `prefers-reduced-motion`.
- Tinte de la foto con `mix-blend-mode: multiply` dentro de `.hero__frame` (no en la figura, porque oscurecía el pie de foto).
## Aprendizajes y errores a evitar
- Los pseudo-elementos con `inset: 0` en una `figure` cubren también el `figcaption`.
- `scrollIntoView` en Chrome headless no espera al scroll suave: usar `scrollBehavior='auto'` + dos `requestAnimationFrame`.
## Próximos pasos
- Revisar textos y jerarquía visual con el usuario.
- Posible imagen Open Graph para compartir el enlace.
