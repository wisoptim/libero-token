
# How to deploy #

## Prepare data ##
1. Get Binance API key. Need to register on https://bscscan.com/register
API key can be found there
2. Get private key for deployment
3. Rename file *.secrets.example.json* into *.secrets.json*
4. Put the keys into the *.secrets.json* file

## Deploy contract ##
1. Install packages
```shell
npm install
```
2. Deploy contract
- parameter *--network* can have bsctestnet or *bscmainnet*
```shell
npx hardhat run scripts/deploy.js --network bsctestnet
```
3. Verify the contract
- address will be in logs after deployment on the previous step
```shell
 npx hardhat verify --network bsctestnet  0x55c2ca72EBe5549193ECaFD22Fc73d9c763097aE
```