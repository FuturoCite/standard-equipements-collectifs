# Schéma des équipements collectifs
Ce schéma permet de modéliser les différents attributs des équipements collectifs 

## Contexte

Il existe un besoin d'harmonisation de la publication en open data de données essentielles produites par les administrations publiques wallones. En octobre 2022, plus de 660 jeux de données sont publiés sur le portail [Open Data Wallonie Bruxelles (ODWB)](https://www.odwb.be/explore/?sort=modified), qui sont très hétérogènes. 

Constatant la production de jeux de données disparates à l'échelle de la fédération Wallonie-Bruxelles, Futuro Cité a réuni, dans le cadre d'un groupe de travail sollicité depuis mai 2021, une vingtaine de collectivités. La concertation de celles-ci a permis 1) d'identifier collectivitement des jeux de données jugés prioritaires et 2) de s'accorder sur des spécifications des modèles de données. 
La standardisation de ces données prioritaires est en effet essentielles pour s'assurer de leur publication homogène et de faciliter leur exploitation (notamment leur agrégation) par les réutilisateurs. Elle faciliten l'exploitation des données publiées par les réutilisateurs (agrégation, consolidation et traitements automatiques).

## Construction du schéma de données 

Les membres du groupe de travail ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles… Ils se sont appuyés sur un état des lieux du patrimoine de données des collectivités wallones et sur une étude des modèles utilisés par des collectivités déjà productrices de ces données (notamment Liège et Namur), en prenant en compte les retours faits par les réutilisateurs de données. 

Toutes les réunions ont fait l'objet de comptes-rendus disponibles *ici - à ajouter !* 

## Description du schéma

La documentation des champs du schéma est accessible sur .... *(le site de futurocité)*

Un *gabarit au format tableur* est également prévu pour faciliter la publication d'un jeu de données conforme au format du schéma.

Le tableau ci-dessous donne un aperçu des champs du schéma.

