# LB2 - Snake Game in Docker

Ein selbst gehostetes Snake Game, das als Docker-Container auf einer AWS EC2 VM läuft.

---

## Idee

Snake Game im Browser, gehostet auf einer AWS VM mit Docker. Nginx liefert die statische `index.html` aus — simpel, aber voll funktionsfähig.

**Stack:**
- `nginx:alpine` als Webserver
- Eigene `index.html` mit Snake Game (HTML/CSS/JS)
- Docker Compose zum Starten

---

## Schritt 1: Projektordner erstellen

```bash
mkdir snake && cd snake
```

---

## Schritt 2: Dockerfile erstellen

```bash
cat > Dockerfile << 'EOF'
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EOF
```

Nginx Alpine ist ein minimales Image (~8MB) — kein unnötiger Ballast.

---

## Schritt 3: Docker Compose Datei erstellen

```bash
cat > docker-compose.yml << 'EOF'
services:
  snake:
    build: .
    ports:
      - "8000:80"
    restart: unless-stopped
EOF
```

---

## Schritt 4: index.html erstellen

```bash
nano index.html
```

Inhalt einfügen (Snake Game HTML/CSS/JS), speichern mit `Ctrl+X` → `Y` → `Enter`.

---

## Schritt 5: Container bauen und starten

```bash
docker compose up -d --build
```

Prüfen ob er läuft:
```bash
docker ps
```

---

## Schritt 6: Port in AWS freigeben

In der AWS Console:
1. EC2 → Instances → deine VM auswählen
2. **Security** → Security Group → **Edit inbound rules**
3. Regel hinzufügen: Type `Custom TCP`, Port `8000`, Source `0.0.0.0/0`
4. **Save rules**

---

## Schritt 7: Im Browser öffnen

```
http://<deine-AWS-Public-IP>:8000
```
![alt text](<../images/Screenshot 2026-05-05 103204.png>)
---

## Aufräumen

Container stoppen und löschen:
```bash
docker compose down
```

Image auch löschen:
```bash
docker image rm snake-snake
```

---

## Fazit

Mit Docker kann man eine App in wenigen Minuten deployen — Dockerfile schreiben, `docker compose up` und fertig. Das Image ist reproduzierbar und läuft auf jeder Maschine gleich.
