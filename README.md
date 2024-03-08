<p align="center">
<br />
<a href="https://thirdweb.com"><img src="https://github.com/thirdweb-dev/typescript-sdk/blob/main/logo.svg?raw=true" width="200" alt=""/></a>
<br />
</p>
<h1 align="center">thirdweb Contracts</h1>
<p align="center">
<a href="https://www.npmjs.com/package/@thirdweb-dev/contracts"><img src="https://img.shields.io/npm/v/@thirdweb-dev/contracts?color=red&logo=npm" alt="npm version"/></a>
<a href="https://github.com/thirdweb-dev/contracts/actions"><img alt="Build Status" src="https://github.com/thirdweb-dev/contracts/actions/workflows/tests.yml/badge.svg"/></a>
<a href="https://discord.gg/thirdweb"><img alt="Join our Discord!" src="https://img.shields.io/discord/834227967404146718.svg?color=7289da&label=discord&logo=discord&style=flat"/></a>

</p>
<p align="center"><strong>Collection of smart contracts deployable via the thirdweb SDK, dashboard and CLI</strong></p>
<br />

## Installation

```shell
# Forge projects
forge install https://github.com/thirdweb-dev/contracts

# Hardhat / npm based projects
npm i @thirdweb-dev/contracts
```

```bash
contracts
|
|-- extension: "extensions that can be inherited by NON-upgradeable contracts"
|   |-- interface: "interfaces of all extension contracts"
|   |-- upgradeable: "extensions that can be inherited by upgradeable contracts"
|   |-- [$prebuilt-category]: "legacy extensions written specifically for a prebuilt contract"
|
|-- base: "NON-upgradeable base contracts to build on top of"
|   |-- interface: "interfaces for all base contracts"
|   |--  upgradeable: "upgradeable base contracts to build on top of"
|
|-- prebuilt: "audited, ready-to-deploy thirdweb smart contracts"
|   |-- interface: "interfaces for all prebuilt contracts"
|   |--[$prebuilt-category]: "feature-based group of prebuilt contracts"
|   |-- unaudited: "yet-to-audit thirdweb smart contracts"
|       |-- [$prebuilt-category]: "feature-based group of prebuilt contracts"
|
|-- infra: "onchain infrastructure contracts"
|   |-- interface: "interfaces for all infrastructure contracts"
|
|-- eip: "implementations of relevant EIP standards"
|   |-- interface "all interfaces of relevant EIP standards"
|
|-- lib: "Solidity libraries"
|
|-- external-deps: "modified / copied over external dependencies"
|   |-- openzeppelin: "modified / copied over openzeppelin dependencies"
|   |-- chainlink: "modified / copied over chainlink dependencies"
|
|-- legacy-contracts: "maintained legacy thirdweb contracts"
```

## Running Tests

1. `yarn`: install contracts dependencies
2. `forge install`: install tests dependencies
3. `forge test`: run the tests

