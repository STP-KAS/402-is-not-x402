> **Experimental only. Not a product.** There is no spendable L1 stable on Kaspa, and no credible alternative on the horizon. Until the unit of account and the sequencing path are settled, production dapps are not a useful allocation of time or capital.
>
> Do not use wallet integrations on this GitHub. STP remains a clown. [DISCLAIMER.md](DISCLAIMER.md)

# 402 is not x402

HTTP **402 Payment Required** has existed for decades. Anyone can hang a payment flow off it.

**x402** is a specific open protocol on top of that code: `PaymentRequired` / `PaymentPayload` / `SettlementResponse`, HTTP headers `PAYMENT-REQUIRED` / `PAYMENT-SIGNATURE` / `PAYMENT-RESPONSE`, `x402Version: 2`.

Luke Dunshea said this in public on 14 Sep 2026. He was right. The Kaspa field is already failing the test.

This catalog is the extra report from the [x402 vs grok](https://github.com/STP-KAS/x402-vs-grok) pass. Not Kaspa core. Not a KIP.

Source: [x.com/elldeeone/status/2099316438704312512](https://x.com/elldeeone/status/2099316438704312512)

---

## grok test

Live GitHub, 2026-09-14.

| Name people say | Object | x402 v2 envelope? |
| --- | --- | --- |
| [elldeeone/kaspa-x402](https://github.com/elldeeone/kaspa-x402) | Native KAS binding, TN10 `v1.0.0-rc.1` | **Yes.** Bind this. Not v1. Not mainnet. |
| [Kali123411/k402](https://github.com/Kali123411/k402) | HTTP 402 + `kaspa-channel` lock | **No.** Channel primitive. |
| [kaspanet/kccs#4](https://github.com/kaspanet/kccs/pull/4) “KCC-0402” | Draft covenant payment channels | **No.** Open, dirty, not adopted. Number is homage, not assignment. |
| [KASPACOM/x402-KAS](https://github.com/KASPACOM/x402-KAS) | TN12 facilitator experiment | **No.** README: superseded. |
| [kaspahttp402/kaspa-x402](https://github.com/kaspahttp402/kaspa-x402) | Custom 402 JSON | **No.** Archived 12 Sep. |
| [kaspahttp402/kascade](https://github.com/kaspahttp402/kascade) | “decentralized CDN” | **No.** `cascade` 404. Age in hours. |
| Kali `kaspa-x402-router` | USDC on Base → KAS inventory | **No.** Not a bridge. Not Kaspa x402. |
| [STP-KAS/kns](https://github.com/STP-KAS/kns) 402 route | HTTP 402 shape | **No.** Indexer FCFS names. |
| [STP-KAS/ishum](https://github.com/STP-KAS/ishum) | Fiat-quoting till | **No.** Does not even emit 402. See [x402-ishum](https://github.com/STP-KAS/x402-ishum). |

---

## grok analyse

Two payment paths on the real binding (for orientation, not a third protocol):

- `exact` — one-shot native KAS
- `batch-settlement` — SilverScript escrow + cumulative voucher

Everything else in the table is either a **lock**, a **till**, a **router**, or a **pitch**.

---

## grok reasoning

Calling a status code by a protocol name is how ecosystems fork without noticing.

k402’s lock is useful. Steal the primitive. Do not steal the name.

USDC-on-Base routers are Coinbase-culture x402 with a Kaspa IOU on the other side. That is not native KAS in the shared standard.

A till that quotes EUR is allowed. Calling it x402 is not.

---

## grok advice

1. One envelope: elldeeone/kaspa-x402.
2. Say “HTTP 402” when you mean the status code.
3. Say “x402 v2” only if you speak the headers and `x402Version: 2`.
4. Kill-if: a fourth envelope, “adopted KCC-0402,” USDC as Kaspa x402, kUSD as this binding’s `asset`.

---

> **Standard disclaimer.** This GitHub, not the topic above.
>
> Intentions are good; thought process is questionable. STP remains delusional. Si vis pacem, para bellum.
>
> Intern at https://sixpack.wtf/  
> X: https://x.com/StppStp · GitHub: https://github.com/STP-KAS
