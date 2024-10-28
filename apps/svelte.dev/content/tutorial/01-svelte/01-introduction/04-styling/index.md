<!-- ---
title: Styling
--- -->
---
title: Aplicando estilo
---


<!-- Just like in HTML, you can add a `<style>` tag to your component. Let's add some styles to the `<p>` element: -->
Al igual que con el HTML, puedes añadir una etiqueta de `<style>` al componente. Añadamos algo de estilo al elemento `<p>`:

<!-- ```svelte
/// file: App.svelte
<p>This is a paragraph.</p>

<style>
+++ p {
        color: goldenrod;
        font-family: 'Comic Sans MS', cursive;
        font-size: 2em;
    }+++
</style>
``` -->
```svelte
/// archivo: App.svelte
<p>Esto es un parrafo.</p>

<style>
+++ p {
        color: goldenrod;
        font-family: 'Comic Sans MS', cursive;
        font-size: 2em;
    }+++
</style>
```
<!-- Importantly, these rules are _scoped to the component_. You won't accidentally change the style of `<p>` elements elsewhere in your app, as we'll see in the next step. -->

Es importante mencionar, que el estilo _está limitado al alcance del componente_. No cambiarás accidentalmente el estilo de otros elementos `<p>` en otras partes de tu aplicación como veremos en el siguiente paso.