This repository is a [forge](https://github.com/foundry-rs/foundry/tree/master/forge) project.

First install the relevant dependencies of the project:

```bash
yarn

forge install
```

To compile contracts, run:

```bash
forge build
```

To run tests:

```bash
forge test
```

## Pre-built Contracts

Pre-built contracts are written by the thirdweb team, and cover the most common use cases for smart contracts.

- [DropERC20](https://thirdweb.com/deployer.thirdweb.eth/DropERC20)
- [DropERC721](https://thirdweb.com/deployer.thirdweb.eth/DropERC721)
- [DropERC1155](https://thirdweb.com/deployer.thirdweb.eth/DropERC1155)
- [SignatureDrop](https://thirdweb.com/deployer.thirdweb.eth/SignatureDrop)
- [Marketplace](https://thirdweb.com/deployer.thirdweb.eth/Marketplace)
- [Multiwrap](https://thirdweb.com/deployer.thirdweb.eth/Multiwrap)
- [TokenERC20](https://thirdweb.com/deployer.thirdweb.eth/TokenERC20)
- [TokenERC721](https://thirdweb.com/deployer.thirdweb.eth/TokenERC721)
- [TokenERC1155](https://thirdweb.com/deployer.thirdweb.eth/TokenERC1155)
- [VoteERC20](https://thirdweb.com/deployer.thirdweb.eth/VoteERC20)
- [Split](https://thirdweb.com/deployer.thirdweb.eth/Split)

[Learn more about pre-built contracts](https://portal.thirdweb.com/pre-built-contracts)

## Extensions

Extensions are building blocks that help enrich smart contracts with features.

Some blocks come packaged together as Base Contracts, which come with a full set of features out of the box that you can modify and extend. These contracts are available at `contracts/base/`.

Other (smaller) blocks are Features, which provide a way for you to pick and choose which individual pieces you want to put into your contract; with full customization of how those features work. These are available at `contracts/extension/`.

[Learn more about extensions](https://portal.thirdweb.com/extensions)

## Contract Audits

- [Audit 1](audit-reports/audit-1.pdf)
- [Audit 2](audit-reports/audit-2.pdf)
- [Audit 3](audit-reports/audit-3.pdf)
- [Audit 4](audit-reports/audit-4.pdf)
- [Audit 5](audit-reports/audit-5.pdf)
- [Audit 6](audit-reports/audit-6.pdf)
- [Audit 7](audit-reports/audit-7.pdf)
- [Audit 8](audit-reports/audit-8.pdf)
- [Audit 9](audit-reports/audit-9.pdf)
- [Audit 10](audit-reports/audit-10.pdf)
- [Audit 11](audit-reports/audit-11.pdf)
- [Audit 12](audit-reports/audit-12.pdf)

## Bug reports

Found a security issue with our smart contracts? Send bug reports to security@thirdweb.com and we'll continue communicating with you from there. We're actively developing a bug bounty program; bug report payouts happen on a case by case basis, for now.

## Feedback

If you have any feedback, please reach out to us at support@thirdweb.com.

## Authors

- [thirdweb](https://thirdweb.com)

## License

[Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0.txt)

## 動かした履歴

- ビルド

  ```bash
  forge build
  ```

  ```bash
  $ forge build
  [⠘] Compiling...
  [⠒] Compiling 829 files with 0.8.23
  [⠘] Solc 0.8.23 finished in 1661.20s
  Compiler run successful with warnings:
  ```

- テスト

  ```bash
  forge test --gas-report
  ```

  問題なければ全て実行されます。

  ```bash
  uite result: ok. 48 passed; 0 failed; 0 skipped; finished in 906.87ms (42.93ms CPU time)
  ```

  特定のテストだけ実行させたいとき

  ```bash
  forge test --match-path src/test/token/TokenERC721.t.sol
  ```

  実行結果

  ```bash
  [⠃] Compiling...
  formFeeInfo() (gas: 31951)
  [PASS] test_event_royaltyForToken() (gas: 66943)
  [PASS] test_event_setOwner() (gas: 107506)
  [PASS] test_event_setPrimarySaleRecipient() (gas: 26242)
  [PASS] test_revert_burn_NotOwnerNorApproved() (gas: 167454)
  [PASS] test_revert_mintTo_NotAuthorized() (gas: 83395)
  [PASS] test_revert_mintNo files changed, compilation skipped

  Ran 39 tests for src/test/token/TokenERC721.t.sol:TokenERC721Test
  [PASS] test_event_defaultRoyalty() (gas: 32193)
  [PASS] test_event_mintTo() (gas: 159309)
  [PASS] test_event_mintWithSignature() (gas: 275443)
  [PASS] test_event_platTo_emptyURI() (gas: 48184)
  [PASS] test_revert_mintWithSignature_InvalidSignature() (gas: 80854)
  [PASS] test_revert_mintWithSignature_MsgValueNotZero() (gas: 330852)
  [PASS] test_revert_mintWithSignature_MustSendTotalPrice() (gas: 321693)
  [PASS] test_revert_mintWithSignature_RecipientUndefined() (gas: 81498)
  [PASS] test_revert_mintWithSignature_RequestExpired() (gas: 77361)
  [PASS] test_revert_setContractURI() (gas: 76772)
  [PASS] test_revert_setDefaultRoyaltyInfo_ExceedsRoyaltyBps() (gas: 19502)
  [PASS] test_revert_setDefaultRoyaltyInfo_NotAuthorized() (gas: 77108)
  [PASS] test_revert_setOwner_NotModuleAdmin() (gas: 21155)
  [PASS] test_revert_setPlatformFeeInfo_ExceedsMaxBps() (gas: 19140)
  [PASS] test_revert_setPlatformFeeInfo_NotAuthorized() (gas: 76729)
  [PASS] test_revert_setPrimarySaleRecipient_NotAuthorized() (gas: 76375)
  [PASS] test_revert_setRoyaltyInfoForToken_ExceedsRoyaltyBps() (gas: 19118)
  [PASS] test_revert_setRoyaltyInfo_NotAuthorized() (gas: 76935)
  [PASS] test_setTokenURI_revert_Frozen() (gas: 45092)
  [PASS] test_setTokenURI_revert_NotAuthorized() (gas: 17694)
  [PASS] test_setTokenURI_state() (gas: 48329)
  [PASS] test_state_burn_TokenOperator() (gas: 167872)
  [PASS] test_state_burn_TokenOwner() (gas: 145060)
  [PASS] test_state_mintTo() (gas: 169775)
  [PASS] test_state_mintWithSignature_NonZeroPrice_ERC20() (gas: 404860)
  [PASS] test_state_mintWithSignature_NonZeroPrice_NativeToken() (gas: 394911)
  [PASS] test_state_mintWithSignature_ZeroPrice() (gas: 279989)
  [PASS] test_state_setContractURI() (gas: 27719)
  [PASS] test_state_setDefaultRoyaltyInfo() (gas: 38711)
  [PASS] test_state_setOwner() (gas: 107260)
  [PASS] test_state_setPlatformFeeInfo() (gas: 31959)
  [PASS] test_state_setPrimarySaleRecipient() (gas: 25422)
  [PASS] test_state_setRoyaltyInfoForToken() (gas: 66916)
  Suite result: ok. 39 passed; 0 failed; 0 skipped; finished in 489.89ms (20.43ms CPU time)

  Ran 1 test suite in 676.78ms (489.89ms CPU time): 39 tests passed, 0 failed, 0 skipped (39 total tests)
  ```

- テストカバレッジの確認方法

  ```bash
  forge coverage --report lcov
  ```