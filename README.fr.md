# BoostPing

**Un outil gratuit qui adapte les paramètres réseau de Windows au jeu d'un seul bouton et rend les jeux en ligne plus réactifs.**

[English](README.md) · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [Español](README.es.md) · [Português (Brasil)](README.pt-BR.md) · Français

> Ce document est une traduction. En cas de différence, la [version coréenne](README.ko.md) fait foi.

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20(64--bit)-0078D4)
![License](https://img.shields.io/badge/license-Freeware-brightgreen)
[![Download](https://img.shields.io/badge/download-kilho.net-orange)](https://down.kilho.net/boostping?lang=fr)

![Écran de BoostPing](images/boostping-en.png)

## Présentation

Par défaut, Windows accumule brièvement les données réseau avant de les envoyer en lot. C'est efficace pour télécharger des fichiers ou naviguer sur le web, mais dans les jeux en ligne — où chaque frappe doit atteindre le serveur immédiatement — le jeu réagit d'autant plus tard.

BoostPing modifie cinq de ces paramètres pour les adapter au jeu. Appuyez sur **Lancer le boost** : il trouve le réseau par lequel vous êtes connecté à internet, applique les paramètres et reconnecte le réseau. Appuyez sur **Couper le boost** : il remet exactement les valeurs d'avant. Vous choisissez les éléments à modifier, et ceux que vous laissez décochés ne sont jamais touchés.

## Fonctionnalités

- **Un seul bouton** — Aucun réglage compliqué ; un appui sur Lancer le boost suffit.
- **Trouve automatiquement le réseau utilisé** — Choisit l'adaptateur réellement connecté à internet et affiche son nom et son IP en bas de la fenêtre. Les adaptateurs réseau virtuels sont ignorés.
- **Cinq éléments, appliqués à votre choix** — ACK immédiat, Aucun délai ACK, Désactiver l'algorithme de Nagle, Lever la limitation réseau, Priorité aux jeux.
- **Restauration exacte** — Mémorise les valeurs d'avant le boost et les remet quand vous le coupez. Les paramètres qui n'existaient pas sont supprimés, et les valeurs que vous aviez modifiées vous-même reviennent à ces valeurs.
- **Reste actif après fermeture** — Les paramètres sont appliqués à Windows : l'effet continue après la fermeture de la fenêtre ou un redémarrage. Relancé, il affiche l'état appliqué tel quel.
- **9 langues** — Coréen · Anglais · Japonais · Chinois · Russe · Italien · Français · Arabe · Espagnol. Suit la langue d'affichage de Windows.

## Téléchargement / Installation

| Type | Lien |
|---|---|
| Programme d'installation | [Télécharger](https://down.kilho.net/boostping?lang=fr) |
| Portable (ZIP) | [Télécharger](https://down.kilho.net/boostping?lang=fr&nosetup) |

La version installée se lance dès la fin de l'installation. Pour la version portable, décompressez le ZIP et lancez `BoostPing.exe`. Dans les deux cas, il demande les **droits d'administrateur**.

## Utilisation

### Premiers pas

1. Lancez BoostPing. Comme il modifie des paramètres de Windows, une fenêtre de confirmation des droits d'administrateur s'affiche : cliquez sur **Oui**.
2. Vérifiez que le nom et l'IP du réseau que vous utilisez apparaissent sur la ligne du bas. (p. ex. `Ethernet (Realtek PCIe GbE Family Controller) · 192.168.0.10`)
3. Pour choisir les éléments à modifier, cliquez sur l'**icône de réglages** en haut à droite pour ouvrir l'écran **TUNING**. Au départ, les cinq sont activés.
4. Cliquez sur **Lancer le boost**. L'état passe à **BOOST** et « Reconnexion du réseau… » s'affiche. À ce moment, internet se coupe brièvement puis se reconnecte.
5. Une fois internet revenu, l'état passe à **ON** avec « Optimisation appliquée ». Il ne reste qu'à lancer votre jeu.
6. Pour revenir à l'état d'origine, cliquez sur **Couper le boost**. Le réseau se reconnecte encore une fois et l'état revient à **READY**.

### Éléments de l'écran

**Écran principal**

| Élément | Description |
|---|---|
| Logo **BOOST//PING** | Ouvre la page de BoostPing |
| Icône de réglages (en haut à droite) | Ouvre l'écran TUNING |
| **STATUS** | **READY** = en attente, **BOOST** = application, **ON** = appliqué |
| 5 barres · **%d / 5 éléments** | Nombre d'éléments activés ; une barre par élément |
| **Lancer le boost** / **Couper le boost** | Appliquer / restaurer les paramètres d'origine |
| Ligne du bas | Nom · IP du réseau utilisé, version du programme |

**Écran TUNING** — Cliquez sur un élément pour l'activer ou le désactiver. Les changements sont enregistrés immédiatement.

| Élément | Effet |
|---|---|
| **ACK immédiat** | Envoie les accusés de réception sans les regrouper |
| **Aucun délai ACK** | Met le minuteur d'accusé différé à 0 |
| **Désactiver l'algorithme de Nagle** | Envoie les petits paquets sans les regrouper |
| **Lever la limitation réseau** | Lève la limite de transfert pendant la lecture multimédia |
| **Priorité aux jeux** | Ne réserve plus de temps CPU aux tâches de fond |

### Situations courantes

**Quand vos actions en jeu semblent arriver avec un temps de retard**
Cliquez sur Lancer le boost dans BoostPing avant de lancer le jeu. C'est dans les jeux en ligne qui échangent souvent de petites données que l'effet se ressent le plus. Comme internet se reconnecte brièvement lors de l'application, mieux vaut l'activer **avant** d'entrer dans une partie.

**Quand vous voulez l'activer une fois pour toutes**
Après avoir activé le boost, vous pouvez fermer la fenêtre de BoostPing. Les paramètres restent dans Windows et demeurent appliqués même après un redémarrage. En relançant BoostPing, l'état s'affiche **ON**.

**Quand vous jouez avec de la musique ou un stream en fond**
Windows limite les transferts réseau pendant la lecture multimédia. Avec **Lever la limitation réseau** activé, cette limite ne s'applique pas, même avec de la musique ou une vidéo en cours.

**Quand vous ne voulez que certains éléments**
Boost coupé (READY), allez dans l'icône de réglages → écran TUNING et cliquez sur les éléments dont vous ne voulez pas pour les désactiver. Les barres et **%d / 5 éléments** de l'écran principal changent aussitôt. Les éléments désactivés ne sont jamais touchés, ni au lancement ni à la coupure.

**Quand vous voulez changer d'éléments boost activé**
Tant que le boost est activé, l'écran TUNING est verrouillé et affiche « Modifiable après avoir coupé le boost. ». Procédez dans cet ordre : Couper le boost → changer les éléments → Lancer le boost.

**Quand vous voulez comparer la différence**
Jouez une partie dans l'état d'origine avec Couper le boost, puis une avec Lancer le boost. La coupure restaure exactement les valeurs d'avant, vous pouvez donc alterner et comparer autant de fois que vous le souhaitez.

**Quand vous aviez déjà modifié vous-même les paramètres réseau**
BoostPing mémorise les valeurs actuelles avant de commencer. Quand vous le coupez, il revient **aux valeurs que vous aviez réglées**, et non aux valeurs par défaut de Windows.

**Quand vous alternez entre Wi‑Fi et filaire sur un portable**
Le boost s'applique au réseau utilisé au moment où vous l'avez lancé. Si vous avez changé de réseau, cliquez sur Couper le boost, puis fermez BoostPing et relancez-le. Quand le nouveau réseau apparaît sur la ligne du bas, cliquez sur Lancer le boost. À la coupure, il restaure toujours le réseau auquel il a été appliqué au départ, même si vous en avez changé depuis.

**Quand vous avez fini de jouer et voulez tout remettre comme avant**
Lancez BoostPing et cliquez sur Couper le boost. Avant de désinstaller le programme, coupez aussi le boost en premier.

**Quand vous ne voyez pas la fenêtre de BoostPing**
Un seul BoostPing peut tourner à la fois. Le relancer alors qu'il est déjà ouvert ramène la fenêtre existante au premier plan (et la restaure si elle était réduite).

## Configuration

Se modifie dans l'écran TUNING et s'enregistre immédiatement. Les réglages sont conservés lors des mises à jour.

| Élément | Valeur par défaut |
|---|---|
| ACK immédiat | Activé |
| Aucun délai ACK | Activé |
| Désactiver l'algorithme de Nagle | Activé |
| Lever la limitation réseau | Activé |
| Priorité aux jeux | Activé |

La langue de l'interface suit la langue d'affichage de Windows (coréen · anglais · japonais · chinois · russe · italien · français · arabe · espagnol ; anglais sinon). L'arabe s'affiche de droite à gauche.

## Configuration requise

- Windows 10 · Windows 11 (64 bits)
- Droits d'administrateur — comme il modifie les paramètres réseau de Windows, une fenêtre de confirmation des droits s'affiche au lancement.
- Aucun runtime supplémentaire n'est nécessaire.

## Mises à jour

BoostPing ne se met **pas** à jour tout seul. Au lancement, il vérifie si une nouvelle version existe et affiche un avis ; en appuyant sur **Oui**, la page de téléchargement s'ouvre et le programme se ferme. Les nouvelles versions sont publiées manuellement après vérification interne et annoncées sur la [page BoostPing](https://kilho.net/boostping). Consultez l'[avis sur la politique de mise à jour](https://en.kilho.net/archives/notice/2940).

## Licence

BoostPing est un **freeware**. Vous pouvez l'utiliser gratuitement partout — au travail, à la maison, dans les administrations ou à l'école — et le redistribuer librement.

## Liens

- Site web : <https://kilho.net/boostping>
- Forum : <https://kilho.top/forum/qna>
- X (Twitter) : <https://www.twitter.com/kilhonet>

© KILHO.NET
