# Première installation linux de ma vie - Dell Precision M4800

Je vais installer un fichier ISO de Kali Linux sur un Dell Precision M4800.

Ce modèle est une station de travail portable sortie vers 2013–2014. Il est équipé d’un processeur Intel Core i7 de 4ᵉ génération, avec 4 cœurs (et parfois 8 threads), ce qui est largement suffisant pour des tâches avancées comme la virtualisation, la cybersécurité ou le développement.

Je vais commencer par télécharger Rufus. C’est un petit logiciel sur mon hp avec mon Windows qui permet de transformer un fichier ISO en clé USB bootable. Grâce à ça, je pourrai démarrer le Dell directement depuis la clé USB pour installer le système.

Un fichier ISO, c’est comme une image complète d’un disque (DVD). Il contient tout le système d’exploitation : fichiers, dossiers, programmes et instructions nécessaires pour démarrer l’ordinateur.

L’ISO que je vais utiliser sera Kali Linux.

## Pourquoi Kali Linux ?

Le Dell Precision M4800 est assez puissant : 16 Go de RAM + Intel Core i7 de 4ᵉ génération (Haswell) + fréquence entre 2.4 et 3.8 GHz. Il peut donc faire tourner Kali sans problème.

Kali Linux est une distribution basée sur Debian spécialement conçue pour la cybersécurité, les tests d’intrusion (pentesting) et l’analyse réseau. Elle intègre directement de nombreux outils professionnels utilisés pour tester la sécurité des systèmes et des réseaux.

Le M4800 avec Kali sera fluide et permettra d’utiliser plusieurs outils en même temps, voire des machines virtuelles, sans ralentissement.

Ça va surtout me permettre de découvrir ce type de système d’exploitation et de commencer à apprendre le monde du “hack”.

## 1) Première tentative : “j’installe normalement”

J’ai téléchargé l’ISO de Kali et je l’ai mise sur ma clé USB avec Rufus. Je démarre Windows, je rentre dans le BIOS et je lance l’installation. Tout a l’air carré.

Sauf qu’au moment où l’installateur veut télécharger des paquets (des fichiers supplémentaires pendant l’installation), ça bloque -_-. Ça n’avance plus, ou alors j’ai des erreurs, et je ne comprends pas pourquoi.

Je me dis que j’ai peut-être téléchargé la mauvaise ISO : une version “online” au lieu d’une version “offline”.

## 2) Deuxième tentative : “j’ai dû prendre la mauvaise ISO”

Je retélécharge donc cette fois-ci le bon ISO et je refais une clé USB avec Rufus. Je parle avec OpenAI ChatGPT au cas où, et il me dit de refaire exactement pareil qu’avant… mais je reste persuadé que le problème vient de l’ISO.

Je relance l’installation… et pareil : dès que j’arrive à l’étape où il veut récupérer certains paquets, j’ai une erreur liée au Wi-Fi.

Ça commence sérieusement à me saouler, mais au moins cette fois-ci je sais que la clé USB est correcte.

Erreur de ma part

J’ai cru que c’était forcément “la mauvaise ISO”, alors qu’en réalité, même avec une ISO offline, certaines étapes peuvent quand même demander une connexion réseau selon les options choisies pendant l’installation.

## 3) J’allège tout, ça va forcément passer

Je refais une installation en essayant d’être plus minimaliste. Je décoche plusieurs options, j’essaye de simplifier au maximum.

Mais malgré ça, ça ne fonctionne toujours pas.

Je commence même à me demander si je n’ai pas cassé le PC…

Je cherche alors des informations sur le modèle de mon ordinateur et je vois sur plusieurs forums que certains utilisateurs avaient réussi à installer d’autres systèmes d’exploitation sans problème, mais galéraient avec Kali Linux.

Encore une erreur de ma part

Le vrai problème venait toujours du Wi-Fi.

## 4) Ok… je vais forcer l’installation

Depuis le début, j’avais deux choix : configurer le Wi-Fi automatiquement ou manuellement.

En automatique, ça plantait.
En manuel, aucun réseau Wi-Fi n’apparaissait.

Après 3 clopes et 2 cafés, je me rappelle soudainement que le M4800 possède un port Ethernet.

Je branche donc un câble réseau pour avoir Internet directement en filaire. Et là, le problème de connexion est enfin réglé.

Je décide alors de relancer une dernière fois l’installation, mais cette fois en forçant une installation ultra minimale.

Tout ce qui était coché, je l’ai décoché.

Et là enfin… ça passe.

L’installation du système démarre correctement.

Une fois terminée, Kali démarre. Je me connecte et je vois le message “minimal installation”, mais au moins j’ai enfin un Kali fonctionnel.

Le plus drôle, c’est que j’avais littéralement le strict minimum du système : écran presque entièrement noir avec juste mon nom d’administrateur en bleu… exactement comme les “hackers” dans les films.

Je reparle ensuite avec ChatGPT pour qu’il me donne les bonnes commandes afin d’installer l’environnement de bureau et certaines applications manquantes de Kali. En gros, je téléchargeais maintenant tout ce que je n’avais pas pu installer auparavant.

Et honnêtement, cette fois-ci, mis à part le temps d’attente, tout s’est très bien passé. Une fois terminé, je redémarre le PC… et là j’avais enfin un vrai Kali Linux fonctionnel.

## 5) W.I.F.I

Par contre, j’avais toujours un problème avec le Wi-Fi.

La carte réseau apparaissait comme “hard-blocked”. J’essaye donc plusieurs commandes avec nmcli, j’installe des paquets, des pilotes… mais rien ne fonctionne.

Je reparle avec ChatGPT, et il me dit que Kali avait déjà tous les paquets nécessaires et que le problème venait probablement d’autre chose… peut-être du BIOS.

Je redémarre donc le PC, j’appuie sur F2 et je vérifie tous les paramètres réseau dans le BIOS : tout était parfaitement configuré.
Je continue à chercher sur des forums, ChatGPT me propose même de désinstaller certains paquets… bref, c’était le bordel.

Et là… je me rappelle qu’hier, avant tout ça, j’avais ouvert le PC pour nettoyer la poussière.
Sur le côté du Dell Precision M4800, il y a un petit interrupteur physique pour activer ou désactiver le Wi-Fi.
Pendant le nettoyage, je l’avais touché sans faire attention.
Depuis le début… le Wi-Fi était simplement désactivé physiquement.

Voilà ma misérable vie.
Dans tous les cas, même si j’avais réussi à régler le problème du Wi-Fi plus tôt, j’aurais quand même dû forcer l’installation minimale.

Mais bon… maintenant j’ai un Dell avec Kali Linux.



https://github.com/user-attachments/assets/618a5057-7bef-42fe-beaa-caee55e85979

<img width="1206" height="2103" alt="IMG_5765" src="https://github.com/user-attachments/assets/b5cb8f95-e8f7-40d3-b61f-33c299abca78" />


