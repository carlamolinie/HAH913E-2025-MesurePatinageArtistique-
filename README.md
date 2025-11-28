# HAH913E-2025-MesurePatinageArtistique-
Working group on movement assessment using an accelerometer on figure skaters: detecting falls based on data.

TRADUCTION EN FRANCAIS DU RAPPORT: 

Analyse des mouvements du haut du corps en danse sur glace et patinage artistique : étude par accéléromètre au poignet
Auteurs : CHANDRA MOHAN Lakshana, FRATY Louis, MOLINIE Carla, PLANE Chloé Date : 1er décembre 2025 Module : HAH913E – Activité Physique pour la Santé Responsable pédagogique : Denis MOTTET

Résumé
Cette étude analyse les profils de mouvement du haut du corps dans deux disciplines sur glace : la danse sur glace et le patinage artistique. Les données ont été recueillies à l'aide d'un accéléromètre porté au poignet lors de sessions d'entraînement réelles. Le traitement du signal a inclus le calcul de l'accélération résultante, un filtrage passe-bas, la détection des pics d'intensité et une analyse fréquentielle. Les résultats indiquent que la danse sur glace se caractérise par des mouvements plus fluides et continus. À l'inverse, le patinage artistique présente des événements de haute intensité (pics > 3 g) plus fréquents et explosifs. Ces conclusions permettent d'orienter les stratégies de préparation physique et de prévention des blessures spécifiques à chaque discipline.

1. Introduction

La danse sur glace et le patinage artistique sont deux disciplines exigeantes qui, bien que partageant les bases de la glisse, mobilisent le corps de manière distincte. Le patinage artistique se caractérise par des éléments explosifs tels que les sauts, les pirouettes rapides et les changements de direction dynamiques. Ces actions requièrent une force rapide, une réactivité neuromusculaire et une capacité à absorber les forces d'impact. À l'inverse, la danse sur glace met l'accent sur le rythme, la fluidité, la posture et la coordination, privilégiant des transitions contrôlées plutôt que la puissance explosive.

Dans une perspective de santé et de performance, il est crucial de comprendre ces différences biomécaniques. La problématique centrale de cette recherche est la suivante : « En quoi la nature des mouvements du haut du corps diffère-t-elle entre la danse sur glace et le patinage artistique, et comment ces différences influencent-elles la charge physique et la prévention des blessures ? ».

Pour répondre à cette question, cette étude utilise l'accélérométrie au poignet pour capturer la dynamique du haut du corps en temps réel. L'objectif est de comparer les profils cinématiques des deux disciplines et de fournir des recommandations basées sur des données objectives pour l'optimisation de l'entraînement.

2. Méthodologie
2.1 Participants

L'étude a porté sur deux athlètes expérimentées, pratiquant leur discipline depuis plus de dix ans et sans blessure depuis au moins six mois.

Sujet 1 (Patinage Artistique) : Chloé, 24 ans, spécialisée dans les sauts et les pirouettes.

Sujet 2 (Danse sur Glace) : Tiphaine, 23 ans, entraînée aux portés et séquences chorégraphiées.

2.2 Matériel et Protocole

Pour quantifier les mouvements, un accéléromètre triaxial a été fixé au poignet dominant (gauche) afin de minimiser les artefacts. L'appareil a été configuré avec une fréquence d'échantillonnage de 100 Hz.

Chaque athlète a réalisé une séance d'entraînement représentative d'environ 15 minutes.

La séance de patinage artistique incluait des sauts, des pirouettes et de courtes séquences techniques.

La séance de danse sur glace consistait en une routine structurée combinant pas, tours et expression artistique continue.

2.3 Traitement des données et Justification des Analyses

Les données brutes ont été traitées via un pipeline Python développé pour ce projet. Les étapes ont inclus le calcul de l'accélération résultante (x,y,z) et l'application d'un filtre passe-bas Butterworth (4e ordre, 20 Hz) pour supprimer le bruit.

L'analyse s'est articulée autour de quatre indicateurs clés, choisis pour leur pertinence scientifique:

Série temporelle de l'accélération totale : L'objectif scientifique est d'observer la structure globale de l'entraînement et d'identifier les phases d'activité intense. Ce graphique permet de repérer les pics brutaux (chocs, réceptions) qui constituent des facteurs de risque pour les articulations du haut du corps.

Histogramme de distribution de l'accélération : Cet outil permet de voir la répartition globale de l'effort (faible, moyen, élevé). Si l'histogramme montre une prévalence de valeurs élevées, cela indique que la séance impose une forte contrainte mécanique au corps, un paramètre clé pour évaluer la charge d'entraînement.

Détection des pics de haute intensité (> 3 g) : Nous avons quantifié les pics d'accélération dépassant 3 g. En biomécanique, des accélérations de cette amplitude sont associées à des forces d'impact significatives et des instabilités. Le comptage de ces pics permet d'estimer la probabilité de blessure et d'identifier les moments critiques nécessitant une intervention technique.

