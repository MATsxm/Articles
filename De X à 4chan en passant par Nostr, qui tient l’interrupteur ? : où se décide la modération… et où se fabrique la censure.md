Article du 1 mars 2026  
Par Marc-Antoine THEVENET  

# De X à 4chan en passant par Nostr, qui tient l’interrupteur ? : où se décide la modération… et où se fabrique la censure
![nostr_quant_256](https://hackmd.io/_uploads/ByCCUoct-e.png)

*Quand on découvre Nostr, Mastodon ou Bluesky, on tombe vite sur une promesse implicite : “décentralisé = liberté” et, par ricochet, “décentralisé = pas de censure”. C’est séduisant, mais c’est rarement vrai tel quel. Dans la vraie vie du web, la question n’est pas “y aura-t-il une forme de modération ?”, mais plutôt : où se situent les points de contrôle et combien il y en a.*

*Pour clarifier, il faut d’abord distinguer trois notions que l’on confond en permanence.*

*La première, c’est la censure au sens strict, généralement associée à une intervention publique (interdiction, blocage ordonné, sanction). La deuxième, c’est la modération privée, c’est-à-dire l’application de conditions d’utilisation par un opérateur (qui, juridiquement, n’est pas une “censure” stricto sensu, même si l’effet ressenti peut être identique). La troisième, plus insidieuse, c’est l’invisibilisation : vous pouvez poster, mais votre contenu n’est plus distribué, plus recommandé, plus visible. Et dans un univers dominé par les “feeds”, la distribution est parfois plus déterminante que l’existence même du contenu.*

*Avec cette grille en tête, on peut comparer cinq modèles : les réseaux centralisés “traditionnels” (X, Facebook…), 4chan (centralisé mais anonyme et “éphémère”), Mastodon (fédération), Bluesky (fédération en construction + modération modulaire), et Nostr (identité par clés + réseau de relays).*


---

### 1 - Les réseaux “traditionnels” : centralisation = pouvoir unifié (et très efficace)
Sur X, Facebook, Instagram, TikTok, etc., le schéma est simple : vous avez un opérateur, une infrastructure, une base de données, une logique de compte gérée par la plateforme, et presque toujours une couche algorithmique de distribution. Autrement dit, une seule entité contrôle à la fois l’hébergement (ce qui existe), les règles (ce qui est autorisé) et la visibilité (ce qui circule).

C’est la centralisation dans sa forme la plus pure. Elle a des avantages très concrets : l’expérience utilisateur est homogène, l’infrastructure est massivement optimisée, et la plateforme peut appliquer des politiques à grande échelle en quelques minutes. Mais la contrepartie est structurelle : un seul bouton peut couper le micro. Suppression de contenu, suspension de compte, démonétisation, ou simple “déclassement” algorithmique : la décision est unifiée, l’effet est global.

C’est aussi pour cela que le débat public se focalise sur ces plateformes : quand le centre décide, tout le monde le ressent.


---

### 2 - 4chan : centralisé, anonyme… et pourtant modéré (et pas du tout décentralisé)
4chan est un excellent “contre-exemple pédagogique”, parce qu’il casse deux illusions fréquentes : l’anonymat n’est pas la décentralisation, et l’absence (relative) d’algorithme n’est pas l’absence de contrôle.

D’un point de vue architecture, 4chan est centralisé : un seul site, une seule infrastructure, un seul opérateur. Les utilisateurs postent généralement sans inscription, donc avec une forte sensation d’anonymat (au moins dans l’interface). Les descriptions générales du service rappellent d’ailleurs le caractère “anonymous imageboard” et l’absence de système d’inscription pour le public.

Ce qui rend 4chan particulier, c’est sa mécanique “board + threads” et son côté éphémère. 4chan explique lui-même une règle très simple : à chaque création de nouveau thread, un thread est supprimé/pruné. Cette logique fait que beaucoup de contenu “disparaît” parce que le site est conçu comme un flux à capacité limitée. Sur le plan sociotechnique, c’est important : un contenu peut sortir du radar non pas parce qu’il est modéré, mais parce qu’il est poussé hors de la fenêtre d’affichage.

Mais cela ne doit pas faire croire à une absence de modération. 4chan dispose d’une organisation de modération opérationnelle : le formulaire “Janitor Applications” décrit explicitement des tâches comme retirer des threads, réponses et images et soumettre des demandes de ban/warn. Donc, même sur un espace “anonyme”, il existe des personnes qui ont des leviers d’action (et un opérateur central qui les délègue).

Dernier point (souvent ignoré) : l’“éphémère” sur le site ne signifie pas “effacé du monde”. L’ArchiveTeam documente le fait que 4chan supprime des threads (bump limits / pruning), tout en rappelant l’existence de nombreux sites d’archives qui sauvegardent threads et images.

En clair : 4chan peut être centralisé et “auto-effaceur” dans sa logique interne, mais le web, lui, copie. Et ces copies peuvent rendre l’effacement pratique (ou juridique) bien plus complexe.

4chan occupe une place très instructive : un point de contrôle unique (comme X/Facebook) + une identité faible (anonymat apparent) + une modération réelle + une disparition souvent “mécanique” (pruning) + une survivance externe par archivage.


---

### 3 - Mastodon : fédération ActivityPub et modération par communautés
Mastodon s’inscrit dans le Fediverse et repose sur ActivityPub, un standard W3C publié comme Recommandation pour la mise en réseau de services sociaux décentralisés (avec des API client-serveur et serveur-serveur).

Concrètement, Mastodon n’est pas “un site” mais une constellation d’instances (serveurs indépendants). Vous vous inscrivez quelque part, et votre instance fédère (ou non) avec d’autres. Le résultat, c’est que la modération devient d’abord locale : l’admin de votre instance contrôle votre environnement immédiat, pas l’ensemble du réseau.

C’est d’ailleurs une logique assumée dans la documentation : pour éviter d’avoir à modérer individuellement de gros volumes d’utilisateurs provenant d’un serveur problématique, Mastodon permet de modérer “des sites entiers” via les domain blocks. Autrement dit, la “censure” (au sens d’empêcher de voir) peut se produire non pas sur une personne isolée, mais sur une instance entière : si deux instances cessent de fédérer, leurs communautés ne se voient plus, ou beaucoup moins.

Mastodon va encore plus loin avec le limited federation mode, qui permet de transformer l’instance en silo en désactivant la fédération large (mécaniquement contraire à l’idée d’un réseau ouvert, mais parfois choisi pour un usage interne). La documentation explique ce mode et ses effets sur les allow-lists / block-lists.

 Le point crucial pour un novice : Mastodon réduit le pouvoir d’un centre unique, mais il le remplace par une pluralité de centres plus petits. La liberté dépend donc fortement du choix de l’instance (culture, règles, tolérance, qualité de modération). On n’est plus dans “un arbitre”, on est dans “des mairies”, avec tout ce que cela implique : protection, mais aussi frontières.


---

### 4 - Bluesky : une fédération “par architecture”, et une modération modulaire (“stackable”)
Bluesky est intéressant parce qu’il est souvent perçu comme “un nouveau Twitter”, alors que son ambition est de reposer sur un protocole (AT Protocol / atproto) visant l’interopérabilité et la portabilité des comptes/données dans un réseau fédéré. La documentation décrit atproto comme un standard et un framework open-source pour bâtir des apps sociales interopérables, avec portabilité de comptes.

Mais la différence majeure avec Mastodon tient à l’architecture technique mise en avant par Bluesky : on y distingue notamment le PDS (Personal Data Server), le Relay, et l’App View. Et surtout, la doc explique que l’App View est la pièce qui assemble le feed et produit les “vues” utilisables par une application, à partir du flux brut (“firehose”) du relay — en gros, une sorte de “prisme” qui transforme des données en expérience sociale.

Ce détail a un impact direct sur la question de la “censure potentielle”. Dans un réseau moderne, le pouvoir n’est pas seulement de stocker ou supprimer, c’est de rendre visible. Et si la couche “App View” (ou l’app dominante) devient centralisée de fait, on retrouve une partie des mécanismes de visibilité des réseaux traditionnels, même si l’architecture promet davantage de substituabilité à terme.

L’autre apport distinctif de Bluesky, c’est sa conception de la modération comme quelque chose de composable : le projet parle d’une approche “stackable” où l’utilisateur peut choisir et configurer des composants de modération, plutôt qu’un unique arbitre opaque. Dans cette logique s’inscrit Ozone, outil open-source destiné à permettre l’inspection et le “labeling” collaboratif du contenu, annoncé par le compte “Bluesky Safety”.

 Pour un novice, ça se traduit par une idée simple : Bluesky cherche à faire de la modération un écosystème (avec labels et services), plutôt qu’une seule police. Mais tant que l’expérience majoritaire passe par une app et des services “principaux”, il existe un centre de gravité. La promesse est donc réelle, mais elle dépend beaucoup de l’ouverture effective du marché des app views, relays et services de modération.


---

### 5 - Nostr : identité par clés + relays, et “résistance à la censure” par design
Nostr pousse la logique “décentralisée” plus loin sur un point précis : l’identité. Dans Nostr, votre “compte” n’est pas un enregistrement sur un serveur ; c’est une paire de clés cryptographiques. NIP-01 décrit cette base : chaque utilisateur a un keypair, et l’objet fondamental est l’“event” signé, transmis via des relays.

Le dépôt principal de Nostr résume sa philosophie de manière explicite : protocole ouvert destiné à créer un réseau social global “censorship-resistant”, sans serveur central de confiance, basé sur des clés et signatures, et transmis par relays.

Le bénéfice évident, côté “censure potentielle”, est que l’on ne peut pas simplement contacter “la plateforme” pour faire disparaître une identité : il n’y a pas de compte central à fermer. Si un relay vous bloque, vous pouvez publier ailleurs, et si un client masque des contenus, vous pouvez changer d’outil. Le contrôle devient éclaté : relays, clients, listes, habitudes d’écosystème.

Mais là encore, la promesse “incensurable” est une illusion. Dans les faits, la visibilité se reconcentre souvent autour de certains relays populaires et de quelques clients dominants, et la modération peut réapparaître via des filtres côté relay ou côté client. Nostr n’abolit pas le contrôle ; il rend surtout plus difficile l’existence d’un interrupteur unique.

Et, point important : plus un système est conçu pour la réplication et la distribution multi-relays, plus la question “où sont mes données” et “qui a copié quoi” devient délicate — ce qui est, en pratique, l’autre face du débat : la résistance à l’effacement et la résistance à la censure se croisent souvent.


---

### Conclusion : la vraie question n’est pas “qui censure ?”, mais “combien de couches peuvent te rendre invisible ?”
Si on devait retenir une seule idée simple : sur un réseau social, il existe toujours des mécanismes qui peuvent réduire ou supprimer la visibilité d’une expression. La différence entre X/Facebook, 4chan, Mastodon, Bluesky et Nostr, c’est l’endroit où ces mécanismes se situent.

Sur les réseaux traditionnels, ils sont concentrés chez un opérateur unique : c’est efficace, mais vulnérable à une décision centrale. Sur 4chan, on retrouve la centralisation, mais avec une expérience anonyme et des contenus qui disparaissent souvent par conception (tout en survivant via des archives externes). Sur Mastodon, la censure/modération devient d’abord une affaire de communautés et de fédération : les frontières (domain blocks, silos) structurent la visibilité autant que les règles. Sur Bluesky, la promesse est celle d’un internet social plus portable et modulaire, avec une modération “stackable” et des briques (PDS/Relay/App View) qui peuvent, en théorie, éviter un monopole de visibilité — à condition que l’écosystème reste réellement substituable. Sur Nostr, l’identité par clés et la multiplicité de relays rendent l’interrupteur unique beaucoup plus difficile, sans faire disparaître les points de pression (relays dominants, clients dominants, infrastructures).


---

Et vous, quelle est votre expérience concrète de ces plateformes (X/Facebook, 4chan, Mastodon, Bluesky, Nostr) : avez-vous déjà constaté de la modération, de l’invisibilisation ou des “frontières” de fédération — et comment percevez-vous le meilleur équilibre entre liberté d’expression, gouvernance et responsabilité ?


---

#TiwazConsulting #RéseauxSociaux #Decentralisation #Censure #Moderation #LibertéExpression #LibertésFondamentales #ViePrivée #ProtectionDesDonnées #DonnéesPersonnelles #RGPD #DPO #Conformité #FreeSpeetch #Mastodon #ActivityPub #Bluesky #ATProtocol #Nostr #4chan #SouverainetéNumérique #GouvernanceDuWeb #Interopérabilité #PortabilitéDesDonnée #Cybersécurité #OSINT #ÉthiqueNumérique #DroitsNumériques #Surveillance #SurveillanceDeMasse
