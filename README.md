# @solar-network/peers

## Installation

```bash
yarn add @solar-network/peers
```

## Usage

### Peers via GitHub

```ts
import { PeerDiscovery } from "@solar-network/peers";

peerDiscovery = await PeerDiscovery.new({
	networkOrHost: "devnet"
})

peers = peerDiscovery
	.withVersion(">=2.4.0-next.0")
	.withLatency(300)
	.sortBy("latency")
	.findPeersWithPlugin("core-api");
```

### Peers via Relay

```ts
import { PeerDiscovery } from "@solar-network/peers";

peerDiscovery = await PeerDiscovery.new({,
	// https://sxp.testnet.sh for development
	networkOrHost: "https://sxp.mainnet.sh/api/peers",
})

peers = peerDiscovery
	.withVersion(">=2.4.0-next.0")
	.withLatency(300)
	.sortBy("latency")
	.findPeersWithPlugin("core-api");
```

## Testing

```bash
yarn test
```

## Credits

## License

[MIT](LICENSE) © [Ark Ecosystem](https://ark.io)
