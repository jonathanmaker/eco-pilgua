# Mejoras y Estilización del Sitio Web Eco Pilgua con CSS

**EVALUACIÓN N°2**

**UNIDAD 2:** Diseño web y CSS  
**ASIGNATURA:** Diseño Web  
**DOCENTE:** Felipe Igor Flores Valdebenito  
**FECHA:** Abril, 2026

**INTEGRANTES:**
- Jonathan Damian Peña
- Oscar Coilla
- Reinaldo Canales G.
- Edwin
- Gerson
- Noni

---

## Contenido
1. [Introducción](#1-introducción)
2. [Descripción de Cambios y Mejoras Visuales](#2-descripción-de-cambios-y-mejoras-visuales)
3. [Justificación de las Decisiones de Diseño](#3-justificación-de-las-decisiones-de-diseño)
4. [Antes y Después – Descripción Comparativa](#4-antes-y-después--descripción-comparativa)
5. [Aportes Individuales](#5-aportes-individuales)
6. [Conclusión](#6-conclusión)

---

## 1. Introducción

El presente informe corresponde a la Evaluación N° 2 de la asignatura Diseño Web, cuyo objetivo es aplicar estilos CSS para mejorar visualmente la página web del emprendimiento **Eco Pilgua**, desarrollada en la evaluación anterior.

Eco Pilgua es un emprendimiento de papelería creativa y sublimación ubicado en Talca, Chile, fundado por una emprendedora que convirtió una historia de resiliencia personal en un negocio lleno de creatividad y cariño. La página web original contaba con una estructura HTML correcta y un CSS básico funcional, pero con oportunidades claras de mejora en términos de diseño visual, jerarquía de contenido, layout y experiencia de usuario.

En esta entrega se aplicaron mejoras al archivo CSS externo (`css/styles.css`) y ajustes menores al HTML para incorporar clases semánticas nuevas. Se mantuvo toda la información original del sitio, respetando la identidad de marca y los colores corporativos verdes del emprendimiento.

---

## 2. Descripción de Cambios y Mejoras Visuales

### 2.1 Variables CSS (Custom Properties)
Para mantener consistencia en los colores corporativos del sitio, se definieron tres variables CSS al inicio del archivo de estilos, dentro del selector `:root`. Estas son `--verde-suave`, `--verde-medio` y `--verde-oscuro`, que corresponden a los tonos verdes de la identidad de la marca. Su uso permite reemplazar valores hexadecimales repetidos por una referencia única, facilitando futuros ajustes de color en un solo lugar.

### 2.2 Header
El header conserva su estructura general (logo, nombre de la marca, eslogan y barra de navegación), aplicando mejoras visuales con CSS. Se mantuvo el fondo blanco y se agregó una sombra suave en la parte inferior para dar separación con el contenido. El logo, ya circular, recibió un efecto leve de aumento al pasar el mouse mediante la propiedad `transform: scale()`, aportando interactividad sin saturar visualmente.

### 2.3 Navegación
La barra de navegación se trabajó con Flexbox para distribuir los enlaces de manera centrada y en espacios uniformes, se insertó un efecto al pasar el cursor por encima resaltando una línea verde debajo del texto con efecto expansivo hacia los lados.

### 2.4 Secciones como Tarjetas
En el código antiguo las secciones no tenían estilo visual propio — eran bloques de texto plano sin separación visual. Se aplicó el patrón de tarjetas en secciones como misión/visión y testimonios, con `border-radius`, `padding`, `box-shadow` y colores de fondo, dando estructura y jerarquía visual al contenido.

### 2.5 Galería de Historia
Anteriormente las fotografías se mostraban empujadas con un atributo `width` en línea. Se rediseñó la galería (.historia-galeria) utilizando **Flexbox** para centrar y distribuir equitativamente las fotografías. Se aplicó `object-fit: cover` para evitar la deformación fotográfica y se establecieron dimensiones fijas. Además, se sumó interactividad agregando bordes redondeados sutiles y un efecto `:hover` de elevación (`transform: translateY(-5px)`) acompañado de sombra para destacar la imagen.

### 2.6 Misión y Visión con Flexbox
Anteriormente la sección de Misión y Visión no tenía estructura visual definida — los artículos aparecían apilados verticalmente sin contenedor ni estilos. Se agregó el div con clase `.articulos-mv` y se aplicó Flexbox para mostrar ambas tarjetas en fila en pantallas grandes y apiladas en móvil. Cada tarjeta recibió `border-left` verde como acento visual, fondo verde suave, `border-radius` y `padding` interno, pasando de texto plano sin estilo a tarjetas organizadas visualmente.

### 2.7 Lista de Productos con CSS Grid
Anteriormente los productos se mostraban como una lista de bullets (`<li>`) sin ningún estilo visual. Se rediseñó completamente usando CSS Grid con `grid-template-columns: repeat(2, 1fr)` para organizar las tarjetas en 2 columnas iguales. Cada ítem pasó de ser un bullet de texto a una tarjeta con `display: flex`, esquinas redondeadas (`border-radius: 10px`), borde sutil y efectos hover avanzados y optimizados para WebKit que revelan imágenes de fondo con una transición muy suave.

### 2.8 Testimonios
Anteriormente los testimonios eran articles simples apilados verticalmente, con imagen centrada y blockquote con borde izquierdo verde, sin tarjetas ni layout horizontal. Se rediseñaron completamente usando un contenedor `.testimonios-grid` con Flexbox, donde cada testimonio se convierte en una tarjeta con fondo verde suave, foto redonda, y un efecto hover de elevación sutil. El diseño es responsivo y apila las tarjetas en móvil de manera automática.

### 2.9 Footer Mejorado
El footer se rediseñó utilizando flexbox como estructura principal. La ubicación del logo de la marca quedó a la izquierda y los datos de contacto distribuidos a la derecha. Se agregaron los respectivos íconos de la librería vectorial *Phosphor Icons* para acompañar visualmente cada dato de redes sociales, dirección y correo, mejorando notablemente la distribución espacial y visual de los datos de contacto.

### 2.10 Diseño Responsivo
Para asegurar la correcta visualización en dispositivos móviles, se aplicaron Media Queries en diferentes secciones de CSS. Para el footer y testimonios se utilizó un breakpoint de **600px**, en donde las tarjetas pasan a una sola columna centrando los elementos. En productos y Misión/Visión, se utilizó un breakpoint de **640px** ajustando la grilla a una sola columna de forma que se adapte perfectamente a las pantallas pequeñas. Con estos ajustes, se garantiza que el sitio brinde una excelente usabilidad táctil.

---

## 3. Justificación de las Decisiones de Diseño

### 3.1 Paleta de colores
Se mantuvo la paleta verde corporativa del sitio original, ya que es coherente con el nombre del emprendimiento (Eco = natural, sustentable) y transmite frescura y confianza. El sistema de variables CSS (`:root`) garantiza consistencia cromática en todos los elementos del proyecto.

### 3.2 Gradiente y Coherencia visual entre Header y Footer
Lograr coherencia entre la parte superior e inferior del sitio permite reforzar la identidad de la marca a lo largo de la experiencia de navegación del usuario. Tanto el header como el footer se estructuraron respetando una solidez visual que enmarca la página y unifica el sitio en ambos extremos del flujo de lectura.

### 3.3 Uso de Flexbox y CSS Grid
Se eligió Flexbox para layouts unidimensionales como la navegación, el footer y la sección de misión/visión, donde los elementos se organizan en una sola dirección (fila o columna). CSS Grid se utilizó para layouts bidimensionales y estrictos como la sección de productos, permitiendo organizar el contenido en filas y columnas simultáneamente, por ejemplo con `grid-template-columns: repeat(2, 1fr)` para crear una grilla simétrica. Ambas técnicas son modernas, nativas del navegador y no requieren librerías externas.

### 3.4 Sistema de tarjetas (Cards)
El patrón de diseño de tarjetas es uno de los más utilizados en interfaces UI modernas porque separa visualmente el contenido, mejora la legibilidad y da sensación de organización. Se aplicó en Misión/Visión, Testimonios y Productos. Cada tarjeta cuenta con `border-radius` para esquinas redondeadas, `padding` para dar respiración al contenido y un `box-shadow` suave que evita el efecto pesado de bordes sólidos, aportando profundidad 3D sin saturar la vista.

### 3.5 Efectos de interacción (hover y transiciones)
En diferentes partes del sitio se aplicaron efectos hover acompañados de transiciones suaves para mejorar la sensación de interactividad (microinteracciones). Tanto el logo como las tarjetas y la botonera responden de forma viva al puntero del usuario. En la sección de tarjetas de productos, el efecto revela mágicamente la imagen de fondo de cada ítem sublimado, utilizando siempre `transition: all 1.2s cubic-bezier` para que la fluidez sea armónica.

### 3.6 Tipografía
Se mantuvo **Segoe UI** como fuente principal, estableciendo una jerarquía clara: `h1` de gran peso y títulos `h2` con márgenes inferiores matemáticos para separar el contenido. El `line-height` general a lo largo del cuerpo del sitio garantiza una legibilidad muy cómoda, indispensable en bloques de texto narrativo como lo es "La Historia" de la emprendedora.

---

## 4. Antes y Después – Descripción Comparativa

La siguiente tabla resume los cambios más relevantes entre el diseño original (Evaluación 1) y el CSS mejorado (Evaluación 2):

| Elemento | Antes | Después | Justificación Técnica |
| :--- | :--- | :--- | :--- |
| **Header** | Fondo blanco `#ffffff` plano, `h1` verde oscuro básico sin sombra. | Gradiente dinámico (verde oscuro a medio), `h1` blanco con text-shadow. | Mayor impacto visual en la zona superior y fuerte consistencia de marca corporativa. |
| **Logo** | Tamaño excesivo (220x220px) con el efecto `:hover` comentado en el código. | Tamaño optimizado (140x140px), con efecto `:hover scale(1.05)` activado y borde fotográfico. | Proporción mejorada respecto al menú e interactividad para invitar al clic. |
| **Navegación** | Links simples de color verde, solo con `gap: 1.5rem` básico. | Botones en línea con línea animada de expansión al hacer hover. | Mejor usabilidad de los botones, haciéndolos clickeables en una zona más amplia. |
| **Secciones** | Sin tarjetas. Contenido directo al `main` sin color de fondo ni `box-shadow`. | Empaquetado estricto en "Tarjetas" con fondos verde suave, bordes y sombreados. | Organización, jerarquía y descanso visual claro entre diferentes tópicos. |
| **Galería** | Imágenes con `border-radius: 4px` y flex básico, pero sin control estricto de proporción. | `object-fit: cover`, altura unificada de 200px, hover 3D con elevación. | Fotomuro consistente, interactivo y atractivo. |
| **Misión y Visión** | Sin estilos específicos en el CSS original (apilamiento por defecto). | Flexbox lado a lado, borde izquierdo acentuado. | Aprovechamiento inteligente del espacio horizontal en pantallas grandes. |
| **Productos** | No existía ninguna regla CSS que apuntara a `#productos` en el archivo base. | Tarjetas completas Grid CSS, fotos emergentes y máscaras para WebKit. | Presentación comercial inmersiva y de impacto. |
| **Testimonios** | Artículos centrados estáticamente con márgenes inferiores de `2.5rem`. | Grid Flexbox responsivo, tarjetas e imágenes circulares con efecto de elevación. | Credibilidad humana y organización coherente. |
| **Footer** | Centrado básico con borde superior gris sólido (`border-top`). | Flexbox ordenado, integración de iconos vectoriales Phosphor. | Coherencia de cierre y facilidad de lectura. |
| **Adaptabilidad** | Ninguna regla `@media` query en el archivo original. | Múltiples Media Queries (`600px` y `640px`). | Accesibilidad absoluta en cualquier dispositivo móvil. |

> *Nota: Las capturas de pantalla del "Antes y Después" se adjuntan en el archivo comprimido de entrega del proyecto, donde se aprecia la gran transformación visual.*

---

## 5. Aportes Individuales

- **Reinaldo Canales Gómez:** Mi aporte fue en las mejoras de la sección misión y visión en las partes del HTML, así como las mejoras en el CSS utilizando Flexbox para mejorar el layout al igual que las “cards”, optimizando el aspecto visual de bordes y el uso de padding. También me enfoqué en el desarrollo del informe, ayudando en secciones como la introducción, la conclusión y el esqueleto de este documento junto al equipo.
- **Oscar Coilla O.:** Trabajé en la sección de Testimonios. Reemplacé la estructura HTML antigua, donde los testimonios eran artículos planos, por una estructura nueva basada en tarjetas con clases reutilizables (`.testimonio`, `.testimonio-foto`, `.testimonio-cita`, `.testimonio-autor`). Apliqué Flexbox para que las tarjetas se acomoden en fila y se apilen automáticamente en pantallas chicas mediante un media query. Cambié las fotografías por imágenes más naturales y reescribí los textos de las citas para sonar más cercanos al perfil real de las clientas. Utilicé las variables CSS del proyecto para mantener la coherencia corporativa.
- **Jonathan Damian Peña:** Realizó el ordenamiento y limpieza general del mockup inicial entregado en la Evaluación 1. Verificó el cierre de etiquetas HTML, configuró el esqueleto visual y centralizó componentes esenciales para facilitar el trabajo posterior con CSS. Adicionalmente, asumió el rol de crear y gestionar el repositorio en GitHub (control de versiones descentralizado) y mejoró estéticamente la estructura del informe.
- **Edwin:** Desarrolló íntegramente la sección de productos mediante CSS Grid y estandarizó la concordancia visual de todo el sitio, unificando colores, márgenes y estilos mediante variables CSS. Implementó el diseño responsivo para garantizar una navegación fluida en dispositivos móviles y optimizó el rendimiento de la web mediante la gestión eficiente de activos visuales. Además, lideró la revisión final del código y la consolidación del informe técnico para asegurar la máxima calidad en la entrega.
- **Gerson:** Ejerció el rol de validación técnica (Quality Assurance). Revisó exhaustivamente que las configuraciones de CSS y el código estuviesen aplicados correctamente, asegurando que el proyecto cumpliera rigurosamente, punto por punto, con los lineamientos y las exigencias de la rúbrica de la evaluación actual.
- **Noni:** Contribuyó activamente en la alineación estética del proyecto, definiendo y verificando los códigos de color para alimentar la sección de variables (`:root`). Buscó e integró los iconos vectoriales utilizados en el Footer, y colaboró en la ortografía, estructuración y edición final de los informes.

---

## 6. Conclusión

La realización de esta evaluación permitió aplicar de forma práctica los conceptos de CSS estudiados en las semanas III y IV de la asignatura, transformando la página web con estructura HTML correcta pero diseño visual básico en un sitio moderno, coherente y atractivo.

Las mejoras implementadas abordan los distintos aspectos del diseño visual: tipografía, colores, espaciados, bordes, sombras y layout, todos ellos requerimientos explícitos de la evaluación. La incorporación de técnicas modernas como **CSS Variables, Flexbox, CSS Grid y transiciones** demuestra el aprendizaje profundo de las herramientas vigentes en la industria del desarrollo web.

Desde la perspectiva del **Box Model** (Modelo de Caja), cada elemento fue diseñado considerando conscientemente el `padding` (espacio interno que deja respirar al contenido), el `margin` (separación externa y matemática entre los diferentes elementos y secciones), el `border` (frontera perimetral visible) y las magnitudes de ancho y alto (`width`/`height`). La implementación global de `box-sizing: border-box` como método de reseteo garantizó un comportamiento predecible y eliminó los típicos dolores de cabeza relacionados a anchos desfasados.

En cuanto al manejo de código, en el sitio de Eco Pilgua se aplican de manera diferenciada selectores por *id* y por *clase* según su contexto. Los **selectores por `id`** se utilizan exclusivamente para secciones únicas estructurales de la página (`#historia`, `#mision-vision`, `#productos`, `#testimonios` y `#contacto`), ya que cada uno representa una sola instancia y permite anclar fluidamente la navegación del usuario. Por otra parte, los **selectores de clase** se reservaron para patrones modulares que se aplican a múltiples elementos repetitivos (`.testimonio`, `.testimonio-foto`, `.articulos-mv`, `.historia-galeria`, `.footer-contenido`). Esta distinción técnica permite mantener una hoja de estilos escalable, evita duplicación irresponsable de reglas CSS y facilita al equipo cualquier mejora futura.

En resumen, el sitio "Eco Pilgua" ha evolucionado desde un sencillo mockup documentativo hacia una sólida presencia digital. Su código y estilo proyectan a la perfección la artesanía, el esmero, y sobre todo, la identidad creativa que define al negocio de forma real y auténtica en el mercado.

---
*Fin del Informe.*
