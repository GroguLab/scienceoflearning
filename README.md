# Science of Learning – órai anyagok

Szemináriumi munkaanyagok a tanulás tudományához (GroguLab, ELTE PPK).
Minden anyagcsomag önállóan működő statikus weboldal: nincs build, nincs függőség,
telefonról QR-kóddal nyitható.

**Élő oldal:** https://grogulab.github.io/scienceoflearning/

## Csomagok

| Mappa | Kurzus | Mi ez |
|---|---|---|
| [`tanulasi-kornyezet/`](tanulasi-kornyezet/) | A tanulás támogatása · OTK-TAN22-109 | Storytelling-alapú tervezőfeladat: persona kártyák, tervezési checklist, befektetői pontozólap, költségkalkulátor, látványterv-galéria |

Új csomag hozzáadása: tegye a saját mappájába, és vegyen fel egy sort a gyökér
`index.html` „Órai anyagcsomagok" szakaszába, valamint ebbe a táblázatba.

## Szerkezet

```
.
├── index.html              gyűjtő főlap – innen nyílik minden csomag
├── .nojekyll               a GitHub Pages ne futtasson Jekyllt
└── tanulasi-kornyezet/     egy teljes anyagcsomag (saját README-vel)
    ├── index.html          oktatói áttekintés
    ├── kontextus.html      kerettörténet – ezt kapják a csoportok elsőként
    ├── persona/            szerepkártyák
    ├── assets/             közös stíluslap és képek
    └── ...                 munkalapok, QR-generátor
```

Minden csomag a saját mappájában zárt egység: a benne lévő oldalak csak egymásra és
a saját `assets/` mappájukra hivatkoznak, így külön is átvihető vagy offline is megnyitható.

## Közzététel (GitHub Pages)

**Settings → Pages → Build and deployment → Source: Deploy from a branch**,
branch: `main`, folder: `/ (root)`, majd *Save*. 1–2 perc múlva él a fenti cím.

## Felhasználás

Az anyagok oktatási célra készültek, szabadon felhasználhatók és átszabhatók a forrás
megjelölésével. A portrék és látványtervek képgenerátorral készültek – nem valós
személyeket és nem valós termeket ábrázolnak. Az árak tájékoztató jellegűek, nem árajánlatok.
