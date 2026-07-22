# OnTrack 🚆

Ett webbaserat frågesportspel för två lag, inspirerat av tågresequizzens klassiska upplägg:
resor mot hemliga resmål via en fallande ledtrådsstege (10 → 8 → 6 → 4 → 2 poäng), nödbroms,
följdfrågor, musikfrågor och specialmoment (Vem där?, Listan, Närmast vinner).

**Detta är ett inofficiellt fan-projekt.** Det är inte anslutet till, godkänt av eller kopplat
till SVT eller programmet *På spåret*. Samtliga resor, ledtrådar, frågor och moment i detta
repo är egenskrivna och faktakollade mot öppna källor.

## Spela

Öppna `index.html` (eller den publicerade sidan) i en webbläsare. En person agerar spelledare:

1. Välj tre resor och upp till tre specialmoment på startskärmen.
2. Öppna **📺 Tittarvy** i ett eget fönster och lägg på projektor/andra skärm — den döljer facit.
3. Lagen "drar i nödbromsen" för att låsa en gissning på aktuell poängnivå; rättning sker när
   båda lagen gissat. Följdfrågor besvaras av båda lagen parallellt.

Kartan i *Närmast vinner* och bilderna i *Listan* hämtas från internet (CARTO/OpenStreetMap
respektive Wikipedia) och har offline-fallback.

## Innehåll

Spelinnehållet ligger i `resor-data.js` och genereras från en lokal kunskapsbas (ingår ej i
repot).

## Fjärrtittarvy på deltagarnas mobiler (valfritt)

Utan konfiguration synkas tittarvyn mellan fönster på samma dator. För att deltagare ska kunna
följa matchen live i sina mobiler: skapa ett gratis Firebase-projekt med Realtime Database,
kopiera `firebase-config.example.js` till `firebase-config.js`, fyll i dina värden och ladda
upp filen. Spelledarvyn visar då en rumskod (📡) — klicka för att kopiera tittarlänken.

## Licens

Koden och det egenskrivna quizinnehållet: © upphovsmannen, alla rättigheter förbehållna.
Kartdata © OpenStreetMap-bidragsgivare, kartplattor © CARTO. Bilder hämtas från Wikipedia/
Wikimedia Commons enligt respektive bilds licens.
