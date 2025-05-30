
# Jeu de la Vie en Java

Ce projet fut conduit en Avril 2024 par Aïssa Pansan et Farouk El Varougou. Je remercie aussi Hamza Laouni pour son aide précieuse.

## Contexte

Ce projet propose une implémentation en Java du célèbre **Jeu de la Vie** (*Game of Life*) de John Conway. Il a été développé dans le cadre d'un projet académique en cours de Programation Orienté Objet (POO). Il a pour but de vid'approfondir les principes de la programmation orientée objet (POO) et d'explorer des concepts avancés en Java, tels que :

- **Héritage** : Le détail de la structure du projet est disponible dans Diag\_class
- **Encapsulation** : Chaque cellule et la grille sont représentées par des classes distinctes, gérant leur propre état et comportement.
- **Polymorphisme** : Surcharge de méthodes pour permettre des comportements spécifiques selon les classes, notamment pour les classes Neighbors ou Grillev2.
- **Abstraction** : Définition de classes et méthodes abstraites pour généraliser les comportements.
- **Itérateurs** : Utilisation d'itérateurs pour parcourir l'ArrayList TableauDynamqueND

## Présentation

Le Jeu de la Vie est un automate cellulaire, où l'évolution de la grille dépend uniquement de son état initial, sans intervention extérieure. Chaque cellule de la grille peut être vivante ou morte, et son état évolue selon des règles simples basées sur les cellules voisines. La particuarité de cette implémentation réside dans la contrainte d'une grille à N-Dimension. Au delà de 3 dimensions, on ne représente qu'une coupe 2D de la grille. L'utilisateur peut choisir la coupe et la dimension de la grille via un fichier de configuration en XML.

## Fonctionnalités

- Génération d'une grille en N-dimension du jeu de la vie.
- Affichage de la grille avec les générations successives, via une interface graphique en Swing
- Possibilité de définir des configurations initiales personnalisées via un fichier XML.
- Progression étape par étape des générations.
- Application des règles classiques du Jeu de la Vie.

## Structure du Projet

```
Java-Game-of-Life/
├── Diag_class/           # Diagrammes UML et documents de conception
├── main.pdf              # Rapport principal du projet
├── Rapport.pdf           # Documentation supplémentaire
├── README.md             # Description et instructions du projet
├── .gitignore            # Fichier gitignore
└── src/                  # Code source Java
    ├── Cell.java
    ├── Grid.java
    ├── GameOfLife.java
    └── Main.java
```

## Objectifs a réaliser 

- [X] : Implémentation de la grille en N-dimension.
- [X] : Génération des coordonnées et des voisinages de cellules.
- [X] : Implémentation des règles.
- [X] : Possibilité de définir des configurations initiales personnalisées, via un fichier de configuration.
- [X] : Développement d'une interface graphique
- [ ] : Simulation cohérente 
	- [X] : Grille 1D
	- [ ] : Grille 2D
	- [ ] : Grille 3D et plus
- [ ] : Ajout de motifs prédéfinis (ex. : planeurs, oscillateurs).
- [ ] : Écriture de tests unitaires pour les composants principaux.

## Prérequis

- Java Development Kit (JDK) 8 ou version ultérieure.

## Compilation et Exécution

1. Cloner le dépôt :
   ```
   git clone https://github.com/Mustang-ing/Java-Game-of-Life.git
   ```
2. Se rendre dans le répertoire du projet :
   ```
   cd Java-Game-of-Life
   ```
3. Compiler le code source :
   ```
   javac src/*.java
   ```
4. Exécuter l'application :
   ```
   java -cp src Main
   ```

## Utilisation

Avant de lancer, la configuration, il est nécessaire de configurer le fichier de confifguration **automate.xml** localisé dans le dossier Fichiers.
Dans ce fichier, on peut :

- Définir la taille de la grille.
- Spécifier les cellules vivantes initiales ou bien générer un grille aléatoire (RANDOM).
- Spécifier les règles qui seront appliquer 
- Spécifier quelle voisinages sont pris en compte, dans le calcul.

