Article du 9 février 2026  
Par Marc-Antoine THEVENET  

# Centraliser l’identité, KYC et autres « Tiers de confiance » : mode d’emploi du prochain désastre
![image_reduite_moins_1Mo](https://hackmd.io/_uploads/SJdGSGhKbg.jpg)

*L’actualité bruisse d’une information devenue presque banale : **un prestataire majeur de KYC** (Know Your Customer) – autrement dit un acteur central de la vérification d’identité pour de grandes organisations, notamment financières – aurait été piraté. Qu’elle soit avérée, partielle ou exagérée, la rumeur a au moins une vertu : elle rappelle une évidence juridique et technique trop souvent écartée au profit d’un discours de “bon sens” sécuritaire. Centraliser des données d’identification extra-sensibles (pièces d’identité, justificatifs, selfies/vidéos, parfois biométrie, traces de vérification) crée mécaniquement une cible à très haute valeur et un point de défaillance unique. Autrement dit : **plus on concentre, plus on attire ; plus on attire, plus l’événement n’est pas “si”, mais “quand”.***

Ce n’est pas une hypothèse d’école. Un incident documenté, par exemple, illustre bien l’attaque “par ricochet” : Transak a indiqué qu’un attaquant, via un phishing sur un poste interne, avait accédé à l’interface d’un prestataire KYC tiers utilisé pour le scan et la vérification de documents, exposant des informations d’utilisateurs accessibles via ce tableau de bord. 

> Plus on concentre, plus on attire ; plus on attire, plus l’événement n’est pas “si”, mais “quand”.



---

### Une question ancienne : SAFARI, la matrice française de la défiance légitime envers les “fichiers totalisants”
La question n’a rien de nouveau. Le scandale **SAFARI** (Système Automatisé pour les Fichiers Administratifs et le Répertoire des Individus) a précisément cristallisé, dès les années 1970, le danger politique et juridique d’une interconnexion généralisée de fichiers autour d’un identifiant unique, permettant de reconstituer “la personne totale” par agrégation technique. La révélation du projet en 1974 a déclenché un mouvement qui conduira à la création d’un cadre protecteur : **la loi Informatique et Libertés (1978) et la CNIL.** La CNIL elle-même revient sur cette genèse et sur le rôle de SAFARI dans la naissance de la loi de 1978. (CNIL) Le parallèle est direct : hier, l’angoisse portait sur la centralisation administrative ; aujourd’hui, la même logique se rejoue avec des infrastructures numériques et des sous-traitants industriels de l’identité, ce qui démultiplie l’échelle, la vitesse de diffusion et l’impact en cas de compromission.


---

### La bascule contemporaine : la protection des mineurs comme vecteur de généralisation de la vérification d’âge

L’exemple le plus parlant, en ce moment, est la dynamique politique visant à interdire l’accès aux réseaux sociaux aux moins de 15 ans, ce qui suppose de fait un mécanisme de vérification d’âge. En France, un texte a été adopté en première lecture le 26 janvier 2026 à l’Assemblée nationale, conduisant à une logique opérationnelle simple : pour exclure les moins de 15 ans, il faut… contrôler l’âge de tout le monde, y compris des adultes. (Le Monde.fr)

C’est ici que l’architecture compte davantage que l’intention. Interdire (ou restreindre) l’accès aux mineurs peut être présenté comme une finalité légitime ; mais le moyen technique choisi peut produire un effet de système : une infrastructure d’identité et de contrôle qui, une fois en place, tend à être réutilisée, étendue, interconnectée — et devient, de facto, une couche de centralisation supplémentaire.


---

### Le “tiers de confiance” : une formule rassurante qui ne fabrique pas de la confiance
Dans ce type de projets, on invoque souvent un “tiers de confiance” chargé d’attester l’âge sans divulguer l’identité. Sur le papier, l’idée est d’éviter que le service final (réseau social, site, plateforme) collecte des données identifiantes. Mais juridiquement et techniquement (je rest un defenseur du ZK-Proof), l’étiquette “de confiance” ne suffit pas : **la confiance est un régime de preuve et de garanties, pas un slogan.** Un tiers – même certifié, même “labellisé” – reste un point de concentration (au minimum technique : flux, jetons, journaux, interfaces d’administration), donc une cible ; et il demeure exposé aux risques classiques (compromission, erreur de configuration, vulnérabilité supply chain, abus d’habilitations, fuite interne, etc.). Autrement dit, on ne supprime pas le risque : on le déplace et, parfois, on le massifie.

**Note :** Gabriel Attal a ainsi affirmé sur RTL, à propos de la vérification d’âge, que ***« Ni l’État, ni les plateformes de réseaux sociaux ne disposeront de ces données puisqu'hébergées par un Tiers de confiance »***. L’argument est présenté comme une garantie, au motif que l’opération passerait par un dispositif “tiers” censé neutraliser tout risque de récupération ou de fuite. Comme si l’existence d’un “tiers de confiance” suffisait, en elle-même, à rendre une architecture de contrôle d’âge non piratable et non détournable… **me voilà rassuré**.

…Et ce genre de discours trop souvent proclamé est, au choix, **la preuve d’une incompétence technique confondante, ou une posture populiste “prête à consommer”**, calibrée pour passer crème — parce qu’il suffit apparemment de prononcer “tiers de confiance” pour abolir le risque.

Certes, l’ARCOM a publié un référentiel, et la CNIL a rendu un avis en insistant sur des garanties de type **“double anonymat”** (le site ne connaît pas l’identité ; l’intermédiaire ne sait pas quel site est consulté), précisément pour limiter les risques de traçabilité et de corrélation. Ce référentiel formalise des exigences visant à empêcher la reconnaissance d’un utilisateur d’une vérification à l’autre, et à empêcher l’émetteur de preuve d’âge de savoir pour quel service la vérification est réalisée.

Mais même dans une approche “privacy by design”, on crée une nouvelle réalité : des acteurs structurants (prestataires d’âge/identité, validateurs, intermédiateurs, opérateurs de transmission) qui deviennent des points de concentration (au minimum des événements techniques, parfois des logs, parfois des données brutes selon les implémentations), et donc des cibles systémiques.


---

### Centralisation, droits fondamentaux et contrôle de proportionnalité : l’angle qu’on évite trop souvent
La centralisation d’identifiants et de preuves d’identité n’est pas seulement un sujet “cyber”. C’est un sujet de droits fondamentaux.

Dans l’ordre juridique européen, la protection de la vie privée et des données est consacrée par la Charte (articles 7 et 8). (EUR-Lex) Le cadre conventionnel (article 8 CEDH) impose, lorsqu’une ingérence est en cause, des exigences de base légale, de nécessité et de proportionnalité dans une société démocratique. 

Or, les dispositifs de vérification d’âge à grande échelle posent une question simple : crée-t-on une ingérence minimisée, strictement cantonnée à l’attribut “âge”, ou installe-t-on, en pratique, une infrastructure permettant la corrélation (qui se connecte, quand, via quel fournisseur), donc une atteinte potentiellement structurelle au secret des communications, à l’anonymat pratique et à la liberté d’aller et venir numérique ?


---

### Le RGPD : l’architecture de la minimisation, pas la religion de l’identification
Le RGPD n’interdit pas le traitement d’identité ; il impose qu’il soit **nécessaire, proportionné, sécurisé et borné**.

D’abord, les principes (article 5) exigent notamment **la limitation des finalités, la minimisation, la limitation de conservation, et l’intégrité/confidentialité** – sous le contrôle de l’accountability. Ensuite, l’article 25 (protection des données dès la conception et par défaut) commande une conception où, par défaut, on ne traite que ce qui est strictement requis. L’article 32 impose des mesures de sécurité “appropriées” au risque ; plus on centralise des données d’identité, plus on augmente le risque intrinsèque (valeur de la cible, conséquences, surface d’attaque), donc plus l’exigence de sécurité grimpe… sans jamais atteindre le “risque zéro”. Enfin, dès lors qu’un traitement est susceptible d’engendrer un risque élevé (échelle, systématicité, population vulnérable, usage de biométrie/vidéo, finalité de contrôle, etc.), l’analyse d’impact (article 35) devient, en pratique, difficilement évitable. 

> Après avoir fait un petit cours accéléré à nos politiques sur ce qu’est (vraiment) un “tiers de confiance”, il faudrait sans doute enchaîner avec l’analyse d’impact — à les entendre, on a l’impression qu’ils n’en connaissent même pas l’existence.


Le point clef est le suivant : **le RGPD est compatible avec la preuve d’un attribut** (ex. “plus de 15 ans”) ; il est structurellement en tension avec les modèles qui aboutissent à institutionnaliser la collecte d’identité pour des usages qui pourraient être servis par des mécanismes nettement moins intrusifs.


---

### L’angle mort : la “dette de risque” créée par les obligations de conservation et par la sous-traitance en cascade
En matière financière, la question est aggravée par les obligations de conservation liées à la LCB-FT : le Code monétaire et financier impose la conservation, pendant cinq ans après la fin de la relation d’affaires, des documents et informations relatifs à l’identité et aux opérations. On crée donc des stocks durables de données d’identité (et souvent des duplications, backups, archivages), ce qui augmente mécaniquement la surface exploitable en cas de compromission.

Sur le plan RGPD, l’autre point de fragilité est la chaîne de sous-traitance : consoles d’administration, prestataires KYC, solutions de vérification, hébergeurs, infogérants, support. À chaque maillon, l’exigence de l’article 28 (choix du sous-traitant, garanties suffisantes, contrat, contrôle des sous-traitants ultérieurs) devient un sujet central de gouvernance. Et, en pratique, le risque n’est pas seulement “l’attaque externe” : la compromission d’un compte interne, l’abus d’habilitations ou un sous-traitant mal maîtrisé suffisent à transformer une architecture centralisée en catastrophe industrielle.


---

### La pente naturelle : de la vérification d’âge à l’infrastructure d’identité transversale
Même lorsqu’un État ou un régulateur annonce “une vérification d’âge respectueuse de la vie privée”, une dynamique structurelle apparaît : standardiser, mutualiser, réutiliser.

Au niveau européen, la Commission travaille explicitement à une approche d’age verification dans le cadre plus large de la mise en œuvre du Digital Services Act, avec des blueprints et une trajectoire vers l’EUDI Wallet. Ce mouvement peut produire de bonnes choses (interopérabilité, réduction du bricolage, exigences “privacy”), mais il porte aussi un risque : l’installation d’un réflexe d’identification comme condition d’accès à des pans entiers de la vie numérique, avec tous les effets de cliquet que l’histoire (SAFARI) nous a appris à redouter.


---

### Pourquoi une fuite KYC/identité n’est pas une fuite comme les autres
Une fuite de données KYC n’est pas une fuite “réversible”. Une pièce d’identité, un justificatif de domicile, une vidéo de vérification, parfois des caractéristiques biométriques : cela alimente l’usurpation, la fraude documentaire, l’ingénierie sociale et, désormais, les deepfakes. On ne “réinitialise” pas une identité comme on change un mot de passe. Et plus la centralisation devient la norme, plus on élargit la population exposée : le contrôle d’âge des mineurs finit par mettre les adultes dans le même couloir de collecte, donc dans le même risque.


---

### Conclusion : le vrai sujet n’est pas le “piratage”, c’est le modèle
Qu’un prestataire KYC ait été compromis, ou qu’il ne s’agisse “que” d’une alerte, le raisonnement de fond ne change pas : la centralisation d’identités est un multiplicateur de dommages. SAFARI a fondé, en France, une culture juridique de méfiance rationnelle envers les “fichiers totalisants”. La loi Informatique et Libertés et, plus tard, le RGPD ne sont pas nés d’une obsession bureaucratique ; ils sont nés d’une idée simple : lorsque l’on construit des systèmes qui permettent l’agrégation, l’interconnexion et la traçabilité, on ne fabrique pas seulement des services — on fabrique des pouvoirs.

Et un pouvoir, tôt ou tard, est utilisé, détourné, ou compromis.


---

#TiwazConsulting #RGPD #CNIL #InformatiqueEtLibertes #ViePrivee #ProtectionDesDonnees #DonneesPersonnelles #Cybersecurite #KYC #IdentiteNumerique #VerificationDAge #TiersDeConfiance #CentralisationDesDonnees #DataBreach #FuiteDeDonnees #UsurpationDIdentite #PrivacyByDesign #Accountability #AIPD #SousTraitance #LCBFT #SurveillanceDeMasse #LibertesFondamentales #EtatDeDroit #SAFARI #ARCOM #DSA #EUDigitalIdentityWallet
