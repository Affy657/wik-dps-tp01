# WIK-DPS-TP01 
Ce projet est une API Rust simple qui retourne les headers d'une requête HTTP GET lorsqu'une requête est effectuée sur /ping.

## Installation et mise en place
1. **Clonez le dépôt:**

        git clone https://path-to-repository/WIK-DPS-TP01.git

2. **Accédez au répertoire du projet:**

        cd WIK-DPS-TP01

3. **Compilez le projet:**

        cargo build --release

## Exécution
**Exécutez le serveur avec la commande suivante:**


    PING_LISTEN_PORT=<port> cargo run --release

Remplacez `<port>` par le numéro de port sur lequel vous souhaitez que le serveur écoute. Si vous ne spécifiez pas PING_LISTEN_PORT, le serveur écoutera sur le port 7878 par défaut.

## Exemples d'utilisation
**Pour obtenir les headers de la requête:**


    $ curl 127.0.0.1:7878/ping
    > {"User-Agent":"curl/7.78.0","Host":"127.0.0.1:7878","Accept":"*/*"}

**Pour une requête autre que GET sur /ping:**

    $ curl -X POST 127.0.0.1:7878/ping
    > (Réponse vide avec code 404)