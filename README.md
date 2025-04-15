<div align="center">

<img src="img/logo.svg" alt="logo" width=100% >

# *2D Side-Scrolling-RPG mit einem Twist*

</div>

<details>
  <summary>  $\LARGE\color{orange}{\ Klicke\ }$ 👉🏼 $\LARGE\color{royalblue}{hier\ }\color{lightgray}{um\ die\ Entwicklung\ zu\ verfolgen}$ </summary>

```mermaid
gantt
    %%   T I T L E
    title BackpackMage

    dateFormat DD-MM-YYYY
    excludes sunday

    axisFormat %d.%m

    section Legend
        today : milestone, crit, active, t0, 15-04-2025, 24h
        week0 : w0, 15-04-2025, 1m
        week1 : w1, 14-04-2025, 6d
        week2 : w2, 21-04-2025, 6d
        week3 : w3, 28-04-2025, 6d
        week4 : w4, 05-05-2025, 6d
        week5 : w5, 12-05-2025, 6d
        week6 : w6, 19-05-2025, 6d
        week7 : w7, 26-05-2025, 5d

        planing               :          crit , plan , 14-04-2025 , 1d
    section Learning
        Unitiy Essentials     : active , crit ,  U , after w0 , 31d

        TILES & Sprites       : active , crit ,  t , after w0 ,  5d
        tilemap               :                 tm , after w0 ,  1d

        ruletile              :                 tr , after tm   ,  1d
        animatedtile          :                 ta , after tr   ,  1d
        spritesheet           :                  s , after ta   ,  1d


        GUI                   :          crit ,  g , after w1 ,  6d
        splashscreen          :                  s , after w1 ,  1d
        titlescreen           :                 ts , after s    ,  1d

        inventory             :                   i, after ts   ,  1d



    section ArtCreation

        %%   T I L E S E T S
        TileSets              : active , crit , tis , after w0 , 60h
        tileset-magetower     :                 tsm , after w0 , 2h
        tileset-mt-acessories :                tsma , after tsm  , 2h
        tileset-woodland      :                 tsw , after tsma , 2h
        tileset-wl-acessories :                tswa , after tsw  , 2h

        %%   S P R I T E S
        Sprites               :          crit , spr , after tis   , 60h
        sprite-player         :                 spp , after tis   , 2h
        sprite-mage           :                 spm , after spp   , 2h
        sprite-paralax-bg     :                spgb , after spm   , 2h
        sprite-inventory      :                spin , after spgb  , 2h

    section UserInterface
        Screens               :          crit , scr , after w1    , 3d
        splashscreen          :                spls , after w1    , 2h
        titlescreen           :                tits , after spls  , 2h

        Inventory             :          crit , inv , after scr   , 9d

    section UnityDevelopment
        Implement-Intro       :               intro , after inv , 3d

        Implement-Inventory   :               invent , after intro , 3d

        Implement-TestLevel   :               test , after invent , 3d

    %%   M I N I M A L   V I A B L E   P R O J E C T
    %%
    MVP                       : milestone , crit , 18-05-2025

    section Testing
        Final Week            :          crit , fiw , 22-05-2025 , 7d

    %%   D E P L O Y M E N T
    %%
    Deploy                    : milestone , crit , 31-05-2025

```

# Sprites

- ### Players 

    > <img src="./img/player.gif" alt="player?">


  
</details>


## Spielprinzip:
- Ihr steuert einen mürrischen Abenteurer, der eigentlich nur seine Ruhe will – doch ein sadistischer Magier zwingt euch mit einem Fluch ihn herumzutragen!
- In diesem 2D Side-Scrolling-RPG müsst ihr Quests erfüllen, Monster bekämpfen und mit dem ständigen Spott des Magiers leben, der euch leiden sieht.
- Werdet ihr den Zauber brechen und euch befreien – oder bleibt ihr für immer sein Spielzeug?

---

## Spielgenre und Zielgruppe

### Genre:
Ich habe mich für einen 2D Inventory-Manager entschieden, mit Elementen eines 2D Side-Scrolling-RPGs umgesetzt in Pixelgrafik.

### Warum?
- RPGs bieten Raum für eine tiefgründige Geschichte und Charakterentwicklung, was perfekt zu meinem Konzept passt: Ein widerwilliger Abenteurer trifft auf einen sadistischen Magier und steckt ihn in seinen Rucksack.
- Die Pixelgrafik verleiht dem Spiel einen nostalgischen, Retro-Charme, der nicht nur bei Indie-Fans gut ankommt.
- Die Genres Herobuilder und Inventory-Manager erfreuen sich momentan großer Beliebtheit aufgrund ihrer Einsteigerfreundlichkeit und hohen Wiederspielwertes.
<div align="center">
  <img src="img/backpack.jpg" alt="example" width=100%>
