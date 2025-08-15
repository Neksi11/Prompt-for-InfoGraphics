Below are 8 ready-to-commit Markdown files. Each file pairs the **generation prompt** with its **ASCII visualization**.

Repo layout suggestion:

```
infographic-templates/
├── prompts/
│   ├── 1_technical_architecture.md
│   ├── 2_grid_concept_layout.md
│   ├── 3_horizontal_comparison_chart.md
│   ├── 4_workflow_comparison.md
│   ├── 5_circular_radial_hub.md
│   ├── 6_timeline_evolution.md
│   ├── 7_ascending_staircase.md
│   └── 8_three_column_architecture.md
└── README.md
```

---

# prompts/1\_technical\_architecture.md

## Technical Architecture Diagram

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[YOUR TITLE]" that clearly communicates "[YOUR CONCEPT/PROCESS]" to a professional audience. The tone should be informative, technical, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white with subtle light colored accent areas.
- Accent color: [YOUR HEX COLOR] for headings, highlights, and key components.
- Typography: geometric sans-serif (Inter, Poppkins, or SF Pro) with strict hierarchy:
   * Headings: bold, clear, and ≤ 40 characters.
   * Body: ≤ 50 words per panel, short sentences, plain English.
- Alignment: Follow a 12-column grid; even margins; balanced spacing.
- All icons flat, vector-sharp, minimal, with rounded edges.

LAYOUT GRID & SECTION ORDER:
1. **Header** (Top-center aligned)
   - Large main title
   - Small pill-shaped definition label
   - One-line concept definition
   - Side-by-side comparison boxes (optional)

2. **Main Architecture Flow** (Center panel):
   - Horizontal workflow diagram
   - Numbered connection points (1-12)
   - Color-coded components with clear labels
   - External service connections

3. **Bottom Sections** (Three-column layout):
   - Left: Category breakdown with icons
   - Center: Sub-categories with visual elements
   - Right: Analogy or comparison section

TYPOGRAPHY & ICONOGRAPHY:
- Font sizes: Title 24-28pt, headers 18-20pt, body 12-14pt
- Icon style: Minimal line art, consistent stroke width, geometric shapes
- Keep 60% visual, 40% text ratio

COLOR & DESIGN RULES:
- Primary: [YOUR HEX] for main components
- Secondary: Light backgrounds for sections
- Grayscale: #374151 for text, #9CA3AF for supporting elements
- Subtle drop shadows on major components

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Vector-sharp lines and icons
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                         [YOUR TITLE]                               │
│                      ┌─────────────┐                               │
│                      │ Definition  │                               │
│                      └─────────────┘                               │
│  ┌──────────────────┐                    ┌──────────────────┐      │
│  │ Basic Tool       │                    │ Your Tool        │      │
│  │ Calling          │                    │ Calling          │      │
│  │ [logos/icons]    │                    │ [logos/icons]    │      │
│  └──────────────────┘                    └──────────────────┘      │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│  ┌─────┐    ①    ┌─────────────┐    ⑦    ┌─────────────┐           │
│  │User │ ────────▶│ MCP Client  │ ────────▶│   Service   │    ⑧      │
│  │     │    ⑥     │     📱      │         │    🔧       │ ────────▶ │
│  └─────┘ ◀──────  │             │    ②    │             │           │
│     ⑪             └─────────────┘ ────────▶│             │           │
│                           │       ⑩       └─────────────┘           │
│                           ③                       │                 │
│                           ▼                       ⑨                 │
│                    ┌─────────────┐                 ▼                 │
│                    │    LLMs     │         ┌─────────────┐           │
│                    │   🤖 📊 ⚙️   │         │   External  │           │
│                    │             │         │  Services   │           │
│                    └─────────────┘         │  💬 🔍 🏠   │           │
│                           │                └─────────────┘           │
│                        ④ ⑤                                          │
│                    ┌─────────────┐                                   │
│                    │  MCP Host   │                                   │
│                    └─────────────┘                                   │
├─────────────────────────────────────────────────────────────────────┤
│ ┌─────────┐    ┌─────────────┐    ┌─────────────────────────────────┐│
│ │  Tasks  │    │ Task Types  │    │        Analogy Section         ││
│ │         │    │             │    │                                 ││
│ │ 🔧 Tools│    │ Model:      │    │    ┌─────────────────────────┐  ││
│ │ 📁 Res. │    │  Search     │    │    │     Local Data          │  ││
│ │ 💭 Prompts│   │  Update DB  │    │    │     Sources             │  ││
│ │         │    │             │    │    │  📊 📁 🗄️             │  ││
│ │         │    │ App:        │    │    └─────────────────────────┘  ││
│ │         │    │  Local Files│    │               │                 ││
│ │         │    │  API Resp.  │    │               ▼                 ││
│ │         │    │             │    │    ┌─────────────────────────┐  ││
│ │         │    │ User:       │    │    │    Third Party          │  ││
│ │         │    │  Doc Q&A    │    │    │    Sources              │  ││
│ │         │    │  Use MCP    │    │    │   💬 🔍 ☁️            │  ││
│ │         │    │             │    │    └─────────────────────────┘  ││
│ └─────────┘    └─────────────┘    └─────────────────────────────────┘│
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/2\_grid\_concept\_layout.md

