# ESG-Vendor-Registry-Move-Smart-Contract
# ♻️ ESG Vendor Registry – Move Smart Contract

A lightweight smart contract on the Aptos blockchain to *register and verify ESG-compliant vendors*. This is ideal for decentralized procurement platforms, sustainability audits, and supply chain transparency.

## 📄 Description

This Move module allows vendors to self-register and declare their ESG (Environmental, Social, and Governance) compliance status. Other users can query the compliance status of any registered vendor using their address.

## 🔧 Features

- ✅ Register vendors with ESG compliance flag
- 🔍 Verify ESG status of vendors by address
- 💡 Simple structure using Aptos Move

## 📦 Module Overview

### Structs

- Vendor: Contains vendor name and a boolean flag is_esg_compliant.

### Functions

#### register_vendor(account: &signer, name: vector<u8>, esg_compliant: bool)

Registers a vendor to the blockchain under the signer's address.

#### is_esg_compliant(vendor_address: address): bool

Returns true if the given vendor address is ESG-compliant.

## 🛠️ Usage Example

```move
// Register a vendor
register_vendor(&signer, b"MyEcoCompany", true);

// Check if a vendor is ESG-compliant
let status = is_esg_compliant(@0xABCD...);
