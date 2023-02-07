# Schéma des équipements collectifs
Ce schéma permet de modéliser les différents attributs des équipements collectifs 

## Contexte

Il existe un besoin d'harmonisation de la publication en open data de données essentielles produites par les administrations publiques wallonnes. En octobre 2022, plus de 660 jeux de données sont publiés sur le portail [Open Data Wallonie Bruxelles (ODWB)](https://www.odwb.be/explore/?sort=modified), qui sont très hétérogènes. 

Constatant la production de jeux de données disparates à l'échelle de la fédération Wallonie-Bruxelles, FuturoCité a réuni, dans le cadre d'un groupe de travail sollicité depuis mai 2021, une vingtaine de collectivités. La concertation de celles-ci a permis 1) d'identifier collectivement des jeux de données jugés prioritaires et 2) de s'accorder sur des spécifications des modèles de données. 
La standardisation de ces données prioritaires est en effet essentielle pour s'assurer de leur publication homogène et de faciliter leur exploitation (notamment leur agrégation) par les réutilisateurs. Elle facilitent l'exploitation des données publiées par les réutilisateurs (agrégation, consolidation et traitements automatiques).

## Construction du schéma de données 

Les membres du groupe de travail ont défini un schéma de données qui décrit le format des fichiers, les différents champs, les valeurs possibles… Ils se sont appuyés sur un état des lieux du patrimoine de données des collectivités wallonnes et sur une étude des modèles utilisés par des collectivités déjà productrices de ces données (notamment Liège et Namur), en prenant en compte les retours faits par les réutilisateurs de données. 


## Description du schéma

