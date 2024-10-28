<!-- ---
title: Dynamic attributes
--- -->
---
title: Atributos dinámicos
---

<!-- Just like you can use curly braces to control text, you can use them to control element attributes. -->
Al igual que puedes usar llaves `{ }` para controlar texto, tambien puedes usarlas para controlar los atributos de los elementos.

<!-- Our image is missing a `src` — let's add one: -->
Nuestra imagen echa en falta una fuente `src` - añadámosla:

<!-- ```svelte
/// file: App.svelte
<img +++src={src}+++ />
``` -->
```svelte
/// archivo: App.svelte
<img +++src={src}+++ />
```

<!-- That's better. But if you hover over the `<img>` in the editor, Svelte is giving us a warning: -->
Eso está mejor. Sin embargo, si pasas el cursor sobre el elemento `<img>` en el editor, Svelte nos hará una advertencia: 

```
`<img>` element should have an alt attribute
```
*El elemento `<img>` debería contener el atributo `alt`

<!-- When building web apps, it's important to make sure that they're _accessible_ to the broadest possible userbase, including people with (for example) impaired vision or motion, or people without powerful hardware or good internet connections. Accessibility (shortened to a11y) isn't always easy to get right, but Svelte will help by warning you if you write inaccessible markup. -->
Al construir aplicaciones web, es importante asegurarse que sean accesibles para el mayor numero de usuario posibles, incluyendo gente (por ejemplo) que tenga visión o movilidad limitada, gente sin hardware potente o una buena conexión a internet. La accesibilidad (conocida como a11y) no es siempre fácil de conseguir correctamente, pero Svelte ayudará advirtiéndote si estás escribiendo html no accesible.

<!-- In this case, we're missing the `alt` attribute that describes the image for people using screenreaders, or people with slow or flaky internet connections that can't download the image. Let's add one: -->
En este caso, echamos en falta el atributo `alt` que sirve para describir una imagen para gente usando lectores de pantalla, o para aquellos con conexiones de internet inconsistentes que no pudieron descargar la imagen. Añadamos el atributo:

<!-- ```svelte
/// file: App.svelte
<img src={src} +++alt="A man dances."+++ />
``` -->
```svelte
/// archivo: App.svelte
<img src={src} +++alt="Un hombre bailando."+++ />
```

<!-- We can use curly braces _inside_ attributes. Try changing it to `"{name} dances."` — remember to declare a `name` variable in the `<script>` block. -->
Podemos usar llaves `{}` _dentro_ de los atributos. Prueba a cambiarlo a `"{nombre} bailando."` - recuerda declarar la variable `nombre` en el bloque `<script>`

<!-- ## Shorthand attributes -->
## Atajos en atributos

<!-- It's not uncommon to have an attribute where the name and value are the same, like `src={src}`. Svelte gives us a convenient shorthand for these cases: -->
No es inusual tener atributos y variables con el mismo nombre, como por ejemplo `src={src}`. Svelte nos proporciona una conveniente atajo para estos casos.

<!-- ```svelte
/// file: App.svelte
<img +++{src}+++ alt="{name} dances." />
``` -->
```svelte
/// archivo: App.svelte
<img +++{src}+++ alt="{nombre} bailando." />
```