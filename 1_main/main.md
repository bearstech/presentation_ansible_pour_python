!SLIDE
#Des serveurs

> Un serveur, ça va, c'est quand il y en a beaucoup que ça pose problème.

!SLIDE
#Application local

> Mon Plone, Mon Django, sur Ma machine

So 2000.

> Dans Mon virtualenv

so 2010.

!SLIDE
# Emballage

Pour un joli site web, il faut un Nginx pour l'emballer, servir directement les assets et compresser ce qu'il peut.

Gunicorn ne DOIT PAS travailler tout nu, il lui faut un proxy qui bufferise, devant.

!SLIDE
#Des services

Une application utilise :

 * Une base de données, relationnelle ou non
 * Redis
 * Elasticsearch
 * …

!SLIDE
#Un build

On ne compile pas python, mais…

 * Makefile
 * Buildout
 * Scons, waf, ou pire?

!SLIDE
#Plus jamais seul

Une application moderne utilise un ensemble de services, locals ou distants,
qui doivent être paramétrés, et déployés sur différents cibles
(avec des paramètres spécifiques).

!SLIDE
#Des recettes

Personne ne doit espérer poser son laptop sur une étagère dans une baie d'un datacenter.

C'est tentant, récurant, mais non.

Il faut pouvoir faire une installation systématique prévisible et reproductible.

**Une recette, des ingrédients, des invités.**

!SLIDE
#Différentes cibles

Le déploiement devra pouvoir se faire dans différent environement.

Une VM local, le LXC d'un Jenkins, un serveur de preprod, de la prod…
Pourquoi pas du Cloud? et puis finalement un autre Cloud!







