## Versions

anchor-cli 1.1.2
solana-cli 3.1.10
node v24.10.0
@codama/cli 1.6.3
@codama/renderers-js 2.5.0
@solana/kit 8.3.0

## TODO 3

Required: fundraiser, vault.

Optional: contributorAccount, contributorAta, tokenProgram, systemProgram.

Codama can derive contributorAccount from the available inputs and its PDA seeds. It can also derive contributorAta from the contributor and mint, while tokenProgram and systemProgram are fixed program addresses.

The fundraiser PDA is required in contribute because its seeds use `fundraiser.maker`, which is a field inside the account being derived. In initialize, the fundraiser PDA uses the caller-provided `maker` account, so Codama can derive it.

## Bonus

Not attempted.

## One thing that surprised me

Codama generated a client that could decode account data and produce the same instruction bytes and account order as the Anchor client.