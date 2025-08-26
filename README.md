# Happy Blender Day - Laboratorio CSS3

## Selectores aplicados

- **Selectores de tipo**:  
  - `header`, `nav`, `section`, `article`, `figure`, `figcaption`, `p`, `h1`, `h2`, `h3`, `ul`, `ol`, `li`, `table`, `th`, `td`, `blockquote`.

- **Selectores de clase**:  
  - `.container` → contenedores principales  
  - `.card` → tarjetas de secciones (agenda, expositores, registro, ubicación)  
  - `.btn` → botones de registro  
  - `.badge` → etiquetas de expositores  
  - `.tag` → elementos decorativos (si se agregan)  

- **Selectores de ID**:  
  - `#inicio` → header  
  - `#agenda`, `#expositores`, `#registro`, `#ubicacion`, `#patrocinadores` → secciones principales  

- **Selectores de atributo**:  
  - `a[target="_blank"]` → enlace externo a Blender.org  
  - `img[alt]` → todas las imágenes con atributo alt  
  - `input[type="email"]` → campo de correo en el formulario  
  - `a[href^="https://"]` → enlaces externos (se añadió indicador "↗")  

- **Selectores combinadores**:  
  - Descendiente: `.card p` → párrafos dentro de tarjetas  
  - Hijo directo: `header > nav` → menú principal  
  - Adyacente: `nav a + a` → separación de enlaces en menú  
  - Hermanos: `.tag ~ .tag` → etiquetas decorativas (ejemplo futuro)  

## Pseudo-clases

- **Estado**:  
  - `:hover` → `.btn` y enlaces en el menú  
  - `:focus-visible` → enlaces en nav y botones  
  - `:active` → botones de formulario  

- **Estructurales**:  
  - `:first-child` → primer elemento de listas (`ul` de agenda y expositores)  
  - `:last-child` → último elemento de listas  
  - `:nth-child(2n)` → elementos pares en listas  
  - `:not(.activo)` → ejemplo preparado para exclusiones de clases  

## Especificidad

- **!important**:  
  - `.badge` dentro de `.card` → sobrescritura en `overrides.css`  
- **Estilo inline**:  
  - `<h3>` de cada expositor → color y fondo inline para la badge  

## Box model

- `box-sizing: border-box` → aplicado global en `base.css`  
- Márgenes y padding controlados en `.card`, `section > h2`, `main > section`  
- Colapso de márgenes entre títulos y tarjetas  

## Overflow

- Párrafo con texto largo en `.card` del registro y agenda  
- `overflow: auto` o `hidden` según necesidad  

## Flexbox

- `nav ul` → `display: flex` para alinear enlaces con `justify-content: center; gap: 1.5rem`  

## Grid

- `#patrocinadores article` → `display: grid` para organizar logotipos de patrocinadores  
- Columnas definidas con `grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));`  

## Position

- `.banner .etiqueta` → `position: relative` en contenedor, `absolute` en la etiqueta decorativa (preparado si se implementa un banner adicional)  