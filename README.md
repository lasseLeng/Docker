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
### Einen Container mit Port-Mapping starten
Port-Mapping leitet einen Host-Port auf einen Container-Port um:
```bash
docker run -d -p <host-port>:<container-port> <image-name>
```

### Einen Container mit einem Namen starten
```bash
docker run --name <container-name> -d <image-name>
```

### Liste der laufenden Container anzeigen
Nur laufende Container anzeigen:
```bash
docker ps
```

Alle Container anzeigen (inkl. gestoppter Container):
```bash
docker ps -a
```

### Einen Container stoppen
```bash
docker stop <container-id>
```

### Einen Container starten (neu starten)
```bash
docker start <container-id>
```

### Einen Container löschen
Einen gestoppten Container löschen:
```bash
docker rm <container-id>
```

Alle gestoppten Container löschen:
```bash
docker rm $(docker ps -a -q)
```

## Logs und Debugging
### Logs eines Containers anzeigen
```bash
docker logs <container-id>
```

### Interaktiv auf einen Container zugreifen
```bash
docker exec -it <container-id> /bin/bash
```

## Docker-Volumes
### Ein Volume erstellen
```bash
docker volume create <volume-name>
```

### Ein Volume zu einem Container hinzufügen
```bash
docker run -d -v <volume-name>:/<container-path> <image-name>
```

### Liste der Volumes anzeigen
```bash
docker volume ls
```

### Ein Volume löschen
```bash
docker volume rm <volume-name>
```

## Docker-Netzwerke
### Ein Netzwerk erstellen
```bash
docker network create <network-name>
```

### Ein Container einem Netzwerk hinzufügen
```bash
docker network connect <network-name> <container-id>
```

### Liste der Netzwerke anzeigen
```bash
docker network ls
```

### Ein Netzwerk löschen
```bash
docker network rm <network-name>
```
