# ScentsbyMaryam — Website Guide

A luxury perfume ordering website for ScentsbyMaryam. Single HTML file — no coding knowledge needed to run or manage it.

---

## 📁 What's Included

| File | Description |
|------|-------------|
| `ScentsbyMaryam.html` | The complete website (storefront, cart, admin panel) |
| `README.md` | This guide |

---

## 🚀 How to Go Live (Get a Shareable Link)

### Option A — Netlify (Recommended, Free)
1. Go to [netlify.com](https://netlify.com) and create a free account
2. Click **"Add new site"** → **"Deploy manually"**
3. Drag and drop `ScentsbyMaryam.html` into the upload box
4. Your site goes live instantly at a link like `your-site.netlify.app`
5. You can rename it to something like `scentsbymaryam.netlify.app` in site settings

### Option B — Custom Domain (Professional)
If you want a link like `www.scentsbymaryam.com`:
1. Buy a domain on [Namecheap](https://namecheap.com) or [GoDaddy](https://godaddy.com) (~₦5,000–₦10,000/year)
2. Connect it to your Netlify site under **Domain Settings**

---

## 🛍️ How the Website Works

### For Customers
- Browse all perfumes, body sprays, and oils
- Filter by category or search by name
- Click any product to see full details
- Add items to cart
- Order directly via WhatsApp (Maryam or Edward)

### WhatsApp Order Flow
When a customer clicks **Order via WhatsApp**, it automatically sends a pre-filled message with their full cart summary to the selected contact.

---

## 🔐 Admin Login

Only Maryam and Edward can access the Admin panel.

| Name | Username | Password |
|------|----------|----------|
| Maryam | `mary101` | `12345678` |
| Edward | `eddie101` | `12345678` |

> **To change a password:** Open `ScentsbyMaryam.html` in a text editor (like Notepad or VS Code), find the section labelled `ADMIN CREDENTIALS` and update the values.

### What Admins Can Do
- Upload real product photos (click the product image in Admin panel)
- Edit product names, notes, and prices
- Changes apply instantly on the live site

---

## 📦 Products & Prices

| Product | Type | Price |
|---------|------|-------|
| Riggs London 4pcs Combo | Perfume | ₦26,000 |
| Riggs Patrol EDP 100ml | Perfume | ₦7,000 |
| Riggs Noble EDP 100ml | Perfume | ₦7,000 |
| Riggs Body Spray — Icon | Body Spray | ₦4,000 |
| Riggs Body Spray — Wes | Body Spray | ₦4,000 |
| Riggs Body Spray — Ace | Body Spray | ₦4,000 |
| Dani 33 Perfume Oil | Oil | Enquire |
| Bushra Perfume Oil | Oil | ₦40,000 |

---

## ✏️ How to Update Products

Open `ScentsbyMaryam.html` in a text editor and find the section labelled:

```
// PRODUCTS — Add, remove or edit products here
```

Each product looks like this:

```javascript
{
  id: 1,
  name: 'Riggs London — 4pcs Combo',
  type: 'perfume',           // perfume | spray | oil
  notes: 'Hero · Icon · Patroni · Eos',
  price: 26000,              // use null for "Enquire"
  badge: 'combo',            // combo | new | oil | null
  emoji: '✨',               // shown if no photo uploaded
  desc: 'Product description here.',
  img: null                  // leave as null; upload via Admin panel
}
```

To **add a new product**, copy one block, paste it after the last product (before the closing `]`), add a comma, and update the details.

To **remove a product**, delete its entire block (from `{` to `},`).

---

## 📞 Contact Numbers

| Name | WhatsApp |
|------|----------|
| Maryam | +234 915 942 6374 |
| Edward | +234 912 690 0303 |

> **To update a number:** Find the section labelled `WHATSAPP NUMBERS` in the HTML file and edit the values.

---

## 🎨 Brand Colours

| Colour | Hex Code |
|--------|----------|
| Gold | `#C9A84C` |
| Black | `#0D0D0D` |
| Forest Green | `#1B3A2D` |

---

## ❓ Common Questions

**Q: Do I need internet to open the website file?**
A: You can open it locally on any computer or phone browser. But to share a link with customers, you need to host it online (see Go Live section above).

**Q: Will my product photos be saved?**
A: Photos uploaded via the Admin panel are stored temporarily in the browser session. For permanent photos, open the HTML file in a text editor, find the product, and set the `img` field to a hosted image URL (e.g. from Google Drive or Cloudinary).

**Q: Can I add more admins?**
A: Yes. In the `ADMIN CREDENTIALS` section, add a new line following the same format as Maryam and Edward.

**Q: How do I add delivery fees to the cart?**
A: Let your developer know, or contact support to have a delivery fee field added to the checkout.

---

*Built for ScentsbyMaryam · Nigeria · 2025*
