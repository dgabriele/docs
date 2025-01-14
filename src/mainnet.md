# Mainnet

## Basic info

- Chain ID: `nois-1`
- Demon: `unois`

## Genesis

- Time: March 28th 15:00 UTC
- URL:
  <https://raw.githubusercontent.com/noislabs/networks/nois1.final.1/nois-1/genesis.json>
- Checksum (sha256):
  `5332fb6477a2d273fd7e5a13bceb213e2a9d408a698c49ab34e8b78736e58cac`

## Binary

- Build `noisd` from <https://github.com/noislabs/noisd>
- Tag: v1.0.1
- `noisd version` should show 1.0.1

## p2p

Seed nodes

- `b3e3bd436ee34c39055a4c9946a02feec232988c@seeds.cros-nest.com:56656`
- `babc3f3f7804933265ec9c40ad94f4da8e9e0017@seed.rhinostake.com:17356`
- `ade4d8bc8cbe014af6ebdf3cb7b1e9ad36f412c0@seeds.polkachu.com:17356`
- `72cd4222818d25da5206092c3efc2c0dd0ec34fe@161.97.96.91:36656` (AM Solutions)
- `20e1000e88125698264454a884812746c2eb4807@seeds.lavenderfive.com:17356`
- `c8db99691545545402a1c45fa897f3cb1a05aea6@nois-mainnet-seed.itrocket.net:36656`
- `400f3d9e30b69e78a7fb891f60d76fa3c73f0ecc@nois.rpc.kjnodes.com:51659`

## RPCs

An incomplete and unchecked list of community provided TendermintRPC endpoints:

| URL                                       | TLS | CORS | tx_index |
| ----------------------------------------- | --- | ---- | -------- |
| https://rpc.cosmos.directory/nois (load balancer) |     |      |          |
| https://rpc-nois.sr20de.xyz:443           | ✅  | ✅   | ✅       |
| https://rpc.nois.hexnodes.co:443          | ✅  | ✅   | ✅       |
| https://m-nois.rpc.utsa.tech:443          | ✅  | ✅   | ✅       |
| https://rpc-nois.d-stake.xyz:443          | ✅  | ✅   | ✅       |
| https://nois.rpc.cumulo.org.es:443        | ✅  | ✅   | ✅       |
| https://nois-mainnet-rpc.itrocket.net:443 | ✅  | ✅   | ✅       |
| https://nois-rpc.nysa.network:443         | ✅  | ❌   | ✅       |
| https://rpc.nois.chaintools.tech/         | ✅  | ✅   | ❌       |
| https://nois.rpc.m.stavr.tech:443         | ✅  | ✅   | ✅       |
| https://nois.rpc.kjnodes.com:443          | ✅  | ✅   | ✅       |

## Contracts

#### nois-drand

```yaml
- Name: nois-drand
  Address: nois19w26q6n44xqepduudfz2xls4pc5lltpn6rxu34g0jshxu3rdujzsj7dgu8
  Code ID: "4"
  Git Asset Name: nois_drand
  Instantiation Message: '{"incentive_point_price":"3000","incentive_denom":"unois","min_round":808287,"manager":"nois1p9tw323xdjp5q3yzuecfahmgrpufmm89z93wpk"}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.11.0
```

#### nois-icecube

```yaml
- Name: nois-icecube
  Address: nois1gwnfyx82rwgc4y9r8vx6nr9v35dwezw3dadw6h39mad9amg7shnsler5f0
  Code ID: "6"
  Git Asset Name: nois_icecube
  Instantiation Message: '{"manager":"nois1p9tw323xdjp5q3yzuecfahmgrpufmm89z93wpk"}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.11.0
```

#### nois-sink

```yaml
- Name: nois-sink
  Address: nois10c0ppz0n57hqrmfp7g7lqs6k4xk9rxhvcfkqt83r8mars2lc57mq0f6cty
  Code ID: "5"
  Git Asset Name: nois_sink
  Instantiation Message: "{}"
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.11.0
```

## IBC channels

Right now the following IBC channels are supported:

|  Protocol | Other chain           | Channel (nois-1) | Channel (other chain) |
| --------- | --------------------- | ---------------- | --------------------- |
| ICS-20    | Stargaze (stargaze-1) | channel-0        | channel-137           |
| ICS-20    | Juno (juno-1)         | channel-1        | channel-225           |

## IBC denoms

On Nois:

- ustars: `ibc/49BAE4CD2172833F14000627DA87ED8024AD46A38D6ED33F6239F22B5832F958`
- ujuno: `ibc/EFF323CC632EC4F747C61BCE238A758EFDB7699C3226565F7C20DA06509D59A5`

unois on:

- Stargaze (stargaze-1):
  `ibc/0F181D9F5BB18A8496153C1666E934169515592C135E8E9FCCC355889858EAF9`
- Juno (juno-1):
  `ibc/1D9E14A1F00613ED39E4B8A8763A20C9BE5B5EA0198F2FE47EAE43CD91A0137B`
