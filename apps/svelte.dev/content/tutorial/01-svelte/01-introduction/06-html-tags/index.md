<!-- ---
title: HTML tags
--- -->
---
title: Etiquetas HTML
---
<!-- TODO: anglicism blob -->
<!-- Ordinarily, strings are inserted as plain text, meaning that characters like `<` and `>` have no special meaning. -->
Comúnmente, las cadenas de caracteres se insertan como texto plano, lo que significa que caracteres como `<` o `>` no tienen especial significado.

<!-- But sometimes you need to render HTML directly into a component. For example, the words you're reading right now exist in a markdown file that gets included on this page as a blob of HTML. -->
Pero en ocasiones necesitas plasmar HTML directamente en un componente. Por ejemplo, lo que estás leyendo ahora mismo existe en un archivo de markdown que se inserta en esta página como un *blob* de HTML

<!-- In Svelte, you do this with the special `{@html ...}` tag: -->
En Svelte, se puede hacer usando la etiqueta especial `{@html ...}`:

<!-- ```svelte
/// file: App.svelte
<p>{+++@html+++ string}</p>
``` -->
```svelte
/// archivo: App.svelte
<p>{+++@html+++ string}</p>
```

<!-- > [!NOTE] Important: Svelte doesn't perform any sanitization of the expression inside `{@html ...}` before it gets inserted into the DOM. This isn't an issue if the content is something you trust like an article you wrote yourself. However if it's some untrusted user content, e.g. a comment on an article, then it's critical that you manually escape it, otherwise you risk exposing your users to <a href="https://owasp.org/www-community/attacks/xss/" target="_blank">Cross-Site Scripting</a> (XSS) attacks. -->
[!NOTE] Importante: Svelte no realiza ningún tipo de sanitización de la expresión dentro de `{@html ...}` antes de ser insertada en el DOM. Esto no es problemático si puedes confiar en el contenido creado por ti. No obstante, si el contenido no es de una fuente fiable, por ejemplo, comentarios creados por usuarios en un artículo, entonces es de vital importancia que se escapen dichos símbolos de manera manual, de lo contrario podrías exponer a tus usuarios a ataques del tipo <a href="https://owasp.org/www-community/attacks/xss/" target="_blank">Cross-Site Scripting</a> (XSS).