## Grid Concept Layout (4×5 or Customizable)

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[NUMBER] [YOUR TOPIC] You Need To Know In [YEAR]" that clearly communicates "[YOUR EDUCATIONAL THEME]" to a professional audience. The tone should be educational, comprehensive, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white with colorful accent squares for each concept.
- Accent colors: Multi-color palette for category differentiation.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Main title: bold, large, ≤ 60 characters.
   * Concept titles: bold, ≤ 25 characters per concept.
   * Body: ≤ 40 words per concept, bullet points for key features.
- Alignment: [X]×[Y] grid layout with consistent spacing.
- All icons flat, vector-sharp, minimal, conceptual representations.

LAYOUT GRID & SECTION ORDER:
1. **Header** (Full width, top)
   - Large numbered title "[NUMBER] [YOUR TOPIC]"
   - Subtitle "[DESCRIPTIVE TEXT]"
   - Minimal spacing before grid

2. **Main Grid** ([X]×[Y] layout):
   - Each square: colored background + icon + title + description
   - Consistent square dimensions
   - 2px white borders between squares

3. **Footer** (Bottom right corner)
   - Small attribution or call-to-action
   - Optional download prompt

TYPOGRAPHY & ICONOGRAPHY:
- Title: 32pt bold, center-aligned
- Concept titles: 14pt bold
- Descriptions: 10pt regular, line height 1.4
- Icons: 48×48px, single color (white), simple geometric style
- Consistent icon stroke weight and corner radius

COLOR & DESIGN RULES:
- Multi-color palette: [LIST YOUR HEX COLORS]
- White text on colored backgrounds
- Maintain sufficient contrast ratio
- 8px padding inside each square
- 2px white gap between squares

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Clean vector graphics, no pixelation
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                    [NUMBER] [YOUR TOPIC]                           │
│                You Need To Know In [YEAR]                          │
├─────────────────────────────────────────────────────────────────────┤
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│ │ 🔧       │ │ 🎨       │ │ 🧠       │ │ 👁️       │               │
│ │Concept 1 │ │Concept 2 │ │Concept 3 │ │Concept 4 │               │
│ │          │ │          │ │          │ │          │               │
│ │Short desc│ │Short desc│ │Short desc│ │Short desc│               │
│ │for this  │ │for this  │ │for this  │ │for this  │               │
│ │concept   │ │concept   │ │concept   │ │concept   │               │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘               │
│                                                                     │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│ │ 📊       │ │ 🤖       │ │ 👀       │ │ 💬       │               │
│ │Concept 5 │ │Concept 6 │ │Concept 7 │ │Concept 8 │               │
│ │          │ │          │ │          │ │          │               │
│ │Short desc│ │Short desc│ │Short desc│ │Short desc│               │
│ │for this  │ │for this  │ │for this  │ │for this  │               │
│ │concept   │ │concept   │ │concept   │ │concept   │               │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘               │
│                                                                     │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│ │ 📈       │ │ 🔍       │ │ ⚡       │ │ 📚       │               │
│ │Concept 9 │ │Concept10 │ │Concept11 │ │Concept12 │               │
│ │          │ │          │ │          │ │          │               │
│ │Short desc│ │Short desc│ │Short desc│ │Short desc│               │
│ │for this  │ │for this  │ │for this  │ │for this  │               │
│ │concept   │ │concept   │ │concept   │ │concept   │               │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘               │
│                                                                     │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│ │ 🎯       │ │ 🔄       │ │ 🏗️       │ │ 📊       │               │
│ │Concept13 │ │Concept14 │ │Concept15 │ │Concept16 │               │
│ │          │ │          │ │          │ │          │               │
│ │Short desc│ │Short desc│ │Short desc│ │Short desc│               │
│ │for this  │ │for this  │ │for this  │ │for this  │               │
│ │concept   │ │concept   │ │concept   │ │concept   │               │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘               │
│                                                                     │
│ ┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│ │ 💡       │ │ ⚠️       │ │ 📏       │ │ 🧠       │               │
│ │Concept17 │ │Concept18 │ │Concept19 │ │Concept20 │               │
│ │          │ │          │ │          │ │          │               │
│ │Short desc│ │Short desc│ │Short desc│ │Short desc│               │
│ │for this  │ │for this  │ │for this  │ │for this  │               │
│ │concept   │ │concept   │ │concept   │ │concept   │               │
│ └──────────┘ └──────────┘ └──────────┘ └──────────┘               │
├─────────────────────────────────────────────────────────────────────┤
│                                          📥 Download Guide         │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/3\_horizontal\_comparison\_chart.md

