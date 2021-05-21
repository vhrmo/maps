---
title: Nadácia - demo máp
layout: nadacia_demo
---

## Počty pacientov po krajoch
* Veľkosť mapy je možné prispôsobiť.
* Mapu je možné vložiť do existujúcej stránky.
* Všetky farby je možné zmeniť / prispôsobiť cieľovej stránke kde bude mapa umiestnená.

[comment]: <> (================================================================================)

### Príklad 1
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

### Príklad 2
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

### Príklad 3
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

## Počty pacientov po okresoch

* Veľkosť mapy je možné prispôsobiť.
* Mapu je možné vložiť do existujúcej stránky.
* Všetky farby je možné zmeniť / prispôsobiť cieľovej stránke kde bude mapa umiestnená.
* Pri prechode myšou ponad číslo sa zobrazí tooltip s názvom okresu.


[comment]: <> (================================================================================)

### Príklad 4
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

### Príklad 5
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

### Príklad 6
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

### Príklad 7
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

### Príklad 8
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

### Príklad 9
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

### Príklad 10
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

### Príklad 11
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


