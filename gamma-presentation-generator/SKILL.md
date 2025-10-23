---
name: gamma-presentation-generator
description: Content-first presentation generator that transforms ideas, documents, and outlines into Gamma AI-style vertical scrolling presentations. Generates self-contained HTML with mobile-responsive cards that grow to fit content. Includes comprehensive theming system with brand color support (uses Brandfetch for automatic brand extraction). No reveal.js or external dependencies. This skill should be used when users request presentation creation, slide generation, pitch deck building, or content conversion to presentation format.
---

# Gamma Presentation Generator

## Purpose

Transform ideas, outlines, documents, or natural language prompts into Gamma AI-style vertical scrolling presentations. This skill generates self-contained HTML files with mobile-responsive cards that prioritize readability and accessibility. Unlike traditional slide-based presentations, Gamma presentations use vertical scrolling with cards that expand to fit content - ensuring perfect readability on all devices from phones to large displays.

## Core Philosophy

**Gamma AI Vertical Scrolling**: This skill generates presentations that embrace the Gamma AI philosophy - vertical scrolling with responsive cards that grow to fit content. Key principles:

1. **Vertical Navigation**: Natural scrolling like a webpage, not horizontal slide clicking
2. **Cards Grow on Mobile**: Content determines card height; text never shrinks below readable sizes (16px minimum)
3. **Self-Contained HTML**: No external dependencies or CDN links; presentations work offline
4. **Content-First Approach**: Narrative structure and compelling content over visual gimmicks
5. **Progressive Enhancement**: Accessible core content enhanced with JavaScript features
6. **Mobile-First Design**: Optimized for phones first, then tablets and desktops

**This skill excels at:**

1. **Intelligent Content Organization**: Taking raw ideas and structuring them into logical, persuasive narratives
2. **Adaptive Structuring**: Applying appropriate narrative frameworks based on presentation goals
3. **Gamma-Style HTML Generation**: Creating self-contained, accessible presentations that work on all devices
4. **Smart Enhancements**: Adding visual suggestions, speaker notes, statistics, and call-to-action elements

## When to Use This Skill

Trigger this skill when users request:

### Creation Requests
- "Create a presentation about [topic]"
- "Build a pitch deck for [product/service]"
- "Generate training slides on [subject]"
- "Make slides for my talk about [topic]"

### Conversion Requests
- "Turn this document into a presentation"
- "Convert these notes to slides"
- "Make this into Gamma format"
- "Transform this outline into a deck"

### Enhancement Requests
- "Add visuals to these slides"
- "Expand this outline into a full presentation"
- "Make this more engaging"
- "Improve the flow of this deck"

### Theming Requests
- "Apply [brand name] theme to this presentation"
- "Use [company] colors and branding"
- "Create a presentation with [color] theme"
- "Brand this presentation for [organization]"

## Theming System

The gamma-presentation-generator includes a comprehensive theming system that allows you to apply consistent branding (colors, typography, logos) to presentations.

### Available Themes

