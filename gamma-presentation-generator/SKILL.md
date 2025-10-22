---
name: gamma-presentation-generator
description: Content-first presentation generator that transforms ideas, documents, and outlines into well-structured, narrative-driven presentations optimized for Gamma and other formats. This skill should be used when users request presentation creation, slide generation, pitch deck building, or content conversion to presentation format.
---

# Gamma Presentation Generator

## Purpose

Transform ideas, outlines, documents, or natural language prompts into well-structured, narrative-driven presentations. This skill focuses on content intelligence and narrative structure rather than just formatting - helping users organize thoughts into compelling stories that work across devices and formats.

## Core Philosophy

**Content-First Approach**: The quality of a presentation depends on narrative structure, logical flow, and compelling content - not just visual design. This skill excels at:

1. **Intelligent Content Organization**: Taking raw ideas and structuring them into logical, persuasive narratives
2. **Adaptive Structuring**: Applying appropriate narrative frameworks based on presentation goals
3. **Multi-Format Output**: Generating markdown that works across platforms (Gamma, PowerPoint, PDFs, speaker notes)
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

### Multi-Format Export

Generate variations optimized for:
- **Gamma**: Vertical scroll, responsive cards
- **PowerPoint**: Traditional slides, 16:9 ratio
- **PDF Handout**: Include all speaker notes
- **Speaker Script**: Full text with timing
- **Blog Post**: Narrative version of content

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
