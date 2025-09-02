**dans OpenStreetMap**
un **chemin** peut être précisé de plusieurs manières
> - la "solidité" ou "**tracktype**" pour osm qui va de 1 à 5 **[voir le wiki OpenStreetMap ici](https://wiki.openstreetmap.org/wiki/FR:Key:tracktype)**<br> ce paramètre donne une idée générale du type de chemin, de la piste en concassé au chemin de champs avec juste le passage sur le terrain

> - son "état de surface" ou "**smoothness**" pour osm qui va de "excellent" à "impassable" pour un véhicule tout terrain dédié **[voir le wiki OpenStreetMap ici](https://wiki.openstreetmap.org/wiki/Key:smoothness)**

> - le matériau de sa surface "**surface**" pour osm qui va du goudron au sol nu en passant par de nombreux autres **[voir le wiki OpenStreetMap ici](https://wiki.openstreetmap.org/wiki/FR:Key:surface)**

# les 5 catégories de chemins représentés sur la carte et pris en compte pour le routage
qui vont de "**utilisable en moto lourde sans pneus vraiment adaptés**" à "**uniquement avec une moto relativement légère aux pneus adaptés**", la cinquième est juste les chemins génériques sans renseignements particulier dans OpenStreetMap.

:white_check_mark: **ces catégories sont utilisées pour représenter visuellement les chemins dans le style d'affichage
et dans chacun des 5 routages**

## chemins "piste" double pointillé
| piste |
| :-------------: |
![carrossable_1](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/piste.png) |

ce sont les tags **OpenStreetMap** que le routage "**moto lourde**" va utiliser en priorité pour vous faire passer
> - "surface" "unhewn_cobblestone"
> - "surface" "paved"
> - "surface" "paving_stones"
> - "surface" "compacted"
> - "surface" "metal"
> - "surface" "chipseal"
> - "surface" "wood"
> - "surface" "fine_gravel"
> - "surface" "asphalt"
> - "surface" "concrete"
> - "tracktype" "grade2"
> - "tracktype" "grade1"

## chemin "carrossable" marron 
| chemins carrossables |
| :-------------: |
|![carrossable_2](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/carrossable.png)|

chemins considérés comme praticables par le routage "**gros_trail**" avec une priorité plus faible
> - "surface" "rock"
> - "surface" "gravel"
> - "surface" "pebblestone"
> - "surface" "cobblestone"
> - "tracktype" "grade3"

## chemins "**selon météo**" en vert continu
| chemins terre |
| :-------------: |
|![chemin_terre](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/terre.png)|

chemins qui peuvent être compliqués à rouler avec une "**moto lourde ou en pneu routier**" quand les conditions météo sont mauvaises
> - "tracktype" "grade4"

## chemins "sol nu"" en vert pointillé
|chemins d'exploitation <br>ou sans précisions|
| :-------------: |
|![chemin_exploit](https://github.com/cricri-du-lauragais/QMapShack_enduro/blob/main/screenshots/legende/exploit.png)|

chemins sans apport de matériaux, tracés à même le sol

:warning: *selon la région et la période de l'année ils peuvent être plus ou moins praticables avec une moto lourde en pneus routiers.*
> - "ford" "yes"/>
> - "smoothness" "very_horrible"/>
> - "smoothness" "horrible"/>
> - "surface" "mud"
> - "surface" "grass"
> - "surface" "sand"
> - "surface" "dirt"
> - "surface" "earth"
> - "surface" "unpaved"
> - "surface" "ground"
> - "tracktype" "grade5"

## les chemins "non précisé"
|chemins d'exploitation <br>ou sans précisions| chemins d'exploitation nuit |
| :-------------: | :-------------: | 
|![chemin_exploit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/f5cd6505-8aee-4115-863e-1958a86ac67f)|![chemin_exploit_nuit](https://github.com/OsmAnd-Rendering/Motorcycle/assets/83398215/e2183c0d-f064-4e79-a928-f0f00988c2c3)|

ce sont les "track" OpenStreetMap qui n'ont aucun des tags précédents

:warning: *leur utilisation est la plus réduite possible avec le routage "**gros_trail**" pour des raisons de sécurité*

# routage
comment les routages des 3 "catégories" de motos utilisent ces classes de chemins
## routage gros_trail
- la première catégorie est privilégiée
- la seconde un petit peu moins
- la troisième est défavorisée
- les 2 dernières (dont les "sans précision") sont bannies (pas totalement, ça laisse une possibilité au moteur de calcul de trouver une alternative)

lorsque le switch "**si chemin sec**" est activé 
- il remonte la seconde catégorie au niveau de la première
- il remonte la troisième au niveau de la seconde

ce qui à pour résultat de proposer plus de chemins au moteur de routage
> malheureusement dans les régions avec peu de chemins renseignés dans Osm, la trace emprunte beaucoup de route, c'est inévitable pour rouler en sécurité, vous pouvez essayer le routage "**petit_trail**" qui est moins restrictif, à vos risques et périls.

## routage "**petit_trail**"
- par défaut le routage **petit_trail** n'applique aucune préférence aux chemins (hors sentiers)

il interdit comme le **gros_trail**
- "smoothness" "impassable"<i> réservé aux enduros</i>
- "highway" "path"<i> sentiers pour les enduros</i>
- "highway" "footway"<i> les chemins piéton</i>
- "highway" "cycleway"<i> les pistes cyclables</i>

- lorsque le switch "**tri les chemins**" est actif, le choix des chemins repose sur le même principe que pour le **gros_trail** avec des priorité plus permissives mais qui n'incite pas à prendre les "chemin non précisé" toujours pour des raisons de sécurité.

## routage "**enduro**"
- aucune préférence dans les chemins
- privilégie lorsqu'il en trouve les difficultés VTT "faciles" (mtb:scale 0 et 1)<br>
<i>points verts sur les sentiers</i>
- dissuade les difficultés VTT mtb:scale 2 et 3 et pédestre sac:scale<br>
<i>points rouges sur les sentiers</i>
- interdit les difficulté VTT et pédestre trop élevées pour une moto de 100 kg<br>
<i>points noirs sur les sentiers</i>
- prends tous les sentiers y compris footway sauf formellement indiqué "access=no ou private"
