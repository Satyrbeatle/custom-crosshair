# Custom Crosshair

Eine clientseitige Fabric-Mod für Minecraft Java Edition 1.21.4, die das Standard-Fadenkreuz durch ein frei anpassbares Crosshair ersetzt.

## Features

- Eigenes Fadenkreuz in beliebiger Farbe
- Einstellbare Größe, Lücke in der Mitte und Liniendicke
- Reiner Client-Mod: kein Server-Plugin nötig, funktioniert auf allen Servern
- Wird nur im Spiel angezeigt, nicht in Menüs oder bei ausgeblendetem HUD

## Voraussetzungen

- Minecraft Java Edition **1.21.4**
- [Fabric Loader](https://fabricmc.net/use/installer/) (ab 0.16.0)
- [Fabric API](https://modrinth.com/mod/fabric-api) für 1.21.4
- Java 21

## Installation

1. Fabric Loader für Minecraft 1.21.4 installieren.
2. Die Fabric API herunterladen und in den Ordner `.minecraft/mods/` legen.
3. Die JAR-Datei dieser Mod ebenfalls in `.minecraft/mods/` legen. Nimm die Datei **ohne** `-sources` oder `-dev` im Namen.
4. Minecraft mit dem Fabric-Profil starten.

## Download

Die fertige JAR wird automatisch von GitHub Actions gebaut:

1. Oben im Repository auf **Actions** klicken.
2. Den neuesten Durchlauf mit grünem Haken öffnen.
3. Unter **Artifacts** auf **CustomCrosshair** klicken und die ZIP entpacken.

## Anpassen

Die Einstellungen stehen in `CrosshairMod.java`:

| Einstellung | Bedeutung | Standard |
|-------------|-----------|----------|
| `color` | Farbe im ARGB-Format | `0xFF00FF00` (grün) |
| `size` | Länge der Arme | `6` |
| `gap` | Lücke in der Mitte | `3` |
| `thickness` | Dicke der Linien | `1` |

Nach einer Änderung baut GitHub Actions automatisch eine neue JAR.

## Selbst bauen

```bash
git clone https://github.com/DEIN-NAME/custom-crosshair.git
cd custom-crosshair
gradle build
```

Die fertige JAR liegt danach in `build/libs/`.

## Fehlerbehebung

- **Minecraft startet nicht:** Prüfe, ob Fabric API und Mod in `mods/` liegen und die Version 1.21.4 passt.
- **Kein Crosshair sichtbar:** Das HUD darf nicht ausgeblendet sein (F1).
- **Build schlägt fehl:** Im Reiter **Actions** den fehlgeschlagenen Schritt öffnen und die Fehlermeldung prüfen.

## Hinweis

Diese Mod verändert nur die Darstellung des Fadenkreuzes auf deinem eigenen Bildschirm. Sie verschafft keinen Vorteil im Spiel. Beachte trotzdem die Regeln des Servers, auf dem du spielst.
