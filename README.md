# Ventana — Repositorio de formación en Neurología Vascular

Sitio estático. No necesita servidor, base de datos ni instalación.

## Publicar en GitHub Pages

1. Crea un repositorio público en github.com (por ejemplo `ventana`).
2. Sube **todos** los archivos de esta carpeta (arrástralos a la ventana del repositorio) y pulsa *Commit*.
3. Ve a *Settings › Pages*. En *Source* elige `Deploy from a branch`, rama `main`, carpeta `/ (root)`. Guarda.
4. A los dos minutos la web está en `https://TUUSUARIO.github.io/ventana/`.

## Dominio propio (opcional, ~10-12 €/año)

En tu registrador, crea cuatro registros A apuntando a:

    185.199.108.153
    185.199.109.153
    185.199.110.153
    185.199.111.153

Luego, en *Settings › Pages › Custom domain*, escribe el dominio y marca *Enforce HTTPS*.

## Editar el contenido

Todo el contenido está en `index.html`. Ábrelo en GitHub, pulsa el lápiz, cambia el texto y haz *Commit*: la web se actualiza sola en un minuto.

Las listas de contenido están en la parte final del archivo, dentro de la clase `Component`:

| Qué quieres cambiar    | Busca          |
|------------------------|----------------|
| Próximas sesiones      | `v.agenda`     |
| Entradas del blog      | `v.posts`      |
| Protocolos             | `v.protocolos` |
| Casos clínicos         | `v.casos`      |
| Cursos y vídeos        | `v.courses`    |
| Enlaces de interés     | `v.linkGroups` |
| Bibliografía comentada | `v.bibEntries` |

Para añadir un elemento, duplica un bloque `{ ... }` de la lista y cambia su texto. Respeta las comas entre bloques.

Los textos de cabecera, títulos de sección y pies están al principio del mismo bloque, en el objeto `T`, con su versión en español y en inglés.

El artículo completo del blog está escrito directamente como texto en la parte de arriba del archivo, dentro del bloque que empieza por `<sc-if value="{{ isArticle }}">`.

## Imágenes

Se suben con *Add file › Upload files* y se referencian por su nombre, por ejemplo `<img src="./mi-figura.png" />`.

## Archivos

- `index.html` — la web entera: contenido, diseño y calculadoras
- `support.js` — motor necesario para que la página funcione; no hay que tocarlo
- `logo-sna.png` — logo de la cabecera
- `aspects-ganglionic-clean.png`, `aspects-supraganglionic-clean.png` — esquemas de la calculadora ASPECTS
- `fig1` a `fig4` — figuras del artículo de isquemia medular

## Licencia

Contenido bajo CC BY-NC-SA 4.0. Las figuras 1 y 4 del artículo de isquemia medular son © de sus editores y se reproducen con fines docentes.
