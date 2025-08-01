**Skript: extract_unique_characters.R**

* Zweck: Extraktion einzigartiger Zeichen aus Transkriptionen
* Sprache: R  
* Ziel: Identifikation und Ausgabe aller Unicode-Zeichen in .txt-Transkriptionen (z. B. für HTR-Projekte mit Transkribus)
* Input: .txt-Dateien in UTF-8  
* Output: Excel-Datei (.xlsx) mit allen in den .txt.-Dateien vorkommenden Zeichen, einschließlich nicht-standardisierter bzw. nicht Unicode-konformer Zeichen
* Use Case: Vorverarbeitung, Datenbereinigung, Zeichenvereinheitlichung  
* Entwickelt für: QuantiSlav (HTR für Kirchenslavisch)  
* Hinweise: Funktioniert nur mit UTF-8-Dateien.

**Script: extract_unique_characters.R**
* Purpose: Extraction of unique characters from transcription files
* Language: R
* Goal: Identify and export all distinct Unicode characters found in .txt transcription files (e.g., for HTR projects using Transkribus)
* Input: .txt files in UTF-8 encoding
* Output: Excel file (.xlsx) containing all characters found in the .txt files, including non-standard and non-Unicode-compliant characters
* Use Case: Preprocessing, data cleaning, character normalization
* Developed for: QuantiSlav (HTR for Church Slavonic)
* Note: Only works with UTF-8 encoded files.

** Skript: replace_characters_in_XML.R

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
