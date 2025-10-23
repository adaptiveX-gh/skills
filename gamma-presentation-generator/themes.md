# Gamma Presentation Theming System

## Overview

The theming system allows you to apply consistent branding (colors, typography, logos) across Gamma presentations. Themes are defined using CSS custom properties (variables) that can be easily swapped.

## How Themes Work

All theme values are stored in CSS custom properties in the `:root` selector. To apply a theme, simply replace the values in the `:root` block or add a theme-specific class to the `<body>` tag.

## Theme Structure

Each theme consists of:

1. **Colors**: Primary, secondary, accent, text colors, backgrounds
2. **Typography**: Font families, sizes, weights
3. **Branding**: Logo URL, brand name
4. **Spacing**: Card radius, padding values

## Available Themes

### 1. Default Theme (Gamma AI)

The standard Gamma AI color scheme with purple/blue gradients.

```css
:root {
    /* Colors */
    --gamma-primary: #5E5ADB;
    --gamma-secondary: #4A90E2;
    --gamma-accent: #FF6B6B;
    --text-primary: #1A1F36;
    --text-secondary: #4E5D78;
    --bg-gradient-start: #F8F9FD;
    --bg-gradient-end: #E8ECF4;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 20px;
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;
    --brand-name: '';
}
```

### 2. Bank Theme

Professional corporate theme for financial institutions. Clean, trustworthy design with conservative colors.

```css
:root {
    /* Colors */
    --gamma-primary: #383B3E;      /* Dark Corporate Gray */
    --gamma-secondary: #2A2D30;    /* Deeper Gray */
    --gamma-accent: #C41F3E;       /* Professional Red */
    --text-primary: #1A1F36;
    --text-secondary: #4E5D78;
    --bg-gradient-start: #F5F5F5;
    --bg-gradient-end: #E8E8E8;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: 'Whitney', 'Helvetica Neue', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 12px;           /* More corporate, less rounded */
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;              /* Add your bank's logo URL */
    --brand-name: '';
}
```

### 3. AdaptiveX Theme

Modern, innovative theme with deep purple accent. Perfect for design, innovation, and business transformation presentations.

```css
:root {
    /* Colors */
    --gamma-primary: #403c8b;      /* Gigas Purple - AdaptiveX brand color */
    --gamma-secondary: #322f6e;    /* Darker purple variant */
    --gamma-accent: #5a56b8;       /* Lighter purple accent */
    --text-primary: #1A1F36;
    --text-secondary: #4E5D78;
    --bg-gradient-start: #F8F7FC;
    --bg-gradient-end: #EFEDF7;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: 'Lexend Deca', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 16px;           /* Modern, rounded */
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;              /* Add AdaptiveX logo data URI */
    --brand-name: 'AdaptiveX';
}
```

### 4. Ocean Theme

Fresh, blue-green theme perfect for nature/environmental presentations.

```css
:root {
    /* Colors */
    --gamma-primary: #006994;      /* Deep ocean blue */
    --gamma-secondary: #0099CC;    /* Bright ocean */
    --gamma-accent: #00C9A7;       /* Turquoise accent */
    --text-primary: #1A1F36;
    --text-secondary: #4E5D78;
    --bg-gradient-start: #E0F7FA;
    --bg-gradient-end: #B2EBF2;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 20px;
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;
    --brand-name: '';
}
```

### 4. Sunset Theme

Warm, energetic theme with orange/red gradients.

```css
:root {
    /* Colors */
    --gamma-primary: #E74C3C;      /* Sunset red */
    --gamma-secondary: #F39C12;    /* Golden orange */
    --gamma-accent: #FF6B6B;       /* Coral accent */
    --text-primary: #2C3E50;
    --text-secondary: #5D6D7E;
    --bg-gradient-start: #FFF5E6;
    --bg-gradient-end: #FFE8CC;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 20px;
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;
    --brand-name: '';
}
```

### 5. Forest Theme

Natural, earthy theme with greens and browns.

```css
:root {
    /* Colors */
    --gamma-primary: #2E7D32;      /* Forest green */
    --gamma-secondary: #558B2F;    /* Light green */
    --gamma-accent: #8BC34A;       /* Fresh green accent */
    --text-primary: #1B5E20;
    --text-secondary: #4E5D78;
    --bg-gradient-start: #F1F8E9;
    --bg-gradient-end: #DCEDC8;
    --card-bg: #FFFFFF;

    /* Typography */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 20px;
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;
    --brand-name: '';
}
```

### 6. Minimal Dark Theme

Sleek, modern dark theme for tech presentations.

