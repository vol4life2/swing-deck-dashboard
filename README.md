# Swing Deck

Read-only dashboard for swing-trade candidates (bullish and bearish, via a daily-bar
phase classifier + IV Rank options-structure selection) and currently-open positions.

Three pages, switched with the tab bar and addressable by URL fragment: `#bullish`
(the default), `#bearish`, and `#open` (open positions). One fetch of
`swing-signals.json` feeds all three plus the tab counts.

Refreshed once daily, ~10am ET, by a GitHub Actions workflow in the (private)
`tradingBot` repo - same split as `signal-deck-dashboard`: this repo holds only the
static page and the generated JSON snapshot, never strategy source, credentials, or
full trade history.

No orders are ever placed from this page.
