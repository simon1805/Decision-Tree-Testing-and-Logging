# Prüfungsaufgabe 2: Decision-Tree

---

## Starten der Umgebung
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/simon1805/Decision-Tree-Testing-and-Logging/main?filepath=index.ipynb)

---

## Kurzbeschreibung
Dieses Notebook implementiert einen einfachen Logging‑ und Timing‑Ansatz für ML‑Funktionen und zwei Unittests für ein Decision‑Tree‑Beispiel. Mit den Dekoratoren **my_logger** und **my_timer** werden Aufrufe und Laufzeiten von `fit()` und `predict()` strukturiert als JSON‑Zeilen protokolliert. Zwei Tests prüfen die **Vorhersagequalität** (Accuracy und Confusion Matrix) und die **Trainingslaufzeit** (Grenzwert 120% einer repräsentativen Laufzeit).

---

## Ausführung der Testfälle

Die implementierten Unit-Tests wurden erfolgreich ausgeführt. Dabei wurden sowohl die Vorhersagefunktion predict() als auch die Trainingsfunktion fit() des Modells überprüft.

### Testfall 1: Überprüfung der Vorhersagefunktion predict()

Für die Vorhersagefunktion wurden die Accuracy sowie die Confusion Matrix als Qualitätsindikatoren verwendet. Die Testdaten wurden aus einer separaten Testdatenmenge geladen und anschließend durch das trainierte Modell klassifiziert.

### Testfall 2: Überprüfung der Trainingsfunktion fit()

Zur Überprüfung der Trainingsfunktion wurde die Laufzeit des Trainings gemessen und mit einer zuvor bestimmten Referenzlaufzeit verglichen. Der Test gilt als bestanden, wenn die gemessene Laufzeit den definierten Grenzwert von 120 % der Referenzlaufzeit nicht überschreitet.

---

## Projektstruktur im Notebook
- **Dekoratoren**: `my_logger`, `my_timer` (schreiben JSON‑Logs in `logs/`)  
- **Wrapperklassen**: `DecisionTreeWrapper`, `RandomForestWrapper` (verwenden die Dekoratoren)  
- **Daten**: `final_data` (eigene Daten oder synthetisch erzeugt im Notebook)  
- **Messung**: Repräsentative `fit()`‑Laufzeit wird einmal gemessen und optional in `rep_runtime.json` gespeichert  
- **Unittests**: Zwei Tests mit `unittest` direkt im Notebook

---
