**[[M2 PSMIC] Données culturelles](README.md)**

# Cours 1 : Introductions aux données culturelles, données structurées & APIs

Ce fichier contient les différents éléments dont vous aurez besoin pour suivre le cours.

## Informations pratiques :
- Enseignant : Karl Pineau
- Contact : karl.pineau@utc.fr
- Lien vers le slide : https://docs.google.com/presentation/d/16W1VXVP69y_zSfwEqcJYAe3dPIOfFdhl0Er_LtLlngY/edit?usp=sharing

## Les pourvoyeurs de données culturelles :
- Les "galleries" :
  - **INHA** : https://www.inha.fr/, à travers AGORHA : http://agorha.inha.fr/ | L'Institut National d'Histoire de l'Art est l'une des principales institutions européennes produisant des données sur l'histoire de l'art
  - **Europeana** : https://www.europeana.eu/ | Europeana est la bibliothèque numérique de l'Union Européenne. Elle a vocation à donner accès et à valoriser la culture et l'histoire européenne au sens large
  - **Biblissima** : http://beta.biblissima.fr/ | Biblissima est une bibliothèque numérique française spécialisée dans la valorisation des collections de manuscrits.
- Les biblothèques :
  - **data.BNF**, **Gallica** : http://data.bnf.fr/ & http://gallica.bnf.fr | Plus besoin de présenter Gallica... data.bnf étant le référentiel de la BNF en matière d'oeuvres et de personnes
  - **NumeLyo** : http://numelyo.bm-lyon.fr/ | Numelyo est la bibliothèque numérique de la ville de Lyon
  - **Library of Congress** : https://www.loc.gov/ | Bibliothèque du congrès américain
  - Et puis aussi tout ça : https://en.wikipedia.org/wiki/List_of_digital_library_projects
- Les archives :
  - **Archives nationales** : http://www.archives-nationales.culture.gouv.fr/ | Qui numérisent de plus en plus leurs archives
  - **France Archives** : https://francearchives.fr/ | La "bibliothèque numérique" des archives françaises
  - **Archives départementales des Yvelines** : http://archives.yvelines.fr/ | Une institution archivistique particulièrement à la pointe en matière de crowdsourcing culturelle, à travers Adopte un poilus notamment
  - **Mémoire des Hommes** : http://memoiredeshommes.sga.defense.gouv.fr/ | Un site du ministère des armées qui référence tous les soldats morts pour la France et qui est particulièrement à la pointe en terme de crowdsourcing
- Les musées :
  - **Musée de Bretagne** : http://www.collections.musee-bretagne.fr/ | Un des rares musées français à proposer ses données en open data
  - **British Museum** : https://collection.britishmuseum.org
  - **Metropolitan Museum** : https://www.metmuseum.org/
  - **Rijksmuseum** : https://www.rijksmuseum.nl/en/
- Les projets de recherche universitaire :
  - **Isidore & Huma-Num** : http://huma-num.fr | La Très Grande Infrastructure de Recherche qui permet à de nombreux projets de recherche d'exister
  - **DARIAH-EU** : https://www.dariah.eu/ | La structure européenne qui héberge et finance un grand nombre de projets
  - **Venice Time Machine** : https://vtm.epfl.ch/ | Un projet de numérisation de la ville de Venise à différentes époques
  - **Persée** : http://data.persee.fr/ | Bibliothèque numérique de revues scientifiques
- Les référentiels :
  - **VIAF** : https://viaf.org/ | Référentiel américain des personnalités
  - **AAT** & **ULAN** : http://www.getty.edu/research/tools/vocabularies/ulan/index.html | Deux référentiels incontournables du Getty sur les techniques et sur les artistes
  - **IdRef** : https://www.idref.fr/ | Référentiel sur les auteurs
  - **Geonames** : http://geonames.org/ | Référentiel sur les lieux
- Les autres :
  - **Wikidata** : https://www.wikidata.org/ | Wikidata est devenue en 5 ans LA base de référence pour les données culturelles. C'est l'équivalent de Wikipédia pour les données
  - **DBpedia** : https://dbpedia.org/ | DBpedia est l'un des premiers projets sur les données à émerger, basé sur les données de Wikipédia
  - **data.gouv.fr** & **data.culture.gouv.fr** : http://data.culture.gouv.fr/ | Référence tous les jeux de données publics sur la culture
  - **Les bases du Ministère : Joconde, Mérimée, Palissy, POP, Moteur Collections** : http://collections.culture.fr/ | Référence toutes les collections françaises.

## Exploiter des jeux de données existants :
- Où trouver des données : http://data.gouv.fr, http://data.culture.gouv.fr, http://data.bnf.fr, [Github (Archives nationales)](https://github.com/ArchivesNationalesFR)
- Structurer en format CSV :

      Léonard, Peintre, 1452
      Brunelleschi, Architecte, 1377
      Michel-Ange, Sculpteur, 1475

- Visualiser des données CSV : https://databasic.io/en/wtfcsv

## Récupérons des données - Jouons avec les APIs :
- Les APIs :
  - URL de l'API Google : https://www.google.com/maps/search/?api=1&query=Paris
  - URL de l'API Geonames : http://api.geonames.org/getJSON?formatted=true&geonameId=2988507&lang=fr&username=demo&style=full