**Default Theme (Gamma AI)**: Purple/blue gradients with modern design
**Bank Theme**: Professional corporate theme for financial institutions (#383B3E, #C41F3E)
**AdaptiveX Theme**: Modern innovation theme with deep purple (#403c8b) for design/transformation
**Ocean Theme**: Fresh blue-green theme for nature/environmental presentations
**Sunset Theme**: Warm orange/red gradients for energetic presentations
**Forest Theme**: Natural greens and browns for eco-friendly content
**Minimal Dark**: Sleek dark theme for tech presentations

See `gamma-presentation-generator/themes.md` for complete theme documentation and all available theme presets.

### How to Apply Themes

1. **Identify brand colors**: Use tools like Brandfetch (https://brandfetch.com/domain.com) to extract brand colors and logos
2. **Select or create theme**: Choose from presets or create custom theme with brand colors
3. **Replace :root values**: Update CSS custom properties in the HTML template
4. **Add logo**: Include brand logo using the `.brand-logo` class
5. **Test on mobile**: Ensure brand colors have sufficient contrast and readability

### Theme Structure

Themes use CSS custom properties (variables) for easy customization:

```css
:root {
    --gamma-primary: #5E5ADB;      /* Primary brand color */
    --gamma-accent: #FF6B6B;        /* Accent/CTA color */
    --text-primary: #1A1F36;        /* Main text color */
    --text-secondary: #4E5D78;      /* Secondary text color */
    --bg-gradient-start: #F8F9FD;   /* Background gradient start */
    --bg-gradient-end: #E8ECF4;     /* Background gradient end */
    --card-bg: #FFFFFF;             /* Card background */
    --font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    --card-radius: 20px;            /* Card border radius */
    --logo-url: url('LOGO_URL');    /* Brand logo URL */
}
```

### Using Brandfetch for Brand Theming

When users request branded presentations:

1. Visit `https://brandfetch.com/[company-domain].com`
2. Extract:
   - Primary colors (hex codes)
   - Accent colors
   - Logo URLs (SVG or PNG)
   - Typography/fonts
3. Create theme using extracted values
4. Apply to presentation

Example: For a financial institution using the Bank theme:
- Primary: #383B3E (Corporate gray)
- Accent: #C41F3E (Professional red)
- Logo: Extract logo URL from Brandfetch
- Typography: Professional corporate fonts

## Instructions

When a user requests a presentation, follow these steps to generate a Gamma AI-style vertical scroll presentation:

### 1. Identify the Request Type

Recognize these triggers:
- "Create a presentation about [topic]"
- "Build slides for [subject]"
- "Generate a deck on [topic]"
- "Make a presentation from [content/file]"
- "Convert [document] to slides"

### 2. Gather Requirements

Ask clarifying questions if not provided:
```
- Topic/Subject (required)
- Purpose: Inform/Educate/Persuade/Inspire
- Audience: Technical/Executive/General/Students
- Length: Number of slides or presentation duration
- Style: Professional/Creative/Academic/Casual
```

### 3. Generate Presentation Structure

Create this markdown format with `---` separating slides:

```markdown
# [Main Title]
[Subtitle or tagline]

---

## [Section Title]

[Content with bullet points, paragraphs, or features]

---

## [Next Section]

### [Subsection if needed]
- Point 1
- Point 2
- Point 3

---
```

### 4. Content Generation Rules

#### For Title Slides:
```markdown
# [Compelling Title]
[Descriptive subtitle that sets context]
[Optional: Date, presenter name, or organization]
```

#### For Content Slides:
```markdown
## [Clear Section Header]

[Introduction paragraph if needed]

- [Concise bullet point]
- [Another key point]
- [Supporting information]

> [Important quote or callout if relevant]
```

#### For Feature/Benefit Slides:
```markdown
## [Section Title]

🚀 **[Feature Name]**
[Brief description of the feature]

💡 **[Another Feature]**
[Description of this feature]

🎯 **[Third Feature]**
[Description of the third feature]
```

#### For Data/Statistics Slides:
```markdown
## [Data Section Title]

**Key Metrics:**
- [Metric 1]: [Value]
- [Metric 2]: [Value]
- [Metric 3]: [Value]

[Explanatory paragraph about what the data means]
```

#### For Conclusion/CTA Slides:
```markdown
## [Conclusion Title]

### Key Takeaways
1. [Main point 1]
2. [Main point 2]
3. [Main point 3]

**[Call to action or next steps]**
```

### 5. Apply Content Guidelines

**Length Guidelines:**
- Title slides: 1-2 sentences
- Content slides: 3-7 bullet points OR 2-3 short paragraphs
- Feature slides: 3-6 features with descriptions
- Data slides: 3-5 key metrics with context

**Writing Style:**
- Use active voice
- Keep sentences under 20 words when possible
- One idea per bullet point
- Avoid jargon unless audience is technical
- Use concrete examples over abstract concepts

**Visual Suggestions:**
When appropriate, suggest images by adding:
```markdown
<!-- Image suggestion: [description of ideal image] -->
```

### 6. Slide Count by Presentation Type

- **5-minute pitch**: 5-7 slides
  1. Title/Hook
  2. Problem
  3. Solution
  4. Benefits/Features
  5. Traction/Proof
  6. Ask/CTA

- **10-minute presentation**: 8-12 slides
  1. Title
  2. Agenda/Overview
  3-9. Main content (6-7 slides)
  10. Summary
  11. Q&A/Contact

- **Educational/Training**: 15-20 slides
  1. Title
  2. Learning objectives
  3-17. Content with examples
  18. Recap
  19. Resources
  20. Questions

- **Status Update**: 6-8 slides
  1. Title
  2. Executive Summary
  3. Progress/Achievements
  4. Challenges
  5. Solutions/Mitigations
  6. Next Steps
  7. Timeline
  8. Questions

### 7. Output Format

Generate a vertical-scrolling HTML document using the template structure. Always provide:

1. **Self-contained HTML file** (no external dependencies)
2. **Vertical scrolling navigation** (not horizontal slides)
3. **Mobile-responsive cards** (that grow to fit content)
4. **Minimum readable font sizes** (never shrink below 16px)

#### Template Usage:

Use `templates/template.html` as the base structure. Follow these steps:

1. **Copy template.html**
2. **Select theme** from `styles/themes.css` and paste :root variables
3. **Copy core styles** from `styles/core.css` into the <style> section
4. **Replace placeholders** ({{PRESENTATION_TITLE}}, {{SLIDE_TITLE}}, etc.) with actual content
5. **Add/remove slides** as needed for the presentation length

#### Quick Reference - File Locations:

- **Template**: `gamma-presentation-generator/templates/template.html`
- **Themes**: `gamma-presentation-generator/styles/themes.css`
- **Core CSS**: `gamma-presentation-generator/styles/core.css`
- **Documentation**: `gamma-presentation-generator/themes.md`

#### Minimal HTML Structure:

See `templates/template.html` for the complete structure. Key elements:

```html
<!-- 1. Define theme variables (copy from styles/themes.css) -->
<style>
    :root {
        --gamma-primary: #403c8b;  /* Your brand color */
        --gamma-accent: #5a56b8;    /* Accent color */
        --logo-url: url('data:image/...');  /* Logo as data URI */
        /* ... other theme variables ... */
    }
    /* 2. Include core.css styles here */
</style>

<!-- 3. Add slide structure -->
<main class="presentation">
    <section class="slide">
        <div class="gamma-card">
            <div class="card-content">
                <h2>Slide Title</h2>
                <p>Content here...</p>
            </div>
        </div>
    </section>
</main>

<!-- 4. Add JavaScript for interactivity -->
<script>
    /* Copy JavaScript from template.html */
</script>
```

**For complete examples:** See the presentation files in the repository:
- `niagara-falls-bank-theme.html`
- `niagara-falls-adaptivex-theme.html`
- `niagara-falls-gamma.html`

### 8. Integration with Other Skills

When other skills are available, enhance the presentation:

```javascript
// If image-generation skill is available:
if (skills.includes('image-generation')) {
    // Add note: "<!-- Generate image: [prompt] -->"
}

// If data-visualization skill is available:
if (skills.includes('data-visualization')) {
    // Add note: "<!-- Create chart: [data description] -->"
}

// If content-research skill is available:
if (skills.includes('content-research')) {
    // Add note: "<!-- Research needed: [topic] -->"
}
```

### 9. Error Handling

If unable to generate presentation:
- Explain why (missing information, unclear request)
- Provide a template the user can fill in
- Offer to generate a different type of presentation

### 10. Quality Checklist

Before outputting, verify:
- [ ] Clear narrative flow from slide to slide
- [ ] No slide has too much content (max 150 words)
- [ ] Each slide has a clear purpose
- [ ] Consistent formatting throughout
- [ ] Opening hooks audience attention
- [ ] Closing has clear next steps
- [ ] Content matches stated audience level
- [ ] Total length appropriate for time limit

### Examples of Complete Flows

#### Example 1: Business Pitch
**Input**: "Create a pitch deck for our AI tutoring app"

**Output**:
```markdown
# EduAI: Personalized Learning at Scale
Revolutionizing education with AI-powered tutoring
October 2024

---

## The Problem

### Education is Failing Students
- 68% of students struggle with standard teaching pace
- 1-on-1 tutoring costs $40-100/hour
- Teachers overwhelmed with 30+ students per class
- Learning gaps compound over time

---

## Our Solution

### AI Tutoring That Adapts to Every Student

🧠 **Personalized Learning Paths**
Adjusts difficulty and pace in real-time

💬 **24/7 Availability**
Students get help whenever they need it

📊 **Progress Analytics**
Teachers and parents see detailed insights

💰 **Affordable Access**
$9.99/month vs $400+/month for human tutors

---

[Continue with more slides...]
```

### Final Notes

**CRITICAL - Gamma AI Philosophy:**
- **Always generate self-contained HTML files** - No reveal.js or external dependencies
- **Vertical scrolling ONLY** - Never use horizontal slide navigation
- **Cards grow on mobile** - Use `height: auto !important` on mobile viewports
- **Enforce minimum font sizes** - Use CSS `max()` to prevent text shrinking below 16px
- **Content determines card height** - Never use fixed heights that cut off content
- **Progressive enhancement** - Works without JavaScript, enhanced with it
- **Semantic HTML** - Proper heading hierarchy and accessibility

**Content Guidelines:**
- Prioritize clarity over cleverness
- When in doubt, use fewer words
- Test on mobile devices (the most important viewport)
- Ensure all content is readable without zooming

**The Result:**
Self-contained, accessible, mobile-first presentations that work offline and look beautiful on all devices - from 4" phones to 27" monitors. This is the Gamma AI advantage.

## Workflow

### Step 1: Understand the Input

Accept and process multiple input types:

**Natural Language Prompts**:
- "Create a presentation about sustainable energy with 5 main points"
- "Build a sales pitch for our new SaaS product"

**Markdown Files**:
- Clean, structured input that can be enhanced

**Bullet Points/Outlines**:
- Quick thoughts that need expansion and structure

**Existing Documents**:
- Content that needs restructuring into presentation format

### Step 2: Determine Presentation Goal

Ask the user (if not clear from context) what their goal is:

**Teaching/Educational**:
- Structure: Concept → Example → Practice
- Focus: Clear explanations, step-by-step progression
- Template: `templates/educational.md`

**Selling/Pitching**:
- Structure: Problem → Solution → Benefits → Proof
- Focus: Emotional resonance, clear value proposition
- Template: `templates/pitch-deck.md`

**Informing/Reporting**:
- Structure: Overview → Details → Summary
- Focus: Clear data presentation, key takeaways
- Template: `templates/status-update.md`

**Inspiring/Storytelling**:
- Structure: Setup → Conflict → Resolution
- Focus: Emotional arc, relatability, transformation
- Template: `templates/storytelling.md`

**Training/Workshop**:
- Structure: Theory → Demo → Hands-on → Reflection
- Focus: Interactive elements, practice exercises
- Template: `templates/workshop.md`

### Step 3: Apply Appropriate Structure

Based on the goal, select and apply the right narrative framework from the templates directory:

- `templates/pitch-deck.md` - For fundraising, sales pitches, product launches
- `templates/educational.md` - For courses, tutorials, how-to presentations
- `templates/status-update.md` - For project updates, quarterly reviews, team reports
- `templates/workshop.md` - For hands-on training sessions, interactive learning
- `templates/storytelling.md` - For narrative-driven talks, case studies, journey stories

Each template provides:
- Proven slide sequences
- Section descriptions
- Content guidelines
- Visual recommendations

### Step 4: Apply Layout Patterns

For each slide, recommend appropriate layout patterns from the `layouts/` directory:

**Hero Slide** (`layouts/hero-slide.md`):
- Opening slides
- Section breaks
- Key messages
- Powerful quotes

**Feature Grid** (`layouts/feature-grid.md`):
- Product features
- Team members
- Benefits lists
- Service offerings

**Timeline** (`layouts/timeline.md`):
- Roadmaps
- Company history
- Project phases
- Process flows

**Comparison** (`layouts/comparison.md`):
- Pricing tiers
- Before/after
- Us vs competitors
- Option evaluation

**Data Visualization** (`layouts/data-viz.md`):
- Metrics and KPIs
- Survey results
- Financial data
- Analytics

### Step 5: Enhance Content

Add intelligent enhancements to raw content:

**Visual Suggestions**:
- "This data would work well as a bar chart"
- "Consider adding a timeline here"
- "Use a comparison table for these options"
- Include layout hints in comments

**Speaker Notes**:
- Add speaking points below slides
- Include transitions and pacing notes
- Suggest emphasis points

**Supporting Data**:
- Add relevant statistics when appropriate
- Include industry benchmarks
- Suggest places for case studies

**Call-to-Action**:
- End with clear next steps
- Include contact information
- Provide follow-up resources

### Step 6: Optimize for Readability

Apply content intelligence rules:

**Slide Pacing**:
- Max 3-5 bullet points per slide
- Max 10-15 words per bullet
- Suggest splitting dense slides

**Visual Hierarchy**:
- Use H1 (#) for slide titles
- Use H2 (##) for main sections
- Use H3 (###) for grid items or sub-sections
- Use lists for sequential information

**Readability**:
- Short sentences
- Active voice
- Strong verbs
- Concrete examples

**Mobile-Friendly**:
- Content scales on small screens
- Images have proper aspect ratios
- Minimum font sizes enforced

## Output Format

Generate markdown with the following structure:

```markdown
# [Slide Title]

[Optional subtitle or key message]

[Main content with proper formatting]

---

<!-- Layout suggestion: hero-slide -->
<!-- Visual: Consider adding background image -->
<!-- Speaker note: Pause here for questions -->
```

Include helpful comments for:
- Layout recommendations
- Visual suggestions
- Speaker notes
- Timing hints
- Transition cues

## Best Practices

### Content Intelligence

**Auto-sectioning**:
- Break long content into logical slides
- Group related information
- Create natural flow between sections

**Visual Suggestions**:
- Recommend specific layouts based on content type
- Suggest when data needs visualization
- Identify opportunities for diagrams or images

**Pacing Detection**:
- Flag slides with too much content
- Recommend splitting complex ideas
- Suggest combining sparse slides

### Narrative Structure

**Opening Strong**:
- Hook the audience immediately
- Set clear expectations
- Establish credibility

**Building Momentum**:
- Logical progression of ideas
- Each slide builds on previous
- Maintain audience engagement

**Closing Powerfully**:
- Summarize key takeaways
- Clear call-to-action
- Memorable ending

### Technical Details

**Slide Separators**:
Use `---` to separate slides:
```markdown
# Slide 1

Content here

---

# Slide 2

More content
```

**Lists and Formatting**:
- Use `-` or `*` for bullet points
- Use `1.` `2.` for numbered lists
- Use `>` for blockquotes
- Use triple backticks for code

**Images and Media**:
```markdown
![Alt text](image-url)
```

**Tables**:
```markdown
| Column 1 | Column 2 |
|----------|----------|
| Data     | Data     |
```

## Common Patterns

### Quick Starters

**10-Minute Talk**:
- 8-10 slides total
- ~1 minute per slide
- Heavy on visuals, light on text
- Clear story arc

**5-Minute Pitch**:
- 5-7 slides total
- Problem → Solution → Traction → Ask
- Focus on key metrics
- Strong visual impact

**Workshop Introduction**:
- Include agenda slide
- Learning objectives
- Interactive elements
- Resources slide at end

### Content Transformation

**From Bullet Points**:
1. Identify main themes
2. Group related points
3. Create slide titles from themes
4. Expand bullets into full thoughts
5. Add context and examples

**From Long-Form Text**:
1. Extract key messages
2. Create slide titles from headers
3. Summarize paragraphs into bullets
4. Pull out quotes and statistics
5. Add visual breaks

**From Data/Spreadsheets**:
1. Identify story in the numbers
2. Choose appropriate visualizations
3. Highlight key insights
4. Provide context for metrics
5. Show trends and patterns

## Quality Checklist

Before finalizing a presentation, verify:

**Structure**:
- [ ] Clear beginning, middle, end
- [ ] Logical flow between slides
- [ ] Appropriate template applied
- [ ] Consistent formatting

**Content**:
- [ ] Each slide has one main idea
- [ ] Text is concise and scannable
- [ ] Examples and data support points
- [ ] Speaker notes included where helpful

**Design Guidance**:
- [ ] Layout suggestions provided
- [ ] Visual recommendations included
- [ ] Accessibility considerations noted
- [ ] Mobile-friendly formatting

**Completeness**:
- [ ] Opening hook present
- [ ] Key messages clear
- [ ] Call-to-action included
- [ ] Contact info/next steps provided

## Example Interactions

### Example 1: From Prompt

**User**: "Create a presentation about machine learning basics"

**Process**:
1. Ask: "What's your goal?" → User selects "Teaching"
2. Apply `templates/educational.md` structure
3. Create outline:
   - What is ML? (Hero slide)
   - Why it matters (Feature grid of use cases)
   - Key concepts (Educational progression)
   - Simple example (Code + explanation)
   - Common mistakes (Comparison of right vs wrong)
   - Practice exercise (Interactive)
   - Resources (Next steps)
4. Add layout suggestions and speaker notes
5. Output complete markdown

### Example 2: From Outline

**User provides**:
```
Product Launch
- New features
- Benefits
- Pricing
- Availability
```

**Process**:
1. Identify goal: Product announcement (Informing)
2. Expand outline using narrative structure:
   - Hero slide: "Introducing [Product] 2.0"
   - Problem context: Why we built this
   - Feature grid: What's new
   - Before/after comparison: Impact
   - Pricing tiers: Plans
   - Timeline: Rollout schedule
   - CTA: Get started today
3. Add visual recommendations
4. Output enhanced presentation

### Example 3: Enhancement Request

**User**: "Make these slides more engaging" [provides basic markdown]

**Process**:
1. Analyze existing structure
2. Identify improvements:
   - Add opening hook
   - Split dense slides
   - Recommend visual layouts
   - Add examples/statistics
   - Include speaker notes
   - Strengthen conclusion
3. Regenerate with enhancements
4. Explain changes made

## Advanced Techniques

### Progressive Disclosure

For complex topics:
1. Start with simple concept
2. Build complexity gradually
3. Use "For those interested" sections
4. Provide optional deep-dive slides in appendix

### Audience Adaptation

Adjust content based on audience:
- **Technical**: Include details, code, architecture
- **Executive**: Focus on business impact, ROI
- **General**: Use analogies, avoid jargon
- **Mixed**: Layer information with optional depth

### Export Formats

The primary output is Gamma AI-style HTML with vertical scrolling:
- **Gamma HTML** (Primary): Vertical scroll, responsive cards, self-contained file
- **Print/PDF Export**: Presentations can be printed or saved as PDF using browser print function
- **Accessibility**: Screen reader compatible with semantic HTML and ARIA labels

## Troubleshooting

### Issue: Too Much Content

**Solution**:
- Split into multiple slides
- Use progressive disclosure
- Move details to appendix or speaker notes

### Issue: Unclear Flow

**Solution**:
- Add transition slides
- Create section breaks
- Use signposting language
- Add "roadmap" slide early

### Issue: Weak Opening

**Solution**:
- Start with question or statistic
- Use powerful quote
- Share relevant story
- Present surprising fact

### Issue: Unmemorable Ending

**Solution**:
- Summarize key takeaways (Rule of 3)
- Include clear call-to-action
- Circle back to opening
- End with powerful quote or question

## References

This skill includes comprehensive resources:

**Templates** (`templates/`):
- Five presentation types with proven structures
- Ready to customize with specific content
- Include section descriptions and best practices

**Layout Patterns** (`layouts/`):
- Five layout types for different content
- Examples and use cases
- Responsive design guidance
- Accessibility notes

**Best Practices** (`references/gamma-best-practices.md`):
- Detailed guidelines for creating effective presentations
- Gamma-specific optimization tips
- Common pitfalls to avoid
- Advanced techniques

## Version Control Friendly

All output is markdown:
- Easy to diff and track changes
- Separate content from styling
- Comments for speaker notes
- Collaborative editing friendly

## Accessibility

Ensure all presentations:
- Use semantic heading hierarchy
- Include alt text for images
- Provide sufficient color contrast
- Don't rely on color alone
- Test with screen readers
- Work on mobile devices

## Getting Started

To use this skill effectively:

1. **Understand the goal**: Teaching, selling, informing, inspiring, or training?
2. **Choose appropriate template**: Match structure to goal
3. **Apply layout patterns**: Use the right layout for each content type
4. **Enhance intelligently**: Add visuals, notes, and supporting data
5. **Optimize for readability**: Follow content intelligence rules
6. **Review quality**: Use the checklist before finalizing

The result: Presentations that communicate clearly, engage audiences, and work beautifully across all devices and formats.

## Core Gamma AI Principles

These principles define what makes a Gamma-style presentation superior to traditional slide formats:

### 1. Vertical Scrolling
- **Natural web-like navigation**: Users scroll down, not click through horizontal slides
- **Continuous flow**: Content flows naturally like a webpage, not discrete chunks
- **Familiar interaction**: Everyone knows how to scroll; it's intuitive and accessible
- **No pagination anxiety**: Users can see their progress and navigate freely

### 2. Cards Grow on Mobile
- **Content-first sizing**: Cards expand to fit content, not the other way around
- **No text shrinking**: Font sizes never drop below readable minimums (16px body, 24px h2, 32px h1)
- **Natural height**: Use `height: auto !important` on mobile to let cards breathe
- **Responsive by design**: Same content works on 4" phones and 27" monitors

### 3. Minimum Font Sizes
- **Always readable**: Use CSS `max()` function to enforce minimums
  - Body: `max(16px, min(2vw, 18px))`
  - H2: `max(24px, min(4vw, 36px))`
  - H1: `max(32px, min(6vw, 48px))`
- **No squinting**: Text remains legible on all screen sizes
- **Accessibility first**: Readable text benefits everyone, especially mobile users

### 4. No External Dependencies
- **Self-contained files**: Everything in one HTML file (CSS and JavaScript inline)
- **Works offline**: No CDN dependencies means presentations work anywhere
- **Future-proof**: No broken links when external services change
- **Fast loading**: No network requests means instant presentation loading

### 5. Progressive Enhancement
- **Works without JavaScript**: Core content is accessible even if JS fails
- **Enhanced with JS**: Smooth scrolling, progress bar, and keyboard nav are bonuses
- **Semantic HTML**: Screen readers and accessibility tools work perfectly
- **Print-friendly**: CSS can be adapted for print media queries

## What NOT to Do

Critical mistakes that break the Gamma philosophy:

### ❌ Don't Use Fixed Heights for Cards
```css
/* WRONG */
.gamma-card {
    height: 600px; /* This forces content to fit a box */
    overflow: hidden; /* This hides overflow content */
}

/* CORRECT */
.gamma-card {
    height: auto; /* Let content determine height */
    min-height: auto; /* Don't enforce minimums */
}
```

### ❌ Don't Scale Text Below 16px
```css
/* WRONG */
@media (max-width: 768px) {
    p { font-size: 12px; } /* Too small to read */
}

/* CORRECT */
@media (max-width: 768px) {
    p { font-size: max(16px, 4vw) !important; } /* Always readable */
}
```

### ❌ Don't Use Horizontal Slide Navigation
```javascript
// WRONG - Don't use reveal.js or similar
Reveal.initialize({
    transition: 'slide',
    navigation: 'horizontal'
});

// CORRECT - Use vertical scrolling
window.scrollTo({ top: nextSlide.offsetTop, behavior: 'smooth' });
```

### ❌ Don't Require External Libraries
```html
<!-- WRONG -->
<script src="https://cdn.jsdelivr.net/npm/reveal.js@4/dist/reveal.js"></script>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reveal.js@4/dist/reveal.css">

<!-- CORRECT -->
<style>
    /* All CSS inline */
</style>
<script>
    // All JavaScript inline
</script>
```

### ❌ Don't Use overflow: hidden on Content Containers
```css
/* WRONG */
.card-content {
    overflow: hidden; /* Cuts off long content */
    max-height: 500px; /* Forces artificial limits */
}

/* CORRECT */
.card-content {
    overflow: visible; /* Let content show naturally */
    height: auto; /* No artificial limits */
}
```

## Testing the Implementation

Use these test cases to verify your Gamma presentations work correctly:

### Test 1: Mobile Responsiveness Test
**Objective**: Verify cards grow to fit content on mobile devices

**Steps**:
1. Create a slide with 20+ bullet points (lots of content)
2. Open the HTML file in a browser
3. Resize window to mobile width (<768px)
4. Inspect the slide card

**Expected Results**:
- ✅ Card grows taller to accommodate all content
- ✅ Text stays at 16px or larger
- ✅ All bullet points are visible without scrolling within the card
- ✅ No horizontal scrolling required
- ❌ Card does NOT have a fixed height
- ❌ Text does NOT shrink below 16px

### Test 2: Vertical Scroll Navigation Test
**Objective**: Ensure navigation is vertical, not horizontal

**Steps**:
1. Open the presentation in a browser
2. Try to navigate using:
   - Mouse scroll wheel
   - Arrow down/up keys
   - Spacebar
   - Touch swipe (on mobile)

**Expected Results**:
- ✅ Scrolling is smooth and vertical
- ✅ Arrow keys move between slides vertically
- ✅ Progress bar updates as you scroll
- ❌ No left/right arrow navigation
- ❌ No horizontal sliding transitions

### Test 3: Offline Functionality Test
**Objective**: Verify presentation works without internet connection

**Steps**:
1. Save the HTML file to your local computer
2. Disconnect from the internet
3. Open the HTML file in a browser

**Expected Results**:
- ✅ Presentation loads instantly
- ✅ All styles render correctly
- ✅ JavaScript features work (progress bar, keyboard nav)
- ✅ No broken resources or missing elements
- ❌ No error messages about failed CDN requests
- ❌ No missing fonts or styles

### Test 4: Font Size Minimum Test
**Objective**: Confirm text never shrinks below readable sizes

**Steps**:
1. Open presentation in browser
2. Use browser DevTools to simulate various screen sizes:
   - 320px (small phone)
   - 375px (iPhone SE)
   - 768px (tablet)
   - 1024px (laptop)
   - 1920px (desktop)
3. Inspect font sizes using DevTools computed styles

**Expected Results**:
- ✅ Body text: Never below 16px
- ✅ H2 headings: Never below 24px
- ✅ H1 titles: Never below 32px
- ✅ All text is easily readable at all sizes
- ❌ No text smaller than 16px at any viewport width

### Test 5: Long Content Card Growth Test
**Objective**: Verify cards expand naturally for varying content lengths

**Steps**:
1. Create three slides:
   - Slide A: 3 bullet points (short content)
   - Slide B: 15 bullet points (medium content)
   - Slide C: 30 bullet points (long content)
2. View on mobile (<768px) and desktop (>1024px)

**Expected Results**:
- ✅ All three slides have different heights based on content
- ✅ Slide C is much taller than Slide A
- ✅ All content is visible without internal scrolling
- ✅ No "view more" buttons or truncation
- ❌ Cards are NOT the same height
- ❌ No content is cut off or hidden

### Test 6: Accessibility Test
**Objective**: Ensure presentations work with assistive technologies

**Steps**:
1. Run browser accessibility audit (Chrome DevTools Lighthouse)
2. Test with screen reader (NVDA, JAWS, or VoiceOver)
3. Test keyboard-only navigation

**Expected Results**:
- ✅ Lighthouse accessibility score >90
- ✅ Screen reader can navigate all content
- ✅ Heading hierarchy is logical (H1 → H2 → H3)
- ✅ All content accessible via keyboard
- ✅ Focus indicators are visible
- ❌ No accessibility errors or warnings

### Test 7: Print/PDF Export Test
**Objective**: Verify presentations can be printed or saved as PDF

**Steps**:
1. Open presentation in browser
2. Use Print Preview (Ctrl/Cmd + P)
3. Check how slides appear in print layout

**Expected Results**:
- ✅ Each card appears on the page
- ✅ Content is readable in print preview
- ✅ Colors are preserved or have good contrast
- ✅ No content is cut off at page boundaries
- ✅ Can save as PDF successfully

## Troubleshooting Common Issues

### Issue: Cards Have Fixed Height on Mobile

**Symptom**: Content is cut off or requires scrolling within cards on mobile devices

**Solution**:
```css
@media (max-width: 768px) {
    .gamma-card {
        height: auto !important;
        min-height: auto !important;
        max-height: none !important;
    }
}
```

### Issue: Text is Too Small on Mobile

**Symptom**: Font sizes drop below 16px on small screens

**Solution**:
```css
@media (max-width: 768px) {
    p, li {
        font-size: max(16px, 4vw) !important;
    }
    h2 {
        font-size: max(24px, 6vw) !important;
    }
    h1 {
        font-size: max(32px, 8vw) !important;
    }
}
```

### Issue: Presentation Requires Internet Connection

**Symptom**: Styles or scripts fail to load when offline

**Solution**: Ensure all CSS and JavaScript are inline in the HTML file. Remove any external `<link>` or `<script src="">` tags that reference CDNs.

### Issue: Horizontal Scrolling Appears

**Symptom**: Users can scroll left/right, content overflows horizontally

**Solution**:
```css
body {
    overflow-x: hidden;
}

.gamma-card {
    max-width: 100%;
    box-sizing: border-box;
}
```
