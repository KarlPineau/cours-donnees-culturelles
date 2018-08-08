**[[M2 PSMIC] Données culturelles](README.md) | [Cours précédent](cours-2.md)**

# Cours 3 : À la découverte du web sémantique

## Informations pratiques :
- Enseignant : Karl Pineau
- Contact : karl.pineau@utc.fr
- Lien vers le support de cours : https://docs.google.com/presentation/d/1ZDMYkDOjlZ_gCxlWWC5aInF9JSoMK7u9IRcSXw9BPOg/edit?usp=sharing

## Structuration des données sémantiques :
- **RDF** : https://fr.wikipedia.org/wiki/Resource_Description_Framework
- **DBpedia** : https://dbpedia.org/

## Les ontologies :
- **Ontologie** : https://fr.wikipedia.org/wiki/Ontologie
    - RDFS : https://www.w3.org/TR/rdf-schema/ | Ontologie de base du web sémantique
    - OWL : https://www.w3.org/TR/owl2-overview/ | Exprime les relations au sein des ontologies
    - SKOS : https://www.w3.org/2004/02/skos/ | Exprime les relations de thésaurus
    - FOAF : http://xmlns.com/foaf/spec/ | Exprime les relations entre personnes
    - FRBR : http://vocab.org/frbr/core.html | Exprime les relations d’ouvrages
    - CIDOC-CRM : http://www.cidoc-crm.org/ | Exprime les connaissances de musées
    - DOREMUS : http://data.doremus.org/ontology/ | Exprime les connaissances en musique 

## Pratique du web sémantique :
- **Wikidata** : https://www.wikidata.org/wiki/Wikidata:Main_Page
- **Page Wikidata de La Joconde** : https://www.wikidata.org/wiki/Q12418
- **Page Wikidata de la déclaration P571, Date de création** : https://www.wikidata.org/wiki/Property:P571

## Le SPARQL EndPoint de Wikidata :
- **SPARQL EndPoint** : https://query.wikidata.org
- Lançons la requête pour obtenir la liste des chats sur Wikidata :

        #Chats
        SELECT ?item ?itemLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q146.
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        }

- Remplaçons les chats par des peintures :

        #Peintures
        SELECT ?item ?itemLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q3305213.
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        } LIMIT 10

- Obtenir les peintures du musée du Louvre :

        #Peintures du Louvre
        SELECT ?item ?itemLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q3305213. #Les items de type "Peinture"
          ?item wdt:P195 wd:Q19675. #Les items dans la collection du musée du Louvre.
          
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        }
        
- Obtenir les peintures du département des peintures du Louvre :

        #Peintures du département des peintures du Louvre
        SELECT ?item ?itemLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q3305213. #Les items de type "Peinture"
          ?item wdt:P195 wd:Q3044768. #Les items dans la collection du département des peintures du musée du Louvre.
          
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        }
     
- Affichons les auteurs des peintures :

        #Peintures du département des peintures du Louvre
        SELECT ?item ?itemLabel ?createurLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q3305213. #Les items de type "Peinture"
          ?item wdt:P195 wd:Q3044768. #Les items dans la collection du département des peintures du musée du Louvre.
          
          OPTIONAL { ?item wdt:P170 ?createur. }
          
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        }

- Les peintures dépeignant un chat :

        #Peintures du département des peintures du Louvre
        SELECT ?item ?itemLabel ?createurLabel 
        WHERE 
        {
          ?item wdt:P31 wd:Q3305213. #Les items de type "Peinture"
          ?item wdt:P195 wd:Q3044768. #Les items dans la collection du département des peintures du musée du Louvre.
          ?item wdt:P180 wd:Q146. # Qui dépeignent un chat
          
          OPTIONAL { ?item wdt:P170 ?createur. }
          
          SERVICE wikibase:label { bd:serviceParam wikibase:language "[AUTO_LANGUAGE],en". }
        }
        
 - Au final :
        
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

## Le SPARQL EndPoint d'Europeana :
- SPARQL EndPoint : http://sparql.europeana.eu/
- Obtenir la liste des concepts présents sur le triplestore :

        select distinct ?Concept where {[] a ?Concept} LIMIT 100
        
- To continue
