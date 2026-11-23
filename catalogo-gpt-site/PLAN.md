# Catálogo PDF de Wilmas Fashion — Plan de trabajo

**Entregable:** `catalogo-wilmas-fashion.pdf`, un documento vertical multipágina al estilo Canva, con navegación interna y enlaces de compra por ficha. **No se construye ni se publica un sitio web.**

**Especificación:** [PROMPT.md](PROMPT.md). La carpeta conserva el nombre original para no romper enlaces. Los PDF y archivos de trabajo de abajo se producirán cuando se ejecute el encargo; no son parte de esta corrección del prompt.

| Ruta prevista | Contenido |
| --- | --- |
| `entrega/catalogo-wilmas-fashion.pdf` | PDF final de venta, con enlaces verificables. |
| `revision/productos.csv` | Matriz interna de fotos, referencias, PVP y estados de aprobación. |
| `revision/resultado.md` | Lista de pruebas, decisiones y pendientes, separada del PDF público. |

### 1. Verificar contenido

- [ ] Inventariar las 76 fotos, agrupar vistas por modelo y dejar aparte las atribuciones sin confirmar.
- [ ] Cotejar cada modelo con la columna PVP del PDF original y registrar el mayor PVP legible. Casos de control: `USD 18,50` y `USD 28,50` → `USD 28,50`; `USD 17,50` y `#####` → pendiente. No incluir precios de negocio.
- [ ] Confirmar con Wilmas los modelos y precios pendientes y verificar el permiso de incrustación de Alvar Essential Alt y Alvar Pro.

### 2. Maquetar y enlazar

- [ ] Montar portada, índice, separadores, fichas y cierre en A4 vertical con fotos y logos originales. Reservar una jerarquía constante para nombre, referencia, PVP y botón.
- [ ] Insertar enlaces de índice, regreso al índice, redes y CTA. Comprobar que cada CTA de ficha codifica el nombre, la referencia y el único PVP que se ve en la página, y siempre apunta a `wa.me/593963966120`.
- [ ] Exportar una prueba en PDF que mantenga los enlaces y el texto seleccionable. No crear una versión web como reemplazo.

### 3. Revisar y entregar el PDF

- [ ] Abrir la exportación en un visor de escritorio y en celular. Probar todos los CTA y enlaces internos sin enviar mensajes. Validar contraste, legibilidad, paginación, fuentes, recortes y orden.
- [ ] Revisar la prueba con el dueño. Exportar la versión final, repetir las pruebas de enlaces y guardar el PDF separado de la matriz de control. No compartirlo públicamente antes de recibir aprobación.
