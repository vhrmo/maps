---
title: Nadácia - demo máp
---

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css"
      integrity="sha512-xodZBNTC5n17Xt2atTPuE1HxjVMSvLVW9ocqUKLsCC5CXdbqCmblAshOMAS6/keqq/sMZMZ19scR4PsZChSR7A=="
      crossorigin=""/>
<script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"
        integrity="sha512-XQoYMqMTK8LvdxXYG3nZ448hOEQiglfqkJs1NOQV44cWnUrBc8PkAOcXy20w0vlaXaVUearIOBhiXZ5V3ynxwA=="
        crossorigin=""></script>
<script src="https://cdn.jsdelivr.net/npm/leaflet-labeled-circle@1.0.3/dist/L.LabeledCircle.js"
        integrity="sha256-UKDnk/3X8sl+NLArMauoubVvGlSQ5gHJAP4Na0QzymQ=" crossorigin=""></script>

<link rel="stylesheet" href="src/nadacia.css" crossorigin=""/>
<script src="src/nadacia.js" crossorigin=""></script>

<style>
    .container {
        width: 100%;
        padding: 3px;
        /*display: inline-flex;*/
    }

    .map {
        width: 700px;
        height: 350px;
        margin: 0 auto;
    }
</style>

# Počty pacientov po krajoch
* Veľkosť mapy je možné prispôsobiť.
* Mapu je možné vložiť do existujúcej stránky.
* Všetky farby je možné zmeniť / prispôsobiť cieľovej stránke kde bude mapa umiestnená.

[comment]: <> (================================================================================)

## Príklad 1
```javascript
    createMap('map1', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors1
        },
        regionalCounts: {
            method: addInfoLabeledCircle
        }
    });
```

<div class="container">
    <div id="map1" class="map"></div>
</div>

<script>
    createMap('map1', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors1
        },
        regionalCounts: {
            method: addInfoLabeledCircle
        }
    });
</script>


[comment]: <> (================================================================================)

## Príklad 2
```javascript
    createMap('map2', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors2
        },
        regionalCounts: {
            method: addInfoDivIcon
        }
    });
```

<div class="container">
    <div id="map2" class="map"></div>
</div>

<script>
    createMap('map2', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors2
        },
        regionalCounts: {
            method: addInfoDivIcon
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 3
```javascript
    createMap('map3', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors3
        },
        regionalCounts: {
            method: addInfoSvgOverlay
        }
    });
```

<div class="container">
    <div id="map3" class="map"></div>
</div>

<script>
    createMap('map3', {
        overlays: [regionsOverlay, regionalCounts],
        regionsOverlay: {
            colorScheme: regionColors3
        },
        regionalCounts: {
            method: addInfoSvgOverlay
        }
    });
</script>

# Počty pacientov po okresoch

* Veľkosť mapy je možné prispôsobiť.
* Mapu je možné vložiť do existujúcej stránky.
* Všetky farby je možné zmeniť / prispôsobiť cieľovej stránke kde bude mapa umiestnená.
* Pri prechode myšou ponad číslo sa zobrazí tooltip s názvom okresu.


[comment]: <> (================================================================================)

## Príklad 4
```javascript
    createMap('map4', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleLabeledCircle,
            anchorColor: 'none',
            fillOpacity: 0.8
        }
    });
```

<div class="container">
    <div id="map4" class="map"></div>
</div>

<script>
    createMap('map4', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleLabeledCircle,
            anchorColor: 'none',
            fillOpacity: 0.8
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 5
```javascript
    createMap('map5', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleLabeledCircle,
            color: '#fca001',
            anchorColor: 'none'
        }
    });
```

<div class="container">
    <div id="map5" class="map"></div>
</div>

<script>
    createMap('map5', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleLabeledCircle,
            color: '#fca001',
            anchorColor: 'none'
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 6
```javascript
    createMap('map6', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon
        }
    });
```

<div class="container">
    <div id="map6" class="map"></div>
</div>

<script>
    createMap('map6', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 7
```javascript
    createMap('map7', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon,
            outerCircleStyle: 'map-marker-circle-outer',
            innerCircleStyle: 'none'
        }
    });
```

<div class="container">
    <div id="map7" class="map"></div>
</div>

<script>
    createMap('map7', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon,
            outerCircleStyle: 'map-marker-circle-outer',
            innerCircleStyle: 'none'
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 8
```javascript
    createMap('map8', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon,
            outerCircleStyle: 'map-marker-circle-outer-red',
            innerCircleStyle: 'none'
        }
    });
```

<div class="container">
    <div id="map8" class="map"></div>
</div>

<script>
    createMap('map8', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: varSizeCircleDivIcon,
            outerCircleStyle: 'map-marker-circle-outer-red',
            innerCircleStyle: 'none'
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 9
```javascript
    createMap('map9', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoLabeledCircle,
            radius: 13
        }
    });
```

<div class="container">
    <div id="map9" class="map"></div>
</div>

<script>
    createMap('map9', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoLabeledCircle,
            radius: 13
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 10
```javascript
    createMap('map10', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoDivIcon,
            outerCircleStyle: 'map-marker-circle2-smaller',
            innerCircleStyle: 'map-marker-circle3-smaller'
        }
    });
```

<div class="container">
    <div id="map10" class="map"></div>
</div>

<script>
    createMap('map10', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoDivIcon,
            outerCircleStyle: 'map-marker-circle2-smaller',
            innerCircleStyle: 'map-marker-circle3-smaller'
        }
    });
</script>

[comment]: <> (================================================================================)

## Príklad 11
```javascript
    createMap('map11', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoSvgOverlay
        }
    });
```

<div class="container">
    <div id="map11" class="map"></div>
</div>

<script>
    createMap('map11', {
        overlays: [districtsOverlay],
        districtsOverlay: {
            method: addInfoSvgOverlay
        }
    });
</script>


