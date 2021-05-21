[avalanche](../README.md) › [API-EVM](../modules/api_evm.md) › [EVMAPI](api_evm.evmapi.md)

# Class: EVMAPI

Class for interacting with a node's EVMAPI

**`remarks`** This extends the [JRPCAPI](common_jrpcapi.jrpcapi.md) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1.md#addapi) function to register this interface with Avalanche.

## Hierarchy

  ↳ [JRPCAPI](common_jrpcapi.jrpcapi.md)

  ↳ **EVMAPI**

## Index

### Constructors

* [constructor](api_evm.evmapi.md#constructor)

### Properties

* [AVAXAssetID](api_evm.evmapi.md#protected-avaxassetid)
* [baseurl](api_evm.evmapi.md#protected-baseurl)
* [blockchainAlias](api_evm.evmapi.md#protected-blockchainalias)
* [blockchainID](api_evm.evmapi.md#protected-blockchainid)
* [core](api_evm.evmapi.md#protected-core)
* [db](api_evm.evmapi.md#protected-db)
* [jrpcVersion](api_evm.evmapi.md#protected-jrpcversion)
* [rpcid](api_evm.evmapi.md#protected-rpcid)
* [txFee](api_evm.evmapi.md#protected-txfee)

### Methods

* [addressFromBuffer](api_evm.evmapi.md#addressfrombuffer)
* [buildExportTx](api_evm.evmapi.md#buildexporttx)
* [buildImportTx](api_evm.evmapi.md#buildimporttx)
* [callMethod](api_evm.evmapi.md#callmethod)
* [export](api_evm.evmapi.md#export)
* [exportAVAX](api_evm.evmapi.md#exportavax)
* [exportKey](api_evm.evmapi.md#exportkey)
* [getAVAXAssetID](api_evm.evmapi.md#getavaxassetid)
* [getAssetDescription](api_evm.evmapi.md#getassetdescription)
* [getBaseURL](api_evm.evmapi.md#getbaseurl)
* [getBlockchainAlias](api_evm.evmapi.md#getblockchainalias)
* [getBlockchainID](api_evm.evmapi.md#getblockchainid)
* [getDB](api_evm.evmapi.md#getdb)
* [getDefaultTxFee](api_evm.evmapi.md#getdefaulttxfee)
* [getRPCID](api_evm.evmapi.md#getrpcid)
* [getTxFee](api_evm.evmapi.md#gettxfee)
* [getUTXOs](api_evm.evmapi.md#getutxos)
* [import](api_evm.evmapi.md#import)
* [importAVAX](api_evm.evmapi.md#importavax)
* [importKey](api_evm.evmapi.md#importkey)
* [issueTx](api_evm.evmapi.md#issuetx)
* [keyChain](api_evm.evmapi.md#keychain)
* [parseAddress](api_evm.evmapi.md#parseaddress)
* [refreshBlockchainID](api_evm.evmapi.md#refreshblockchainid)
* [setAVAXAssetID](api_evm.evmapi.md#setavaxassetid)
* [setBaseURL](api_evm.evmapi.md#setbaseurl)
* [setBlockchainAlias](api_evm.evmapi.md#setblockchainalias)

## Constructors

###  constructor

\+ **new EVMAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1.md), `baseurl`: string, `blockchainID`: string): *[EVMAPI](api_evm.evmapi.md)*

*Overrides [JRPCAPI](common_jrpcapi.jrpcapi.md).[constructor](common_jrpcapi.jrpcapi.md#constructor)*

*Defined in [src/apis/evm/api.ts:669](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L669)*

This class should not be instantiated directly.
Instead use the [Avalanche.addAPI](avalanche.avalanche-1.md#addapi) method.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`core` | [AvalancheCore](avalanchecore.avalanchecore-1.md) | - | A reference to the Avalanche class |
`baseurl` | string | "/ext/bc/C/avax" | Defaults to the string "/ext/bc/C/avax" as the path to blockchain's baseurl |
`blockchainID` | string | "" | The Blockchain's ID. Defaults to an empty string: ''  |

**Returns:** *[EVMAPI](api_evm.evmapi.md)*

## Properties

### `Protected` AVAXAssetID

• **AVAXAssetID**: *Buffer* = undefined

*Defined in [src/apis/evm/api.ts:58](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L58)*

___

### `Protected` baseurl

• **baseurl**: *string*

*Inherited from [APIBase](common_apibase.apibase.md).[baseurl](common_apibase.apibase.md#protected-baseurl)*

*Defined in [src/common/apibase.ts:38](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L38)*

___

### `Protected` blockchainAlias

• **blockchainAlias**: *string* = undefined

*Defined in [src/apis/evm/api.ts:56](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L56)*

___

### `Protected` blockchainID

• **blockchainID**: *string* = ""

*Defined in [src/apis/evm/api.ts:54](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L54)*

___

### `Protected` core

• **core**: *[AvalancheCore](avalanchecore.avalanchecore-1.md)*

*Inherited from [APIBase](common_apibase.apibase.md).[core](common_apibase.apibase.md#protected-core)*

*Defined in [src/common/apibase.ts:36](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L36)*

___

### `Protected` db

• **db**: *StoreAPI*

*Inherited from [APIBase](common_apibase.apibase.md).[db](common_apibase.apibase.md#protected-db)*

*Defined in [src/common/apibase.ts:40](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L40)*

___

### `Protected` jrpcVersion

• **jrpcVersion**: *string* = "2.0"

*Inherited from [JRPCAPI](common_jrpcapi.jrpcapi.md).[jrpcVersion](common_jrpcapi.jrpcapi.md#protected-jrpcversion)*

*Defined in [src/common/jrpcapi.ts:17](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/jrpcapi.ts#L17)*

___

### `Protected` rpcid

• **rpcid**: *number* = 1

*Inherited from [JRPCAPI](common_jrpcapi.jrpcapi.md).[rpcid](common_jrpcapi.jrpcapi.md#protected-rpcid)*

*Defined in [src/common/jrpcapi.ts:19](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/jrpcapi.ts#L19)*

___

### `Protected` txFee

• **txFee**: *BN* = undefined

*Defined in [src/apis/evm/api.ts:60](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L60)*

## Methods

###  addressFromBuffer

▸ **addressFromBuffer**(`address`: Buffer): *string*

*Defined in [src/apis/evm/api.ts:134](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L134)*

**Parameters:**

Name | Type |
------ | ------ |
`address` | Buffer |

**Returns:** *string*

___

###  buildExportTx

▸ **buildExportTx**(`amount`: BN, `assetID`: Buffer | string, `destinationChain`: Buffer | string, `fromAddressHex`: string, `fromAddressBech`: string, `toAddresses`: string[], `nonce`: number, `locktime`: BN, `threshold`: number): *Promise‹[UnsignedTx](api_evm_transactions.unsignedtx.md)›*

*Defined in [src/apis/evm/api.ts:566](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L566)*

Helper function which creates an unsigned Export Tx. For more granular control, you may create your own
[UnsignedTx](api_avm_transactions.unsignedtx.md) manually (with their corresponding [TransferableInput](api_avm_inputs.transferableinput.md)s, [TransferableOutput](api_avm_outputs.transferableoutput.md)s).

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`amount` | BN | - | The amount being exported as a [BN](https://github.com/indutny/bn.js/) |
`assetID` | Buffer &#124; string | - | The asset id which is being sent |
`destinationChain` | Buffer &#124; string | - | The chainid for where the assets will be sent. |
`fromAddressHex` | string | - | - |
`fromAddressBech` | string | - | - |
`toAddresses` | string[] | - | The addresses to send the funds |
`nonce` | number | 0 | - |
`locktime` | BN | new BN(0) | Optional. The locktime field created in the resulting outputs |
`threshold` | number | 1 | Optional. The number of signatures required to spend the funds in the resultant UTXO  |

**Returns:** *Promise‹[UnsignedTx](api_evm_transactions.unsignedtx.md)›*

An unsigned transaction ([UnsignedTx](api_avm_transactions.unsignedtx.md)) which contains an [ExportTx](api_avm_exporttx.exporttx.md).

___

###  buildImportTx

▸ **buildImportTx**(`utxoset`: [UTXOSet](api_evm_utxos.utxoset.md), `toAddress`: string, `ownerAddresses`: string[], `sourceChain`: Buffer | string, `fromAddresses`: string[]): *Promise‹[UnsignedTx](api_evm_transactions.unsignedtx.md)›*

*Defined in [src/apis/evm/api.ts:506](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L506)*

Helper function which creates an unsigned Import Tx. For more granular control, you may create your own
[UnsignedTx](api_avm_transactions.unsignedtx.md) manually (with their corresponding [TransferableInput](api_avm_inputs.transferableinput.md)s, [TransferableOutput](api_avm_outputs.transferableoutput.md)s).

**`remarks`** 
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`utxoset` | [UTXOSet](api_evm_utxos.utxoset.md) | A set of UTXOs that the transaction is built on |
`toAddress` | string | The address to send the funds |
`ownerAddresses` | string[] | The addresses being used to import |
`sourceChain` | Buffer &#124; string | The chainid for where the import is coming from |
`fromAddresses` | string[] | The addresses being used to send the funds from the UTXOs provided  |

**Returns:** *Promise‹[UnsignedTx](api_evm_transactions.unsignedtx.md)›*

An unsigned transaction ([UnsignedTx](api_avm_transactions.unsignedtx.md)) which contains a [ImportTx](api_avm_importtx.importtx.md).

___

###  callMethod

▸ **callMethod**(`method`: string, `params?`: Array‹object› | object, `baseurl?`: string, `headers?`: object): *Promise‹[RequestResponseData](common_apibase.requestresponsedata.md)›*

*Inherited from [JRPCAPI](common_jrpcapi.jrpcapi.md).[callMethod](common_jrpcapi.jrpcapi.md#callmethod)*

*Defined in [src/common/jrpcapi.ts:21](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/jrpcapi.ts#L21)*

**Parameters:**

Name | Type |
------ | ------ |
`method` | string |
`params?` | Array‹object› &#124; object |
`baseurl?` | string |
`headers?` | object |

**Returns:** *Promise‹[RequestResponseData](common_apibase.requestresponsedata.md)›*

___

###  export

▸ **export**(`username`: string, `password`: string, `to`: string, `amount`: BN, `assetID`: string): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:239](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L239)*

Send ANT (Avalanche Native Token) assets including AVAX from the C-Chain to an account on the X-Chain.

After calling this method, you must call the X-Chain’s import method to complete the transfer.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the X-Chain account specified in `to` |
`password` | string | The password of the Keystore user |
`to` | string | The account on the X-Chain to send the AVAX to. |
`amount` | BN | Amount of asset to export as a [BN](https://github.com/indutny/bn.js/) |
`assetID` | string | The asset id which is being sent  |

**Returns:** *Promise‹string›*

String representing the transaction id

___

###  exportAVAX

▸ **exportAVAX**(`username`: string, `password`: string, `to`: string, `amount`: BN): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:274](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L274)*

Send AVAX from the C-Chain to an account on the X-Chain.

After calling this method, you must call the X-Chain’s importAVAX method to complete the transfer.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the X-Chain account specified in `to` |
`password` | string | The password of the Keystore user |
`to` | string | The account on the X-Chain to send the AVAX to. |
`amount` | BN | Amount of AVAX to export as a [BN](https://github.com/indutny/bn.js/)  |

**Returns:** *Promise‹string›*

String representing the transaction id

___

###  exportKey

▸ **exportKey**(`username`: string, `password`: string, `address`: string): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:474](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L474)*

Exports the private key for an address.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The name of the user with the private key |
`password` | string | The password used to decrypt the private key |
`address` | string | The address whose private key should be exported  |

**Returns:** *Promise‹string›*

Promise with the decrypted private key as store in the database

___

###  getAVAXAssetID

▸ **getAVAXAssetID**(`refresh`: boolean): *Promise‹Buffer›*

*Defined in [src/apis/evm/api.ts:183](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L183)*

Fetches the AVAX AssetID and returns it in a Promise.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`refresh` | boolean | false | This function caches the response. Refresh = true will bust the cache.  |

**Returns:** *Promise‹Buffer›*

The the provided string representing the AVAX AssetID

___

###  getAssetDescription

▸ **getAssetDescription**(`assetID`: Buffer | string): *Promise‹any›*

*Defined in [src/apis/evm/api.ts:146](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L146)*

Retrieves an assets name and symbol.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`assetID` | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or an b58 serialized string for the AssetID or its alias.  |

**Returns:** *Promise‹any›*

Returns a Promise<Asset> with keys "name", "symbol", "assetID" and "denomination".

___

###  getBaseURL

▸ **getBaseURL**(): *string*

*Inherited from [APIBase](common_apibase.apibase.md).[getBaseURL](common_apibase.apibase.md#getbaseurl)*

*Defined in [src/common/apibase.ts:63](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L63)*

Returns the baseurl's path.

**Returns:** *string*

___

###  getBlockchainAlias

▸ **getBlockchainAlias**(): *string*

*Defined in [src/apis/evm/api.ts:67](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L67)*

Gets the alias for the blockchainID if it exists, otherwise returns `undefined`.

**Returns:** *string*

The alias for the blockchainID

___

###  getBlockchainID

▸ **getBlockchainID**(): *string*

*Defined in [src/apis/evm/api.ts:99](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L99)*

Gets the blockchainID and returns it.

**Returns:** *string*

The blockchainID

___

###  getDB

▸ **getDB**(): *StoreAPI*

*Inherited from [APIBase](common_apibase.apibase.md).[getDB](common_apibase.apibase.md#getdb)*

*Defined in [src/common/apibase.ts:68](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L68)*

Returns the baseurl's database.

**Returns:** *StoreAPI*

___

###  getDefaultTxFee

▸ **getDefaultTxFee**(): *BN*

*Defined in [src/apis/evm/api.ts:210](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L210)*

Gets the default tx fee for this chain.

**Returns:** *BN*

The default tx fee as a [BN](https://github.com/indutny/bn.js/)

___

###  getRPCID

▸ **getRPCID**(): *number*

*Inherited from [JRPCAPI](common_jrpcapi.jrpcapi.md).[getRPCID](common_jrpcapi.jrpcapi.md#getrpcid)*

*Defined in [src/common/jrpcapi.ts:78](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/jrpcapi.ts#L78)*

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** *number*

___

###  getTxFee

▸ **getTxFee**(): *BN*

*Defined in [src/apis/evm/api.ts:219](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L219)*

Gets the tx fee for this chain.

**Returns:** *BN*

The tx fee as a [BN](https://github.com/indutny/bn.js/)

___

###  getUTXOs

▸ **getUTXOs**(`addresses`: string[] | string, `sourceChain`: string, `limit`: number, `startIndex`: [Index](../interfaces/common_interfaces.index.md)): *Promise‹object›*

*Defined in [src/apis/evm/api.ts:305](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L305)*

Retrieves the UTXOs related to the addresses provided from the node's `getUTXOs` method.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`addresses` | string[] &#124; string | - | An array of addresses as cb58 strings or addresses as [Buffer](https://github.com/feross/buffer)s |
`sourceChain` | string | undefined | A string for the chain to look for the UTXO's. Default is to use this chain, but if exported UTXOs exist from other chains, this can used to pull them instead. |
`limit` | number | 0 | Optional. Returns at most [limit] addresses. If [limit] == 0 or > [maxUTXOsToFetch], fetches up to [maxUTXOsToFetch]. |
`startIndex` | [Index](../interfaces/common_interfaces.index.md) | undefined | Optional. [StartIndex] defines where to start fetching UTXOs (for pagination.) UTXOs fetched are from addresses equal to or greater than [StartIndex.Address] For address [StartIndex.Address], only UTXOs with IDs greater than [StartIndex.Utxo] will be returned.  |

**Returns:** *Promise‹object›*

___

###  import

▸ **import**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:353](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L353)*

Send ANT (Avalanche Native Token) assets including AVAX from an account on the X-Chain to an address on the C-Chain. This transaction
must be signed with the key of the account that the asset is sent from and which pays
the transaction fee.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the account specified in `to` |
`password` | string | The password of the Keystore user |
`to` | string | The address of the account the asset is sent to. |
`sourceChain` | string | The chainID where the funds are coming from. Ex: "X"  |

**Returns:** *Promise‹string›*

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

___

###  importAVAX

▸ **importAVAX**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:389](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L389)*

Send AVAX from an account on the X-Chain to an address on the C-Chain. This transaction
must be signed with the key of the account that the AVAX is sent from and which pays
the transaction fee.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The Keystore user that controls the account specified in `to` |
`password` | string | The password of the Keystore user |
`to` | string | The address of the account the AVAX is sent to. This must be the same as the to argument in the corresponding call to the X-Chain’s exportAVAX |
`sourceChain` | string | The chainID where the funds are coming from.  |

**Returns:** *Promise‹string›*

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

___

###  importKey

▸ **importKey**(`username`: string, `password`: string, `privateKey`: string): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:419](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L419)*

Give a user control over an address by providing the private key that controls the address.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`username` | string | The name of the user to store the private key |
`password` | string | The password that unlocks the user |
`privateKey` | string | A string representing the private key in the vm's format  |

**Returns:** *Promise‹string›*

The address for the imported private key.

___

###  issueTx

▸ **issueTx**(`tx`: string | Buffer | [Tx](api_evm_transactions.tx.md)): *Promise‹string›*

*Defined in [src/apis/evm/api.ts:443](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L443)*

Calls the node's issueTx method from the API and returns the resulting transaction ID as a string.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`tx` | string &#124; Buffer &#124; [Tx](api_evm_transactions.tx.md) | A string, [Buffer](https://github.com/feross/buffer), or [Tx](api_avm_transactions.tx.md) representing a transaction  |

**Returns:** *Promise‹string›*

A Promise<string> representing the transaction ID of the posted transaction.

___

###  keyChain

▸ **keyChain**(): *[KeyChain](api_evm_keychain.keychain.md)*

*Defined in [src/apis/evm/api.ts:647](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L647)*

Gets a reference to the keychain for this class.

**Returns:** *[KeyChain](api_evm_keychain.keychain.md)*

The instance of [KeyChain](api_avm_keychain.keychain.md) for this class

___

###  parseAddress

▸ **parseAddress**(`addr`: string): *Buffer*

*Defined in [src/apis/evm/api.ts:128](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L128)*

Takes an address string and returns its [Buffer](https://github.com/feross/buffer) representation if valid.

**Parameters:**

Name | Type |
------ | ------ |
`addr` | string |

**Returns:** *Buffer*

A [Buffer](https://github.com/feross/buffer) for the address if valid, undefined if not valid.

___

###  refreshBlockchainID

▸ **refreshBlockchainID**(`blockchainID`: string): *boolean*

*Defined in [src/apis/evm/api.ts:108](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L108)*

Refresh blockchainID, and if a blockchainID is passed in, use that.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`blockchainID` | string | undefined |

**Returns:** *boolean*

A boolean if the blockchainID was successfully refreshed.

___

###  setAVAXAssetID

▸ **setAVAXAssetID**(`avaxAssetID`: string | Buffer): *void*

*Defined in [src/apis/evm/api.ts:198](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L198)*

Overrides the defaults and sets the cache to a specific AVAX AssetID

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`avaxAssetID` | string &#124; Buffer | A cb58 string or Buffer representing the AVAX AssetID  |

**Returns:** *void*

The the provided string representing the AVAX AssetID

___

###  setBaseURL

▸ **setBaseURL**(`baseurl`: string): *void*

*Inherited from [APIBase](common_apibase.apibase.md).[setBaseURL](common_apibase.apibase.md#setbaseurl)*

*Defined in [src/common/apibase.ts:47](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/common/apibase.ts#L47)*

Sets the path of the APIs baseurl.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`baseurl` | string | Path of the APIs baseurl - ex: "/ext/bc/X"  |

**Returns:** *void*

___

###  setBlockchainAlias

▸ **setBlockchainAlias**(`alias`: string): *string*

*Defined in [src/apis/evm/api.ts:87](https://github.com/ava-labs/avalanchejs/blob/cfff19f/src/apis/evm/api.ts#L87)*

Sets the alias for the blockchainID.

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`alias` | string | The alias for the blockchainID.   |

**Returns:** *string*