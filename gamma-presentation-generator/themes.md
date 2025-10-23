# Gamma Presentation Theming System

## Overview

The theming system allows you to apply consistent branding (colors, typography, logos) across Gamma presentations. Themes are defined using CSS custom properties (variables) that can be easily swapped.

## How Themes Work

All theme values are stored in CSS custom properties in the `:root` selector. To apply a theme, simply replace the values in the `:root` block or add a theme-specific class to the `<body>` tag.

## Theme Files

All theme definitions are available in `styles/themes.css`. This file contains:
- 7 pre-built themes (Default, Bank, AdaptiveX, Ocean, Sunset, Forest, Minimal Dark)
- Complete CSS custom properties for each theme
- Logo placeholders and examples

To use a theme:
1. Open `styles/themes.css`
2. Find the `.theme-{name}` class you want
3. Copy the :root variables from that theme
4. Paste into your presentation's `<style>` section

## Theme Structure

Each theme consists of:

1. **Colors**: Primary, secondary, accent, text colors, backgrounds
2. **Typography**: Font families, sizes, weights
3. **Branding**: Logo URL, brand name
4. **Spacing**: Card radius, padding values

## Available Themes

### 1. Default Theme (Gamma AI)

The standard Gamma AI color scheme with purple/blue gradients.

**Colors**: Purple (#5E5ADB), Blue (#4A90E2), Red accent (#FF6B6B)
**Style**: Modern, rounded (20px radius)
**Best For**: General presentations, tech talks, creative content

See `styles/themes.css` (`.theme-default`) for complete theme definition.

### 2. Bank Theme

Professional corporate theme for financial institutions. Clean, trustworthy design with conservative colors.

**Colors**: Dark Gray (#383B3E), Corporate Red (#C41F3E)
**Style**: Corporate, sharp (12px radius)
**Best For**: Financial presentations, corporate reports, professional decks

See `styles/themes.css` (`.theme-bank`) for complete theme definition.

### 3. AdaptiveX Theme

Modern, innovative theme with deep purple accent. Perfect for design, innovation, and business transformation presentations.

**Colors**: Gigas Purple (#403c8b), Light Purple accent (#5a56b8)
**Typography**: Lexend Deca font family
**Style**: Modern, rounded (16px radius)
**Best For**: Design sprints, innovation workshops, transformation presentations

See `styles/themes.css` (`.theme-adaptivex`) for complete theme definition.

### 4. Ocean Theme

Fresh, blue-green theme perfect for nature/environmental presentations.

**Colors**: Ocean Blue (#006994), Turquoise (#00C9A7)
**Style**: Fresh, rounded (20px radius)
**Best For**: Environmental topics, marine content, sustainability

See `styles/themes.css` (`.theme-ocean`) for complete theme definition.

### 5. Sunset Theme

Warm, energetic theme with orange/red gradients.

**Colors**: Sunset Red (#E74C3C), Golden Orange (#F39C12)
**Style**: Warm, energetic (20px radius)
**Best For**: Creative presentations, energetic talks, warm topics

See `styles/themes.css` (`.theme-sunset`) for complete theme definition.

### 6. Forest Theme

Natural, earthy theme with greens and browns.

**Colors**: Forest Green (#2E7D32), Fresh Green (#8BC34A)
**Style**: Natural, rounded (20px radius)
**Best For**: Eco-friendly content, nature topics, sustainability

See `styles/themes.css` (`.theme-forest`) for complete theme definition.

### 7. Minimal Dark Theme

Sleek, modern dark theme for tech presentations.

**Colors**: Purple (#BB86FC), Teal (#03DAC6), Pink accent (#CF6679)
**Style**: Dark, sharp (8px radius)
**Best For**: Tech presentations, developer talks, modern content

See `styles/themes.css` (`.theme-dark`) for complete theme definition.

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

All header banner styles are included in `styles/core.css` (lines 271-341). Copy the entire core.css file into your `<style>` section to use header banners.

**Key features of header banner CSS:**
- Uses theme accent color for gradient background
- Logo positioned on right side
- White text overlay with shadow
- Pattern overlay for visual interest (can be disabled with `.simple` class)
- Fully responsive for mobile devices
- Dark variant available with `.dark` class

**When to Use Header Banners:**
- ✅ Content slides with data, lists, or information
- ✅ Section introduction slides (not the main title slide)
- ✅ Slides that need strong branding presence
- ❌ Hero/title slides (use centered logo instead)
- ❌ Slides with very little content
- ❌ Image-focused slides where banner would compete

**Required CSS for Centered Logo:**

The `.brand-logo` styles are included in `styles/core.css` (lines 96-120). Copy the entire core.css file into your `<style>` section to use centered logos.

**Key features:**
- Centered with auto margins
- 200px wide on desktop, 150px on mobile
- Responsive sizing for all devices
- Uses `--logo-url` theme variable

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

Theme variables are automatically applied throughout the presentation CSS in `styles/core.css`. The core styles use CSS custom properties (variables) to apply your theme consistently across:

- **Headings**: Gradient text using `--gamma-primary` and `--gamma-accent`
- **Accent bars**: Top border on cards using theme colors
- **Lists**: Bullet points and numbers styled with `--gamma-primary`
- **Background**: Body gradient using `--bg-gradient-start` and `--bg-gradient-end`
- **Typography**: Font families from `--font-family`
- **Spacing**: Card radius and padding from theme variables

See `styles/core.css` for complete implementation details.

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
