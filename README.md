# Hyperledger Evote API Only

The objective of this repository is to provide a API only version of the [evote sample](https://github.com/IBM/evote) to execute locally. This version won't have Vue.

Install VSCode with IBM Blockchain Platform extension:
- [VSCode version 1.39](https://code.visualstudio.com/updates/v1_39)
- [IBM Blockchain Platform Extension for VSCode](https://github.com/IBM-Blockchain/blockchain-vscode-extension)

Install Node 8.17.0:

```bash
  nvm install 8.17.0
  nvm use 8.17.0
```

Follow this [steps](https://github.com/IBM/evote/blob/master/docs/run-local.md) to Start the Fabric Runtime, Install/Instantiate Contract and Export Wallet.

Root Endpoint: `localhost:8081`

| Route | Method | Params
| ------------- | ------------- | ------------- |
| /getCurrentStanding  | GET  | |
| /queryAll  | GET  | |
| /queryWithQueryString  | POST  | {"selected":"voter"} |
| /queryByKey  | POST  | {"key":"V1"} |
| /validateVoter  | POST  | {	"voterId":"132" } |
| /registerVoter  | POST  | { "voterId":"132", "registrarId":"312", "firstName":"Fulano", "lastName":"Beltrano" }|
| /castBallot  | POST  | { "electionId":"n50d924785omxkhiofy9", "voterId":"132", "picked":"Democrat"}|
