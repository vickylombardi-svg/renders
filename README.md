# Renders Tassaroli

Galería web de los 86 renders del anteproyecto de la **Fundación Tassaroli**
(anteproyecto: Estudio Lucchesi), ordenados por espacio. Sitio estático: no
tiene build ni dependencias.

## Deploy

Sitio estático: sin build, sin dependencias. Publicar la raíz del repo.

**Netlify** (donde está hoy): `netlify.toml` fija `publish = "."` y los
headers. Dos ajustes que NO viven en el repo y se tocan en el panel:

- *Site configuration → Access & security → Visitor access*: tiene que estar
  en **Public**. Si queda protegido, Netlify devuelve 401 y manda a
  `app.netlify.com/edge-access`: el visitante necesitaría cuenta de Netlify.
- *Site configuration → Site details → Change site name*: define el subdominio,
  que es lo que queda impreso en el QR. Cambiarlo después rompe los QR ya
  impresos.

**Vercel**: `vercel.json` cubre el mismo caso (Framework Preset `Other`,
Output Directory `.`). Los dos archivos pueden convivir.

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
