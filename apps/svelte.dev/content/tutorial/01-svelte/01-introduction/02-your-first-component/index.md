<!-- ---
title: Your first component
--- -->
---
title: Tu primer componente
---

<!-- In Svelte, an application is composed from one or more _components_. A component is a reusable self-contained block of code that encapsulates HTML, CSS and JavaScript that belong together, written into a `.svelte` file. The `App.svelte` file, open in the code editor to the right, is a simple component. -->
En Svelte, una aplicación se compone de uno o más _componentes_. Un componente es un bloque de código autocontenido y reusable que encapsula el HTML, CSS y Javascript pertenecientes al componente en un mismo archivo `.svelte`.

<!-- ## Adding data -->
##Añadiendo datos
<!-- TODO: anglicism markup html -->
<!-- A component that just renders some static markup isn't very interesting. Let's add some data. -->
Un componente que dibuje en pantalla contenido estático no es muy interesante. Añadamos algunos datos.

<!-- First, add a script tag to your component and declare a `name` variable: -->
Primero, añade la etiqueta `<script>` a tu componente y declara una variable `nombre`:

<!-- ```svelte
/// file: App.svelte
+++<script>
    let name = 'Svelte';
</script>+++

<h1>Hello world!</h1>
``` -->
```svelte
/// archivo: App.svelte
+++<script>
    let nombre = "svelte"
</script>+++

<h1>Hola mundo!</h1>
```
<!-- Then, we can refer to `name` in the markup: -->
A continuación, podemos referirnos a `nombre` en el código html.

<!-- ```svelte
/// file: App.svelte
<h1>Hello +++{name}+++!</h1>
``` -->
```svelte
/// archivo: App.svelte
<h1>Hola +++{nombre}+++!</h1>
```
<!-- TODO: anglicism {} llaves -->
<!-- Inside the curly braces, we can put any JavaScript we want. Try changing `name` to `name.toUpperCase()` for a shoutier greeting. -->
Podemos poner el Javascript que queramos dentro de las llaves `{ }`. Prueba a cambiar `nombre` por `nombre.toUpperCase()` para enfatizar el saludo.
<!-- ```svelte
/// file: App.svelte
<h1>Hello {name+++.toUpperCase()+++}!</h1>
``` -->
```svelte
/// archivo: App.svelte
<h1>Hola {nombre+++.toUpperCase()+++}!</h1>
```