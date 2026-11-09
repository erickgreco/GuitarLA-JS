# GuitarLA

Tienda en línea de guitarras con carrito de compra, desarrollada con React, JavaScript y Vite.

**Demo:** https://guitarla-js-erickgreco.netlify.app/

## Funcionalidades

- Catálogo de guitarras con imagen, descripción y precio.
- Agregar productos al carrito.
- Aumentar y disminuir la cantidad de cada producto.
- Eliminar productos o vaciar el carrito.
- Cálculo automático del total.
- Persistencia del carrito en `localStorage`.

## Stack

| Área                 | Tecnología        |
| -------------------- | ----------------- |
| UI                   | React             |
| Lenguaje             | JavaScript (ES6+) |
| Bundler / Dev server | Vite              |
| Estilos              | CSS (`index.css`) |
| Despliegue           | Netlify           |
| Control de versiones | Git + GitHub      |

## Arquitectura

La lógica del carrito está separada de la interfaz: los componentes solo renderizan y la lógica de estado vive en un hook personalizado.

| Archivo                     | Responsabilidad                                                                     |
| --------------------------- | ----------------------------------------------------------------------------------- |
| `src/main.jsx`              | Punto de entrada; monta la aplicación en el DOM                                     |
| `src/App.jsx`               | Componente raíz; consume `useCart` y distribuye datos y funciones a los componentes |
| `src/components/Header.jsx` | Encabezado y vista del carrito                                                      |
| `src/components/Guitar.jsx` | Tarjeta de producto del catálogo                                                    |
| `src/hooks/useCart.js`      | Hook personalizado con el estado y las operaciones del carrito                      |
| `src/data/db.js`            | Catálogo de guitarras (datos locales)                                               |
| `src/index.css`             | Estilos globales                                                                    |

## Ejecutar en local

Requisitos: Node.js (versión LTS) y npm.

```bash
git clone git@github.com:erickgreco/GuitarLA-JS.git
cd GuitarLA-JS
npm install
npm run dev
```

Scripts disponibles:

| Comando           | Descripción                                    |
| ----------------- | ---------------------------------------------- |
| `npm run dev`     | Servidor de desarrollo con recarga en caliente |
| `npm run build`   | Genera el build de producción en `dist/`       |
| `npm run preview` | Sirve localmente el build de producción        |

## Despliegue

El sitio se despliega en Netlify, conectado a este repositorio: cada `push` a `main` dispara un deploy automático.

| Configuración     | Valor           |
| ----------------- | --------------- |
| Build command     | `npm run build` |
| Publish directory | `dist`          |

## Autor

**Erick Gutierrez Sanchez**
GitHub: [@erickgreco](https://github.com/erickgreco)
