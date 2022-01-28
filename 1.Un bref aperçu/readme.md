# Un bref aperçu

## Traversée et manipulation du DOM

Obtenez l' <button>élément avec la classe 'continue' et changez son code HTML en 'Next Step...'

```javascript
( "button.continue" ).html( "Next Step..." )
```

## Gestion des événements

Affiche l' #banner-messageélément masqué display:nonedans son CSS lorsqu'un bouton #button-containerest cliqué.

```javascript
var hiddenBox = $( "#banner-message" );
$( "#button-container button" ).on( "click", function( event ) {
  hiddenBox.show();
});
```

## Ajax

Appelez un script local sur le serveur /api/getWeather avec le paramètre de requête zipcode=97201 et remplacez le code #weather-tempHTML de l'élément par le texte renvoyé.


```javascript
$.ajax({
  url: "/api/getWeather",
  data: {
    zipcode: 97201
  },
  success: function( result ) {
    $( "#weather-temp" ).html( "<strong>" + result + "</strong> degrees" );
  }
});
```
