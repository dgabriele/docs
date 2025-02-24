# Testnet 005

## Basic info

- Chain ID: `nois-testnet-005`
- Demon: `unois`

## Genesis

- URL:
  <https://raw.githubusercontent.com/noislabs/networks/nois-testnet-005/nois-testnet-005/genesis.json>
- Checksum (sha256):
  `1647cabd044110d6beda2fc4a32fb50dfbb5babff74bdf41503c58123ded3389`

## Binary

- Build `noisd` from <https://github.com/noislabs/noisd>
- Tag: v1.0.1
- `noisd version` should show 1.0.1

## p2p

Seed nodes

- `bf07906c7cf0f23606c83be15624be2c67b3929c@139.59.154.47:17356`
- `da81dd66bca4bba509163dbd06b4a6b2e05c2e12@nois-testnet-seed.itrocket.net:21656`

## RPCs

An incomplete and unchecked list of community provided TendermintRPC endpoints:

| URL                                       | TLS | CORS | tx_index |
| ----------------------------------------- | --- | ---- | -------- |
| https://nois-testnet-rpc.polkachu.com:443 | ✅  | ✅   | ✅       |
| https://nois-testnet.rpc.kjnodes.com:443  | ✅  | ?    | ?        |
| https://rpc.nois.mcbnode.online:443       | ✅  | ?    | ?        |
| http://185.198.27.109:26657               | No  | ?    | ?        |
| https://nois-testnet-rpc.itrocket.net:443 | ✅  | ✅   | ✅       |

---

## Contracts

#### nois-drand

```yaml
- Name: nois-drand
  Address: nois14xef285hz5cx5q9hh32p9nztu3cct4g44sxjgx3dmftt2tj2rweqkjextk
  Code ID: "1"
  Git Asset Name: nois_drand
  Instantiation Message: '{"incentive_point_price":"3000","incentive_denom":"unois","min_round":,"manager":"nois1tfg9ptr84t9zshxxf5lkvrd6ej7gxjh75lztve"}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.11.0
  Config:
    gateway: nois1c9l6qcl82u7zkgjduj2snfuv5rz6jzwsumw4nktgytzclazujc6qc05p5j
    incentive_denom: unois
    incentive_point_price: "3000"
    manager: nois1tfg9ptr84t9zshxxf5lkvrd6ej7gxjh75lztve
    min_round: 833618
```

#### nois-icecube

```yaml
- Name: nois-icecube
  Address: nois1gwnfyx82rwgc4y9r8vx6nr9v35dwezw3dadw6h39mad9amg7shnsler5f0
  Code ID: "6"
  Git Asset Name: nois_icecube
  Instantiation Message: '{"manager":"nois1tfg9ptr84t9zshxxf5lkvrd6ej7gxjh75lztve"}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.11.0
```

#### nois-gateway

