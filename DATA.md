# Documentation des données — Codes postaux Maroc

## Format du fichier

- **Fichier** : `codes_postaux_marocains.json`
- **Encodage** : UTF-8
- **Format** : JSON avec une clé racine `"Feuille 1"` contenant un tableau d’objets.

## Schéma d’un enregistrement

```json
{
  "VILLE": "RABAT",
  "QUARTIER": "QUARTIER HASSAN",
  "CODE POSTAL": "10020"
}
```

| Champ         | Type   | Description                                      |
|---------------|--------|--------------------------------------------------|
| `VILLE`       | string | Nom de la ville (ex. RABAT, CASABLANCA)          |
| `QUARTIER`    | string | Nom du quartier, secteur ou lieu-dit             |
| `CODE POSTAL` | string | Code postal à 5 chiffres (ex. 10000, 20000)      |

## Exemples d’entrées

```json
{
  "VILLE": "RABAT",
  "QUARTIER": "QUARTIER ROYAL",
  "CODE POSTAL": "10000"
}
```

```json
{
  "VILLE": "TIFLET",
  "QUARTIER": "HAY SALAM",
  "CODE POSTAL": "15400"
}
```

## Notes

- Un même code postal peut correspondre à plusieurs quartiers (d’une même ville ou de villes différentes).
- Les libellés sont en majuscules dans le jeu de données.
- Utiliser une comparaison insensible à la casse si besoin pour des recherches par ville ou quartier.
