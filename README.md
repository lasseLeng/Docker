# Docker Cheat Sheet

Dieses Dokument enthält die wichtigsten Docker-Befehle zur Verwaltung von Containern, Images, Netzwerken und Volumes.

## Docker-Images
### Image herunterladen
Ein Image aus dem Docker Hub herunterladen:

```bash
docker pull <image-name>
```
### Liste der heruntergeladenen Images anzeigen

```bash
docker images
```

### Ein Image löschen

```bash
docker rmi <image-id>
```
## Docker-Container
### Einen neuen Container erstellen und starten

Einen Container im Vordergrund starten:
```bash
docker run <image-name>
```

Einen Container im Hintergrund (detached mode) starten:
```bash
docker run -d <image-name>
```

