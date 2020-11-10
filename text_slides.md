## Texte des diapos

1. Bonjour. Mon nom est Olivier Gimenez. Je suis chercheur au CNRS à Montpellier. Je vais vous parler de mes premiers pas dans le deep learning, et son application à la reconnaissance d'espèces sur des photos prises grâce à des pièges photographiques. 

2. Je travaille beaucoup sur les relations prédateur-proies, des interactions entre espèces qui façonnent les communautés de grands mammifères. 

3. Il s'agit d'un travail en collaboration avec Anna Chaine, Maëlis Kervellec, toutes deux stagiaires de M1, Vincent Miele le grand organisateur de ces journées, les collègues de l'Office Français de la Biodiversité et des fédérations de chasse de l'Ain et du Jura.  
La ppale question que l'on se pose est de comprendre comment l'environnement et les relations entre prédateurs et proies s'articulent. 

4. Pour ce faire, les collègues de l'OFB et des fédérations de chasse collectent des données dans l'habitat naturel des espèces qui nous intéressent, grâce à des pièges photos laissés à des endroits stratégiques. Alors pas avec du matériel comme celui-ci qui disparaitrait bien vite. 

5. Mais plutôt ce genre de piège photo. Avec un système où l'on installe un appareil de chaque côté de chemins où les prédateurs sont susceptibles de passer, comme ici une femelle et ses petits.  
Cette méthode est non-invasive, autrement dit on n'a pas besoin de capturer physiquement les animaux. Le souci est qu'on se retrouve avec des tonnes de photos auxquelles il faut associer une étiquette espèce. C'est là qu'entre en jeu le deep learning. 

6. Vincent nous a présenté l'approche ce matin. L'idée est de nourrir les algorithmes avec des photos et en sortie de récupérer l'espèce qui se trouve sur la photo. 

7. Pour faire mes premiers pas en DL, j'ai utilisé imaginecology. Sérieusement, jetez-y un coup d'oeil. C'est bourré de ressources précieuses et pertinentes. Il y une intro au DL, des codes, des papiers, des données pour entrainer vos modèles. Et surtout tout un tas de tutoriels pour vous former. Bravo à Vincent et Gaspard pour ce boulot! 

8. J'ai utilisé le tutoriel détection d'animaux sur des images issues de pièges photos. On utilise Retinanet qui adopte l'approche en deux temps détection et classification. Vous pouvez retrouver mes pérégrinations sur GitHub.

9. Avant de passer aux résultats, je rappelle que je suis débutant. Je me forme avec l'aide de Vincent qui n'est toutefois pas responsables de mes errements. 

10. Quels sont mes résultats?

11. Dans un premier temps, j'ai fait du transfer learning sur un site d'étude dans le Jura où on avait tout un tas de photos déjà étiquetées. 

12. Les résultats sont plutôt bons. On arrive à détecter sur les images et classifier le lynx, et ses proies, le chamoix et le chevreuil, avec un degré de certitude élevé.

13. C'est le cas aussi pour d'autres espèces présentes sur les photos. 

14. Ensuite, j'ai voulu utilisé mon modèle pour étiqueter automatiquement des photos prises avec des pièges installés sur un autre site, dans l'Ain. Ces photos ont aussi été étiquetées à la main.

15. On obtient ce genre de résultats. Avec en colonne les espèces, les vrais positifs, les faux positifs, et les faux négatifs.  
Et là, si on se débrouille pas mal pour le lynx, c'est le drame pour ses proies, avec un excès de faux positif pour le chamois, et de faux négatifs pour les chevreuils. 

16. Passé la frustration...

17. Je me suis demandé pourquoi de si mauvais résultats. Plusieurs raisons possibles. 
18. On sait par exemple que généraliser un modèle entrainé sur un site à un autre site est difficile en DL. Les pièges, les conditions environnementales, le terrain, l'exposition, des tas de choses peuvent être différentes.  
Il se peut aussi que le jeu de données d'entrainement soit trop pauvre.  
Ce que je compte faire maintenant, sur le conseil de Vincent, c'est utiliser les données des deux sites pour entrainer mon modèle. 

19. Je finirai cet exposé en donnant qqs leçons que j'ai apprises en cours de chemin.

20. La terminologie peut être un obstable. Sur imaginecology, vous trouverez un glossaire qui vous sauvera. Le point de vue d'une statisticienne peut aussi être utile pour faire le // avec un vocabulaire plus familier.  
Je me suis posé pas mal de questions sur la reproductibilité. Entrainer un modèle s'apparente parfois à de la cuisine avec sa part d'improvisation.  
Il y a aussi des questions de droit et d'éthique qui se posent quand on traite des photos sur lesquelles nos conspécifiques se mettent en scène.  
Se pose aussi la question de l'empreinte écologique de l'approche DL comme on a souvent besoin d'utiliser des cartes graphiques, très gourmandes en énergie, sur de longues périodes.  
Enfin, je conseille à celles et ceux qui comme moi veulent se former d'aller voir ce que font les pros. Il y a par exemple cette compétition organisée par Sara Beery où vous retrouverez les conseils des meilleures équipes. Je vous suggère d'ailleurs de suivre Sara, ainsi que Mikey Tabak, deux étoiles montantes du DL pour l'écologie.  
Dernier point, apprendre Python ne peut pas faire de mal comme le DL se parle en Python, et pour ce faire, si comme moi vous êtes plutôt utilisateur de R, je vous conseille ces deux ouvrages. 

21. Merci pour votre écoute. 

22. Et si vous voulez en savoir plus sur lynx et écologie statistique, un peu d'autopromotion avec cet article que nous venons d'e publier dans The Conversation à l'occasion de la Fête des Sciences.

