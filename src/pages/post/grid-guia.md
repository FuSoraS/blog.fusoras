---
layout: ../../layouts/MarkdownLayout.astro
title: Uso de grid para card
Description:
author: FuSoraS
---
[Repositorio en GitHub](https://github.com/FuSoraS/explicaciones-rapidas)
- `display: grid` Cambiamos el modo de la etiqueta `section` a grid esto nos permite usar columnas y filas.
- `grid-template-columns: repeat(3, 1fr);` Definimos `3` columnas, `1fr` definimos que las 3 columnas tienen que ocupar el mismo espacio
- `width: 150px` definimos el ancho del contenedor
```css
section {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    width: 150px;
}
```
- `text-align` centramos el texto
- `padding: 10px` definimos la separacion entre las card.
```css
div {
    background-color: #fff;
    padding: 10px;
    text-align: center;
}
```
- `margin: 0;` quitamos la separacion entre el parrafo y la imagen
- `padding: 5px` creamos un espacio de `5px` del fondo rojo para que se vea mas bonito
```css
p {
    width: 150px;
    color: white;
    background-color: red;
    margin: 0;
    padding: 5px;
}
```

Definimos que va a ocupar todo el ancho y altura de `section` que tiene un ancho de `150px` por lo tanto tiene ese tamaño
```css
img {
    height: 100%;
    width: 100%;
}
```