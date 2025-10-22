# Gamma Best Practices

## Overview

This document provides detailed guidelines for creating presentations optimized for Gamma's vertical scroll format and responsive design philosophy.

## Gamma's Core Principles

### 1. Vertical Scroll Design

Unlike traditional slide decks, Gamma uses vertical scrolling cards:
- **Content flows naturally** like a webpage
- **Each card = one concept** (similar to a slide)
- **Responsive by default** - works on any device
- **Progressive disclosure** - reveal information as you scroll

### 2. Content-First Philosophy

Gamma prioritizes content over decoration:
- **Substance over style** - great content matters most
- **Built-in design** - templates handle aesthetics
- **Focus on message** - writer focuses on what to say
- **Automatic polish** - Gamma handles typography, spacing, colors

### 3. Mobile-First Responsive

Every Gamma presentation must work beautifully on mobile:
- **Cards adapt** to screen size
- **Text scales** appropriately
- **Images optimize** for bandwidth
- **Navigation simplifies** for touch

## Markdown Best Practices

### Heading Hierarchy

Use semantic headings correctly:

```markdown
# Card Title (H1)
Main title of each card/slide

## Section Heading (H2)
Major sections within a card

### Subsection (H3)
Creates grid items or subsections

#### Minor Heading (H4)
Rarely needed, use sparingly
```

**Rules**:
- One H1 per card maximum
- Don't skip levels (H1 → H3)
- H3 triggers grid layout when multiple in sequence
- Keep headings short (5-10 words max)

### Card Separators

Use `---` (three hyphens) to separate cards:

```markdown
# First Card

Content here

---

# Second Card

More content
```

**Best Practices**:
- Blank line before and after separator
- Use consistently throughout
- One main idea per card

### Lists

**Unordered Lists**:
```markdown
- First item
- Second item
- Third item
  - Nested item
  - Another nested item
```

**Ordered Lists**:
```markdown
1. First step
2. Second step
3. Third step
```

**Rules**:
- 3-5 items optimal
- 7 items maximum per list
- Keep items concise (1-2 lines)
- Use parallel structure
- Nested lists for sub-points (max 1 level deep)

### Emphasis

```markdown
**Bold text** for emphasis
*Italic text* for subtle emphasis
> Blockquote for pull quotes or important notes
```

**Guidelines**:
- Bold for key terms and important points
- Italic sparingly, for subtle emphasis
- Blockquotes for quotes, testimonials, or callouts

### Code Blocks

```markdown
\`\`\`javascript
function example() {
  return "formatted code";
}
\`\`\`
```

**Tips**:
- Always specify language for syntax highlighting
- Keep code examples short (< 15 lines per card)
- Add comments to explain complex parts
- Consider splitting long code across multiple cards

### Tables

```markdown
| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Row 1    | Data     | Data     |
| Row 2    | Data     | Data     |
```

**Best Practices**:
- Keep tables simple (3-5 columns max)
- Use for structured data only
- Include headers always
- On mobile, tables become scrollable or stack
- Consider using grid layout instead for better mobile UX

### Images

```markdown
![Alt text description](https://example.com/image.jpg)
```

**Requirements**:
- Always include descriptive alt text
- Use high-resolution images (min 1920px width for full-bleed)
- Prefer 16:9 aspect ratio
- Optimize file size (use WebP when possible)
- Use HTTPS URLs

## Layout Patterns

### Hero Card

Perfect for:
- Opening card
- Section breaks
- Key messages
- Impactful quotes

```markdown
# Big Bold Statement

Optional subtitle or supporting text
```

**Characteristics**:
- Minimal text (5-15 words)
- Large typography
- Often paired with background image
- High visual impact

### Grid Layout

Triggered automatically by multiple H3 headings:

```markdown
## Main Heading

### Item 1
Description

### Item 2
Description

### Item 3
Description
```

**Optimal Grid Sizes**:
- 2 items: Side-by-side (1x2)
- 3 items: Row (1x3) or L-shape
- 4 items: Square (2x2)
- 6 items: Rectangle (2x3)
- 9 items: Large grid (3x3)

