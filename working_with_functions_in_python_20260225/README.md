# Függvények használata Pythonban – PyLadies Budapest

Ez az anyag a Python függvényeinek használatát mutatja be magyar nyelven, gyakorlati példákkal. Egyszerű saját függvényektől indulva érintjük a pozicionális (positional) és kulcsszavas (keyword) argumentumokat, majd rekurzív, illetve magasabb rendű függvényekre és dekorátorokra is kitérünk.

## Notebookok tartalma

### 01 - Már használod a beépített függvényeket
A függvény nem más, mint egy újrahasznosítható kódrészlet, amelyet egyszer megírunk, nevet adunk neki, és annyiszor hívjuk meg, ahányszor szükségünk van rá. Ez a notebook megmutatja, hogy a Python beépített függvényeit valójában már a legelső lépésektől használjuk – és hogyan fedezhetjük fel a többit is.

**Témák:**
- Saját függvény létrehozása (paraméterekkel és visszatérési értékkel, illetve azok nélkül)
- Ismerős beépített függvények: `print()`, `sum()` – ezeket már korábban is használtuk
- Beépített függvények típusának felderítése (`type()`)
- Információszerzés beépített függvényekről (`help()`, hivatalos dokumentáció)
- A `builtins` modul felfedezése (`dir(builtins)`, `help(__builtins__)`)
- Haladó megközelítés: az `inspect` modul használata a beépített függvények és dokumentációjuk kilistázásához

## Környezet előkészítése

A projekt Python **3.14**-et használ, a függőségeket pedig a [uv](https://docs.astral.sh/uv/) kezeli.
A `pyproject.toml` és a `uv.lock` fájlok alapján bárki könnyedén reprodukálhatja a környezetet.

> **Megjegyzés:** A bemutatott példák Python 3.11 vagy újabb verzióval is futtathatók. Az `uv` által kezelt környezet használata nem kötelező – bármilyen Python környezetben futtathatod a notebookokat, amennyiben a megfelelő Python verzió elérhető.

### 1. A `uv` telepítése

Ellenőrizd, hogy telepítve van-e már a `uv`:

```bash
uv --version
```

Ha a parancs nem található vagy hibát ad, telepítsd az alábbi módon:

```bash
# macOS / Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell)
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 2. Projekt környezet létrehozása

Lépj be a projekt könyvtárába, majd futtasd:

```bash
uv sync
```

Ez automatikusan:
- letölti és telepíti a megfelelő Python verziót (3.14), ha még nincs a gépen
- létrehozza a `.venv` virtuális környezetet
- telepíti az összes függőséget a `uv.lock` alapján

### 3. Jupyter notebook indítása

```bash
uv run jupyter notebook
```

Ez elindítja a Jupyter szervert a projekt virtuális környezetével (Python 3.14).

### 4. Használat VS Code / Cursor szerkesztőben

Ha a notebookot VS Code-ban vagy Cursor-ban szeretnéd megnyitni:
1. Nyisd meg a projekt könyvtárat a szerkesztőben
2. Nyiss meg egy `.ipynb` fájlt
3. Jobb felül kattints a kernel selectorra
4. Válaszd: **Python Environments...** → `.venv/bin/python (Python 3.14.0)`
