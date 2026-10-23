# cloud vps server hosting: Four Specs That Decide the Bill, and Every GoMami Plan Priced From $29/mo

The median entry-level cloud VPS across 157 hosts, checked in September 2026, cost $13.48 a month. GoMami's cheapest plan is $29 and its most expensive is $999. That spread is the entire question this article answers: what sits between those numbers, and does your workload need any of it?

GoMami Networks (AS36002) sells VPS and dedicated servers in Hong Kong, Japan, Singapore and Los Angeles, with routing tuned toward mainland China over China Telecom CN2 GIA, Unicom AS9929 and Mobile CMIN2. If your users are in Frankfurt or Ohio, most of that premium is wasted on you. If a real share of your traffic comes from Shenzhen, Shanghai or Beijing, it's the part of the invoice that decides whether your site works at 9pm.

> **Quick pick:** the HKG Pulse Mini — 2 vCPU, 4GB RAM, 60GB NVMe, 1TB outbound at 1Gbps, $59/mo — covers what a normal China-facing web stack actually needs, and Hong Kong has the shortest documented return path of the three Asian regions. 👉 [check the HKG Pulse Mini on the GoMami store](https://gomami.io/aff.php?aff=415&pid=4)

## The four specs that actually decide your monthly bill

Outbound traffic allowance, port speed, CPU generation, and whether DDoS scrubbing is bundled or an add-on do more to set your monthly cost than the vCPU count does. Get those four wrong and a $29 plan ends up costing more than a $79 one.

**Outbound traffic allowance.** GoMami bills outbound traffic only; inbound is free. That's unusual and it changes the math for backup targets, mirrors, media pullers and anything that downloads more than it serves. A 500GB allowance that only counts egress behaves very differently from the "1TB transfer" line on a mainstream cloud page, which usually counts both directions or bills egress separately at a per-GB rate.

**Port speed.** The Nano tiers sit at 1Gbps, the mid tiers at 2–3Gbps, and the LAX Titan at 10Gbps. Port speed caps a single-threaded transfer long before the traffic allowance does.

**CPU generation.** GoMami runs three distinct generations: EPYC 9575F (Turin, up to 5GHz), Ryzen 9 9950X (Peak, up to 5.7GHz), and EPYC 7763 / 7773X / 7K83 / 7K62 (Pulse, 3.3–3.5GHz). The Pulse line is cheaper per core, the Peak line is for single-thread-bound workloads like game servers, and Turin is the newest silicon with daily AWS S3 backups included on every plan.

**DDoS: bundled or billed?** This is where the marketing page and the documentation diverge, and it's covered in detail below.

One operational gap worth knowing before you commit: plan changes go through a support ticket. There's no self-serve resize button, which is a real difference from Vultr or Google Cloud. Deployment itself is fast — 1 to 5 minutes after payment, with IP and credentials emailed — and there's a REST API if you'd rather automate.

## Every GoMami plan, by product line

The homepage only shows six plans and doesn't label which region they belong to, so the tables below use the region-labeled listings from the store and stock trackers. Prices are monthly, USD.

**Hong Kong — Turin (AMD EPYC 9575F, up to 5GHz)**

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Turin Mini | 2 / 4GB / 100GB | 1TB / 2Gbps | $69 | [ HKG Turin Mini](https://gomami.io/aff.php?aff=415&pid=14) |
| Turin Air | 4 / 8GB / 140GB | 2TB / 2Gbps | $129 | [ HKG Turin Air](https://gomami.io/aff.php?aff=415&pid=15) |
| Turin Pro | 6 / 16GB / 180GB | 5TB / 5Gbps | $299 | [ HKG Turin Pro](https://gomami.io/aff.php?aff=415&pid=16) |
| Turin Ultra | 12 / 32GB / 220GB | 10TB / 5Gbps | $599 | [ HKG Turin Ultra](https://gomami.io/aff.php?aff=415&pid=22) |

**Hong Kong — Peak (AMD Ryzen 9 9950X, up to 5.7GHz)**

Two price figures for this line are in circulation: GoMami's homepage lists the Ryzen 9 9950X Mini at **$59**, while the store listing and independent trackers record **$69**. The table uses $69; confirm the cart total before paying. Air and Pro agree at $99 and $199 across all sources.

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Peak X5 Mini | 2 / 4GB / 40GB | 1TB / 2Gbps | $69 (homepage: $59) | [ HKG Peak X5 Mini](https://bit.ly/Gomami) |
| Peak X5 Air | 4 / 8GB / 60GB | 2TB / 2Gbps | $99 | [ HKG Peak X5 Air](https://bit.ly/Gomami) |
| Peak X5 Pro | 6 / 16GB / 80GB | 5TB / 5Gbps | $199 | [ HKG Peak X5 Pro](https://bit.ly/Gomami) |

**Hong Kong — Pulse (AMD EPYC 7763, 3.5GHz)**

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Pulse Nano | 2 / 2GB / 40GB | 500GB / 1Gbps | $49 | [ HKG Pulse Nano](https://gomami.io/aff.php?aff=415&pid=26) |
| Pulse Mini | 2 / 4GB / 60GB | 1TB / 1Gbps | $59 | [ HKG Pulse Mini](https://gomami.io/aff.php?aff=415&pid=4) |
| Pulse Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $119 | [ HKG Pulse Air](https://gomami.io/aff.php?aff=415&pid=5) |
| Pulse Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $269 | [ HKG Pulse Pro](https://gomami.io/aff.php?aff=415&pid=6) |
| Pulse Ultra | 16 / 32GB / 300GB | 10TB / 5Gbps | $499 | [ HKG Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=25) |

**Hong Kong — Forge (dedicated, AMD EPYC 7663, 56 cores / 112 threads)**

Pricing on this line has moved and the two records differ by $200/mo. An earlier review listed Forge Mini at **$399/mo plus a $68 one-time setup fee**; the October 2026 stock snapshot shows **$599/mo**. Treat the table as an indication and confirm on the order page before budgeting.

| Plan | RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Forge Mini | 128GB / 960GB | 10TB / 2Gbps | $599 (earlier record: $399 + $68 setup) | [ HKG Forge Mini](https://bit.ly/Gomami) |
| Forge Air | 256GB / 4TB | 20TB / 2Gbps | $899 (earlier record: $699 + $68 setup) | [ HKG Forge Air](https://bit.ly/Gomami) |

**Japan — Pulse (AMD EPYC 7773X / 7K83, 3.5GHz)**

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Nano | 2 / 2GB / 40GB | 500GB / 1Gbps | $29 | [ JPN Pulse Nano](https://gomami.io/aff.php?aff=415&pid=13) |
| Mini | 2 / 4GB / 60GB | 1TB / 1.5Gbps | $49 | [ JPN Pulse Mini](https://gomami.io/aff.php?aff=415&pid=10) |
| Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $89 | [ JPN Pulse Air](https://gomami.io/aff.php?aff=415&pid=11) |
| Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $169 | [ JPN Pulse Pro](https://gomami.io/aff.php?aff=415&pid=12) |
| Ultra | 12 / 32GB / 300GB | 10TB / 3Gbps | $338 | [ JPN Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=24) |

**Singapore — Pulse (AMD EPYC 7663, 3.5GHz)**

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Nano | 2 / 2GB / 40GB | 500GB / 1Gbps | $29 | [ SIN Pulse Nano](https://gomami.io/aff.php?aff=415&pid=21) |
| Mini | 2 / 4GB / 60GB | 1TB / 1Gbps | $49 | [ SIN Pulse Mini](https://gomami.io/aff.php?aff=415&pid=17) |
| Air | 4 / 8GB / 80GB | 2TB / 1Gbps | $89 | [ SIN Pulse Air](https://gomami.io/aff.php?aff=415&pid=18) |
| Pro | 8 / 16GB / 100GB | 5TB / 3Gbps | $169 | [ SIN Pulse Pro](https://gomami.io/aff.php?aff=415&pid=19) |
| Ultra | 12 / 32GB / 300GB | 10TB / 3Gbps | $338 | [ SIN Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=23) |

**Los Angeles — Pulse (AMD EPYC 7K62, 3.3GHz)**

| Plan | vCPU / RAM / NVMe | Traffic / Port | Price | Order |
| --- | --- | --- | --- | --- |
| Nano | 2 / 2GB / 40GB | 1TB / 1Gbps | $29 | [ LAX Pulse Nano](https://gomami.io/aff.php?aff=415&pid=27) |
| Mini | 2 / 4GB / 60GB | 2TB / 1Gbps | $59 | [ LAX Pulse Mini](https://gomami.io/aff.php?aff=415&pid=28) |
| Air | 4 / 8GB / 80GB | 4TB / 2Gbps | $129 | [ LAX Pulse Air](https://gomami.io/aff.php?aff=415&pid=29) |
| Pro | 6 / 16GB / 100GB | 8TB / 3Gbps | $259 | [ LAX Pulse Pro](https://gomami.io/aff.php?aff=415&pid=30) |
| Ultra | 12 / 32GB / 300GB | 15TB / 5Gbps | $599 | [ LAX Pulse Ultra](https://gomami.io/aff.php?aff=415&pid=31) |
| Titan | 12 / 32GB / 600GB | 30TB / 10Gbps | $999 | [ LAX Pulse Titan](https://gomami.io/aff.php?aff=415&pid=32) |

The LAX line launched in June 2026 with a 20% recurring coupon, `Hi,LAX`, which brings the Nano from $29 down to $23.20. The campaign was announced as limited-stock. Whether it still applies in October is something only the cart will tell you, so try the code before paying rather than assuming.

Two more caveats the tables can't show. The homepage also displays an EPYC 7763 plan at $39 that isn't labeled by region; a third-party record from May 2026 shows a Hong Kong 2 vCPU / 4GB / 40GB / 1TB plan at exactly $39 before a 15% coupon, so that price did exist at some point. Treat the homepage figure as a "from" number. Separately, GoMami's own purchase documentation lists Hong Kong, Japan and Singapore as available locations and doesn't mention Los Angeles at all — LAX plans have been on sale since June, so this is likely a stale doc, but check availability before you plan around it.

## The two headline numbers need a footnote

The homepage sells on "RTT under 50ms across mainland China" and "up to 600 Gbps DDoS mitigation". Both are true in a narrow sense and misleading if you read them the obvious way. The docs spell out what's actually included.

On latency, the documented figures are Hong Kong under 30ms, Japan under 50ms, and Singapore under 70ms, with an explicit note that real numbers vary by ISP and you should test before buying. The single "<50ms" on the homepage really only covers Hong Kong and Japan.

On DDoS, every instance gets best-effort detection and scrubbing by default. The 600 Gbps scrubbing capacity is a paid add-on, not something bundled into every plan. Worse for planning purposes: when an attack is large enough to affect other customers on the node, your IP gets blackholed for 30 to 60 minutes, released automatically, with no manual override. If you're running a game server or anything with a public target on its back, budget for the add-on and design around the blackhole window. 👉 [see what the DDoS add-on and default protection actually cover](https://bit.ly/Gomami)

That distinction matters more than it looks. A $29 Nano and a $999 Titan share the same default protection tier; the difference in exposure is something you buy separately.

## What independent testing shows

A December 2025 review of the HKG Turin Mini (2 vCPU, 4GB, 100GB) is the most detailed public benchmark available, and it's worth reading for the parts that contradict the marketing.

Performance was genuinely strong: Geekbench 5 came in at 2259 single-core and 4262 multi-core, and fio hit 8.03 GB/s on 1MB blocks. For a 2-vCPU slice, that's server-grade silicon behaving like server-grade silicon.

The bandwidth numbers were carrier-dependent in a way the "three-network optimized" phrase doesn't convey:

- Shenzhen Telecom (500Mbps local): 475 Mbits/sec to Hong Kong
- Jinan Unicom (500Mbps local): 545–572 Mbits/sec
- Guangdong Mobile (1Gbps local): 37.5 Mbits/sec up, 284 Mbits/sec down
- Wuhan Mobile: 33.4 Mbits/sec up, 549 Mbits/sec down
- Ningbo Mobile: 37.7 Mbits/sec up, 653 Mbits/sec down

Mobile uplink is being QoS'd hard on the Hong Kong path, with intermittent stalls, while download is fine. The same pattern showed up on the Japan node. Singapore was the best of the three for Mobile. Unicom to Singapore had upstream stalling issues of its own. The reviewer's own summary: Telecom users are well served everywhere, Unicom users should prefer Hong Kong, Mobile users should look at Singapore first.

Practical takeaway: if your workload is upload-heavy from China Mobile — streaming in, large file sync, live contribution — test that specific direction during your refund window. If it's download-heavy, the picture is much better.

There's also a routing point worth internalizing. A Google Cloud discussion from October 2026 documented two Premium Tier VMs hitting the same Beijing Unicom address at 21:53 local time: the Hong Kong instance returned through Orange AS5511 at 250–300ms RTT, while the Taiwan instance went direct into AS4837 at 60–70ms. Same provider, same tier, wildly different result. "The server is in Hong Kong" tells you almost nothing; the return path does.

## GoMami versus mainstream cloud VPS pricing

GoMami is not competing on price, and the comparison makes that concrete. The figures below were checked on 24 September 2026 from each provider's own pricing page.

| Provider / plan | Specs | Price |
| --- | --- | --- |
| Google Cloud e2-micro | 2 vCPU / 1GB | $6.12/mo |
| Google Cloud e2-small | 2 vCPU / 2GB | $12.23/mo |
| Akamai (Linode) Nanode 1GB | 1 vCPU / 1GB / 25GB / 1TB | $5.00/mo |
| Vultr | 2 vCPU / 4GB / 80GB / 3TB | $20.00/mo |
| Cloudzy 4GB DDR5 | 2 vCPU / 4GB / 120GB / 5TB | $14.48/mo |
| OVHcloud b3-8 | 2 vCPU / 8GB / 50GB NVMe | $44.17/mo, 14-day refund |
| Scaleway STARDUST1-S | 1 vCPU / 1GB | $0.49/mo |
| InterServer | 2GB RAM / SSD / 2TB | $3.00/mo |
| Median of 157 hosts, entry plan | varies | $13.48/mo first price |

A 2 vCPU / 4GB box costs $14.48 at Cloudzy with 5TB of transfer, $20 at Vultr with 3TB, and $59 at GoMami with 1TB. You are paying roughly $40 a month for routing, not for RAM. If your traffic never touches China, that $40 buys nothing you can measure.

The honest version of "who shouldn't buy this" comes from the reviewers themselves: an independent test concluded that budget-limited personal users should buy elsewhere, and a separate review lists the same three disqualifiers — cheapest-possible Linux box, audience entirely in the US or Europe, budget capped at a few dollars a month.

## Billing, IPs and the rules that can end your service

Three billing details sit outside the pricing table and change what a month actually costs.

**Over-traffic throttles rather than suspends.** Exceed the monthly quota and bandwidth gets throttled while the server stays online. There's no hard cutoff to monitor; the machine goes slow and you have to notice. The quota resets at the start of each billing cycle, not on the first of the month.

**No grace period at expiry.** The service is suspended on the due date, data retained and restored on payment, then terminated five days after that with data possibly unrecoverable. Set a renewal reminder before you need it.

**The 24-hour refund has conditions.** Full refund within 24 hours of activation, returned to the original payment method, limited to one per user and to first-time purchases. Renewals don't qualify. Neither do services terminated for terms violations, used account credit, or IPs blackholed by DDoS. Alipay refunds take 1–3 business days, credit cards 5–10, crypto 1–3. Once approved, the instance and its data are deleted immediately — back up before you file the ticket. 👉 [read the refund terms before you order](https://bit.ly/Gomami)

Two IP rules matter more for this audience than they would on a generic cloud. If an IP becomes unreachable from mainland China, the documented path is to check whether it's globally down first, run `ping` and `traceroute`, then open a ticket so support can verify the status — if it's confirmed blocked, support will help you change the IP. That's a routine problem for anything China-facing, and having a documented remedy is worth more than a spec bump. Additional IP addresses also go through a ticket rather than a self-serve panel.

One hard limit deserves its own line: the terms of service prohibit bot operations, with TikTok named specifically, and violations mean immediate account termination without refund. Deliberate overuse of bandwidth, CPU time or disk IO falls under the same clause. If your project's business model depends on automating a social platform, this is the wrong host and no support ticket will change that.

## Which plan for which workload

Match the workload to the line first, then to the size.

- **China-facing website or API under steady load:** HKG Pulse Mini ($59) or Air ($119). The EPYC 7763 has enough single-core grunt for a normal LEMP stack, and the Hong Kong return path is the shortest of the three regions.
- **Game server or anything single-thread-bound:** HKG Peak X5 Mini, Ryzen 9 9950X at up to 5.7GHz. This is the one line where the extra clock speed is the entire product.
- **Newest hardware, backups included:** HKG Turin Mini ($69). EPYC 9575F instead of Ryzen 9 9950X, plus daily automatic backup to AWS S3 on every tier.
- **Cheapest China-optimized entry:** JPN Pulse Nano or SIN Pulse Nano at $29. Tokyo and Singapore both route over the same three carriers; Singapore is the better pick if your audience skews Mobile, Japan if you need Tokyo peering for other reasons. 👉 [check the JPN Pulse Nano at $29](https://gomami.io/aff.php?aff=415&pid=13)
- **Containerized or multi-tenant workloads:** Pulse Air or Pro. More cores per dollar than Turin, and horizontal scaling doesn't care about boost clocks.
- **High-volume egress:** LAX Ultra ($599, 15TB at 5Gbps) or Titan ($999, 30TB at 10Gbps). The Titan's traffic allowance is the reason it exists.
- **Dedicated silicon, no noisy neighbours:** Forge. 56 cores / 112 threads of EPYC 7663 in Hong Kong, instant activation, OS reinstall from the panel.

If none of those map to you — a $5 personal box, an audience in Europe, a project that will never see a Chinese IP — the mainstream options in the table above are cheaper and perfectly adequate. Buying China routing you don't use is the most common way to overpay here.

## FAQ

**Does GoMami include DDoS protection by default?** Yes, but only best-effort automatic scrubbing. The 600 Gbps capacity advertised on the homepage is a paid add-on, and attacks that affect other customers trigger a 30–60 minute IP blackhole with no manual override.

**What happens if my IP gets blocked in mainland China?** Open a ticket and support will verify the status. If it's confirmed blocked, they'll help you change the IP. IP blocking is usually tied to what's running on the server, so check your own usage first.

**Is traffic really outbound-only?** Yes. Inbound traffic is not counted, which makes the 500GB on a Nano go further than it sounds if your workload pulls more than it pushes.

**How fast is setup?** Deployment completes in 1–5 minutes after payment, with IP and login credentials emailed. Supported images include Ubuntu 22.04/24.04, Debian 11/12, CentOS Stream 9, AlmaLinux 8/9 and Windows Server 2019/2022, plus custom ISO.

**Can I resize without rebuilding?** Not self-serve. Plan changes currently require a support ticket, and extra IP addresses do too.

**What's the actual latency to China?** Documented typicals are under 30ms for Hong Kong, under 50ms for Japan and under 70ms for Singapore. Measured results vary by carrier and time of day, and the docs recommend testing first — which the 24-hour refund window exists to make possible. Sample across several hours rather than one ping run; congestion on these paths arrives in waves, and a ten-packet test can land entirely inside a calm stretch.

## Before you check out

Pick by direction of traffic first. If most of your bytes go out to Chinese users, the Hong Kong Pulse Mini at $59 is the sane default, and the Turin Mini at $69 adds newer silicon plus daily backups. If you upload more than you download from a Mobile connection, look at Singapore before Hong Kong, because that's where the third-party numbers look healthiest. If you only ever download, Hong Kong wins on distance.

Then do three things before the 24 hours run out: run your own throughput test against your actual users' carriers in both directions, confirm the cart price matches the plan you think you picked — the homepage and the store don't always quote the same figure for the same configuration — and check that whatever the server will be doing is allowed under the terms, since a violation ends the service without a refund.

👉 [compare all GoMami plans and current pricing](https://bit.ly/Gomami)
