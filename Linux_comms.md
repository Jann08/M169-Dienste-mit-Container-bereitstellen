# Die wichtigsten Linux-Befehle

## Datei- und Verzeichnisoperationen
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `ls` | Verzeichnisinhalt anzeigen | `ls -la` (alle Dateien inkl. versteckte) |
| `cd` | Verzeichnis wechseln | `cd /home/user/dokumente` |
| `pwd` | Aktuelles Verzeichnis anzeigen | `pwd` |
| `mkdir` | Neues Verzeichnis erstellen | `mkdir neuer_ordner` |
| `rmdir` | Leeres Verzeichnis löschen | `rmdir alter_ordner` |
| `rm` | Dateien/Verzeichnisse löschen | `rm -rf ordner` (rekursiv erzwingen) |
| `cp` | Dateien kopieren | `cp quelle.txt ziel.txt` oder `cp -r ordner1/ ordner2/` |
| `mv` | Dateien verschieben/umbenennen | `mv alt.txt neu.txt` |
| `touch` | Leere Datei erstellen | `touch neue_datei.txt` |

## Dateien anzeigen und bearbeiten
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `cat` | Dateinhalt anzeigen | `cat datei.txt` |
| `less` | Datei seitenweise anzeigen | `less grosse_datei.log` (q zum Beenden) |
| `head` | Erste Zeilen anzeigen | `head -n 20 datei.txt` |
| `tail` | Letzte Zeilen anzeigen | `tail -f logdatei.log` (live verfolgen) |
| `nano` | Einfacher Texteditor | `nano config.json` |
| `vim` | Fortgeschrittener Editor | `vim script.py` |
| `grep` | Nach Text suchen | `grep "fehler" logdatei.log` |

## Berechtigungen und Benutzer
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `chmod` | Berechtigungen ändern | `chmod +x script.sh` (ausführbar machen) |
| `chown` | Besitzer ändern | `chown user:gruppe datei.txt` |
| `sudo` | Mit Admin-Rechten ausführen | `sudo apt install paket` |
| `whoami` | Aktuellen Benutzer anzeigen | `whoami` |
| `passwd` | Passwort ändern | `passwd` |

## Paketverwaltung (Ubuntu/Debian)
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `apt update` | Paketlisten aktualisieren | `sudo apt update` |
| `apt upgrade` | Alle Pakete aktualisieren | `sudo apt upgrade` |
| `apt install` | Paket installieren | `sudo apt install git` |
| `apt remove` | Paket entfernen | `sudo apt remove git` |
| `apt search` | Nach Paketen suchen | `apt search python` |

## Netzwerk und Internet
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `ping` | Erreichbarkeit testen | `ping google.com` |
| `wget` | Datei herunterladen | `wget https://example.com/datei.zip` |
| `curl` | Daten übertragen | `curl https://api.github.com` |
| `ssh` | Remote-Verbindung | `ssh user@server.com` |
| `ifconfig`/`ip` | Netzwerkkonfiguration | `ip addr show` |

## Prozesse und System
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `ps` | Laufende Prozesse | `ps aux` (alle Prozesse) |
| `top`/`htop` | Prozessmonitor | `top` (q zum Beenden) |
| `kill` | Prozess beenden | `kill -9 1234` (Prozess-ID 1234 erzwingen) |
| `df` | Festplattennutzung | `df -h` (lesbar) |
| `du` | Verzeichnisgröße | `du -sh ordner/` |
| `free` | RAM-Nutzung | `free -h` |
| `uname` | Systeminfo | `uname -a` |
| `reboot` | Neustarten | `sudo reboot` |
| `shutdown` | Herunterfahren | `sudo shutdown now` |

## Archivierung und Komprimierung
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `tar` | Archiv erstellen/extrahieren | `tar -czvf archiv.tar.gz ordner/` (packen) |
| `zip`/`unzip` | ZIP-Archive | `zip -r archiv.zip ordner/` |
| `gzip`/`gunzip` | GZIP-Komprimierung | `gzip datei.txt` |

## Nützliche Kurzbefehle
| Befehl | Beschreibung |
|--------|--------------|
| `ctrl + c` | Aktuellen Prozess abbrechen |
| `ctrl + z` | Prozess pausieren |
| `ctrl + d` | Terminal schließen |
| `!!` | Letzten Befehl wiederholen |
| `history` | Befehlshistorie anzeigen |
| `man befehl` | Handbuch zu einem Befehl |
| `clear` | Terminal leeren |
| `which` | Pfad eines Programms finden |