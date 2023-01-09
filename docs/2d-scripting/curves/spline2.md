# SPLINE2

Erzeugt einen Spline mit <code>n</code> Kontrollpunkten, die Tangentenwinkel in den Kontrollpunkten müssen angegeben werden. Tangentenwinkel starten in der lokalen X-Achse und laufen gegen den Uhrzeigersinn.


|Symbol|Beschreibung|
|--|--|
| <code>n</code> | Anzahl der Kontrollpunkte |
|<code>status</code>| <code>j1</code> + <code>j2</code> Spline Eigenschaften|
|<code>xi, yi</code>| Koordinaten der Kontrollpunkte|
|<code>anglei</code>|Tangentenwinkel der Kurve|

- <code>j1 = 1</code>: Spline ist geschlossen, erster und letzter Kontrollpunkt werden verbunden. Funktioniert in der Version 2013 leider nicht, wird aber in der nächsten Version korrigiert.
- <code>j2 = 2</code>: Spline automatisch glätten, angegebene Tangentenwinkel werden ignoriert

## Smartpart
```smartpart
SPLINE2 n, status, x1, y1, angle1, ..., xn, yn, anglen
```