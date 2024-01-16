# Produkt-backlog för MyPokeDB
## 1. Klasser & Struktur
  ### Controllers / Facades
  #### MainFacade
  * Konstruktor skapar instanser av PokeAPIFacade och MongoDBFacade.
  * Metod för att hämta data från PokeAPIFacade och spara returen i MongoDBFacade.
  #### PokeAPIFacade
  * Konstruktor skapar sträng för API-anrop.
  * Metod för att hämta namnen på alla pokemons från APIet.
  * Metod för att hämta specifik information om en pokemon från APIet.
  #### MongoDBFacade
  * Konstruktor skapar en connectionString.
  * Metod för att spara inkommande data i databasen.
  ### Models
  #### Pokemon
  * Konstruktor sparar all inkommande information om Pokemon vid initiering av objektet.
  * Metod fr att omvandla objektet till en sträng.
  * Metod för att skapa ny pokemon.
  * Metod för att ändra information om pokemon.
  #### Database
  * Konstruktor initialiserar objektet och sätter värdet för dess egenskaper.
  * Metod för att konvertera objektet till en sträng.
  * Metod för att hämta pokemons baserat på type.
  * Metod för att hämta pokemons baserat på region.
  * Metod för att hämta pokemon baserat på namn.
  * Metod för att lägga till pokemon i databasen.
  * Metod för att uppdatera pokemon i databasen.
  * Metod för att ta bort pokemon ur databasen.
  ### Views
  #### Pokemon Details View
  * Komponent som läser in detaljerad information om EN pokemon och presenterar den för användaren.
  #### Pokemon List View
  * Komponent som listar pokemon för användaren.
  * Möjlighet till filtrering med Select-element.
  * Skickar input till Databasen, och listar returen.
  #### User Pokemon Collection View
  * Komponent som visar användarens egna pokemons.
  * Presenterar varje pokemon som ett "Card" som har knapparna "redigera" och "radera".
  * Knapp för att skapa ny pokemon.
  #### Confirmation / Error View
  * Komponent för att ge feedback till användaren vid lyckade/misslyckade händelser.
  #### Home View
  * Komponent för applikationens startsida
  
  
