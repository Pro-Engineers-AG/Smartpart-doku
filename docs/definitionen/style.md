# Style - Textstil

## Neuen Textstil definieren


### Smartpart

| Symbol | Bezeichnung |
|--|--|
| name | Name des Textstils |
| font_family | Name der Schriftart z.B. "Arial" |
| size | Zeichenhöhe in mm, Maßstäbliche Grösse = <code>Zeichnhöhe / GLOB_SCALE * 100</code> |
| anchor | Einfügepunkt des Textes 1 - 9 |
| face_code | Nicht unterstützt, muss aber angegeben werden. (0) |
| filling | 0: Ohne Hintergrund, 1: Mit Hintergrund |

#### Anchor

|   |   |   |
|:-:|:-:|:-:|
|1|2|3|
|4|5|6|
|7|8|9|


```smartart
DEFINE STYLE name font_family, size, anchor, face_code, filling
```