## Horizontal Comparison Chart (3-Panel)

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[YOUR COMPARISON TITLE]" that clearly communicates "Understanding [A] vs [B] vs [C]" to a professional audience. The tone should be career-focused/informative, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white.
- Accent colors: [COLOR 1], [COLOR 2], [COLOR 3] for differentiation.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Section titles: bold, large, ≤ 20 characters.
   * Category headers: medium weight, ≤ 15 characters.
   * Body: ≤ 30 words per section, clear and concise.
- Alignment: Three horizontal sections, equal height distribution.
- Character illustrations: flat, professional, diverse representation (optional).

LAYOUT GRID & SECTION ORDER:
1. **First Section** (Top section, [COLOR 1] theme)
   - Character illustration or icon (left)
   - Title and focus description (right)
   - Skills and key information sections

2. **Second Section** (Middle section, [COLOR 2] theme)
   - Character illustration or icon (left)
   - Title and focus description (right)
   - Skills and key information sections

3. **Third Section** (Bottom section, [COLOR 3] theme)
   - Character illustration or icon (left)
   - Title and focus description (right)
   - Skills and key information sections

TYPOGRAPHY & ICONOGRAPHY:
- Section titles: 28pt bold, white text
- Category headers: 16pt medium weight, white text
- Body text: 18pt regular, white text
- Character illustrations: 200×250px, flat style, minimal detail
- Consistent proportions and styling

COLOR & DESIGN RULES:
- Three-color system with white text overlay
- Each section takes 33% of vertical space
- Visual elements positioned left, text content right
- 40px padding around all content
- Subtle inner shadows for depth

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Clean vector illustrations
- High contrast for readability
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│ ┌─────────────────────────────────────────────────────────────────┐ │
│ │                        [ROLE A]                                 │ │
│ │  👷‍♂️             Focus: [FOCUS AREA]                            │ │
│ │  [Character]       Skills: [SKILL 1, SKILL 2, SKILL 3]         │ │
│ │  Illustration      Motto: "[MOTTO]"                             │ │
│ │                                                                 │ │
│ └─────────────────────────────────────────────────────────────────┘ │
├─────────────────────────────────────────────────────────────────────┤
│ ┌─────────────────────────────────────────────────────────────────┐ │
│ │                        [ROLE B]                                 │ │
│ │  👨‍💼             Focus: [FOCUS AREA]                            │ │
│ │  [Character]       Skills: [SKILL 1, SKILL 2, SKILL 3]         │ │
│ │  Illustration      Motto: "[MOTTO]"                             │ │
│ │                                                                 │ │
│ └─────────────────────────────────────────────────────────────────┘ │
├─────────────────────────────────────────────────────────────────────┤
│ ┌─────────────────────────────────────────────────────────────────┐ │
│ │                        [ROLE C]                                 │ │
│ │  👨‍🔬             Focus: [FOCUS AREA]                            │ │
│ │  [Character]       Skills: [SKILL 1, SKILL 2, SKILL 3]         │ │
│ │  Illustration      Motto: "[MOTTO]"                             │ │
│ │                                                                 │ │
│ └─────────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/4\_workflow\_comparison.md

## Workflow Comparison (2×2 Grid)

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[YOUR WORKFLOW TITLE]" that clearly communicates "[YOUR PROCESS COMPARISON THEME]" to a professional audience. The tone should be technical, progressive, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white with light colored section backgrounds.
- Accent colors: [COLOR 1], [COLOR 2], [COLOR 3], [COLOR 4] for workflow differentiation.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Workflow titles: bold, ≤ 20 characters.
   * Step labels: medium weight, numbered.
   * Body: ≤ 25 words per step, technical but accessible.
