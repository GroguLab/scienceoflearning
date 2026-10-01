# Tanulási környezetek tervezése – órai anyagok

Statikus weboldal az **A tanulás támogatása** (OTK-TAN22-109, ELTE PPK) szeminárium
storytelling-alapú tervezőfeladatához. Telefonról, QR-kóddal nyitható.

## Mit tartalmaz

| Oldal | Kinek | Mire |
|---|---|---|
| `kontextus.html` | **a csoportoknak, elsőként** | kerettörténet + szerepválasztás: innen nyílik a választott megrendelő kártyája |
| `index.html` | oktatónak | áttekintés, innen nyílik minden |
| `persona/csaba.html`, `laura.html`, `daniel.html`, `nora.html` | tervezőcsapatoknak | persona kártyák portréval, saját szavas megszólalással, igényekkel és tervezési kihívással |
| `persona/befektetok.html` | befektetői csoportnak | a szerep leírása és a három munkaanyag |
| `checklist.html` | mindenkinek | egyoldalas tervezési ellenőrzőlista (A4-re nyomtatható) |
| `befektetoi-lap.html` | befektetőknek | pontozólap szintleírásokkal + automatikus 50M-elosztó |
| `koltsegtabla.html` | tervezőcsapatoknak | tájékoztató egységárak + eszközkalkulátor |
| `galeria.html` | **csak a bemutatók után** | a négy AI-val generált látványterv, kísérőszöveg nélkül |
| `qr.html` | oktatónak | QR-kódok generálása és nyomtatása |

Nincs build, nincs függőség: sima HTML + egy CSS + néhány soros JS.
A QR-oldal egyetlen külső könyvtárat tölt be CDN-ről (qrcode-generator, MIT); minden más offline is működik.

## Közzététel GitHub Pages-en

1. Új repó a GitHubon (pl. `tanulasi-kornyezet`), **Public**.
2. Töltse fel ennek a mappának a *tartalmát* (ne magát a mappát): `index.html`, `assets/`, `persona/`, a többi `.html` és ez a README.
   Böngészőből: *Add file → Upload files*, majd a mappákat is be lehet húzni.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch: `main`, folder: `/ (root)`. *Save*.
4. 1–2 perc múlva él: `https://FELHASZNALONEV.github.io/tanulasi-kornyezet/`
5. Nyissa meg a `qr.html`-t ezen a címen – az alap-URL magától kitöltődik –, és nyomtassa ki a kódokat.
6. Órán elég egyetlen kód: a **kontextus kártyáé**. A csoportok ebből olvassák a helyzetet,
   és ebből nyitják meg a választott szerep kártyáját. A galéria kódját csak a bemutatók után ossza ki.

## Mit érdemes testre szabni

- **Persona-szövegek:** `persona/*.html`, a szöveg közvetlenül a HTML-ben van.
- **Színek:** `assets/style.css` tetején, a `:root` blokkban (minden personának saját színe van).
- **Pontozás és keretösszegek:** `befektetoi-lap.html` alján, a script elején:
  `BASE` (alapkeret, 20 M), `PERF` (teljesítménykeret, 30 M), `STEP` (kerekítés, 0,5 M).
- **Árak:** `koltsegtabla.html`, a táblázat sorai. Az `f` jelölés ellenőrzött webshop-árat,
  a `b` nagyságrendi becslést jelent.

## Forrásokról

Az árak 2026. októberi magyar webshopárak alapján, tájékoztató jelleggel szerepelnek – nem árajánlatok.
A checklist hivatkozásai: Barrett és mtsai (2015); Shield & Dockrell (2008); ANSI/ASA S12.60-2010;
Wannarka & Ruhl (2008); Kariippanon és mtsai (2021); Dumont, Istance & Benavides (2010).
A portrék és a látványtervek képgenerátorral készültek, nem valós személyeket és nem valós termeket ábrázolnak.
