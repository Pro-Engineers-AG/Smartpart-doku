# CURVE_B2

<code>CURVE_B2</code> erzeugt eine Bezierkurve mit <code>n</code> Kontrollpunkten, die Form der Bezierkurve wird über Tangentenpunkte gesteuert (Tangentenpunkt = Koordinaten im Bezug zum lokalen Koordinatenursprung). Der erste Punkt hat keinen vorangehenden und der letzte keinen nachfolgenden Tangentenpunkt. Es kann nach dem letzten Kontrollpunkt ein Tangentenpunkt angegeben werden, dieser hat aber keine Funktion, dass liegt an den mathematischen Eigenschaften der Bezierkurve.


| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpuntke |
| <code>status</code> | <code>j1</code> + <code>j2</code> Darstellungsoptionen |
| <code>xi, yi</code> | Koordinaten der Kontrollpunkte | 
| <code>t_prev_xi, t_prev_yi</code> | Tangentenpunkt **vor** dem Kontrollpunkt | 
| <code>t_next_xi, t_next_yi</code> | Tangentenpunkt **nach** dem Kontrollpunkt | 

- <code>j1 = 1</code>: Umrissline darstellen
- <code>j2 = 2</code>: Füllung darstellen

## Smartpart
```smartpart
CURVE_B2 n, status,
    x1, y1, t_next_x1, t_next_y1,
    ...
    t_prev_xn, t_prev_yn,
    xn, yn
```

