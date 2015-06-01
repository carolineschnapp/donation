Add donation on cart page
=============

This quick tutorial will show you how to add a field for tip or donation to your cart page. It works by adding a product multiple times, worth $1, using [Ajax](https://docs.shopify.com/support/your-website/themes/can-i-use-ajax-api).

![Alt text](https://monosnap.com/file/BxCXbuyE5FrA7XnCcLTO3CeLeRCoIm.png)

This donation can only be added to the order on the Cart page at <kbd>/cart</kbd>. **This solution will not work in a cart drawer or cart popup.** You will need to disable any cart drawer or popup in your theme if you wish to continue.

This tutorial won't work for you if you use the **Lookbook** theme.

If your store uses **Classic**, **Pop**, **Solo**, or **Supply**, visit your [Customize theme page](//www.shopify.com/admin/themes/current/editor), look in the **Cart Page** section, and deselect the **Enable Ajaxify Cart** box.

If you use the **Brooklyn** theme, go to your [Customize theme page](//www.shopify.com/admin/themes/current/editor), look in the **Products** section, and deselect the **Enable slide-out shopping cart** box.

[View Demo](http://donation-tutorial.myshopify.com/)

#### Features
- Works with a donation product.
- If product has a $1 variant, an input box is presented for user to type in an amount. Goal is to add any amount of dollars as donation to the cart.
- Additional variants can be used for fixed amounts, e.g. $10, $50, $100, $250.
- If there's no $1 variant, then all variants are fixed amounts.
- Uses Ajax requests to update the cart.

#### Files Included
```
├── snippets
│   └── donation.liquid
```

#### How to use

1. Create a donation product. If you want an input box, add a variant of $1 to it.
2. If you want to provide fixed amount options, add those as variants to your product.
3. On the Navigation page, create a link list with handle 'donation'.
4. Include the <kbd>donation.liquid</kbd> snippet anywhere in the cart.liquid template.

#### Step by step instructions

1. Create a product for your donation. Name your product however you want. Remember to uncheck **This product requires shipping**, and optionally uncheck **Charge taxes on this product**.

2. To include a box (on your cart page) where the user inputs the exact dollar amount to donate, add a $1-priced variant to your product that also has the *Title* set to $1:

   ![Alt text](https://monosnap.com/file/CVqLZsAB3PAW1lO2MW7LUnr16348pb.png)

3. Add more variants if you want to list suggested amounts on your cart page:

   ![Alt text](https://monosnap.com/file/LrcHZGpFu1Ivxbc1kRAPbjRk4fc5JA.png)

4. If you only want to list suggested amounts, skip the $1-priced variant:

   ![Alt text](https://monosnap.com/file/coqOUUz8CcaJDFniwkq5DJqZuKsChD.png)

5. Create a link list called "Donation". **The link list name "Donation" is mandatory.**

6. Under the **Links** section, type in "Donation" for the <tt>Link Name</tt>.

7. Under <kbd>Links To...</kbd> select **Product**.

8. Click **Select a product** and choose the product you created, e.g. "Donation".

9. Click **Save**.

10. Go to the Edit HTML/CSS page in your Shopify admin.

11. Under the *Snippets* folder, click on **Add a new snippet** and type in "donation".

12. Copy (<code>command + c</code> on a Mac, <code>ctrl + c</code> on a PC) and paste (<code>command + v</code> on a Mac, <code>ctrl + v</code> on a PC) the [content from this link](https://raw.githubusercontent.com/carolineschnapp/donation/master/snippets/donation.liquid) to your snippet.

13. Click **Save**.

14. Paste the following code in your [cart.liquid](https://www.shopify.com/admin/themes/current?key=templates/cart.liquid) file. You may want to place it somewhere near your checkout button.
 
   ```liquid
   {% include 'donation' %}
   ```
   
15. Save your changes. You're done.

