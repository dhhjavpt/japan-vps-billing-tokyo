# Cheap Japan VPS: Why a 30 Mbps Plan and a 1 Gbps Plan Both Count as Tokyo, How Billing Cycles Hide the Real Cost, and Whether You Need a Native Japanese IP

Japan VPS pricing starts around $3.83/mo when you pay a year up front for 768 MB of RAM and a 30 Mbps port, and it runs past €31.99/mo for unmetered traffic on a gigabit uplink. That is a 14x spread for the same country label. Port speed, monthly traffic allowance and how the IP is registered explain the difference; CPU cores do not.

Below are LightLayer's Tokyo plans with the numbers its order page actually shows, the arithmetic on how much a 20 Mbps port moves in a month, where annual billing hides the real cost at four other providers, and the question most buyers skip: is the "Japan" in a Japan VPS a location, or a Japanese IP?

> For a proxy, a Telegram bot, a small site or a game relay for a dozen players, LightLayer's Tokyo **TYO-VG02** is the practical starting point: 1 vCPU, 1 GB RAM, 50 GB SSD and a 20 Mbps unmetered port at **$9.00/mo** recurring as the order configurator displays it. 👉 [Check the TYO-VG02 configuration and current recurring total](https://account.lightlayer.net/?affid=74)

## The Tokyo plans and what the order page charges

LightLayer builds one hardware shape and changes the network around it: 1 vCPU, 1 GB RAM, 50 GB SSD, one IPv4. Region, route class and port speed are the entire product decision. In Tokyo the configurator lists two plans.

