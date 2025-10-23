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

Always provide:

1. **The Markdown Content** (ready to convert)
2. **Speaker Notes** (if requested)
3. **Image Suggestions** (if relevant)
4. **Customization Tips**

Example output structure:
```
Here's your presentation about [topic]:

[MARKDOWN CONTENT]

---

**Customization Suggestions:**
- Consider adding [specific data] to slide 3
- Include your company logo on the title slide
- Add team photos to slide 5

**Image Suggestions:**
- Slide 2: [Image description]
- Slide 4: [Image description]
```

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

- Always optimize for mobile viewing (cards that grow, not shrink)
- Maintain minimum font sizes (16px body, 24px headers)
- Use semantic markdown for better conversion
- Include metadata comments for enhanced processing
- Prioritize clarity over cleverness
- When in doubt, use fewer words

This instruction set ensures consistent, high-quality presentation generation that follows the Gamma AI vertical-scroll philosophy while remaining flexible enough to handle various content types and user needs.

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
