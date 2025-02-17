# instapic-app

# Guía sobre Estilos en CSS

## `display: flex`

`display: flex` es una propiedad de CSS que convierte un contenedor en un **contenedor flexible**, permitiendo organizar los elementos internos de forma eficiente.

### **Propiedades principales**
- `flex-direction`: Define la dirección de los elementos (`row`, `column`, etc.).
- `justify-content`: Controla la alineación horizontal.
- `align-items`: Controla la alineación vertical.
- `flex-wrap`: Permite que los elementos se ajusten en varias líneas.
- `gap`: Define el espacio entre los elementos.

### **Ejemplo**
```css
.container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

```
Esto centra los elementos horizontal y verticalmente dentro de `.container`.

# Propiedades de Flexbox en CSS

## 1. `flex-direction`
Esta propiedad define la dirección en la que se colocan los elementos dentro de un contenedor flex.

### Valores posibles:
- `row` (por defecto): Los elementos se colocan en una fila de izquierda a derecha.
- `row-reverse`: Los elementos se colocan en una fila de derecha a izquierda.
- `column`: Los elementos se colocan en una columna de arriba hacia abajo.
- `column-reverse`: Los elementos se colocan en una columna de abajo hacia arriba.

### Ejemplo:
```css
.container {
    display: flex;
    flex-direction: column;
}
```

---

## 2. `justify-content`
Esta propiedad controla la alineación horizontal de los elementos flexibles dentro de su contenedor.

### Valores posibles:
- `flex-start` (por defecto): Alinea los elementos al inicio.
- `flex-end`: Alinea los elementos al final.
- `center`: Centra los elementos en el contenedor.
- `space-between`: Distribuye los elementos con el máximo espacio entre ellos.
- `space-around`: Distribuye los elementos con espacio alrededor de cada uno.
- `space-evenly`: Distribuye los elementos con espacio igual entre ellos.

### Ejemplo:
```css
.container {
    display: flex;
    justify-content: space-between;
}
```

---

## 3. `align-items`
Esta propiedad controla la alineación vertical de los elementos flexibles dentro del contenedor.

### Valores posibles:
- `stretch` (por defecto): Los elementos se estiran para llenar el contenedor.
- `flex-start`: Alinea los elementos en la parte superior.
- `flex-end`: Alinea los elementos en la parte inferior.
- `center`: Centra los elementos verticalmente.
- `baseline`: Alinea los elementos según la línea base del texto.

### Ejemplo:
```css
.container {
    display: flex;
    align-items: center;
}
```

---

## 4. `flex-wrap`
Determina si los elementos flexibles deben ajustarse a una nueva línea cuando el espacio es insuficiente.

### Valores posibles:
- `nowrap` (por defecto): Los elementos se mantienen en una sola línea.
- `wrap`: Los elementos se ajustan a nuevas líneas si es necesario.
- `wrap-reverse`: Igual que `wrap`, pero en orden inverso.

### Ejemplo:
```css
.container {
    display: flex;
    flex-wrap: wrap;
}
```

---

## 5. `gap`
Define el espacio entre los elementos flexibles dentro del contenedor.

### Valores posibles:
- Un solo valor: Define un espacio uniforme en ambas direcciones.
- Dos valores: El primer valor define el espacio entre filas y el segundo entre columnas.

### Ejemplo:
```css
.container {
    display: flex;
    gap: 20px;
}
```

---

## 1. `body` (Estilos generales)
```css
body {
    font-family: 'Ubuntu', 'Courier New', Courier, monospace;
    color: #023047;
    background-color: #f1f1f1;
    margin: 0px;
    padding: 0px;
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}
```
- Define la fuente del texto con una prioridad (primero *Ubuntu*, si no está disponible, *Courier New*, y así sucesivamente).
- Color del texto: `#023047` (un tono azul oscuro).
- Fondo de la página: `#f1f1f1` (gris claro).
- Elimina los márgenes y el padding por defecto.
- Usa `display: flex` para organizar los elementos en columna.
- `min-height: 100vh;` asegura que el `body` tenga al menos la altura completa de la pantalla.

