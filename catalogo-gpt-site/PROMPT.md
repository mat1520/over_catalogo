# Prompt maestro · Catálogo PDF de Wilmas Fashion

Copia este prompt en la herramienta que usarás para maquetar el catálogo y proporciona el [repositorio](https://github.com/mat1520/over_catalogo) como fuente. La carpeta conserva el nombre `catalogo-gpt-site/` para mantener sus enlaces, pero **el entregable es un PDF, no una web**.

---

## Encargo

Actúa como diseñador editorial de moda. Diseña un **catálogo comercial multipágina en PDF**, en español de Ecuador, para compartir por WhatsApp y consultar desde un celular. Toma como referencia la [página 2 del catálogo de Gravity Streetwear en Canva](https://www.canva.com/design/DAG7DqU67YQ/oK-3QYnKUpPYa6fCwMSPfw/view?utlId=h9f9eb0b81a#2): una composición vertical sobria, encabezados claros por categoría, fotografía protagonista y espacios amplios. No copies su marca, textos, fecha ni imágenes.

**No entregues un sitio, landing page, HTML como producto final, checkout ni visor web.** La compra se inicia desde enlaces clicables dentro del PDF. Si se usa GPT Site u otra IA como apoyo, debe dar instrucciones para exportar el PDF o entregar el PDF; no debe publicar una web como sustituto. Revisa [el plan de trabajo](PLAN.md).

## Insumos y verificación

| Archivo | Uso |
| --- | --- |
| [`datos-catalogo.md`](../datos-catalogo.md) | Marca, contactos, dirección y redes verificadas. |
| [`precios/lista-de-precios-wilmas-fashion.pdf`](../precios/lista-de-precios-wilmas-fashion.pdf) | Fuente principal de los PVP. Verifica visualmente la columna correcta. |
| [`imagenes/`](../imagenes/) | Revisa las 76 fotos: 51 de conjuntos, 16 de sudaderas con capucha, 4 con medio cierre y 5 de cuello redondo. Agrupa ángulos del mismo modelo; no crees un producto por foto. |
| [`marca/logos/`](../marca/logos/) y [PDF original de logos](../marca/logos/logos-originales.pdf) | Usa los recursos oficiales, sin redibujarlos. |
| [`marca/tipografia.md`](../marca/tipografia.md) | Alvar Essential Alt y Alvar Pro, con condiciones de uso. |

Antes de maquetar, arma una matriz interna con referencia estable, modelo, categoría, fotos, fila o bloque del PDF de precios, PVP legibles, PVP elegido y estado de verificación. Revisa todas las fotos; registra las que no puedas atribuir, sin asignar modelos por parecido. No inventes stock, tejidos, colores comerciales, tallas, nombres, características ni precios. El catálogo final solo debe mostrar prendas y datos aprobados.

## Regla de precios: un PVP por prenda

1. Para cada modelo identificado, muestra **el valor numérico más alto legible de la columna PVP** entre sus tallas. No uses el máximo de toda la categoría ni las columnas **Mínimo** o **Precio de negocio**. Formato: `USD 28,50`.
2. Muestra **una cifra por ficha**, sin «desde», rangos ni tablas de precio por talla. Si el cliente consulta otra talla, el mensaje de WhatsApp conserva el mismo PVP mostrado.
3. Un `#####` o valor ilegible no equivale a cero y podría ocultar el mayor PVP. Marca el modelo como pendiente hasta que Wilmas confirme la cifra. Si hay una discrepancia entre columnas, regístrala para revisión sin sustituir el PVP por el mínimo. No publiques una ficha sin confirmar la relación foto–modelo y el precio.

Ejemplos para comprobar la lectura del PDF, **no para asignar precios a fotos sin identificar**:

| Bloque de origen | PVP máximo legible |
| --- | ---: |
| Conjuntos Nike / Jombriel / Trébol | USD 28,50 |
| Conjuntos Balaclava | USD 30,00 |
| Conjuntos de mujer tubo | USD 27,50 |
| Hoodies David | USD 17,50 |
| Chompas cuello redondo Palm Angels / Calvin | USD 17,50 |

## Diseño editorial y paginación

- **Formato:** A4 vertical, márgenes de 14–18 mm y retícula consistente. Prioriza una ficha protagonista o, como máximo, dos fichas por página de venta. Usa fotos amplias, sin recortar partes importantes de la prenda. Evita colocar precios o contacto sobre fondos fotográficos que dificulten la lectura.
- **Portada:** `wilmas-principal.png`, foto editorial aprobada y título «Catálogo Wilmas Fashion». Wilmas Fashion es la marca; «Over» solo nombra la línea de conjuntos correspondiente.
- **Índice:** enlaza internamente las secciones con fichas verificadas. Orden sugerido: Conjuntos, Sudaderas con capucha, Sudaderas con medio cierre, Sudaderas de cuello redondo. Omite categorías sin prendas confirmadas.
- **Separadores y fichas:** abre cada categoría con un título claro y una buena foto. En cada ficha coloca foto, nombre confirmado, referencia, PVP único y botón «Comprar por WhatsApp». Usa numeración discreta y enlaces «Volver al índice» en los separadores y en el cierre.
- **Cierre:** explica cómo consultar disponibilidad y tallas por WhatsApp, sin prometer stock ni condiciones no confirmadas. Incluye local, redes y contacto. Usa `wilmas-logotipo.png` o `wilmas-fashion-factory.png` como firma. Los sellos Sport, Urban y Kids solo se usan para líneas confirmadas.
- **Identidad:** Alvar Essential Alt para títulos y nombres; Alvar Pro para texto, precios y botones. No deformes ni recolorees los logos. Usa una paleta sobria de blanco, negro carbón y grises, con un acento discreto para compra. Emplea archivos de fuentes licenciados y comprueba el permiso de incrustación en PDF. Si no están disponibles, entrega una prueba con sustitución claramente indicada y pide aprobación antes de exportar la versión final.

## WhatsApp y navegación

- **Único destino de compra:** `+593 96 396 6120`, normalizado como `593963966120`. No uses los números publicados en redes como destinos de compra.
- Genera un enlace distinto por ficha **al maquetar/exportar**, a partir de sus datos aprobados. Usa `https://wa.me/593963966120?text=` seguido del mensaje codificado una sola vez en URL: `Hola, Wilmas Fashion. Me interesa [nombre] (ref. [referencia]). Vi el precio de USD [precio]. ¿Me confirman disponibilidad y tallas?`
- Vincula el botón completo a la URL. Para el CTA general: `Hola, Wilmas Fashion. Quisiera información sobre el catálogo y cómo comprar.` Muestra también el número visible como respaldo si el visor no activa enlaces. No envíes mensajes de prueba; comprueba el destinatario y el borrador.
- Usa hipervínculos estándar en el PDF: índice, vuelta al índice, CTA de compra y redes. **No dependas de animaciones, JavaScript, video ni transiciones del visor.** Si consultas [The Prompts Factory](https://thepromptsfactory.com/), usa **AFTERIMAGE — Gallery exchange** como inspiración para secuencias impresas de fotos, y **Editions — Scatter sort** para organizar bloques visuales por categoría. No copies sus recursos ni intentes reproducir los efectos en el PDF.

## Datos exactos del cierre

- **Local:** Centro Comercial de Mayoristas y Negocios Andinos, av. Pedro Vicente Maldonado **10385** y Quimiag, **Asociación La Campana**, pasillos **15A, 16A y 15B**, sur de Quito. [Referencia de la marca](https://www.tiktok.com/@wilmasfashionec/video/7707224390018157825).
- **Redes:** [Instagram @wilmasfashionec](https://www.instagram.com/wilmasfashionec/), [TikTok @wilmasfashion](https://www.tiktok.com/@wilmasfashion) y [TikTok @wilmasfashionec](https://www.tiktok.com/@wilmasfashionec/).
- No anuncies Amaguaña ni Calderón como locales vigentes. No inventes horarios, envíos, cambios ni devoluciones.

## Exportación y entrega

Entrega **`catalogo-wilmas-fashion.pdf`**, optimizado para compartir, con texto seleccionable, fuentes autorizadas incrustadas cuando corresponda y enlaces activos. Si usas Canva, exporta una prueba como **PDF estándar** y comprueba el resultado descargado, no solo la vista de Canva. No uses opciones de aplanado o conversión a imágenes que eliminen los enlaces o el texto.

Antes de aprobarlo, abre el archivo descargado en escritorio y celular, prueba el índice y los CTA de cada ficha, revisa el número de destino y compara cada PVP con la matriz. Comprueba legibilidad, alineación, fotos sin cortes no previstos y ausencia de páginas vacías. Entrega por separado la matriz y los pendientes; no incluyas en el PDF público el precio de negocio, credenciales ni notas internas. El dueño aprueba la prueba antes de compartir el PDF final.
