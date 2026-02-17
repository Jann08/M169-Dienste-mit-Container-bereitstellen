## Git Grundbefehle
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `git init` | Neues Repository erstellen | `git init` |
| `git clone` | Repository kopieren | `git clone git@github.com:user/repo.git` |
| `git status` | Status anzeigen | `git status` |
| `git add` | Dateien zum Commit vormerken | `git add .` (alle) oder `git add datei.txt` |
| `git commit` | Änderungen speichern | `git commit -m "Nachricht"` |
| `git push` | Änderungen hochladen | `git push origin main` |
| `git pull` | Änderungen herunterladen | `git pull origin main` |
| `git fetch` | Änderungen abrufen (ohne mergen) | `git fetch origin` |

## Branches verwalten
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `git branch` | Branches anzeigen | `git branch` (lokal) oder `git branch -r` (remote) |
| `git branch neu` | Neuen Branch erstellen | `git branch feature-login` |
| `git checkout` | Branch wechseln | `git checkout feature-login` |
| `git switch` | Branch wechseln (neuere Variante) | `git switch main` |
| `git checkout -b` | Branch erstellen und wechseln | `git checkout -b neuer-branch` |
| `git merge` | Branch zusammenführen | `git merge feature-login` |
| `git branch -d` | Branch löschen | `git branch -d alter-branch` |

## Änderungen rückgängig machen
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `git reset` | Commit rückgängig machen | `git reset --soft HEAD~1` (letzten Commit) |
| `git revert` | Commit umkehren (neuer Commit) | `git revert HEAD` |
| `git restore` | Datei wiederherstellen | `git restore datei.txt` |
| `git clean` | Unverfolgte Dateien löschen | `git clean -fd` |
| `git stash` | Änderungen zwischenspeichern | `git stash` / `git stash pop` |

## Informationen anzeigen
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `git log` | Commit-Historie | `git log --oneline --graph` (übersichtlich) |
| `git diff` | Änderungen anzeigen | `git diff` (uncommitted) |
| `git show` | Commit-Details | `git show HEAD` |
| `git blame` | Wer hat wann geändert? | `git blame datei.txt` |
| `git remote -v` | Remote-Repositorys anzeigen | `git remote -v` |
| `git tag` | Tags anzeigen/erstellen | `git tag v1.0.0` |

## SSH & Authentifizierung (für GitHub)
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `ssh-keygen` | SSH-Schlüssel erstellen | `ssh-keygen -t ed25519 -C "email@example.com"` |
| `ssh -T git@github.com` | SSH-Verbindung testen | `ssh -T git@github.com` |
| `cat ~/.ssh/id_rsa.pub` | Öffentlichen Schlüssel anzeigen | `cat ~/.ssh/id_rsa.pub` |
| `eval $(ssh-agent)` | SSH-Agent starten | `eval $(ssh-agent -s)` |
| `ssh-add` | Schlüssel zum Agent hinzufügen | `ssh-add ~/.ssh/id_rsa` |

## Fortgeschrittene Git-Befehle
| Befehl | Beschreibung | Beispiel |
|--------|--------------|----------|
| `git rebase` | Commits umbasieren | `git rebase main` |
| `git cherry-pick` | Einzelnen Commit übernehmen | `git cherry-pick commit-hash` |
| `git bisect` | Fehler suchen (binäre Suche) | `git bisect start` |
| `git submodule` | Untermodule verwalten | `git submodule add https://...` |
| `git archive` | Repository als ZIP exportieren | `git archive --format=zip HEAD > repo.zip` |

## Nützliche Kombinationen
| Befehl | Beschreibung |
|--------|--------------|
| `git add . && git commit -m "update"` | Alle Änderungen committen |
| `git pull --rebase` | Pull mit Rebase (sauberere Historie) |
| `git log --oneline --decorate --graph --all` | Komplette Branch-Historie visualisieren |
| `git commit --amend -m "Neue Nachricht"` | Letzten Commit ändern |
| `git push --force-with-lease` | Erzwingen pushen (sicherer als --force) |