**Avoid**:
- Odd numbers > 5 (visual imbalance)
- More than 9 items (information overload)
- Varying content lengths (creates visual chaos)

### Content + Image Split

```markdown
# Heading

Main content on one side

![Image description](image.jpg)
```

**Tips**:
- Text naturally flows around images
- Images can be left, right, or full-width
- Maintain aspect ratio
- Use high-quality images

### Timeline/Sequence

```markdown
## Journey

### Phase 1: Beginning
Description

### Phase 2: Middle
Description

### Phase 3: End
Description
```

**Best for**:
- Chronological progressions
- Step-by-step processes
- Project phases
- Historical narratives

### Data Visualization

Tables become responsive automatically:
```markdown
| Metric | Q1 | Q2 | Q3 |
|--------|----|----|-----|
| Revenue | $1M | $1.5M | $2M |
| Users | 10K | 15K | 22K |
```

**For better mobile experience**, consider text-based representations:
```markdown
### Revenue Growth

Q1: $1M
Q2: $1.5M (+50%)
Q3: $2M (+33%)

**Trend**: Strong growth trajectory
```

## Typography Rules

### Text Length Guidelines

**Card Title (H1)**:
- Ideal: 3-7 words
- Maximum: 12 words
- Use title case
- Avoid full sentences

**Section Heading (H2)**:
- Ideal: 2-5 words
- Maximum: 8 words
- Descriptive and scannable

**Body Text**:
- Ideal: 50-75 characters per line
- Maximum: 100 characters per line
- Short paragraphs (3-4 lines max)

**Bullet Points**:
- Ideal: 5-10 words
- Maximum: 15 words
- Parallel structure
- Start with strong verbs

### Readability

**Use Active Voice**:
- ✅ "We increased revenue by 40%"
- ❌ "Revenue was increased by 40%"

**Strong Verbs**:
- ✅ "Launch the product"
- ❌ "Do a product launch"

**Concrete Language**:
- ✅ "Save 10 hours per week"
- ❌ "Save significant time"

**Simple Words**:
- ✅ "Use" not "utilize"
- ✅ "Help" not "facilitate"
- ✅ "Start" not "commence"

## Visual Hierarchy

### Information Density

**Hero Cards**: 5-10% of deck
- Minimal text
- Maximum impact
- Strategic placement

**Content Cards**: 70-80% of deck
- Balanced text and white space
- 3-5 elements per card
- Clear focus

**Dense Cards**: 10-15% of deck
- Tables, detailed comparisons
- Use sparingly
- Follow with spacious card

### Emphasis Techniques

**Size**:
- H1 for primary message
- H2 for supporting points
- Body text for details

**Position**:
- Top = most important
- Middle = details
- Bottom = next steps

**Whitespace**:
- Breathing room = importance
- Crowded = less priority

**Color**:
- Don't rely solely on color
- Use for accent, not meaning
- Ensure sufficient contrast

## Content Pacing

### Card Length

**Short Card** (1-2 scrolls):
- Single concept
- 1 heading + 2-4 bullets
- Fast pacing

**Medium Card** (3-4 scrolls):
- Multiple related points
- Grid layouts
- Comparison tables
- Standard pacing

**Long Card** (5+ scrolls):
- Comprehensive coverage
- Detailed explanations
- Use section breaks
- Slow pacing

**Recommendation**: Vary card length for rhythm

### Presentation Flow

**Opening** (10% of cards):
1. Hero card with title
2. Hook or context
3. Agenda or objectives

**Body** (75% of cards):
1. Logical progression
2. One idea per card
3. Evidence and examples
4. Varied pacing

**Closing** (15% of cards):
1. Summary of key points
2. Call-to-action
3. Next steps
4. Contact information

## Mobile Optimization

### Design for Small Screens

**Font Sizes**:
- Never smaller than 16px body text
- Headings scale automatically
- Test on actual devices

