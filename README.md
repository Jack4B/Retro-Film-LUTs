# Retro-Film – filtry 144³ PNG (D9)

260 filmów, oryginalne HaldCLUT (RawTherapee Film Simulation Collection), PNG pod nazwami `luts/<kategoria>/<id>.png`.
Łącznie 378138252 B PNG. Po rozpakowaniu: RGB8, R najszybciej, 8957952 B dla 144³ (`unpackedLength` w `catalog-144.json`).
Wyjątki od 144³ (natywnie inny poziom HaldCLUT): negative_color/kodak_ektar_100 (256³).
Weryfikacja: `sha256sum -c SHA256SUMS`. Licencja: CC BY-SA 4.0 (`LICENSE`), atrybucja: Pat David, Pavlov Dmitry, Michael Ezra.
Zbudowane przez `tools/packs/build144png.py` z https://github.com/Jack4B/Retro-Film.
