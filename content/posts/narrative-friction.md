---
date: '2026-05-18'
draft: false
title: 'Reading Between the Filings: Narrative Friction in Corporate Disclosures'
weight: 11
tags: ["Research"]
summary: "Companies tell investors one story and regulators another. This project asks what the distance between those stories can tell us about firm-level uncertainty."

cover:
  image: "/images/disclosure_gap.png"
  alt: "Placeholder cover image for the narrative friction project"
  caption: "The distance between two corporate stories can have a price."
  relative: false
---

# Reading Between the Filings

*When companies say one thing to investors and another to regulators, can we measure the gap?*

---

In January 2007, Countrywide Financial's CEO told investors the company was *"well-positioned to capitalize on the opportunities that are emerging in this period of transition in the mortgage market."* The 2006 10-K filed with the SEC told a different story: *"Our delinquency and loss experience on all types of loans has been increasing... our financial condition and results of operations will be adversely affected."*

Eighteen months later, Countrywide collapsed.

This pattern — executives painting a rosy picture on the earnings call while their lawyers quietly document trouble in regulatory filings — isn't unique to Countrywide. It plays out across markets and decades. But until recently, it had never been systematically measurable.

## The two faces of corporate disclosure

Every public company in the US produces two kinds of documents about its financial condition: the **earnings call**, voluntary and management-controlled (incentive: project confidence), and the **10-K/10-Q filing**, mandatory and supervised by lawyers facing personal liability (incentive: be thorough and cautious).

I call the measurable divergence between these two documents **narrative friction**. When times are good, both narratives coexist comfortably. But when a company faces real trouble, the tension between "what we want to say" and "what we have to say" gets acute. The friction widens — not because management is lying, but because maintaining narrative consistency across two documents with opposing incentives gets harder when there's more to hide. That widening, I hypothesized, should leave a measurable trace — and predict future stock volatility.

## The finding

Working on 3,377 paired earnings-call-and-10-K observations across 214 S&P 500 firms from 2006 to 2024, I built a four-layer NLP pipeline that measures friction along nearly orthogonal dimensions: statistical language surprise, concept-level hedging, cross-document logical consistency, and affective tone.

The result: when a company's friction increases relative to its own historical baseline, its future volatility increases too — and the relationship holds within firms over time, ruling out industry or firm-type effects. The market does detect friction in the short term and partially penalizes it. But the penalty is incomplete, and the hidden information eventually resolves — sometimes as a crash, sometimes as a rally.

The most striking case in my test set was Simon Property Group, February 2021. The earnings call said *"we've turned the corner."* The 10-K, filed for the same period, documented a 23.9% NOI decline, tenant bankruptcies, and $400M in rent abatements. The 130-day return was +30.5%.

**Friction doesn't predict direction. It predicts magnitude.** The distance between two narratives signals that something big is coming — not which way it will go.

---

Every quarter, thousands of executives step up to a microphone and narrate a version of their company's reality. Hours or weeks later, their lawyers file a different version with the SEC. The distance between those two versions has always existed. Now it can be measured — and it turns out that distance has a price.

*Link to full article will be available soon.*
