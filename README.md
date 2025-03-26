
# AutoPay Script for ESX

## Leírás
Az AutoPay script automatikus banki levonásokat hajt végre a játékosok bankszámlájáról meghatározott időközönként, figyelembe véve a bankszámla egyenlegét és a tulajdonukban lévő járművek számát. A levont összeg egy részét egy frakció számlájára is átutalja.

## Funkciók
- Automatikus levonás a játékosok bankszámlájáról.
- Levonás mértéke a bankszámla egyenlegétől és a járművek számától függ.
- A levonott összeg egy része a frakció számlájára kerül.
- A levonásokat konfigurálhatod a **config.lua** fájlban.
- A rendszer értesítéseket küld a játékosoknak a levonásról.
- Discord webhook logolás (opcionális, de ki lehet kapcsolni).
  
Config fájl konfigurálása: Nyisd meg a config.lua fájlt és állítsd be a kívánt beállításokat, például a levonás mértékét, a frakció számláját és az értesítési típusokat.

A script indítása: A server.cfg fájlban add hozzá az alábbi sort, hogy a script elinduljon a szerveren:


start supply-tax
Config.lua
A config.lua fájlban a következő beállításokat találod, amiket a saját igényeid szerint módosíthatsz:

LowThreshold: Az alacsony egyenleg határérték.

MediumThreshold: A közepes egyenleg határérték.

HighThreshold: A magas egyenleg határérték.

LowDeduction: Az alacsony egyenlegnél levont összeg.

MediumDeduction: A közepes egyenlegnél levont összeg.

HighDeductionPercent: A magas egyenlegnél levont összeg százaléka.

MinBankBalanceLimit: A minimum bankszámla egyenleg, ami alatt nem történik levonás.

DeductionInterval: A levonások közötti időintervallum másodpercben.

FactionAccount: A frakció számlája, ahova a levont összeg egy része kerül.

FactionSharePercent: A levonott összeg százaléka, ami a frakció számlájára kerül.

A script háromféle értesítést küldhet a játékosoknak:

Venice-notification "codem"

okokNotify  "okok"

ESX alapú notification "esx"

A használni kívánt értesítési rendszert a config.lua fájlban választhatod ki.
