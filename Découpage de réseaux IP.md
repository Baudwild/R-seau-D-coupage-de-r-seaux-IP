## Le réseau 172.16.1.0/24 en symétrique :

- On le découpe en 4 sous-réseaux.
- Le nombre supérieur à 50 est ici 64 dans le tableau de puissance.
- le nombre d'adresses IP disponible au total, soit 64.
- Donc 2 puissance 6, soit 64, moins les 2 adresses (réseau et diffusion), donne un total de 62.
- On a donc 62 adresses IP disponibles sur chaque sous-réseaux.
- Le CIDR : 32 - 6 = /26.

#### on a donc les 4 sous-réseaux suivants :

##### Sous-réseau 1 : Le Pôle informatique 
- Adresse de réseau : 172.16.1.0/26
- Début de plage IP disponible : 172.16.1.1
- Fin de plage IP disponible :172.16.1.62
- Adresse de broadcast : 172.16.1.63

##### Sous-réseau 2 : Le Pôle développement 
- Adresse de réseau : 172.16.1.64/26
- Début de plage IP disponible : 172.16.1.65
- Fin de plage IP disponible : 172.16.1.126
- Adresse de broadcast : 172.16.1.127

##### Sous-réseau 3 : Le Pôle Administratif 
- Adresse de réseau : 172.16.1.128/26
- Début de plage IP disponible : 172.16.1.129
- Fin de plage IP disponible : 172.16.1.190
- Adresse de broadcast : 172.16.1.191

##### Sous-réseau 4 : Le Pôle Technicien 
- Adresse de réseau : 172.16.1.192/26
- Début de plage IP disponible : 172.16.1.193
- Fin de plage IP disponible : 172.16.1.254
- Adresse de broadcast : 172.16.1.255


## Le réseau 172.16.1.0/24 en asymétrique :

#### On cherche en premier le nombre d'hôte pour chaque département :

- Le Pôle informatique (50 équipements) = 2^6-2 = 64-2 = 62
- Le Pôle développement (12 équipements) = 2^4-2 = 16-2 = 14
- Le Pôle Administratif (20 équipements) = 2^5-2 = 32-2 = 30
- Le Pôle Technicien (15 équipements) = 2^5-2 = 32-2 = 30 

#### Les sous-réseaux seront dans cette ordre :

Le Pôle informatique (62 hôtes)
Le Pôle Administratif (30 hôtes)
Le Pôle Technicien (30 hôtes)
Le Pôle développement (14 hôtes)

#### on a donc les 4 sous-réseaux suivants :

##### Sous-réseau 1 : Le Pôle informatique 
- Adresse de réseau : 172.16.1.0/26 (CIDR : 32 - 6 = /26)
- Début de plage IP disponible : 172.16.1.1
- Fin de plage IP disponible :172.16.1.62
- Adresse de broadcast : 172.16.1.63

##### Sous-réseau 2 : Le Pôle Administratif 
- Adresse de réseau : 172.16.1.64/27 (CIDR : 32 - 5 = /27)
- Début de plage IP disponible : 172.16.1.65 
- Fin de plage IP disponible : 172.16.1.94
- Adresse de broadcast : 172.16.1.95

##### Sous-réseau 3 : Le Pôle Technicien 
- Adresse de réseau : 172.16.1.96/27 (CIDR : 32 - 5 = /27)
- Début de plage IP disponible : 172.16.1.97
- Fin de plage IP disponible : 172.16.1.126
- Adresse de broadcast : 172.16.1.127

##### Sous-réseau 4 : Le Pôle développement 
- Adresse de réseau : 172.16.1.128/28 (CIDR : 32 - 4 = /28)
- Début de plage IP disponible : 172.16.1.129
- Fin de plage IP disponible : 172.16.1.142
- Adresse de broadcast : 172.16.1.143
