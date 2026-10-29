# DeliveryKit for Claude

DeliveryKit lets you sell digital downloads and memberships with Stripe Checkout and automatic file delivery. This plugin connects Claude to your DeliveryKit workspace and adds guided workflows, so you can set up a store, launch a product, publish to a subscriber library, collect leads, and review sales by describing what you want.

## Install

```
/plugin install deliverykit --marketplace ow/deliverykit-claude
```

Or from your shell: `claude plugin marketplace add ow/deliverykit-claude`, then `claude plugin install deliverykit@deliverykit`. On claude.ai, add it from Customize > Plugins.

## Setup

After installing, sign in to DeliveryKit when Claude asks you to connect. You need a DeliveryKit account; the setup skill can walk a new merchant through creating a workspace and connecting Stripe. Start in sandbox mode to try things safely.

## Skills

- `set-up-store`: create a workspace and connect Stripe.
- `launch-product`: product, price, file, delivery rules and checkout link.
- `review-sales`: sales, orders, customers and subscription status.
- `run-membership-library`: subscription products, library posts and subscriber imports.
- `collect-leads`: free downloads exchanged for a confirmed email address.

## What it will not do

Claude asks before changes that affect your store or email your subscribers. It cannot refund orders, cancel buyer subscriptions, or take buyer payments in chat; buyers pay on Stripe-hosted checkout.

Support: support@deliverykit.app. Privacy: https://deliverykit.app/privacy
