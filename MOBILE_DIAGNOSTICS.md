# Mobile Display Issues - Diagnostic Information

## Issues Reported
1. **Get the Mat page**: All images are broken on mobile
2. **Homepage**: Bottom sections not loading, only partially transparent background images

## Investigation Findings

### Product Page Images
- Product page images are present in the HTML
- Images load from `https://korumat.com/cdn/shop/products/` and use protocol-relative URLs
- Images should work on mobile if lazy-loading JavaScript is functioning

### Homepage Background Sections
- Uses `background-media-text` sections with responsive images
- Mobile fallback CSS sets `background: #f4f4f4` (light gray) when images fail to load
- Protocol-relative URLs: `//korumat.com/cdn/shop/files/...`
- Local relative URLs: `cdn/shop/files/...`

### Potential Causes
1. **Lazy-loading JavaScript not loading on mobile** - Theme uses `lazyload` library
2. **Protocol-relative URL issues** on custom domain setup
3. **Mobile browser loading external CDN slower** causing visible gaps
4. **CORS or security policy blocking** certain resources

### Files to Check on Mobile
1. `cdn/shop/t/9/assets/vendor-v2.js` (lazy-loading library)
2. `cdn/shop/t/9/assets/theme*.js` (theme JavaScript)
3. `cdn/shop/t/9/assets/theme.scss*.css` (theme styles)
4. Product images from korumat.com CDN

### Next Steps
1. Test site on actual mobile device browser console
2. Check network tab for failed resource loads
3. Verify CNAME/custom domain DNS setup isn't blocking resources
4. Consider converting protocol-relative URLs to absolute HTTPS URLs

