à propos des calculs d'itinéraire avec **BRouter** et mes differents profiles
- ils respectent tous les interdictions qui figurent dans **OpenStreetMmap**, tant sur les chemins que sur les barrières (accès non, privé, sauf ayant droit, véhicules, motor véhicules, motorcycle, agricultural, forestier)
- ne prennent pas les voie cyclable ou piétonne
- les sens interdit, interdiction de tourner
- plus la moto est lourde et moins les chemins accidentés ou avec un gros relief, ou sans précisions dans openstreemap sont choisis

Chaque itinéraire ou trace proposée peut être forcée en ajoutant des points de passages même sur les interdictions (il faut beaucoup de point pour forcer une interdiction)

le "**dirtbike_big**" et le "**dirtbike_big_wet**" sont dédiés aux motos lourdes avec des pneus trop routiers et / ou des pratiquants sans trop de technique, les 2 sont les mêmes avec juste une option d'activée ou non (**QMapShack** ne gère pas encore les options comme la version web de **BRouter**)
ils prennent majoritairement des chemins empierrés solides, le wet est plus restrictif
- quelques chemins "inconnus" ou moins faciles peuvent être pris sur de courtes distances par le "**dirtbike_big**"

le "**dirtbike_light**" s'adresse aux motos "**trail**" légères ou aux pilotes de grosses avec de l'expérience et une moto équipée de bons pneus
- prend n'importe quel chemin hors interdiction 
- prend des sentiers (monotrace indépendamment de la légalité de l'accès !) uniquement s'ils sont notés "faciles" dans **OpenStreetMmap**

le "**dirtbike_enduro**" s'adresse aux motos d'enduro en restant restrictif sur les sentiers en fonction de leur notation ou du relief (indépendamment de la légalité de l'accès aux monotraces)

le "**dirtbike_enduro_hard**" comme son nom l'indique se permet de passer sur des sentiers avec une notation plus difficile et est plus permissif sur le relief 

note :
- peu importe que vous choisissiez trace ou itinéraire, vous pouvez convertir dans les 2 sens sans problème, la seule restriction à trace est qu'une fois créé vous ne pouvez pas modifier la totalité de la trace en changeant de profil contrairement à un itinéraire.
- une fois créé vous pouvez modifier en ajoutant des points de passage sans problème, vous aurez le recalcul en temps "presque réel" avec les caractéristiques du profile choisi.
- vous pouvez modifier pour ajouter des parties "hors piste" facilement
