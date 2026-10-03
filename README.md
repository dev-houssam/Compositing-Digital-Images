# Compositing-Digital-Images

Compositing Digital Images : C'est notamment le papier qui formalise l'algèbre de Porter-Duff pour combiner des images, avec le concept de canal alpha pour représenter la couverture/opacité d'un pixel

Dans le contexte d'optimisation extreme.

Recherches : 
Lien (Point d'entrée) : https://www.emaxilde.net/talks/bit-twiddling-duff-s-device-les-optimisations-extremes-de-code/#/5/2/5

Lien : https://dl.acm.org/doi/epdf/10.1145/964965.808606

---

# Compositing Digital Images

**Compositing Digital Images** est un travail de Thomas Porter et Tom Duff publié en 1984. Il a posé les bases d'une manière standard de **combiner plusieurs images numériques entre elles**.

L'idée principale est de pouvoir prendre une image **source**, une image **de fond** et des informations de transparence (**alpha**) pour calculer précisément le résultat :

```text
        Image A
      ┌─────────┐
      │  🌳     │
      │    A    │
      └────┬────┘
           │
           ▼
      Compositing
           │
           ▼
      ┌─────────┐
      │ 🌳 + 🏠 │
      │  résultat│
      └─────────┘
```

Le papier introduit notamment les opérations **Porter-Duff** (`over`, `in`, `out`, `atop`, `xor`, etc.), qui permettent de définir mathématiquement comment les pixels d'une image doivent être combinés avec ceux d'une autre.

## Ce que cela a permis

Ces principes sont devenus une base du **compositing 2D** utilisé pour :

* 🖼️ superposer des images et des calques ;
* 🎨 gérer la transparence avec le **canal alpha** ;
* 🎬 composer des scènes et des effets visuels ;
* 🪟 afficher des interfaces avec des éléments transparents ;
* ✨ créer des effets et des compositions graphiques ;
* 🧩 construire les systèmes modernes de **calques** dans les logiciels graphiques.

En pratique, lorsqu'un logiciel permet de dire :

> « Place cette image transparente par-dessus celle-ci »

il utilise une forme de cette logique de **compositing**.

**Porter-Duff a donc fourni une manière formelle de décrire comment des images numériques peuvent être combinées pixel par pixel.**



