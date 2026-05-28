# 7. Molang

← [Keyframes](06-Keyframes) · **7 / 12** · [Particle →](08-Particle)

---

📖 **Offizielle Doku:** [GeckoLib Molang Wiki](https://github.com/bernie-g/geckolib/wiki/Molang)

## Was ist Molang?

**Molang** sind **Funktionen**, die anstelle oder zusammen mit Keyframe-Values agieren. Sie laufen quasi **unendlich weiter** und können ganz einfach für **Idle-Animationen** benutzt werden.

> 🔑 **Wichtig:** Wenn eine Animation mit einer Molang-Animation enden und unendlich weiter gehen soll, **muss die Animation am Molang-Frame enden**.

---

## Beispiele nach Loop-Modus

### Hold On Last Frame

Animation läuft einmal durch und der letzte Frame (Molang) läuft endlos weiter.

![Hold On Last Frame Setup](images/image-21.png)

![Hold On Last Frame Resultat](images/testEmotes.gif)

---

### Loop

Komplette Animation wiederholt sich endlos.

![Loop Setup](images/image-22.png)

![Loop Resultat](images/testEmotes2.gif)

---

### Play Once

Animation läuft genau einmal durch und endet danach komplett.

![Play Once Setup](images/image-23.png)

![Play Once Resultat](images/testEmotes3.gif)

---

← [Keyframes](06-Keyframes) · **7 / 12** · [Particle →](08-Particle)
