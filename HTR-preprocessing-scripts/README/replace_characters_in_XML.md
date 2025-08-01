**Skript:** replace_characters_in_XML.R

* Zweck:  
Automatisierte Ersetzung nicht-standardisierter oder benutzerdefinierter Zeichen in Transkribus PAGE-XML-Dateien auf Basis einer benutzerdefinierten Ersetzungsliste.
* Sprache: R
* Ziel: 
Normalisierung bzw. Standardisierung der Zeichenverwendung innerhalb der `<Unicode>`-Tags in Transkribus-Trainingsdaten mithilfe einer Ersetzungstabelle.
* Input:  
- Ein Verzeichnis mit PAGE-XML-Dateien (.xml)  
- Eine Excel-Datei (`.xlsx`) mit zwei Spalten:  
  - Spalte 1: Zeichen oder Strings, die ersetzt werden sollen  
  - Spalte 2: Zielzeichen oder Ersatzstrings
* Output:  
- Die ursprünglichen XML-Dateien werden **überschrieben** – alle betroffenen `<Unicode>`-Inhalte sind danach ersetzt.
* Use Case: 
- Vorbereitung und Bereinigung von Trainingsdaten in HTR-Workflows  
- Vereinheitlichung der Zeichencodierung (z. B. bei Unicode- oder PUA-Zeichen)  
- Vorverarbeitungsschritt zur Sicherstellung konsistenter Zeichenverwendung
* Entwickelt für: QuantiSlav (HTR für Kirchenslawisch)
* Hinweise:  
- Die **Ersetzungstabelle (`replacement_mappings.xlsx`) muss manuell erstellt werden**.  
  Sie sollte zwei Spalten enthalten (keine Spaltennamen notwendig):  
  1. Spalte: Zeichen, die ersetzt werden sollen  
  2. Spalte: Ersatzzeichen  
- Das Skript überschreibt die Dateien im angegebenen XML-Verzeichnis. Es empfiehlt sich, vor der Anwendung Sicherungskopien der XML-Dateien zu erstellen.

**Script:** replace_characters_in_XML.R

* Purpose: 
Automated replacement of non-standard or custom characters in Transkribus PAGE-XML files based on a user-defined mapping file.
* Language: R
* Goal:
Normalize or standardize character usage within `<Unicode>` tags of Transkribus PAGE-XML training data using a replacement list.
* Input:  
- A directory of PAGE-XML files (.xml)  
- An Excel file (`.xlsx`) containing replacement character mappings (2 columns: "from", "to")
* Output:
- The original XML files are overwritten with updated character content inside `<Unicode>` tags.
* Use Case:  
- Preprocessing step in HTR workflows (e.g. for model retraining in Transkribus)  
- Unicode normalization and harmonization across heterogeneous transcription sources
* Developed for: QuantiSlav (HTR for Church Slavonic)
* Note:  
- You need to create a replacement file (`replacement_mappings.xlsx`) manually.  
  This file should contain:
  - Column 1: Characters or strings to be replaced  
  - Column 2: Replacement characters or strings  
- The script modifies the files in place. Create backups before use.
