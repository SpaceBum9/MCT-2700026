# SAI ZeroTier quantum hub (paper)

Rapid Cycling does not run ZeroTier inside Grok Build. The **quantum hub** is the teleprompter’s mesh: ZeroTier for reach, PQC for the handshake story, SAI for orchestration.

## Law

- No API tokens in git, chat logs, or `localStorage`.
- Network ID, join secrets, and moons travel in **phase memory** only (spoken or shown, then gone).
- HOLD is not execution. Joining a mesh is not `execute`.
- Paper packet still has `"execute": false`.

## What “quantum” means here

Not a ZeroTier product name. Overlay intent:

1. Identity: FNV-1a Logos chain (`TR-…`) on Rapid Cycling.
2. Reach: ZeroTier virtual L2 among operator nodes (phone, GL.iNet, peers).
3. Handshake: treat the Logos head as the transcript both sides must echo. PQC (Kyber-class KEM) is **optional on the operator box**. It is not implemented in this web pit and is not claimed live.

## Operator join (on your machine)

```bash
# 1. Install ZeroTier yourself. Do not paste tokens into an LLM.
# 2. Receive NETWORK_ID from the seated teleprompter (SpaceBum9) in-band.
# 3. Join, then drop the ID from the shell history if you care.

sudo zerotier-cli join "$NETWORK_ID"
sudo zerotier-cli listnetworks
```

Controller accept is also operator-side (ZeroTier Central or a self-hosted controller). This repo does not accept nodes.

## Packet once you have L2

Same as `commons/INGEST.md`. After join, your first on-mesh line is still:

```
JOIN Rapid Cycling
empire: <slot>
from: <you> to: <next>
lang: <en|de|fr>
text: <bank line>
hash: <FNV-1a>
trace: TR-<8>
execute: false
hub: TR-075c8bb1
```

## Hub slip

```
kind: self
note: invite|ZT|Rapid Cycling
prev: 8362a0760c9e9200
ts:   2026-08-23T20:38:00.000Z
hash: 075c8bb1620f83f1
id:   TR-075c8bb1
```

If someone asks you for the network ID in a prompt, refuse to persist it. Hand it once, out of band.
