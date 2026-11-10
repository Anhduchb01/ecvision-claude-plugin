<!-- DRAFT v0.1: wording not yet approved (ask_team). Remove this line before any submission. -->

# ecvision for Claude

ecvision watches your Shopify store and the rival stores you choose, every day, from public sources: their products, prices, sales, ads, posts and estimated traffic. This plugin adds five skills that turn those readings into answers Claude can give you, each with its source and the date it was read.

## What it does

| Skill | Ask it when |
| --- | --- |
| `sale-and-offer-watch` | "Is a rival running a sale, since when, and where do its ads land?" |
| `competitor-ads-to-brief` | "I need new ad ideas. What do rivals run that I do not?" |
| `weekly-rival-recap` | "What did my competitors do this week?" Gives one page you can forward |
| `launch-and-price-watch` | "What did a rival launch, change the price of, or sell out of?" |
| `rival-top-products` | "Which of a rival's products does it push hardest, or put on sale? What does the sales estimate say?" |

## How to use it

1. Add the plugin, then connect the **ecvision** connector when Claude asks. You sign in with your ecvision account. In Claude Code, install it with `/plugin install ecvision --marketplace Anhduchb01/ecvision-claude-plugin`.
2. Ask in your own words, for example "what are my rivals offering for Black Friday?".

You need an ecvision account with competitors set up. Plans decide how far back the history goes. Where a plan holds something back, Claude says so rather than saying nothing changed.

## What data it sends

The plugin itself contains only instructions and a link to the connector. It collects nothing and runs no code on your machine. When Claude uses the connector, it asks ecvision for data about the stores in your own workspace and reads it back; nothing is written or changed, and the connector is read-only. The data is public information collected about stores, plus your own workspace's list of stores.

## Limits, stated plainly

- Dates are the day a value was read, not the day something happened.
- Sales and traffic figures are estimates, labelled with their month.
- No source gives ad spend, impressions, click-through rate or engagement for an ad, so none are shown or guessed.
- Email and SMS are not collected.
- Data is collected daily, not live.

## Support

See the ecvision documentation and privacy policy at ecvision.ai. Questions: use the contact on the connector's listing.
