## Base Learn
Learn to Build Smart Contracts and Onchain Apps.

## Information
- Site:  [Base Docs](https://docs.base.org/base-learn/docs/welcome/)
- Claim Roles: [Base Learn](https://guild.xyz/base/base-learn)

## Tested Platform
- Software

  ```
  Foundry
  Forge 0.2.0
  ```

## Install & Dependence
- Foundry
- OpenZeppelin

## Install Foundry
- First, you'll need to install Foundry. Run this command in your terminal

  ```
  curl -L https://foundry.paradigm.xyz | bash
  ```

- Then run

  ```
  foundryup
  ```

## Clone Repository
- Clone base-learn Repository

  ```
  git clone https://github.com/0xfas/base-learn.git
  ```

- Move to base-learn Repository

  ```
  cd base-learn
  ```

## How to Run
- Create a .env file

  ```
  touch .env
  ```

- Edit .env file

  ```
  BASE_MAINNET_RPC="https://mainnet.base.org"
  BASE_SEPOLIA_RPC="https://sepolia.base.org"
  BASESCAN_API_KEY="Your Base API Key"
  PRIVATE_KEY="Your Private Key"
  CHAIN="84532"
  ```

- Build Your Project

  ```
  source .env
  ```

  ```
  forge build
  ```

- Run Tests

  ```
  forge test
  ```

## Deploy & Verify CLI Commands
- For Basic Deploy

  ```
  forge create --rpc-url $BASE_SEPOLIA_RPC --private-key $PRIVATE_KEY <src/"Your Deploy Files":"Your Contract">
  ```

  Example:

  ```
  forge create --rpc-url $BASE_SEPOLIA_RPC --private-key $PRIVATE_KEY src/BasicMath.sol:BasicMath
  ```

- For Deploy With Constructor Arguments

  ```
  forge create --rpc-url $BASE_SEPOLIA_RPC --private-key $PRIVATE_KEY <src/"Your Deploy Files":"Your Contract"> --constructor-args "value 1" "value 2"
  ```

  Example:

  ```
  forge create --rpc-url $BASE_SEPOLIA_RPC --private-key $PRIVATE_KEY src/EmployeeStorage.sol:EmployeeStorage --constructor-args 1000 Pat 50000 112358132134
  ```

- For Basic Verify

  ```
  forge verify-contract <Your Contract Address> --chain $CHAIN <src/"Your Deploy Files":"Your Contract">
  ```

  Example:

  ```
  forge verify-contract 0xF1EaXXXXX --chain $CHAIN src/BasicMath.sol:BasicMath
  ```

- For Verify With Constructor Arguments

  ```
  forge verify-contract <Your Contract Address> --chain $CHAIN <src/"Your Deploy Files":"Your Contract"> --constructor-args $(cast abi-encode "constructor(data type, data type)" "value 1" "value 2")
  ```

  Example:

  ```
  forge verify-contract 0xF1EaXXXXX --chain $CHAIN src/EmployeeStorage.sol:EmployeeStorage --constructor-args $(cast abi-encode "constructor(uint16,string,uint32,uint256)" 1000 Pat 50000 112358132134)
  ```

## Other
- Install The OpenZeppelin Library

  ```
  forge install OpenZeppelin/openzeppelin-contracts
  ```

- Export a Remapping in Our Directory to Help Locate The Library

  ```
  forge remappings > remappings.txt
  ```

- Flag Indicating Whether to Flatten The Source Code Before Verifying

  ```
  --flatten
  ```

- Wait For Verification Result After Submission

  ```
  --watch
  ```

## Follow Airdrop Infinity 🌐
➖ Telegram Channel: [Airdrop Infinity](https://t.me/airdropinfinityid)\
➖ Telegram Group: [Airdrop Infinity Group](https://t.me/airdropinfinitygroup)\
➖ X: [0xFAS](https://x.com/0xFASNET)

## Donate ☕
♦️ Ethereum: 0x8B42A04627120f4e23c8702d2b8127A3827aDcf9

❤️ Thank You