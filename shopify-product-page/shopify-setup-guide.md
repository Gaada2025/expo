# Shopify Setup Guide: The Perimenopause Reset Workbook
### The Reset Co. — Digital Product Store

---

## Overview

This guide walks you through setting up a fully functional Shopify digital product store to sell "The Perimenopause Reset Workbook" as an instant digital download at $27 per purchase.

---

## Step 1: Install the Digital Downloads App

1. Log in to your Shopify admin at `your-store.myshopify.com/admin`.
2. In the left sidebar, click **Apps**, then click **App Store**.
3. In the search bar, type **Digital Downloads**.
4. Select the app published by **Shopify** (it is free and official).
5. Click **Install app** and confirm the permissions prompt.
6. Once installed, the Digital Downloads app will appear under **Apps** in your admin sidebar.

---

## Step 2: Create the Product Listing

1. In your Shopify admin, go to **Products > Add product**.
2. Fill in the following fields:

   **Title:**
   ```
   The Perimenopause Reset Workbook
   ```

   **Description:**
   Paste the contents of `shopify-product-description.html` into the description field. Click the `<>` (HTML) icon in the description toolbar to switch to HTML view, then paste the code.

   **Price:** `27.00`

   **Compare at price:** (Optional) Set to `47.00` to show a crossed-out original price.

   **Product type:** `Digital Download`

   **Vendor:** `The Reset Co.`

   **Tags:** Add the following tags:
   ```
   perimenopause, workbook, digital download, womens health, hormones, reset, midlife, pdf
   ```

3. Under **Inventory**, uncheck **Track quantity** (digital products have unlimited stock).

4. Under **Shipping**, uncheck **This is a physical product** — this prevents Shopify from requesting a shipping address at checkout.

5. Click **Save**.

---

## Step 3: Upload the PDF as a Digital Download

1. Open the **Digital Downloads** app from your Apps menu.
2. Find your newly created product — "The Perimenopause Reset Workbook" — in the list.
3. Click **Add file** next to the product.
4. Upload your workbook PDF file (ensure it is a final, high-quality version before uploading).
5. Once uploaded, the file will be linked to the product automatically.
6. The app handles secure download link generation and file delivery for every purchase.

> **Tip:** If your PDF exceeds 5 GB, use a tool like Dropbox or Google Drive and link the download manually via a post-purchase email instead (see Step 4 for configuration).

---

## Step 4: Set Up Automatic Email Delivery

Shopify's Digital Downloads app sends an automatic download email to the customer immediately after payment is confirmed.

1. Open the **Digital Downloads** app.
2. Click **Settings** (gear icon or top-right menu).
3. Under **Email**, review the default email template.
4. Customize the subject line and body text to match The Reset Co. brand. Example:

   **Subject:** `Your Perimenopause Reset Workbook is ready to download!`

   **Body opening line:** `Thank you for your purchase from The Reset Co. Your workbook is one click away.`

5. Save your changes.

Additionally, review Shopify's built-in notification emails:
- Go to **Settings > Notifications**.
- Click **Order confirmation** and customize the branding (logo, colors, footer text) to match The Reset Co.

---

## Step 5: Configure the Product Page with Custom HTML

Your `index.html` file contains a custom-designed product page. To use it within Shopify:

### Option A — Paste into a Shopify Custom Page (Recommended for a standalone landing page)

1. In your Shopify admin, go to **Online Store > Pages**.
2. Click **Add page**.
3. Set the **Title** to: `The Perimenopause Reset Workbook`
4. In the content editor, click the `<>` (HTML source) icon.
5. Copy the body content from your `index.html` (everything inside the `<body>` tags, not the `<body>` tags themselves).
6. Paste it into the HTML editor.
7. Click **Save**.
8. Note: Shopify strips `<style>` tags from page content. Move all CSS from `index.html` into your theme's custom CSS file (see Step 6).

### Option B — Use the Custom HTML as a Product Description

1. Go to **Products** and open your workbook product.
2. Click the `<>` HTML icon in the description editor.
3. Paste the relevant HTML sections (headline, bullet points, guarantee) from `index.html`.
4. This approach keeps the landing page content tied directly to the product listing.

---

## Step 6: Add Custom CSS via the Theme Editor

Because Shopify removes inline styles and `<style>` blocks from page and product content, your custom styles must live in the theme.