---

## 2. `header` (Encabezado)
```css
header {
    background-color: #219ebc;
    color: white;
    padding: 20px;
    text-align: center;
}
```
- Fondo azul (`#219ebc`).
- Texto en color blanco.
- Espaciado interno de `20px`.
- Alineación centrada del contenido.

---

## 3. `main` (Sección principal)
```css
main {
    flex: 1;
    padding: 10px 20px;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}
```
- `flex: 1;` permite que ocupe el espacio disponible entre el `header` y el `footer`.
- `padding: 10px 20px;` agrega margen interno.
- `width: 100%;` asegura que ocupe todo el ancho disponible.
- Usa `display: flex` para organizar los elementos en columna y centrarlos.

---

## 4. `#login-box` (Caja del formulario de login)
```css
#login-box {
    background-color: #FFF;
    padding: 20px 40px;
    max-width: 400px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    margin: 0 auto;
    display: flex;
    flex-direction: column;
}
```
- Fondo blanco.
- Espaciado interno `20px 40px`.
- Ancho máximo de `400px`.
- Bordes redondeados (`border-radius: 10px`).
- Sombra ligera (`box-shadow`).
- Se centra horizontalmente (`margin: 0 auto`).
- Organiza su contenido en columna (`display: flex; flex-direction: column;`).

### **Título del login**
```css
#login-box h2 {
    text-align: center;
    margin-bottom: 10px;
}
```
- Centra el texto del título `<h2>`.
- Agrega un pequeño espacio inferior.

---

## 5. Estilos de los `input` (Campos de texto y contraseña)
```css
input[type="text"], input[type="password"] {
    background-color: #FFF;
    border: 2px solid #219ebc;
    color: #023047;
    padding: 10px;
    font-size: 16px;
    border-radius: 5px;
    width: 100%;
    box-sizing: border-box;
    margin-bottom: 20px;
}
```
- Bordes `2px` de color azul (`#219ebc`).
- Color del texto azul oscuro (`#023047`).
- `width: 100%` asegura que ocupe todo el ancho disponible.
- `border-radius: 5px;` para bordes redondeados.
- `box-sizing: border-box;` evita que el `padding` afecte el ancho.

### **Efecto cuando están enfocados (`focus`)**
```css
input[type="text"]:focus, input[type="password"]:focus {
    border-color: #fb8500;
    outline: none;
}
```
- Cuando se selecciona el campo, cambia el borde a naranja (`#fb8500`).
- Elimina el contorno predeterminado (`outline: none;`).

---

## 6. Menú de navegación en el `header`
```css
header > ul {
    display: flex;
}
```
- Usa `display: flex` para organizar los elementos en fila.

```css
header > ul li {
    list-style: none;
    margin: auto;
}
```
- Quita los estilos de lista.
- Centra los elementos con `margin: auto`.

```css
header > ul li a {
    text-decoration: none;
    cursor: pointer;
    color: #FFF;
    font-weight: bolder;
    font-size: 18px;
}
```
- Enlaces sin subrayado.
- Color blanco.
- Texto en negrita y tamaño `18px`.

---

## 7. `footer` (Pie de página)
```css
footer {
    display: flex;
    padding: 20px;
    justify-content: center;
    background-color: #023047;
    color: #FFF;
}
```
- Se alinea el contenido al centro (`justify-content: center`).
- Fondo azul oscuro (`#023047`).
- Texto en color blanco.

### **Iconos en el `footer`**
```css
footer i {
    margin-left: 20px;
    margin-right: 20px;
    font-size: 30px;
}
```
- Agrega separación entre iconos (`margin-left: 20px; margin-right: 20px;`).
- Tamaño del icono `30px`.

---
