
https://github.com/user-attachments/assets/5588d2d8-1250-4918-8a6e-c30598f0c4d1
# tonkeeper-ios-critical-bug
Critical security bug in Tonkeeper iOS: invalid mnemonic creates usable wallet, assets locked
# 🚨 Critical Bug: Tonkeeper iOS accepts invalid mnemonic — causes asset loss

## Summary
A critical bug in Tonkeeper iOS allows importing an invalid 12-word mnemonic without checksum validation, generating a functional wallet.

The same mnemonic is **correctly rejected** by Tonkeeper Android.

This inconsistency can cause **irreversible asset loss** when users unknowingly store assets in wallets generated from invalid mnemonics.

---

## Environment
- **Device (iOS):** iPhone 16 Pro Max  
- **iOS version:** 18.5  
- **Tonkeeper iOS version:** 5.26  
- **Device (Android):** [Your Android device model]  
- **Android version:** [Your Android version]  
- **Tonkeeper Android version:** 5.26  
- **Wallet address (iOS-generated):** `UQA9i4g2LFQ0J6-kIqXW-gyC1Nku1YfnQ0PHpvGoUw7Iio2P`

---

## Steps to Reproduce
### Test mnemonic (invalid, should fail checksum validation):
attack liquid dial wrestle jungle arrive wolf mirror tonight solid sister slab


**1. Import on Tonkeeper iOS**
- Result: Successfully imports and generates a usable wallet
- Address: [Paste iOS-generated address here]

**2. Import on Tonkeeper Android**
- Result: Fails to import — error: `invalid mnemonic`

---

## Actual Result
- **iOS:** Imports invalid mnemonic successfully, wallet works temporarily but later becomes inaccessible
- **Android:** Rejects the invalid mnemonic (expected behavior)

---

## Expected Result
Both iOS and Android should reject invalid mnemonic phrases via checksum validation.  
No wallet should be generated from an invalid mnemonic.

---

## Evidence
- 📹 **iOS Import Video**: [Insert link or upload]  
- 📷 **Android Import Screenshot**: [Insert link or upload]  
- 🔗 **On-chain transactions** from iOS wallet:  
  - [Transaction 1 link]  
  - [Transaction 2 link]  
- 📷 **Error screenshots** when attempting transactions after lockout: [Insert link]

---

## Impact
- Users can unknowingly store assets in wallets generated from invalid mnemonics.
- Assets become inaccessible when the wallet cannot be recovered.
- This is a **Tonkeeper iOS implementation bug**, not user error.

---

## Requested Action
- Fix checksum validation in Tonkeeper iOS to match Android behavior.
- Assist affected users in recovering wallets 

https://github.com/user-attachments/assets/b15183e1-b6a2-42ac-a1f8-26dda262934c

or compensate asset losses.
- Publicly acknowledge this bug to warn other users.

---

## Contact
For verification or follow-up, please reach me via GitHub Issues on this repository.



https://github.com/user-attachments/assets/168f7cfa-4f74-49fb-9a4b-3733b7080413



https://github.com/user-attachments/assets/99882cf4-5bd2-429b-8b3c-cad16b56b0a8


