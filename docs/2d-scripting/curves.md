# Kurven

## SPLINE2
Erzeugt einen Spline mit *n* Kontrollpunkten, die Tangentenwinkel in den Kontrollpunkten müssen angegeben werden. Tangentenwinkel starten in der lokalen X-Achse und laufen gegen den Uhrzeigersinn.

### Smartpart
```
SPLINE2 n, status, x1, y1, angle1, ..., xn, yn, anglen
```
### Pythonpart
```python
import NemAll_Python_Geometry as AllplanGeo
```

|Symbol|Beschreibung|
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1</code> + <code>j2</code> Spline Eigenschaften|
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|
|<code>anglei</code>|Tangentenwinkel der Kurve|

- <code>j1 = 1</code>: Spline ist geschlossen, erster und letzter Kontrollpunkt werden verbunden. Funktioniert in der Version 2013 leider nicht, wird aber in der nächsten Version korrigiert.
- <code>j2 = 2</code>: Spline automatisch glätten, angegebene Tangentenwinkel werden ignoriert

## SPLINE2_A
<code>SPLINE2_A</code> ist eine Erweiterung des <code>SPLINE2</code> Befehls und erzeugt Bezier-Splines mit <code>n</code> Kontrollpunkten, Tangentenwinkel und Tangentenlängen müssen angegeben werden.

```
SPLINE2 n, status, x1, y1, angle1, len_prev1, len_next1, ..., xn, yn, anglen, len_prevn, len_nextn
```

| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1</code> + <code>j2</code> Spline Eigenschaften|
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|
|<code>anglei</code>|Tangentenwinkel der Kurve|
|<code>len_previ</code> | Länge der Tangente **vor** dem Kontrollpunkt |
|<code>len_nexti</code> | Länge der Tangente **nach** dem Kontrollpunkt |

## CURVE_B2
<code>CURVE_B2</code> erzeugt eine Bezierkurve mit <code>n</code> Kontrollpunkten, die Form der Bezierkurve wird über Tangentenpunkte gesteuert (Tangentenpunkt = Koordinaten im Bezug zum lokalen Koordinatenursprung). Der erste Punkt hat keinen vorangehenden und der letzte keinen nachfolgenden Tangentenpunkt. Es kann nach dem letzten Kontrollpunkt ein Tangentenpunkt angegeben werden, dieser hat aber keine Funktion, dass liegt an den mathematischen Eigenschaften der Bezierkurve.

    CURVE_B2 n, status,
        x1, y1, t_next_x1, t_next_y1,
        ...
        t_prev_xn, t_prev_yn,
        xn, yn


| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpuntke |
| <code>status</code> | <code>j1</code> + <code>j2</code> Darstellungsoptionen |
| <code>xi, yi</code> | Koordinaten der Kontrollpunkte | 
| <code>t_prev_xi, t_prev_yi</code> | Tangentenpunkt **vor** dem Kontrollpunkt | 
| <code>t_next_xi, t_next_yi</code> | Tangentenpunkt **nach** dem Kontrollpunkt | 

- <code>j1 = 1</code>: Umrissline darstellen
- <code>j2 = 2</code>: Füllung darstellen

## CURVE_N2
<code>CURVE_N2</code> erzeugt eine NURBS-Kurve mit <code>n</code> Kontrollpunkten. Diese Kurve wird von Allplan als Polygon gezeichnet, die Anzahl der berechneten Punkte kann über die Direktiven <code>RESOL</code> und <code>RISE</code> gesteuert werden.

    CURVE_N2 n, status, x1, y1, ..., xn, yn

| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1 + j2 + j3</code> Darstellungsoptionen |
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|

- <code>j1 = 1</code>: Umrisslinie darstellen
- <code>j1 = 2</code>: Füllung darstellen
- <code>j1 = 4</code>: geschlossene Kurve, erster und letzter Punkt wird verbunden.
