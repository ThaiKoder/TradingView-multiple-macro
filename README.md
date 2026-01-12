# Multiple Macro – TradingView (Pine Script v5)

## 📌 Description

**Multiple Macro** est un indicateur TradingView développé en **Pine Script v5** permettant de visualiser jusqu’à **22 macros temporelles** (London, New York, autres sessions) directement sur le graphique ou dans un **nouveau panneau**.

Chaque macro représente une **fenêtre horaire clé** (manipulation, expansion, reversal, spooling, etc.)



## 🎯 Fonctionnalités principales

* ✅ Jusqu’à **22 macros configurables**
* 🕒 Gestion précise des **sessions horaires (UTC-5 / New York)**
* 📈 Affichage :

  * **Sur le graphique (On Chart)** avec lignes verticales + labels
  * **Dans un nouveau panneau (New Pane)** avec boxes
* 🏷️ Labels dynamiques avec **nom + plage horaire**
* 🎨 Couleur personnalisable
* ➡️ Extension automatique des macros
* 🔔 Alertes quand une barre entre dans une macro
* 🧹 Nettoyage mémoire automatique (lignes / labels)



## 🧠 Logique de l’indicateur

* Chaque macro est définie par :

  * un **toggle ON/OFF**
  * un **titre**
  * une **session horaire**
* L’indicateur détecte :

  * l’entrée dans la macro
  * la sortie de la macro
* Il trace :

  * une ligne verticale au début et à la fin
  * une ligne horizontale de référence
  * un label centré sur la macro
* Le comportement est adapté :

  * aux **vendredis**
  * aux **cryptos vs marchés traditionnels**



## ⚙️ Paramètres

### 🔧 Settings

| Paramètre          | Description                  |
| ------------------ | ---------------------------- |
| Macro color        | Couleur des macros           |
| Macro mode         | `On Chart` ou `New Pane`     |
| Show Time          | Affiche l’heure sur le label |
| Extend Macro Lines | Prolonge les lignes          |

### 🕒 Macros

* Groupées par :

  * **London**
  * **New York**
  * **Autres**
* Chaque macro contient :

  * ✔️ Enable / Disable
  * ✏️ Titre
  * ⏰ Session horaire (format HHMM-HHMM)



## 🚨 Alertes

* Alerte déclenchée **à chaque barre** entrant dans une macro
* Exemple :

```pinescript
alert("Barre dans la macro", alert.freq_once_per_bar)
```

* `alertcondition()` inclus pour automatisation TradingView



## 🕰️ Timezone

* Les sessions sont calculées en **UTC-5 (New York)**
* Conversion automatique pour l’affichage



## 🧩 Cas d’usage

* Journées types London / NY
* Repérage de :

  * Manipulation
  * Expansion
  * Reversal
  * Spooling
  * Power Hours



## 📦 Installation

1. Ouvre **TradingView**
2. Pine Editor → Nouveau script
3. Colle le code
4. Sauvegarde & ajoute au graphique



## ⚠️ Notes

* Conçu pour les timeframes **intraday**
* Peut atteindre les limites TradingView si trop d’objets sont affichés
* Nettoyage mémoire intégré pour éviter les erreurs



## 🛠️ Développé avec

* Pine Script v5
* TradingView