| Plan | vCPU / RAM / Storage | Port and traffic | IPv4 | Recurring price | Order |
| --- | --- | --- | --- | --- | --- |
| TYO-VG02 | 1 vCPU / 1 GB / 50 GB SSD | 20 Mbps, unmetered | 1 (non-native) | $9.00/mo | [Open TYO-VG02](https://account.lightlayer.net/?affid=74) |
| TYO-VG04 | 1 vCPU / 1 GB / 50 GB SSD | 30 Mbps, 1 TB | 1 (non-native) | $9.00/mo | [Open TYO-VG04](https://account.lightlayer.net/?affid=74) |

Those are the recurring totals the configurator displays, with the billing cycle selector on the same page. The wider catalogue is much cheaper per month and much narrower per port: roughly 80 plans worldwide, and thirteen of them share a **$24.99/yr** tag while their ports run from 5 Mbps in Taiwan to 200 Mbps unmetered in Los Angeles. Monthly entry in Los Angeles is $4.00. Tokyo costs more because Tokyo is the thing you came for.

## What 20 Mbps actually moves in a month

A 20 Mbps port saturated for 30 days moves about 2.5 MB/s, which works out to roughly **6.4 TB**. The 30 Mbps plan carries a 1 TB monthly allowance, and 1 TB at 3.75 MB/s disappears in about three days of full-rate traffic. So TYO-VG02 hands you more usable volume than TYO-VG04 unless you specifically need the extra burst and stay under a terabyte.

The same trade-off runs through every cheap Japan VPS listing, just with different numbers. HostDare caps JSSD0 at 30 Mbps and 250 GB/mo. JUSTG fixes the port at 500 Mbps but meters 500 GB up to 6 TB by plan. KernelHost sells unmetered traffic at up to 1 Gbps. LightNode meters 1 to 4 TB across four tiers without publishing a port figure. A 20 Mbps unmetered port handles a proxy, a small WordPress site, an API backend or a Minecraft relay. It will not handle relaying video or seeding large files, and no amount of extra RAM fixes that.

LightLayer is not the cheapest RAM per dollar in Tokyo. It is the cheapest way in this set to get an unmetered port at a Japanese location on a monthly basis, and 6.4 TB of theoretical throughput at HostDare's or JUSTG's metered rates would cost several times $9.

## Annual prices and monthly prices are different products

HostDare's first three Japan plans are annual only. JSSD0 is $45.99/yr, JSSD1 $95.99/yr, JSSD2 $120.99/yr, and the monthly column does not begin until JSSD3 at $45.99/mo. The famous $3.83/mo is a 12-month commitment on 768 MB of RAM, and there is no month-to-month version of it.

JUSTG publishes both cycles and the gap is large. The 1 core / 512 MB plan is $19.99/mo or $119.99/yr, exactly half the monthly total. The 4 core / 4 GB plan is $49.99/mo or $499.99/yr, a $99.89 saving. KernelHost bills in euros, prepaid, with no contract and no minimum term, so its price is a price rather than a promotion.

LightLayer's terms state that price changes apply to new orders only, not to services already running, which means the rate you sign up at is the rate you renew at. Put that next to the $24.99/yr plans elsewhere in the catalogue and the annual figure is the one worth comparing across providers. Never put an annual price divided by twelve in the same column as a monthly price, because the commitment behind them is not the same thing. 👉 [See the Tokyo plans with the billing cycle selector](https://account.lightlayer.net/?affid=74)

## Tokyo datacenter or Japanese IP?

LightLayer labels its Tokyo IPv4 as non-native, on both plans, in the configurator. Taiwan, Hong Kong and Singapore get the same treatment; the Los Angeles plans are the native ones. No plan card lists IPv6.

That only matters if something reads the address. Latency for users in Tokyo, Seoul or Taipei does not care where the IP is registered. Account systems, app stores, ad platforms, streaming catalogues and some AI APIs do care.

JUSTG takes the opposite position and says so plainly: every Tokyo plan ships one native Japanese IPv4 plus IPv6, and the company reports that its own October 2026 test unlocked ChatGPT, Claude, Gemini, Netflix Japan and Disney+ from those addresses, with the caveat that third-party services can change their policies. KernelHost declines to promise anything, stating that each geolocation service applies its own rules when deciding which country an address belongs to.

Both are official positions and both are honest. If your workload is "hold a session that looks Japanese", pay for the native IP. If it is "serve users in East Asia with lower latency", the non-native address is not a problem, and the registration type is printed on the order page before you pay.

## Fine print that decides whether cheap stays cheap

LightLayer refunds only for faults attributable to the provider. There is no general refund window, and the abuse policy is priced: $20 to $50 per incident per IP, with the instance suspended on the first complaint and 6 hours to respond. Blocked or spam-flagged addresses are not replaced. The brand is also young and public third-party discussion is thin, so keep a backup somewhere else.

HostDare offers a 3-day refund with $0.50 to $1 deducted, and can decline the request if you used 20% or more of the monthly bandwidth. Windows works there but you supply the licence, and JSSD3 or higher is recommended.

KernelHost's Edge line ships without Windows and without IPv6, so a Windows workload rules it out entirely.

JUSTG lets you move a VPS between Tokyo, Seoul and Moscow once every 30 days, and the move issues a new IP while deleting the old server. Anything pinned to that address, a whitelist or a login bound to the IP, breaks on migration.

## Five providers side by side

| Provider (location) | Entry price | Entry specification | Port and traffic | Main catch |
| --- | --- | --- | --- | --- |
| LightLayer (Tokyo) | $9.00/mo | 1 vCPU / 1 GB / 50 GB SSD | 20 Mbps, unmetered | Non-native IP, no IPv6, no general refunds |
| HostDare (Osaka) | $45.99/yr (~$3.83/mo) | 1 core / 768 MB / 10 GB NVMe | 30 Mbps, 250 GB/mo | Annual only at entry; conditional refunds |
| LightNode (Tokyo) | $7.71/mo | 1 vCPU / 2 GB / 50 GB NVMe | 1 TB, port speed not published | Traffic tiers stop at 1 TB |
| JUSTG (Tokyo) | $19.99/mo | 1 core / 512 MB / 10 GB | 500 Mbps, 500 GB/mo | Highest entry cost here |
| KernelHost (Tokyo) | from €31.99/mo | 1 vCPU / 2 GB (Edge KVM) | Up to 1 Gbps, unmetered | No Windows or IPv6 on Edge; EUR billing |

## Pick by workload, then check three things

Lowest possible monthly cost for an always-on box: HostDare JSSD0 at $45.99/yr, if 768 MB of RAM and a 30 Mbps port cover the job and you accept annual billing. Most RAM per dollar on a metered plan: LightNode's $7.71 Start with 2 GB and 1 TB. A documented native Japanese IP: JUSTG from $19.99/mo. High-concurrency streaming with unmetered traffic: KernelHost from €31.99/mo, in euros, without Windows.

For a Tokyo box with an unmetered port, a flat renewal and a $9 monthly entry, LightLayer's TYO-VG02 is the one that fits, and the 6.4 TB of theoretical throughput is what the other four charge for by the terabyte.

Before you pay, confirm four things on the order page: the billing cycle and the renewal price attached to it, whether the IPv4 is native or non-native, whether IPv6 and Windows are included, and which limit your workload hits first, the port speed or the monthly allowance.

👉 [Start with the TYO-VG02 in Tokyo and confirm the recurring total before checkout](https://account.lightlayer.net/?affid=74)
