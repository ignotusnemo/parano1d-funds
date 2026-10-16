# Verify voluntary fund locks

The funds choose to lock part of the protocol rewards they have already received in timelocked vaults.

**The protocol's three-year allocation period is the duration of reward payments to the funds. Each voluntary lock has its own unlock block, recorded in the monthly report.** New protocol payouts continue to the original fund addresses on the existing schedule.

Each confirmed lock is accompanied by a public contract file with its terms and a verified funding receipt. The corresponding monthly report links to the file and records the amount and unlock block.

## October 2026

Both vaults hold **500,000 NOID** each and unlock at block **490,000**, estimated around **16 January 2027**.

- [Download the O(1) Network Fund contract](https://raw.githubusercontent.com/ignotusnemo/parano1d-funds/main/proofs/2026-10/network-fund-vault.json).
- [Download the Parano1d Lab contract](https://raw.githubusercontent.com/ignotusnemo/parano1d-funds/main/proofs/2026-10/lab-fund-vault.json).

The [October report](../reports/2026-10-16.md#voluntary-locks) records both vault addresses and funding transactions. Each vault returns funds to its fund's original allocation address after unlock.

## In the wallet

1. Synchronize your Parano1d wallet with the network.
2. Download the contract file linked in the report.
3. Open **F7 → Open file**, select the file and inspect the verification result.
4. Check the funding receipt: the deposit is 500,000 NOID from the corresponding fund address into its reported vault.
5. Check the rules: a timelocked vault whose owner is the corresponding fund address and whose unlock block is 490,000. Before that block, the owner has no permitted withdrawal.
6. Add the contract to **My contracts** and check its current funded instances and balances. The sum of its live instances is the amount currently held in that vault.

The funding receipt establishes the deposit. Your node checks current State to establish how much remains in the vault when you inspect it. Keep the contract in My contracts to check it again later.

These files contain public contract data. Spending authority remains with the owner specified by the contract.

## Records for each lock

Each published lock includes:

| Record | Purpose |
| --- | --- |
| Contract file | Public terms and funding evidence, opened in F7 |
| Vault address | Identifies the contract receiving the deposit |
| Owner address | Identifies the authority allowed to withdraw after unlock |
| Funding transaction | Identifies the transfer from the fund address into the vault |
| Amount and unlock block | State what the report commits to |

Unlock dates are estimates from the block target. The contract enforces its block height.

See also [contracts in the GUI](https://docs.parano1d.org/contracts/gui) and [receipts and recovery](https://docs.parano1d.org/contracts/receipts-and-recovery).
