# shopify-debug-engine
Lightweight Shopify Debug Dashboard for storefront debugging

![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

A lightweight, production-safe debugging dashboard for Shopify themes — built to inspect real storefront state without switching to admin.

---

## Why this exists

Debugging Shopify themes is rarely about fixing code.

It’s about understanding:
- why data is missing
- why a section behaves differently across templates
- why logic silently fails

Instead of jumping between admin, theme files, and console — this dashboard brings everything into one place.

---

## What it does

The Debug Engine runs inside the storefront and exposes:

### Context
- Page type
- Template detection

### Product & Cart
- Variant state
- Availability
- Cart totals

### Metafields
- Product, Collection, Customer, Shop
- Type-aware rendering

### Metaobjects
- Structured content debugging

### Sections & Blocks
- Active blocks
- Empty section detection

### Logic Signals
- Sale logic
- Template mismatch
- Data presence checks

---

## Debug Engine (Key Feature)

Instead of just showing data, it detects issues:

Examples:

- ⚠ Missing metafield used in UI  
- ⚠ Variant unavailable but button active  
- ⚠ Empty section after merchant edit  
- ⚠ Template and object mismatch  

This turns debugging from guessing into visibility.

---

## Installation

1. Add snippets:

/snippets/dev-dashboard.liquid  

2. Include in `theme.liquid` before closing body:

{% render 'dev-dashboard' %}

3. Enable debug mode:

?debug=1
or in editor mode in admin
---

## Quick Demo

Open any page and add:

?debug=1

The dashboard will appear in the bottom-right corner showing live store data and issues.

---

## Safety

- Hidden by default  
- Works on live stores  
- No frontend impact  
- No dependency on apps  

---

## Use Cases

- Debugging metafields not rendering  
- Understanding section behavior across templates  
- Verifying cart and product state  
- Identifying silent logic failures  

---

## Philosophy

Most Shopify issues are not errors — they are state problems.

This tool helps you see that state clearly.

---

## Future Improvements

- Severity-based issue detection  
- Namespace auto-detection  
- Variant-level debugging  
- UI enhancements  

---

## Contributing

Feel free to fork, extend, or adapt for your own workflow.

---

## License

MIT
