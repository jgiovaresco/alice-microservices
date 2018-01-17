# Assembling blocks

- Maintenant qu'on a construit nos microservices, comment assemble-t-on tout ça pour avoir un produit qui fonctionne ?

- On va se concentrer sur quelques problèmes auquels on a dû faire face :
  - La gestion de la configuration
  - Le deploiement de tous ces services
  - La garantie que l'ensemble fonctionne

- S'il y a bien un outil qui nous a bien aidé c'est Kubernetes !










Beaucoup de talk sur les microservices parlent de l'enfer de la configuration
=> expliquer les avantages apportés par K8S
- k8s qu'est ce que c'est : orchestrateur
- k8s way to manage outage


Process de release
- release herbdo
- on a du le définir
- update des modules => test tag de la version
- Meme si on met à jour qu'un service, toute la plateforme est taggée








Small facts à renommer

dev stacks:
- service interne
- service externe

metadata: ex. L'utilisateur à propager, id_correlation
service en elixir
