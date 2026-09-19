# Renders Tassaroli

Galería web de los 86 renders del anteproyecto de la **Fundación Tassaroli**
(anteproyecto: Estudio Lucchesi), ordenados por espacio. Sitio estático: no
tiene build ni dependencias.

## Deploy en Vercel

1. En Vercel: **Add New → Project** e importá este repositorio.
2. Framework Preset: **Other**.
3. Build Command: vacío · Output Directory: `.` (la raíz).
4. Deploy.

`vercel.json` ya manda `X-Robots-Tag: noindex, nofollow` en todas las rutas y
cachea `/assets/*` por un año. Junto con `robots.txt`, la galería no se indexa:
entra quien tiene el link o el QR.

## Estructura

| Ruta                | Qué es                                          |
| ------------------- | ----------------------------------------------- |
| `index.html`        | La galería entera: markup, estilos y JS inline. |
| `assets/thumb/*`    | Miniaturas de la grilla (560 px).               |
| `assets/full/*`     | Imagen del visor (1400 px).                     |
| `assets/isotipo-fundacion.png` | Isotipo de la marca.                 |

Los renders originales, en calidad completa, están en Google Drive; cada
imagen del visor enlaza a su archivo.

## Marca

Paleta, tipografías y lockup tomados del sistema del sitio de la Fundación:
papel `#FAF9F6`, tinta `#14213D`, azul `#2563EB`, Archivo para texto y
Martian Mono sólo para datos.
