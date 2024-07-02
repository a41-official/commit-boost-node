# commit-boost-node

Commit Boost Client Deployment

## Init

Download Network Configs to `network-configs/` from Repositories in [Commit-Boost Organization](https://github.com/Commit-Boost)

### Geth

```shell
docker run --rm -v $PWD/network-configs/genesis.json:/network-configs/genesis.json -v $PWD/data/geth:/data/geth/execution-data ethereum/client-go init --datadir=/data/geth/execution-data --state.scheme=hash /network-configs/genesis.json
```

## Deploy

```shell
cp .env.sample .env
docker compose up -d
```
