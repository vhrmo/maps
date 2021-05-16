# Maps library

Library to help display overlay information over a map of Slovakia.

* [Demo](Demo.md)
* [Documentation on Github pages](https://vhrmo.github.io/maps)
* [Development info](Development.md)

# Nadácia

JavaScript obsahuje štatistické dáta ku dňu: _TODO add_date_tbd_

### Použitie

#### 1. Vložte JS a CSS do hlavičky stránky

```html
<head>

    ...

    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
          integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
          crossorigin=""/>
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
            integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
            crossorigin=""></script>
    <script src="https://cdn.jsdelivr.net/npm/leaflet-labeled-circle@1.0.3/dist/L.LabeledCircle.js"
            integrity="sha256-UKDnk/3X8sl+NLArMauoubVvGlSQ5gHJAP4Na0QzymQ=" crossorigin=""></script>

    <link rel="stylesheet" href="https://vhrmo.github.io/maps/src/nadacia.css" crossorigin=""/>
    <script src="https://vhrmo.github.io/maps/src/nadacia.js" crossorigin=""></script>

    ...

</head>
```

#### 2. Definujte map container v HTML

```html
    <div class="container">
        <div id="map1" class="map"></div>
    </div>
```

Príklad štýlov pre HTML komponenty:

```css
    .container {
        width: 100%;
        padding: 3px;
    }

    .map {
        width: 700px;
        height: 350px;
        margin: 0 auto;
    }
```


#### 3. Pridajte inicializačný skript mapy na koniec BODY elementu

```html

<body>

    ...

    <script>
        createMap('map1', {
            overlays: [districtsOverlay],
            districtsOverlay: {
                method: varSizeCircleLabeledCircle,
                anchorColor: 'none',
                fillOpacity: 0.8
            }
        });
    </script>
</body>


```