- Alignment: 2×2 grid layout with consistent spacing.
- All icons flat, vector-sharp, workflow-focused.

LAYOUT GRID & SECTION ORDER:
1. **Top-Left Workflow** ([COLOR 1] theme)
   - Linear or branching flow diagram
   - Sequential steps with connecting arrows
   - Clear start-to-finish process

2. **Top-Right Workflow** ([COLOR 2] theme)
   - Process flow with decision points
   - Multiple pathway options
   - Trigger-based or conditional steps

3. **Bottom-Left Workflow** ([COLOR 3] theme)
   - Complex multi-step process
   - Tool/resource selection elements
   - Memory or data compilation steps

4. **Bottom-Right Workflow** ([COLOR 4] theme)
   - Advanced orchestration process
   - Multi-agent or collaborative elements
   - Research, planning, execution phases

TYPOGRAPHY & ICONOGRAPHY:
- Section titles: 22pt bold
- Step labels: 12pt medium weight
- Flow text: 10pt regular
- Icons: 32×32px, minimal line art
- Consistent arrow styles for flow direction
- Process/user avatars: circle icons

COLOR & DESIGN RULES:
- Each quadrant gets unique background color
- White content boxes with subtle shadows
- Connecting arrows in section accent colors
- Consistent spacing and alignment

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Clean workflow diagrams
- Consistent visual hierarchy
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│ ┌────────────────────────┐    ┌────────────────────────────────────┐ │
│ │    [WORKFLOW A]        │    │         [WORKFLOW B]               │ │
│ │                        │    │                                    │ │
│ │ User ──①──▶ Process ───┤    │ Trigger ──①──▶ Action ──②──▶ Result│ │
│ │  │         │     ▲    │    │    │            │              │   │ │
│ │  │         ②     │    │    │    │            ③              │   │ │
│ │  │         ▼     ③    │    │    ▼            ▼              ▼   │ │
│ │  └──▶ Response ──┘    │    │ Manual ◀──── Schedule ────▶ Auto   │ │
│ │                        │    │                                    │ │
│ └────────────────────────┘    └────────────────────────────────────┘ │
├─────────────────────────────────────────────────────────────────────┤
│ ┌────────────────────────┐    ┌────────────────────────────────────┐ │
│ │    [WORKFLOW C]        │    │         [WORKFLOW D]               │ │
│ │                        │    │                                    │ │
│ │ Input ──①──▶ Select ───┤    │ Orchestrator ──①──▶ Planner       │ │
│ │   │         Tools ▲    │    │      │              │              │ │
│ │   │           │   │    │    │      ②              ③              │ │
│ │   ②          ③   │    │    │      ▼              ▼              │ │
│ │   ▼           ▼   │    │    │ Data ◀──────── Agent ────────▶ Results │
│ │ Multi-Step ──Actions──┤    │ Retrieval       Network             │ │
│ │   │                    │    │      │              │              │ │
│ │   ④                    │    │      ④              ⑤              │ │
│ │   ▼                    │    │      ▼              ▼              │ │
│ │ Memory ──⑤──▶ Output   │    │ Context ────────▶ Output           │ │
│ │                        │    │                                    │ │
│ └────────────────────────┘    └────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/5\_circular\_radial\_hub.md

## Circular/Radial Hub Layout

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[YOUR CENTRAL THEME] [YEAR]" that clearly communicates "[YOUR COMPREHENSIVE OVERVIEW]" to a professional audience. The tone should be futuristic, comprehensive, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white.
- Accent colors: Multi-color palette with [PRIMARY HEX] as main, plus [4-6 SECONDARY COLORS] for sections.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Central title: bold, large, ≤ 20 characters.
   * Section titles: bold, ≤ 20 characters.
   * Body: ≤ 30 words per description, technical but clear.
- Alignment: Circular/radial layout with center focus.
- All icons flat, vector-sharp, topic-relevant.

LAYOUT GRID & SECTION ORDER:
1. **Central Hub** (Circle center)
   - Main title
   - Year or key identifier prominently displayed
   - Connecting lines to outer sections

2. **Outer Sections** ([NUMBER] major categories radiating outward)
   - [SECTION 1] (position)
   - [SECTION 2] (position)
   - [SECTION 3] (position)
   - [SECTION 4] (position)
   - [SECTION 5] (position)
   - [SECTION 6] (position)

3. **Detail Boxes** (Around periphery)
   - Workflow diagrams for each category
   - Technical specifications or examples
   - Tool and platform references

