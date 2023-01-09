# Text 2D


Erzeugt den Text <code>expression</code> an der Position <code>(x, y)</code>.

| Symbol | Bezeichnung |
|--|--|
| (x, y) | Position |
| expression | Anzuzeigender Text |

## Smartpart
```smartpart
TEXT2 x, y, expression
```

### Beispiel
```smartpart
! Definiere einen neuen Stil
DEFINE STYLE "Ueberschrift", "Arial", 20, 1, 0, 0

! Setze zuvor erstellten Stil
STYLE "Ueberschrift"

! Fuege Text "Hallo Welt!" bei Koordinate 0,0 ein.
TEXT2 0, 0, "Hallo Welt"
```