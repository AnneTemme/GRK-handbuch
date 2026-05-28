
Dein Arbeitsbereich ist ausschließlich der **GRK-handbuch** Unterordner in Obsidian. Alles was du dort schreibst und mit `share: true` versiehst landet automatisch in docs und damit auf der Webseite.

---
- **GRK-Handbuch** ist der Hauptordner (gleichzeitig das Git Repository)
- **docs** ist der Ordner den MkDocs für die Webseite nutzt
- **GRK-handbuch** ist dein eigentlicher Obsidian Vault

Das bedeutet: du schreibst in dem Unterordner **GRK-handbuch** – und Enveloppe publiziert die Dateien in den **docs** Ordner, von wo MkDocs sie auf die Webseite bringt.

Öffne also in Obsidian den Vault **GRK-handbuch** – das ist dein Schreibbereich.

---

**Neue Seite erstellen:**

1. In Obsidian neue Notiz anlegen
2. Ganz oben im Textbereich Frontmatter einfügen:

```
---
share: true
---
```

3. Inhalt schreiben

**Seite veröffentlichen:** 
4. In Obsidian: **cmd + P** → **Enveloppe** → richtigen Upload-Befehl wählen 
5. In GitHub Desktop: Änderungen erscheinen automatisch 6. Unten links Beschreibung eingeben → **"Commit to main"** 7. Oben **"Push origin"** 8. Webseite aktualisiert sich automatisch in 1-2 Minuten

---

**Struktur aufbauen:**

- Ordner in Obsidian = Abschnitte in der Navigation
- Unterordner = Unterabschnitte
- Einfach Ordner anlegen und Notizen darin ablegen

---

**Seiten verlinken:**

- In Obsidian normal mit `[[Seitenname]]` verlinken
- Das wird automatisch zu einem klickbaren Link auf der Webseite

---

**Navigation anpassen:**

- In der `mkdocs.yml` kannst du die Reihenfolge der Abschnitte manuell festlegen – das machen wir wenn die ersten Inhalte da sind
