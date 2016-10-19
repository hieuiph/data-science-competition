# Decodage d'une formule de pricing MAIF

https://www.datascience.net/fr/home/#_=_

La MAIF souhaite tester l’efficacité du reverse engineering tarifaire. Cette approche consiste à déterminer l’équation ou l’algorithme permettant de calculer les prix d’une couverture d’assurance automobile, à partir de l’observation des résultats (prix public) sur un échantillon de profils. 

L’objectif du challenge est d’estimer le prix d’un contrat pour chaque assuré dans le groupe test. 


Description des variables

Les données contiennent 34 variables dont 10 explicites (code postal, année de naissance, marque du véhicule, profession,...).

La variable "id" est l'identifiant de la ligne, la variable prime_tot_ttc est la variable d'intérêt que l'on cherche à modéliser.
Taille des données

Deux jeux d’échantillons d’apprentissage/de test seront utilisés (un pour chaque phase du challenge).

    L’échantillon d’apprentissage contient 300 000 observations
    L’échantillon de test contient 30 000 observations

Transformation des données pour le challenge

Les données (caractéristiques des assurés, algorithme de calcul) sont fictives mais représentatives de la réalité MAIF.

Résultat attendu

Le fichier que doit fournir le candidat est un fichier au format .csv, dont la structure est présentée ci-dessous et où la variable COTIS est le prix estimé par le compétiteur.
ID;	COTIS
123;	10080
124;	12005
...	...
Critère quantitatif utilisé

L’indicateur de performance qui sera utilisé pour classer les modèles dans la phase 1 est la Mean Absolute Percentage Error (MAPE). 

M=100%n∑i=1n|Pt−Pt∗Pt| 

où Pt
est le prix de réel constaté, Pt∗ le prix estimé par le modèle, et n

l'effectif de l'échantillon

(lire en anglais : http://en.wikipedia.org/wiki/Mean_absolute_percentage_error)
