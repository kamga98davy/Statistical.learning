La problématique se fonde sur un jeu de données accessible publiquement via la plateforme **Kaggle**.

Il s'agit d'une base regroupant les données de **près de 2 000 clients** ayant été contactés en 2019 lors du lancement d'une nouvelle assurance voyage incluant une **couverture Covid**. 

L'entreprise souhaite désormais tirer parti de cet historique pour affiner ses actions marketing et cibler efficacement les futurs clients.

La **target** (**TravelInsurance**) est binaire : elle indique si un client a souscrit (`1`) ou non (`0`) à l'assurance voyage proposée. Elle est donc modélisée à l'aide d'une **loi binomiale**, associée à une **fonction de lien logit**, conformément aux approches classiques en classification. Ce cadre est cohérent avec les méthodes d'arbres de classification comme **CART**, **Random Forests** et **Gradient Boosting**, qui seront testées et comparées dans ce projet.

Les variables explicatives disponibles dans le jeu de données incluent notamment :

  1. l'âge du client (**Age**),
  2. son secteur d'activité(**Employment Type**),
  3. son niveau d'études (diplômé universitaire ou non) (**GraduateOrNot**),
  4. son revenu annuel (en roupies indiennes) (**AnnualIncome**),
  5. la taille de son foyer familial (**FamilyMembers**),
  6. la présence d'une maladie chronique (**ChronicDiseases**),
  7. sa fréquence de voyage (voyageur fréquent ou non) (**FrequentFlyer**),
  8. s'il a déjà voyagé à l'étranger (**EverTravelledAbroad**).

Toutes ces informations sont susceptibles d'influencer la décision du client face à l'offre d'assurance, ce qui justifie leur intégration dans le modèle.

L'analyse sera précédée d'une **analyse exploratoire des données**, principalement réalisée à l'aide du package `ggplot2`, afin de visualiser les relations entre la variable réponse et les covariables, détecter d'éventuelles anomalies et comprendre les structures de dépendance.

Le choix du cadre binomial logit est soutenu par les références suivantes :

* Frees, E. W. (2010). *Regression Modeling with Actuarial and Financial Applications*. Cambridge University Press.

Ainsi, ce travail vise à sélectionner le **modèle d'arbre optimal** permettant une prédiction fiable de l'adhésion à l'assurance voyage, tout en garantissant une bonne capacité de généralisation.
