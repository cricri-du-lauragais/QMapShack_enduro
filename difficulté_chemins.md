**dans OpenStreetMap les sentiers (path pour Osm) peuvent être décrit par au moins 2 échelles de difficulté**
> - VTT sur 6 niveaux, c'est le tag **mtb:scale** **[détaillé ici dans le wiki Osm](https://wiki.openstreetmap.org/wiki/FR:Key:mtb:scale)**
>
> - pédestre (randonnée), c'est le tag **sac_scale** **[détaillé ici dans le wiki Osm](https://wiki.openstreetmap.org/wiki/FR:Key:sac_scale)**

# sentier "facile" points verts
pour une moto d'enduro ...
| facile | facile nuit |
| :-------------: | :-------------: | 
|![facile](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/d5aad369-dae3-447c-8620-a78afc0ac9da)|![facile_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/a1f8e361-bd4e-404e-b061-4933ccba4f73)|

ce sont les tags suivants qui vont être utilisés par les routages
> - "mtb:scale" "0"

# sentiers "technique" points oranges
| technique | technique nuit |
| :-------------: | :-------------: | 
|![technique](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/06c179fc-8409-40c5-bb39-17b22d31e528)|![technique_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/2c38ce54-ad75-415e-a726-b7d4e10d3c24)|

> - "mtb:scale" "1"
> - "sac_scale" "hiking"

# sentiers "difficiles" points rouges 
(peut nécessiter de pousser le moto ...)
| difficile | difficile nuit |
| :-------------: | :-------------: | 
|![difficile](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/3248e3a0-b165-412a-8dac-ba69b3baa0d4)|![difficile_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/c7923c45-c67d-4174-942e-10216f62569d)|

> - "mtb:scale" "2"
> - "mtb:scale" "3"
> - "sac_scale" "mountain_hiking"

# sentiers "impassables" points noirs (blanc en mode nuit)
| infranchissable | infranchissable nuit |
| :-------------: | :-------------: | 
|![impassable](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/d783f7b3-1db7-4e94-994f-fba57a67297a)|![impassable_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/8a42c82e-caed-4c0c-95a6-811edfd30aa9)|

> - "mtb:scale" "4"
> - "mtb:scale" "5"
> - "mtb:scale" "6"
> - "sac_scale" "demanding_mountain_hiking"
> - "sac_scale" "alpine_hiking"
> - "sac_scale" "demanding_alpine_hiking"
> - "sac_scale" "difficult_alpine_hiking"

# chemins
la même échelle s'applique aux chemins (track) mais d'une part ils sont rarement précisés car ça reste des chemins (dont la largeur permet de passer en "louvoyant" entre les obstacles) et d'autre part ils sont destinés à des engins motorisés (spécialisés parfois)

vous trouverez 
- quelques points **orange** pour un chemin dégradé 
> **smoothness=horrible**
- des points **rouges** pour un chemin très dégradé ou boueux (bourbier)
> **surface=mud**
> **smoothness=very_horrible**
- des points **noir** (blanc en mode nuit) pour un chemin détruit impassable par un 4 roues (ou plus)
> **smoothness=impassable**

# montée (affectueusement surnommée "grimpette")
- tant sur les chemins que les sentiers vous pouvez rencontrer de **GROS** points rouge qui marquent une pente > à 40%

| pente > 60° | pente > 60° nuit |
| :-------------: | :-------------: | 
|![grimpette](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/a475d3ea-a825-413a-9590-57cfc4105aca)|![grimpette_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/3e5ddca2-44fc-47cb-9016-7f0db7ac5cef)|

> mtb:scale:uphill=5
