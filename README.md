# VPS Indonesia: Jakarta or Singapore, Which Evoxt Plan Fits Your Workload, and What Does It Cost Month by Month? (All 11 Plans Priced)

Evoxt runs a Jakarta node peered with JKT-IX, and its published plans start at **$2.99/month** for 512 MB and run to **$95.99/month** for 16 cores and 32 GB. For a site whose visitors are mostly in Indonesia, the sensible starting point is **VM-1 at $5.99/month**: 1 core, 2 GB RAM, 20 GB storage, 500 GB of monthly transfer.

The reason the word "Indonesia" matters in that paragraph is distance. A request served from a Jakarta data center reaches an Indonesian visitor in roughly **1–5 ms**. Served from Singapore it takes **15–30 ms**, and from the US **200 ms or more**. On a single page load nobody notices. Across a checkout flow, a dashboard, or a game server tick, the difference shows up.

Below is every plan Evoxt currently lists, what each one is actually good for, what the pricing structure quietly rewards, and the handful of things the pricing page doesn't tell you.

> **Quick pick:** Most readers land on **VM-1 ($5.99/month)** for a small site or API, or **VM-1.5 ($6.95/month)** if the workload benefits from a second core at the same 2 GB. Skip VM-0.5 and VM-0.75 unless you're running a bot or a jump box. 👉 [Start with VM-1 on the Evoxt console](https://bit.ly/EvoXt)

## All Evoxt plans, side by side

Evoxt's pricing page lists 11 configurations. All are on the same high-frequency CPU platform (up to 6.0 GHz per core per the official page), all include a free weekly offsite backup, and all bill monthly.

