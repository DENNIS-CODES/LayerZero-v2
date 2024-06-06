<div align="center">
  <a href="https://layerzero.network">
    <img alt="LayerZero" style="width: 20%" src="https://layerzero.network/static/logo.svg"/>
  </a>

  <h1>LayerZero V2</h1>

  <p>
    <strong>Omnichain Interoperability Protocol</strong>
  </p>

  <p>
    <a href="https://docs.layerzero.network/v2"><img alt="Tutorials" src="https://img.shields.io/badge/docs-tutorials-blueviolet" /></a>
  </p>
</div>

LayerZero is an immutable, censorship-resistant, and permissionless messaging protocol that connects over 60 blockchains, enabling omnichain interoperability for blockchain applications. 

With LayerZero V2, developers can create applications that seamlessly interact across multiple blockchains.

- **Solidity Contract Standards**: [Send arbitrary data, tokens, and external calls to multiple chains](https://docs.layerzero.network/v2/developers/evm/overview).
- **Decentralized Verifier Networks (DVNs)**: [Configure any number and type of DVNs](https://docs.layerzero.network/v2/home/modular-security/security-stack-dvns) to verify your application's cross-chain messages.
- **Executors**: [Automatically deliver messages on behalf of the source sender](https://docs.layerzero.network/v2/home/permissionless-execution/executors) and handle destination gas for a fee.

Refer to the [LayerZero V2 Docs](https://docs.layerzero.network/v2) for implementation details, handling, and debugging LayerZero contracts.

Join the `#dev-general` channel on [Discord](https://discord-layerzero.netlify.app/discord) to discuss technical issues.

[Audit Reports](https://github.com/LayerZero-Labs/Audits)

## Build & Test

```bash
yarn && yarn build && yarn test
```

## Build an Omnichain Application (OApp)

All contracts in the `/oapp` directory can be used to build an Omnichain Application (OApp):

- **OApp**: The OApp Standard provides a generic message-passing interface to send and receive arbitrary data between contracts on different blockchains. See the [OApp Quickstart](https://docs.layerzero.network/v2/developers/evm/oapp/overview) to start building.
- **OFT**: The Omnichain Fungible Token (OFT) Standard allows tokens to be transferred across blockchains without asset wrapping or middlechains. See the [OFT Quickstart](https://docs.layerzero.network/v2/developers/evm/oft/quickstart) to learn more.

## Protocol Contracts

The core, immutable protocol contract interfaces, such as the [LayerZero Endpoint](https://docs.layerzero.network/v2/home/protocol/layerzero-endpoint), are located in the `/protocol` directory.

## MessageLib

Contracts related to the append-only, on-chain [MessageLibs](https://docs.layerzero.network/v2/home/protocol/message-library) are in the `/messagelib` directory. Inside, you will find reference implementations for how the [DVN](https://docs.layerzero.network/v2/home/modular-security/security-stack-dvns) and [Executor](https://docs.layerzero.network/v2/home/permissionless-execution/executors) communicate with Ultra Light Nodes on each chain.

- **DVN**: Developers can run a custom DVN by deploying a DVN contract on every supported chain. See the [Build DVN](https://docs.layerzero.network/v2/developers/evm/off-chain/build-dvns) guide.
- **Executor**: Deploy a custom Executor to ensure seamless message execution on the destination chain. See the [Executor](https://docs.layerzero.network/v2/developers/evm/off-chain/build-executors) guide.

## Acknowledgments

Thank you to the core development team for building LayerZero Endpoints:
- Ryan Zarick
- Isaac Zhang
- Caleb Banister
- Carmen Cheng
- T. Riley Schwarz

## Licensing

The primary license for LayerZero is the Business Source License 1.1 (BUSL-1.1). See the [`LICENSE`](./LICENSE) for more details.
