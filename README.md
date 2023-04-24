# Casper Network Data Download Instructions
This repository provides instructions on how to download the Casper network data snapshot and place it in the appropriate directory. The snapshot was taken on 1034499.

## Requirements
The wget command-line utility must be installed on your system.
## Instructions
- Stop the node launcher by running the following command:

``` sudo systemctl stop casper-node-launcher ```

- Install zstd by running the following command:

``` sudo apt update && sudo apt install -y zstd ```

- Navigate to the directory where you want to download the snapshot.

``` cd /var/lib/casper/casper-node/casper  ```

- Run the following command to download the snapshot:

``` wget https://caspernetwork.live/db.tar.zst ```

``` zstd -d --long=31 db.tar.zst | sudo -u casper tar xv ```

- Start the node launcher again by running the following command:

``` sudo logrotate -f /etc/logrotate.d/casper-node ``` <br>
``` sudo systemctl start casper-node-launcher; sleep 2 ```

- Verify that the node is running properly by checking its status:

``` systemctl status casper-node-launcher ```

- The snapshot is now ready to use in the Casper network.

License
This repository is licensed under the MIT License. See LICENSE for more information.
