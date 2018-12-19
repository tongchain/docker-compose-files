# docker-dev mode
```
docker-compose -f docker-compose-simple.yaml up
```
```
docker exec -it chaincode bash
go build -o receipt
CORE_CHAINCODE_LOGLEVEL=debug CORE_PEER_ADDRESS=peer:7052 CORE_CHAINCODE_ID_NAME=mycc:1.0 ./receipt
```

```
docker exec -it cli bash
peer chaincode install -n mycc -v 1.0 -p chaincodedev/chaincode
```
