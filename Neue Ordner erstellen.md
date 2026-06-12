**Neuen Ordner/Kapitel anlegen – Checkliste**

**1. Ordner in Obsidian erstellen**  
Wie gewohnt – Rechtsklick → Neuer Ordner, an gewünschter Stelle in der Struktur.

**2. `index.md` im neuen Ordner anlegen**  
Mit Frontmatter für den Titel, danach der Inhalt:

yaml

```yaml
---
title: Name des Kapitels
---

Kurze Einleitung zum Thema...
```

**3. `.pages` Datei anlegen** (steuert Reihenfolge im Ordner)

Terminal-Befehl (Pfad anpassen):

bash

```bash
printf "nav:\n  - index.md\n  - ...\n" > "$HOME/Documents/GRK-Handbuch/docs/Pfad/Zum/Ordner/.pages"
```

Das setzt `index.md` an erste Stelle, alles andere folgt alphabetisch.

**4. Falls der neue Ordner auf der ERSTEN Ebene liegt** (direkt unter `docs`)

Zusätzlich die `.pages` Datei in `docs/` selbst anpassen – den neuen Ordnernamen an der gewünschten Stelle einfügen:

```
nano ~/Documents/GRK-Handbuch/docs/.pages
```

**5. Committen und pushen**

bash

```bash
cd ~/Documents/GRK-Handbuch
git add .
git commit -m "neuer Ordner: <Name>"
git push origin main
```

---

**Wichtig**: Schritt 3 (die `.pages` Datei) ist nur nötig wenn der Ordner **Unterordner** enthält und du die `index.md` an erster Stelle haben möchtest. Ein Ordner mit nur losen `.md`-Dateien ohne `index.md` braucht keine `.pages` Datei – die alphabetische Reihenfolge greift dann automatisch.