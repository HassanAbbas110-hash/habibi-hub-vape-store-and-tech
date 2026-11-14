# New shop: paste this into a new Claude session

Start a **new session** (not this one). Attach the shop's pictures (logo, shopfront, inside the shop, shelves; Google Maps screenshots are fine), fill in what you know below, and send.

---

Build a website for a new vape shop from my template.

**Template:** `C:\Users\HP\CloudVapor Site`. Don't edit it. Copy it to `C:\Users\HP\Sites\<Shop Name>` and work in the copy (move this session there). Read `README.md` first and follow it. Don't read the rest of the codebase unless something breaks.

**Shop details** (leave blank what I don't know, and don't invent anything):
- Name:
- Short name (used in "Hi ___" messages):
- Address (street / centre or mall / road / town / postcode / province):
- Phone (also WhatsApp):
- Email:
- Website or WooCommerce store (if any):
- Trading hours:
- Instagram:
- Facebook:
- Delivery partner (name + link, or "none"):
- Anything special (owner's name, lounge, second branch, etc.):

**Pictures:** attached. Use them like this:
1. **Logo:** find it in the pictures. If it's on a photo or a coloured background, crop it and make the background transparent. Use it for `images.logo`.
2. **Brand colour:** take the main colour from the logo and signage and use it as `accent`. Keep the dark theme unless the brand is clearly light; then also adjust `--bg`, `--panel`, `--ink` in `assets/site.css`.
3. **Photos:** assign the best ones to `shopfront`, `interior`, `disposables` and `eliquids` (any shelf shot works for the last two). Crop out phone screenshot bars first.

**Then:**
4. Write `new-brand.json` and run `python tools/rebrand.py new-brand.json`. Set `onlineStore` to `""` unless the shop has its own WooCommerce store.
5. Rewrite the copy that's specific to the shop: the hero headline and lead, the About page story, the meta descriptions, and the FAQs about payment and delivery. Use only facts I gave you, and keep it short and human, not salesy.
6. **Products:** keep the template's catalogue as sample stock for now. If the shop has a WooCommerce store, run `python tools/snapshot.py` to load its real stock instead.
7. **Test:** serve it locally and open every page at desktop and phone width. Fix any sideways scrolling, console errors, broken images or leftover old-brand text.
8. **Publish:** new public GitHub repo named after the shop, with GitHub Pages turned on (the steps are in the README). Ask me before creating it.
9. **Report back:** the live link, a screenshot of the home page, and a short list of anything still missing (hours, socials, products and so on).

Keep it efficient: use the rebrand script rather than editing files one by one.
