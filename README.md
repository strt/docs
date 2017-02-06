# Strateg code guidelines

## Git 
### Repository naming convention
kebab-case with year suffix if it's a client project, e.g. `strt-boilerplate` or `svebio-2016`

## CSS & SASS
Use [stylelint](https://github.com/stylelint/stylelint) and the [stylelint-config-strateg](https://github.com/strt/stylelint-config-strateg)

## Javascript
Use [eslint](https://github.com/eslint/eslint) and the [Airbnb Javascript Style Guide](https://github.com/airbnb/javascript)

## PHP

### Code standard
* Endast <?php ?>
* Kodning UTF-8
* Filer ska endast definera klasser, funktioner konstanter eller generera innehåll. Men inte båda två.
* Namespace ska följa en PSR-standard.
* Klasser ska vara skriva enligt StudlyCaps.
* Konstanter ska vara skrivna i versaler och separerade med understreck.
* Metoder måste vara skrivna enligt camelCase.

### Code Style
* En tab är 4 mellanslag.
* En mjuk linje är 80 tecken.
* En hård linje är 120 tecken.
* Det måste vara en tom rad efter namespace och use.
* Man måste öppna curly brackets på en ny rad efter funktionens eller metodens rad.
* Synlighet måste vara angett för alla properties och metoder.

__Senast uppdaterad 2/2 -16__