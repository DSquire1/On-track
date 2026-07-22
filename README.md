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

## Mobiler: tittarvy + lagvyer (valfritt)

Utan konfiguration synkas tittarvyn mellan fönster på samma dator. Med ett gratis
Firebase-projekt (Realtime Database) blir spelet flerspelarläge: kopiera
`firebase-config.example.js` till `firebase-config.js`, fyll i dina värden och ladda upp filen.
Startskärmen visar då rumskod och tre delbara länkar: **📺 Tittarvy** (följer matchen live,
facit dolt) samt **📱 Lag 1/Lag 2** — lagvyer där laget drar i nödbromsen med sin
resmålsgissning, skickar svar på följdfrågor/musikfråga och buzzar i Vem där?, direkt från
mobilen. Spelledaren ser inskickade svar och dömer rätt/fel som vanligt.

## Licens

Koden och det egenskrivna quizinnehållet: © upphovsmannen, alla rättigheter förbehållna.
Kartdata © OpenStreetMap-bidragsgivare, kartplattor © CARTO. Bilder hämtas från Wikipedia/
Wikimedia Commons enligt respektive bilds licens.