```css
:root {
    /* Colors */
    --gamma-primary: #BB86FC;      /* Purple accent */
    --gamma-secondary: #03DAC6;    /* Teal accent */
    --gamma-accent: #CF6679;       /* Pink accent */
    --text-primary: #E1E1E1;
    --text-secondary: #B0B0B0;
    --bg-gradient-start: #121212;
    --bg-gradient-end: #1E1E1E;
    --card-bg: #1E1E1E;

    /* Typography */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --font-base: max(16px, min(2vw, 18px));
    --font-h1: max(32px, min(6vw, 48px));
    --font-h2: max(24px, min(4vw, 36px));
    --font-h3: max(18px, min(3vw, 24px));

    /* Spacing */
    --max-width: 1100px;
    --card-radius: 8px;            /* Sharp, modern edges */
    --card-padding: 56px;
    --card-padding-mobile: 32px 24px;

    /* Branding */
    --logo-url: none;
    --brand-name: '';
}
```

## How to Apply a Theme

### Method 1: Replace :root values and Add Logo

Simply copy the theme's `:root` block and paste it into your presentation's `<style>` section.

**Important: Adding Your Logo**

Since presentations should be self-contained (Gamma AI philosophy), use one of these methods for logos:

**Option A: Inline SVG Data URI (Recommended)**
```css
--logo-url: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg">...</svg>');
```

**Option B: Base64 Encoded Image**
```css
--logo-url: url('data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAA...');
```

**Option C: External URL (Not Recommended)**
```css
--logo-url: url('https://your-cdn.com/logo.svg');
```
⚠️ Warning: External URLs may break if the server is down or blocks hotlinking (like Brandfetch does).

**How to Create a Data URI:**
1. Use online tool: https://yoksel.github.io/url-encoder/ (for SVG)
2. Or use: https://www.base64-image.de/ (for PNG/JPG)
3. Copy the data URI and paste into `--logo-url`

**Simple Placeholder Example:**
```css
--logo-url: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 200 60"><rect fill="%23C41F3E" width="200" height="60" rx="8"/><text x="100" y="38" font-family="Arial" font-size="24" font-weight="bold" fill="white" text-anchor="middle">COMPANY</text></svg>');
```

### Method 2: Add Header Banners to Content Slides

Add branded header banners to content slides (not hero/title slides) for a professional, corporate look:

```html
<section class="slide">
    <div class="gamma-card">
        <div class="card-content">
            <!-- Header Banner with Logo -->
            <div class="header-banner">
                <div class="banner-logo"></div>
                <h2>Your Slide Title</h2>
            </div>

            <!-- Regular content below -->
            <h3>Subsection</h3>
            <p>Content goes here...</p>
        </div>
    </div>
</section>
```

**Header Banner Variants:**

```html
<!-- Default: Red gradient with pattern overlay -->
<div class="header-banner">

<!-- Dark variant: Corporate gray gradient -->
<div class="header-banner dark">

<!-- Simple variant: No pattern overlay -->
<div class="header-banner simple">
```

The header banner:
- Uses theme accent color (red for Bank theme)
- Places logo on the right side
- Title overlays the banner in white
- Includes subtle pattern for visual interest
- Fully responsive on mobile devices

### Method 3: Add Logo to Title Slide

For themes with logos, add this to your title slide:

```html
<section class="slide">
    <div class="gamma-card">
        <div class="card-content center">
            <div class="brand-logo"></div>
            <h1>Presentation Title</h1>
            <p class="subtitle">Subtitle</p>
        </div>
    </div>
</section>
```

**Required CSS for Header Banners:**

