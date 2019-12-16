# process_mining

Conversion notes:

* Docs to Markdown version 1.0β17
* Mon Dec 16 2019 03:06:35 GMT-0800 (PST)
* Source doc: https://docs.google.com/open?id=1JT3W-4urmcIay4O_hRGSXFODmRD5ZQB219OiKaBOMY4
* This is a partial selection. Check to make sure intra-doc links work.
* This document has images: check for >>>>>  gd2md-html alert:  inline image link in generated source and store images to your server.
----->


<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 0; ALERTS: 6.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>


<h2>Manuel d'utilisation de Business Process Analysis in R </h2>


<p>Suites des packages pour l'analyse des events logs (bupar)

<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Manuel-d0.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Manuel-d0.png "image_tooltip")

<h3>Introduction</h3>


**Ce manuel contient les étapes nécessaires pour faire une analyse typique des fichiers log à l'aide de bupar sur R. Ci-dessous les liens nécessaire pour aller plus loin ou pour voir les tutoriels nécessaires pour bien maîtriser ce sujet .**

<h4>LES LIENS :</h4>




*   [https://www.coursera.org/learn/process-mining/](https://www.coursera.org/learn/process-mining/) : UN TUTORIEL TRÈS COMPLET SUR LE PROCESS MINING EN UTILISANT PROMTOOLS  QUI EST LE LOGICIEL LE PLUS CONNU POUR CE DOMAINE .
*   [https://www.bupar.net/getting_started.html](https://www.bupar.net/getting_started.html) : LE SITE DE BUPAR QUI CONTIENT UN MANUEL D'UTILISATION POUR IMPLÉMENTER LES DIFFÉRENTES MÉTHODES .

<h4>Les outils pour commencer :</h4>




1. R  : pour commencer, il faut installer le logiciel R pour interpréter le code R.
2. R-studio : ce logiciel est un environnement de développement gratuit, libre et multiplateforme pour R,vous devez installer R avant R-Studio puis vous installez R-Studio .
3. Les packages nécessaires : 

    Pour installer un package, ecrivez :** install.packages(“Nompackage”) **et **library(“Nompackage”) **pour l’importer

    1. Bupar : [https://cran.r-project.org/web/packages/bupaR/bupaR.pdf](https://cran.r-project.org/web/packages/bupaR/bupaR.pdf)
    2. xesreadR : [https://cran.r-project.org/web/packages/xesreadR/xesreadR.pdf](https://cran.r-project.org/web/packages/xesreadR/xesreadR.pdf)
    3. edeaR : [https://cran.r-project.org/web/packages/edeaR/edeaR.pdf](https://cran.r-project.org/web/packages/edeaR/edeaR.pdf)
    4. processmapR : [https://cran.r-project.org/web/packages/processmapR/processmapR.pdf](https://cran.r-project.org/web/packages/processmapR/processmapR.pdf)
    5. dplyr : [https://cran.r-project.org/web/packages/dplyr/dplyr.pdf](https://cran.r-project.org/web/packages/dplyr/dplyr.pdf)
    6. devtools : [https://cran.r-project.org/web/packages/devtools/devtools.pdf](https://cran.r-project.org/web/packages/devtools/devtools.pdf)
    7. processanimateR : [https://cran.r-project.org/web/packages/processanimateR/processanimateR.pdf](https://cran.r-project.org/web/packages/processanimateR/processanimateR.pdf)
    8. processmonitR  : [https://cran.r-project.org/web/packages/processmonitR/processmonitR.pdf](https://cran.r-project.org/web/packages/processmonitR/processmonitR.pdf)
    9. stringi : [https://cran.r-project.org/web/packages/stringi/stringi.pdf](https://cran.r-project.org/web/packages/stringi/stringi.pdf)

<h3>Description de l’architecture de la suite de packages Bupar:</h3>


<h3>

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Manuel-d2.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Manuel-d2.png "image_tooltip")
 </h3>


<h3>Que faire ? :</h3>


Il y a une approche très connue dans le domaine du Process Mining et Data science pour commencer un projet ,voici les différentes étapes et les résultats correspondants :



1. **Extraction**: transformer les données brutes en données d'événement
2. **Preprocessing**: enrichir et filtrer les données d'événement
1. **Agrégation: **supprimer les données redondantes
2. **Filtrage:** afficher les modèles selon les instances de processus ou les événements
3. **Enrichissement:** ajouter des attributs de données utiles
3. **Analyse**: obtenir des informations utiles dans le processus
1. **Organisationnel**: se concentrer sur les acteurs d'un processus et sur la manière dont ils travaillent ensemble.
2. **Flux de contrôle**: mettre l'accent sur le flux et la structure du processus, par exemple (Le parcours d'un patient à la salle d'urgence).
3. **Performance**: se concentre sur le temps et l'efficacité, par exemple (combien de temps faut-il avant qu'un patient puisse quitter le service d'urgence? Ou dans quelle zone ou à quelle heure de la journée les trains sont-ils le plus en retard?)
4. **Plus loin:** existe-t-il des liens entre les acteurs et les problèmes de performance? .
1. L’EXTRACTION : 

Cette partie est très importante , elle permet d'extraire les données  et de les transformer en des datasets qui peuvent être traités dans l'analyse en process Mining , ces datasets transformés doivent répondre à des critères bien spécifiques, par exemple ils doivent avoir des colonnes comme **Case_id ou activity_id…** suivant l'utilité de chaque colonne et les critères quelle doit suivre :



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Manuel-d3.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Manuel-d3.png "image_tooltip")


**CASE_id : **contient les valeurs uniques qui permettent d’identifier les instances du processus.

**Activity id :** Chaque instance du processus est une suite des événements qui consiste à faire une activité bien definie et activity_id contient le label de cette activité par exemple : l'activité Eating 

<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Manuel-d4.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Manuel-d4.png "image_tooltip")


**Activity instance Id : **cet attribut désigne les différentes instances de chaque activité au cours des événements par exemple quelqu'un peut instancier l'activité dormir et chaque instance de cette activité à un identifiant unique .

**Lifecyle : **cycle de vie contient les différents états  des instances des activités comme par exemple start qui désigne que  cette activité vient de se commencer , Pause qui signifie qu’elle est en pause et complete qui montre que cette instance d’activité est terminée.

**Timestamp : **permet d’enregistrer le moment exact des événements (“la date et l’heure”) .

**Ressource : **identifie les différents acteurs du processus , c’est-à-dire ceux qui ont fait l'activité ou ont effectué la tâche , cette colonne peut-être vide si l’event log correspond à un seul acteur .

<h4>Création d’un event log :</h4>


Les events log que bupar accepte doivent être sous-format XES ou CSV ou base de données ,on peut structurer le dataset à l’aide de la fonction :

 eventlog(

        case_id = "patient",

        activity_id = "activity",

        activity_instance_id = "activity_instance",

        lifecycle_id = "status",

        timestamp = "timestamp",

        resource_id = "resource"

    )

en précisant pour chaque attribut du tableau la colonne correspondante dans le format des event logs standards.

Il y a différents types de problème qu’on peut rencontrer concernant les valeurs de ces attributs, par exemple si le CASE_id n’est pas unique on doit faire du nettoyage pour regler le probleme. Un problème que nous avons rencontré avec nos data sets est qu’il y avait deux colonnes en plus qui ne servent à rien, que le **CASE_id** était écrit **CASE_CONCEPT_NAME **et que l’attribut **activity_instance_id **ne contenait pas des valeurs uniques. Voici une de nos méthodes pour le nettoyage :



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Manuel-d5.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Manuel-d5.png "image_tooltip")


La méthode pour importer le dataset s’il est sous format XES est : 


```
read_xes("chemin_complet_menant_au_dataset") 	
```


en spécifiant le chemin du fichier. Sinon si c’est sous un autre format vous l’importez avec :


```
read.table("lechemin") ou read.csv("") …
```


Enfin, pour exécuter le code, vous devez l’ouvrir avec RStudio par exemple (conseillé), spécifier les bons chemins des data sets dans les fonctions read_xes (ligne 43 à 50). Puis, soit tout sélectionner et cliquer sur le bouton run (pour tout exécuter en une fois); soit se positionner sur une ligne et faire “ctrl + enter” (ceci pour exécuter les lignes une par une).

<h2>II.	PREPROCESSING et III.	Analyses : </h2>



    Ceci n’est pas une documentation des packages mais une présentation de l’approche et comment faire. Pour avoir plus de détails, veuillez aller sur le site bupar.net 


<!-- Docs to Markdown version 1.0β17 -->
