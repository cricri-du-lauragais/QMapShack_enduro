**dans OpenStreetMap les sentiers (path pour Osm) peuvent être décrit par au moins 2 échelles de difficulté**
> - VTT sur 6 niveaux, c'est le tag **mtb:scale** **[détaillé ici dans le wiki Osm](https://wiki.openstreetmap.org/wiki/FR:Key:mtb:scale)**
>
> - pédestre (randonnée), c'est le tag **sac_scale** **[détaillé ici dans le wiki Osm](https://wiki.openstreetmap.org/wiki/FR:Key:sac_scale)**

# sentier "facile" points verts
| facile |
| :-------------: |
|![facile](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/facile.png)|

ce sont les tags suivants qui vont être utilisés par les routages
> - "mtb:scale" "0"

# sentiers "technique" points oranges
| technique |
| :-------------: |
|![technique](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/technique.png)|

> - "mtb:scale" "1"
> - "sac_scale" "hiking"

# sentiers "difficiles" points rouges 
(peut nécessiter de pousser le moto ...)
| difficile |
| :-------------: |
|![difficile](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/difficile.png)|

> - "mtb:scale" "2"
> - "mtb:scale" "3"
> - "sac_scale" "mountain_hiking"

# sentiers "impassables" points noirs
| infranchissable |
| :-------------: |
|![impassable](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/impassable.png)|

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

| pente > 60° |
| :-------------: |
|![grimpette](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/grimpette.png)|

> mtb:scale:uphill=5