```css
/* Header Banner - Corporate style with logo */
.header-banner {
    position: relative;
    background: linear-gradient(135deg, var(--gamma-accent), #D32F4F);
    margin: -56px -56px 32px -56px;
    padding: 48px 56px 80px 56px;
    min-height: 120px;
}

@media (max-width: 768px) {
    .header-banner {
        margin: -32px -24px 24px -24px;
        padding: 32px 24px 60px 24px;
        min-height: 100px;
    }
}

/* Logo in header banner - right aligned */
.header-banner .banner-logo {
    position: absolute;
    top: 24px;
    right: 56px;
    width: 120px;
    height: 40px;
    background-image: var(--logo-url);
    background-size: contain;
    background-repeat: no-repeat;
    background-position: right center;
    opacity: 0.95;
}

@media (max-width: 768px) {
    .header-banner .banner-logo {
        right: 24px;
        width: 100px;
        height: 32px;
    }
}

/* Title overlay on banner */
.header-banner h2 {
    color: #FFFFFF;
    text-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    margin-bottom: 0;
    position: relative;
    z-index: 1;
    background: none;
    -webkit-text-fill-color: #FFFFFF;
}

/* Pattern overlay for visual interest */
.header-banner::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background:
        linear-gradient(45deg, rgba(255,255,255,0.05) 25%, transparent 25%),
        linear-gradient(-45deg, rgba(255,255,255,0.05) 25%, transparent 25%),
        linear-gradient(45deg, transparent 75%, rgba(255,255,255,0.05) 75%),
        linear-gradient(-45deg, transparent 75%, rgba(255,255,255,0.05) 75%);
    background-size: 60px 60px;
    opacity: 0.3;
}

/* Variant: Simple header bar (no pattern) */
.header-banner.simple::before {
    display: none;
}

/* Variant: Dark header */
.header-banner.dark {
    background: linear-gradient(135deg, var(--gamma-primary), var(--gamma-secondary));
}
```

**When to Use Header Banners:**
- ✅ Content slides with data, lists, or information
- ✅ Section introduction slides (not the main title slide)
- ✅ Slides that need strong branding presence
- ❌ Hero/title slides (use centered logo instead)
- ❌ Slides with very little content
- ❌ Image-focused slides where banner would compete

**For centered logo on title slides, add this CSS:**

```css
.brand-logo {
    width: 200px;
    height: 60px;
    margin: 0 auto 32px;
    background-image: var(--logo-url);
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
}

@media (max-width: 768px) {
    .brand-logo {
        width: 150px;
        height: 45px;
        margin-bottom: 24px;
    }
}
```

### Method 3: Create Custom Theme

To create your own theme:

1. Start with the default theme structure
2. Replace color values with your brand colors
3. Update typography if you have custom fonts
4. Add your logo URL if needed
5. Adjust spacing/radius to match your brand guidelines

Example custom theme:

```css
:root {
    /* Your Brand Colors */
    --gamma-primary: #YOUR_PRIMARY_COLOR;
    --gamma-secondary: #YOUR_SECONDARY_COLOR;
    --gamma-accent: #YOUR_ACCENT_COLOR;
    --text-primary: #YOUR_TEXT_COLOR;
    --text-secondary: #YOUR_SECONDARY_TEXT_COLOR;
    --bg-gradient-start: #YOUR_BG_START;
    --bg-gradient-end: #YOUR_BG_END;
    --card-bg: #FFFFFF;

    /* Your Typography */
    --font-family: 'YourFont', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;

    /* Your Branding */
    --logo-url: url('YOUR_LOGO_URL');
    --brand-name: 'Your Brand';
}
```

## Theme Usage in CSS

The theme variables are used throughout the presentation CSS:

```css
/* Headings use gradient with theme colors */
h1 {
    background: linear-gradient(135deg, var(--gamma-primary), var(--gamma-accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}

/* Accent bar uses theme colors */
.gamma-card::before {
    background: linear-gradient(90deg, var(--gamma-primary), var(--gamma-accent));
}

/* Lists use theme primary color */
ul li::before {
    color: var(--gamma-primary);
}

/* Background uses theme gradient */
body {
    background: linear-gradient(180deg, var(--bg-gradient-start) 0%, var(--bg-gradient-end) 100%);
}
```

## Best Practices

1. **Contrast**: Ensure text colors have sufficient contrast against backgrounds (WCAG AA: 4.5:1 for body text)
2. **Brand Consistency**: Use official brand colors and fonts from brand guidelines
3. **Logo Placement**: Place logos on title slide and optionally in footer
4. **Testing**: Test your theme on mobile devices to ensure readability
5. **Color Harmony**: Use color theory - complementary, analogous, or triadic color schemes

## Accessibility Considerations

When creating custom themes:

- Maintain minimum contrast ratios (4.5:1 for normal text, 3:1 for large text)
- Don't rely on color alone to convey information
- Test with color blindness simulators
- Ensure logo has adequate contrast against background
- Keep font sizes above minimum readable values (16px)

## Integration with Brandfetch

You can use Brandfetch to automatically extract brand colors and logos:

1. Visit `https://brandfetch.com/DOMAIN.com`
2. Extract primary colors, accent colors, and logo URLs
3. Create a custom theme using those values
4. Apply to your presentation

Example Brandfetch extraction for a financial institution:
- Primary: #383B3E (Corporate gray)
- Accent: #C41F3E (Professional red)
- Logo: Extract from Brandfetch brand assets
- Typography: Corporate font family from brand guidelines
