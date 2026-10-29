---
name: launch-product
description: Launch a sellable digital product end to end in DeliveryKit, from product and price to delivered file and checkout link. Use when the user wants to sell a PDF, ebook, template, video or other download.
---

# Launch a product

Work in this order, confirming the workspace and Stripe environment (sandbox or live) before the first change.

1. `list_merchant_catalog` to check the product does not already exist.
2. Confirm name, price, currency and one-time vs monthly/yearly, then `create_merchant_product` and `create_merchant_price`. Always pass an `idempotency_key` and reuse the same key and inputs when retrying.
3. Files: check you can read the file bytes and make an HTTP request. If so, `create_merchant_upload`, send the file exactly as the returned `upload_request` says, then `complete_merchant_upload` and `create_merchant_file`. If you cannot transfer the file, say so plainly and ask the user to add it in the DeliveryKit dashboard. Never claim an untransferred file was uploaded, and never put file bytes in the conversation.
4. `get_merchant_file_targets`, then `configure_merchant_delivery` to attach the file. Ask about download limits, access period and PDF stamping rather than assuming. Show the change and get approval first.
5. Optionally improve the product page with `get_merchant_product_page` and `update_merchant_product_page`.
6. `create_merchant_checkout_link` and hand the Stripe-hosted URL to the user. Buyer payments never happen in chat.

Confirm currency and amount whenever you create or change a price or checkout link.
