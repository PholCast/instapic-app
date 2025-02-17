# instapic-app

# Guía sobre Estilos en CSS

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
