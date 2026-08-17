# LCSGameKit

## Le Jeu

**Tire avant que les charges syndic explosent !** est un shoot'em up humoristique pour iPhone et iPad dont l'action se déroule dans une copropriété.

Inspiré de Space Invaders, le joueur incarne un résident qui doit repousser les envahisseurs de chaque local du bâtiment — la cave, le garage, le jardin, la banque… — avant que les charges de copropriété n'atteignent des sommets. Neuf niveaux, chacun avec ses ennemis thématiques, sa musique et son bonus exclusif.

[:material-apple: Télécharger sur l'App Store](https://games.apple.com/fr/game/6770456492){ .md-button .md-button--primary }

---

**LCSGameKit** est le package Swift qui fournit l'intégralité du moteur de jeu de cette application.

## Ce que contient le package

| Module | Rôle |
|--------|------|
| `LCSMenuView` | Interface principale : navigation, menus, écran titre |
| `LCSGameView` | Intégration SwiftUI / SpriteKit |
| `GameScene` | Moteur de jeu (SpriteKit) |
| `LCSLevel` | Définition des 9 niveaux et de leurs thèmes visuels |
| `SoundManager` | Audio procédural et haptiques |
| `LCSGamepadManager` | Support manette MFi / DualSense |
| `HighScoreStore` | Meilleurs scores locaux |
| `StatsStore` | Statistiques de jeu persistantes |
| `GameCenterManager` | Classements et succès Game Center |
| `PurchaseStore` | Achat intégré (StoreKit 2) |

## Prérequis

- iOS 18.6+
- Swift 6.0
- Xcode 16+

## Démarrage rapide

```swift
import LCSGameKit
import SwiftUI

struct ContentView: View {
    var body: some View {
        LCSMenuView()
    }
}
```

Pour intégrer le jeu dans une application existante avec un bouton de retour :

```swift
LCSMenuView(onExitToNikolai: {
    // callback appelé quand l'utilisateur quitte vers l'app hôte
    dismiss()
})
```
