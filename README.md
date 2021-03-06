*ReadMe entrega desafío SEO - Felipe Uribe Herrera*

### Índice
- [Optimizaciones SEO](#optimizaciones-seo)
    * [Index](#index)
    * [Resto de páginas](#resto-de-páginas)
- [Uso de SASS](#uso-de-sass)
    * [@extend](#extend)
    * [Mapas](#mapas)
    * [@mixin](#mixins)
- [FAVICON](#favicon)

# Optimizaciones SEO:

## Index

```html
Meta tags base, los cuales se van a repetir y modificar mínimamente en el resto de las páginas.

<meta name="Keywords" content="Soluciones Nutricionales, Viandas, Viandas saludables, Sano, Rico, Nutrititvo">

<meta name="description" content="Inicio de mi página web, viandas saludables para empresas y particulares">

<title>Soluciones Nutricionales - Home</title>
```
[`volver al índice`](#índice)

## Resto de páginas

Modificaciones y agregados en el index:
- cambios en los títulos para tener relación con la página.
- cambios en el meta name='title' para tener relación con la página.
- cambios en el meta name='description' para tener relación con la página (ejemplificados abajo).
- se agregaron los siguentes *keywords* en las paginas:

```html
<!-- nosotros.html -->
<meta name="Keywords" content="Cocinero, Cocina, Equipo de cocina, Viandas, Viandas para empresas, Quienes somos">

<meta name="description" content="Nuestro equipo de cocina, quienes somos">

<!-- hace-tu-pedido.html -->
<meta name="Keywords" content="Menú, Pedido, Precios accesibles, Viandas saludables, Viandas">

<meta name="description" content="Generá tu pedido con las viandas que más te gusten">

<!-- servicios.html -->
<meta name="Keywords" content="Pack de viandas, Comida saludable, Viandas, Servicios">

<meta name="description" content="Servicio de viandas, packs de viandas y opciones saludables">
```
[`volver al índice`](#índice)

# Uso de SASS

## Extend
Usé @extend para setear
```scss
//----  variables
.btn-primary {
        @extend .boton;
        }
``` 
[`volver al índice`](#índice)

## MAPAS
Use mapas para los colores de mis iconos en mis redes sociales dentro de todos mis footer en los html.
```scss
$redes: (
    facebook: #3b5999,
    instagram: #e4405f,
    twitter: #55acee,
    pinterest: #bd081c,
    linkedin: #0077B5,
);

@each $red,
$color in $redes {
    .red-#{$red} {
        color: $color;
        display: inline-block;
        margin: 0 5px;
        width: 100px;
        height: 100px;
        text-align: center;
    }
}
```
[`volver al índice`](#índice)

## MIXINS
Utilicé @mixin para aplicar en encabezados de h1, h2 y h3 adaptandolo a media queries.

```scss
// en _variables.scss
@mixin encabezados {
    h1 {
        font-size: 1.5em;
    }

    h2 {
        font-size: 1.2em;
    }

    h3 {
        font-size: 1em;
    }
}

@mixin encabezados($tamaño) {
    h1 {
        font-size: $tamaño;
    }

    h2 {
        font-size: $tamaño - 0.2;
    }

    h3 {
        font-size: $tamaño - 0.5;
    }
}

@include encabezados(2em);

@include encabezados(1.5em);

@media(min-width: 480px) {
    @include encabezados(2em);
}

@media(min-width: 768px) {
    @include encabezados(2.5em);
}
```

# FAVICON
## Imagen y herramientas utilizadas
Imagen de logo: <br>
```html
<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">
<link rel="icon" href="./pages/img/favicon.ico" type="image/x-icon" sizes="16x16">
```

La foto la convertí en .ico usando [Favicon Generator](https://www.favicon-generator.org) y los apliqué en los html.

[`volver al índice`](#índice)