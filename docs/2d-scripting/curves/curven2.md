# CURVE_N2

<code>CURVE_N2</code> erzeugt eine NURBS-Kurve mit <code>n</code> Kontrollpunkten. Diese Kurve wird von Allplan als Polygon gezeichnet, die Anzahl der berechneten Punkte kann über die Direktiven <code>RESOL</code> und <code>RISE</code> gesteuert werden.

| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1 + j2 + j3</code> Darstellungsoptionen |
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|

- <code>j1 = 1</code>: Umrisslinie darstellen
- <code>j1 = 2</code>: Füllung darstellen
- <code>j1 = 4</code>: geschlossene Kurve, erster und letzter Punkt wird verbunden.


## Smartpart
```smartpart
CURVE_N2 n, status, x1, y1, ..., xn, yn
```