1. Go to **Online Store > Themes**.
2. On your active theme, click **Customize**.
3. In the bottom-left corner, click **Edit code** (or exit the customizer and use the **Actions > Edit code** option on the Themes page).
4. Open `assets/base.css` (or `assets/theme.css` depending on your theme).
5. Scroll to the bottom and paste in the custom CSS rules from your `index.html` `<style>` block.
6. Click **Save**.

> **Alternative:** In the theme editor sidebar, look for **Theme settings > Custom CSS** — some themes (like Dawn) provide a dedicated custom CSS input box here without requiring code editing.

---

## Step 7: Set Up the Dawn Theme (Recommended)

Dawn is Shopify's free, performance-optimized default theme — ideal for digital product stores.

1. Go to **Online Store > Themes**.
2. If Dawn is not your current theme, click **Explore free themes**, select **Dawn**, and click **Add**.
3. Once added, click **Customize** to open the visual theme editor.
4. Set your brand colors:
   - Go to **Theme settings > Colors**.
   - Set your primary color to match The Reset Co. brand palette.
5. Upload your logo:
   - Go to **Theme settings > Logo** and upload a PNG or SVG logo file.
6. Set your typography:
   - Go to **Theme settings > Typography** and select fonts that match your brand.
7. Configure the homepage:
   - Add a **Hero banner** section with a headline and a "Shop Now" button pointing to your product page.
   - Add a **Featured product** section and select "The Perimenopause Reset Workbook".
8. Click **Save**.

---

## Step 8: Connect Payment Methods

1. Go to **Settings > Payments** in your Shopify admin.
2. **Shopify Payments** (recommended):
   - Click **Complete account setup** under Shopify Payments.
   - Enter your banking and business details.
   - This enables credit/debit card payments with no third-party transaction fees.
3. **PayPal** (optional but recommended for digital products):
   - Under **Alternative payment methods**, click **Activate PayPal**.
   - Log in to your PayPal account to connect it.
4. **Apple Pay / Google Pay:**
   - These activate automatically when Shopify Payments is enabled and the customer's browser supports them.
5. Click **Save**.

> **Note:** If Shopify Payments is not available in your country, use **Stripe** or another supported provider under **Third-party payment providers**.

---

## Step 9: Add a Custom Domain

A custom domain (e.g., `shop.theresetco.com`) builds trust and brand recognition.

1. Go to **Settings > Domains**.
2. Click **Buy new domain** to purchase a domain through Shopify, or click **Connect existing domain** if you already own one.
3. If connecting an existing domain (e.g., from GoDaddy, Namecheap, Squarespace):
   - Copy the Shopify IP address and CNAME record shown on screen.
   - Log in to your domain registrar and update your DNS records accordingly.
   - DNS propagation can take up to 48 hours.
4. Once connected, click **Set as primary** to make it your store's main URL.

---

## Step 10: Test the Purchase Flow End-to-End

Before launching, complete a full test purchase to confirm everything works.

1. In your Shopify admin, go to **Settings > Payments**.
2. Under Shopify Payments, click **Manage**, then enable **Test mode**.
3. Visit your store's product page and add the workbook to the cart.
4. Go through checkout using Shopify's test credit card:
   - **Card number:** `4111 1111 1111 1111`
   - **Expiry:** Any future date
   - **CVV:** Any 3 digits
5. Complete the order.
6. Check that you receive:
   - An order confirmation email from Shopify.
   - A separate download link email from the Digital Downloads app.
7. Click the download link to confirm the PDF downloads correctly.
8. Go to **Orders** in your admin and verify the order appears.
9. Disable **Test mode** when you are satisfied everything works.
10. Announce your launch!

---

## Quick Launch Checklist

- [ ] Digital Downloads app installed
- [ ] Product created with correct price ($27), no shipping, no inventory tracking
- [ ] PDF uploaded and linked in Digital Downloads
- [ ] Download email customized with The Reset Co. branding
- [ ] Custom HTML/CSS from index.html integrated into theme
- [ ] Dawn theme configured with brand colors, logo, and fonts
- [ ] Payment methods activated (Shopify Payments + PayPal)
- [ ] Custom domain connected (optional but recommended)
- [ ] Test purchase completed successfully
- [ ] Test mode disabled before launch

---

*Guide prepared for The Reset Co. — The Perimenopause Reset Workbook digital store setup.*
