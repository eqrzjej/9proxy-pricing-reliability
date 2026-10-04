# 9proxy review: Per-IP vs per-GB pricing, the outage record, and how to buy without tying up your budget

Most people searching for a 9proxy review are not comparing proxies in the abstract. They saw a provider quoting $0.015 per IP, noticed that is a small fraction of what Bright Data or Oxylabs charge, and now want two answers: does this actually work, and where is the catch?

The catch is not the IP quality. It is the 2026 reliability record and a wallet that does not give money back. Both are documented, and both should shape how much you deposit. Here is what the service sells, what it costs after the June price change, what happened during the blackouts, and who should still consider it.

## What 9Proxy actually sells

9Proxy is a residential proxy provider. Its pool is advertised at 20M+ residential IPs across 90+ countries, with targeting down to country, state, city, ZIP code and ISP, over HTTP/HTTPS and SOCKS5. Those two protocols matter more than they sound: SOCKS5 with `host:port:user:pass` is what anti-detect browsers, proxychains, and most scraper scripts expect by default.

The pricing split is where the product gets interesting, because the two models work in completely different ways.

**Residential Proxies by IP.** You buy a block of IPs. Bandwidth per IP is unlimited, and unused IPs never expire. Individual IPs stay alive for a few hours up to roughly 24 hours. You drive this model through the 9Proxy desktop app, which forwards local ports, plus an optional Auto-Rotation feature that swaps IPs on selected ports at intervals you set.

**Residential Proxies by GB.** You buy traffic and generate as many endpoints as you want from the dashboard. No app required. Authenticate with username/password or by whitelisting your own IP. Sessions can be sticky (hold an IP for X minutes) or rotating (new IP per request).

The IP model is permanent stock; the GB model is consumable fuel. That difference decides everything downstream, including how much risk you carry if the service goes dark.

> If you cannot describe your workload in either "how many identities do I need" or "how many gigabytes will I burn", you will buy the wrong plan here. Fixed-session work (logged-in accounts, browser profiles, checkout flows) is per-IP work. Broad collection across many targets is per-GB work.

## 9Proxy pricing: everything currently on the price list

9Proxy ran its first price increase on June 1, 2026, raising IP-based packages and bundles by roughly 20%. GB-based packages were explicitly left untouched. The numbers below reflect that split: IP and bundle figures are post-adjustment, GB figures are unchanged.

### IP-based packages (unlimited bandwidth per IP, IPs never expire)

| Package | Price per IP | Total | Billing unit | Buy |
| --- | --- | --- | --- | --- |
| 100 IPs | $0.24 | $24 | One-time block | Get the 100 IP package |
| 500 IPs | $0.144 | $72 | One-time block | Get the 500 IP package |
| 1,000 IPs + 500 bonus IPs | $0.084 | $126 | One-time block | Get the 1,500 IP package |
| 100,000 IPs | $0.023 | $2,300 | One-time block | Get a commercial IP block |
| 500,000 IPs | ~$0.017 | $8,625 | One-time block | Get a 500,000 IP block |

The middle of this ladder (2,500 / 5,000 / 15,000 / 25,000 / 50,000 IPs) is still sold, but those tiers changed on June 1 too. Before the adjustment they ran $175 / $300 / $600 / $750 / $1,250, and the 1,000+500 tier moved from $105 to $126, so treat the old numbers as history, not as a quote.

### GB-based packages (180-day validity)

| Package | Price per GB | Total | Buy |
| --- | --- | --- | --- |
| 5 GB | $3.00 | $15 | Start with 5 GB |
| 50 GB + 5 GB bonus | $2.10 | $105 | Get 55 GB |
| 100 GB | $1.50 | $150 | Get 100 GB |
| 200 GB | $1.00 | $200 | Get 200 GB |
| 1,000 GB | $0.80 | $800 | Get 1,000 GB |
| 2,000 GB | $0.75 | $1,500 | Get 2,000 GB |

### Enterprise GB packages (traffic never expires)

| Package | Price per GB | Total | Buy |
| --- | --- | --- | --- |
| 3,000 GB | $0.72 | $2,160 | Get 3,000 GB Enterprise |
| 6,000 GB | $0.70 | $4,200 | Get 6,000 GB Enterprise |
| 10,000 GB | $0.68 | $6,800 | Get 10,000 GB Enterprise |

Enterprise also unlocks team mode: one owner plus up to five members, shared bandwidth that does not expire inside the team, per-member traffic controls, and activity logs.

