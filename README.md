# Codes postaux Maroc

Dataset des codes postaux du Maroc (ville, quartier, code postal) au format JSON.

## Contenu

- **`codes_postaux_marocains.json`** — Liste des localités avec code postal (ville, quartier, code postal).

## Structure des données

Chaque entrée contient :

| Champ         | Description                    |
|---------------|--------------------------------|
| `VILLE`       | Nom de la ville                |
| `QUARTIER`    | Quartier ou secteur concerné   |
| `CODE POSTAL` | Code postal à 5 chiffres       |

Le fichier est organisé sous la clé `"Feuille 1"`, qui contient un tableau d’objets.

## Utilisation

### Charger le fichier (JavaScript / Node.js)

```javascript
const data = require('./codes_postaux_marocains.json');
const entries = data['Feuille 1'];

// Exemple : trouver les quartiers d'une ville
const rabat = entries.filter(e => e.VILLE === 'RABAT');
```

### Charger le fichier (Python)

```python
import json

with open('codes_postaux_marocains.json', 'r', encoding='utf-8') as f:
    data = json.load(f)

entries = data['Feuille 1']

# Exemple : rechercher par code postal
postal_10000 = [e for e in entries if e['CODE POSTAL'] == '10000']
```

### Exemples de requêtes

- **Par ville** : filtrer sur `VILLE` (ex. `RABAT`, `CASABLANCA`, `MARRAKECH`).
- **Par code postal** : filtrer sur `CODE POSTAL` (chaîne de 5 chiffres).
- **Par quartier** : filtrer sur `QUARTIER` (nom du quartier ou secteur).

## Licence

Vérifiez les conditions d’utilisation des données avant toute réutilisation ou diffusion.
