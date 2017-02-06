# Strateg code guidelines

## File structure and naming

## HTML

## SASS/CSS

## JS

## PHP
## Kodstandard
* Endast <?php ?>
* Kodning UTF-8
* Filer ska endast definera klasser, funktioner konstanter eller generera innehåll. Men inte båda två.
* Namespace ska följa en PSR-standard.
* Klasser ska vara skriva enligt StudlyCaps.
* Konstanter ska vara skrivna i versaler och separerade med understreck.
* Metoder måste vara skrivna enligt camelCase.

## Kodstil
* En tab är 4 mellanslag.
* En mjuk linje är 80 tecken.
* En hård linje är 120 tecken.
* Det måste vara en tom rad efter namespace och use.
* Man måste öppna curly brackets på en ny rad efter funktionens eller metodens rad.
* Synlighet måste vara angett för alla properties och metoder.
* true, false och null ska vara med små bokstäver
* extend och implement ska vara på samma rad som klassnamnet
* Properties och Methods ska inte prefix:as med en eller flera underscores
* Methods ska inte ha ett mellanrum mellan namn och parenteser
* Metodargument med defaultvärde ska komma sist i listan.
* Om metodnamn + argument är längre än en mjuk eller hård linje, dela upp argument på ny rad per argument med en indentering, som en metod body. slutparentesen ska ligga på samma rad som öppnings måsvingen för bodyn.
* abstract, final måste vara före synligheten.
* static måste komma efter synligheten.
* vid anrop av metoder ska inte mellanslag finnas, förrutom vid argumentlistning.

## Kontrollstruktur
* elseif ska inte innehålla ett mellanslag
* En switch statement MÅSTE INTE innehålla kommentarer för att visa att den fortsätter längre ner i koden.
* En foreach behöver inte innehålla key variabel.
* Vid osäkra operationer, använd alltid try/catch.

__Senast uppdaterad 6/2 -17__