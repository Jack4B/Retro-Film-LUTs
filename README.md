# Retro-Film-LUTs – paczka filtrów HaldCLUT PNG

Paczka 260 filtrów filmowych do aplikacji Retro-Film, pobieranych na żądanie. Pliki są
oryginalnymi HaldCLUT z RawTherapee Film Simulation Collection zapisanymi bezstratnie jako PNG.

- 259 filtrów w siatce **144³** (HaldCLUT poziom 12, obraz 1728×1728),
- 1 filtr w siatce **256³** (`negative_color/kodak_ektar_100`, HaldCLUT poziom 16, obraz 4096×4096).
- Łącznie 378 138 252 B PNG.
- Aplikacja pobiera pliki wyłącznie z tagu **`luts-v1`** (nie z `main`):
  `https://raw.githubusercontent.com/Jack4B/Retro-Film-LUTs/luts-v1/<file>`.

## Układ

```
catalog-144.json          katalog: id, displayName, category, file, grid, format, bytes, unpackedLength, sha256
SHA256SUMS                sumy SHA-256 wszystkich plików
luts/<kategoria>/<id>.png HaldCLUT PNG
LICENSE, THIRD_PARTY.md   licencja i atrybucja
```

Kategorie: `bw`, `colorslide`, `instant_consumer`, `instant_pro`, `negative_color`, `negative_new`, `negative_old`.

Po rozpakowaniu każdy filtr to surowe RGB8, `R` zmienia się najszybciej, potem `G`, na końcu `B`;
długość = `grid³ · 3` (`unpackedLength`): 8 957 952 B dla 144³, 50 331 648 B dla 256³.

## Weryfikacja

```sh
git clone --branch luts-v1 https://github.com/Jack4B/Retro-Film-LUTs.git
cd Retro-Film-LUTs
sha256sum -c SHA256SUMS
```

## Licencja i atrybucja

RawTherapee Film Simulation Collection – autorzy: Pat David, Pavlov Dmitry, Michael Ezra
(https://rawpedia.rawtherapee.com/Film_Simulation). Licencja: **CC BY-SA 4.0**
(https://creativecommons.org/licenses/by-sa/4.0/). Paczka jest udostępniana na tej samej licencji – patrz `LICENSE`.
Nazwy filmów są wyłącznie opisowe; brak powiązania z producentami ani ich poparcia.
