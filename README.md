# 🔒 **OPSEC-GUIDE-FR** 🔒
<br><br>

<p align="center">
  <img src="picture/ops.jpg" width="600" style="background-color:black; padding:2px;">
</p>
<br><br>

## 📖 **Introduction**
L'**OPSEC (Operational Security)**, ou **Sécurité Opérationnelle**, est l'ensemble des pratiques qui protègent vos informations sensibles et votre identité lors d'enquêtes en **OSINT (Open Source Intelligence)**. Dans un monde où les données publiques sont abondantes, une mauvaise OPSEC peut exposer vos méthodes, votre localisation ou même menacer votre sécurité physique. Ce guide, conçu pour les débutants comme les experts, s'inspire de ressources expertes et vise à vous armer d'une mentalité défensive. 

**Pourquoi l'OPSEC ?** Elle anticipe les risques : de la simple fuite IP à une traque par des acteurs malveillants (criminels, États). Adoptez un **modèle de menace** personnalisé et itérez constamment. [Lisez plus sur les bases OPSEC](https://www.dhs.gov/sites/default/files/2024-11/24_110824_identify-theft-508.pdf) (PDF du DHS).

---

## 🎯 **1. Définir votre Modèle de Menace**
Avant de plonger dans une enquête, cartographiez les dangers. C'est la fondation de toute OPSEC !

### Étapes Clés 🚀
1. **Identifiez l'adversaire** : Un hacker amateur ou un APT étatique ? Utilisez [ce modèle MITRE ATT&CK](https://attack.mitre.org/) pour évaluer.
2. **Protégez les actifs critiques** : IP, empreinte navigateur, métadonnées, habitudes de recherche.
3. **Évaluez le niveau de risque** : 
   - **Bas** : Recherche Google basique (VPN suffisant).
   - **Moyen** : Réseaux sociaux (VM + extensions).
   - **Haut** : Dark web (Tor + TAILS).

