# test
cp mychannel.block ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && cp mycc.tar.gz ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && cd ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && docker cp mychannel.block cli1:/opt/gopath/src/github.com/hyperledger/fabric/peer/ && docker cp mycc.tar.gz cli1:/opt/gopath/src/github.com/hyperledger/fabric/peer/ && docker exec -it cli1 bash && peer channel join -b mychannel.block && peer channel update -o orderer0.example.com:7050 -c mychannel -f ./channel-artifacts/Org2MSPanchors.tx --tls --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer0.example.com/msp/tlscacerts/tlsca.example.com-cert.pem && peer lifecycle chaincode install mycc.tar.gz && peer lifecycle chaincode approveformyorg --channelID mychannel --name mycc --version 1.0 --init-required --package-id mycc_1:87dd7f13892fb21800aaabcfd2499f553446bd5d26b079f2f939ab111a648b5c --sequence 1 --tls true --cafile /opt/gopath/src/github.com/hyperledger/fabric/peer/crypto/ordererOrganizations/example.com/orderers/orderer0.example.com/msp/tlscacerts/tlsca.example.com-cert.pem



cp docker-compose-up.yaml ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && cd ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && docker-compose -f docker-compose-up.yaml up -d



rm -r channel-artifacts && rm -r crypto-config && rm 配置文件.zip
cp 配置文件.zip ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && cd ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && unzip 配置文件.zip

mkdir ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10 && cp 配置文件.zip ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && cd ../go/src/github.com/hyperledger/fabric/scripts/fabric-samples/multiple-deployment10/ && unzip 配置文件.zip

sudo vim /etc/hosts

10.0.0.35 orderer0.example.com
10.0.0.35 orderer1.example.com
10.0.0.44 orderer2.example.com
10.0.0.45 orderer3.example.com
10.0.0.46 orderer4.example.com
10.0.0.47 orderer5.example.com
10.0.0.48 orderer6.example.com
10.0.0.49 orderer7.example.com
10.0.0.50 orderer8.example.com
10.0.0.51 orderer9.example.com
10.0.0.52 orderer10.example.com
10.0.0.35 peer0.org1.example.com
10.0.0.35 peer1.org1.example.com
10.0.0.44 peer0.org2.example.com
10.0.0.44 peer1.org2.example.com
10.0.0.45 peer0.org3.example.com
10.0.0.45 peer1.org3.example.com
10.0.0.46 peer0.org4.example.com
10.0.0.46 peer1.org4.example.com
10.0.0.47 peer0.org5.example.com
10.0.0.47 peer1.org5.example.com
10.0.0.48 peer0.org6.example.com
10.0.0.48 peer1.org6.example.com
10.0.0.49 peer0.org7.example.com
10.0.0.49 peer1.org7.example.com
10.0.0.50 peer0.org8.example.com
10.0.0.50 peer1.org8.example.com
10.0.0.51 peer0.org9.example.com
10.0.0.51 peer1.org9.example.com
10.0.0.52 peer0.org10.example.com
10.0.0.52 peer1.org10.example.com

service network-manager restart
