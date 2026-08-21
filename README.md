# Landing de portafolio personal — PFO1

Landing de portafolio personal desarrollada en HTML y CSS puro para la materia Desarrollo de Sistemas Web (Back End) de la Tecnicatura en Desarrollo de Software. Presenta mi perfil, mis habilidades, una sección personal y una forma de contacto, con un enlace visible a mi GitHub.

**🔗 URL publicada en Vercel:** (https://portfolio-pfo1.vercel.app/)  

**🔗 Repositorio:**  https://github.com/sil-graci/portfolio-pfo1

**🔗 GitHub:** https://github.com/sil-graci

## Cómo verlo localmente

Es un sitio estático, no necesita instalación. Alcanza con abrir `index.html` en el navegador, o servirlo con cualquier servidor estático (por ejemplo la extensión "Five Server" de VS Code).

## Estructura del proyecto

```
portfolio-landing/
├── index.html
├── style.css
├── images/
│   ├── avatar.png│  
└── README.md
```

## Decisiones de diseño

- **Concepto:** portafolio de una estudiante de desarrollo de software, pensado para reflejar identidad de "developer en formación" sin caer en un estilo genérico. El elemento distintivo es el **footer con estética de terminal** (ventana con barra de semáforo y un `echo` con cursor parpadeando), que retoma visualmente el mundo del código.
- **Paleta:** base cálida y clara (`#f5f7f1` / `#ebefe4`) con coral (`#ff6f59`) como acento principal, teal (`#1f8a85`) como acento secundario y amarillo mostaza (`#ffc857`) como highlight — colorida pero equilibrada, sin caer en tonos saturados.
- **Tipografía:** `Fraunces` para títulos (con carácter propio), `Sora` para el texto de lectura y `JetBrains Mono` para los elementos con estética de código (nav, chips de habilidades, footer). Todo cargado desde Google Fonts.
- **Layout:** se combinan **Flexbox** (header, hero, contacto entre sí, tarjetas de la sección personal en su contenedor) **y CSS Grid** (grilla de habilidades, grilla de tarjetas de la sección personal, grilla del formulario de contacto). Se eligió Flexbox para alineaciones lineales de una dimensión (nav, distribución hero) y Grid para las cuadrículas de tarjetas, donde interesa controlar filas y columnas a la vez.
- **Animaciones:** cursor parpadeante (hero y footer) vía `@keyframes`, subrayado animado en los enlaces del nav, elevación sutil al pasar el mouse por botones y chips de habilidades, y un efecto typewriter en el mensaje del footer que revela el texto caracter por caracter al cargar la página. Se respeta `prefers-reduced-motion` para desactivar las animaciones si el usuario lo prefiere.
- **Responsive:** unidades relativas y `clamp()` para tipografía fluida, grillas con `auto-fit`/`minmax()` que se adaptan solas, y breakpoints en `720px` y `480px` donde el header y las secciones con dos columnas pasan a una sola columna y se reduce el espaciado para pantallas chicas.
- **Accesibilidad:** etiquetas semánticas (`header`, `nav`, `main`, `section`, `footer`), `aria-labelledby` conectando cada sección con su título, foco visible con `:focus-visible`, y todas las imágenes con texto alternativo descriptivo.
- **Imágenes:** el avatar del hero (`images/avatar.png`) es una ilustración generada con Microsoft Copilot a partir de una foto propia (ver declaración de IA más abajo). 

## Declaración de uso de IA

### Claude (Anthropic)

- **Herramienta y para qué la usé:** a través de la interfaz web de Claude.ai. La usé para generar la estructura HTML semántica completa y el CSS (variables, tipografía, layout con Flexbox y Grid, animaciones y responsive), a partir de mis datos (usuario de GitHub, carrera, habilidades e intereses personales) y de una dirección de paleta de colores colorida pero equilibrada, sin caer en tonos saturados. También la usé después para ajustar detalles puntuales: el tamaño y recorte del avatar (`object-fit`), su posición en el hero (`flex-basis`, `gap`), la corrección de espaciados excesivos en mobile, la corrección de un atributo `class` duplicado en el HTML, y la incorporación de la animación typewriter del footer, y para armar la estructura y redacción de este mismo README.
- **Plan:** gratuito.
- **Experiencia previa con la herramienta:** la usé antes para consultas puntuales, no para generar un proyecto completo de este tamaño.
- **Qué revisé/adapté con criterio propio:** Fui releyendo y ajustando textos y decisiones de diseño a lo largo de todo el proceso (no solo al final), revisé que el contenido de "Sobre mí" y "Fuera del código" reflejara mis intereses reales (música, bici, series), decidí los valores finales de espaciado y tamaño del avatar probando distintas opciones hasta que quedó como quería. En el caso del README, algunos términos técnicos usados en la sección de decisiones de diseño (por ejemplo, nombres específicos de propiedades CSS) los fui consultando con la IA, y si bien los entendí, todavía me falta práctica para poder usarlos con soltura.

### Microsoft Copilot

- **Herramienta y para qué la usé:** generación de la ilustración/avatar (`images/avatar.png`) que se muestra en el hero de la landing, a partir de una foto propia que le di como referencia.
- **Plan:** gratuito.
- **Experiencia previa con la herramienta:** la usé antes para generar otras imágenes, aunque no para un avatar de uso personal como este.
- **Qué revisé/adapté con criterio propio:** generé varias variantes a partir de la consigna y elegí la que mejor representaba lo que buscaba. Después ajusté mediante CSS su recorte, formato circular y borde (`object-fit`, `border-radius`, `outline`) para integrarla mejor con la paleta de colores de la landing, probando distintos valores en el navegador hasta llegar al resultado final.