### Bundle packages (IPs plus GB in one purchase)

| Bundle | Contents | Price | Buy |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | Get the Starter bundle |
| Growth | 1,500 IPs + 50 GB | $180 | Get the Growth bundle |
| Pro | 5,000 IPs + 500 GB | $720 | Get the Pro bundle |

Bundled traffic is valid 180 days. Bundles rose 20% in the June adjustment, from $25 / $150 / $600.

## Reading the price ladder honestly

The "$0.015 per IP" and "$0.68 per GB" figures on the homepage are the top of each ladder. $0.015/IP is the 500,000-IP rate. $0.68/GB is the 10,000 GB rate. At the entry end you pay 14 to 16 times more per unit: $0.24 per IP for 100 IPs, $3.00 per GB for 5 GB.

That is not a bait-and-switch, it is just volume pricing, and every residential provider does it. The practical consequence is that 9Proxy's entry pricing is competitive but not remarkable, while its high-volume pricing is genuinely low for residential IPs.

Two structural details are worth more than a few cents per unit:

- **Per-IP bandwidth is unlimited.** If you pull 2 MB pages all day, the cost does not move. Providers that bill purely by GB punish exactly that workload.
- **IP blocks do not expire.** You buy 500 IPs, use 200 this month, and 300 are still there next quarter. Monthly subscriptions to rotating pools do not work that way.

## The reliability record you have to weigh

This is the part most affiliate reviews soften, and it is the part that decides whether 9Proxy is a good deal for you.

**June 28, 2026:** the website stopped loading, the desktop app timed out, active sessions dropped, and prepaid balances became unusable. Support went quiet. Users reported the same three failures across Lagos, Washington, Nairobi, Frankfurt and Moscow.

**June 29, 2026:** the company posted the same notice to its Facebook page and its BlackHatWorld seller account, describing a service disruption and saying it was "focused on a stable and secure recovery rather than a rushed fix." No cause, no restoration time.

**Mid-July 2026:** the site came back after roughly two and a half weeks. Balances were inaccessible throughout, and no root cause was published.

**August 2026:** a reseller-side update reported that GB traffic plans were working again while IP-based plans remained in maintenance. The same report flagged it as a second interruption.

**September 2026:** uptime logs show short gaps on September 7 and September 12, with the site reachable again from September 13.

One thing the outage was *not*, based on the registry records: a law enforcement seizure. The domain kept its usual registrar lock and Cloudflare nameservers, and no agency named the company. Seized proxy networks look different at the registry level, and this one did not. Public review sentiment also reads as noisy rather than uniformly negative, with Trustpilot scores quoted across write-ups ranging from 1.8 to 4.6 out of 5. Treat any single score with suspicion and read the recent entries yourself.

What this means in practice: when 9Proxy is running, it issues real, working residential IPs. The risk is availability, and the company has not explained what caused the blackouts. Two interruptions in one summer is a pattern, not bad luck.

## Refunds, replacements, and the wallet rules

Read this before you top up, because it is where the outage risk turns into money risk.

- **All sales are final.** The refund policy states that purchases and wallet deposits are non-refundable, with no exceptions.
- **Wallet funds are non-withdrawable.** Money you put into the 9Proxy Wallet can only be spent inside 9Proxy. It does not expire as long as your account is active, but it cannot come back out.
- **The remedy for a dead IP is a replacement, not a refund.** If a proxy fails within 60 seconds of first use, report it, check the Today List, and you get an automatic replacement.
- **The Today List saves real money.** IPs used in the past 24 hours can be reused free, which cuts waste on short test runs and abandoned sessions.

The practical rule that follows: buy the smallest package that covers your next two weeks, then scale. Depositing $500 into a wallet you cannot withdraw from, in order to earn a volume rate, is a bet on uptime you have no way to enforce. Auto-Refresh on critical jobs helps, since it swaps out offline IPs automatically, but it does not help when the whole network is down.

## Independent test results

Third-party numbers on 9Proxy are thin but not empty. A Geekflare test ran 300 sequential requests through rotating residential IPs against a major e-commerce site behind Cloudflare, and reported 293 successful passes (97.7%), 5 CAPTCHA challenges (1.7%), 2 hard blocks (0.6%), and an average response time of 0.63 seconds. The CAPTCHAs clustered in one IP range, which is normal for residential pools and cleared on rotation.