**Touch Targets**:
- Buttons min 44x44px
- Links have adequate spacing
- No hover-dependent interactions

**Images**:
- Use responsive images
- Provide multiple sizes
- Optimize for bandwidth
- Test loading times

**Tables**:
- Keep simple (3 columns max for mobile)
- Consider alternative layouts
- Enable horizontal scroll if needed
- Or stack as cards

### Testing Checklist

- [ ] Text readable without zooming
- [ ] Images load quickly
- [ ] No horizontal scrolling required
- [ ] Touch targets easily tappable
- [ ] Navigation intuitive
- [ ] Content order makes sense
- [ ] Tables usable or re-formatted

## Accessibility

### Color & Contrast

**Requirements**:
- Text contrast ratio: 4.5:1 minimum
- Large text (18pt+): 3:1 minimum
- Don't use color alone to convey meaning

**Testing**:
- Use browser dev tools
- Check with color blindness simulators
- Verify in grayscale mode

### Semantic Structure

**Use Proper Headings**:
- Heading hierarchy must be logical
- Don't skip levels
- One H1 per card

**Alt Text for Images**:
- Describe content and context
- Not "image" or "photo"
- Be specific and concise
- Skip decorative images

**Link Text**:
- ✅ "Download the report"
- ❌ "Click here"

### Screen Reader Friendly

**Lists**:
- Use proper markdown lists
- Don't use bullets or numbers manually

**Tables**:
- Include header row
- Use semantic table markup
- Provide caption if complex

**Navigation**:
- Logical reading order
- Keyboard accessible
- Skip links for long content

## Common Pitfalls

### Avoid These Mistakes

**1. Wall of Text**:
- ❌ Paragraphs > 5 lines
- ✅ Break into bullets or multiple cards

**2. Inconsistent Formatting**:
- ❌ Mixing styles arbitrarily
- ✅ Use templates, maintain patterns

**3. Too Many Fonts/Styles**:
- ❌ Bold + italic + color + size
- ✅ Pick one emphasis method

**4. Unclear Hierarchy**:
- ❌ Everything looks equally important
- ✅ Clear primary/secondary/tertiary levels

**5. Poor Image Quality**:
- ❌ Pixelated, stretched, or tiny images
- ✅ High-res, proper aspect ratio

**6. Navigation Confusion**:
- ❌ No sense of where you are
- ✅ Section breaks, clear progress

**7. Information Overload**:
- ❌ Cramming everything on one card
- ✅ One idea per card, progressive disclosure

**8. Ignoring Mobile**:
- ❌ Designing only for desktop
- ✅ Mobile-first approach

## Advanced Techniques

### Progressive Disclosure

Reveal complexity gradually:

```markdown
# Simple Concept

Basic explanation everyone can understand

---

## For Those Interested

### Technical Details
More advanced information

### Deep Dive
Expert-level content
```

### Storytelling Arc

Structure for emotional impact:

1. **Setup**: Establish context
2. **Problem**: Introduce tension
3. **Journey**: Show attempts
4. **Resolution**: Present solution
5. **Transformation**: Show impact

### Data Storytelling

Make numbers compelling:

1. **Context first**: Why this data matters
2. **Visualize**: Use appropriate format
3. **Highlight insight**: What it means
4. **Action**: What to do about it

### Interactive Elements

Engage your audience:

```markdown
## Your Turn

**Before we continue, think about**:
- [Question 1]
- [Question 2]

**Share in the chat** or **Discuss with neighbor**
```

## Templates & Themes

### Choosing a Gamma Theme

Consider:
- **Audience**: Professional, creative, academic
- **Brand**: Colors and style guide
- **Content**: Serious, playful, inspirational
- **Format**: Presentation, document, website

### Customization Options

**Limited customization by design**:
- Focus on content, not styling
- Themes handle aesthetics
- Ensures consistency
- Maintains accessibility

**What you can control**:
- Theme selection
- Image choices
- Layout patterns (via markdown structure)
- Content organization

## Performance Optimization

### Loading Speed

