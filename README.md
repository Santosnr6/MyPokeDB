# Planering för MyPokeDB

## 1. Översikt
Detta projekt syftar till att utveckla en ASP.NET-applikation i C# som kommer att fungera som en interaktiv Pokémondatabas. På applikationen kommer användaren bland annat kunna slumpa fram random pokémons, söka efter specifika pokémons, skapa egna pokémons och lägga till dem i sin egen lokala kopia av databasen.

## 2. Krav
  ### Funktionella Krav
  * Sökfunktionalitet:  Användaren skall kunna söka efter specifika pokémons.
  * Slumpgenerator: Användaren skall kunna slumpa fram X antal pokemons aserat på olika parametrar. Tex för att bestämma sitt party för en genomspelning.
  * Listfunktionalitet: Övergripande data om ALLA pokemon skall kunna visas, och filtrerasm av användaren.
  * Dagens pokémon: dagens pokemon skall visas på startsidan, baserat på dagens datum.
  * Databasfunktionalitet: användaren skall kunna skapa en egen "lokal region" där hen kan skapa, redigera och radera egena pokémons.
  ### Icke-funktionella Krav
  * Prestanda: Applikationen skall vara responsiv, snabb och ge relevant feedback.
  * Användarvänlighet: Applikationen skall ha ett enkelt och intuitivt GUI.
  * Säkerhet: Applikationen kommer lagra data om pokémons på ett säkert sätt.
  * Kodkvalité: Enhetstester kommer att appliceras på applikationen.
  * Utbyggbarhet: Applikationens kod skall vara skriven på ett sätt så att nya funktioner enkelt kan läggas till i framtiden.
## 3. Plattform och teknik
  * Utvecklingsmiljö: Microsoft Visual Studio
  * Ramverk: ASP.NET Core
  * Tredjepartstjänster: PokeAPI
  * Dataförvaring: Lagring av data på MongoDB
## 4. Användningsfall
  ### Användningsfall 1: Hämta info om specifik pokémon
  * Aktör: Användaren.
  * Beskrivning: En användare skall kunna söka efter en specifik pokemon på dess namn (ev. även id), och få tillbaks utförlig information om just den.
  ### Användningsfall 2: Visa lista över pokémons
  * Aktör: Användaren.
  * Beskrivning: Användaren skall kunna se en lista över alla tillgängliga pokémons med grundläggande info. Denna lista skall även kunna filtreras baserat på region.
  ### Användningsfall 3: Generera slumpmässiga pokémons
  * Aktör: Användaren.
  * Beskrivning: Användaren skall kunna generera fram slumpmässiga pokémons, baserat på parametrar som användaren anger.
  ### Användningsfall 4: Hantera egna pokémons
  * Aktör: Användaren, Databasen.
  * Beskrivning: Användaren skall kunna skapa, uppdatera, eller radera egena pokémons från databasen. Användaren anger information som sedan sparas i databasen.
## 5. Tasks för användningsfall
  ### Användningsfall 1:
  * Designa en input-funktion som tar emot användarens sökparametrar.
  * Implementera funktion som söker i databasen med hjälp av input från användaren.
  * Presentera resultat från sökningen:
    - Om pokémon hittades: Detaljerad information om pokémon.
    - Om pokémon ej hittades: Feedback till användaren.
  ### Användningsfall 2: 
  * Designa en input funktion där användaren kan ange vilken regions pokémon he vill lista.
  * Implementera funktion som läser användarens input, och baserat på den hämtar pokémons från databasen.
  * Presentera resultat för användaren
  ### Användningsfall 3: 
  * Designa en input-funktion där användaren kan välja att ange X antal parametrar som bas för slumpgeneratorn.
  * Implementera en funktion som söker ut alla pokémons i databasen som passar in på parametrarna, och sedan slumpar fram önskat antal.
  * Presentera resultat från genereringen:
    - Om generering lyckades: Presentera pokemons på ett tillfredsställande sätt.
    - Om genereing misslyckades: Ge feedback till användaren.
  ### Användningsfall 4: 
  * Implementera en "databas-sida" för användaren där hen kan välja att se sina skapade pokémons, eller att skapa ny pokémon.
  * Implementera en input-funktion som läser informaton om användarens nya pokémon, och sedan sparar den till databasen.
  * Implementera en input-funktion som först läser in information om vald pokémon, och sedan låter användaren redigera informationen som sparas i databasen.
  * Implementera funktion som tar bort vald pokémon ur databasen.
    
