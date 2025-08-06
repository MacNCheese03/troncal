# [Diseño y visualización de información](https://github.com/profesorfaco/troncal/) → Clase 07 → 30 de septiembre

### Presentando datos con HTML y (un `fetch` de) JavaScript

A los perritos se les adiestran en inglés. El `fetch` implica, para el perrito adiestrado, el deber de ir a buscar algo que ya se lanzó.

En línea, con GitHub o servicios tales como https://myjson.online/, usted puede lanzar un JSON. 

Al lenguaje de programación JavaScript le podría pedir, tal como a un perrito adiestrado, que para llenar una variable vaya a buscar un JSON:

```
var perrito = await fetch("https://raw.githubusercontent.com/profesorfaco/troncal/main/clase-07/datos.json");
```

Al mismo lenguaje de programación le podría indicar que trate a lo que ha llenado la variable como un documento de intercambio ligero de datos basado en la notación de objetos de JavaScript, para luego imprimirlo en la consola:

```
var perrito = await fetch("https://raw.githubusercontent.com/profesorfaco/troncal/main/clase-07/datos.json");
var data = await perrito.json();
console.log(data);
```

Este lenguaje de programación podría ser incluido entre etiquetas que así lo marquen, como embebido entre definiciones de hypertexto, quedando en: 

```
<script>
var perrito = await fetch("https://raw.githubusercontent.com/profesorfaco/troncal/main/clase-07/datos.json");
var data = await perrito.json();
console.log(data);
</script>
```




 y un contexto de función asincrónica, siendo el marcado `<script>…</script>` que corresponde al modo en que el lenguaje de descripción HTML le indica a un navegador que lea otro lenguaje, que no se limita a la descripción sino que crece a la programación.



_ _ _ _ 

[clase-06](https://github.com/profesorfaco/troncal/blob/main/clase-06/README.md) ⇆ [clase-08](https://github.com/profesorfaco/troncal/blob/main/clase-08/README.md)
