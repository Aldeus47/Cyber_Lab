# Commandes Windows testé et leurs utilitées :

1.  ipconfig : Affiche les support de connection de la machine ainsi que les information relative aux connection
 [Ethernet]: Connection internet filaire
 [Wi-Fi]: connection internet sans fil
 [Bluetooth]: connection locale sans fil
    
     ex :
            Carte réseau sans fil Wi-Fi :
            Suffixe DNS propre à la connexion. . . : home
            Adresse IPv6. . . . . . . . . . . . . .: 2a01:cb05:92b1:9300:4e96:d6a8:1990:60bd
            Adresse IPv6 temporaire . . . . . . . .: 2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6
            Adresse IPv6 de liaison locale. . . . .: fe80::ea8b:8715:b02:c028%6
            Adresse IPv4. . . . . . . . . . . . . .: 192.168.1.14
         Masque de sous-réseau. . . . . . . . . : 255.255.255.0
         Passerelle par défaut. . . . . . . . . : fe80::3a06:e6ff:fe46:9290%6
         192.168.1.1

2.  ping : Teste l'état et la rapidité du réseaux internet ou local
 [réseaux_internet] : connextion à un site présent sur le web
 [réseaux_local] : connection à une machine connécté localement / à proximité
     ex : 
         Envoi d’une requête 'ping' sur google.com (2a00:1450:4007:80b::200e) avec 32 octets de données :
         Réponse de 2a00:1450:4007:80b::200e : temps=12 ms
         Réponse de 2a00:1450:4007:80b::200e : temps=14 ms
         Réponse de 2a00:1450:4007:80b::200e : temps=13 ms
         Réponse de 2a00:1450:4007:80b::200e : temps=13 ms

         Statistiques Ping pour 2a00:1450:4007:80b::200e:
         Paquets : envoyés = 4, reçus = 4, perdus = 0 (perte 0%),
         Durée approximative des boucles en millisecondes :
         Minimum = 12ms, Maximum = 14ms, Moyenne = 13ms

3.  netstat : Liste les connections actives de la machine
     ex :
         Connexions actives

         Proto  Adresse locale         Adresse distante       État
         TCP    192.168.1.14:53139     40.126.31.130:https    TIME_WAIT
         TCP    192.168.1.14:60087     lb-140-82-114-26-iad:https  ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:49432  [2603:1020:805:3::401]:https  ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:53144  [2620:1ec:bdf::42]:https  ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:55749  [2603:1020:805:3::401]:https  ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:59101  wa-in-f188:5228        ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:59125  [2602:f79a::1]:https   ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:59126  [2602:f79a::1]:https   ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:59457  [2603:1020:206:4::208]:https  ESTABLISHED
         TCP    [2a01:cb05:92b1:9300:b850:b3f8:96a3:6fb6]:63446  [2603:1020:1001:11::2]:https  ESTABLISHED

4.  tracert : Trace l'intineraire d'un pacquet jusqu'à sa destination :
 [intineraire] : Chemin emprinté (routeur / proxy...)
     ex :
         Détermination de l’itinéraire vers google.com (2a00:1450:4007:80e::200e)
         avec un maximum de 30 sauts :

         1     2 ms     2 ms     1 ms  livebox.home [2a01:cb05:92b1:9300:3a06:e6ff:fe46:9290]
         2     5 ms     5 ms     6 ms  2a01cb08a004020f0193025300770159.ipv6.abo.wanadoo.fr [2a01:cb08:a004:20f:193:253:77:159]
         3     *        *        *     Délai d’attente de la demande dépassé.
         4     *        *        *     Délai d’attente de la demande dépassé.
         5    15 ms    12 ms    12 ms  2001:4860:1:1::6d8
         6     *        *        *     Délai d’attente de la demande dépassé.
         7    13 ms    11 ms    12 ms  2001:4860:0:1::4222
         8    14 ms    12 ms    12 ms  2001:4860:0:1::1af7
         9    14 ms    12 ms    12 ms  par10s42-in-x0e.1e100.net [2a00:1450:4007:80e::200e]

         Itinéraire déterminé.