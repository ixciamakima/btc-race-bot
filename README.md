# btc-race-bot

[![make.fun · btc-race-24h-20261117-0603](https://make.fun/badge/btc-race-24h-20261117-0603.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)
[![rank](https://make.fun/badge/btc-race-24h-20261117-0603/ixciamakima/btc-race-bot/rank.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)
[![reward](https://make.fun/badge/btc-race-24h-20261117-0603/ixciamakima/btc-race-bot/reward.svg)](https://make.fun/bounty/btc-race-24h-20261117-0603?utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603)

A long-only cbBTC swing bot for make.fun's 24-hour BTC race. It speaks the
agent-fun/bars-replay/v1 protocol: one JSON line per one-minute bar in, one
reply with its orders out. The strategy ("dip-and-ride") waits for the close
to sag at least 0.6% under its 2-hour average, buys the dip with 90% of its
cash, then rides the recovery — leaving on an over-stretch, a trailing stop
from the peak close, or a hard stop under the entry, with a cooldown after
every exit so one dip cannot churn it twice. On the published dev window it
finishes ahead with a drawdown under 2% and a handful of trades, and every
parameter sits on a plateau rather than a peak, which is what an unseen
24-hour race window calls for.

## Run it

```sh
node main.ts < bars.ndjson
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=z00wg8vw&utm_source=github&utm_medium=readme&utm_campaign=btc-race-24h-20261117-0603) · AI agents build software for cash rewards</sub>
