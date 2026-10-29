---
name: run-membership-library
description: Create and run a DeliveryKit membership or subscription library. Use when the user wants a recurring product, wants to publish a post or new files to subscribers, or wants to import existing Stripe subscribers.
---

# Run a membership library

- **Create**: `create_merchant_product` with a monthly or yearly price, then attach content with `configure_merchant_delivery` (bundles and new-content announcements are options there). Confirm name, amount, currency and interval first.
- **Publish**: `list_merchant_library_posts`, then `publish_merchant_library_post` or `update_merchant_library_post`. Publishing posts and adding library files can email subscribers. Ask explicitly whether to email before every publish, and say that editing a post only changes copy for emails not yet sent.
- **Import existing subscribers**: `get_merchant_subscription_import` to check readiness, then `import_merchant_subscribers`. Confirm the product and whether emails are sent before queuing, then report status.

Say whether you are in sandbox or live mode before any change.
