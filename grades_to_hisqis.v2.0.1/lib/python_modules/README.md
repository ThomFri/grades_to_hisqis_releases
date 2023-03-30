# Oft benötigte Python-Methoden
- Hier gebündelt, um sie über ``git submodule add https://github.com/ThomFri/python_modules.git`` zu clonen...
- ... und über ``from python_modules.<<MODUL>> import <<METHODE>>`` einzubinden

## Module
| Modul      | Kurzbeschreibung                |
|------------|---------------------------------|
| ``file``   | Übernimmt Handling mit Dateien  |
| ``cache``  | Übernimmt Handling des Cache    |
| ``input``  | Zur Abfrage von Nutzereingaben  |
| ``others`` | Weitere kleinere Funktionen     |
| ``output`` | Zur schönen Ausgabe             |


## How to prevent detatched head after cloning

For initing **[Restart PyCharm afterwards!]**
```batch
git submodule add https://github.com/ThomFri/python_modules.git
git submodule update --init --recursive
git submodule foreach "(git checkout master)"

```

For cloning, this helps
```batch
git clone --recursive https://github.com/ThomFri/<<REPO>>.git
cd <<REPO>>
git submodule update --init --recursive
git submodule foreach "(git checkout master)"
```

For (manual) update, this helps:
```batch
git pull
git submodule update
```
