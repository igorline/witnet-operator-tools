# WitStats

## Existing EthStats

In the same way than https://ethstats.io/ for Ethereum we want a network dashboard for Witnet.

As you can see on [Medium][ethstats-guide] the architecture is composed of the server app, the monitoring dashboard, and the client app that serves as the glue between a blockchain node and the server :

![Architecture of EthStats](https://github.com/witnet/witnet-operator-tools/raw/witstats-first/witstats/images/architecture.png)

* the monitoring dashboard is connected by WebSocket to the server app

* the server app provides the API to the monitoring dashboard and the client app

* the client app requests the API of the blockchain node to get monitoring data and send them to the server app

The client app is opensourced on [GitHub][ethstats-cli]

The server app is opensourced on [GitHub][ethstats-server]

The monitoring dashboard is opensourced on [GitHub][ethstats-dashboard]

## Existing Witnet node status

To cover our [wishlist](WishList.md) we first need to :

* check what is already available in Witnet Wallet Server to adapt EthStats client app into WitStats client app by modifying the API requests sent to the blockchain node to get monitoring data

* select first the monitoring data which are already sent by the client app to the server app

* make work a first version of the dashboard with this first monitoring data

[ethstats-guide]: https://medium.com/alethio/a-guide-to-deploying-alethios-free-open-source-products-18216617722e
[ethstats-cli]: https://github.com/Alethio/ethstats-cli
[ethstats-server]: https://github.com/Alethio/ethstats-network-server
[ethstats-dashboard]: https://github.com/Alethio/ethstats-network-dashboard
[wishlist]: https://github.com/witnet/witnet-operator-tools/raw/witstats-first/witstats/