Un [gabarit au format tableur](https://github.com/FuturoCite/standard-equipements-collectifs/blob/main/Schema_equipements_collectifs_gabarit%20copie.xlsx) est également prévu pour faciliter la publication d'un jeu de données conforme au format du schéma.

Un exemple valide au format CSV est consultable [ici](https://github.com/FuturoCite/standard-equipements-collectifs/blob/main/exemple-valide.csv).  

Le tableau ci-dessous donne un aperçu des champs du schéma.

<table>
  <tr>
   <td><strong>Nom</strong>
   </td>
   <td><strong>Remplissage obligatoire/optionnel</strong>
   </td>
   <td><strong>Description</strong>
   </td>
  </tr>
  <tr>
   <td>Identifiant 
   <br>(id)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient un identifiant unique local. Le producteur de données le génère en associant le code INS de la commune dans laquelle se situe l'équipement à un nombre. Ce champ permet d'éviter localement les doublons. Le code INS de la commune est accessible ici : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Nom 
   <br>(name)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le nom de l'équipement
   </td>
  </tr>
  <tr>
   <td>Description 
   <br>(description)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient une courte description de l'équipement
   </td>
  </tr>
  <tr>
   <td>Nom de la commune 
   <br>(municipality)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le nom de la commune dans laquelle se situe l'équipement collectif. Le nom de la commune provient de la base de données BeST Address : https://opendata.bosa.be/index.fr.html ou de la liste des codes INS : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Code INS 
   <br>(ins_code)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le code INS de la commune où se situe l'équipement. Il est accessible ici : https://statbel.fgov.be/fr/open-data/code-refnis
   </td>
  </tr>
  <tr>
   <td>Partie de commune 
   <br>(zone_address)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ continent le nom de la partie de commune où se situe l'équipement, conforme à l'appelation dans StatBel : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie
   </td>
  </tr>
  <tr>
   <td>Code INS de la partie de commune 
   <br>(ins_zone_address)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient le code INS de la partie de commune où se situe l'équipement. La découpe géographique de StatBel Level 5 (NIS6) liste ces codes : https://statbel.fgov.be/fr/propos-de-statbel/methodologie/classifications/geographie
   </td>
  </tr>
  <tr>
   <td>Nom de rue 
   <br>(street_name)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ renseigne le nom de la voirie où se situe l'équipement (ou de la voirie la plus proche de l'emplacement PMR si l'emplacement n'est pas en voirie).
   </td>
  </tr>
  <tr>
   <td>Code rue BeSTAddress 
   <br>(street_number)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ contient le code de la voirie où se situe l'équipement collectif dans la base de données BeSTAdress (ou de la voirie la plus proche s'il n'est pas en voirie) :<a href="https://opendata.bosa.be/index.fr.html"> https://opendata.bosa.be/index.fr.html</a>
   </td>
  </tr>
  <tr>
   <td>Code rue national 
   <br>(street_number_rrn)
   </td>
   <td>Optionnel
   </td>
   <td>Code de la voirie où se situe l'équipement dans le registre national (ou de la voirie la plus proche si l'emplacement n'est pas en voirie)
   </td>
  </tr>
  <tr>
   <td>Numéro de police le plus proche 
   <br>(house_number)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il contient le numéro de police (numéro de maison) le plus proche de l'équipement.
   </td>
  </tr>
  <tr>
   <td>Distance au point d'adresse 
   <br>(distance)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique la distance, en mètres, entre l'équipement et le point d'adresse le plus proche introduit via les autres champs (code_rue_bestadress, num_police, …). En cas de décimale, le séparateur est le point.
   </td>
  </tr>
  <tr>
   <td>Coordonnées 
   <br>(coordinates)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ indique les coordonnées de l'équipement. Il respecte le format WGS 1984 (latitude,longitude). Ne pas mettre d'espace après la virgule. Les coordonnées d'un lieu peuvent être générées ici :<a href="https://www.coordonnees-gps.fr/carte/pays/BE"> https://www.coordonnees-gps.fr/carte/pays/BE</a>
   </td>
  </tr>
  <tr>
   <td>Géométrie 
   <br>(geometry)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique les coordonnées de la zone correspondante à l'équipement. Ce champ est à compléter dans le cas d'un équipement s'étendant sur une large zone tel qu'une plaine de jeu, un canisite
   </td>
  </tr>
  <tr>
   <td>Précisions sur l'emplacement 
   <br>(location_details)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ donne des précisions jugées utiles sur l'emplacement de l'équipement.
   </td>
  </tr>
  <tr>
   <td>Photo 
   <br>(picture)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ contient une url renvoyant vers une photo de l'équipement
   </td>
  </tr>
  <tr>
   <td>Accessibilité PMR 
   <br>(disabled_access)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ est recommandé. Il indique si l'équipement est accessible pour les personnes à mobilité réduite (valeur 'true') ou non (valeur 'false'). Si non applicable/non connu : ne pas renseigner ce champ.
   </td>
  </tr>
  <tr>
   <td>Horaires 
   <br>(schedule)
   </td>
   <td>Optionnel
   </td>
   <td>Le champ indique les horaires auxquelles l'équipement est accessible. Il respecte le format proposé par OpenStreetMap (https://wiki.openstreetmap.org/wiki/FR:Key:opening_hours). L'outil YoHours (https://projets.pavie.info/yohours/) permet de générer des horaires au bon format. Le format OSM permet d'indiquer des exceptions pendant certaines périodes (vacances, jours fériés…). Pour les générer au bon format en utilisant YoHours, il suffit de les renseigner en cliquant sur le bouton 'plus' vert, situé en haut à gauche.
   </td>
  </tr>
  <tr>
   <td>Type d'équipement 
   <br>(type)
   </td>
   <td>Obligatoire
   </td>
   <td>Ce champ indique le type de l'équipement. Valeurs possibles : Point d'eau potable ; Toilette publique ; Bac à sel ;Canisite ; Poubelle publique ; Cendrier ; Banc public ; Plaine de jeux ; Equipement sportif ; Jardin partagé ; Panneau d’affichage ; Boite à livres ; Bulle à verre ; Bulle à vêtements ; Autre
   </td>
  </tr>
  <tr>
   <td>Précisions sur le type d'équipement 
   <br>(type_details)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ décrit avec plus de précision le type de l'équipement. Par exemple, pour un jeu de type cendrier : cendrier sur pied, cendrier au sol ou cendrier mural. Pour un jeu de type toilette publique : urinoir ou toilette.
   </td>
  </tr>
  <tr>
   <td>statut 
   <br>(status)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique si l’équipement est disponible ou non au moment de la création/mise à jour du jeu de données. Un équipement pourrait par exemple ne plus être disponible car il n'est plus accessible pendant des travaux.
   </td>
  </tr>
  <tr>
   <td>Date d'installation de l'équipement 
   <br>(installation_date)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique la date d'installation de l'équipement. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
  <tr>
   <td>Date de dernière maintenance 
   <br>(last_maintenance_date)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique la dernière date de maintenance de l'équipement. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD).
   </td>
  </tr>
  <tr>
   <td>Gestionnaire 
   <br>(provider)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ indique le nom du gestionnaire de l'équipement collectif
   </td>
  </tr>
  <tr>
   <td>Payant 
   <br>(paying)
   </td>
   <td>Optionnel
   </td>
   <td>Ce champ précise si l'équipement est payant ou gratuit (valeur 'true') ou gratuit (valeur 'false'). Par exemple dans le cadre des toilettes publiques. Si non applicable/non connu : ne pas renseigner ce champ.</td>
  </tr>
  <tr>
   <td>Date de création de la donnée 
   <br>(created_date)
   </td>
   <td>Optionnel (recommandé)
   </td>
   <td>Ce champ indique la date de création de la donnée dans le jeu. Il respecte le format ISO 8601 : année-mois-jour (YYYY-MM-DD)
   </td>
  </tr>
  <tr>
   <td>Date de dernière modification de la donnée 
   <br>(last_modified_date)
   </td>
   <td>Optionnel (recommandé)
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

### Recommandations pour le nommage des fichiers 

Les fichiers doivent, sauf exception et autant que possible, respecter les règles de nommage suivantes :

* YYYY-MM-DD : Date de création du fichier
* idProducteur : code ISN unique de la commune pour identifier le producteur
* equipements-collectifs : nom du fichier, en minuscules non accentuées
* territoire : Nom du territoire concerné, non accentué (exemple : Liege)
* extension : Si les règles de formatage sont respectées, l'extension est .csv

Exemple : 2022-10-25_62063_equipements-collectifs_Liege.csv

### Recommandations pour la mise en conformité 

Ces conseils reprennent ceux du [Socle commun des données locales publié par OpenDataFrance](https://scdl.opendatafrance.net/docs/recommandations-relatives-aux-jeux-de-donnees.html)

Les fichiers doivent comporter :

* Toutes les colonnes, y compris celles dont les cellules ne sont pas renseignées, dans le bon ordre, et avec des en-têtes correctement nommées sur la première ligne (nom correspondant strictement au schéma)
* Autant de lignes que nécessaire comprenant des cellules dont les valeurs peuvent être obligatoires (elles doivent être impérativement renseignées) ou optionnelles (elles sont seulement recommandées ou soumises à condition de disponibilité / pertinence)
