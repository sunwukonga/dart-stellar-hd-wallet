# Stellar HD Wallet

Stellar HD Wallet, base on bip39 and stelalr sdk，you can use it to generate random mnemonic and get account from mnemonic

## import

pubspec.yaml
```
stellar_hd_wallet: ^1.0.0
```

## example
```
    import 'package:stellar_hd_wallet/stellar_hd_wallet.dart';

    void main(){
        // get random mnemonic ( english )
        final mnemonic = StellarHDWallet.generateMnemonic();
        print(mnemonic);
        final wallet = StellarHDWallet.fromMnemonic(mnemonic);
        final keypair = wallet.getKeyPair();
        // get accountId
        final accountId = keypair.accountId;
        final secretSeed = keypair.secretSeed;
        print(accountId);
        print(secretSeed);
        final keypairIndex1 = wallet.getKeyPair(index: 1);
        print(keypairIndex1.accountId);
        print(keypairIndex1.secretSeed);
    }

```

