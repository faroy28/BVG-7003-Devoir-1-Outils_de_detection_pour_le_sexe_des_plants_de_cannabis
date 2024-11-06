# Devoir-1-BVG-7003

**Détermination du sexe des plants de *Cannabis sativa* en fonction du niveau d’expression du gène REM16**


## **Cas d'utilisation:** 
Le présent pipeline est conçu pour déterminer le sexe des plants de cannabis à partir de données transcriptomiques. La première partie du script utilise un jeu de données obtenu lors d'une analyse transcriptomique de 138 plants de cannabis ou le sexe des plants était préalablement connu. Suite à une revue de littérature, l'hypothèse voulant que les locus LOC115699937 (REM16) et LOC115696989 (FT1) puissent être de bons marqueurs pour confirmer le sexe des plants a été soumise. La première partie du script a donc pour but de confirmer cette hypothèse, en montrant la différence marquée de l'expression du gène REM16 en fonction du sexe de la plante, en utilisant le gène FT1 comme témoin. La deuxième partie du script est utilisable avec votre propre jeu de données transcriptomiques. Il sert à trier vos plants de cannabis par leur sexe en fonction de l'expression du locus LOC115699937 (REM16) obtenue par votre expérience. La classification du sexe a été établie en interprétant les données transcriptomiques du gène REM16 et les graphiques obtenus dans la première partie du script. D'après ces derniers, le sexe femelle est attribué lorsque l'expression du gène REM16 est supérieure à 9.5. À l'inverse, le sexe mâle est donné lorsque l'expression du gène REM16 est inférieure à 9.5. La deuxième partie du script permettra de visualiser sous forme de liste quels sont vos plants mâles et femelles. 

## **Données d’entrées**
La première partie du script nécessite le téléchargement du fichier CSV donné dans ce dépôt (2_Data_RNASeq_Cannabis_Sex.zip).
Afin d’utiliser la deuxième partie du script pour déterminer le sexe de vos plants de cannabis, vous devez avoir en votre possession un fichier CSV contenant des données d’expression géniques provenant d’une analyse transcriptomique effectuée sur vos plants. Les données doivent contenir :
-	 Les valeurs d’expression génique de chacun des gènes en format numérique
-	 L’identifiant de chacun des plants (nom des plants) doit être présent avec les valeurs d’expression géniques y étant liées.
-	Pour chacune des valeurs d’expression génique, le nom du gène auquel il fait référence doit être indiqué dans l’entête de la colonne. 
-	Pour une utilisation simplifiée du script, il est fortement conseillé d’attribuer le terme : « LOC115699937 » pour les valeurs d’expression liés aux gène REM16. 

## **Résultats:**
 **Première partie**
A)	Évaluation du niveau d’expression du gène REM16 en fonction du sexe de la plante
Cette partie est conçue pour schématiser le niveau d’expression du gène REM16 sous le format d’un graphique de type « boxplot ». On remarque que selon le sexe, le niveau d’expression semble significativement différent. Il est juste d’affirmer qu’un niveau d’expression supérieur à 9.5 est associé au sexe femelle, contrairement aux plants male qui semblent avoir un niveau d’expression inférieur à 9.5. 
B)	Évaluation du niveau d’expression du gène FT1 en fonction du sexe de la plante
Cette section est très similaire à la précédente. Elle montre sous forme d’un graphique de type « boxplot » le niveau d’expression du gène FT1 en fonction du sexe des plants. Le graphique révèle qu’il n’y a pas de différence significative entre les plants mâles et femelles au niveau de l’expression du gène en question. 
C)	Évaluation du niveau d’expression des gènes REM16 et FT1 en fonction du sexe de la plante. 
Cette partie combine les résultats des sections A et B. Elle procure sous forme de graphique de type « Boxplot » les niveaux d’expressions des gènes REM16 et FT1 en fonction du sexe des plantes. 

 **Deuxième partie**
Avec vos propres données transcriptomiques, vous obtiendrez une liste composée de deux colonnes. La première colonne « Male.Plants » vous indiquera tous les identifiants de plantes étant liés à des plants mâles d’après leur niveau d’expression du gène REM16. À l’inverse, la deuxième colonne « Female.Plants » vous indiquera les identifiants de plantes liés à des plants femelles.

## **Instructions**
1.	Assurez-vous d’avoir téléchargé R et R studio sur votre ordinateur (https://posit.co/download/rstudio-desktop/)
2.	Assurez-vous également d’avoir téléchargé le package «ggplot2» dans l’onglet « Packages » de la fenêtre en bas à droite de l’interface d’R studio. Si celui-ci n’est pas installé, veuillez entrer la ligne suivante en première de code : install.packages("ggplot2")
3.	Téléchargez le fichier CSV donné dans ce dépôt. 
4.	Copier le chemin d’accès du fichier et coller ce dernier dans la ligne suivante de la première partie du script :
tab <- read.csv("Coller votre chemin d’accès ici")
Attention : Remplacer les « \ » par des « / »
5.	Exécuter les lignes de codes de chacune des sections A, B et C pour visualiser les graphiques montrant l’expression des gènes REM16 et FT1 en fonction du sexe des plants.
6.	Pour la deuxième partie du script, assurez-vous que votre fichier d’analyse transcriptomique est sous format CSV. Il est fortement conseillé d’attribuer le terme : « LOC115699937 » pour les valeurs d’expression liés aux gènes REM16. 
7.	Copier le chemin d’accès de votre fichier et coller celui-ci dans la ligne suivante dans la deuxième partie du script :
tab <- read.csv("Coller votre chemin d’accès ici ")
8.	Sélectionnez « Run all » afin d’exécuter l’entièreté du script