```yaml
- Name: nois-gateway
  Address: nois1xwde9rzqk5u36fke0r9ddmtwvh43n4fv53c5vc462wz8xlnqjhls6d90xc
  Code ID: "44"
  Git Asset Name: nois_gateway
  Instantiation Message: '{"manager":"nois1tfg9ptr84t9zshxxf5lkvrd6ej7gxjh75lztve","price":{"denom":"unois","amount":"50000000"},"payment_code_id":57,"sink":"nois10c0ppz0n57hqrmfp7g7lqs6k4xk9rxhvcfkqt83r8mars2lc57mq0f6cty"}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.13.0
  Config:
    drand: nois14xef285hz5cx5q9hh32p9nztu3cct4g44sxjgx3dmftt2tj2rweqkjextk
    manager: nois1tfg9ptr84t9zshxxf5lkvrd6ej7gxjh75lztve
    payment_code_id: 58
    payment_initial_funds: null
    price:
      amount: "50000000"
      denom: unois
    sink: nois10c0ppz0n57hqrmfp7g7lqs6k4xk9rxhvcfkqt83r8mars2lc57mq0f6cty
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
---

### Proxies

#### uni-6

```yaml
- Chain-id: uni-6
  Address: juno13atw6x2vlvckz7fx89dc8zz7e83ysj3m8rs5dazcwj8scdwugn8s89wwqc
  Git Asset Name: nois_proxy
  Instantiation Message: '{"prices":[{"denom":"ujunox","amount":"100"}],"withdrawal_address":"juno1q6yvx8lxpheqflkcl0qf89czej4akrsfzc6xs2","callback_gas_limit":500000,"test_mode":false,"mode":{"ibc_pay":{"unois_denom":{"ics20_channel":"channel-175","denom":"ibc/717352A5277F3DE916E8FD6B87F4CA6A51F2FBA9CF04ABCFF2DF7202F8A8BC50"}}}}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.12.0
  Config:
    callback_gas_limit: 500000
    mode:
      ibc_pay:
        unois_denom:
          denom: ibc/717352A5277F3DE916E8FD6B87F4CA6A51F2FBA9CF04ABCFF2DF7202F8A8BC50
          ics20_channel: channel-175
    nois_beacon_price: "50000000"
    nois_beacon_price_updated: "1681597699262712630"
    payment: nois1jh3tteg4cgq8850urwkahxhqazzhq2lgs4q6jkt7ayxgkphvllkqxk4v4r
    prices:
    - amount: "100"
      denom: ujunox
    test_mode: false
    withdrawal_address: juno1q6yvx8lxpheqflkcl0qf89czej4akrsfzc6xs2
```

#### injective-888

```yaml
- Chain-id: injective-888
  Address: inj1492g0dmg4l7dm6nppsy5zhuwh8q350j2wfrxrd
  Git Asset Name: nois_proxy
  Instantiation Message: '{"prices":[{"denom":"inj","amount":"100"},{"denom":"ibc/B0D9A85855FFB4C6472AD514B48C91275453B2AFC501472EE29895C400463E6B","amount":"50000000"}],"manager":"inj1decjtp0szudj4flvfa57wvkqenkeuk5pt28j7t","callback_gas_limit":10000,"test_mode":false,"mode":{"ibc_pay":{"unois_denom":{"ics20_channel":"channel-46","denom":"ibc/B0D9A85855FFB4C6472AD514B48C91275453B2AFC501472EE29895C400463E6B"}}}}'
  URL: "https://github.com/noislabs/nois-contracts"
  Version: v0.13.0
  Config:
    callback_gas_limit: 500000
    manager: inj1decjtp0szudj4flvfa57wvkqenkeuk5pt28j7t
    mode:
      ibc_pay:
        unois_denom:
          denom: ibc/B0D9A85855FFB4C6472AD514B48C91275453B2AFC501472EE29895C400463E6B
          ics20_channel: channel-46
    nois_beacon_price: "50000000"
    nois_beacon_price_updated: "1682297627977789371"
    payment: nois1y9hngs5f2gzvwepz5gxhmsehlytaf6n045vnhmxh27rdq44cg56std3zde
    prices:
    - amount: "100"
      denom: inj
    - amount: "1000000"
      denom: ibc/B0D9A85855FFB4C6472AD514B48C91275453B2AFC501472EE29895C400463E6B
    test_mode: false
```

---

## IBC denoms

On Nois:

unois on:

```yaml
- chain-id: uni-6
  denom: ibc/717352A5277F3DE916E8FD6B87F4CA6A51F2FBA9CF04ABCFF2DF7202F8A8BC50
  channel-id: channel-175
- chain-id: euphoria-2
  denom: ibc/70D9353E4D43D860BF051ECE427C427687EDED77E61EFEF2CFF2839D28E6AE43
  channel-id: channel-61
- chain-id: injective-888
  denom: ibc/B0D9A85855FFB4C6472AD514B48C91275453B2AFC501472EE29895C400463E6B
  channel-id: channel-46
```