TYPOGRAPHY & ICONOGRAPHY:
- Central title: 24pt bold
- Section titles: 16pt bold
- Descriptions: 11pt regular
- Icons: 40×40px, consistent line weight
- Connecting lines: 2pt, section accent colors
- Circular badge elements for branding

COLOR & DESIGN RULES:
- [PRIMARY COLOR] as main accent
- Each section gets unique color coding
- White backgrounds for text boxes
- Subtle gradients on circular elements
- Consistent spacing and alignment
- Clean connecting lines between elements

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Scalable vector elements
- Clean radial layout geometry
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│  ┌─────────────────┐                    ┌─────────────────────────┐ │
│  │   [SECTION A]   │                    │      [SECTION B]        │ │
│  │                 │                    │                         │ │
│  │ 🎤 Description  │                    │ 📊 Description          │ │
│  │ • Feature 1     │                    │ • Feature 1             │ │
│  │ • Feature 2     │────────┐  ┌────────│ • Feature 2             │ │
│  └─────────────────┘        │  │        └─────────────────────────┘ │
│                              ▼  ▼                                  │ │
│  ┌─────────────────┐    ┌─────────────┐    ┌─────────────────────┐ │
│  │   [SECTION F]   │    │    [YEAR]   │    │     [SECTION C]     │ │
│  │                 │◀───│             │───▶│                     │ │
│  │ 🔧 Description  │    │ [MAIN TITLE]│    │ 🌐 Description      │ │
│  │ • Feature 1     │    │   TRENDS    │    │ • Feature 1         │ │
│  │ • Feature 2     │────│             │────│ • Feature 2         │ │
│  └─────────────────┘    └─────────────┘    └─────────────────────┘ │
│                              ▲  ▲                                  │ │
│  ┌─────────────────┐        │  │        ┌─────────────────────────┐ │
│  │   [SECTION E]   │        │  │        │      [SECTION D]        │ │
│  │                 │────────┘  └────────│                         │ │
│  │ 💻 Description  │                    │ 🔍 Description          │ │
│  │ • Feature 1     │                    │ • Feature 1             │ │
│  │ • Feature 2     │                    │ • Feature 2             │ │
│  └─────────────────┘                    └─────────────────────────┘ │
│                                                                     │
│ ┌─────────────────────────────────────────────────────────────────┐ │
│ │            Additional Detail Boxes Around Periphery            │ │
│ │ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐   │ │
│ │ │Workflow │ │Tech     │ │Platform │ │Tools    │ │Examples │   │ │
│ │ │Diagram  │ │Specs    │ │Integration│ │& APIs  │ │& Uses   │   │ │
│ │ └─────────┘ └─────────┘ └─────────┘ └─────────┘ └─────────┘   │ │
│ └─────────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/6\_timeline\_evolution.md

## Timeline/Evolution Layout

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "Evolution of [YOUR TOPIC]" that clearly communicates "[YOUR PROGRESSION THEME]" to a professional audience. The tone should be historical, progressive, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white.
- Accent colors: [PRIMARY HEX] as main theme with lighter backgrounds for sections.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Era/phase titles: bold, large, ≤ 20 characters.
   * Section headers: medium weight, ≤ 25 characters.
   * Body: ≤ 40 words per section, clear bullet points.
- Alignment: Structured grid with clear section divisions.
- All icons flat, vector-sharp, topic-relevant.

LAYOUT GRID & SECTION ORDER:
1. **Header** (Top section)
   - Multi-column comparison: [ERA 1] | [ERA 2] | [ERA 3]
   - Key characteristics for each era/phase

2. **Middle Sections** (Two main diagrams)
   - [WORKFLOW/PROCESS 1] (left)
   - [WORKFLOW/PROCESS 2] (right)

3. **Bottom Sections** (Two analytical diagrams)
   - [FRAMEWORK/CONCEPT] (bottom-left)
   - [EVOLUTION/FLOW] (bottom-right)

TYPOGRAPHY & ICONOGRAPHY:
- Era titles: 18pt bold
- Section headers: 14pt medium
- Body text: 11pt regular
- Icons: 36×36px, consistent theme color
- Workflow arrows: clear directional flow
- Consistent spacing between elements

