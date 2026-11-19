# Paediatric Intubation

An offline web app for emergency paediatric airway reference. It is installable on phones and tablets.

- **Lookup:** pick a weight (under 1 year), or an age and a weight (1 year and over). It shows the ETT size and length, laryngoscope blade, Guedel, LMA, iGel and Air-Q sizes, the accessory sizes for the chosen tube's internal diameter, ETT sizes through an LMA, and ventilator starting settings.
- **Tables:** the four equipment tables laid out like the source sheets, with the selected row highlighted.
- **Checklist:** the paediatric intubation checklist as tick boxes, with a reset button.
- **Ventilator:** suggested initial ventilator settings.

## Source

The values were transcribed from photographs of:

- *Paediatric Airway Equipment Quick Reference*, Brighton Anaesthesia / University Hospitals Sussex NHS Foundation Trust (Dr Andrew Kermode, Dr James Andren, Dr Emma Lillie, 2022)
- *Paediatric Intubation Checklist*, St Richard's Hospital, Chichester, version 1.3, April 2024

## ⚠️ Before clinical use

Check every value against the printed originals. Some values had to be inferred from photographs, where cells span several rows. This app is an aide-memoire. It does not replace clinical judgement or local guidelines. The authors of the source sheets have not reviewed it.

Only one value is calculated rather than copied: the tidal volume (5–8 ml/kg × weight).

## Install on a phone

1. Open the GitHub Pages link in **Safari** (iPhone) or **Chrome** (Android).
2. iPhone: tap **Share**, then **Add to Home Screen**. Android: open the **⋮** menu, then **Install app** or **Add to Home screen**.
3. Open it once while you are online. After that it works offline.

## Tube-type guidance (RCUK 2025)

The Lookup and Tables pages present cuffed tubes as the first choice, following Resuscitation Council UK 2025 Paediatric Life Support: use cuffed tracheal tubes for all children over 30 days corrected gestational age, and monitor and limit cuff pressure to the manufacturer's limit. Uncuffed tubes are shown for newborns, babies under 3 kg (no Microcuff size is listed below 3 kg), or when a cuffed tube won't pass. The cuffed formula (age ÷ 4 + 3.5, valid up to 8 years per ERC 2025) is shown alongside the sheet's size for ages 1–8. **All tube sizes are unchanged from the source sheet.** Neither the RCUK 2025 newborn guideline nor the ERC 2025 paediatric guideline gives a newborn tube-size table.

## Printing

The Print button prints every tab (Lookup, Tables, Checklist, Ventilator) in landscape A4, one page each. Lookup is skipped when no patient is selected. Some phones ignore print requests from home-screen apps, iPhone in particular. On those, the app makes the same pages as a PDF instead, so you can use **Share or print PDF** (on iPhone, then tap Print) or **Download PDF**.

The PDF is made on the device with [html2canvas](https://github.com/niklasvh/html2canvas) and [jsPDF](https://github.com/parallax/jsPDF) (both MIT licence). Copies of both are kept in `vendor/` so this works offline.

## Updating

1. Edit the data arrays near the top of the `<script>` block in `index.html` (`T1`, `T2W`, `T2A`, `T3`, `T4`, `CHECK`).
2. Increase `VERSION` in `sw.js` (for example `paw-v2`) so installed copies pick up the change.

## Hosting

The app is static files with no build step. In the repository, go to **Settings → Pages** and set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