Analyse Fréquentielle (FFT) : Une analyse spectrale a été réalisée pour étudier la périodicité du mouvement. Elle permet d'identifier la cadence et de détecter des mouvements répétitifs. Sur le plan de la santé, des gestes répétitifs mal exécutés peuvent entraîner des microtraumatismes ; la FFT aide donc à comprendre la régularité technique.

3. Résultats
3.1 Analyse Qualitative des Profils de Mouvement

L'inspection visuelle des séries temporelles révèle deux signatures motrices distinctes. Le profil du patinage artistique est caractérisé par des pics d'accélération intermittents et de grande amplitude, correspondant aux sauts et aux changements de direction rapides. Ce modèle reflète une demande de puissance explosive suivie de stabilisation.

À l'inverse, le profil de la danse sur glace présente un signal beaucoup plus lisse et continu. Bien que des variations d'accélération soient présentes, elles sont moins brutales, suggérant une stratégie de mouvement axée sur la fluidité et le contrôle postural plutôt que sur la force balistique.

[ESPACE RÉSERVÉ FIGURE 1 : Séries Temporelles Comparées] La Figure 1 illustre l'accélération résultante (m/s 
2
 ) au cours du temps. Notez les pics aigus chez la patineuse artistique (haut) comparés à l'amplitude modérée et constante chez la danseuse (bas).

3.2 Évaluation Quantitative de la Charge Mécanique

L'analyse des histogrammes et la détection des pics confirment les observations qualitatives. La séance de patinage artistique a montré une accélération maximale significativement plus élevée et un nombre plus important d'événements dépassant le seuil de 3 g.

[ESPACE RÉSERVÉ FIGURE 2 : Histogrammes d'Intensité] La Figure 2 montre la densité de probabilité de l'accélération. L'histogramme du patinage artistique s'étend davantage vers les hautes valeurs (queue de distribution).

Le Tableau 1 résume les métriques quantitatives. Le coefficient de variation, mesurant la variabilité du signal, est plus élevé pour le patinage artistique, quantifiant la nature irrégulière et explosive de la discipline.

Tableau 1 : Indicateurs de Performance Biomécanique

Métrique	Patinage Artistique (Chloé)	Danse sur Glace (Tiphaine)
Accélération Max (Pic) (m/s 
2
 )	[Insérer Donnée]	[Insérer Donnée]
Nombre de Pics > 3 g	[Insérer Donnée]	[Insérer Donnée]
Accélération Moyenne (m/s 
2
 )	[Insérer Donnée]	[Insérer Donnée]
Coefficient de Variation	Élevé	Faible
3.3 Analyse Fréquentielle et Rythmique

L'analyse FFT a mis en évidence une fréquence dominante dans les données de danse sur glace, correspondant au rythme de patinage et à la cadence musicale. Le spectre du patinage artistique est plus chaotique, reflétant la nature apériodique d'un programme ponctué d'éléments techniques discrets.

[ESPACE RÉSERVÉ FIGURE 3 : Spectre Fréquentiel (FFT)]

4. Discussion
Les résultats de cette étude confirment l'hypothèse selon laquelle le patinage artistique et la danse sur glace imposent des charges mécaniques distinctes au haut du corps.

Le patinage artistique est clairement caractérisé par des accélérations intermittentes et explosives. La fréquence élevée des pics supérieurs à 3 g souligne les forces d'impact importantes transmises par les membres supérieurs, notamment lors des réceptions de sauts et de l'initiation des rotations. Ces résultats suggèrent que les patineurs artistiques sont plus exposés aux risques de traumatismes aigus liés aux impacts. Par conséquent, la préparation hors glace devrait prioriser le développement de la puissance explosive, de l'agilité et de la résilience aux impacts

Il est important de noter les limites de cette étude. L'utilisation d'un capteur unique au poignet ne capture qu'un aspect local de la biomécanique. Des mesures complémentaires sur le tronc ou les membres inférieurs offriraient une vision plus globale. De plus, la masse corporelle n'a pas été normalisée, ce qui peut moduler les forces d'impact.

5. Conclusion
En conclusion, ce projet a utilisé avec succès l'accélérométrie au poignet pour différencier les signatures motrices du patinage artistique et de la danse sur glace. Nous avons démontré que le patinage artistique est une discipline d'impulsion caractérisée par une forte variabilité et des forces d'impact , tandis que la danse sur glace est une discipline de flux caractérisée par la continuité et la régularité.

6. Références
Ressources Académiques & Cours

Mottet, D. (2024). HAH913E: Physical Activity for Health – Guidelines for the project. Université de Montpellier.

Mottet, D. (2024). Justification des analyses et graphiques. Support de cours, HAH913E.

Littérature Biomécanique & Patinage 3. King, D. L. (2018). The Science of Figure Skating: Jumps. American College of Sports Medicine (ACSM). (Explique les forces de réception de 3 à 8 fois le poids du corps). 4. Knox, A., et al. (2024). Monitoring Internal and External Training Loads in Artistic Skating. Journal of Sports Science & Medicine. (Valide l'utilisation des "Impacts > 2-5 g" comme métrique de risque).

7. Annexes