Other write-ups report success rates around 99% and response times in the 0.6 to 1.3 second range on US and EU routes. 9Proxy itself advertises 99.95% uptime, which the mid-2026 events plainly do not support as a service-level number. Use the independent test as the realistic baseline: mid-to-high 90s success on hard targets, sub-second responses when the network is healthy.

## How to get started, step by step

1. **Create an account.** Registering through a referral link applies the affiliate program's 5% discount for the new user. 👉 Create a 9Proxy account and pick a package
2. **Pick a model before a size.** Logged-in sessions and browser profiles go on per-IP. Bursty scraping, SERP checks and ad verification go on per-GB.
3. **Set up access.** For per-IP, install the desktop app (Windows client; a macOS build has been available) and forward ports, or use Proxy2Web for a browser-only check with standard credential auth. For per-GB, open the dashboard's Proxy Generator, pick country/state/city/ZIP/ISP, choose sticky or rotating, and export endpoints as `.txt` or `.csv`.
4. **Test before you scale.** Run a handful of requests against your actual targets and confirm the geo matches what you ordered. Anything broken in the first 60 seconds gets replaced.

Integration is straightforward: native SOCKS5 works with AdsPower, Dolphin Anty, Multilogin, BitBrowser, proxychains and plain Python, using the same credentials any other provider would issue. Payment options include cards, crypto (USDT, BTC, ETH, LTC, DOGE and others), and region-specific local methods.

## Discounts: what is actually available

There is no public promo code sitting on 9Proxy's homepage, and the older ones are dead. The April 2026 GB sale issued a personal 9% coupon that expired June 30, 2026, and the Lunar New Year code `LNY2026` took 8% off regular IP and GB packages before that campaign closed in February.

What does still apply:

- **5% off for referred sign-ups**, which is part of the affiliate program alongside lifetime commissions for the referrer.
- **5% extra IPs when you pay in crypto**, per partner documentation.
- **Account-issued coupons.** 9Proxy's pattern is to drop codes into Dashboard → My Account → My Coupons rather than publish them broadly, so it is worth checking there before every larger order.

There is no confirmed free trial. The honest low-risk test is a $15 / 5 GB pack or a $24 / 100 IP pack, not a "try before you buy" program that does not exist.

## Who should buy 9Proxy, and who should not

**It fits if:** you run multi-accounting or anti-detect browser workflows where each profile needs a stable IP and unlimited bandwidth; you scrape at moderate volume across many targets and can tolerate occasionally swapping a blocked IP; budget is a first-order constraint; and you can keep a second, funded provider on standby.

**Look elsewhere if:** you need a service-level agreement, compliance paperwork or enterprise invoicing; your pipelines cannot survive a two-week outage; or you want a refund path. A provider that has gone dark twice in one summer and sells non-refundable, non-withdrawable balance is not the place to park a large prepayment.

## FAQ

**Is 9Proxy a scam?**
No. The domain has been registered since 2014, the company publishes refund and payment policies, and third-party tests show real residential IPs working against hardened targets. The risk is uptime and refund terms, not fake proxies.

**Is 9Proxy down right now?**
Uptime monitoring shows the site reachable in mid-September 2026 after two short gaps in early September. Status changes fast, so check before paying and keep a fallback running if your work is time-sensitive.

**Can I get a refund if it breaks?**
Per 9Proxy's own policy, no. All purchases and wallet deposits are final. The only remedy is automatic replacement of an IP that fails within 60 seconds of allocation.

**Which plan is better for scraping?**
Rotating collection across many pages is cheaper per unit on GB packages. Work that depends on a session surviving, such as logged-in accounts, belongs on IP-based packages with unlimited bandwidth.

**Does it work with anti-detect browsers?**
Yes. SOCKS5 and HTTP with username/password authentication is the standard configuration for AdsPower, Dolphin Anty, Multilin and similar tools, and no extra integration is needed.

## Bottom line

9Proxy's pitch holds up on paper: residential IPs from $0.015 at volume, unlimited bandwidth on IP-based plans, blocks that never expire, city and ISP-level targeting, and a 20M+ pool. If your workload is multi-account sessions or mid-volume scraping and you value cost predictability, the per-IP model remains one of the cheaper ways to run it.

The caveats are specific and documented. IP and bundle prices went up around 20% on June 1, 2026. The service went dark for about two and a half weeks from June 28, returned, and has wobbled since. Refunds do not exist. So buy small, keep the balance lean, verify your targets in the first 60 seconds, and do not treat the wallet as a savings account.

👉 Check the current per-IP and per-GB prices and start with the smallest package that fits your next project
