# BRIDGE

## A CENTRAL PLATFORM FOR POINTS OF SALE MANAGEMENT

Nous allons commencer par donner un peu de contexte. Le produit que nous développons à pour but
de capter du traffic internet pour l'amener dans les magasins physiques.
Nous proposons une plateforme unifée permettant la gestion de points de vente. Cette plateforme fournit
un ensemble de service :

- le service historique étant le "Store Locator" : il s'agit d'un site internet vitrine qui permet de chercher
les points de vente, connaitre leur horaires d'ouverture, les produits et services disponibles...
- en parallèle nous proposons d'autre service comme le "Presence Management" qui consiste à publier les données
des points de vente sur un ensemble d'annuaires (GMB, Pages Jaunes...)
- ou encore une solution permettant de gérer ses campagnes AdWords plus facilement

## SOME FIGURES

Un petit slide marketing pour vous donner une idée du traffic :
- 515k points de vente
- 15M de pages visitées quotidiennement

Comme vous pouvez le voir la plateforme doit pouvoir subir un peu de charge.

## V2

Jusqu'à Janvier 2016, le produit reposait sur une application Rails. Il s'agit d'une
application monolithique au dessus d'une base Postgres.

J'en profite pour vous donner un peu de vocabulaire que nous risquons d'employer

- Front Office / Store Locator :  ce sont les sites web dont j'ai parlé un peu avant.
Pour ceux-ci le SEO est très important car on veut attirer un maximum de traffic
- Backoffice permettant de gérer les données de points de vente ou de consulter les différentes statistiques
- API publique pour gérer les données de façon programatique

La V2 étant un monolithe il faut être conscient que tout le traffic est reçu par l'application Rails :
les utilisateurs du Backoffice et les internautes se rendant sur les FrontOffice tappent tous dessus.

Le nombre de client augmentant il est devenu de plus en plus difficile de faire scaler le produit pour
absorber une charge de plus en plus importante. C'est pourquoi la boite a décidé de partir sur une V3

## WHY GOING MICRO-SERVICES ?

- le produit s'y prête plutôt bien : nous avons différents modules métiers
- la société a l'ambition de grossir énormément : ce qui voulait dire + de clients et + de développeurs
  - il nous faudrait donc scaler plus facilement que l'application actuelle
  - et nous allions devoir nous organiser pour développer avec une équipe de plus en plus nombreuses.

C'est pourquoi nous nous sommes laissés tenté par l'approche Micro-Service
