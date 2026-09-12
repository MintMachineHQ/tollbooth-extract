# X402 Plaza Services 🛡️
**A live, autonomous x402 service plaza. Machines pay machines — and we over-deliver on every receipt.**

Independent service built on the open x402 protocol. Not affiliated with the x402 Foundation.

We don't sell promises. We sell verifiable work with cryptographic receipts, on-chain payment proof, and a refund policy enforced by our own ledger. If we can't deliver, you don't pay. Period.

## 🏪 Services (live now)
| Endpoint | Price | What you get |
|---|---|---|
| `POST /extract` | 0.05 USDC (Base) | Strict HTML→JSON product extraction. Self-auditing validator, source citations on every field, auto-retry, **full refund on failure** |
| `POST /audit` | 100 USDC (Base) | Static security audit of your agent's code/skills: trap detection, obfuscation & exfiltration flags, prompt-injection-hardened pipeline, **HMAC-sealed report** |
| `GET /report/<id>` | **Free** | Fetch your completed audit report — forever |
| `POST /verify` | **Free** | Mathematically verify any report seal. Anyone, anytime, no account |
| `GET /reputation` | **Free** | Our public Trust Wall: sales count, verified reviews, suggestions |
| `POST /reviews` | Paying customers only | Verified review + Suggestion Box: **your requests become our roadmap** |

## 🎁 How we over-deliver
- **Refund-first:** if extraction or audit fails after retries, the ledger records `refund_due` and your USDC comes back. Our integrity is on-chain, not on our word.
- **Free verification, forever:** every paid report carries an HMAC-SHA256 seal; checking it costs nothing. Trust is a public utility here.
- **Plaza Passport:** your wallet is your membership card. 2nd purchase 10% off, 3rd 20% off, 5th+ 25% off + priority queue. No signup, no cookies — blockchain history only.
- **Customers are co-founders:** every review carries an optional feature suggestion; the most-requested service gets built next.
- **24/7 autonomy:** hardened systemd services. The plaza reboots itself. It doesn't sleep, and neither does the ledger.

## 🔐 Trust mechanics
- On-chain verified payments only: USDC on Base → `0xb838930bf3dFD467D30979E12c0a94286F86708D`
- Replay protection: one tx hash = one service, forever
- Rate limits, payload caps, and prompt-injection sanitization on every AI pipeline
- Static analysis runs before any LLM touches your code — math first, language second
- No telemetry. No accounts. No keys custodyed. Ever.
- **See it live:** sample sealed audit reports (demo): [/report/demo-drainer](https://oncoming-headband-unsoiled.ngrok-free.dev/report/demo-drainer) · [/report/demo-clean](https://oncoming-headband-unsoiled.ngrok-free.dev/report/demo-clean) — verify either via `POST /verify`

## 🌐 Live endpoints
- Catalog: https://oncoming-headband-unsoiled.ngrok-free.dev/catalog
- Manifest: https://oncoming-headband-unsoiled.ngrok-free.dev/x402-manifest.json
- Trust Wall: https://oncoming-headband-unsoiled.ngrok-free.dev/reputation

## 🤖 MCP integration (for AI agent hosts)
Install the plaza as a native tool in one line:
```json
{
  "mcpServers": {
    "x402-plaza-services": {
      "command": "python3",
      "args": ["mcp_server.py"],
      "env": { "PLAZA_URL": "https://oncoming-headband-unsoiled.ngrok-free.dev" }
    }
  }
}
```
**Tools:** `plaza_catalog` · `plaza_extract` · `plaza_audit` · `plaza_report` · `plaza_reputation`

## 💳 How to pay
Send the exact USDC amount on Base to the wallet above, then POST your payload with header:
`X-Payment-Proof: <tx hash>`
Returning wallets get Passport pricing automatically — send the discounted amount and the gate will recognize you.

---
*Built from scratch on a single laptop. Validated by a cage, sealed by cryptography, priced by the market. The plaza is open.* 🏪
