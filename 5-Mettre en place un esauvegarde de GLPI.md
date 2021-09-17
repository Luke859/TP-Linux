# Mettre en place une sauvegarde de GLPI

---
## **1- Les différents types de sauvegardes**

---

<br>

Il existes 4 types de sauvegardes de fichiers, la sauvegarde complète, incrémentale, différentielle et miroir. Je vais parler de ces 4 types de sauvegardes.

Commençons par la sauvegarde complète : 

**La sauvegarde complète** -> 
- Elle consiste à copier tous les fichiers et dossiers d'un système donc à chaque fois que vous allez faire une sauvegarde du système elle stockera une copie complète supplémentaire de la source de données.

- Cette sauvegarde prend plus de temps et demande beaucoup de mémoire de stockage. Par contre quand vous avez besoin pour récupérer des données elles sont les plus rapides et les plus simples à faire.

<br>

**La sauvegarde différentielle** -> 
- Elle va effectuer une copie initiale et complète de tous vos fichiers et dossiers. Les prochaines sauvegardes vont permettre de stocker tous les changements apportés depuis votre dernière sauvegarde complète.

- Cette sauvegarde est rapide et prend peu de place de stockage. Pour la récupération de données elle est très rapide.

<br>

**La sauvegarde incrémentale** -> 
- Elle effectue une copie complète de toute les données et les sauvegardes qui suivent permettent d'enregistrer les modifications apportées depuis la dernière sauvegarde .

- Cette sauvegarde est rapide et prend peu de place de stockage Pour la récupération de données elle est lente.

<br>

**La sauvegarde mirroir** ->
- Elle effectue une copie exacte des données.

- Cette sauvegarde ne contient pas de fichiers anciens ou obsolètes et a une capacité de restauration rapide.

<br>

---

## **2- A quelle fréquence me conseillez vous de réaliser une sauvegarde sur une base de données en entreprise ?**
---

En entreprise je conseille de réaliser une sauvegarde de la base de données aussi souvent que possible donc toutes les semaines en cas de pertes de données, faire souvent des sauvegardes permet d'éviter cela.

<br>

---
## **3- Quel type de sauvegarde choisir ?**

---

Le type de sauvegarde que je choisirais sera la sauvegarde différentielle car elle est rapide pour les sauvegardes, prend peu de place au niveau du stockage et pour la récupération de données elle est très rapide.