<table>
  <tr>
   <td><strong>Nom</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>Identifiant
   </td>
   <td>Ce champ contient un identifiant unique local. Le producteur de données le génère en associant le code INS de la commune dans laquelle se situe l'équipement à un nombre. Ce champ permet d'éviter localement les doublons. Le code INS de la commune est accessible ici : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Nom
   </td>
   <td>Ce champ contient le nom de l'équipement
   </td>
  </tr>
  <tr>
   <td>Description
   </td>
   <td>Ce champ contient une courte description de l'équipement
   </td>
  </tr>
  <tr>
   <td>Nom de la commune
   </td>
   <td>Ce champ contient le nom de la commune dans laquelle se situe l'équipement collectif. Le nom de la commune provient de la base de données BeST Address : https://opendata.bosa.be/index.fr.html ou de la liste des codes INS : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Code INS
   </td>
   <td>Ce champ contient le code INS de la commune où se situe l'équipement. Il est accessible ici : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Partie de commune
   </td>
   <td>Ce champ continent le nom de la partie de commune où se situe l'équipement, conforme à l'appelation dans StatBel : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie
   </td>
  </tr>
  <tr>
   <td>Code INS de la partie de commune
   </td>
   <td>Ce champ contient le code INS de la partie de commune où se situe l'équipement. La découpe géographique de StatBel Level 5 (NIS6) liste ces codes : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie
   </td>
  </tr>
  <tr>
   <td>Nom de rue
   </td>
   <td>Ce champ renseigne le nom de la voirie où se situe l'équipement (ou de la voirie la plus proche de l'emplacement PMR si l'emplacement n'est pas en voirie).
   </td>
  </tr>
  <tr>
   <td>Code rue BeSTAddress
   </td>
   <td>Ce champ contient le code de la voirie où se situe l'équipement collectif dans la base de données BeSTAdress (ou de la voirie la plus proche s'il n'est pas en voirie) :<a href="https://opendata.bosa.be/index.fr.html"> https://opendata.bosa.be/index.fr.html</a>
   </td>
  </tr>
  <tr>
   <td>Code rue national
   </td>
   <td>Code de la voirie où se situe l'équipement dans le registre national (ou de la voirie la plus proche si l'emplacement n'est pas en voirie)
   </td>
  </tr>
  <tr>
   <td>Numéro de police le plus proche
   </td>
   <td>Ce champ est recommandé. Il contient le numéro de police (numéro de rue) le plus proche de l'équipement.
   </td>
  </tr>
  <tr>
   <td>Distance au point d'adresse
   </td>
   <td>Ce champ indique la distance, en mètres, entre l'équipement et le point d'adresse le plus proche introduit via les autres champs (code_rue_bestadress, num_police, …). En cas de décimale, le séparateur est le point.
   </td>
  </tr>
  <tr>
   <td>Coordonnées
   </td>
   <td>Ce champ indique les coordonnées de l'équipement. Il respecte le format WGS 1984 (latitude,longitude). Ne pas mettre d'espace après la virgule. Les coordonnées d'un lieu peuvent être générées ici :<a href="https://www.coordonnees-gps.fr/carte/pays/BE"> https://www.coordonnees-gps.fr/carte/pays/BE</a>
   </td>
  </tr>
  <tr>
   <td>Géométrie
   </td>
   <td>Ce champ indique les coordonnées de la zone correspondante à l'équipement. Ce champ est à compléter dans le cas d'un équipement s'étendant sur une large zone tel qu'une plaine de jeu, un canisite
   </td>
  </tr>
  <tr>
   <td>Précisions sur l'emplacement
   </td>
   <td>Ce champ donne des précisions jugées utiles sur l'emplacement de l'équipement.
   </td>
  </tr>
  <tr>
   <td>Photo
   </td>
   <td>Ce champ contient une url renvoyant vers une photo de l'équipement
   </td>
  </tr>
  <tr>
   <td>Accessibilité PMR
   </td>
   <td>Ce champ indique l'accessibilité de l'équipement pour les personnes à mobilité réduite.
   </td>
  </tr>
  <tr>
   <td>Horaires
   </td>
   <td>Le champ indique les horaires auxquelles l'équipement est accessible. Il respecte le format proposé par OpenStreetMap (https://wiki.openstreetmap.org/wiki/FR:Key:opening_hours). L'outil YoHours (https://projets.pavie.info/yohours/) permet de générer des horaires au bon format. Le format OSM permet d'indiquer des exceptions pendant certaines périodes (vacances, jours fériés…). Pour les générer au bon format en utilisant YoHours, il suffit de les renseigner en cliquant sur le bouton 'plus' vert, situé en haut à gauche.
   </td>
  </tr>
  <tr>
   <td>Type d'équipement
   </td>
   <td>Ce champ indique le type de l'équipement. Valeurs possibles : Point d'eau potable ; Toilette publique ; Bac à sel ;Canisite ; Poubelle publique ; Cendrier ; Banc public ; Plaine de jeux ; Equipement sportif ; Jardin partagé ; Panneau d’affichage ; Boite à livres ; Bulle à verre ; Bulle à vêtements ; Autre
   </td>
  </tr>
  <tr>
   <td>Précisions sur le type d'équipement
   </td>
   <td>Ce champ décrit avec plus de précision le type de l'équipement. Par exemple, pour un jeu de type cendrier : cendrier sur pied, cendrier au sol ou cendrier mural. Pour un jeu de type toilette publique : urinoir ou toilette.
   </td>
  </tr>
  <tr>
   <td>statut
   </td>
   <td>Ce champ indique si l’équipement est disponible ou non au moment de la création/mise à jour du jeu de données. Un équipement pourrait par exemple ne plus être disponible car il n'est plus accessible pendant des travaux.
   </td>
  </tr>
  <tr>
   <td>Date d'installation de l'équipement
   </td>
   <td>Ce champ indique la date d'installation de l'équipement. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
  <tr>
   <td>Date de dernière maintenance
   </td>
   <td>Ce champ indique la dernière date de maintenance de l'équipement. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
  <tr>
   <td>Gestionnaire
   </td>
   <td>Ce champ indique le nom du gestionnaire de l'équipement collectif
   </td>
  </tr>
  <tr>
   <td>Payant
   </td>
   <td>Ce champ précise si l'équipement est payant ou gratuit. Par exemple dans le cadre des toilettes publique
   </td>
  </tr>
  <tr>
   <td>Date de création de la donnée
   </td>
   <td>Ce champ indique la date de création de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD)
   </td>
  </tr>
  <tr>
   <td>Date de dernière modification de la donnée
   </td>
   <td>Ce champ indique la date de la dernière modification de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
</table>

## Format de fichier 

Le format de fichier retenu pour la publication des données est le CSV (Comma Separated Values, valeurs séparées par des virgules).

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de formatage suivantes :

* l’encodage des caractères est UTF-8,
* le séparateur des colonnes est la virgule,
* le séparateur des nombres décimaux est le point,
* le séparateur de valeurs multiples dans un champ est le point-virgule,
* si un champ contient une virgule, il doit être entouré de guillemets doubles,
* chaque ligne doit avoir le même nombre de champs,
* le type MIME ou Content-Type est text/csv.

### Recommandation pour le nommage des fichiers 

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

YYYY-MM-DD_idProducteur_lieux-de-mediation-numerique_territoire.csv

* YYYY-MM-DD : Date de création du fichier
* idProducteur : code ISN unique de la commune pour identifier le producteur
* equipements-collectifs : nom du fichier, en minuscules non accentuées
* territoire : Nom du territoire concerné, non accentué (exemple : Liege)
* extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 2022-10-25_62063_equipements-collectifs_Liege.csv

### Recommandation pour la mise en conformité 

Ces conseils reprennent ceux du [Socle commun des données locales publié par Open Data france](https://scdl.opendatafrance.net/docs/recommandations-relatives-aux-jeux-de-donnees.html)

Les fichiers doivent comporter :

* Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
* Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