**Outil recommandé** : Créez une mindmap avec [MindMeister](https://www.mindmeister.com/) ou consultez [ce template OPSEC](https://github.com/OffcierCia/Crypto-OpSec-SelfGuard-RoadMap).

**Emoji Tip** : 🛡️ Pensez "bouclier" – adaptez à votre scénario !

---

## 🛡️ **2. Principes Fondamentaux de l'OPSEC**
Suivez le cycle OPSEC en 5 étapes (inspiré du [manuel NSA](https://nsarchive2.gwu.edu/NSAEBB/NSAEBB436/docs/EBB-005.pdf)) :

1. **Identifier les infos critiques** 🔍 : IP, timezone, cookies, EXIF dans les images.
2. **Détecter les menaces** ⚠️ : Acteurs motivés via [OSINT Framework](https://osintframework.com/).
3. **Évaluer les vulnérabilités** 🔍 : Testez avec [Panopticlick](https://panopticlick.eff.org/).
4. **Analyser les risques** 📊 : Probabilité x Impact (utilisez [ce calculateur simple](https://www.riskwatch.com/risk-matrix)).
5. **Appliquer des contre-mesures** 🛠️ : Isolation + anonymisation.

**Principes d'Or** 💎 :
- **Compartmentalisation** : Séparez enquêtes et vie privée (un appareil dédié).
- **Anonymisation** : Masquez tout ce qui trace.
- **Blend In** : Imitez un utilisateur lambda ([guide EFF](https://ssd.eff.org/)).

---

## 🛠️ **3. Meilleures Pratiques et Outils**
### a. **Configuration de l'Environnement** 💻
- **Machine Virtuelle (VM)** : Isolez avec [VirtualBox](https://www.virtualbox.org/) ou [VMware](https://www.vmware.com/). Pour l'extrême : [TAILS OS](https://tails.net/) (bootable USB, amnésique).
- **Chiffrement** 🔐 : [VeraCrypt](https://www.veracrypt.fr/) pour disques cachés ; activez [FileVault](https://support.apple.com/fr-fr/HT204837) sur Mac.
- **Mises à Jour** 🔄 : Automatisez avec [WSUS Offline](https://wsusoffline.net/) (Windows).

**Ressource** : [Checklist VM OPSEC](https://www.tracelabs.org/initiatives/osint-vm).

### b. **Navigation et Browser** 🌐
- **Browsers Sécurisés** : [Firefox](https://www.mozilla.org/fr/firefox/new/) en mode privé ou [Brave](https://brave.com/) (bloque pubs/trackers).
- **Extensions Essentielles** 🛠️ :
  | Extension | But | Lien |
  |-----------|-----|------|
  | [HTTPS Everywhere](https://www.eff.org/https-everywhere) | Force HTTPS | EFF |
  | [uBlock Origin](https://ublockorigin.com/) | Bloque trackers/WebRTC | GitHub |
  | [Privacy Badger](https://privacybadger.org/) | Anti-tracking auto | EFF |
  | [CanvasBlocker](https://add0n.com/canvasblocker.html) | Anti-fingerprinting | Add0n |
  | [User-Agent Switcher](https://addons.mozilla.org/fr/firefox/addon/user-agent-string-switcher/) | Change profil | Mozilla |

- **Test Empreinte** : [AmIUnique](https://amiunique.org/) ou [BrowserLeaks](https://browserleaks.com/).

**Tip** : Désactivez JS via [NoScript](https://noscript.net/) pour sites suspects.

### c. **Masquage IP et Réseau** 🌍
- **VPN Premium** : [Mullvad](https://mullvad.net/) (paiement crypto, no-logs) ou [ProtonVPN](https://protonvpn.com/).
- **Tor** 🌀 : [Tor Browser](https://www.torproject.org/download/) pour .onion ; guide [ici](https://www.torproject.org/).
- **Proxy** : [Bright Data](https://brightdata.com/) pour tâches ciblées.

**Ressource** : [Comparatif VPN OPSEC](https://www.privacyguides.org/en/vpn/).

### d. **Comptes et Identités** 👤
- **Sock Puppets** : Personas via [Fake Name Generator](https://www.fakenamegenerator.com/) + photos [ThisPersonDoesNotExist](https://thispersondoesnotexist.com/).
- **Emails Jetables** : [ProtonMail](https://proton.me/mail) (encrypté) ou [Temp Mail](https://temp-mail.org/).
- **Numéros Virtuels** : [SMS-Activate](https://sms-activate.org/) pour 2FA.

**Outil** : [KeePassXC](https://keepassxc.org/) pour mots de passe.

### e. **Recherche et Sources** 🔍
- **Moteurs** : [DuckDuckGo](https://duckduckgo.com/) ou [Searx](https://searx.space/).
- **Outils Silencieux** : [Sherlock](https://github.com/sherlock-project/sherlock) pour usernames (local).
- **Métadonnées** : Nettoyez avec [ExifTool](https://exiftool.org/).

**Ressource** : [OSINT Framework Tree](https://osintframework.com/tree.html).

### f. **Communication** 📱
- **Encrypté** : [Signal](https://signal.org/) pour messagerie ; [PGP](https://www.openpgp.org/) pour emails.
- **Évitez** : Slack/Teams sans E2EE.

---

## ⚠️ **4. Exemples de Fautes et Leçons**
| Cas | Erreur | Leçon | Lien |
|-----|--------|-------|------|
| **Ross Ulbricht (Silk Road)** | Réutilisation emails/aliases | Compartiment strict | [Article Wired](https://www.wired.com/2015/03/silk-road/) |
| **Alexandre Cazes (AlphaBay)** | Patterns comportementaux | Multi-couches anonymat | [BBC Report](https://www.bbc.com/news/technology-40747881) |
| **Général OSINT** | Fuite IP en recherche | Toujours VPN+VM | [EFF Surveillance](https://ssd.eff.org/) |

**Tip** : Étudiez [ce cas d'école](https://www.bellingcat.com/resources/2021/01/11/osint-opsec-guide/).

---

## ❌ **5. Erreurs Courantes à Éviter**
- 🚫 Appareils personnels pour enquêtes.
- 🚫 Oubli EXIF ([testez ici](https://exifdata.com/)).
- 🚫 Réutilisation d'identifiants.
- 🚫 Ignorer timing/fingerprinting.
- 🚫 Partage OPSEC sur Twitter (même anonyme !).

**Ressource** : [Top 10 Erreurs OPSEC](https://www.dutchosintguy.com/post/basic-opsec-tips-tricks-for-osint-researchers).

---

## 🕵️‍♂️ **6. Cas Pratiques**
Cette section explore des cas réels d'échecs et de succès en OPSEC lors d'enquêtes OSINT. Elle illustre comment des failles ont conduit à des arrestations ou des expositions, et comment un bon OPSEC a permis des victoires décisives. Les leçons sont tirées d'analyses expertes pour renforcer votre pratique.

### a. **Cas d'Échecs OPSEC : Leçons d'Exposition**
Ces exemples montrent comment des négligences ont permis à des enquêteurs OSINT de démasquer des acteurs malveillants via des traces numériques publiques.

| Cas | Description Brève | Failles OPSEC | Leçon pour OSINT | Source |
|-----|-------------------|---------------|------------------|--------|
| **Ross Ulbricht (Dread Pirate Roberts, Silk Road, 2013)** | Fondateur du marketplace dark web arrêté après liaison d'emails personnels (rossulbricht@gmail.com) et posts forums avec son pseudonyme via Google+ et StackOverflow. | Réutilisation d'emails/aliases, style d'écriture unique, IP traces. | Compartimenter identités : évitez liens entre comptes anonymes et publics ; testez pour corrélation OSINT. | [Article Wired](https://www.wired.com/2015/03/silk-road/) |
| **Alexandre Cazes (AlphaBay, 2017)** | Admin arrêté via en-têtes emails (Pimp_Alex_91@hotmail.com) liés à posts forums de 2008 ; patterns comportementaux malgré Tor. | Réutilisation d'emails, timing opérationnel, anonymat insuffisant. | Masquez métadonnées et variez comportements ; combinez Tor/VPN pour éviter fingerprinting. | [BBC Report](https://www.bbc.com/news/technology-40747881) |
| **Emil Babadjov (Vendor AlphaBay)** | Vendeur identifié via email lié à Coinbase/Facebook (alias inversé "Lime Vojdabab"). | Liens financiers/sociaux non isolés. | Séparez finances et enquêtes ; utilisez wallets anonymes. | [Darknet Markets](https://www.vice.com/en/article/alphabay-dark-web-marketplace-emails) |
| **Jose Robert Porras (Vendor AlphaBay)** | Photo main avec marijuana : empreintes digitales extraites et matchées aux records. | Métadonnées/images non nettoyées. | Strippez EXIF/forensics visuels avant partage ; testez images. | [Vice Article](https://www.vice.com/en/article/alphabay-dark-web-marketplace-photos) |
| **APT1 (Groupe Hacker Chinois)** | Identifiés via nicknames récurrents ("Ugly Gorilla"), timestamps Beijing, IP et breaches. | Patterns naming/timing constants. | Variez alias et horaires ; analysez vos propres traces OSINT. | [Mandiant Report](https://www.mandiant.com/resources/apt1-exposing-one-of-chinas-cyber-espionage-units) |

### b. **Cas de Succès OPSEC : Victoires Grâce à l'Anonymat**
Ces enquêtes montrent comment un OPSEC solide a permis de collecter des intel sans exposition, souvent en exploitant les failles des cibles.

| Cas | Description Brève | Rôle OPSEC | Leçon pour OSINT | Source |
|-----|-------------------|------------|------------------|--------|
| **Tracking ISIS Fighters (2015)** | Photos/vidéos sociales géolocalisées (métadonnées, landmarks) pour identifier camp d'entraînement près de Raqqa ; partagé avec agences. | Anonymat via proxies, scrub de métadonnées sur données collectées. | Utilisez outils forensics (Google Earth) sans traces ; compartimentez pour éviter riposte. | [Bellingcat ISIS](https://www.bellingcat.com/news/mena/2015/06/28/the-isis-guide-to-building-an-effective-islamic-state-a-brief-history/) |
| **Exposing Poachers (Afrique du Sud)** | Posts Instagram géotaggés analysés pour traquer braconniers à Kruger ; arrestations via network analysis. | VM isolée pour scraping ; pas de liens personnels. | Bloquez géotags/cookies lors de collectes ; collaborez encrypté. | [Wildlife Crime Tech](https://www.wcs.org/our-work/wildlife-crime/wildlife-crime-technology) |
| **Identifying Russian Soldiers (Ukraine, 2014, Bellingcat)** | Selfies avec insignes/landmarks croisés avec satellite imagery ; preuve d'intervention russe. | Tor/VPN pour recherches ; crowdsourcing anonyme. | Crowdsourcéz sans exposer sources ; validez via multiples OSINT layers. | [Bellingcat MH17](https://www.bellingcat.com/news/uk-and-europe/2016/02/17/flight-mh17-downed-by-missile-fired-from-a-53rd-anti-aircraft-missile-brigade-buk-tel-9n316-rocket/) |
| **Unmasking Child Trafficking Network (Thorn)** | Scraping ads sociales pour patterns ; facial rec + missing DB pour rescues (centaines d'enfants). | Burner accounts, encryption pour data ; pas de traces vers enquêteurs. | Agrégez data sans patterns personnels ; priorisez E2EE pour collab. | [Thorn Impact](https://www.thorn.org/impact/) |

**Tip Global** : Dans ces cas, les échecs des cibles (métadonnées, réutilisation) ont été exploités via OSINT. Inversez : appliquez ces leçons pour vous protéger. Étudiez [Bellingcat's Guide](https://www.bellingcat.com/resources/how-tos/2021/01/11/osint-opsec-guide/).

---

## 🏋️‍♂️ **7. Exercices Pratiques OPSEC**
Mettez en pratique ces exercices progressifs pour tester et renforcer votre OPSEC. Commencez par les basiques et montez en complexité. Chaque exercice inclut des étapes, outils et vérifications. Temps estimé : 30-60 min par exercice.

### **Exercice 1 : Audit de Votre Empreinte Navigateur (Niveau Débutant) 🔍**
**Objectif** : Identifier et réduire votre fingerprinting.
1. Ouvrez un navigateur incognito et visitez [AmIUnique](https://amiunique.org/).
2. Notez votre score d'unicité (IP, User-Agent, Canvas, etc.).
3. Installez [uBlock Origin](https://ublockorigin.com/) et [CanvasBlocker](https://add0n.com/canvasblocker.html).
4. Retestez : Visez < 1% d'unicité.
**Vérification** : Comparez avant/après. Si >5%, ajoutez [User-Agent Switcher](https://addons.mozilla.org/fr/firefox/addon/user-agent-string-switcher/).
**Ressource** : [Guide EFF Fingerprinting](https://ssd.eff.org/module/categories-fingerprinting).

### **Exercice 2 : Création d'un Sock Puppet Anonyme (Niveau Débutant) 👤**
**Objectif** : Générer une identité fictive sans traces.
1. Utilisez [Fake Name Generator](https://www.fakenamegenerator.com/) pour nom, bio, adresse.
2. Créez un email via [Temp Mail](https://temp-mail.org/).
3. Générez une photo avec [ThisPersonDoesNotExist](https://thispersondoesnotexist.com/).
4. Créez un compte Twitter/Reddit avec VPN activé (ex. Mullvad).
5. Postez un tweet neutre et vérifiez via [Sherlock](https://github.com/sherlock-project/sherlock) si liens vers votre identité réelle.
**Vérification** : Recherchez l'email/nom sur Google – zéro résultats liés à vous.
**Ressource** : [Sock Puppet Guide](https://www.bellingcat.com/resources/how-tos/2021/01/11/osint-opsec-guide/).

### **Exercice 3 : Nettoyage de Métadonnées d'une Image (Niveau Intermédiaire) 📸**
**Objectif** : Éliminer les traces EXIF pour éviter géolocalisation.
1. Téléchargez une photo personnelle (ex. selfie).
2. Vérifiez métadonnées avec [Jeffrey's Image Metadata Viewer](https://exif.regex.info/exif.cgi).
3. Utilisez [ExifTool](https://exiftool.org/) (installez via commande) : `exiftool -all= image.jpg`.
4. Re-testez : Vérifiez localisation/timestamp supprimés.
5. Uploadez anonymement sur Imgur et vérifiez via [InVID Verification](https://www.invid-project.eu/tools-and-services/invid-verification/).
**Vérification** : Aucune info sensible visible.
**Ressource** : [ExifTool Tutorial](https://www.sans.org/blog/metadata-extraction-with-exiftool/).

### **Exercice 4 : Simulation d'Enquête Anonyme avec VM (Niveau Intermédiaire) 💻**
**Objectif** : Isoler une recherche OSINT.
1. Installez [VirtualBox](https://www.virtualbox.org/) et créez une VM Ubuntu.
2. Installez Tor Browser dans la VM.
3. Recherchez un sujet sensible (ex. "dark web forums") via Tor.
4. Notez résultats dans un fichier encrypté avec [VeraCrypt](https://www.veracrypt.fr/).
5. Fermez VM et vérifiez host machine (pas de logs).
**Vérification** : Testez IP sur [ipleak.net](https://ipleak.net/) avant/après – aucune fuite.
**Ressource** : [TraceLabs VM Setup](https://www.tracelabs.org/initiatives/osint-vm).

### **Exercice 5 : Modèle de Menace Personnel (Niveau Avancé) 📊**
**Objectif** : Cartographier vos risques.
1. Listez vos actifs (appareils, comptes, habitudes) dans un doc encrypté.
2. Identifiez menaces (ex. "collègue curieux" ou "hacker ciblé").
3. Scorez risques (1-10) avec [ce matrice](https://www.riskwatch.com/risk-matrix).
4. Priorisez 3 contre-mesures (ex. 2FA partout, VPN quotidien).
5. Revoyez dans 1 mois.
**Vérification** : Document mis à jour, actions implémentées.
**Ressource** : [MITRE Threat Modeling](https://attack.mitre.org/resources/threat-modeling/).

**Conseil Général** : Faites ces exercices en solo, puis partagez anonymement sur [OSINTFR](https://discord.com/invite/dWY9sWFKYD) pour feedback. Temps total : 3-5h.

---

## 🎓 **8. Ressources Avancées et Formation**
- **Guides Gratuits** : [EFF Surveillance Self-Defense](https://ssd.eff.org/) | [Bellingcat OPSEC](https://www.bellingcat.com/resources/how-tos/2021/01/11/osint-opsec-guide/).
- **Cours** : [SANS OPSEC](https://www.sans.org/cyber-security-courses/practical-open-source-intelligence/) (payant).
- **Communautés** : Rejoignez [OSINTFR Discord](https://discord.com/invite/dWY9sWFKYD) pour tips.
- **Outils Gratuits** : [OPSEC Cheat Sheet](https://github.com/Jieyab89/OSINT-Cheat-sheet/wiki/OSINT-for-OPSEC-%28Operational-security%29).

---

## 📅 **Conclusion et Mise à Jour**
L'OPSEC est une **discipline vivante** : testez mensuellement votre setup avec [ce checklist](https://www.tracelabs.org/initiatives/osint-vm). En novembre 2025, avec l'essor de l'IA (fingerprinting avancé), priorisez l'apprentissage continu.

**Restez vigilant** 🕵️‍♂️ : Votre sécurité dépend de votre paranoïa saine. Contributions bienvenues ! [Forkez ce repo](https://github.com/votre-repo) pour updates.

> 📌 *Dernière mise à jour : 08 novembre 2025*  
> _Sources : EFF, Dutch OSINT Guy, et plus._
