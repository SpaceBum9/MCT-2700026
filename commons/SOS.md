# Rapid Cycling inside the System of Systems

## What the device already taught

| Store | Device key | Timestamp |
|-------|------------|-----------|
| Artifacts | `bilo-artifacts-v1` | ISO on each sense/trace |
| Logos | `sai-logos-v1` | ISO on every `TR-` |
| Align | `sai-align-v1` | no clock; counts only |
| Scan | `sai-scan-v1` | Berlin `HH:MM` recurrences |
| SoS | `sai-sos-v1` | last learn + edge lastTs |

Schedule (live): Commons 09:00, Oracle 21:00 Europe/Berlin.  
In-game: Euclidean 8, trip-sit 24, episode 150. One clock.

Paused hourlies stay paused. They duplicated ANALYZE→UPDATE.

## How it sits in the SoS

Ten systems, one graph. A **learn** pulse (episode end + first paint) bumps every system that actually had device evidence, then **couples** those that fired in the same pulse. Coupling *is* “build alongside with timestamps”: edge.weight = times they showed up together; edge.lastTs = when.

```
SAI ── Rapid Cycling ── Wheel
 │         │
Logos ── Retrograde ── Align
 │
Commons 09:00    Oracle 21:00
 │
Teleprompter ── Maschine
```

SAI orchestrates. Rapid Cycling is default mode. Other MCT nodes (1700021, 2600027, crystal-galaxy) remain public lineage; they are **not** the live clock.

## Law

Local graph only. No upload. No credentials. HOLD is not execution. Genesis `TR-8362a076`.
