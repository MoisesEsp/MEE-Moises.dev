# Portafolio — Moisés Espinoza

Sitio web personal estático con mi perfil, habilidades, proyectos y datos de contacto.
Está construido con **HTML y CSS puros**, sin frameworks, dependencias ni paso de
compilación.

**Ver en vivo:** https://moisesesp.github.io/MEE-Moises.dev/

## Secciones

- **Inicio**: presentación, rol y enlaces principales.
- **Sobre mí**: perfil profesional y datos rápidos.
- **Habilidades**: lenguajes, bases de datos, herramientas y soporte.
- **Proyectos**: repositorios destacados con sus tecnologías.
- **Experiencia**: trabajos y gestión de servicios.
- **Educación**: formación académica.
- **Certificaciones**: cursos completados.
- **Contacto**: correo, teléfono y redes.

## Tecnologías

| Área | Detalle |
| --- | --- |
| Estructura | HTML5 semántico |
| Estilos | CSS puro con variables y `clamp()` |
| Animaciones | CSS scroll-driven (`animation-timeline: view()`) |
| Diseño | Paleta del tema *wallhaven* de Omarchy, responsive |
| Despliegue | GitHub Pages (rama `main`, raíz) |

## Estructura del proyecto

```text
.
├── index.html              # Estructura de la página
├── css/
│   └── styles.css          # Todos los estilos
├── assets/
│   └── img/
│       └── profile.webp    # Foto del hero
└── InfPersonal.md          # Fuente del contenido
```

`AGENTS.md` y `MEMORY.md` son notas de trabajo del proyecto y no forman parte de la web.

## Cómo verlo en local

Puedes abrir `index.html` directamente en el navegador. Si prefieres servirlo por HTTP:

```bash
python3 -m http.server 8000
```

Y entra en <http://localhost:8000>.

## Detalles de implementación

- Cada sección es una banda independiente con borde superior, título numerado y un
  número grande de fondo, para que los bloques no se mezclen.
- Las animaciones están dentro de `@supports` y se desactivan con
  `prefers-reduced-motion: reduce`; en navegadores sin soporte la web se ve igual,
  solo sin movimiento.
- Sin JavaScript: la navegación son anclas y el menú se adapta a móvil con scroll
  horizontal.
- Comprobado a 1440, 820 y 375 px, con 100 en accesibilidad, buenas prácticas y SEO
  en Lighthouse.

## Despliegue

El sitio se publica con GitHub Pages desde la rama `main`, carpeta raíz. Cada `push`
a `main` reconstruye la web automáticamente. No hay build ni GitHub Actions.

## Sobre este proyecto

Es un proyecto didáctico: el código está pensado para que alguien que empieza a
programar pueda leerlo y entenderlo. Por eso no usa herramientas que oculten el HTML
o el CSS.

## Contacto

- GitHub: [@MoisesEsp](https://github.com/MoisesEsp)
- LinkedIn: [Moisés Espinoza](https://linkedin.com/in/moises-espinoza-b9b4b738a)
- Correo: [Moisesesp726@gmail.com](mailto:Moisesesp726@gmail.com)
