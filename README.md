# Rapport sur l'intégration de Hibernate pour la gestion de produits dans une base de données MySQL

Introduction

Ce projet a pour objectif de développer une application Java en utilisant Hibernate pour gérer des produits dans une base de données MySQL. Hibernate, un framework ORM (Object-Relational Mapping), permet de simplifier l'accès à une base de données en mappant des objets Java à des tables SQL. Le projet utilise également Spring pour la gestion des dépendances et des configurations.

# Configuration du projet

Le projet a été configuré avec les dépendances suivantes :

- Spring Framework : Pour la gestion des beans et des configurations.
- Hibernate ORM : Pour l'accès aux données et la gestion des transactions.
- MySQL : Comme base de données relationnelle.
  
# Les principales classes du projet incluent :

- Product : Entité représentant un produit avec des attributs comme le nom et le prix.
- IDao : Interface définissant les opérations de base de données.
- ProductDaoImpl : Implémentation de IDao pour les opérations sur la base Product.
- Presentation2 : Classe principale pour tester l'insertion de produits dans la base de données.

# Structure de l'application
1. Classe Product : La classe Product représente un produit avec deux champs : name et price. Elle est annotée avec @Entity et @Table pour indiquer à Hibernate de mapper cette classe à la table product dans la base de données.

2. Interface IDao :L'interface IDao définit les méthodes de base pour la gestion des entités. Dans notre cas, elle est implémentée par ProductDaoImpl.

3. Classe ProductDaoImpl : Cette classe implémente l'interface IDao pour la gestion des produits. Elle utilise Hibernate pour insérer un produit dans la base de données.

4. Classe Presentation2 : La classe Presentation2 est utilisée pour tester l'application. Elle crée un contexte Spring, injecte un ProductDaoImpl et sauvegarde un produit dans la base de données.

