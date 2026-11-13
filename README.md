# Almaty VPS: What It Costs, Which Plan You Actually Need, and Is $1.77/mo Enough? (JustHost's Full Plan Table and the Real Annual Bill)

Searching for an Almaty VPS turns up quotes from roughly $5.94 to $29 per month among providers that publish an Almaty data center. JustHost prices below that band, with its entry VPS at **$1.77/mo on 12-month billing** and $2.21 month-to-month. One caveat up front: JustHost's plan list gives you specs and price, not data center cities, so if the server physically sitting in Almaty is the whole point, confirm the location with support before you pay. Below is every plan JustHost currently lists, what each tier actually handles, what twelve months costs, and how the pricing lines up against the providers that do document an Almaty facility.

> **Quick pick:** For a small site, a scraper, a proxy endpoint, or a single app aimed at Central Asian users, take **Sirius: 1 core, 1 GB RAM, 20 GB NVMe, unmetered 300 Mbit fair-share port at $2.81/mo, or $2.25/mo on annual billing.** It costs 60 cents more than the entry plan and doubles both the disk and the port speed. 👉 [See JustHost's current VPS plans and prices](https://justhost.asia/en/services/vps/tariffs?ref=196392)

## Every JustHost VPS plan on the price list

JustHost splits its lineup into two groups: three discounted "special offer" plans that carry a three-month minimum order, and a KVM series that ships with both IPv4 and IPv6 addresses.

### Special offers (orders from 3 months)

| Plan | vCPU / RAM | NVMe | Port (fair-share) | Price | Order |
| --- | --- | --- | --- | --- | --- |
| New Star | 1 core / 1 GB | 10 GB | 100 Mbit (~31+ TB/mo) | $2.21/mo · **$1.77/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Double Star | 2 cores / 2 GB | 20 GB | 200 Mbit (~62+ TB/mo) | $4.11/mo · **$3.28/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Bright Star | 4 cores / 4 GB | 30 GB | 300 Mbit (~93+ TB/mo) | $5.68/mo · **$4.54/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |

### KVM series with IPv4 + IPv6

| Plan | vCPU / RAM | NVMe | Port (fair-share) | Price | Order |
| --- | --- | --- | --- | --- | --- |
| Sirius | 1 core / 1 GB | 20 GB | 300 Mbit (~93+ TB/mo) | $2.81/mo · **$2.25/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Arcturus | 1 core / 2 GB | 30 GB | 300 Mbit (~93+ TB/mo) | $4.01/mo · **$3.21/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Alpha Centauri | 2 cores / 2 GB | 40 GB | 400 Mbit (~124+ TB/mo) | $5.21/mo · **$4.17/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Vega | 2 cores / 4 GB | 80 GB | 500 Mbit (~155+ TB/mo) | $7.79/mo · **$6.23/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Capella | 4 cores / 4 GB | 120 GB | 750 Mbit (~232+ TB/mo) | $10.61/mo · **$8.49/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Rigel | 4 cores / 8 GB | 200 GB | 750 Mbit (~232+ TB/mo) | $16.20/mo · **$12.96/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Antares | 5 cores / 8 GB | 300 GB | 750 Mbit (~232+ TB/mo) | $19.20/mo · **$15.36/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |
| Betelgeuse | 6 cores / 12 GB | 400 GB | 750 Mbit (~232+ TB/mo) | $26.40/mo · **$21.12/mo** annual | [ Order](https://justhost.asia/en/services/vps/tariffs?ref=196392) |

The page also lists an 8-core / 16 GB / 500 GB Spica tier above Betelgeuse; check the live pricing page for its current rate. All plans run on NVMe, include DDoS filtering, and come with 24/7 support according to JustHost's own documentation.

## Which tier fits which job

**A static site or a brochure page with a tiny database.** New Star's 1 GB of RAM will hold, but 10 GB of NVMe is the binding constraint: a Linux install, a web server, and a couple of years of logs will crowd it. Sirius gives the same RAM and core count with double the disk and triple the port for 60 cents more. Take Sirius.

**One small web app, WordPress with a plugin stack, or a lightweight API.** Arcturus (2 GB / 30 GB, $4.01) is the tidy minimum. If PHP workers or Node processes start queueing, Alpha Centauri's second core for $1.20 more is the cheaper fix than migrating later.

**Docker with three or four containers, or the app and its database on one box.** Vega at $7.79 with 4 GB and 80 GB. 4 GB is roughly where MySQL or Postgres and the application stop competing for memory.

**A Minecraft or other game server.** Capella, 4 cores and 120 GB for $10.61. Game servers burn CPU on world ticks and chunk generation, so cores matter more than the RAM step you'd get by jumping to Rigel.

**The 4-core trap worth knowing about.** Bright Star and Capella have identical CPU and RAM (4 cores / 4 GB), but Capella costs $10.61 against $5.68 because it carries 120 GB instead of 30 GB. If your workload is CPU-bound and disk-light, Bright Star does the same compute for about half. Paying for Capella only makes sense when you'll actually use the storage.

**Stepping up from 8 GB.** Rigel is $16.20 and Antares is $19.20. The extra $3 buys one more core and another 100 GB of NVMe. That's a fair trade only if the disk gets used; otherwise Rigel covers the same 8 GB of RAM.

## What a year actually costs

The annual figure is a prepay discount, not a different product. Here's the spread on the plans most people shortlist:

| Plan | Monthly billing, 12 months | Annual prepay, 12 months | Saved |
| --- | --- | --- | --- |
| New Star | $26.52 | **$21.24** | $5.28 |
| Sirius | $33.72 | **$27.00** | $6.72 |
| Arcturus | $48.12 | **$38.52** | $9.60 |
| Vega | $93.48 | **$74.76** | $18.72 |
| Capella | $127.32 | **$101.88** | $25.44 |
| Rigel | $194.40 | **$155.52** | $38.88 |
| Betelgeuse | $316.80 | **$253.44** | $63.36 |

Two things the table doesn't show. First, the three "special offer" plans have a three-month minimum order, so the smallest first payment on New Star is $6.63, not $2.21. Second, a full year of New Star at $21.24 costs less than a single month of the cheapest 2-core plan from one of the Almaty-documented providers below. That gap is the strongest argument for JustHost, and also the reason to read the next section carefully. 👉 [Lock in the 12-month rate on any plan](https://justhost.asia/en/services/vps/tariffs?ref=196392)

## What "unmetered" and "fair-share" mean here

Every plan lists an unmetered port at 100 to 750 Mbit, with JustHost equating 100 Mbit to "31+ TB monthly" and 750 Mbit to "232+ TB." There's no hard traffic cap, but the port is shared rather than dedicated. For a website, an API, a bot, or a game server, that distinction never surfaces. For a seedbox or large file distribution, it does: providers advertising a dedicated 2 Gbps port will outperform a fair-share 100 Mbit port under sustained load, and that's part of what their higher price buys.

## The Almaty question you should settle first

JustHost's pricing page sells you a spec sheet and a price; data center cities aren't part of the plan names. If your project needs the server physically in Almaty, for a Kazakh IP, local search visibility, or latency to users in Kazakhstan, confirm with support before you pay that the Almaty location is selectable on the plan you've chosen. JustHost advertises 24/7 support, so this is a five-minute question, and it's better answered before the charge than after.

## How the Almaty-documented providers compare

These four all state an Almaty data center on their own pages. Prices and specs are as published; nothing here is a recommendation to move.

| Provider | Entry price | Entry specs | Almaty facility | Notes |
| --- | --- | --- | --- | --- |
| JustHost | $2.21/mo ($1.77 annual) | 1 core / 1 GB / 10 GB NVMe / 100 Mbit | Confirm with support | 3-month minimum on this tier |
| is\*hosting | $5.94/mo | 1 Xeon core / 1 GB / 20 GB SSD / 2 TB | Yes, Sairam Data Centre | TIER III Design and Facility certifications, free weekly backups, 6 tiers |
| Hostry | $7.00/mo | 1 vCPU / 1 GB / 20 GB NVMe | Yes | 12 tiers; traffic allowance not listed on the plan table |
| LightNode | $7.71/mo | 1 vCPU / 2 GB / 50 GB NVMe / 1 TB | Yes | Hourly billing, 99.95% uptime claim, delivery stated as within about a minute to a few minutes |
| AVANETCO | $29/mo | 2 cores / 2 GB / 40 GB SSD | Yes | 2 Gbps port, unmetered, 99.9% uptime, 1–3 hour activation; page marks prices updated 2026-10-04 |

The pattern: every provider that documents an Almaty rack starts between $5.94 and $29 for a comparable or smaller box, and several bundle extras JustHost doesn't mention, such as free weekly backups or hourly billing. JustHost wins clearly on price and loses the "published Almaty address" argument until you confirm the location yourself.

## FAQ

**Is $1.77/mo the price I'll actually pay?** It's the 12-month prepay rate on New Star. Month-to-month is $2.21, and that tier requires a minimum three-month order, so the smallest first invoice is $6.63.

**Is the bandwidth really unlimited?** JustHost lists an unmetered port with a fair-share speed cap (100 Mbit on New Star up to 750 Mbit on the larger plans) and equates those to 31+ TB and 232+ TB per month. No hard cap, but the port is shared.

**Do I get a dedicated IP?** The KVM series is sold with IPv4 and IPv6 addresses included, per the pricing page.

**What happens if I want a refund?** JustHost maintains a refund and cancellation policy, revised October 7, 2026. It states that refunds on ordinary withdrawal are processed within 10 calendar days of the request and are returned through the original payment channel, with deductions allowed only for documented, actually incurred expenses. The policy doesn't advertise a standalone headline money-back window, so read the clause that applies to your order before paying. 👉 [Read the current plans and refund terms](https://justhost.asia/en/services/vps/tariffs?ref=196392)

**Is DDoS protection included or extra?** Included. JustHost's FAQ describes built-in, multi-layered filtering on every VPS that monitors traffic and blocks attacks as they start.

**Can I run Windows?** JustHost's published plan information doesn't enumerate supported operating systems, so ask support before ordering if Windows is a requirement.

## The decision, in one pass

- Cheapest box that can still hold a small site: **Sirius, $2.25/mo annual**.
- One app plus its database, or a few Docker containers: **Vega, $6.23/mo annual**.
- CPU-bound game server: **Capella, $8.49/mo annual**, or Bright Star at $4.54 if disk isn't the issue.
- 8 GB of RAM or more: **Rigel, $12.96/mo annual**; Antares only if the extra 100 GB gets used.
- Almaty location is non-negotiable: confirm it's selectable on your plan before checkout. A $1.77 server three countries away doesn't solve the problem you came here with.

Two things to check before you enter payment details: whether you're on a three-month-minimum tier or a 12-month prepay, and whether the Almaty location appears for the plan you picked.

👉 [Pick your plan and confirm the Almaty location](https://justhost.asia/en/services/vps/tariffs?ref=196392)
