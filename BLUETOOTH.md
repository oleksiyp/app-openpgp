# Bluetooth build of the Ledger OpenPGP app (unofficial)

This fork of [LedgerHQ/app-openpgp](https://github.com/LedgerHQ/app-openpgp) changes **one line**:

```diff
-#ENABLE_BLUETOOTH = 1
+ENABLE_BLUETOOTH = 1
```

so the app answers over Bluetooth on Ledger Flex and Stax. It is used by
[sealctl](https://github.com/oleksiyp/sealctl).

* Branch: `ble-support`. CI (`.github/workflows/ble-build.yml`) fails if anything else differs
  from upstream, builds Flex and Stax binaries and publishes their hashes.
* A weekly job opens a pull request when upstream changes.
* Not affiliated with or signed by Ledger. Sideloading shows an "unverified app" warning;
  verify that the hash shown by `ledgerblue.listApps` matches the published `app.sha256`.

Installation steps: see the `INSTALL.txt` inside each release archive.
