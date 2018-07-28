# [M2 PSMIC] Données culturelles - Cours 1

Ce fichier contient les différents éléments dont vous aurez besoin pour suivre le cours.

## Informations pratiques :
- Enseignant : Karl Pineau
- Contact : karl.pineau@utc.fr

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
  
 - Autre point
