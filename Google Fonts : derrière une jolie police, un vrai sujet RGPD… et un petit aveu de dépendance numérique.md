# Google Fonts : derrière une jolie police, un vrai sujet RGPD… et un petit aveu de dépendance numérique

![google-fonts-une-question-rgpd-under-1mb](https://hackmd.io/_uploads/B1Yo2mF5Zg.jpg)


> La dépendance numérique ne s’impose pas toujours par la force. Très souvent, elle s’installe par paresse.

Je vais tenter d’expliquer quelque chose d’assez technique en le banalisant un peu (dsl les puristes), parce qu’entre nous, “chargement distant de ressources typographiques via API tierce” n’est pas exactement le genre de formule qui donne envie de poursuivre la lecture avec enthousiasme. Vous comprendrez dès lors un format quelque peu "original".

Prenons un exemple très simple.

Vous arrivez sur un site web.
Le site est élégant, le texte est beau.
La police est plus flatteuse que l’éternel duo Arial / Times New Roman.

Vous vous dites donc, que vous êtes simplement en train de lire une page.

En réalité, pas tout à fait.

Car si le site utilise Google Fonts à distance, il ne sert pas lui-même sa police. Le navigateur de l’utilisateur va chercher les ressources nécessaires directement auprès de Google. Google précise d’ailleurs que son API Google Fonts ne dépose pas de cookies (ouf !), mais qu’elle reçoit notamment l’adresse IP de l’utilisateur, l’URL demandée ainsi que des en-têtes HTTP comme le user-agent et le referer.

Et c’est là que le sujet devient intéressant.

Parce que beaucoup de gens pensent encore que, s’il n’y a pas de cookie, il n’y a pas de sujet vie privée.

**C’est faux !**

Le cookie n’est qu’un outil parmi d’autres. Une simple requête vers un service tiers peut déjà suffire à créer un flux de données personnelles. Et en droit européen, l’adresse IP n’est pas un détail technique folklorique laissé à l’abandon dans un coin du navigateur : c’est bien une donnée personnelle. La CNIL le rappelle expressément.

> Autrement dit, derrière une police “un peu plus jolie”, on n’a pas seulement un choix graphique. On a aussi, potentiellement, un traitement de données personnelles.

Pas forcément un immense scandale.
Pas nécessairement un dispositif de surveillance façon roman dystopique (le mien va bientôt sortir 😂).
Mais certainement pas un non-sujet.

Le vrai problème n’est pas typographique. **Il est juridique.**


---


À partir du moment où un site fait appel à un tiers pour charger une ressource, il faut regarder la situation pour ce qu’elle est réellement : un flux vers un destinataire externe, impliquant au moins certaines données techniques associées à la navigation.

Cela signifie qu’il faut raisonner en juriste et non en simple amateur de belles polices.

Il faut se demander :

Le traitement est-il identifié ?
Quelle est sa base légale ?
L’information fournie aux personnes est-elle correcte ?
Le flux est-il nécessaire ?
Existe-t-il une alternative moins intrusive ?
Et, sait-on vraiment où partent les données ?

Oui, tout cela… pour une police de caractères.

Le numérique a parfois ce talent particulier : réussir à transformer un détail d’apparence anodine en mini-cas pratique de droit des données personnelles.


---


### La base légale : là où le confort cesse d’être une justification

Dans ce type de situation, beaucoup d’organismes seront tentés d’invoquer l’intérêt légitime.

Après tout, vouloir un site harmonieux, lisible, cohérent, agréable à consulter, cela peut parfaitement relever d’un intérêt légitime.

Très bien.

Mais l’intérêt légitime n’est pas un joker juridique que l’on brandit en disant :
“J’aimais bien cette typographie, donc j’ai externalisé sans trop réfléchir.”

La CNIL rappelle qu’un traitement fondé sur l’intérêt légitime suppose bien plus qu’une préférence de confort : il faut un intérêt légitime réel, un traitement nécessaire à la poursuite de cet intérêt, **et une mise en balance avec les droits et libertés des personnes concernées.**

Et c’est précisément ici que Google Fonts à distance devient juridiquement inconfortable.

Pourquoi ?
> Parce que la même police peut très souvent être hébergée localement.

Autrement dit, si vous pouvez obtenir le même résultat visuel, avec la même qualité d’affichage, sans faire partir une requête chez un tiers, il devient tout de suite plus difficile d’expliquer que l’externalisation était réellement “nécessaire”.

En français courant :
> quand vous pouvez faire la même chose proprement chez vous, il faut commencer à avoir de très bons arguments pour justifier le détour chez le voisin.



---


### La transparence : le point faible de beaucoup de sites

Le RGPD impose une information concise, transparente, compréhensible et aisément accessible. La CNIL le rappelle très clairement au sujet des articles 12, 13 et 14 du RGPD.

Et c’est souvent ici que les difficultés commencent.

Parce que beaucoup de sites excellent dans l’art d’écrire des phrases très nobles sur la confiance, le respect, l’engagement et la protection de la vie privée.

En revanche, quand il s’agit d’expliquer concrètement qu’une simple police appelle un tiers et entraîne un flux de données techniques, le silence devient tout de suite beaucoup plus inspiré.

Or la conformité n’est pas censée se limiter aux grands traitements visibles, spectaculaires ou “marketingement” identifiables. Elle concerne aussi les petites dépendances techniques qui, mises bout à bout, organisent la circulation réelle des données.

Et c’est précisément ce qui rend ce sujet intéressant : il rappelle que le RGPD ne commence pas avec les plateformes géantes ou l’IA générative. Il commence souvent dans l’architecture la plus banale du web quotidien.

### Le chapitre V du RGPD qui débarque… pour une police

Et puis il y a la question que tout DPO finit tôt ou tard par se poser : **où vont les données ?**

Dès lors qu’un service tiers entre en jeu, la question des destinataires et, le cas échéant, des transferts internationaux n’est jamais très loin.

Sur ce point, la Commission européenne rappelle que le EU-U.S. Data Privacy Framework bénéficie d’une décision d’adéquation adoptée le 10 juillet 2023, permettant les flux vers les organismes américains qui y participent. Google LLC apparaît d’ailleurs sur la liste officielle des participants au programme.

Cela ne signifie pas que tout débat s’évanouit comme par magie. Cela signifie simplement que le cadre juridique n’est plus celui du grand chaos post-Schrems II que beaucoup ont connu. Mais pour un éditeur de site, cela reste un rappel très concret : même pour afficher une typographie soignée, on peut se retrouver à rouvrir des questions de flux internationaux, de documentation et de cartographie des destinataires.

Ce qui est tout de même une manière assez baroque de gérer un choix esthétique.


---

### Minimisation, privacy by design… et un peu de bon sens

Le point le plus simple est souvent le plus oublié.

Si une police peut être servie localement, sans solliciter un tiers, sans exposer l’utilisateur à une transmission supplémentaire, sans complexifier l’analyse juridique, sans élargir inutilement la chaîne de dépendance technique, alors cette solution est bien souvent la plus cohérente.

Et elle l’est à plusieurs titres à la fois.

Elle est plus sobre.
Elle est plus maîtrisée.
Elle est plus lisible juridiquement.
Elle est plus conforme à l’esprit de minimisation.
Et elle est plus fidèle à une logique de privacy by design.

En somme, elle a le mérite rare de réduire à la fois le bruit technique, le risque juridique et la paresse architecturale.


---

### Et la souveraineté numérique dans tout ça ?

C’est ici, à mon sens, que le sujet dépasse largement la seule question RGPD.

Google Fonts n’est pas seulement une affaire de conformité.

C’est aussi un symptôme culturel.

Le symptôme d’un web qui a pris l’habitude d’externaliser presque tout : les polices, les scripts, les bibliothèques, la mesure d’audience, les captchas, les vidéos, les dépendances front, les CDN, les widgets, parfois même des fonctions élémentaires qui pourraient parfaitement être maîtrisées en interne.

Pris séparément, chaque appel paraît anodin.
Mis bout à bout, ils racontent autre chose.

Ils racontent un numérique qui, par habitude plus que par nécessité, accepte de dépendre d’acteurs tiers — souvent extra-européens — pour des briques pourtant simples, courantes, parfois presque triviales.

Et c’est exactement là que la souveraineté numérique cesse d’être un slogan pour colloque ministériel.

Elle devient une question très concrète :

> Sommes-nous encore capables de faire tourner un site simple, élégant, performant et juridiquement propre sans dépendre d’un prestataire externe pour afficher une police de caractères ?

La question a l’air modeste.
Elle ne l’est pas.

Parce que la souveraineté numérique ne commence pas seulement dans les grands débats sur le cloud, l’IA ou les infrastructures critiques. Elle commence aussi dans les petits choix techniques du quotidien : ce que l’on héberge, ce que l’on maîtrise, ce que l’on délègue par nécessité… et ce que l’on abandonne par réflexe.

Sous cet angle, héberger localement une police, ce n’est pas seulement une bonne pratique RGPD.
C’est aussi un petit acte de maîtrise technique.
Un choix de sobriété.
Et, à son échelle, un geste de souveraineté numérique.

Pas le grand soir.
Pas une révolution.
Mais déjà un refus poli de la dépendance inutile.


---


### La vraie morale de l’histoire

Google Fonts à distance n’est pas “le mal absolu”.
Mais ce n’est pas neutre.

Ce n’est pas seulement un choix de design.
C’est potentiellement un traitement de données personnelles, un flux vers un tiers, une base légale à justifier, une information à fournir, un destinataire à documenter, et un révélateur très concret de notre dépendance technique.

Et au fond, c’est peut-être cela qui mérite d’être retenu :

Quand une police peut être servie localement, continuer à la charger depuis un tiers n’est pas seulement un choix discutable au regard du RGPD. C’est aussi, très souvent, un petit renoncement inutile à la maîtrise de son propre environnement numérique.

On parle souvent de souveraineté numérique comme d’un horizon stratégique lointain.
Mais parfois, elle commence beaucoup plus humblement.

Par exemple au moment très précis où l’on décide d’arrêter d’aller chercher chez les autres ce que l’on peut parfaitement héberger chez soi.

Et comme dirait Benjamin Bellamy qui m'a inspirer cet article : 
> La dépendance numérique ne s’impose pas toujours par la force. Très souvent, elle s’installe par paresse.


---
***Note de bas de page :** les développements techniques relatifs au fonctionnement précis des appels à Google Fonts ont été volontairement écartés ici. En pus que synthèse, lorsque les polices sont chargées depuis une source externe, Google peut associer une adresse IP à la consultation d’une page déterminée sur un site identifié.*


---


#TiwazConsulting #RGPD #ProtectionDesDonnees #ViePrivee #Privacy #DPO #SouveraineteNumerique #Web #DeveloppementWeb #GoogleFonts #PrivacyByDesign #Minimisation #Conformite #DonneesPersonnelles #TransfertsDeDonnees #EuropeNumerique #NumeriqueResponsable #Google #LegalTech #CNIL #DataProtection