- Postman :
  - URL de téléchargement de Postman : https://www.getpostman.com/apps
- Gallica :
  - URL de la documentation de l'API Gallica : http://api.bnf.fr/api-document-de-gallica
  - URL OAI-PMH de Gallica : https://gallica.bnf.fr/services/OAIRecord

## Glossaire des données culturelles :
- Les ARK :
  - Exemple d'ARK de la BNF : `ark:/12148/bpt6k5738219s`
  - Exemple d'URL utilisant un ARK de la BNF : https://gallica.bnf.fr/ark:/12148/bpt6k5738219s
- IIIF :
  - Exemple d'image rendue par un serveur IIIF : https://media.nga.gov/iiif/public/objects/1/0/6/3/8/2/106382-primary-0-nativeres.ptif/full/full/0/default.jpg
  - Appliquons une petite modification à la fin de l'URL de cette image : https://media.nga.gov/iiif/public/objects/1/0/6/3/8/2/106382-primary-0-nativeres.ptif/full/full/0/gray.jpg
  
## Retour aux APIs :
- Une requête sur Gallica : https://gallica.bnf.fr/services/OAIRecord?ark=bpt6k5738219s
- Le résultat obtenu :


        <?xml version="1.0" encoding="UTF-8"?>
        <results ResultsGenerationSearchTime="0:00:00.027" countResults="1" resultType="CVOAIRecordSearchService" searchTime="">
            <visibility_rights>all</visibility_rights>
            <notice>
                <record>
                    <header>
                        <identifier>oai:bnf.fr:gallica/ark:/12148/bpt6k5738219s</identifier>
                        <datestamp>2018-04-26</datestamp>
                        <setSpec>gallica:theme:8:84</setSpec>
                        <setSpec>gallica:typedoc:monographies</setSpec>
                    </header>
                    <metadata>
                        <oai_dc:dc xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:oai_dc="http://www.openarchives.org/OAI/2.0/oai_dc/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.openarchives.org/OAI/2.0/oai_dc/ http://www.openarchives.org/OAI/2.0/oai_dc.xsd">
                            <dc:identifier>https://gallica.bnf.fr/ark:/12148/bpt6k5738219s</dc:identifier>
                            <dc:title>La plage d'Etretat par l'auteur de "Monsieur X et Mme ***"</dc:title>
                            <dc:publisher>Michel Levy (Paris)</dc:publisher>
                            <dc:date>1868</dc:date>
                            <dc:format>In-18</dc:format>
                            <dc:language>fre</dc:language>
                            <dc:language>français</dc:language>
                            <dc:relation>Notice du catalogue : http://catalogue.bnf.fr/ark:/12148/cb33539190h</dc:relation>
                            <dc:type xml:lang="eng">text</dc:type>
                            <dc:type xml:lang="fre">monographie imprimée</dc:type>
                            <dc:type xml:lang="eng">monographie imprimée</dc:type>
                            <dc:source>Bibliothèque nationale de France, département Littérature et art, Y2-59413</dc:source>
                            <dc:rights xml:lang="fre">domaine public</dc:rights>
                            <dc:rights xml:lang="eng">public domain</dc:rights>
                            <dc:format>Nombre total de vues :  374</dc:format>
                            <dc:description>Contient une table des matières</dc:description>
                            <dc:description>Avec mode texte</dc:description>
                        </oai_dc:dc>
                    </metadata>
                </record>
            </notice>
            <provenance>bnf.fr</provenance>
            <sdewey>84</sdewey>
            <dewey>8</dewey>
            <source>Bibliothèque nationale de France, département Littérature et art, Y2-59413</source>
            <typedoc>monographie</typedoc>
            <nqamoyen>92.57</nqamoyen>
            <mode_indexation>text</mode_indexation>
            <title>La plage d'Etretat par l'auteur de "Monsieur X et Mme ***"</title>
            <date nbIssue="1">1868</date>
            <first_indexation_date>03/05/2010</first_indexation_date>
        </results>
  
- Requête en JSON : https://media.nga.gov/public/manifests/nga_highlights.json
- Extrait du code JSON obtenu :

      {
          "@context": "http://iiif.io/api/presentation/2/context.json",
          "@id": "https://media.nga.gov/public/manifests/nga_highlights.json",
          "@type": "sc:Manifest",
          "logo": "https://www.nga.gov/content/dam/ngaweb/imgs/NGAEB.jpg",
          "label": "National Gallery of Art Collection Highlights",
          "metadata": [
              {
                  "label": "Description",
                  "value": "Highlights from the collection of the National Gallery of Art"
              }
          ],
          "description": "A selection of highlights from the National Gallery of Art",
          "guid": "e61700b6-7cb9-4c14-92ab-4246a345ec71",
          "viewingDirection": "left-to-right",
          "viewingHint": "individuals"
      }

## Sauvegarder les données récupérées :
- Télécharger SublimeText : https://www.sublimetext.com/
- Le menu de SublimeText pour modifier le langage utilisé : View > Syntax [> Javascript > JSON]
