# Journey of Grace — pilgrimage photobook orders

A small, static, single-page order form for Justin Tan’s Turkey / Croatia / Medjugorje pilgrimage photobook.

## Open locally

From this directory, run:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000> in a browser. You can also open `index.html` directly, although the local server is the more reliable way to preview a static site.

## Notes

- The page collects order details in the browser only; there is no backend or database in v1.
- Price is **$60 AUD per copy**. PayPal links are generated dynamically for the selected quantity using `https://paypal.me/pilgrimagephotobook/{total}AUD`.
- PayID on the confirmation panel is Justin’s mobile **`0406 498 806`**.
- On Continue, the browser posts the order to FormSubmit (`formsubmit.co`), which emails `justin@tuenproductions.com`, then shows PayPal / PayID / cash instructions. A mailto backup remains on the confirmation screen.

FormSubmit endpoint uses the activated form hash `65c4b5fc74cd890a8a2a6ca74d704353` (not the naked email) so the address is not exposed in page source.
