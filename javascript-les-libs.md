# javascript-selected-libraries

e document liste les librairies utilisées chez [Steamulo](http://www.steamulo.com/) (et celles à fuir), dans un but d'unification de nos stacks entre les projets.
C'est un document vivant, qui référence nos débats passés ou à venir, et les librairies à surveiller.

## Common

### [Fetch](https://developer.mozilla.org/fr/docs/Web/API/Fetch_API)
+ \+ standard ES 6
+ \+ Fonctionne avec des promesses

En cas de besoin plus poussés, on utilise Axios

### [Axios](https://github.com/mzabriskie/axios)
+ \+ Fonctionne dans le navigateur et dans Node
+ \+ Permet de transformer la requête avant envoi et la réponse reçue
+ \+ Permet l'annulation d'une requête

### [Moment](http://momentjs.com/)
+ Gestion/manipulation/comparaison de dates
+ [Moment-timezone](http://momentjs.com/timezone/) ajoute la gestion de la zone.

:eyes: A tester: [date-fns](https://date-fns.org/), moins lourd, immutable & pure.

### [lodash](https://lodash.com/)
+ Peu utilisé, la plupart des fonctions sont présentes dans ES6
+ Penser à [Lodash-fp](https://github.com/lodash/lodash/wiki/FP-Guide) en cas d'utilisation poussée de programmation fonctionnelle

### [Highcharts](https://www.highcharts.com/)
+ Rendus de graphiques. Très complet, avec beaucoup de types de graphiques différents

### [Swiper](http://idangero.us/swiper/)
+ Créer toute sorte de carousel.
+ \+ N'utilise pas de librairie extérieure
+ \+ Gère le touch
+ \+ Layout à base de flexbox
+ \+ Lazy loading d'images



## Angular JS
### [Angular-swiper](https://github.com/ksachdeva/angular-swiper)
+ Utiliser Swiper dans AngularJS

### [ng-translate](https://angular-translate.github.io/)
+ Traductions

### ng-resource
+ Utile avant Fetch

### [angular-material](https://material.angularjs.org/latest/)
+ Implémentation material design de bonne qualité

### [angular-bootstrap](https://angular-ui.github.io/bootstrap/)
+ Utilisation des composants Bootstrap



## Angular ( > v2)
### [Ngrx-store](https://github.com/ngrx/platform)
+ Implémentation de Flux pour Angular
+ \+ Utilise [RxJS](https://github.com/reactivex/rxjs) de manière intensive,
ce qui permet d'avoir des mises à jour en flux continu
+ \- Pour garder une cohérence technique dans les services, il vaut mieux utiliser RxJS dans les différents services du projet
+ :question: Y-a-t-il un équivalent à Redux-SAGA ?



## React
### [Redux](http://redux.js.org/)
+ Implémentation de Flux pour React
+ Pour créer un store ; découpler les données de leur affichage.
+ Eviter le passage de données et callback entre les composants.
+ Attention à bien découper les composants en 2 types : "presentational" / "container"
+ :question: Avec Redux-SAGA ou avec Redux-thunk ?

### [Material-ui](https://github.com/callemall/material-ui)
+ :warning: **À ne pas utiliser** car le code généré n'est pas propre et pas entièrement customisable.


### [Isomorphic-fetch](https://github.com/matthew-andrews/isomorphic-fetch)
:question: Y-a-t-il un intérêt par rapport à Fetch ?

### [React-bootstrap](https://react-bootstrap.github.io/)
:question: A voir ce que ça vaut ?

## Vue
### [Vuex](https://github.com/vuejs/vuex)
+ Implémentation de Flux pour Vue

:question: Y-a-t-il un équivalent à Redux-SAGA ?

### [Vue-resource](https://github.com/pagekit/vue-resource)
:warning: [Déprécié](https://medium.com/the-vue-point/retiring-vue-resource-871a82880af4), il faut plutôt lui préférer Axios.



## [JQuery](https://jquery.com/)
Nothing, I loved you, but it's 2017 and I can't make SPAs with you.
