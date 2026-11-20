# 13. Cosmetic-Typen

← [Ingame-Test](12-Ingame-Test) · **13 / 15** · [Referenz →](14-Referenz)

---

Jedes Cosmetic hat in seiner `.norisk.json` einen **`type`**. Der Typ entscheidet, **wo** das Cosmetic am Spieler sitzt und welche Sonderregeln gelten.

## Alle Typen

| `type` | Sitzt an | Besonderheit |
|--------|----------|--------------|
| `HAT` | Kopf | Ersetzt den Helm (abschaltbar mit `"shouldReplaceHelmet": false`) |
| `FACE` | Kopf | |
| `BANDANA` | Kopf | |
| `BACK` | Rücken | |
| `WINGS` | Rücken | |
| `CAPE` | Rücken | **Kein Modell** — nur eine Textur. Mit `"hasElytraTexture": true` auch auf der Elytra |
| `SUIT` | ganzer Körper | Blendet die Rüstung aus |
| `ACCESSORIES` | Körper | |
| `PET` | Schulter / Brust | Sitzt auf dem Spieler |
| `BUDDY` | eigene Figur | Läuft dem Spieler hinterher → [Buddys](#buddys) |
| `OVERLAY` | Körper | **Kein Modell** — Textur liegt über dem Skin |
| `SHOES` | Füße | |
| `AURA` | um den Spieler | |
| `SHIELD` | rechte Hand | Braucht zusätzlich eine `<name>.shield.json` |

> 💡 Cosmetics am **Kopf** und `SHOES` passen sich automatisch an getragene Rüstung an, damit nichts durch den Helm oder die Stiefel ragt.

### Welcher Knochen?

Der Typ sagt, *wo* das Cosmetic hängt — *wie* es sich bewegt, bestimmt der `armor`-Knochen, in den du die Cubes legst (siehe [2. Aufbau](02-Aufbau)). Flügel kommen also z.B. in `armorBody`, Schuhe in `armorRightBoot` / `armorLeftBoot`.

---

## Buddys

Ein **Buddy** ist kein Teil des Spielers, sondern eine **eigene kleine Figur**, die dem Spieler hinterherläuft. Er folgt über Treppen und Kanten, springt, schwimmt, setzt sich hin, wenn der Spieler stillsteht, und schläft irgendwann ein.

### Modell

- Der Buddy steht **frei auf dem Boden** und bewegt sich nicht mit dem Spieler. Alle Cubes kommen deshalb in einen eigenen Knochen, dessen Name mit `armor` beginnt — wir nehmen dafür **`armorBuddy`**. Den gibt es im Plugin-Rig nicht, leg dir die Gruppe selbst an. Cubes außerhalb eines `armor…`-Knochens zählen nicht zur Größe — liegt gar nichts darin, wird der Buddy **nicht angezeigt**.
- Die Füße gehören auf **Höhe 0**. Schwebt das Modell darüber, schwebt der Buddy auch ingame.
- Die Größe des Modells ist gleichzeitig seine **Hitbox**: daraus berechnet der Client, wo der Buddy hinpasst, wo sein Schatten liegt und wo der Name erscheint. Lange Gegenstände (Schwerter, Schläger …) machen die Hitbox mit größer.

### Animationen

| Animation | Wann | | Fehlt sie … |
|-----------|------|---|-------------|
| `nrc.idle` | steht still neben dem Spieler | **Pflicht** | bleibt das Modell in der Grundpose |
| `nrc.walking` | läuft hinterher, Tempo passt sich an | **Pflicht** | |
| `nrc.running` | rennt, wenn der Spieler sprintet oder er aufholen muss | empfohlen | wird `nrc.walking` genommen |
| `nrc.sitting` | sitzt, wenn der Spieler ca. 8–12 s stillsteht | empfohlen | wird `nrc.idle` genommen |
| `nrc.afk` | schläft nach ca. 30–40 s oder wenn der Spieler im Bett liegt | empfohlen | wird `nrc.idle` genommen |
| `nrc.jumping` | springt Kanten hinunter — die Länge bestimmt die Sprungdauer | optional | fällt er einfach |
| `nrc.swimming` | schwimmt | empfohlen | wird `nrc.walking` bzw. `nrc.idle` genommen |
| `nrc.swimmidle` | treibt still im Wasser (zwei **m**!) | empfohlen | wird `nrc.swimming` genommen |
| `nrc.flying` | **nur fliegende Buddys**, läuft die ganze Zeit in der Luft | Pflicht für Flieger | wird `nrc.walking` bzw. `nrc.idle` genommen |
| `nrc.quirk_1` … `nrc.quirk_4` | kurze Einmal-Aktion im Stehen (Kratzen, Gähnen …) | optional | |
| `nrc.shop` | Vorschau im Shop | optional | zeigt der Shop `nrc.idle` |

`nrc.sneaking` und `nrc.crawling` werden bei Buddys **nicht** benutzt — beim Schleichen läuft er nur langsamer.

> 💡 Laufen, Rennen, Schwimmen, Fliegen und die Idles als **Loop** anlegen. Quirks **nicht** loopen — sie spielen einmal und blenden dann zurück in `nrc.idle`. Solange ein Quirk läuft, bleibt der Buddy stehen. Im Wasser gibt es keine Quirks.

### Wetter & Nacht (optional)

Buddys können auf **Regen**, **Schnee** und **Nacht** reagieren. Dafür legst du zusätzliche Animationen mit dem Namen der Zone an:

| Animation | Wann |
|-----------|------|
| `nrc.<zone>.start` | einmal, wenn der Buddy **in** die Zone kommt (z.B. es fängt an zu regnen) |
| `nrc.<zone>.stop` | einmal, wenn der Buddy die Zone **verlässt** |
| `nrc.<zone>.<animation>` | statt der normalen Animation, solange er in der Zone ist — z.B. `nrc.rain.walking`, `nrc.rain.idle`, `nrc.rain.sitting` |

`<zone>` ist `rain`, `snow` oder `night`.

Beispiel Regen: `nrc.rain.start` (Regenschirm aufspannen) → `nrc.rain.idle` / `nrc.rain.walking` (mit Schirm) → `nrc.rain.stop` (Schirm zuklappen).

> 💡 Das ist **keine Pflicht**. Du kannst auch nur einzelne Zonen oder einzelne Animationen davon anlegen.

### `.norisk.json`

```json
{
    "id": "a1b2c3d4-0000-4000-8000-000000000000",
    "name": "Mein Buddy",
    "creator": "Tinus",
    "price": 1500,
    "type": "BUDDY",
    "path": "mein_buddy",
    "rarity": "EPIC",
    "isExclusive": false
}
```

> ⚠️ Ältere Dateien mit `"type": "WALKING_PET"` funktionieren **nicht mehr** — auf `BUDDY` umstellen.

### Was Spieler einstellen können

- **Name:** Spieler können ihrem Buddy einen Namen geben (max. 16 Zeichen). Der Name erscheint, wenn man den Buddy anschaut.
- **Schatten:** Jeder kann Buddy-Schatten in den Cosmetics-Einstellungen für sich abschalten.

### Versionen

Buddys gibt es auf Minecraft **1.7.10 – 1.12.2** und **ab 1.16.5**. Auf 1.13 – 1.16.4 werden sie nicht angezeigt.

---

← [Ingame-Test](12-Ingame-Test) · **13 / 15** · [Referenz →](14-Referenz)
