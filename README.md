# Frontend Mentor - Solución para Room homepage ✨

Esta es una solución al desafío [Room homepage challenge en Frontend Mentor](https://www.frontendmentor.io/challenges/room-homepage-BtdBY_ENq). Los desafíos de Frontend Mentor te ayudan a mejorar tus habilidades de codificación construyendo proyectos realistas.

## Tabla de Contenidos 📋

- [Resumen 📝](#resumen-📝)
  - [El desafío](#el-desafío)
  - [Captura de pantalla 📸](#captura-de-pantalla-📸)
  - [Enlace 🔗](#enlace-🔗)
- [Mi Proceso 🚀](#mi-proceso-🚀)
  - [Construido con 🏗️](#construido-con-🏗️)
  - [Lo que aprendí 🧠](#lo-que-aprendí-🧠)
  - [Desarrollo Continuo 📈](#desarrollo-continuo-📈)
  - [Recursos Útiles 📚](#recursos-útiles-📚)
- [Autor 🧑‍💻](#autor-🧑‍💻)
- [Agradecimientos 🙌](#agradecimientos-🙌)

## Resumen 📝

### El desafío

Los usuarios deberían ser capaces de:

- Ver el diseño óptimo para el sitio dependiendo del tamaño de la pantalla de su dispositivo.
- Ver los estados hover para todos los elementos interactivos en la página.

### Captura de pantalla 📸

![Captura de pantalla de la solución de Room homepage](./design/desktop-design-slide-1.jpg)

### Enlace 🔗

- URL de la Solución (Repositorio): [https://github.com/josecervera20/room-homepage](https://github.com/josecervera20/room-homepage)

## Mi Proceso 🚀

### Construido con 🏗️

- Marcado semántico HTML5
- Propiedades personalizadas de CSS (Variables CSS)
- Flexbox (para layouts responsivos y alineación de elementos)
- CSS Grid (para la estructura general del layout principal)
- Diseño Mobile-first
- [Google Fonts](https://fonts.google.com/specimen/League+Spartan) (Fuente League Spartan)

### Lo que aprendí 🧠

Durante este proyecto, consolidé y profundicé en varias áreas clave del desarrollo frontend, especialmente en la construcción de layouts responsivos y el manejo de estados de `hover` complejos utilizando solo HTML y CSS:

- **Diseño Responsivo Avanzado con CSS Grid y Flexbox**: Utilicé una combinación de CSS Grid para la estructura principal de la página (`.main`) y Flexbox para la alineación interna de componentes como el `.main__controls`, `.main__cta`, y la navegación (`.main__nav`, `.main__links`). Esto me permitió crear layouts complejos que se adaptan fluidamente de móvil a escritorio.

  ```css
  /* Ejemplo de Grid para el layout principal */
  .main {
    display: grid;
    grid-template: repeat(5, max-content) / 1fr;
    grid-template-areas:
      "main"
      "shop"
      "image1"
      "about"
      "image2";
  }

  @media (min-width: 768px) {
    .main {
      grid-template-columns: repeat(7, 1fr);
      grid-template-areas:
        "main main main main shop shop shop"
        "main main main main shop shop shop"
        "main main main main shop shop shop"
        "image1 image1 about about about image2 image2"
        "image1 image1 about about about image2 image2";
    }
  }
  ```

- **Estados de Hover en Elementos de Navegación**: Practiqué la creación de efectos visuales al pasar el ratón sobre los enlaces de navegación, utilizando pseudo-elementos (`::after`) para crear una línea animada que aparece por debajo del texto, mejorando la interactividad.

  ```css
  .main__link::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -5px;
    width: 0%;
    height: 2px;
    background-color: var(--white);
    transition: width 0.3s ease;
  }

  .main__link:hover::after {
    width: 100%;
  }
  ```

- **Variables CSS para Consistencia**: Reforcé la práctica de definir variables CSS en `:root` para colores y fuentes, lo que hace el código más limpio, mantenible y fácil de escalar o modificar la paleta de colores globalmente.

### Desarrollo Continuo 📈

Me gustaría seguir profundizando en:

- **Animaciones CSS Complejas**: Explorar animaciones más avanzadas usando `keyframes` y transiciones para añadir más dinamismo a los elementos sin depender de JavaScript.
- **Accesibilidad (a11y)**: Prestar aún más atención a los atributos ARIA, la navegación con teclado y la semántica HTML para asegurar que mis proyectos sean accesibles para todos los usuarios.
- **Optimización de Imágenes**: Explorar técnicas avanzadas de optimización de imágenes (como `srcset` o formatos de nueva generación) para mejorar los tiempos de carga de la página.

### Recursos Útiles 📚

- [Frontend Mentor](https://www.frontendmentor.io/) - Una plataforma excelente para desafíos de codificación.
- [The Markdown Guide](https://www.markdownguide.org/) - Una referencia útil para la sintaxis de Markdown.
- [MDN Web Docs](https://developer.mozilla.org/es/docs/Web) - Siempre una fuente invaluable para entender propiedades CSS y el funcionamiento de HTML.

## Autor 🧑‍💻

- GitHub - [@josecervera20](https://github.com/josecervera20)

## Agradecimientos 🙌

Agradezco a la comunidad de Frontend Mentor por proporcionar desafíos tan valiosos que me permiten mejorar mis habilidades y construir proyectos realistas. También a las herramientas de depuración de navegadores que fueron cruciales para entender el comportamiento de los SVGs y las interacciones de `hover`.
