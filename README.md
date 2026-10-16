# Parano1d funds

Monthly reports on protocol funding, spending and locked balances for the O(1) Network Fund and Parano1d Lab.

## Funds

**O(1) Network Fund** finances operation, maintenance, security and adoption of the live network.

```text
o1r3djxaz54k47kr54x76cwqkhl6xqucescv943m5m8uvc5w6x7euqct3h07
```

**Parano1d Lab** supports the founders, core developers, researchers and contributors advancing the protocol.

```text
o1xcjdp3udp5sgwcvnmjlu9s53u4fx5m3hpquvg0uem2pr2mrr9dqq38jple
```

These addresses receive the protocol allocations.

## Protocol funding

Parano1d launched on 21 August 2026 with no premine. During the original three 365-day target-time years from genesis, the block subsidy is allocated as follows:

| Recipient | Share |
| --- | ---: |
| Miners | 90% |
| O(1) Network Fund | 5% |
| Parano1d Lab | 5% |

The protocol pays both funds automatically every 2,880 blocks, approximately once a day at the 30-second target.

| Payout-block height | Gross subsidy per block | Each fund per full payout |
| --- | ---: | ---: |
| 210,537–1,261,736 | 16 NOID | 2,304 NOID |
| 1,261,737–2,312,936 | 11.30 NOID | 1,627.20 NOID |
| 2,312,937–3,223,778 | 8 NOID | 1,152 NOID |

Each payout uses the subsidy tier at its payout block. The allocation ends at block **3,223,778**, which settles the final partial payout period. All subsequent block subsidies go to miners. Transaction fees, after the State-growth burn, are miner-claimable.

The first report includes the earlier allocation schedule. The full issuance schedule and payout rules are documented in [network economics](https://docs.parano1d.org/protocol/economics). Fund recipients and payout calculations are defined in the [protocol source](https://github.com/ignotusnemo/parano1d/blob/5302b3f303f1b26e0a6a3de6f6d15aad7b3161ea/noid_chain/src/consensus/development_allocation.rs).

## Reports

Reports record protocol receipts, spending, fund balances and any active locks. Moving funds into a vault keeps them in the fund; the transaction fee is an expense.

| Date | Period |
| --- | --- |
| [16 October 2026](reports/2026-10-16.md) | Launch on 21 August through 16 October 2026 |
