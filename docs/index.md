# LCSGameKit

**LCSGameKit** est un package Swift qui fournit l'intégralité du moteur de jeu pour l'application *Tire avant que les charges syndic explosent !* — un shoot'em up humoristique à thème de copropriété.

## À propos du jeu

Le joueur incarne un résident d'une copropriété et doit éliminer les envahisseurs de chaque local (cave, garage, jardin…) avant que les charges de copropriété n'explosent.  
Le principe est celui d'un Space Invaders revisité : vagues d'ennemis descendants, tir vers le haut, bonus à intercepter.

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
