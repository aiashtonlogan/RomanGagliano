# Logan Brands — Site Build Standards

## 1. Logan Brands Fixed Badge (every page, bottom-left)
- Logo: Logan_Brands_Logo.png, 55px wide, filter:invert(1), base64 embedded
- position: fixed, bottom: 20px, left: 20px, z-index: 999
- opacity: 0.4 default, 1.0 on hover, smooth transition
- Dark pill background: rgba(0,0,0,0.4), padding 8px 12px, border-radius 6px
- Links to https://www.loganbrands.com (new tab)

## 2. Logan Brands Footer Credit (centered at bottom of every site)
- Logo: Logan_Brands_Logo.png, 80px wide, filter:invert(1), base64 embedded
- Centered in footer
- Small text underneath: "Built by Logan Brands"
- opacity: 0.6 default, 1.0 on hover
- Links to https://www.loganbrands.com (new tab)

## 3. Mobile Cursor
- Hide ALL cursors on mobile/touch devices
- Add to every site's CSS:
@media (hover: none) and (pointer: coarse) {
  * { cursor: none !important; }
}

## 4. Logo Embedding
- Always base64 embed Logan_Brands_Logo.png
- Command:
  b64=$(base64 -w 0 "Logan_Brands_Logo.png") && sed -i "s|src=\"Logan_Brands_Logo.png\"|src=\"data:image/png;base64,$b64\"|g" index.html
