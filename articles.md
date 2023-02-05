## Artikel 1

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur imperdiet libero ut felis luctus, quis finibus velit luctus. Phasellus iaculis quis tortor ac aliquet. Etiam vulputate accumsan placerat. Suspendisse potenti. Vestibulum volutpat non mauris vel interdum. Maecenas vestibulum odio a ligula egestas, sed molestie nulla blandit. Quisque quis blandit lorem. Ut tincidunt turpis ac risus fermentum hendrerit. Phasellus ut commodo leo. Quisque in sapien commodo, venenatis massa id, viverra ligula. Maecenas dolor ex, pharetra in lorem eget, lacinia sollicitudin tellus. Aliquam dignissim mi vitae egestas ornare.

<button class="read-article" data-article-name="Article 1">Read Article 1</button>

## Artikel 2

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

<button class="read-article" data-article-name="Article 2">Read Article 2</button>

## Artikel 3

Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.

<button class="read-article" data-article-name="Article 3">Read Article 3</button>


<script>
      // Get all buttons
       var buttons = document.querySelectorAll(".read-article");
       var pageLoadTime = new Date(); 
     
       // Loop through buttons
       for (var i = 0; i < buttons.length; i++) {
     
         // Get article name
         var articleName = buttons[i].getAttribute("data-article-name");
     
         // Event listner for button click
         buttons[i].addEventListener("click", function() {
            var clickTime = new Date();
           var readingTime = (clickTime - pageLoadTime) / 1000 / 60;  // convert to minutes 
     
           // Push values to the data layer
           dataLayer.push({
             'event': 'artikel',
             'eventCategory': 'Article',
             'articleName': articleName,
              'readingTime': readingTime 
           });
          console.log(dataLayer);
         });
       }
     
     </script>
