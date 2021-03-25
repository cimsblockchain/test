# test
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
