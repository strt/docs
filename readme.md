# Strateg code of conduct

## Contents
<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<!-- https://github.com/thlorenz/doctoc -->

- [Git](#git)
- [JavaScript](#javascript)
- [SASS and CSS](#sass-and-css)
  - [Style](#style)
  - [Naming convention](#naming-convention)
- [PHP](#php)
  - [Kodstandard](#kodstandard)
  - [Kodstil](#kodstil)
  - [Kontrollstruktur](#kontrollstruktur)
  - [Autoloading](#autoloading)
  - [HTTP-Message](#http-message)
  - [Dokumentering](#dokumentering)
- [SiteVision](#sitevision)
  - [Dokumentering](#dokumentering-1)
  - [Kodstil](#kodstil-1)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Git
+ `kebab-case` repository names with year suffix if it's a client project, e.g. `boilerplate` or `svebio-2016`
+ Commit often and after each added/updated feature
+ Don't push broken code
+ Write present-tense, imperative-style commit messages. `Add`, `Fix`, `Refactor` etc
+ Every project should contain a readme that describes how to set-up the project  

## JavaScript
Use [eslint](https://github.com/eslint/eslint) with the [Airbnb](https://github.com/airbnb/javascript) preset

## SASS and CSS
### Style
Use [stylelint](https://github.com/stylelint/stylelint) and the [stylelint-config-strateg](https://github.com/strt/stylelint-config-strateg) preset

### Naming convention
BEM – read more about it [here](http://getbem.com/introduction/)

#### camelCase class names
###### ✅ Good
``` SASS
.searchBar {}
```

###### ❌ Bad 
``` SASS
.search-bar {}
.search_bar {}
// etc
```

#### Don't use id selectors
###### ✅ Good
``` SASS
.header {}
```

###### ❌ Bad 
``` SASS
#header {}
```

#### Only nest class names one level
###### ✅ Good
``` SASS
.nav {
  &__list {
    list-style: none;
  }

  &__item {
    display: inline-block;
  }
}
```

###### ❌ Bad 
``` SASS
.nav {
  &__list {
    list-style: none;
  }

  &__list__item {
    display: inline-block;
  }
}
```

#### Place modifiers at the bottom
###### ✅ Good
``` SASS
.hero {
  display: flex;

  &.-large {
    min-height: 100vh;
  }
}
```

###### ❌ Bad 
``` SASS
.hero {
  &.-large {
    min-height: 100vh;
  }

  display: flex;
}
```

#### Place breakpoints at the bottom of the current selector
###### ✅ Good
``` SASS
.hero {
  display: flex;

  @include breakpoint(mobile) {
    flex-flow: column wrap;
  }

  // Place modifiers below block or element breakpoints
  &.-large {
    min-height: 100vh;

    @include breakpoint(mobile) {
      min-height: 60vh;
    }
  }
}
```

###### ❌ Bad 
``` SASS
.hero {
  display: flex;

  &.-large {
    min-height: 100vh;
  }

  @include breakpoint(mobile) {
    flex-flow: column wrap;

    &.-large {
      min-height: 60vh;
    }
  }
}
```

## PHP
### Kodstandard
* Endast <?php ?>
* Kodning UTF-8
* Filer ska endast definera klasser, funktioner konstanter eller generera innehåll. Men inte båda två.
* Namespace ska följa en PSR-standard.
* Klasser ska vara skriva enligt StudlyCaps.
* Konstanter ska vara skrivna i versaler och separerade med understreck.
* Metoder måste vara skrivna enligt camelCase.
* Variabler och properties måste var skrivna enligt camelCase.

### Kodstil
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

### Kontrollstruktur
* elseif ska inte innehålla ett mellanslag
* En switch statement MÅSTE INTE innehålla kommentarer för att visa att den fortsätter längre ner i koden.
* En foreach behöver inte innehålla key variabel.
* Vid osäkra operationer, använd alltid try/catch.
* Vid definition av funktion eller method ska inte ett mellanrum mellan funktion-namn och argumentlistning finnas.

### Autoloading
* Hänvisas till www.php-fig.org

### HTTP-Message
* I störta utsträckning, använd http koder för return meddelanden.
* Hänvisas till www.php-fig.org

### Dokumentering
* Skall följa den standard som används av PHPDoc.
* Ett block av dokumentering ska alltid innehålla Author, Param och Return om detta är applicerbart.
* Ett block ska alltid finnas för metoder och funktioner.
* Man måste inte använda inline kommentarer. Dessa skrivs med //.

## SiteVision
### Dokumentering
* Ska följa standarden enligt [jsdoc](http://usejsdoc.org/)
* En scriptmodul ska alltid i toppen ha ett block med author, description och versionsnummer av SV.

### Kodstil
* Använd endast det officiella publika API:et.
* All kod ska wrappas i en self-invoking function.
