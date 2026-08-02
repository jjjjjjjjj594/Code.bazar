# CodeBazaar — Setup Guide

## What's included
A code marketplace with search + category tabs, a full product detail page
per listing (image gallery, features, installation guide, requirements,
version/changelog, FAQ, and genuine rating/reviews), and a UPI + email
purchase flow.

## ⚠️ Zaroori: images folder bhi upload karo
Site ke saath ek `images/` folder bhi hai jisme har product ke screenshots
hain. GitHub (ya jahan bhi host karo) par:

1. `index.html` upload karo
2. Ek naya folder banao naam **`images`** (bilkul yahi naam, chhote letters)
3. Us `images` folder ke andar, saari `.png` files upload karo jo iske saath
   di gayi hain

Agar `images` folder missing hoga ya galat naam ka hoga, to product detail
page me photos nahi dikhengi (bas khaali box dikhega) — baaki sab kaam
karega.

## Rating & Reviews — important note
Koi fake review nahi dala gaya hai — har product "No reviews yet" se start
hota hai. Jab bhi koi asli customer kharide, wo khud apna review de sakta hai
(5-star rating + text). Reviews us buyer ke apne browser me save hote hain
(localStorage) — koi shared/global database nahi hai, isliye ye completely
static site rehti hai, koi backend nahi chahiye.

## Adding a new product to the store
`index.html` khol kar `PRODUCTS` array me naya entry add karo:
```js
{
  id: 18,
  name: 'yourfile.zip',
  title: 'Product Name',
  desc: 'Short description...',
  tag: 'javascript',
  price: 99,
  tags: ['html','css'],
  gumroadUrl: '',
  images: ['images/yourimage_1.png'],
  version: 'v1.0',
  lastUpdated: 'Jul 2026',
  fileSize: '8 KB',
  features: ['Feature one', 'Feature two'],
  install: ['Step one', 'Step two'],
  requirements: 'Any modern browser...',
  changelog: [{ v:'v1.0', d:'Jul 2026', note:'Initial release' }],
  faq: [{ q:'Question?', a:'Answer.' }]
}
```

## Files in this delivery
- `index.html` — the full site
- `images/` — screenshots used in each product's gallery
