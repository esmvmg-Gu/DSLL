# Días con y sin lluvia

Aplicación web que cuenta los días con lluvia y sin lluvia de estaciones climáticas:

- **Automáticas** (archivos .txt de WeatherLink): suma las lecturas de cada día.
- **Convencionales** (descarga del formulario en .xlsx o .csv): usa la "Lluvia total" de las 7:00.

Funciona en el navegador, se puede instalar como aplicación en la computadora o el celular y sirve sin internet.

## Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `dias-lluvia`).
2. Sube **todo el contenido de esta carpeta** a la raíz del repositorio, incluida la carpeta `icons` y el archivo `.nojekyll`.
   - Desde la web: *Add file → Upload files*, arrastra los archivos y luego *Commit changes*.
3. Ve a **Settings → Pages**.
4. En *Build and deployment*, en *Source* elige **Deploy from a branch**. Luego elige la rama `main` y la carpeta `/ (root)`, y presiona **Save**.
5. En uno o dos minutos la app queda en `https://TU-USUARIO.github.io/dias-lluvia/`.

## Instalar la aplicación

- **Computadora (Chrome o Edge):** abre la dirección y presiona el botón **Instalar aplicación** que aparece arriba. También puedes usar el ícono de instalar en la barra de direcciones.
- **Android (Chrome):** presiona **Instalar aplicación**, o abre el menú ⋮ y elige *Instalar aplicación* / *Agregar a pantalla principal*.
- **iPhone o iPad (Safari):** toca **Compartir** y luego **Agregar a pantalla de inicio**.

## Actualizar la aplicación

Cuando cambies `index.html` (por ejemplo, con datos nuevos incluidos), súbelo de nuevo a GitHub y cambia la versión en `sw.js`:

```js
const VERSION = 'lluvia-v2';   // antes 'lluvia-v1'
```

Con conexión, la app instalada carga la versión nueva la próxima vez que se abre.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La aplicación, con los datos de las estaciones incluidos |
| `manifest.webmanifest` | Nombre, colores e íconos para instalarla |
| `sw.js` | Permite usarla sin internet |
| `xlsx.full.min.js` | Lector y generador de Excel ([SheetJS](https://sheetjs.com), licencia Apache 2.0) |
| `icons/` | Íconos de la aplicación |

Nota: los archivos que subas dentro de la app no se guardan en GitHub. Solo se usan en esa sesión del navegador.
