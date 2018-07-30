# Nettoyer et aligner des données
Rendre les données exploitables

## Installons quelques logiciels pour nettoyer nos données
- Pour commencer, nous allons devoir utiliser Python : https://www.python.org/downloads/ | Téléchargez la version 3.* (3.7 a priori)
- Ensuite, téléchargeons un logiciel pour utiliser Python : https://www.jetbrains.com/pycharm/download/ | Téléchargez la version Community (gratuite)
- Enfin, nous allons avoir besoin d'un dernier logiciel, OpenRefine : http://openrefine.org/download.html
- Pour finir, les logiciels type Excel, Google SpreadSheet ou LibreOffice Sheet sont très utiles pour les données tabulées.

### Débutons avec Python :
- **Assurez-vous d'avoir bien installer Python 3.7** auparavant (https://www.python.org/downloads/)
- **Installez Pycharm CE** et lancez Pycharm CE. Pycharm est un **IDE**, c'est-à-dire un Environnement de Développement Intégré. Cela signifie que c'est un logiciel avec lequel vous pouvez créer tout un projet Python, en autonomie.
- Au premier lancement, Pycharm va demander à être configuré. Inutile de modifier quoi que ce soit à la configuration initiale proposée :)
- Une fois configuré, vous allez pouvoir créer un nouveau projet :
![Créez un nouveau projet](/media/cours-2-capt-1.png)
  - Placez-le dans un répertoire "*PycharmProjects*" (déjà créé par votre ordinateur normalement)
  - Intitulez-le "*cours-donnees-culturelles*"
  - Déroulez la partie "*Project interpreter*" et vérifiez que la ligne "*Base interpreter*" indique bien **Python 3.7**
  - Cliquez sur *Create*
- Votre environnement de travail doit ressembler à ceci :
![Environnement de travail](/media/cours-2-capt-2.png)
- Faites un clic droit sur le dossier racine de votre projet dans la colonne de gauche (cours-donnees-culturelles) : new > Python file
- Intitulez ce fichier "**hello**", et cliquez sur "*OK*"
- Ce fichier s'ouvre (ou alors ouvez-le) et tapez-y `print('Bonjour !')`
- Faites y un clic droit sur le nom de votre fichier **hello.py** (en haut, au-dessus de la zone de saisie) et cliquez sur "**Run 'hello'**".
- Une fenêtre s'ouvre en bas de votre écran, et "Bonjour !" y apparait.
![Environnement de travail](/media/cours-2-capt-3.png)

## Des logiciels en ligne utiles pour analyser les données
Mais attention, cela signifie que vous devez y uploader vos données, donc prenez garde à ne pas y laisser de données confidentielles
- **WTFcsv** : Un petit outil de visualisation des données CSV, pratique pour déceler les erreurs d'encodage https://databasic.io/en/wtfcsv/


## Un peu de doc :
- https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1198040/
- https://support.office.com/en-us/article/Top-ten-ways-to-clean-your-data-2844B620-677C-47A7-AC3E-C2E157D1DB19
- https://fr.wikipedia.org/wiki/Nettoyage_de_donn%C3%A9es
