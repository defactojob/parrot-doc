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

## DebtType (PAI)

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

## Vault Type (SOL)

vaultType wSOL: 8PcJ5FmtmuYQCvBhaHkVY5DKVBn8BsMtV5RVqHU4h8ir

```
vaultType wSOL: 8PcJ5FmtmuYQCvBhaHkVY5DKVBn8BsMtV5RVqHU4h8ir
{
  version: 0,
  debtType: DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h,
  collateralToken: So11111111111111111111111111111111111111112,
  collateralTokenHolder: 9xRXTJWjKwv9sLczhWaPGD6hsJo26qRGN65Essq7R4TM,
  priceOracle: 6C8dCcYDd7ykNT2EFU6drGAhJhoGqbEBU5kNowHox34p,
  nonce: 252,
  minimumCollateralRatio: 80000,
  liquidationCollateralRatio: 12500,
  liquidationPenalty: 500,
  interestRate: 14623560433,

  // ...
  debtCeiling: 25000000001,
  // ...

}

{
  vaultTypePDA: 62Xb5ydBN1vrkg85SuKEL6aPv4bsy6iTiH3Jvki8NfNr,
  collateralHolder: {
    mint: So11111111111111111111111111111111111111112,
    owner: 62Xb5ydBN1vrkg85SuKEL6aPv4bsy6iTiH3Jvki8NfNr,
    amount: 102043434,
    delegateOption: 0,
    delegate: null,
    state: 1,
    isNativeOption: 1,
    isNative: true,
    delegatedAmount: 0,
    closeAuthorityOption: 0,
    closeAuthority: null,
    isInitialized: true,
    isFrozen: false,
    rentExemptReserve: 2039280
  }
}
interest rate per year: 499.999999972176 (5%)
```

* collateralToken: Es9vMFrzaCERmJfrF4H2FYD4KCoNkY11McCe8BenwNYB
* priceOracle: 6C8dCcYDd7ykNT2EFU6drGAhJhoGqbEBU5kNowHox34p
* interestRate: 14623560433
* `collateralTokenHolder.owner` should be `vaultTypePDA`
* minimumCollateralRatio: 80000 (800%)
* liquidationCollateralRatio: 12500 (125%)
* liquidationPenalty: 500 (5%)
* debtCeiling 25000000001 (25k)

## Debt Type (pBTC)

debtType: BMvtz4D3pDD7PQrf19A9VDPBN6HCBTww26Gcx1YMy3XJ

```
{
  debtType: {
    version: 0,
    debtToken: DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun,
    debtOriginator: E2Z1LARf4JhYB4KM4HM9nZYTkown9UqcDKV7iYDcfwFP,
    interestsHolder: 7dPyEyWxdfqAUyTpuUyxhtSKQYFgVsw9v8qXmvkA5or2,
    owner: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
    nonce: 255
  },
  debtTypePDA: 8df6UEhPTC97TXi5FQBG9bA3GrXYU7nTWtzrTV1exmKs,
  debtToken: {
    mintAuthorityOption: 1,
    mintAuthority: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
    supply: 100000000,
    decimals: 8,
    isInitialized: true,
    freezeAuthorityOption: 0,
    freezeAuthority: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00>
  },
  debtOriginator: {
    mint: DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun,
    owner: 8df6UEhPTC97TXi5FQBG9bA3GrXYU7nTWtzrTV1exmKs,
    amount: 99972700,
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
    mint: DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun,
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
}
```

* `debtType.debtToken` should be PAI
  * DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun
* `debtType.debtToken.mintAuthority` should be multisig PDA
  * 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te
* `debtType.debtOriginator.owner` should be `debtTypePDA`
  * 8aTV8MJRHMxRq6KSBVENEJciSQGKdheCEHAtM6j7qL1w
  * TODO needs transfer
* `debtType.interestsHolder.owner` should be multisig PDA
  * 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te


### Debt Token (pBTC)

