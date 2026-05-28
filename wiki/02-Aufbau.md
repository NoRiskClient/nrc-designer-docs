# 2. Aufbau

← [Grundlagen](01-Grundlagen) · **2 / 12** · [Model →](03-Model)

---

Gerade wenn du Emotes mit Gegenständen oder Cosmetics erstellen willst, ist die **Struktur deines Modells** besonders wichtig. Falsche Hierarchie = später nicht animierbar.

## Das 7-Knochen-System

Wir benutzen ein **6**, bzw. mittlerweile **7-Knochen-System** — heißt: alles was du erstellen willst, **muss in einen dieser Knochen**. Erkennbar sind diese Gruppen am Präfix `armor` vor dem Namen. Sie finden sich nur in den **Unterordnern** des Templates.

![Die 7 Armor-Knochen im Outliner](images/image-3.png)

## Cubes richtig einsortieren

### Cubes, die sich mit dem Player bewegen

Angenommen du willst **Flügel** erstellen — dann kommen die Cubes dieser Flügel in einen eigenen Ordner, und dieser Ordner kommt in den passenden `armor`-Folder.

![Flügel-Beispiel: Cubes in armor-Folder](images/image-4.png)

### Cubes außerhalb des Player-Rigs

Wenn Cubes **außerhalb** des Player-Rigs sein sollen — z.B. für **Terrain** oder Gegenstände, die sich **NICHT** mit dem Main-Rig bewegen — kommen sie in einen Ordner **außerhalb** des Rigs.

![Cubes außerhalb des Rigs](images/image-5.png)

## Pivot-Punkte & Rigging

> ⚠️ **WICHTIG:** Wenn du diese später angenehm animieren willst, solltest du beim Modeln die **Pivot-Punkte der Folder richtig setzen** und alle Parts, die du animieren möchtest, **einzeln riggen** — denn du kannst nur **Folder, nicht Cubes** animieren.

![Pivot-Punkte setzen](images/image-6.png)

![Einzelne Folder für Animation](images/image-7.png)

---

← [Grundlagen](01-Grundlagen) · **2 / 12** · [Model →](03-Model)
