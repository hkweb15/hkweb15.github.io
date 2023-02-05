## Artikel 1

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur imperdiet libero ut felis luctus, quis finibus velit luctus. Phasellus iaculis quis tortor ac aliquet. Etiam vulputate accumsan placerat. Suspendisse potenti. Vestibulum volutpat non mauris vel interdum. Maecenas vestibulum odio a ligula egestas, sed molestie nulla blandit. Quisque quis blandit lorem. Ut tincidunt turpis ac risus fermentum hendrerit. Phasellus ut commodo leo. Quisque in sapien commodo, venenatis massa id, viverra ligula. Maecenas dolor ex, pharetra in lorem eget, lacinia sollicitudin tellus. Aliquam dignissim mi vitae egestas ornare.

<button class="read-article" data-article-name="Article 1">Read Article 1</button>
<button class="order">Beställ</button>

## Artikel 2

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur imperdiet libero ut felis luctus, quis finibus velit luctus. Phasellus iaculis quis tortor ac aliquet. Etiam vulputate accumsan placerat. Suspendisse potenti. Vestibulum volutpat non mauris vel interdum. Maecenas vestibulum odio a ligula egestas, sed molestie nulla blandit. Quisque quis blandit lorem. Ut tincidunt turpis ac risus fermentum hendrerit. Phasellus ut commodo leo. Quisque in sapien commodo, venenatis massa id, viverra ligula. Maecenas dolor ex, pharetra in lorem eget, lacinia sollicitudin tellus. Aliquam dignissim mi vitae egestas ornare.

<button class="read-article" data-article-name="Article 2">Read Article 2</button>
<button class="order">Beställ</button>

## Artikel 3

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur imperdiet libero ut felis luctus, quis finibus velit luctus. Phasellus iaculis quis tortor ac aliquet. Etiam vulputate accumsan placerat. Suspendisse potenti. Vestibulum volutpat non mauris vel interdum. Maecenas vestibulum odio a ligula egestas, sed molestie nulla blandit. Quisque quis blandit lorem. Ut tincidunt turpis ac risus fermentum hendrerit. Phasellus ut commodo leo. Quisque in sapien commodo, venenatis massa id, viverra ligula. Maecenas dolor ex, pharetra in lorem eget, lacinia sollicitudin tellus. Aliquam dignissim mi vitae egestas ornare.

<button class="read-article" data-article-name="Article 3">Read Article 3</button>
<button class="order">Beställ</button>


<script>
      // Get all buttons
      var buttons = document.querySelectorAll(".read-article");
        var pageLoadTime = new Date(); 

    for (var i = 0; i < buttons.length; i++) {
       var articleName = buttons[i].getAttribute("data-article-name");

     buttons[i].addEventListener("click", (function(articleName) {
     return function() {
        var clickTime = new Date();
        var readingTime = (clickTime - pageLoadTime) / 1000 / 60;  // convert to minutes 

       // Push values to the data layer
        dataLayer.push({
        'event': 'read_article',
        'eventCategory': 'lasta_artiklar',
        'artikelnamn': articleName,
        'lastid': readingTime 
       });
        console.log(dataLayer);
      };
    })(articleName));
  }
</script>
