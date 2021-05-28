# Mainnet Addresses

This document contains the list of accounts related to the Parrot Protocol.

## Multisig (2/3)

* Multisig: GZXtZrRTaazATgJpWKReqUEYE6L2CSQRHkFnXQDPA2vD
  * [Multisig Walle UI](https://multisig.projectserum.com/#/GZXtZrRTaazATgJpWKReqUEYE6L2CSQRHkFnXQDPA2vD)
* Multisig PDA: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te

```
{
  multisigProgramID: A9HAbnCwoD6f2NkZobKFf6buJoN9gUVVvX5PoUnDHS6u,
  multisigPK: GZXtZrRTaazATgJpWKReqUEYE6L2CSQRHkFnXQDPA2vD,
  multisigPDA: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
  multisigPDANonce: 255
}
```

## Parrot Program

* Program: HajXYaDXmohtq2ZxZ6QVNEpqNn1T53Zc9FnR1CnaNnUf
* Upgrade Authority should be multsig PDA
  * 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te

## DebtType

debtType: DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h

```
debtType: {
    version: 0,
    debtToken: Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS,
    debtOriginator: 2MbGB5NQiXPUtnQnh6si6pNLopbiC1NGRSup6FWoy2wd,
    interestsHolder: 7JcXTXrUsTZGrqohWmSCiRUFLj1KCp5rXdEiFA2Ww5d2,
    owner: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
    nonce: 253
},
debtTypePDA: 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w,
debtToken: {
    mintAuthorityOption: 1,
    mintAuthority: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
    supply: 110001000000,
    decimals: 6,
    isInitialized: true,
    freezeAuthorityOption: 0,
    freezeAuthority: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00>
},
debtOriginator: {
    mint: Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS,
    owner: 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w,
    amount: 110001000000,
    delegateOption: 0,
    delegate: null,
    state: 1,
    isNativeOption: 0,
    isNative: false,
    delegatedAmount: 0,
    closeAuthorityOption: 0,
    closeAuthority: null,
    isInitialized: true,
    isFrozen: false,
    rentExemptReserve: null
},
interestsHolder: {
    mint: Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS,
    owner: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
    amount: 0,
    delegateOption: 0,
    delegate: null,
    state: 1,
    isNativeOption: 0,
    isNative: false,
    delegatedAmount: 0,
    closeAuthorityOption: 0,
    closeAuthority: null,
    isInitialized: true,
    isFrozen: false,
    rentExemptReserve: null
}

```

* `debtType.debtToken` should be PAI
  * Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS
* `debtType.debtToken.mintAuthority` should be multisig PDA
  * 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te
* `debtType.debtOriginator.owner` should be `debtTypePDA`
  * 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w
* `debtType.interestsHolder.owner` should be multisig PDA
  * 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te

### Debt Token (PAI)

```
debtType.debtToken (PAI): {
  mintAuthorityOption: 1,
  mintAuthority: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
  supply: 110001000000,
  decimals: 6,
  isInitialized: true,
  freezeAuthorityOption: 0,
  freezeAuthority: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00>
}
```

* SPL Token Account: [Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS](https://explorer.solana.com/address/Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS)
* Mint Authority: [5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te](https://explorer.solana.com/address/5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te)
  * Should be multisig PDA
* Decimals: 6

### Debt Originator (PAI)

```
debtType.debtOriginator: {
  mint: Ea5SjE2Y6yvCeW5dYTn7PYMuW5ikXkvbGdcmSnXeaLjS,
  owner: 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w,
  amount: 110001000000,
  delegateOption: 0,
  delegate: null,
  state: 1,
  isNativeOption: 0,
  isNative: false,
  delegatedAmount: 0,
  closeAuthorityOption: 0,
  closeAuthority: null,
  isInitialized: true,
  isFrozen: false,
  rentExemptReserve: null
}
```

* Owner: 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w
  * debtTypePDA of `[debt_type.pubkey, nonce]`

## Debt Type

* Debt Type Account: [DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h](https://explorer.solana.com/address/DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h)


## Vault Type (USDT)

```
vaultType USDT: 85EuQhTe2ZmbQpmTjqymLmKepgZgJytYFavvivpDwyTg
{
  version: 0,
  debtType: DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h,
  collateralToken: Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB,
  collateralTokenHolder: 2H5ojXwCuw41umvdXK2YhG83D1WUtpAF1T1KLPcbrLFu,
  priceOracle: STABLEQRACLE1111111111111111111111111111111,
  nonce: 255,
  minimumCollateralRatio: 10495,
  liquidationCollateralRatio: 10000,
  liquidationPenalty: 500,
  interestRate: 0,
  interestAccum: 0,
  interestAccumUpdated: 80211100,
  accruedInterests: 0,
  debtCeiling: 50000000000,
  totalDebt: 0
}
{
  vaultTypePDA: DGi3TxcKUq3E5t1mL33n9jRgdWWKngeRkP3fUppG4inn,
  collateralHolder: {
    mint: Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB,
    owner: DGi3TxcKUq3E5t1mL33n9jRgdWWKngeRkP3fUppG4inn,
    amount: 0,
    delegateOption: 0,
    delegate: null,
    state: 1,
    isNativeOption: 0,
    isNative: false,
    delegatedAmount: 0,
    closeAuthorityOption: 0,
    closeAuthority: null,
    isInitialized: true,
    isFrozen: false,
    rentExemptReserve: null
  }
}
```

* collateralToken: Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB
* priceOracle: STABLEQRACLE1111111111111111111111111111111
* interestRate: 0
* `collateralTokenHolder.owner` should be `vaultTypePDA`
* minimumCollateralRatio: 10495

## Vault Type (USDC)

```
vaultType USDC: BgA1FW2FbKCSEoi96atEZK9PToqvVos4f9hqESLJ2Zt1
{
  version: 0,
  debtType: DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h,
  collateralToken: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v,
  collateralTokenHolder: E6rHy8KhRYbrZg8qxRvVVyRYu5gRCHLpCbtqMaxUQVMq,
  priceOracle: STABLEQRACLE1111111111111111111111111111111,
  nonce: 253,
  minimumCollateralRatio: 10495,
  liquidationCollateralRatio: 10000,
  liquidationPenalty: 500,
  interestRate: 0,
  interestAccum: 0,
  interestAccumUpdated: 80210276,
  accruedInterests: 0,
  debtCeiling: 50000000000,
  totalDebt: 0
}
{
  vaultTypePDA: DefDiDiauGqS8ZUiHHuRCpmt8XZPGTTp6DY7UQP5NkkP,
  collateralHolder: {
    mint: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v,
    owner: DefDiDiauGqS8ZUiHHuRCpmt8XZPGTTp6DY7UQP5NkkP,
    amount: 0,
    delegateOption: 0,
    delegate: null,
    state: 1,
    isNativeOption: 0,
    isNative: false,
    delegatedAmount: 0,
    closeAuthorityOption: 0,
    closeAuthority: null,
    isInitialized: true,
    isFrozen: false,
    rentExemptReserve: null
  }
}
```

* collateralToken: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v
* priceOracle: STABLEQRACLE1111111111111111111111111111111
* interestRate: 0
* `collateralTokenHolder.owner` should be `vaultTypePDA`
* minimumCollateralRatio: 10495