# GGV vs. Mieterstrom – Szenariorechner (Streamlit)

Dieses Tool visualisiert die wirtschaftlichen Effekte zweier Modelle innerhalb eines Wohnkomplexes:
- **GGV (gebäudegebäudenahe Versorgung / Kundenanlage)** mit freier interner Preisgestaltung
- **Mieterstrommodell** gemäß § 21 EEG / § 42a EnWG mit Preisdeckel (≤ 90% Grundversorgungstarif) und Mieterstromzuschlag

## Features
- Parametrische Eingaben (kWp, Erträge, EV-Anteil, Preise, CAPEX/OPEX, Degradation, Preis-/Kostenwachstum, Diskontsatz)
- Automatischer **Mieterstrom-Preisdeckel** (90% lokaler Grundversorgungstarif)
- Mieterstromzuschlag auf EV-Mengen
- Cashflow-, kumulierter Cashflow- und Energiefluss-Charts
- Export der Jahreswerte als CSV

## Annahmen & Hinweise
- **Einspeisevergütung**: Eingabe als ct/kWh; ab >100 kWp typ. Direktvermarktung – Vermarktergebühr als Abzug modelliert.
- **Mieterstromzuschlag**: Gilt nur für an Mieter gelieferte **EV-Mengen** (nicht für Einspeisung).
- **0% USt (§ 12 Abs. 3 UStG)** für PV-/Speicher-Lieferung & Installation ist **nicht separat modelliert**, da dies die CAPEX netto reduziert (bitte CAPEX als Netto angeben).
- EV/Einspeiseanteil wird über Slider gesteuert; Batterie/Optimierung kann als Δ-Parameter berücksichtigt werden.
- Vereinfachtes Modell, **keine Rechts- oder Steuerberatung**.

## Installation
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Start
```bash
streamlit run app.py
```
Die App startet im Browser.

## Dateien
- `app.py` – Streamlit-App
- `requirements.txt` – Python-Abhängigkeiten
- `README.md` – diese Anleitung

## Lizenz & Haftung
Ohne Gewähr; Nutzung auf eigenes Risiko. Prüfen Sie projektspezifische EEG-/EnWG-/Messstellenpflichten und lokale Tarife.
