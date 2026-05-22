# Prüfungsaufgabe 2: Decision-Tree

---

## Starten der Umgebung
Das Notebook kann per mybinder (https://mybinder.org/) geöffnet werden.
Folgende Daten müssen in die Felder eingetragen werden:
- Github Repo: https://github.com/simon1805/Decision-Tree-Testing-and-Logging.git
- Git ref: main
- File to open: index.ipynb

---

## Kurzbeschreibung
Dieses Notebook implementiert einen einfachen Logging‑ und Timing‑Ansatz für ML‑Funktionen und zwei Unittests für ein Decision‑Tree‑Beispiel. Mit den Dekoratoren **my_logger** und **my_timer** werden Aufrufe und Laufzeiten von `fit()` und `predict()` strukturiert als JSON‑Zeilen protokolliert. Zwei Tests prüfen die **Vorhersagequalität** (Accuracy und Confusion Matrix) und die **Trainingslaufzeit** (Grenzwert 120% einer repräsentativen Laufzeit).

---

## Projektstruktur im Notebook
- **Dekoratoren**: `my_logger`, `my_timer` (schreiben JSON‑Logs in `logs/`)  
- **Wrapperklassen**: `DecisionTreeWrapper`, `RandomForestWrapper` (verwenden die Dekoratoren)  
- **Daten**: `final_data` (eigene Daten oder synthetisch erzeugt im Notebook)  
- **Messung**: Repräsentative `fit()`‑Laufzeit wird einmal gemessen und optional in `rep_runtime.json` gespeichert  
- **Unittests**: Zwei Tests mit `unittest` direkt im Notebook

---
