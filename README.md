Add donation on cart page
=============

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
4. Include the <tt>donation.liquid</tt> snippet anywhere in the cart.liquid template.