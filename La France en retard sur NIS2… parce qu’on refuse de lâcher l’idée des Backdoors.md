Article du 26 février 2026
Par Marc-Antoine THEVENET

# La France en retard sur NIS2… parce qu’on refuse de lâcher l’idée des Backdoors
![NIS2_moins_1MB](https://hackmd.io/_uploads/BJTK5ZAuWl.jpg)
*Il y a des textes qui devraient avancer sans même qu’on ait besoin de forcer. Pas parce qu’ils sont “techniques”. Mais parce qu’ils touchent à ce qui tient encore debout quand tout vacille : la résilience.*

*La transposition de NIS2 (et des volets “entités critiques”/résilience) fait partie de ces textes. On parle ici de continuité d’activité, de sécurité des SI, de gouvernance, de notification d’incidents, de responsabilisation des acteurs — bref, de la mise en cohérence d’un pays qui vit désormais dans le numérique, qu’il le veuille ou non.*

*Et pourtant, le débat public — relayé notamment par Philippe Latombe — laisse entendre une chose inquiétante : ce texte serait retardé, voire bloqué, parce qu’un point cristallise tout. Un point qui n’a rien d’anecdotique : le chiffrement. Plus précisément, l’article 16 bis introduit au Sénat, visant à empêcher qu’on impose des mécanismes d’affaiblissement volontaire (clés maîtresses, accès non consenti, “portes dérobées”, appelez ça comme vous voulez).*

> Je vais le dire sans détour : si l’on retarde une loi de résilience cyber pour préserver la possibilité d’affaiblir le chiffrement, alors on est en train d’organiser le monde à l’envers.

---

### I - Le chiffrement n’est pas un confort : c’est une garantie
On parle souvent du chiffrement comme d’un “outil” utilisé par les uns et les autres. C’est faux. Le chiffrement est surtout une garantie collective :

garantie que nos communications ne deviennent pas un buffet à volonté pour les prédateurs (criminels, espions, opportunistes) ;
garantie que les données sensibles des entreprises, des hôpitaux, des collectivités, des avocats, des journalistes, des citoyens ne sont pas, par design, exposées ;
garantie qu’un incident de sécurité ne se transforme pas automatiquement en catastrophe nationale parce que l’architecture a été rendue fragile volontairement.

En tant que juriste et DPO, je ne peux pas faire semblant : affaiblir le chiffrement, ce n’est pas “faciliter les enquêtes”. C’est fabriquer un risque systémique.

Et un risque systémique, par définition, n’est pas “gérable” par des slogans.

---

### II - Backdoor, “accès encadré”, “exception technique” : même problème, même pente
On peut maquiller le débat avec des mots rassurants : “accès légal”, “accès sous contrôle”, “exception”, “encadrement”. Mais juridiquement et techniquement, la question ne change pas.

Soit on reste dans une logique ciblée, proportionnée, contrôlable : enquête, saisies, exploitation d’un terminal, infiltrations sous contrôle, coopération judiciaire, etc.
Soit on crée une logique structurelle : un mécanisme d’accès intégré, industrialisable, donc exploitable et extensible.

Une backdoor n’est jamais “neutre”. Ce n’est pas une “clé réservée aux gentils”. C’est une faiblesse. Et les faiblesses finissent toujours par avoir plusieurs utilisateurs.

Pour plus d'information et critiques sur le sujet, n'hésitez pas à lire mes précédentes publications.

---

### III - Le droit n’a pas vocation à compenser une difficulté opérationnelle par une atteinte de masse
Il est souligné l’idée qu’un service régalien aurait des difficultés opérationnelles croissantes face au chiffrement généralisé (RCS, E2EE, etc.). Très bien. Admettons même que ce constat soit exact.

Mais juridiquement, c’est là que le raisonnement doit s’arrêter.

Parce que la conséquence implicite — “c’est plus difficile donc il faut un accès structurel” — est une dérive. Une dérive vers quoi ? Vers un État qui se donne les moyens non pas d’enquêter sur des individus, mais de rendre possible l’accès à tous les individus, par architecture.

Et là, on change de nature : on ne parle plus de sécurité. On parle de capacité de surveillance.

Or, la logique des libertés fondamentales est précisément de dire :

l’État n’obtient pas des pouvoirs structurels sur tous au motif que c’est “plus pratique”.

Le principe de proportionnalité n’est pas une formule décorative. C’est une barrière. Et plus une mesure est large, plus cette barrière doit être haute.

---

### IV - Le paradoxe NIS2 : renforcer la cyber… en affaiblissant la sécurité ?
C’est peut-être le point le plus absurde : NIS2 vise un niveau élevé de cybersécurité, une meilleure maturité, une gouvernance renforcée, une résilience accrue.

Et, dans le même mouvement, certains voudraient garder ouverte l’idée d’un affaiblissement volontaire d’un des piliers de la sécurité moderne.

Je pose la question simplement : comment peut-on exiger des organisations qu’elles augmentent leur niveau de sécurité tout en envisageant de leur imposer une fragilité ?

Côté conformité, c’est un casse-tête :

comment un RSSI peut-il “réduire le risque” quand un risque est injecté par construction ?
comment un DPO peut-il défendre l’idée de sécurité appropriée, de confidentialité, d’intégrité, si l’on institutionnalise une faiblesse ?
qui portera la responsabilité lorsque cette fragilité sera exploitée (et elle le sera) ? l’éditeur ? l’organisation ? l’État ? personne ?

On ne construit pas une politique de résilience sur un trou béant “réservé aux bonnes intentions”.

---

### V - Le vrai problème, c’est la méthode : mélanger résilience et tentation de surveillance
Si l’article 16 bis pose des questions de technique législative (cavalier, article 45, etc.), cela se discute. Mais cela ne justifie pas de prendre en otage un texte de transposition essentiel.

S’il doit y avoir un débat sur un “accès légal” aux contenus chiffrés, qu’il soit autonome, frontal, assumé, et jugé à l’aune :

de la nécessité,
de la proportionnalité,
des garanties,
et des contrôles indépendants réellement robustes.

Pas greffé dans un texte de cybersécurité comme si c’était un simple détail.

Parce que ce n’est pas un détail. C’est une ligne de crête : celle qui sépare la sécurité d’un pays et la tentation permanente de la surveillance “par défaut”.

---

### VI - Angle DPO : le grand paradoxe “cyber” de la backdoor
Je le dis sans détour : exiger (directement ou indirectement) un affaiblissement du chiffrement, c’est créer une contradiction normative entre :

NIS2, qui organise la montée en maturité cyber, la gestion des risques, la notification, la résilience.
RGPD, qui impose une sécurité appropriée, et dont la mise en œuvre concrète (dans les guides, la pratique, les contrôles) valorise des mesures robustes, dont le chiffrement lorsqu’il est pertinent.
et l’objectif affiché de la Stratégie nationale 2026-2030, qui assume le chiffrement comme composant essentiel du socle de sécurité.

Ce n’est pas seulement une bataille idéologique. C’est une question d’accountability : qui portera la charge des incidents facilités par l’affaiblissement ? Qui répondra aux personnes concernées quand une fragilité “imposée” sera exploitée ? Quelle position pour les RSSI, les DPO, les assureurs, les sous-traitants, les éditeurs ?

> La vérité opérationnelle, c’est que la backdoor transforme l’exception en architecture — et l’architecture en risque systémique.

---

### VII - Ma position (et je la maintiens) : la DGSI n’est pas le centre du droit
Je vais formuler cela proprement, mais fermement :

L’éventuelle difficulté d’un service, quel qu’il soit, ne doit jamais devenir un prétexte pour fragiliser les libertés fondamentales de millions de personnes.
La réponse à la complexité technologique, ce n’est pas “affaiblissons le socle”. C’est : moyens, doctrine, ciblage, coopération, investigation moderne — et oui, acceptation démocratique d’un certain niveau de contrainte… mais dans les limites du droit.

Le droit n’existe pas pour rendre l’État “plus confortable”. Il existe pour rendre l’État légitime.
Conclusion

NIS2 est une nécessité. La résilience est une urgence. Le chiffrement n’est pas l’ennemi : c’est l’un des derniers remparts rationnels contre le chaos cyber, l’espionnage, la criminalité et les abus.

On ne renforce pas la cybersécurité en organisant, même “exceptionnellement”, l’affaiblissement de la sécurité.

Une démocratie ne se défend pas en installant des fragilités structurelles au cœur de la vie privée de tous.
> Le chiffrement protège la société. Les backdoors protègent l’idée qu’on se fait du contrôle. Ce n’est pas la même chose.

---

#TiwazConsulting #NIS2 #Cybersecurite #Cybersécurité #ResilienceNumerique #InfrastructureCritique #EntitesEssentielles #EntitesImportantes #ANSSI #Renseignement #DGSI #Chiffrement #EndToEndEncryption #E2EE #Backdoor #PortesDerobees #SecretDesCorrespondances #ViePrivee #LibertesFondamentales #EtatDeDroit #Proportionnalite #Necessite #ControleDemocratique #CNIL #RGPD #Accountability #SecuriteDesDonnees #PrivacyByDesign #PrivacyByDefault #SurveillanceDeMasse #SecuriteNationale #DroitsHumains #CEDH #CJUE #France #Europe #SouveraineteNumerique
