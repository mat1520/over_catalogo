# Prompt maestro · Catálogo web de Wilmas Fashion

Copia este documento en GPT Site. Si usas **ChatGPT Sites**, inicia la conversación con `@Sites` y abre el repositorio como proyecto de Codex si esa opción está disponible. Si el editor no puede leer GitHub, adjunta el prompt y los insumos del repositorio. No publiques el sitio hasta que el dueño apruebe la vista previa y la tabla de productos.

---

## Encargo

Actúa como diseñador editorial y desarrollador web. Crea un **catálogo web de Wilmas Fashion**, en español de Ecuador, rápido en celular y destinado a iniciar compras por WhatsApp. El resultado debe sentirse como un catálogo de moda: fotografía protagonista, tipografía de marca, aire entre bloques y movimiento puntual. No construyas un checkout, no pidas datos personales y no generes un PDF.

**Repositorio de referencia:** [mat1520/over_catalogo](https://github.com/mat1520/over_catalogo), rama `main`. Lee [el plan](PLAN.md) y usa los insumos originales; no cambies los archivos fuente:

| Fuente | Úsala para |
| --- | --- |
| [`datos-catalogo.md`](../datos-catalogo.md) | Nombre de marca, contactos, redes, ubicación y notas de verificación. |
| [`precios/lista-de-precios-wilmas-fashion.pdf`](../precios/lista-de-precios-wilmas-fashion.pdf) | Cotejar visualmente la columna **PVP** de cada modelo. |
| [`imagenes/`](../imagenes/) | Revisar las 76 fotos: 51 de conjuntos, 16 de sudaderas con capucha, 4 con medio cierre y 5 de cuello redondo. Agrupa vistas del mismo modelo en una galería. Las carpetas no prueban que dos prendas sean el mismo modelo. |
| [`marca/logos/`](../marca/logos/) y [su PDF original](../marca/logos/logos-originales.pdf) | Logos oficiales. |
| [`marca/tipografia.md`](../marca/tipografia.md) | **Alvar Essential Alt** y **Alvar Pro**, con sus condiciones de uso. |

### 1. Datos y PVP: una cifra por prenda

1. Antes de maquetar, crea una matriz interna por modelo con `id`, `nombre`, `categoria`, `fotos`, `textoAlternativo`, `referenciaPvp`, `pvpCentavos` y `estadoVerificacion`. Identifica los modelos con evidencia del repositorio o confirmación del propietario. No inventes nombres, colores comerciales, materiales, stock, tallas, precios ni equivalencias por parecido. Revisa todas las fotos; deja en la matriz las que no se puedan atribuir. No crees una tarjeta por cada foto.
2. Para **cada modelo identificado**, toma **el mayor valor numérico legible de la columna PVP** entre las tallas de su fila o bloque. Guarda el valor en centavos enteros y muéstralo como `USD 28,50` (dos decimales, coma decimal). No uses las columnas **Mínimo** ni **Precio de negocio**, ni el máximo de toda la categoría. Una ficha muestra **un solo precio**, sin «desde», rangos ni tabla por talla. Cambiar o mencionar una talla en el mensaje no cambia ese precio.
3. No conviertas `#####`, blancos ni cifras ilegibles en cero o en precios inferidos. Un `#####` puede ocultar un PVP mayor: marca esa ficha como **por confirmar**. Si el PVP se lee pero no concuerda con otra columna, no lo sustituyas por el mínimo: registra la discrepancia para revisión. Si no se verifica la relación foto–modelo, no publiques la ficha como producto identificable. Si el modelo es conocido pero su precio no está cerrado, deja la ficha fuera de la página pública hasta validarlo o, si el dueño lo aprueba expresamente, muestra «Consultar precio» con un CTA de consulta; no lo presentes como un precio aprobado.
4. Usa estos valores como comprobación de lectura del PDF, **no** como asignaciones automáticas a las fotos:

   | Bloque del PDF | PVP máximo legible |
   | --- | ---: |
   | Conjuntos Nike / Jombriel / Trébol | USD 28,50 |
   | Conjuntos Balaclava | USD 30,00 |
   | Conjuntos de mujer tubo | USD 27,50 |
   | Hoodies David | USD 17,50 |
   | Chompas cuello redondo Palm Angels / Calvin | USD 17,50 |

### 2. Compra por WhatsApp

- **Número de compra:** `+593 96 396 6120`. Usa exclusivamente `593963966120` en los CTA de compra; no lo sustituyas por el WhatsApp de redes ni por el teléfono alternativo.
- En cada ficha aprobada, genera el enlace a partir de **ese** producto. Base: `https://wa.me/593963966120?text=` más el mensaje codificado una sola vez con `encodeURIComponent`. Texto: `Hola, Wilmas Fashion. Me interesa [nombre] (ref. [id]). Vi el precio de USD [precio]. ¿Me confirman disponibilidad y tallas?` Si hay una URL pública de ficha estable, puedes agregarla sin parámetros de seguimiento. No envíes mensajes automáticamente.
- Un CTA general, fuera de las fichas, usa `Hola, Wilmas Fashion. Quisiera información sobre el catálogo y cómo comprar.`; el CTA de consulta de una prenda no debe incluir un precio sin confirmar. Los enlaces deben ser elementos `<a>` navegables con nombre accesible. Si abren otra pestaña, usa `rel="noopener noreferrer"`. El enlace debe funcionar en WhatsApp móvil y en WhatsApp Web; verifica el destino sin enviar mensajes.

### 3. Marca, composición y contenido

- Usa **Wilmas Fashion** como marca y **Over** solo donde corresponda a la línea de conjuntos. Portada: logo `wilmas-principal.png`; encabezado compacto: `wilmas-logotipo.png`; pie o editorial: `wilmas-fashion-factory.png` o `wilmas-sello-original.png`. Sport, Urban y Kids solo identifican líneas verificadas, no las deduzcas por estética. Usa los PNG originales: no recrees, deformes, recortes ni recolorees los logos.
- Asigna **Alvar Essential Alt** a titulares y nombres de producto; **Alvar Pro** a cuerpos, botones y precios. Carga archivos web locales (`woff2`) solo si se entregan con licencia de uso web y autorización para el destino elegido. No descargues copias informales ni intentes extraer las fuentes de un sitio o PDF. Sin archivos autorizados, usa `system-ui, -apple-system, "Segoe UI", sans-serif` únicamente en la vista previa y señala que falta aprobación tipográfica antes de publicar.
- Toma como base sobria la [página 2 del catálogo Gravity Streetwear en Canva](https://www.canva.com/design/DAG7DqU67YQ/oK-3QYnKUpPYa6fCwMSPfw/view?utlId=h9f9eb0b81a#2): guía editorial de categoría, titular con espacio y atención a la prenda. No copies marca, textos, fecha ni imágenes de Gravity. Propón fondo claro, negro carbón, grises neutros y un solo acento discreto para CTA; son decisiones de diseño, no colores oficiales.
- Orden de la página: encabezado con anclas → portada y CTA → categorías filtrables (**Conjuntos**, **Sudaderas con capucha**, **Sudaderas con medio cierre**, **Sudaderas de cuello redondo**) → fichas con foto, nombre, PVP y compra → cómo comprar → local y redes → pie. Las categorías sin productos verificados no muestran una grilla vacía: se mantienen fuera hasta que haya productos aprobados.
- Ubicación publicable: **Centro Comercial de Mayoristas y Negocios Andinos**, av. Pedro Vicente Maldonado **10385** y Quimiag, **Asociación La Campana**, pasillos **15A, 16A y 15B**, sur de Quito. Enlaza la referencia del repositorio. No publiques Amaguaña o Calderón como sucursales vigentes ni inventes horarios, envíos o políticas. Redes verificadas: [Instagram @wilmasfashionec](https://www.instagram.com/wilmasfashionec/), [TikTok @wilmasfashion](https://www.tiktok.com/@wilmasfashion) y [TikTok @wilmasfashionec](https://www.tiktok.com/@wilmasfashionec/).

### 4. Movimiento, sin distraer de la compra

Explora las vistas públicas de [The Prompts Factory](https://thepromptsfactory.com/) por **nombre**. Úsalas como referencias de interacción; no copies prompts, código ni recursos de la biblioteca:

| Vista de referencia | Adaptación a Wilmas |
| --- | --- |
| **AFTERIMAGE — Gallery exchange** | Al tocar otra foto de la misma ficha, fundido breve (180–220 ms) en un marco de tamaño fijo. Galería manual, sin reproducción automática. |
| **Editions — Scatter sort** | Al filtrar por categoría, usa una transición discreta de opacidad y desplazamiento de 4–8 px (160–220 ms); sin dispersión, giros ni reordenamientos dramáticos. |

En portada, permite una sola entrada suave de imagen y título (≤350 ms). No uses loaders que bloqueen, parallax agresivo ni scroll forzado. Realiza el movimiento con CSS y JavaScript ligero; si falla JS, las prendas visibles y sus enlaces siguen accesibles. Con `prefers-reduced-motion: reduce`, muestra todo sin desplazamiento ni transición. Mantén foco visible, filtros navegables por teclado y `aria-pressed` en el filtro seleccionado. El precio y la compra nunca dependen de pasar el cursor.

### 5. Entrega para GPT Site

- Mantén el futuro sitio dentro de `catalogo-gpt-site/sitio/`, con `index.html`, CSS, JS, datos validados y recursos relativos. Conserva las imágenes originales fuera del paquete; exporta al sitio solo las imágenes utilizadas y optimizadas, con dimensiones, `srcset` y carga diferida debajo del primer bloque. No uses rutas `C:\...`, ni dependas de enlaces temporales, del PDF de precios en tiempo de ejecución o de cargar las fotos desde la vista de GitHub.
- Entrega una vista previa funcional a 360, 768 y 1440 px y prueba en el entorno GPT Site real (según las opciones de importación disponibles en la cuenta). Si admite proyecto, abre esta carpeta como proyecto compatible; si solo acepta archivos adjuntos, proporciona el prompt y los recursos aprobados. No asumas que acepta ZIP ni publiques automáticamente. La carpeta es portable y puede empaquetarse si el destino lo admite.
- Entrega informe de pendientes (foto ↔ modelo, PVP, licencia de fuentes), matriz verificable, y lista de pruebas. El proyecto de publicación no incluye el PDF de origen, precios de negocio, observaciones internas, credenciales ni información personal. La aprobación del propietario es necesaria antes de publicar.
