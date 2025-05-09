<div align="center">

<img src="img/title-0.0.7.png" alt="logo" width=100% >

# *2D Side-Scrolling-RPG mit einem Twist*

</div>

<details>
  <summary>  $\LARGE\color{orange}{\ Klicke\ }$ 👉🏼 
$\LARGE\color{lime}{hier\ }\color{lightgray}{um\ die\ Downloads\ zu\ sehen}$   </summary>
  
- Das vollständige Archiv kann mit dem **`Downloadbutton`**, rechts kopiert werden:

  > ###### Screenshot:
  >  <img src="https://github.com/user-attachments/assets/a4326d7b-0438-44cf-a636-89e35750e407" link="https://github.com/IxI-Enki/backpackmage/blob/master/backpackmage-0.0.1.7z" alt="Erklärender Screenshot" Width=400px>

  # Downloads 
    - Windows:
      - [ Version 0.0.1 ](https://github.com/IxI-Enki/backpackmage/blob/master/backpackmage-0.0.1.7z)
      - [ Version 0.0.5 ](https://github.com/IxI-Enki/backpackmage/blob/master/backpackmage-0.0.5.7z)
      - [ Version 0.0.7 ](https://github.com/IxI-Enki/backpackmage/blob/master/backpackmage-0.0.7-exe.7z)
      > - download raw file
      > - unzip archive (7z)
      > - play with BPM.exe

    - Linux [ Version 0.0.2 ](https://github.com/IxI-Enki/backpackmage/blob/master/backpackmage-0.0.2-linux.x86_64.7z)
      > - download raw file
      > - unzip archive (7z)
      > - `sudo apt-get install libglu1-mesa libxcursor1 libxrandr2` - install dependencies
      > - `chmod +x backpackmage-0.0.2-linux.x86_64` - to make file executeable
      > - `./backpackmage-0.0.2-linux` - execute program
</details>

---

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
        today : milestone, crit, active, t0, 06-05-2025, 24h
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

        TILES & Sprites       :   done , crit ,  t , after w0 ,  5d
        tilemap               :   done ,        tm , after w0 ,  1d

        ruletile              :   done ,        tr , after tm   ,  2d
        animatedtile          :   done ,        ta , after tr   ,  1d
        spritesheet           :   done ,         s , after ta   ,  1d


        GUI                   :          crit ,  g , after w2 ,  6d
        splashscreen          :   done ,         s , after w2 ,  1d
        titlescreen           :   done ,        ts , after s    ,  1d

        inventory             :                   i, after ts   ,  1d



    section ArtCreation

        %%   T I L E S E T S
        TileSets              :   done , crit , tis , after w0 , 120h
        tileset-magetower     :   done ,        tsm , after w0 , 2h
        tileset-mt-acessories :   done ,       tsma , after tsm  , 2h
        tileset-woodland      :   done ,        tsw , after tsma , 2h
        tileset-wl-acessories :   done ,       tswa , after tsw  , 2h

        %%   S P R I T E S
        Sprites               :   done , crit , spr , after tis   , 120h
        sprite-player         :                 spp , after tis   , 2h
        sprite-mage           :                 spm , after spp   , 2h
        sprite-paralax-bg     :  active,       spgb , after spm   , 2h
        sprite-inventory      :  active,       spin , after spgb  , 2h

    section UserInterface
        Screens               :   done , crit , scr , after w2    , 3d
        splashscreen          :   done ,       spls , after w2    , 2h
        titlescreen           :   done ,       tits , after spls  , 2h

        Inventory             : active ,  crit , inv , after scr   , 9d

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
# Tiles 

## Tilemaps
| MageTower |  Woodland |
| :--: | :--: |
| <span><img src="./img/magetower-big.png" alt="MageTower" ></span> | <span><img src="./img/woodland-big.png" alt="Woodland" ></span> |
| Decor | Water |
| <span><img src="./img/map-decor.png" alt="Decor" width=400px></span> | <span><img src="./img/water.png" alt="Water" width=80px></span> |
| TileMap | NormalMap |
| <span><img src="./img/tileMap.png" alt="TileMap" ></span> | <span><img src="./img/normalMap.png" alt="NormalMap" ></span> |

## Ruletiles

| <span><img src="./img/ruletiles-wl.png" alt="Ruletiles in Unity" ></span> | <span><img src="./img/ruletiles-example.png" alt="Woodland" ></span> |
| :--: | :--: |

## Lighting with Normal Maps

https://github.com/user-attachments/assets/69735791-062f-482f-8116-82653ce57a5f

# Sprites

- ### Players  
    > <span><img src="./img/player.gif" alt="player?" width=100px><img src="./img/player2.gif" alt="player2?" width=100px><img src="./img/player3.gif" alt="player3?" width=100px><img src="./img/player_01_bp.gif" alt="player1?" width=100px><img src="./img/player_02_bp.gif" alt="player2?" width=100px><img src="./img/player_03_bp.gif" alt="player3?" width=100px></span>

- ### Enemies
    > <span><img src="./img/bat_01.gif" alt="bat" width=100px></span>

- ## ShaderGraph
  > comming

---
- # Behaviours

- ## AnimationGraph
  > comming
  

  
- ## Enemy Brains
    ![brains](https://github.com/user-attachments/assets/4269d165-6581-45d0-8736-e8e3b1f751b4)
    
    > ![HappyLittleMonsters](https://github.com/user-attachments/assets/2dec3c41-9f00-4651-9ea5-da84bb10712a)<br>
    > **They can now:**
    >   - detect: Walls, Standing on safe ground, Other enemies or players (individually),
    >   - idle, walk and jump<br>
    > ![SkeletonMobbing](https://github.com/user-attachments/assets/7588eb0b-c047-49e8-8436-7461b6f0daa9)


    


  
</details>


--- 

# <p align="center"> Übersicht </p>

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
