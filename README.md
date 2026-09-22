# DIJUL

Acertijo interactivo de tres sellos que termina en un poema. Es una pagina estatica: sin backend, sin base de datos y sin paso de compilacion.

## Uso

Abrir `index.html` en el navegador, o servir la carpeta por HTTP:

```
python -m http.server 8000
```

## Flujo

1. Portal de entrada.
2. Tres sellos; cada respuesta correcta descifra una llave del candado.
3. Poema final con el jardin de flores amarillas.

En movil, el acertijo muestra un teclado propio en pantalla que cambia entre numerico y de texto segun el sello.

## Estructura

| Archivo | Rol |
| --- | --- |
| `index.html` | Estructura, estilos y logica |
| `flowers.css` | Escena de flores amarillas |
| `fl.mp3` | Musica de fondo |
| `script.js` | Quita la clase de carga inicial |
| `flores-amarillas.markdown` | Atribucion del diseno de flores (CodePen) |

## Configuracion

- Respuestas, pistas y frases de cada sello: objeto `riddleStepsData` en `index.html`.
- Teclado por sello: campo `keyboard` (`numeric` o `text`) dentro de ese mismo objeto.
- La pagina carga Google Fonts; sin conexion usa las tipografias del sistema.

## Creditos

El diseno de las flores amarillas proviene de un CodePen de Edward Ruiz. Detalle en `flores-amarillas.markdown`.
