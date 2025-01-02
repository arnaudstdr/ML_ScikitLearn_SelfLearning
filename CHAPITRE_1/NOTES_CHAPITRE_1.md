# 📚 Vue d'ensemble du Machine Learning

Date : **29/12/2024**  

## Table des matières
- [📚 Vue d'ensemble du Machine Learning](#-vue-densemble-du-machine-learning)
  - [Table des matières](#table-des-matières)
  - [Introduction](#introduction)
    - [Résumé](#résumé)
  - [Supervision de L'apprentissage](#supervision-de-lapprentissage)
    - [Résumé](#résumé-1)
  - [Apprentissage groupé ou apprentissage en ligne](#apprentissage-groupé-ou-apprentissage-en-ligne)
    - [Résumé](#résumé-2)
    - [Problèmes rencontrés](#problèmes-rencontrés)
    - [Liens Jupyter notebook](#liens-jupyter-notebook)

## Introduction

<table>
  <tr>
    <td style="width: 30%; vertical-align: top; border-right: 1px solid #ccc;">
      <h3>Mots-clés / Questions</h3>
      <ul>
        <li>
        <strong>Jeux d'entraînement</strong> (<i>training ste</i>) : Exemple de données utilisées par le système pour son apprentissage.</li>
        <li>
        <strong>Observation</strong> (<i>instance</i>) : C'est le nom donné à chacun de ces exemple en statistique. On part aussi parfois d'<i>échantillon</i> ou <i>sample</i> en Anglais.</li>
        <li>
        <strong>Modèle</strong> : C'est la parie du système d'apprentissage automatique qui apprend et effectue des prédictions.</li>
        <li>
        <strong>Exploration des données</strong> (<i>data mining</i>): Consiste à explorer de gros volumes de données pour y d"écouvrir des éléments de structuration qui n'étaient pas immédiatements apparents.</li>
      </ul>
    </td>
    <td style="width: 70%; vertical-align: top; padding-left: 10px;">
      <h3>Notes principales</h3>
      <ul>
        <li>
        L'apprentissage automatique est la science (et l'art) de programmer les oridnateurs de sorte qu'ils puissent <i>apprendre</i> à partir de données.
        </li>
        <li>La prmière utilisation à grande échelle du machine Learning date des années 90 avec les 
        <strong>filtres de spam</strong>.
        </li>
        <li><strong>Exemples d'applications</strong> :
            <ul>
                <li>Analyse d'images : classifiaction d'images / Utilise en général les réseaux de neurones convolutif (CNN) ou parfois de transformateurs.</li>
                <li>Détection de tumeurs : CNN ou transformers</li>
                <li>Classification automatique d'articles de presse : Traitement Automatique du Langage Naturel (TALN) avec des réseaux de neurones récurrents (RNR) ou des CNN, mais de meilleurs résultats avec des transformateurs.</li>
                <li>Identification de commentaires inappropriés : TALN</li>
                <li>Synthèse de long documents : TALN</li>
                <li>Chatbot : TALN et Compréhension de Langage Naturel (CLN)</li>
                <li>Développement d'une interface de commande vocale : reconnaisance vocale ce qui implique le traitement d'échantillon audio ; RNR, CNR ou transformateurs.</li>
                <li>Détection d'utilisations frauduleuses de carte bancaires : c'est de la détection d'anomalies effectuer à l'aide de <strong>forêt d'isolation, de mélanges gaussions</strong> (chapitre 9).</li>
                <li>Segementation de clientèle en fonction de leurs achats : utilisation des k-moyennes, de DBSCAN ou d'autres algorithmes (chapitre 9).</li>
                <li>Visualisation de données à partir d'un jeu de données complexe de grande dimension.</li>
            </ul>
        </li>
      </ul>
    </td>
  </tr>
</table>

### Résumé
> - Le Machine Learning est à la fois une **science** et un **art**, consistant à programmer les ordinateurs pour qu'ils apprennent à partir de données, sans être explicitement programmés.
> - Il a été utilisé pour la première fois à grande échelle dans les années 1990, notamment pour les **filtres de spam**.
> - **Applications typiques** :
>   - Analyse et classification d'images (CNN, transformateurs).
>   - Détection de tumeurs et anomalies médicales (CNN, transformateurs).
>   - Traitement automatique du langage naturel (TALN), comme les chatbots ou la classification d'articles.
>   - Reconnaissance vocale et interfaces vocale (RBR, CNN, transformateurs).
>   - Détection de frandes bancaires (forêt d'isolation, mélanges gaussiens).
>   - Segmentation client et analyse comportementale (k-moyennes,DBSCAN).
>   - Visualisation et exploitation de données complexes.

---

## Supervision de L'apprentissage

<table>
  <tr>
    <td style="width: 30%; vertical-align: top; border-right: 1px solid #ccc;">
      <h3>Mots-clés / Questions</h3>
      <ul>
        <li><strong>Cible</strong> (en anglais <i>target</i>) : Prédiction de valeur numérique.</li>
        <li><strong>Caractéristiques</strong> : Ce sont les atributs ou variables d'une observation.</li>
        <li><strong>Variables explicatives</strong> (ou <i>prédicateurs)</i>: Représentent les caractéristiques de l'observation. Exemple pour une voiture : Km, âge; marque, etc.</li>
        <li>1. <strong>Qu'est-ce que l'apprentissage supervisé 2 ?</strong>
        </li>
        <li>2. <strong>Qu'est-ce qu'une tâche de classification ?</strong>
        </li>
        <li>3. <strong>Qu'est-ce qu'une variable cible (target) ?</strong>
        </li>
        <li>4. <strong>Quelles sont les caractéristiques ou variables explicative ? ?</strong>
        </li>
        <li>5. <strong>Quels sont les exemples d'applications en apprentisaage supervisé ?</strong>
        </li>
      </ul>
    </td>
    <td style="width: 70%; vertical-align: top; padding-left: 10px;">
      <h3>Notes principales</h3>
      <ul>
        <li>Les systèmes d'apprentissage automatique peuvent être classés en fonction de l'importance et de la nature de la supervision qu'ils requièrent durant la phase d'entraînement.</li>
        <li><strong>Apprentissage supervisé</strong> :</li>
            <ul>
                <li>Les données d'entraînement fournis à l'algorithme comportent les soulutions désirés, appelées <i>étiquettes</i> (en anglais, <i>labels</i>). <a href="/images/CHAPITRE_1/Fig_1-5.png">Voir Figure 1.5</a></li>
                <li>
                Une des tâches classique d'apprentissage supervisé est la <i>classification</i>. Par exemple le filtre de spam.</li>
                <li>Autre tâche classique est de prédire une valeur numérique <i>cible</i>, telle que le prix d'une voiture et cela à partir des valeurs d'un certains nombre d'<i>attributs</i> ou <i>variables</i>.<a href="/images/CHAPITRE_1/Fig_1-6.png">Voir Figure 1.6</a></li>
            </ul>
        <li><strong>Apprentissage non supervisé</strong> :</li>
            <ul>
                <li>Les données d'apprentissage ne sont pas étiquetées, le système essaie d'apprendre sans professeur.</li>
                <li>Exemple avec des données sur les visiteurs d'un blog :</li>
                    <ul>
                    <li>Utilisation du <i>partitionnment</i> (en anglais, <i>clustering</i>) pour tenter de détecter des groupes de visiteurs similaires.<a href="/images/CHAPITRE_1/Fig_1-8.png">Voir Figure 1.8</a></li>
                    <li>À aucun moment il est dit à l'algorithme il est dit à quel groupe un visiteurn appartient.</li>
                    <li>Avec l'utilisation d'un algorithme de partitionnement de type <i>classification hiérarchique</i> (en anglais, <i>hierarchical clustering</i>), il subdivisera éventuellement chaque groupe en groupes plus petits.</li>
                    </ul>
              <li>Il est judicieux de tenter de réduire le nombre de variables des données d'entraînement -> réduire la dimension de l'espace sur lequel vous allez travailler avec un algorithme de réduction de dimension. Exécution plus rapide de l'algorithmz d'apprentissage, les données occuperont moins d'espace sur le disque et en mémoire et dans certains cas possibilité d'avoir de meilleurs résultats.</li>
              <li>Une des tâches non supervisée d'importance est la <i>détection d'anomalies</i> qui sert principalement pour détecter des transactions de carte bancaire inhabituelles. Il est important d'avoir un jeux de données très propre car le système reçoit essentiellement des observations normales afin d'apprendre à les reconnaître.</li>
            </ul>
        <li><strong>Apprentissage semi-supervisé :</strong></li>
            <ul>
              <li>L'étiquetage des données prend beaucoup de temps et d'argent, il est courant d'avoir des observations non étiquetées et peu étiquetées.</li>
              <li>Ce genre d'apprentissage est souvent utilisé pour les services d'hébergement d'images tels que Google Photos. Où en donnant simplement une étiquette par personne reconnu il va classer les photos avec cette personne sous la même étiquette.</li>
            </ul>
        <li><strong>Apprentissage auto-supervisé</strong> :</li>
            <ul>
              <li>Génére un jeu de données entièrement étiqueté à partir de données totalement dépourvues d'étiquettes. Avec ce nouveau jeu de données, n'importe que algorithme d'apprentissage supervisé peut être utilisé.</li>
              <li>En général l'étape finale consiste à affiner le modèle sur un jeu de données étiquetées. Ce transfert de connaissance d'une tâche à une autre est appelé <i>apprentissage par transfert</i> et c'est une technique les plus importantes en apprentissage automatique de nos jours, particulièrement avec l'utilisation de réseaux de neurones profonds.</li>
            </ul>
        <li><strong>Apprentissage par renforcement :</strong></li>
            <ul>
              <li>Cet Apprentissage est très différent. Le système d'apprentissage, appelé <i>agent</i>, observer l'environnement, sélectionner et accomplir des actions et obtenir sois en retour des <i>récompenses</i> ou des <i>pénalités</i>.</li>
              <li>Il doit apprendre de lui-même quelle est la meilleure stratégie, ou <i>politique</i> pour obtenir autant de récompenses que possible.</li>
            </ul>
      </ul>
    </td>
  </tr>
</table>

### Résumé
> L'apprentissage supervisé utilise des données d'entraînement étiquetées ou non pour apprendre à prédire une variable cible. Les principales tâches incluent :
- La **classification** (attribuer des catégories, comme dans les filtres de spam).
- La **régression** (prédire des valeurs numériques, comme le prix d'une voiture).
> Cette aproche repose sur l'utilisation de caractéristiques (ou variables explicatives) pour construire un modèle capable de généraliser à de nouvelles données.


## Apprentissage groupé ou apprentissage en ligne

<table>
  <tr>
    <td style="width: 30%; vertical-align: top; border-right: 1px solid #ccc;">
      <h3>Mots-clés / Questions</h3>
        <h4>Mots-clés</h4>
          <ol>
            <li><strong>Apprentissage groupé (Batch Learning)</strong> : Méthode d'entraînement sur un lot complet de données fixes.</li>
            <li><strong>Réentraînement</strong> : Processus consistant à mettre à jour un modèle en réentraînent entièrement avec de nouvelles données.</li>
            <li><strong>Dégradation du modèle</strong> : Perte de performance dur à l'évolution des données alors que le modèle reste inchangé.</li>
            <li><strong>Coût en ressources</strong> : Besoins importants en CPU, mémoire, espace disuque et temps pour entraîner un modèle.</li>
            <li><strong>Apprentissage en ligne</strong> : Entraînement progressif du modèle avec des des données arrivant en continu.</li>
            <li><strong>Mini-lots</strong> : Petits groupes de données utilisés pour l'entraînement en ligne.</li>
            <li><strong>Apprentissage hors-mémoire</strong> : Traitement de grande quantités de données trop volumineuses pour tenir en mémoire.</li>
            <li><strong>Taux d'apprentissage (learning rate)</strong> : Paramètre contrôlant la vitesse d'adaptation du modèle.</li>
            <li><strong>Dégradation des performances</strong> : Perte de qualité du modèle causée par des données incorrectes ou non représentatives.</li>
            <li><strong>Surveillance des anomalies</strong> : Processus pour détectet et réagir aux données aberrantes afin d'éviter les biais.</li>
          </ol>
        <h4>Questions</h4>
          <ol>
            <li>Qu'est-ce que l'apprentissage groupé et comment fonctionne-t-il ?</li>
            <li>Quels sont les inconvénients principaux de l'apprentissage groupé ?</li>
            <li>Pourquoi l'apprentissage groupé peut-il poser problème pour des systèmes à évolution rapide ?</li>
            <li>Quels sont les besoins en ressources pour entraîner un modèle avec méthode ?</li>
            <li>Qu'est-ce que l'apprentissage en ligne et en quoi diffère-t-il de l'apprentissage groupé ?</li>
            <li>Quels sont les avantages principaux de l'apprentissage en ligne ?</li>
            <li>Qu'est-ce qu'un mini-lot, et pourquoi est-il utilisé en apprentissage en ligne ?</li>
            <li>Comment le taux d'apprentissage influence-t-il le comportement du modèle ?</li>
            <li>Quels sont les risques associés à l'apprentissage en ligne ?</li>
            <li>Comment peut-on surveiller et gérer les anomalies dans les données d'entrée ?<li>
          </ol>
    </td>
    <td style="width: 70%; vertical-align: top; padding-left: 10px;">
      <h3>Notes principales</h3>
      <h4>Apprentissage groupé</h4>
        <ul>
          <li>L'apprentissage groupé consiste à entraîner un modèle sur un lot de données complet et fixe, ce qui nécessite des ressources importantes (CPU, mémoire, espace disque) et du temps. Une fois entraîné, le modèle est utilisé sans apprentissage supplémentaire jusqu'à ce qu'il soit réentraîné avec un nouveau jeu de données complet. Ce mode d'apprendtissage convient pour des systèmes où les données changent lentement.</li>
          <li>Cependant, il présente des limites :</li>
              <ul>
                  <li><strong>Adaptabilité limitée</strong> : Le modèle ne peut pas apprendre progressivement, ce qui peut provoquer une perte de performance si les données évoluent rapidement.</li>
                  <li><strong>Coût élevé</strong> : L'entraînement complet exige des ressources informatiques importantes, ce qui peut devenir coûteux ou irréalisable pour de grands volumes de données.</li>
                  <li><strong>Autonomie restreinte</strong> : Pour des dispositifs à ressources limitées (smartphones, engins spatiaux), l'apprentissage groupé est peu adapté.</li>
              </ul>
        </ul>
      <h4>Apprentissage en Ligne</h4>
        <ul>
          <li>L'apprentissage en ligne consiste à entraîner un modèle progressivement à partir de nouvelles données, soit une par une, soit par petits groupes appelés <strong>mini-lots</strong>. Chaque étape est rapide et économique, permettant au modèle de s'adapter en temps réel à des donénes évolutives, comme les tendances financières. Cette méthode est également adaptée aux systèmes disposant de ressources limitées, comme un smartphone.</li>
          <li><strong>Avantages :</strong><li>
            <ul>
              <li><strong>Adaptabilité</strong> : Idéal pour des environnements changeants et des systèmes en évolution rapide.</li>
              <li><strong>Apprentissage hors-mémoire</strong> : Permeet de traiter des volumes de données trop importantes pour être chargés en mémoire.</li>
            </ul>
          <li><strong>Limitations :</strong></li>
            <ul>
              <li><strong>Sensibilité au taux d'apprentissage :<strong></li>
                <ul>
                  <li>Taux élevé : Adaptation rapide, mais risque d'oublier les anciennes données.</li>
                  <li>Taux faible : Meilleure stabilité, mais mois de réctivité.</li>
                </ul>
              <li><strong>Risque de dégradation :</strong> Une mauvaise qualité des nouvelles données peut détériorer les performances du modèles.</li>
              <li><strong>Surveillance nécessaire :</strong> Les anomalies dans les données d'entrée doivent être détectées et corrigées pour éviter les biais ou les erreurs (exemple : capteurs défectueux ou attaques ciblées).</li>
            </ul>
        </ul>
    </td>
  </tr>
</table>

### Résumé
- **Apprentissage groupé (Batch Learning)** :
  - Entraîenement complet sur un lot de données fixes.
  - Convient aux systèmes avec des données évoluant lentement, mais limité en termes d'adaptabilité et coûteux en ressources.
  - L'apprentissage progressif n'est pas possible, ce qui peut entraîner une perte de performance si les données changent rapidement.
- **Apprentissage en ligne (Online Learning)** :
  - Modèle entraîné progressivement avec des données arrivant en continu (une par une ou en mini-lots).
  - Idéal pour des environnements évolutifs et des sytèmes à ressources limitées.
  - Sensible au **taux d'apprentissage** :
    - Un taux élevé favorise une adaptation rapide mais risque de faire oublier les anciennes données.
    - Un taux faible assure une meilleure stabilité mais ralentit la réactivité.
  - Nécessite une surveillance des données pour détecter et corriger les anomalies ou données non représentatives.
- **Action pour approfondir** :
  - Réviser les conditions d'utilisation des deux méthodes et les impacts sur les performances selon les cas d'usage.

### Problèmes rencontrés
- Pourquoi mon modèle SVM sous-performe avec ce dataset ?
- Quelle est la différence entre RMSE et MAE ?

### Liens Jupyter notebook
Exemple de code pour la fonction `np.linspace` : [Voir le notebook](NOTEBOOK_CHAPITRE_1.ipynb).
