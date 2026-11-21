# Legends Equipment — Cone & Hopper Volume Calculator

A browser-based engineering tool from **Legends Equipment** that calculates the inside volume of cones and hoppers, and the total weight of material when they are full.

The whole app is a single self-contained file, `index.html`. Nothing to install and no server needed. Open it in any modern browser, or host it on any web page.

## Shapes

1. Round Symmetric Cone
2. Round Symmetric Cone with Sidewall
3. Round Asymmetric Cone (one vertical wall)
4. Round Asymmetric Cone with Sidewall
5. Square / Rectangular Hopper
6. Square / Rectangular Hopper with Sidewall

## Features

- **Input units:** feet, inches, mm, cm or meters.
- **Dimension diagram:** you type the dimensions into boxes placed on the drawing, and it redraws to scale as you type.
- **Linked angle and height:** enter the cone/hopper angle and the height is calculated, or enter the height and the angle is calculated. The angle can be measured from horizontal or from vertical.
- **Volume output:** in ft³, in³, yd³, m³, cm³, liters or US gallons, with a breakdown of each section (cone/hopper and sidewall), the heights and the wall angles. Rectangular hoppers also show the side wall and corner (valley) angles.
- **Material weight:** enter the bulk density in lb/ft³, kg/m³, g/cm³, lb/US gal or lb/in³ and get the total weight when full in lb, kg, short tons or metric tonnes.
- **Job reference:** reference / job #, customer, company, prepared by, material and notes.
- **Customer report:** a branded report with the dimensioned drawing and results. Use **Print / Save as PDF**.
- **Saved calculations:** save, reopen, search and delete jobs. **Export / Import** moves them between computers as a `.json` file.

## Using it

- **Locally:** download `index.html` and double-click it.
- **Hosted:** turn on GitHub Pages for this repository (Settings → Pages → Deploy from branch `main`, folder `/root`). The calculator will then be available at `https://legendsequip.github.io/VolumeCalcs/`.
- **On a website:** upload `index.html` to the site, or embed the hosted page in an `<iframe>`.

> **Saved calculations are stored in each user's own browser.** They are not shared between people or computers. Use **Export** to back them up or share them, and **Import** to load them.

## Formulas

| Section | Formula |
|---|---|
| Round cone (frustum) | `V = π·H·(D² + D·d + d²) / 12` |
| Cylinder sidewall | `V = π·D²·S / 4` |
| Square / rectangular hopper | `V = H·[L·W + l·w + (L+l)·(W+w)] / 6` |
| Box sidewall | `V = L·W·S` |
| Height from angle | `H = run × tan(angle from horizontal)` |
| Weight | `Weight = Volume × bulk density` |

For a symmetric cone or hopper, run = (top − outlet) / 2. For an asymmetric cone, run = (top − outlet).

The results are theoretical volumes for the inside dimensions entered, at 100% level fill, and do not include the outlet spout. Verify critical values before use.

© Legends Equipment