| Plan | CPU / RAM | Storage | Monthly transfer | Price | Order |
| --- | --- | --- | --- | --- | --- |
| VM-0.5 | 1 core / 512 MB | 5 GB | 250 GB | $2.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-0.75 | 1 core / 1 GB | 10 GB | 250 GB | $4.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-1 | 1 core / 2 GB | 20 GB | 500 GB | $5.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-1.5 | 2 cores / 2 GB | 20 GB | 500 GB | $6.95/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-2 | 2 cores / 4 GB | 30 GB | 1,000 GB | $11.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-3 | 4 cores / 4 GB | 30 GB | 1,000 GB | $14.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-4 | 4 cores / 8 GB | 60 GB | 2,000 GB | $23.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-6 | 8 cores / 8 GB | 60 GB | 2,000 GB | $29.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-8 | 8 cores / 16 GB | 80 GB | 3,000 GB | $47.99/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-12 | 16 cores / 16 GB | 80 GB | 3,000 GB | $60.95/mo | [ Deploy](https://bit.ly/EvoXt) |
| VM-16 | 16 cores / 32 GB | 100 GB | 5,000 GB | $95.99/mo | [ Deploy](https://bit.ly/EvoXt) |

Prices are in USD, billed monthly. Evoxt's FAQ states that billing periods run from monthly up to three years, and that you can top up account credit and let the system apply it to future invoices. The pricing page doesn't publish a prepay discount rate, so check the cart total at checkout rather than assuming one.

Evoxt also sells resource upgrades à la carte. You can add CPU, RAM or storage to an existing VM without moving to a different plan, which matters if you outgrow VM-1 by 1 GB of RAM rather than by a full tier.

## The pricing is linear, and that changes how you choose

Run the numbers per gigabyte of RAM and a pattern appears: from VM-1 upward, Evoxt charges almost exactly **$3 per GB of RAM per month**, regardless of plan size.

- VM-1: $5.99 ÷ 2 GB = $3.00
- VM-2: $11.99 ÷ 4 GB = $3.00
- VM-8: $47.99 ÷ 16 GB = $3.00
- VM-16: $95.99 ÷ 32 GB = $3.00

Two conclusions follow. First, buying a bigger plan does not get you a volume discount; VM-16 costs the same per gigabyte as VM-1. Second, the two smallest plans are the expensive ones per unit: VM-0.5 works out to $5.98 per GB and VM-0.75 to $4.99 per GB. If you need a full gigabyte of RAM, VM-0.75 makes sense only as a disposable utility box. For $1 more, VM-1 doubles the RAM, doubles the storage and doubles the transfer allowance.

The other pattern is that several plans hold RAM flat and add cores for a few dollars:

- VM-1 → VM-1.5: +$0.96 for a second core, same 2 GB, same 20 GB, same 500 GB.
- VM-2 → VM-3: +$3 for two more cores, same 4 GB.
- VM-4 → VM-6: +$6 for four more cores, same 8 GB.

That's the cheapest way to buy concurrency on this lineup. A single-core 2 GB box handles a low-traffic WordPress site fine; it struggles the moment PHP workers queue up behind each other. Paying $0.96 to stop that is a straightforward trade.

👉 [Compare VM-1 and VM-1.5 at the current price](https://bit.ly/EvoXt)

## What an Indonesian node actually buys you

Two separate things happen when your server sits in Jakarta instead of Singapore.

**Latency.** Domestic routing means the round trip stays inside Indonesia. The commonly cited figures for Jakarta-origin traffic are 1–5 ms to a local data center, 15–30 ms to Singapore, and 200 ms+ to the US. For a brochure site, that's invisible. For anything where a user waits on a response, it compounds: a WooCommerce checkout that fires a dozen sequential requests pays that gap a dozen times.

**Peering.** Evoxt's Jakarta region is described as connected to JKT-IX plus multiple Tier 1 providers. Direct connection to an Indonesian internet exchange means traffic from local ISPs is handed off domestically instead of being routed out through an international gateway and back. This affects more than raw milliseconds; it removes a class of path instability that shows up as inconsistent load times for users on smaller local ISPs.

One clarification worth keeping in mind when you compare providers: **data center tier ratings describe mechanical and electrical redundancy, not service uptime.** A Tier 3 facility is rated 99.982% for power and cooling (roughly 1.6 hours of disruption a year at most); Tier 4 is 99.995% (about 30 minutes). Evoxt separately advertises a 99.99% uptime commitment for its service. Those are different numbers measuring different things, and providers that advertise "Tier 3" in a headline are not promising you 99.982% availability of your VM.

A third-party review of the Jakarta node reports AMD EPYC 9004 hardware, KVM virtualization, NVMe in RAID10, an I/O figure around 2,300 MB/s, one IPv4 plus IPv6, and Windows Server 2012/2016/2022 among the available images. That's a single reviewer's test, not a lab benchmark, but it's consistent with Evoxt's own claims about high clock speeds.

**When Jakarta is the wrong call.** If your visitors are mostly in Europe or North America, a Jakarta node adds latency for them rather than removing it. Evoxt lists 17 regions, so the right move is to pick the region nearest your actual audience and treat Indonesia as one option among several, not a default.

## Matching a plan to what you're running

**A blog, docs site, or brochure site.** VM-1 at $5.99. One core, 2 GB, 20 GB of storage is enough for a static or lightly cached WordPress install, and the 500 GB transfer allowance covers a site doing tens of thousands of monthly page views with room to spare. Don't buy VM-2 "to be safe."

**WooCommerce, Laravel, or a small SaaS.** VM-1.5 at $6.95, or VM-2 at $11.99 if the database shares the box. The jump to VM-2 buys 4 GB of RAM and a second terabyte of transfer, which matters once you're running MySQL, Redis and PHP-FPM on one machine. Start on VM-1.5 and use à la carte upgrades if you need more memory before you need more disk.

**Always-on automation: n8n, LiteLLM, crawlers, scheduled jobs.** VM-2 at $11.99. These workloads are memory-hungry and bursty rather than CPU-bound, and they run 24/7, so RAM is what you'll hit first. The 1 TB transfer allowance is generous for API calls.

**Game servers (Minecraft, Palworld).** VM-3 at $14.99 for a small group, VM-4 at $23.99 for a populated modded server. Minecraft is single-thread heavy, which favors Evoxt's high-clock cores, but modpacks and Palworld push memory. 4 cores and 8 GB is the realistic floor for anything with more than a handful of players.

**Databases and anything else where a dropped packet costs money.** VM-8 at $47.99 or above. At that tier you're buying headroom and 3 TB of transfer, not speed.

## The real cost over time

Evoxt's price is the price. The home page states there are no extra bandwidth fees and no CPU burst fees, which is not universal in this market; plenty of providers advertise a low headline number and bill overage separately. Every plan also includes a weekly offsite backup at no cost, which elsewhere is often a paid add-on.

Running the monthly rates out:

| Plan | First 12 months | Second 12 months |
| --- | --- | --- |
| VM-0.5 | $35.88 | $35.88 |
| VM-1 | $71.88 | $71.88 |
| VM-1.5 | $83.40 | $83.40 |
| VM-2 | $143.88 | $143.88 |
| VM-3 | $179.88 | $179.88 |
| VM-4 | $287.88 | $287.88 |

No renewal markup is published, so year two costs the same as year one at list price. Any saving has to come from prepaying, and the size of that saving is only visible in the cart. If you're planning a three-year commitment, price the prepay option against monthly billing before you commit; a discount that doesn't beat the flexibility of monthly billing isn't a discount.

The cost that isn't on the invoice is your own time. These are self-managed machines. Evoxt's control panel covers monitoring, firewall rules, IP reassignment, cloning, VNC access and backups, which handles the infrastructure side. It does not handle your application stack: no one is going to debug your PHP-FPM pool for you. If you want a managed service, budget for it separately. For reference, one Indonesian provider prices managed service at Rp 250,000/month on top of the VPS and excluding panel licences.

## Before you check out

A few things the pricing page doesn't answer, and that are worth a support ticket rather than an assumption:

- **Refund terms.** No refund window is published on the pricing page. Ask before paying, particularly if you're prepaying for a year or more.
- **What happens past the transfer cap.** Plans are metered at 250 GB to 5,000 GB per month. The page doesn't state whether overage is billed, throttled or suspended. Size your plan with margin, or ask.
- **Windows licensing.** Windows Server images are offered. Whether a licence is bundled into the plan price isn't stated, so confirm if Windows is the reason you're buying.
- **IPv4 and IPv6.** Plans include one IPv4 address and IPv6 is available across VMs. If you need additional IPv4 addresses, Evoxt sells floating IPs as a separate product.
- **Region selection.** Jakarta is one of 17 regions. Make sure you actually select it during deployment; the plan price is the same, but the wrong region undoes the entire point.

## How Evoxt compares to other Jakarta options

For context, these are the published entry prices and terms from other providers serving Indonesian traffic. All four run Jakarta or West Java facilities.

| Provider | Entry price | Location | Notable terms |
| --- | --- | --- | --- |
| Evoxt | $2.99/mo (512 MB / 1 core / 5 GB / 250 GB) | Jakarta, JKT-IX peering | 11 plans, weekly offsite backup included, 99.99% uptime claim, 17 regions |
| LightNode | $7.71/mo (2 GB / 1 vCPU / 50 GB NVMe / 1 TB) | Jakarta | Hourly billing, no contract, 99.95% uptime, Alipay and Google Pay accepted |
| Anymhost | Rp 100,000/mo (1 GB / 1 vCPU / 25 GB NVMe) | Jakarta, Cyber 1 Building | Unmetered bandwidth on a 1 Gbps port, 30-day refund on unresolved technical issues, self-managed |
| Host.id | Rp 75,000/mo (1 GB / 1 core / 20 GB NVMe) | Jakarta, Tier 3 | Prices exclude 11% VAT, VPN/proxy/tunnel use prohibited, 99.5% SLA, unmanaged |
| Rumahweb | Rp 50,000/mo (512 MB / 1 vCPU / 10 GB SSD) | Bogor (Tier 3) and Bekasi (Tier 4) | Unmanaged by default, managed service Rp 250,000/mo, port 25 closed by default |

The pattern: Evoxt's entry point is the cheapest in USD terms and its mid-range plans undercut most local providers on a per-gigabyte basis, while the Indonesian hosts compete on local payment methods, unlimited-bandwidth framing and Indonesian-language support. If you need to pay in rupiah through a local bank transfer, that's a real reason to choose a local provider. If you're paying by card, PayPal or crypto, Evoxt accepts credit and debit cards, PayPal, Bitcoin and USDt Tron.

Note that "unlimited bandwidth" from local providers usually comes with a port speed limit or a fair-use clause, and at least one provider explicitly bans VPN, proxy and tunnel traffic. Evoxt's metered allowances avoid that ambiguity, but read the acceptable use policy if your workload is unusual.

## The decision, reduced to three lines

Running one site with modest traffic and no concurrency problem: **VM-1, $5.99/month**. Running an application where users wait on multiple sequential requests, or where a database shares the box: **VM-1.5 or VM-2**. Running something memory-bound around the clock: **VM-2 at minimum, VM-4 if it's a game server**.

Then confirm two things before you pay: the refund policy, since none is published, and the transfer overage rule, since your plan is metered. Those are the only two places where the bill can surprise you.

👉 [Deploy a Jakarta VM on Evoxt and pick your plan](https://bit.ly/EvoXt)
