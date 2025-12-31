# Empath Grief Care Support Groups Website

A professional, single-page website displaying grief support group schedules and information for Empath Health across multiple Florida service areas.

## Brand Colors

This site uses Empath Health's official brand color palette:

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| Deep Eggplant | `#3D1951` | Primary typeface, headers, navbar background |
| Purple (Outer Petal) | `#8431A5` | Card borders, accents, links, buttons |
| Deep Pink (Second Petal) | `#CD5599` | Hover states, bullet points, interactive elements |
| Orange (Inner Petal) | `#FF4338` | Available for CTAs and emphasis |
| Gray (Support Color) | `#BDBBBC` | Information boxes, subtle backgrounds |

## Service Areas

The website covers grief support groups across five service areas:

1. **Marion County** - Hospice of Marion County Area
2. **Hillsborough & Pinellas Counties** - Suncoast Hospice Areas
3. **DeSoto, Charlotte, Manatee, and Sarasota Counties** - Tidewell Hospice Area
4. **Broward & Palm Beach Counties** - Trustbridge Area
5. **Virtual & Special Events** - Hosted by Tidewell Hospice

## Features

### Smart Filtering
- **Sticky navigation bar** with area-specific filter buttons
- Filter by geographic area or view all groups at once
- Special filter for virtual seminars and special events
- Smooth scrolling to filtered sections

### Interactive Location Cards
- **Click any group session card** to open Google Maps with the location
- All addresses pre-mapped for instant directions
- Visual indicator (📍) on each location
- Hover effects show cards are interactive

### User Experience
- **Responsive design** - Works seamlessly on desktop, tablet, and mobile
- **Clickable logo** - Links back to empathhealth.org/grief-services
- **Click-to-call phone numbers** for mobile users
- **Clean visual hierarchy** - White cards on light gray backgrounds
- **Professional typography** - Poppins font from Google Fonts

### Group Types

The site displays various support group categories:
- Friends in Grief
- Traumatic Loss
- Child Loss
- Spousal/Partner Loss (multiple levels)
- Parent Loss
- Adult Child Loss
- General Grief & Loss
- Living with Suicide Loss
- Virtual Seminars
- Special Events

## Deployment

This site is hosted on **Cloudflare Pages** and automatically deploys from the `main` branch.

### Production URL
[Grief Groups Landing Page](https://empath-grief-care-landing.pages.dev/)

### Automatic Deployment
1. Push changes to the `main` branch on GitHub
2. Cloudflare Pages automatically detects the changes
3. Site rebuilds and deploys in ~60 seconds
4. Changes are live

## Local Development

This is a static HTML site - no build process required!

Simply open `index.html` in any modern web browser to view the site locally.

## Updating Content

### To Update Group Schedules:
1. Edit the `index.html` file
2. Find the appropriate service area section
3. Update dates, times, or add/remove group sessions
4. Commit and push to `main` branch

### To Add New Locations:
1. Add the group session HTML in the appropriate section
2. Update the `locationAddresses` object in the JavaScript at the bottom of `index.html`
3. Add the address in format: `'Location Name': 'Full Address with City, State, ZIP'`

### Example:
```javascript
locationAddresses = {
    'New Location Name': '123 Main Street, City, FL 12345',
    // ... existing addresses
};
```

## Design System

### Color Variables
All colors are defined as CSS variables in the `:root` selector for easy maintenance:

```css
:root {
    --empath-eggplant: #3D1951;
    --empath-purple: #8431A5;
    --empath-pink: #CD5599;
    --empath-orange: #FF4338;
    --empath-gray: #BDBBBC;
}
```

### Typography
- **Font Family**: Poppins (Google Fonts)
- **Weights Used**: 300, 400, 500, 600, 700

### Component Structure
- `.service-area` - Main section containers
- `.group-category` - Category headers with colored bullets
- `.group-session` - Individual clickable group cards
- `.filter-bar` - Sticky navigation with filter buttons

## Contact Information

**For Registration & Information:**
Phone: [(888) 308-7150](tel:8883087150)

**For Virtual Seminar Registration:**
Email: jspurr@empathhealth.org

**For Spanish Virtual Group Registration:**
Phone: [(727) 244-4514](tel:7272444514)

## Related Links

- [Empath Health Main Site](https://empathhealth.org)
- [Grief Services Page](https://empathhealth.org/grief-services)

## File Structure

```
empath-grief-care/
├── index.html          # Main website file (single-page application)
├── README.md           # This file
└── .gitignore          # Git ignore rules
```

## Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile Safari (iOS)
- ✅ Chrome Mobile (Android)

## Contributing

This website is maintained for Empath Health. For content updates or corrections, please contact Ryan McKee @ Evenstar MSP (941) 222-2002.

## License

Created for Empath Health - All rights reserved.

---

**Built with ❤️ for Empath Health**  
*Here for the Full Life*