**Images**:
- Compress without quality loss
- Use modern formats (WebP)
- Lazy load below fold
- Provide appropriate sizes

**Content**:
- Keep reasonable length (20-30 cards typical)
- Split very long decks
- Use links for supporting materials

**Media**:
- Embed videos from optimized hosts
- Use thumbnails with play buttons
- Don't autoplay

## Collaboration & Sharing

### Version Control

**Markdown Benefits**:
- Easy to diff changes
- Track history clearly
- Merge contributions
- Comment on specific lines

**Best Practices**:
- Meaningful commit messages
- Small, focused changes
- Review before merging
- Tag releases

### Team Workflow

**Roles**:
- **Content Owner**: Manages structure and message
- **Contributors**: Add domain expertise
- **Reviewers**: Check quality and accuracy
- **Designer**: Selects theme and images

**Process**:
1. Outline structure (all stakeholders)
2. Draft content (content owner + contributors)
3. Review and revise (reviewers)
4. Polish and finalize (designer + content owner)
5. Present and iterate (based on feedback)

## Platform-Specific Tips

### Gamma vs PowerPoint

**Gamma Advantages**:
- Mobile-responsive automatically
- Modern, clean design
- Web-native (easy sharing)
- Collaborative editing
- Version history

**When to use PowerPoint**:
- Strict template requirements
- Offline presentation needed
- Animation-heavy
- Organizational mandate

### Export Options

**From Gamma**:
- PDF: For printing or offline viewing
- Link: For web sharing
- Embed: For websites

**From Markdown** (this skill):
- Gamma: Upload markdown directly
- PowerPoint: Convert via Pandoc
- PDF: Via markdown → HTML → PDF
- Website: Via markdown processors

## Quality Checklist

Before sharing, verify:

### Content Quality
- [ ] One clear message per card
- [ ] Logical flow and progression
- [ ] No typos or grammatical errors
- [ ] Data and facts verified
- [ ] Images relevant and high-quality

### Structure
- [ ] Opening hook present
- [ ] Clear narrative arc
- [ ] Smooth transitions
- [ ] Strong conclusion
- [ ] Call-to-action included

### Formatting
- [ ] Consistent heading hierarchy
- [ ] Proper markdown syntax
- [ ] Card separators used correctly
- [ ] Lists properly formatted
- [ ] Code blocks with language specified

### Design
- [ ] Appropriate theme selected
- [ ] Visual hierarchy clear
- [ ] Whitespace balanced
- [ ] Not too crowded or too sparse
- [ ] Images properly sized

### Mobile Experience
- [ ] Tested on phone
- [ ] Text readable
- [ ] Images load quickly
- [ ] Tables work or adapt
- [ ] Navigation smooth

### Accessibility
- [ ] Color contrast sufficient
- [ ] Alt text provided
- [ ] Heading hierarchy semantic
- [ ] Screen reader friendly
- [ ] Keyboard navigable

## Resources

### Learning More

**Gamma Documentation**:
- gamma.app/help
- Community forums
- Video tutorials
- Template gallery

**Presentation Skills**:
- Nancy Duarte's books
- Slide:ology principles
- TED talk guidelines
- Storytelling frameworks

**Markdown Reference**:
- CommonMark specification
- GitHub Flavored Markdown
- Markdown guide (markdownguide.org)

### Tools

**Markdown Editors**:
- VS Code with Markdown extension
- Typora
- iA Writer
- Obsidian

**Image Optimization**:
- TinyPNG
- Squoosh
- ImageOptim
- Kraken.io

**Accessibility Testing**:
- WAVE browser extension
- axe DevTools
- Color contrast checkers
- Screen readers (NVDA, VoiceOver)

## Conclusion

Great Gamma presentations prioritize:

1. **Clear content** over decoration
2. **Logical structure** over complexity
3. **Mobile experience** over desktop-only thinking
4. **Accessibility** over aesthetics alone
5. **Story** over data dumps

Focus on these principles, use the templates and layouts provided, and your presentations will engage and inform audiences across any device.
