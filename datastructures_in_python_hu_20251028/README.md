# Adatstruktúrák Pythonban - PyLadies Budapest

Ez az anyag a Python beépített adatstruktúráit mutatja be magyar nyelven, gyakorlati példákkal és feladatokkal.

## Notebookok tartalma

### 01 - Listák (`list`)
A lista a Python egyik legalapvetőbb és legsokoldalúbb adatstruktúrája: rendezett, indexelhető, módosítható gyűjtemény, amely eltérő típusú elemeket is tárolhat.

**Témák:**
- Listák inicializálása (`[]` és `list()` konstruktor)
- Elem elérése (indexing), szeletelés (slicing)
- Lista bejárása (elem-alapú, index-alapú, enumerate)
- Elemek hozzáadása (`append`, `insert`, `extend`) és módosítása
- Elemek törlése (`del`, `remove`, `pop`, `clear`)
- Tartalmi ellenőrzések (`all`, `any`)
- List comprehensions (szűrés, transzformáció, feltételes értékadás)
- Listák másolása: shallow copy vs deep copy (mutable vs immutable)
- Gyakorló feladat: maximumkeresés, típusellenőrzés

### 02 - Szótárak (`dict`)
A szótár kulcs-érték párokat tárol, és a Python 3.7-es verziójától megőrzi a beszúrás sorrendjét. Rendkívül gyors kulcs-alapú keresést biztosít.

**Témák:**
- Szótárak inicializálása (`{}` és `dict()` konstruktor)
- Elem elérése, hozzáadása, módosítása (`[]`, `.get()`, `.update()`, merge operátor `|`)
- Hibakezelés hiányzó kulcsoknál (`KeyError`, `defaultdict`)
- Bejárás (kulcsokon, értékeken, kulcs-érték párokon)
- Törlés (`del`, `.pop()`)
- Tartalmi ellenőrzések (`in`, `all`, `any`)
- Dictionary comprehensions (szűrés, transzformáció, kulcs-érték csere)
- Gyakorló feladat: előfordulási gyakoriság számítása

### 03 - Tuple-ök (`tuple`)
A tuple a lista immutable (módosíthatatlan) változata: rendezett, indexelhető, de a létrehozás után nem változtatható meg. Ideális fix adatrekordok és állandó értékek tárolására.

**Témák:**
- Tuple inicializálása (`()` és `tuple()` konstruktor, egyetlen elemű tuple)
- Elem elérése (indexing) és szeletelés (slicing)
- Másolás és összefűzés
- Csomagolás (packing) és kicsomagolás (unpacking)
- Bejárás (iterálás)
- Tartalmi ellenőrzések (`in`, `.count()`, `.index()`)
- Tuple-ök és generátorok (generator expression vs tuple)
- Mikor ajánlott / nem ajánlott a tuple használata

### 04 - Halmazok (`set`)
A halmaz rendezetlen gyűjtemény, amely csak egyedi, immutable elemeket tárolhat. Fő előnye a rendkívül gyors tartalmazás-vizsgálat és a matematikai halmazműveletek támogatása.

**Témák:**
- Set inicializálása (`{}` és `set()` konstruktor, duplikátumok automatikus szűrése)
- Elem hozzáadása (`add`, `update`) és törlése (`remove`, `discard`, `pop`, `clear`)
- Tartalmazás vizsgálata (`in`) és sebesség-összehasonlítás listával
- Halmazműveletek: unió (`|`), metszet (`&`), különbség (`-`), szimmetrikus különbség (`^`)
- Részhalmaz, szuperhalmaz és diszjunkt vizsgálat
- Helyben módosító műveletek (`|=`, `&=`, `-=`)
- Set comprehensions (halmaz-értelmezés)
- Frozenset (módosíthatatlan halmaz, szótárkulcsként való használat)
- Gyakorlati példák: duplikátumok eltávolítása, jogosultság-kezelés, konfigurációellenőrzés
- Mikor ajánlott / nem ajánlott a set használata
- Gyakorló feladatok: szerverszoftverek összehasonlítása, egyedi betűk számlálása