COLOR & DESIGN RULES:
- Primary [HEX COLOR] for headers and accents
- Light version of primary for section backgrounds
- White content areas with subtle borders
- Clean workflow arrows and connection lines
- Consistent padding and margins

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Clean architectural diagrams
- Professional business appearance
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                    Evolution of [YOUR TOPIC]                       │
├─────────────────────────────────────────────────────────────────────┤
│ ┌──────────────┐ ┌──────────────┐ ┌──────────────────────────────┐  │
│ │   [ERA 1]    │ │   [ERA 2]    │ │          [ERA 3]             │  │
│ │              │ │              │ │                              │  │
│ │ ▶ Feature A  │ │ ▶ Feature A  │ │ ▶ Feature A                  │  │
│ │ ▶ Feature B  │ │ ▶ Feature B  │ │ ▶ Feature B                  │  │
│ │ ▶ Feature C  │ │ ▶ Feature C  │ │ ▶ Feature C                  │  │
│ │              │ │              │ │                              │  │
│ └──────────────┘ └──────────────┘ └──────────────────────────────┘  │
├─────────────────────────────────────────────────────────────────────┤
│ ┌────────────────────────────────┐ ┌─────────────────────────────┐  │
│ │        [WORKFLOW 1]            │ │      [WORKFLOW 2]           │  │
│ │                                │ │                             │  │
│ │ Step 1 ──①──▶ Step 2 ──②──▶   │ │ Protocol A ──①──▶ System   │  │
│ │   │             │              │ │    │               │        │  │
│ │   │             ③              │ │    │               ②        │  │
│ │   ▼             ▼              │ │    ▼               ▼        │  │
│ │ Action ◀── Planning ──④──▶     │ │ Resource ◀── Agent ──③──▶  │  │
│ │   │                            │ │    │                       │  │
│ │   ⑤                            │ │    ④                       │  │
│ │   ▼                            │ │    ▼                       │  │
│ │ Result                         │ │ Output                     │  │
│ └────────────────────────────────┘ └─────────────────────────────┘  │
├─────────────────────────────────────────────────────────────────────┤
│ ┌────────────────────────────────┐ ┌─────────────────────────────┐  │
│ │    [CONCEPTUAL FRAMEWORK]      │ │    [ATTENTION FLOW]         │  │
│ │                                │ │                             │  │
│ │     ┌─────────────────────┐    │ │ [ERA 1]: User → Search →    │  │
│ │     │    Central Hub      │    │ │          ML → Ad Auction   │  │
│ │     │                     │    │ │                             │  │
│ │ ┌───│   [MAIN CONCEPT]    │───┐│ │ [ERA 2]: User → Algorithm→  │  │
│ │ │   │                     │   ││ │          Feed → Engage     │  │
│ │ ▼   └─────────────────────┘   ▼│ │                             │  │
│ │Element A              Element B││ │ [ERA 3]: User → Agent →     │  │
│ │    │                      │   ││ │          Service → Execute │  │
│ │    ▼                      ▼   ││ │                             │  │
│ │Sub-A                   Sub-B  ││ │                             │  │
│ └────────────────────────────────┘ └─────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/7\_ascending\_staircase.md

## Ascending Staircase / Maturity Model

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[YOUR FRAMEWORK TITLE]" that clearly communicates "[NUMBER] Levels of [YOUR CONCEPT]" to a professional audience. The tone should be educational, progressive, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white with gradient colored steps.
- Accent colors: Gradient from light [COLOR] at bottom to deep [COLOR] at top.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Level titles: bold, large, ≤ 30 characters.
   * Descriptions: medium weight, ≤ 50 words.
   * Bullet points: ≤ 15 words each, clear and actionable.
- Alignment: Staircase/stepped layout ascending left to right.
- Optional: Human figures or icons showing progression.

LAYOUT GRID & SECTION ORDER:
1. **Staircase Structure** ([NUMBER] ascending levels)
   - Each level as a wider step
   - Increasing color saturation with height
   - Optional progression indicators

2. **Side Panel** (Right side)
   - "Higher [CAPABILITY/BENEFIT]" arrow
   - "The more you climb the framework, the less:" text
   - Benefits or trade-offs list

3. **Footer** (Bottom)
   - Optional call-to-action or attribution
   - Additional resources or links

TYPOGRAPHY & ICONOGRAPHY:
- Level titles: 16pt bold, white text
- Descriptions: 12pt medium, white text
- Bullet points: 10pt regular, white text
- Optional figures: Simple line art, consistent style
- Arrow: Bold, pointing upward
- Gradient overlay on steps

