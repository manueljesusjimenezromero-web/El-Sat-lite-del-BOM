# Análisis: identificación de objetos predefinidos (Criterio a)

## 1. `window` frente a objetos nativos como `Math` o `JSON`

`window` es el objeto global del **BOM** (Browser Object Model). Pertenece al navegador, no al lenguaje: representa la ventana y da acceso a `document`, `location`, `history`, `navigator`, `screen`, `setTimeout()`, `open()`, etc. Fuera del navegador no existe.

`Math` y `JSON` son **objetos nativos del lenguaje**. Existen en cualquier entorno que ejecute JavaScript.

**¿Por qué no hace falta escribir `window.Math`?** En el navegador, `window` es el objeto global, y todo lo definido en el ámbito global cuelga de él. Al escribir `Math`, el motor lo busca en el ámbito global y lo encuentra, así que el prefijo `window.` es opcional.

## 2. Clasificación de las instrucciones

| Instrucción | Categoría | Motivo |
|---|---|---|
| `window.open()` | **BOM** | Método de `window` que abre una ventana del navegador. |
| `parseFloat()` | **Objeto nativo de JS** | Función global definida por el estándar ECMAScript. |
| `Math.floor()` | **Objeto nativo de JS** | Método del objeto nativo `Math`. |
| `navigator.userAgent` | **BOM** | Propiedad del objeto `navigator`. |
