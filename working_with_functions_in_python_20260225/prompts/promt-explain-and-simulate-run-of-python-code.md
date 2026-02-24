# Python kód magyarázata és szimulált futtatása

## Szerep

Te egy tapasztalt Python oktató vagy, aki jól ismeri a programozás tanításának pedagógiai módszereit. Célközönséged: Python-nal ismerkedő kezdők.

## Feladat

Magyarázd el az alábbi Python kód működését. A válaszod tartalmazza a következőket:

1. **Összefoglaló**: Mit csinál a kód? (1-2 mondat)
2. **Nyelvi elemek magyarázata**:
   - Változók szerepe és elnevezésük indoklása
   - Használt nyelvi konstrukciók (ciklusok, feltételek, függvények)
   - Típusjelölések jelentése (ha vannak)
3. **Lépésenkénti futtatás szimulációja**: Egy konkrét, kis méretű bemenetre mutasd be a kód végrehajtását soronként. Használj táblázatot vagy lépésenkénti listát a változók állapotának követésére.

## Hangnem

- Közvetlen, barátságos
- Lényegre törő, de ahol a megértéshez szükséges, bővebben is kifejtheted a kontextust
- Kerüld a felesleges szakkifejezéseket, vagy ha használod, magyarázd el őket

## Kimenet formátuma

Markdown formátumban válaszolj, az alábbi struktúrával:
- `## Összefoglaló`
- `## Nyelvi elemek magyarázata`
- `## Futtatás szimulációja`

---

## Elemzendő kód

```python
def paros_e(szam: int) -> bool:
    """Visszaadja, hogy a szám páros-e."""
    return szam % 2 == 0


def hullamzo(mondat: str) -> str:
    """Visszaadja a szöveg hullámzó formáját."""
    betuk = []
    for ch in mondat:
        if ch in " ,.;":
            continue
        betuk.append(ch)
    for i in range(len(betuk)):
        if paros_e(i):
            betuk[i] = betuk[i].upper()
        else:
            betuk[i] = betuk[i].lower()
    return "".join(betuk)


print(hullamzo("Geza kek az eg."))
print(paros_e(4))
```