</div>

---

## Spielziele

### Was sollen Spieler:innen erreichen?
- Die Spieler steuern den Abenteurer durch vom Magier aufgezwungene Quests und Abenteuer.
- Die Hauptaufgabe ist es, diese Missionen zu erfüllen, um den Magier zufriedenzustellen – und vielleicht einen Weg zu finden, den Fluch zu brechen.
- **Niederlage**: Zu oft scheitern oder Bedingungen nicht erfüllen, was dazu führt, dass der Magier die Kontrolle übernimmt oder der Abenteurer stirbt.

---

## Hauptmechaniken

### Zentrale Mechaniken:
  - **Bewegung und Erkundung**: Side-Scrolling-Steuerung durch Wälder, Dungeons und Dörfer (z.B. mit WASD).
  - **Kampf**: Einfaches Echtzeit-Kampfsystem (Klicken zum Angreifen).
  <div align="center">
    <img src="img/fightscene.jpg" alt="fight" width=40%>
  </div>

  - **Inventory-Management**: Grid-basiertes Inventar zum Sammeln und Verwalten von einer großen Anzahl an Gegenständen, Waffen und Ausrüstungen.
  <div align="center">
    <img src="img/loot.jpg" alt="collectables" width=40%>
  </div>

  - **Charakterentwicklung**: Finde Gegenstände durch Quests und Kämpfe, um Fähigkeiten zu verbessern.
  - **NPC-Interaktion**: Dialoge mit NPCs für Quests, Infos oder Handel.
  - **Magier-Mechanik**: Der Magier greift zufällig ein, z.B. mit Hindernissen oder temporären Boni/Mali.

---

## USP (Unique Selling Point)

### Was macht das Spiel besonders?
Die einzigartige Dynamik zwischen dem widerwilligen Abenteurer und dem sadistischen Magier!
Diese Beziehung sorgt für Humor (z.B. der Magier verspottet den Spieler) und Spannung (gefährliche Situationen).
Zusätzlich parodiert das Spiel RPG-Tropen: Der Held will gar kein Held sein, wird aber dazu gezwungen.

---
### Zielgruppe:
- Alter: 16–35 Jahre
- Interessen: RPG-Fans, Indie-Gamer, Liebhaber von schwarzem Humor und Retro-Stil
- Warum? Die Mischung aus Humor, Herausforderung und einer einzigartigen Beziehung zwischen Abenteurer und Magier spricht vor allem Spieler an, die narrative Tiefe und kreative Konzepte schätzen.

---

## Umsetzung in Unity

- **Grafik**: Pixel-Art-Assets.
- **Steuerung**: WASD/Pfeiltasten, Spacebar - für Side-Scrolling-Bewegung.
- **Kampfsystem**: Einfache Klick-Attacken, mit Synergien durch mitgenommene Gegenstände.
- **Inventory**: Grid-System mit Drag-and-Drop-Funktion.
- **Quests**: Quest-Log mit Fortschrittsskripten.
- **Dialogsystem**: Textboxen mit Auswahlmöglichkeiten.
- **Magier-Mechanik**: Events gesteuert durch mitgeführte Gegenstände und Spielfortschritt via Skripte.

---

### Zusammenfassung
Dieses 2D Side-Scrolling-RPG kombiniert klassische RPG-Elemente mit einer frischen, humorvollen Prämisse: Ein Abenteurer, der unter dem Fluch eines sadistischen Magiers leidet, kämpft widerwillig um seine Freiheit. Mit Pixelgrafik, zugänglichen Mechaniken und einer starken Story ist es ideal für Indie-Fans und RPG-Liebhaber!

---

## MoodBoard

### Level:
<img src="img/level-mood.jpg" alt="level-moodboard" width=100%>

---

# Benutzte Grafiken und Schriften

### Font -  *ExpressionPro*:

<div align="center">
<img src="img/font-expression.jpg" alt="gimiks-moodboard" width= 90%>
</div>

### Beispiel Monster, Charaktere & Items:

<div align="center">
<img src="img/fantasy-mood.jpg" alt="acessories-moodboard" width=48%>
<img src="img/fantasy2-mood.jpg" alt="gimiks-moodboard" width=48%>
</div>

---
### Angepasstes Tileset - *Tranquill*:
<div align="center">
  <img src="img/tileset-mood.jpg" alt="tileset-adjusted" width=90%>
</div>
