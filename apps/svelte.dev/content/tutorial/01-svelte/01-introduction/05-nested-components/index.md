<!-- ---
title: Nested components
--- -->
---
title: Componentes anidados
---

<!-- It would be impractical to put your entire app in a single component. Instead, we can import components from other files and include them in our markup. -->
No sería práctico poner la aplicación entera en un único componente. En su lugar, podemos importar componentes de otros archivos e incluirlos en nuestro html.

<!-- Add a `<script>` tag to the top of `App.svelte` that imports `Nested.svelte`... -->
Incluye la etiqueta `<script>` al inicio de `App.svelte` e importa `Nested.svelte`...

<!-- ```svelte
/// file: App.svelte
+++<script>
    import Nested from './Nested.svelte';
</script>+++
``` -->
```svelte
/// archivo: App.svelte
+++<script>
    import Nested from './Nested.svelte';
</script>+++
```

<!-- ...and include a `<Nested />` component: -->
... y añade el componente `<Nested />`:

<!-- ```svelte
/// file: App.svelte
<p>This is a paragraph.</p>
+++<Nested />+++
``` -->
```svelte
/// archivo: App.svelte
<p>Esto es un parrafo.</p>
+++<Nested />+++
```

<!-- Notice that even though `Nested.svelte` has a `<p>` element, the styles from `App.svelte` don't leak in. -->
Fíjate que aunque `Nested.svelte` tiene un elemento `<p>`, los estilos aplicados en `App.svelte` no se propagan.

<!-- > [!NOTE] Component names are capitalised, to distinguish them from HTML elements. -->
[!NOTE] Los nombres de los componentes se capitalizan para distinguirlos de los elementos nativos de HTML.