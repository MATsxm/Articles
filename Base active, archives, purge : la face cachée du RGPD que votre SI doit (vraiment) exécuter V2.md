Article du 13 février 2026  
Par Marc-Antoine THEVENET  

# Base active, archives, purge : la face cachée du RGPD que votre SI doit (vraiment) exécuter
![rgpd_archives_95](https://hackmd.io/_uploads/HJEQ0B6tWl.jpg)

*TL;DR -- Le RGPD ne se résume pas à “définir une durée de conservation” dans un registre : l’article 5(1)(e) impose de prouver que vos données personnelles suivent un vrai cycle de vie. Concrètement : base active (usage métier), archivage intermédiaire (obligation légale / preuve / contentieux avec accès restreint), éventuellement archivage définitif (cadre spécifique), puis purge ou anonymisation effective. Cette logique se couple à l’accountability (art. 5(2)) et à l’exactitude (art. 5(1)(d)) : il faut aussi traiter les données obsolètes. Sur le terrain, c’est un chantier lourd et technique (référentiels multiples, copies, sauvegardes, droits d’accès) — au point que, dans un grand groupe, une purge/mise à jour peut mobiliser près de deux ans de travail. Bref : la conformité “durée de conservation” n’est pas un tableau Excel, c’est une ingénierie de gouvernance et de preuve.*


---

La “durée de conservation” est trop souvent traitée comme une simple ligne de registre ou une clause de politique interne. Or, au sens du RGPD, elle constitue une obligation de gouvernance : elle doit se traduire en règles opposables dans le SI, dans les processus métiers, et dans la capacité à démontrer que l’organisme ne conserve pas “par défaut”. 

> **Astuce :** partez du principe qu’en contrôle, la question n’est pas “quelle est votre durée ?”, mais “montrez-moi comment elle s’exécute et comment vous le prouvez”.

Le fondement doctrinal est l’article 5(1)(e) (limitation de conservation) : conserver “sous une forme identifiante” n’est admissible que le temps nécessaire à la finalité ; la conservation plus longue n’est pensable qu’au titre de l’archivage (intérêt public / recherche / statistique) avec garanties (renvoi à l’art. 89). 

> **Astuce :** formalisez, pour chaque traitement, un “événement de bascule” incontestable (fin de contrat, clôture de dossier, dernier contact) : c’est lui qui rend la durée défendable.

Ce principe se lit avec l’accountability (art. 5(2)) : le responsable du traitement doit être en mesure de démontrer le respect des principes. Ici, l’accountability a une portée très concrète : une règle non exécutable (ou non auditée) est une règle fragile, même si elle est bien écrite. 


> **Astuce :** exigez un livrable “preuve” (logs, rapports de purge, tickets, PV de recette) au même titre qu’un livrable “politique”.

À côté de la conservation, l’article 5(1)(d) impose l’exactitude : les données doivent être tenues à jour et les données inexactes doivent être rectifiées ou effacées. C’est un point souvent sous-estimé : l’obsolescence n’est pas seulement un problème de qualité, c’est un risque juridique autonome (décisions erronées, prospection indue, contentieux). 

> **Astuce :** introduisez des “revues de fraîcheur” (périodicité et critères) au moins pour les référentiels critiques (CRM, RH, fournisseurs, usagers).


---

### Le modèle opératoire : Base active → Archivage intermédiaire → Archivage définitif → Purge
La doctrine opérationnelle (notamment CNIL) est utile car elle convertit l’abstraction “limitation de conservation” en changements de régimes : régimes d’usage, d’accès, et de sécurité. En pratique, on ne “garde pas moins”, on fait circuler la donnée entre des espaces dont la finalité et les habilitations évoluent. 

> **Astuce :** matérialisez ces espaces dans l’architecture (même logique) : “où vit la donnée aujourd’hui ?” doit avoir une réponse technique, pas seulement documentaire.


La base active correspond à la période d’usage courant, pendant laquelle la donnée est nécessaire à la finalité principale (gestion opérationnelle d’un contrat, d’un dossier, d’un service). Le critère n’est pas la place disque, mais la nécessité fonctionnelle. 

> **Astuce :** si une donnée n’est plus consultée/éditée dans les processus normaux, elle n’a probablement plus vocation à être en base active.


L’archivage intermédiaire commence lorsque la finalité initiale est atteinte : la donnée n’est plus utile au quotidien, mais reste nécessaire pour une finalité distincte (obligation légale, preuve, précontentieux/contentieux, prescription). Ce basculement impose une logique de restriction d’accès : l’opérationnel n’est plus légitime, la consultation devient ponctuelle et justifiée (souvent juridique, audit, conformité). 

> **Astuce :** votre test simple en audit : “qui a accès ?” — si l’accès reste large, vous êtes probablement en conservation excessive déguisée.


Cet archivage intermédiaire doit être séparé (physiquement ou logiquement) de la base active et doit être gouverné : habilitations spécifiques, traçabilité, règles de “dégel” (litigation hold), sécurité cohérente. Il ne s’agit pas d’un “dépotoir”, mais d’un espace à finalité probatoire. 

> **Astuce :** imposez un principe : “archive = lecture seule + accès nominatif + journalisation”, sauf exception formalisée.


L’archivage définitif renvoie à la logique patrimoniale/historique (souvent secteur public / régime d’archives). En RGPD, ce régime ne se présume pas : il s’adosse à l’exception de l’art. 5(1)(e) et aux garanties de l’art. 89, donc à une finalité d’archivage dans l’intérêt public/recherche/statistique et à une minimisation renforcée. 

> Astuce : bannissez les formulations internes du type “on archive définitivement au cas où” : si la finalité n’est pas qualifiable juridiquement, l’argument est perdant.


La purge (effacement) ou l’anonymisation est la conséquence normale du cycle : à l’expiration des durées (base active + intermédiaire), la donnée ne doit plus exister sous forme identifiante. Juridiquement, l’enjeu n’est pas l’intention, mais la capacité à exécuter l’effacement de façon fiable (y compris sur les copies). 

> **Astuce :** distinguez “suppression logique” (masquage) et “suppression effective” (effacement réel) et fixez clairement laquelle répond à votre obligation.


---

### Au-delà du principe : sécurité, droits des personnes, et robustesse contentieuse
Conserver trop longtemps augmente mécaniquement la surface d’attaque et l’impact d’un incident, ce qui finit par rejaillir sur l’appréciation de la sécurité (art. 32) et sur la crédibilité de la gouvernance. La limitation de conservation est aussi une mesure de sécurité “par réduction du risque”. 

> **Astuce :** rattachez la purge au plan de gestion des risques SSI : cela aide à obtenir des arbitrages et des budgets.


Le droit à l’effacement n’est pas absolu, mais ses exceptions (obligation légale, défense en justice, etc.) n’autorisent pas le statu quo : elles justifient en général un basculement en archivage intermédiaire, avec restriction d’accès et durée alignée sur la prescription/obligation. En doctrine, “contentieux” justifie rarement la base active. 

> **Astuce :** documentez un processus “litigation hold” (qui décide, sur quelle base, combien de temps, quelles données) : c’est souvent le chaînon manquant.


La mise à jour des données (exactitude) se heurte aux SI éclatés : la même donnée circule entre CRM, ERP, support, marketing, fichiers partagés, messageries, exports. Sans stratégie, l’obsolescence devient structurelle et rend la conformité fragile (notamment lorsque les traitements produisent des effets sur les personnes). 

> **Astuce :** identifiez un “référentiel maître” par catégorie de données, et imposez la synchronisation (ou la priorité) plutôt que la duplication libre.



---

### Méthode “doctrine → système” : rendre l’article 5(1)(e) vérifiable
Une mise en conformité solide repose sur quatre blocs indissociables : (1) politique de conservation avec événements déclencheurs, (2) architecture d’archivage (séparation + habilitations + traçabilité), (3) mécanismes de purge industrialisés (y compris exceptions), (4) preuve d’exécution (rapports, logs, contrôles). Sans ces quatre piliers, la durée de conservation reste une promesse. 

> **Astuce :** traitez la purge comme un produit : “backlog, règles, recette, monitoring”, pas comme une tâche ponctuelle.


---

### Note terrain (DPO)
Il faut le dire nettement : la purge, comme la mise à jour de données personnelles obsolètes, est un travail chronophage et complexe (multiplicité des sources, dépendances applicatives, historiques, sauvegardes, usages métiers, résistance au changement). J’ai déjà vu des chantiers de grande ampleur s’étaler sur des durées longues : un "Camarade" DPO (:P) s’est attelé à la tâche pour un grand groupe et cela a demandé près de deux ans de travail. 

> Astuce : pour éviter l’enlisement, découpez le programme en “vagues” (traitements prioritaires, référentiels critiques, quick wins) et imposez des critères de sortie mesurables (taux de purge, réduction volumétrique, baisse des droits d’accès, preuves).


---

#TiwazConsulting #RGPD #GDPR #DPO #CNIL #DataProtection #GouvernanceDesDonnées #DataGovernance #Archivage #Purge #DataRetention #Accountability #PrivacyByDesign #SécuritéDesDonnées #Article5 #Conformité #RegistreDesTraitements #AIPD #SI #RSSI #Anonymisation
