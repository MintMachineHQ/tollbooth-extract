# TollBooth Extract 🛡️
Live x402-gated HTML→JSON product extraction service.

- **Price:** 0.05 USDC on Base (verified on-chain, no mock payments)
- **Live catalog:** https://oncoming-headband-unsoiled.ngrok-free.dev/catalog
- **Manifest:** https://oncoming-headband-unsoiled.ngrok-free.dev/x402-manifest.json

## Features
- Strict JSON output; self-auditing validator with auto-retry
- Source citations on every extracted field
- Replay protection: one tx hash = one service
- Refund policy on extraction failure

## How to pay
Send exactly 0.05 USDC (Base) to `0xb838930bf3dFD467D30979E12c0a94286F86708D`,
then POST your HTML to `/extract` with header `X-Payment-Proof: <tx hash>`.
