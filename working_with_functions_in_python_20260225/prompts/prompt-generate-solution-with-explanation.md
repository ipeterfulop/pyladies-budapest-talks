# Feladat megoldásának generálása és elmagyarázása


## Szerep

Te egy tapasztalt Python oktató vagy, aki jól ismeri a programozás tanításának pedagógiai módszereit. Célközönséged: Python-nal ismerkedő kezdők. Egy programozási feladat megoldását kell kigenerálnod és elmagyarázd a megoldás felépítésének lépéseit, indokoltságát. 

## Feladat (közepes-nehéz)

Old meg az alábbi programozási feladatot:

```{text}
## Feladat: Spirális mátrix bejárás

Adott egy **n × n méretű mátrix** (négyzetes táblázat), amely egész számokat tartalmaz. A mátrix valójában egy lista, ami további listákat tartalmaz – minden belső lista egy sor.

**Példa egy 4×4-es mátrixra:**

```
┌────┬────┬────┬────┐
│  1 │  0 │  1 │  4 │  ← 1. sor
├────┼────┼────┼────┤
│  2 │ -1 │  0 │  3 │  ← 2. sor
├────┼────┼────┼────┤
│  7 │  1 │  0 │  1 │  ← 3. sor
├────┼────┼────┼────┤
│  2 │ -1 │  0 │  5 │  ← 4. sor
└────┴────┴────┴────┘
```

Python-ban ez így néz ki:

```python
matrix = [
    [ 1,  0,  1,  4],
    [ 2, -1,  0,  3],
    [ 7,  1,  0,  1],
    [ 2, -1,  0,  5],
]
```

**A feladat:** Járd be a mátrix elemeit **spirálisan, az óramutató járásának megfelelően** (kívülről befelé haladva), és gyűjtsd össze az elemeket egy listába!

**A bejárás iránya:**

```
→ → → → ↓
        ↓
↑ → → ↓ ↓
↑ ↑ ← ← ↓
↑       ↓
← ← ← ← ←
```

**Lépések:**
1. Felső sor balról jobbra: `1, 0, 1, 4`
2. Jobb oszlop fentről le: `3, 1, 5`
3. Alsó sor jobbról balra: `0, -1, 2`
4. Bal oszlop lentről fel: `7, 2`
5. Folytatás befelé haladva: `-1, 0, 0, 1`

**Eredmény:**

```python
[1, 0, 1, 4, 3, 1, 5, 0, -1, 2, 7, 2, -1, 0, 0, 1]
``` 


Generáld ki a feladatot megoldó kódot és Magyarázd el a kód működését, az algoritmus felépítésének indoklását. A válaszod tartalmazza a következőket:

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