---
name: collect-leads
description: Offer a free download in exchange for a confirmed email address with DeliveryKit Lead gen, and review the leads. Use for lead magnets, free checklists, or questions about who opted in.
---

# Collect leads

Lead gen products need no Stripe connection or sandbox/live choice.

- **Create or edit**: `create_merchant_lead_gen_product`, `update_merchant_lead_gen_product`, and the page with `get_merchant_lead_gen_product_page` and `update_merchant_lead_gen_product_page`. Attach the file using the file steps in `launch-product`.
- **Review**: `list_merchant_lead_gen_products` for requested, confirmed and downloaded counts, then `list_merchant_leads`.
- Lead emails are customer data. Only say a lead agreed to marketing when `marketing_consent_at` is set, and only list marketing opt-ins when asked for them.
