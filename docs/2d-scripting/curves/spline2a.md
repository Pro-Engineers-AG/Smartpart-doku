# SPLINE2_A
<code>SPLINE2_A</code> ist eine Erweiterung des [SPLINE2](spline2.md) Befehls und erzeugt Bezier-Splines mit <code>n</code> Kontrollpunkten, Tangentenwinkel und Tangentenlängen müssen angegeben werden.

## Smartpart

| Symbol | Beschreibung |
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1</code> + <code>j2</code> Spline Eigenschaften|
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|
|<code>anglei</code>|Tangentenwinkel der Kurve|
|<code>len_previ</code> | Länge der Tangente **vor** dem Kontrollpunkt |
|<code>len_nexti</code> | Länge der Tangente **nach** dem Kontrollpunkt |

```smartpart
SPLINE2 n, status, x1, y1, angle1, len_prev1, len_next1, ..., xn, yn, anglen, len_prevn, len_nextn
```

