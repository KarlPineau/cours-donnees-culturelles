# Cours 2


## SPARQL :
    #Les oeuvres du Louvre dépeignant un chat avec leur photo, leur date et leur auteur
    SELECT ?item ?createurLabel ?itemLabel ?image ?date_de_fondation_ou_de_cr_ation WHERE {
      ?item wdt:P31 wd:Q3305213. # Les objets qui sont des peintures
      ?item wdt:P195 wd:Q3044768. # Qui appartiennent à la collection des peintures du Louvre
      ?item wdt:P180 wd:Q146. # Qui dépeignent un chat

      OPTIONAL { ?item wdt:P170 ?createur. }
      OPTIONAL { ?item wdt:P18 ?image. }
      OPTIONAL { ?item wdt:P571 ?date_de_fondation_ou_de_cr_ation. }

      SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
    }
