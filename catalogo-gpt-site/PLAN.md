# Catálogo web de Wilmas Fashion — Implementation Plan

> **Para el equipo de implementación:** ejecuta el plan por tareas y marca los pasos completados con `[x]`. Este documento no implementa ni publica el sitio.

**Objetivo:** presentar prendas verificadas con un PVP único y compra por WhatsApp en un catálogo web preparado para GPT Site.

**Arquitectura:** separar los insumos del repositorio, la matriz de verificación y los archivos públicos del sitio. Renderizar en HTML las fichas y sus enlaces, y añadir filtros, galerías y movimiento como mejoras progresivas.

**Tecnologías:** HTML semántico, CSS, JavaScript y datos JSON; sin backend de pagos. Usar las opciones de vista previa del GPT Site elegido para validar compatibilidad.

**Especificación:** [PROMPT.md](PROMPT.md).

### Archivos previstos

| Ruta dentro de `catalogo-gpt-site/` | Contenido |
| --- | --- |
| `validacion/productos.csv` | Matriz de aprobación y traza de foto, modelo y PVP; no incluir en el paquete público. |
| `sitio/index.html` | Portada, categorías, fichas accesibles con enlaces y pie. |
| `sitio/datos/productos.json` | Solo datos públicos aprobados; misma fuente para generar las fichas y mensajes. |
| `sitio/estilos.css`, `sitio/catalogo.js` | Diseño adaptable, filtros y galería; sin bloquear las fichas base. |
| `sitio/assets/` | Logos, fotos optimizadas y fuentes web únicamente si están autorizadas. |
| `validacion/resultado.md` | Pruebas, pendientes e instrucciones reales de vista previa/importación. |

### Tarea 1 — Inventariar y validar

- [ ] Revisar las 76 fotos, agrupar vistas y registrar qué fotos se usaron, cuáles son alternativas y cuáles quedaron pendientes. Cotejar la categoría visual con los modelos del PDF, sin inferir equivalencias.
- [ ] Registrar por modelo el bloque del PDF, los PVP válidos en centavos y su máximo. Casos de control: `1850, 2850 → 2850`; `1950, 3000 → 3000`; `1750, ##### → revisión`, no «1750 confirmado». Comparar visualmente las filas con la columna PVP.
- [ ] Entregar la matriz y pedir a la marca que apruebe modelos, precios dudosos y archivos licenciados. Exportar a JSON solo los modelos publicables; dejar los pendientes fuera del HTML público salvo un CTA de consulta expresamente autorizado.

### Tarea 2 — Construir y probar la experiencia

- [ ] Generar las fichas desde los datos aprobados, con un precio por modelo, fotos, texto alternativo y el enlace individual. En una ficha de prueba, decodificar `text` y comprobar nombre, referencia, precio y caracteres con tildes; probar el CTA general y confirmar que **todos** los destinos de compra son `593963966120`. No enviar mensajes.
- [ ] Montar la composición de marca, navegación por categorías, galería y contacto. Comparar visualmente los logos con los originales; confirmar que Amaguaña y Calderón no figuran como sucursales vigentes.
- [ ] Probar 360, 768 y 1440 px, teclado, foco, contraste, carga de imágenes, filtro sin resultados, movimiento reducido y funcionamiento sin JavaScript. Sin scripts, la grilla base y sus enlaces deben seguir utilizables.

### Tarea 3 — Entregar la vista previa

- [ ] Probar `sitio/` como proyecto autónomo: sin rutas rotas, sin dependencias del PDF, sin credenciales y sin datos internos en el paquete. Confirmar que el entorno GPT Site de la cuenta puede abrir o adaptar el proyecto.
- [ ] Adjuntar captura móvil y escritorio, resultado de pruebas y pendientes. Si faltan fuentes licenciadas, señalar que la vista previa usa un sustituto. Guardar la versión revisable; no publicar sin aprobación.
