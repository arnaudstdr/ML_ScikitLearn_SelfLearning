# 📚 Vue d'ensemble du Machine Learning

Date : **29/12/2024**  

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
            </ul>
        <li>Exemples, définitions ou schémas</li>
      </ul>
    </td>
  </tr>
</table>

### Résumé
> Résumez ici les points clés, conclusions ou idées principales en 2-3 phrases pour une révision rapide.
- [ ] Point clé 1
- [ ] Point clé 2
- [ ] Action pour approfondir

### Problèmes rencontrés
- Pourquoi mon modèle SVM sous-performe avec ce dataset ?
- Quelle est la différence entre RMSE et MAE ?

### Liens Jupyter notebook
Exemple de code pour la fonction `np.linspace` : [Voir le notebook](NOTEBOOK_CHAPITRE_1.ipynb).
