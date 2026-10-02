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

## Hol él ez az anyag

Ez a mappa a [GroguLab/scienceoflearning](https://github.com/GroguLab/scienceoflearning)
repó része, és GitHub Pages-en jelenik meg:

**https://grogulab.github.io/scienceoflearning/tanulasi-kornyezet/**

A repó gyökerében egy gyűjtő főlap van, onnan is ide nyílik az út.

### Az órai használat menete

1. Nyissa meg a `qr.html`-t a fenti élő címen – az alap-URL magától kitöltődik –,
   és nyomtassa ki a kódokat.
2. Órán elég egyetlen kód: a **kerettörténeté** (`kontextus.html`). A csoportok ebből
   olvassák a helyzetet, és ebből nyitják meg a választott szerep kártyáját.
3. A galéria kódját **csak a bemutatók után** ossza ki.

### Ha külön, önálló oldalként szeretné közzétenni

A mappa zárt egység, a benne lévő oldalak csak egymásra hivatkoznak. Töltse fel ennek a
mappának a *tartalmát* (ne magát a mappát) egy új, public repó gyökerébe, majd
**Settings → Pages → Source: Deploy from a branch**, branch: `main`, folder: `/ (root)`.

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