COLOR & DESIGN RULES:
- Gradient progression: Light [HEX] → Medium [HEX] → Dark [HEX]
- White text for contrast on colored backgrounds
- Each step 20% darker than previous
- Clean step edges with subtle shadows
- Consistent step height and depth

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Smooth gradient transitions
- Clean geometric step shapes
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                    [YOUR FRAMEWORK TITLE]                          │
│                                                                     │
│                                                     ┌─────────────┐ │
│                                                     │Higher       │ │
│                                            ┌────────│[CAPABILITY] │ │
│                                            │        │and Autonomy │ │
│                                   ┌────────│        └─────────────┘ │
│                          ┌────────│        │                        │
│                 ┌────────│        │        │                        │
│        ┌────────│        │        │        │                        │
│   👤   │        │        │        │        │                        │
│  ──────│        │        │        │        │                        │
│ Level 1│Level 2 │Level 3 │Level 4 │Level 5 │                        │
│        │        │        │        │        │                        │
│[TITLE] │[TITLE] │[TITLE] │[TITLE] │[TITLE] │                        │
│        │        │        │        │        │                        │
│Desc &  │Desc &  │Desc &  │Desc &  │Desc &  │                        │
│bullets │bullets │bullets │bullets │bullets │                        │
│• Point │• Point │• Point │• Point │• Point │                        │
│• Point │• Point │• Point │• Point │• Point │                        │
│• Point │• Point │• Point │• Point │• Point │                        │
└────────┴────────┴────────┴────────┴────────┘                        │
│                                                                     │
│ The more you climb the framework, the less:                        │
│ • [TRADE-OFF 1]                                                    │
│ • [TRADE-OFF 2]                                                    │
│ • [TRADE-OFF 3]                                                    │
│                                                                     │
│ ┌─────────────────────────────────────────────────────────────────┐ │
│ │                    [CALL-TO-ACTION]                             │ │
│ │                 📚 [RESOURCE/LINK]                              │ │
│ └─────────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────────┘
```

---

# prompts/8\_three\_column\_architecture.md

## Three-Column Architecture Comparison

### Prompt

```md
{
[IMAGE PROMPT]
TITLE & THEME:
Create a clean, high-resolution, flat-style infographic titled "[SYSTEM A] vs [SYSTEM B] vs [SYSTEM C]" that clearly communicates "Evolution of [YOUR ARCHITECTURE TYPE]" to a professional audience. The tone should be technical, comparative, and visually engaging, suitable for LinkedIn.

BRAND STYLING RULES:
- Background: white.
- Accent colors: [PRIMARY HEX] with different intensities for each architecture type.
- Typography: geometric sans-serif (Inter, Poppins, or SF Pro) with strict hierarchy:
   * Architecture titles: bold, large, ≤ 20 characters.
   * Component labels: medium weight, ≤ 15 characters.
   * Descriptions: ≤ 25 words, technical but accessible.
- Alignment: Three-column comparison layout with consistent spacing.
- All icons flat, vector-sharp, system-focused.

LAYOUT GRID & SECTION ORDER:
1. **Header** (Top center)
   - Shared input element (query, trigger, etc.)
   - Attribution or branding element

2. **Three Architecture Columns** (Equal width)
   - [SYSTEM A] (left column)
   - [SYSTEM B] (center column)
   - [SYSTEM C] (right column)

3. **Output Section** (Bottom, shared or individual)
   - Output endpoints for each system
   - Consistent styling across architectures

TYPOGRAPHY & ICONOGRAPHY:
- Architecture titles: 18pt bold
- Component labels: 12pt medium
- Process text: 10pt regular
- Icons: 32×32px, consistent color theme
- System components: geometric shapes
- Flow arrows: clean directional lines

COLOR & DESIGN RULES:
- Light [COLOR] backgrounds for each column
- Darker [COLOR] for component boxes
- White text on colored backgrounds
- Consistent border radius on all components
- Clean separation lines between columns
- Subtle shadows for depth

TECHNICAL OUTPUT SPECS:
- Size: 1080×1350 px (4:5 ratio) for LinkedIn
- Format: PNG for static version
- Resolution: 300 DPI
- Clean architectural diagrams
- Technical accuracy in component representation
}
```

### ASCII Visualization

```
┌─────────────────────────────────────────────────────────────────────┐
│                                                                     │
│              [SYSTEM A] vs [SYSTEM B] vs [SYSTEM C]                │
│                                                                     │
│                          User Query                                 │
│                             │                                       │
│          ┌─────────────────────────────────────────┐                │
│          │                                         │                │
├──────────┼─────────────────────────────────────────┼────────────────┤
│          │                                         │                │
│ ┌────────▼────────┐ ┌─────────▼─────────┐ ┌────────▼────────┐      │
│ │   [SYSTEM A]    │ │   [SYSTEM B]      │ │   [SYSTEM C]    │      │
│ │                 │ │                   │ │                 │      │
│ │ ┌─────────────┐ │ │ ┌─────────────┐   │ │ ┌─────────────┐ │      │
│ │ │ Database    │ │ │ │   Memory    │   │ │ │   Memory    │ │      │
│ │ │ 🗄️          │ │ │ │   🧠        │   │ │ │   🧠        │ │      │
│ │ └─────────────┘ │ │ └─────────────┘   │ │ └─────────────┘ │      │
│ │        │        │ │        │          │ │        │        │      │
│ │        ▼        │ │        ▼          │ │        ▼        │      │
│ │ ┌─────────────┐ │ │ ┌─────────────┐   │ │ ┌─────────────┐ │      │
│ │ │ Embedding   │ │ │ │ Planning    │   │ │ │  Planning   │ │      │
│ │ │ 📊          │ │ │ │ 📋          │   │ │ │  📋         │ │      │
│ │ └─────────────┘ │ │ └─────────────┘   │ │ └─────────────┘ │      │
│ │        │        │ │        │          │ │        │        │      │
│ │        ▼        │ │        ▼          │ │        ▼        │      │
│ │ ┌─────────────┐ │ │ ┌─────────────┐   │ │ ┌─────────────┐ │      │
│ │ │ Vector DB   │ │ │ │ Agent       │   │ │ │Query Agent  │ │      │
│ │ │ 🔍          │ │ │ │ 🤖          │   │ │ │ 🔍          │ │      │
│ │ └─────────────┘ │ │ └─────────────┘   │ │ └─────────────┘ │      │
│ │        │        │ │        │          │ │        │        │      │
│ │        ▼        │ │        ▼          │ │        ▼        │      │
│ │ ┌─────────────┐ │ │ ┌─────────────┐   │ │ ┌─────────────┐ │      │
│ │ │ Retrieval   │ │ │ │ MCP Server  │   │ │ │ MCP Server  │ │      │
│ │ │ ⚡          │ │ │ │ 🔗          │   │ │ │ 🔗          │ │      │
│ │ └─────────────┘ │ │ └─────────────┘   │ │ └─────────────┘ │      │
│ │        │        │ │        │          │ │        │        │      │
│ │        ▼        │ │        ▼          │ │        ▼        │      │
│ │ ┌─────────────┐ │ │ ┌─────────────┐   │ │ ┌─────────────┐ │      │
│ │ │ Generation  │ │ │ │ Build KG    │   │ │ │Multi-agent  │ │      │
│ │ │ 🤖          │ │ │ │ 🕸️          │   │ │ │ Workflow    │ │      │
│ │ └─────────────┘ │ │ └─────────────┘   │ │ │ 🤖🤖🤖      │ │      │
│ │                 │ │                   │ │ └─────────────┘ │      │
│ └─────────────────┘ └───────────────────┘ └─────────────────┘      │
│          │                   │                     │                │
│          ▼                   ▼                     ▼                │
│    ┌──────────┐        ┌──────────┐          ┌──────────┐           │
│    │ Output   │        │ Output   │          │ Output   │           │
│    └──────────┘        └──────────┘          └──────────┘           │
│                                                                     │
└─────────────────────────────────────────────────────────────────────┘
```

---

# README.md (root)

```md
# Infographic Templates — Prompts + ASCII Layouts

This repository contains **8 pre-designed infographic templates**, each stored as a markdown file pairing a **prompt** with an **ASCII visualization**. Use them to generate consistent, LinkedIn-ready visuals with any AI image tool.

## Folders
- `prompts/` — All template markdown files

## Templates
1. Technical Architecture Diagram
2. Grid Concept Layout (4×5)
3. Horizontal Comparison Chart (3-Panel)
4. Workflow Comparison (2×2 Grid)
5. Circular/Radial Hub Layout
6. Timeline/Evolution Layout
7. Ascending Staircase/Maturity Model
8. Three-Column Architecture Comparison

## How to Use
1. Open any file in `prompts/` and copy the **Prompt** block into your image generator.
2. Keep the **ASCII Visualization** open as a structure guide while designing.
3. Export at **1080×1350 (4:5)**, 300 DPI, PNG for LinkedIn.

## Contributing
- Add new templates by creating a new markdown file in `prompts/` with the same structure (Prompt + ASCII Visualization).
- Submit PRs with a preview image in your description.

## License
MIT (or your preferred license).
```