```
debtToken: {
  mintAuthorityOption: 1,
  mintAuthority: 5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te,
  supply: 100000000,
  decimals: 8,
  isInitialized: true,
  freezeAuthorityOption: 0,
  freezeAuthority: <Buffer 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00>
}
```

* SPL Token Account: [DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun](https://explorer.solana.com/address/DYDWu4hE4MN3aH897xQ3sRTs5EAjJDmQsKLNhbpUiKun)
* Mint Authority: [5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te](https://explorer.solana.com/address/5jwBGfXVpcEY9Hqmw2hCu77NMnoMeVKzgKCChf82d1Te)
  * Should be multisig PDA
* Decimals: 8

## Vault Type (USDC-pBTC)

vaultType USDC:pBTC 5dRJyjAadyEQ4vFr8ic1q7nncPiRX5JsHLPQPHgENmSc

```
{
  version: 0,
  debtType: BMvtz4D3pDD7PQrf19A9VDPBN6HCBTww26Gcx1YMy3XJ,
  collateralToken: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v,
  collateralTokenHolder: 3D8UyBKWyQ26B6dupWjtehrUifi5nF6LmGwD6hwgB6yg,
  priceOracle: EjwENJ2jbJ9psKeapDezu5oKQe9chnU4wQJFE4ufymDs,
  nonce: 255,
  minimumCollateralRatio: 40000,
  liquidationCollateralRatio: 12500,
  liquidationPenalty: 500,
  interestRate: 2924712087,
  interestAccum: 1613750839971468,
  interestAccumUpdated: 85882672,
  accruedInterests: 9980998175877125,
  debtCeiling: 100000000,
  totalDebt: 503596123193268934993925
}
{
  vaultTypePDA: DQV7nFUWKSsiT7eWPhfGhdiRFsU1DmnEYgbFGKuPPsMs,
  collateralHolder: {
    mint: EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v,
    owner: DQV7nFUWKSsiT7eWPhfGhdiRFsU1DmnEYgbFGKuPPsMs,
    amount: 100006897,
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
interest rate per year: 100.0000000070496
```

* oracle: EjwENJ2jbJ9psKeapDezu5oKQe9chnU4wQJFE4ufymDs
  * how many SAT to purchase USDC
* 1% borrow rate

## Vault Type (PTT)

Parrot Test Token is a vault type used by the team to test liquidation using the mainnet environment.

* Team controls the minting of PTT for testing purposes.
* Debt ceiling is set to $1000. There is no way to go above that.
* totalDebt is a fixed point U64F64 number, represented as `13082536426707183180`.
  * This is equivalent to about $0.7 PAI

```
{
  version: 0,
  debtType: DNFiMrAVT3RatwZwfMxRfeVvsY96ha18ZnXKyuZkFh5h,
  collateralToken: E2Ub8wPfxxEvdrtumbfeL2HaQHgpd3gUGkDxDmmgN3p9,
  collateralTokenHolder: CACqmtL8sQtyiJT1seToU3pLnYSC6NHzF6y3vBS2uNp3,
  priceOracle: 5o3S9uVpJh2mkFW44GHtLuNjCFqFV1CumR2Q7mC44LFD,
  nonce: 254,
  minimumCollateralRatio: 80000,
  liquidationCollateralRatio: 12500,
  liquidationPenalty: 500,
  interestRate: 14623560433,
  interestAccum: 8115871310468938,
  interestAccumUpdated: 84341889,
  accruedInterests: 14475329890214995650124,
  debtCeiling: 1000000000,
  totalDebt: 13082536426707183180
}

{
  vaultTypePDA: 4wqB5wkBbQu4E4V3RofEJmy2zgHh354nvvPqhZw2ySVc,
  collateralHolder: {
    mint: E2Ub8wPfxxEvdrtumbfeL2HaQHgpd3gUGkDxDmmgN3p9,
    owner: 4wqB5wkBbQu4E4V3RofEJmy2zgHh354nvvPqhZw2ySVc,
    amount: 63776,
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

interest rate per year: 499.999999972176
```
