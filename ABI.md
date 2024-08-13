# Application Binary Interface
Is a standard way to interact with contracts via RPC calls or contract interaction.]
## Base structure
```json
{
"abi":[
    {
      "inputs": [
       {
         "internalType": "",
         "name": "",
         "type": "",
         "indexed": false,
         "anonymous": false,
       },
       {
        "components": [
          {
            "internalType": "",
             "name": "",
             "type": ""
          }
        ]
         "indexed": false,
         "internalType": "",
         "name": "",
         "type": ""
       }
    ],
    "outputs": []
    }
  ]
}
```
**abi**: is the base property that holds the whole data, each object on it has information about: constructor, functions, events, errors.  
**abi.inputs**: holds information about parameters, theirs internalType, name and type.  
**abi.inputs.name**: holds information about name of error, function or event.  
**abi.inputs.type**: holds information about oject type that can be: constructor, function, event, error.  
**abi.inputs[0].internalType**: mostly is the same as type, but in case of structs we have information about the struct, the contract that represents it and struct name, ther components are similar to inputs/outputs objects.  
**abi.inputs[0].name**: holds information about the name of parameters of error, function or event, it could be about inputs or outputs.  
**abi.inputs[0].type**: holds information about parameters of error, function, events and are typefied as uint, int, string, bytes, address, tupple.  
**abi.inputs[0].indexed**: it allows to index by event information when getting data from blockchain.  
**abi.inputs[1].components**: holds information about each struct component with internalType, name and type inside.  
**abi.inputs[1][0].internalType**: holds information about struct component intertalType mostly same as type, only changing if it has a struct inside another struct.  
**abi.inputs[1][0].name**: holds information about struct component name.  
**abi.inputs[1][0].type**: holds information about struct component type as uint, int, string, bytes, address, tupple.  
**abi.inputs[1].indexed**: in case of a struct parameter be related of an event, and it allows to index by event information when getting data from blockchain.  
**abi.inputs[1].anonnymous**: is used on events and if they are, events can only be easy indexed when have its original abi.  
**abi.outputs**: holds information about return data, theirs internalType, name and type.  

## Objects sample

### Function
```json
{
  "inputs": [
    {
      "internalType": "uint256",
      "name": "userId",
      "type": "uint256"
    }
  ],
  "name": "getUser",
  "outputs": [
    {
      "components": [
        {
          "internalType": "uint256",
          "name": "createdAt",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "id",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "name",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "level",
          "type": "uint256"
        },
        {
          "internalType": "uint256",
          "name": "level",
          "type": "uint256"
        }
      ],
      "internalType": "struct BattleRoyal.user",
      "name": "",
      "type": "tuple"
    }
  ],
  "stateMutability": "view",
  "type": "function"
}
```
### Event
```json
{
  "anonymous": false,
  "inputs": [
    {
      "indexed": false,
      "internalType": "uint256",
      "name": "amount",
      "type": "uint256"
    },
    {
      "indexed": true,
      "internalType": "uint256",
      "name": "userId",
      "type": "uint256"
    },
    {
      "indexed": true,
      "internalType": "address",
      "name": "user",
      "type": "address"
    }
  ],
  "name": "PlayReward",
  "type": "event"
}
```
### Error
```json
{
  "inputs": [
    {
      "internalType": "uint256",
      "name": "timeTilOpen",
      "type": "uint256"
    },
    {
      "internalType": "address",
      "name": "user",
      "type": "address"
    }
  ],
  "name": "MarketClosed",
  "type": "error"
}
```
