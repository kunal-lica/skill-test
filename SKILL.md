

# Studio Ghibli Theme Park Architectural Visualization

> Enables AI agents to generate designs, illustrations, and UI experiences that capture the whimsical, handcrafted architectural aesthetic of Studio Ghibli theme park environments — blending European fantasy architecture with Japanese pastoral sensibility.

## When to Use This Skill

- When a user requests designs, illustrations, or UI themes inspired by Studio Ghibli, fantasy villages, whimsical architecture, or fairy-tale environments
- When building landing pages, game UIs, or immersive web experiences for theme parks, fantasy destinations, children's entertainment, or travel/tourism in a storybook style
- When creating concept art direction, mood boards, or style guides that evoke a warm, handcrafted, nostalgic fantasy world rooted in naturalism

## Core Principles

### 1. Organic Asymmetry in Architecture
Nothing is perfectly geometric. Structures appear hand-built with slight irregularities — rooflines that bow and undulate, walls that lean subtly, windows of varying sizes grouped organically. Buildings look as though they grew over decades through additions rather than being designed all at once. Roof pitches vary between 45°–65° and feature exaggerated curves at the eaves. Towers are cylindrical or conical with tapered tops, never sharp or aggressive.

### 2. Warm Earth-Tone Dominant Palette
The color world is grounded in sun-warmed earth tones with strategic accent colors drawn from nature. The palette reads as if viewed through golden-hour light even in daytime scenes. Colors appear slightly desaturated, as if painted in gouache or watercolor rather than digitally rendered.

### 3. Lush Greenery Integration
Architecture is never isolated from nature. Vegetation climbs walls, drapes over balconies, fills every gap between structures, and softens every hard edge. Grass is deep and textured, not flat. Trees are full-canopy deciduous with visible individual leaf clusters. Plantings appear semi-wild — cultivated but not manicured. The ratio of green/natural elements to built elements is approximately 40-60% green to 40-60% structure in any given composition.

### 4. Storybook Scale and Proportion
Human-scale details (doors, windows, railings) are slightly exaggerated in proportion — doors are taller and narrower, windows are more deeply recessed, chimneys are oversized. This creates a sense of childlike wonder, as if the viewer is slightly smaller than the world around them. Multi-story structures (3-5 floors) are common, with each floor slightly different in style, suggesting historical layering.

### 5. Handcrafted Material Honesty
Every surface communicates its material: plaster is textured with visible brush or trowel marks, timber framing is rough-hewn with visible grain, stone is irregular and mortared, roof tiles are individually placed with slight variation in color. Metal elements (railings, lanterns, weathervanes) appear wrought by hand — ornate but not machine-perfect. No material appears factory-produced or synthetic.

### 6. Layered Depth Composition
Scenes are composed in clear foreground-midground-background layers with atmospheric perspective. Foreground elements frame the scene (often vegetation or architectural details). The midground contains the primary subject. Background fades into soft sky or distant hills. This creates a storybook diorama effect.

### 7. Golden Atmospheric Light
Lighting is perpetually warm, evoking late morning or golden hour. Shadows are soft and slightly blue-tinted (never harsh black). There is a subtle ambient glow to the entire scene. Light appears to wrap around objects rather than creating sharp contrast. The sky is typically a gentle gradient from warm blue to soft white near the horizon.

## Detailed Specifications

### Visual Language / Style Tokens

**Primary Color Palette:**
| Role | Color | Hex | Usage |
|------|-------|-----|-------|
| Warm Cream (walls) | Pale warm beige | `#F2E6D0` | Primary building surfaces, backgrounds |
| Timber Brown | Rich warm brown | `#6B4226` | Exposed timber framing, wood accents |
| Roof Terracotta | Muted red-brown | `#A0522D` | Roof tiles, brick details |
| Roof Slate | Warm dark grey | `#5C5C52` | Secondary roofing, stone bases |
| Deep Forest Green | Rich muted green | `#3A5F0B` | Dense foliage, hedges |
| Meadow Green | Warm mid green | `#6B8E23` | Grass, lighter vegetation |
| Leaf Green | Bright warm green | `#8FBC3B` | Sunlit foliage highlights |
| Sky Blue | Soft warm blue | `#87AECC` | Sky, water reflections |
| Sky White | Warm white | `#F0EDE4` | Horizon, clouds, light sources |
| Shadow Blue | Muted cool blue | `#7A8B99` | Shadows, depth |
| Accent Teal | Muted blue-green | `#4A7C72` | Patina on copper, special details |
| Accent Red | Warm brick red | `#8B3A3A` | Shutters, doors, small accents |
| Accent Gold | Warm ochre | `#C5A23E` | Ornamental details, weathervanes |

**Secondary/Accent Colors (used sparingly):**
- Window pane reflection: `#D4E4F0` (cool pale blue)
- Flower accents: `#D4698A` (muted rose), `#E8C84A` (warm yellow), `#7B68AE` (muted lavender)
- Smoke/mist: `#D8D4CC` at 40-60% opacity

**Typography (for UI applications):**
- Primary Headings: Serif with slight hand-drawn quality — use `Playfair Display`, `Cormorant Garamond`, or `EB Garamond` at weight 600-700
- Body Text: Warm humanist sans-serif — use `Nunito`, `Quicksand`, or `Lato` at weight 400
- Accent/Display: Hand-lettered or calligraphic — use `Caveat`, `Amatic SC`, or `Patrick Hand`
- Base font size: 16px, line-height 1.6, letter-spacing +0.02em on body
- Heading scale: 2.618 (golden ratio) — h1: 42px, h2: 26px, h3: 20px

**Spacing Scale (8px base):**
- xs: 4px
- sm: 8px
- md: 16px
- lg: 24px
- xl: 40px
- xxl: 64px
- Section padding: 64px–96px vertical

**Border and Shape Tokens:**
- Border radius (small elements — buttons, inputs): 12px
- Border radius (cards, panels): 20px–24px
- Border radius (large containers, modals): 32px
- No sharp corners anywhere in the design system
- Borders: 1px solid `#D4C9B8` (warm muted line) — never stark grey or black
- Prefer irregular/organic clip-paths or SVG masks over standard rectangles for image frames

**Shadows:**
- Card shadow: `0 4px 20px rgba(107, 66, 38, 0.12)`
- Elevated shadow: `0 8px 32px rgba(107, 66, 38, 0.18)`
- No sharp drop shadows; all shadows should feel like ambient occlusion
- Shadow color always warm-tinted, never pure black

**Texture and Surface:**
- Backgrounds should have subtle paper or canvas texture (noise at 2-4% opacity, warm-tinted)
- Illustration surfaces suggest brushstroke — slight grain, not photorealistic
- Gradients are always soft and warm: vertical from `#87AECC` to `#F0EDE4` for skies

### Component Patterns

**Card Component (e.g., destination card):**
```
- Container: 24px border-radius, warm cream background (#F2E6D0)
- Image area: fills top, masked with slight arch or irregular shape at bottom edge
- Content padding: 24px
- Title: Serif, 20px, weight 700, color #3D2B1F
- Description: Humanist sans, 15px, weight 400, color #6B5D4F, line-height 1.6
- CTA: Text link with arrow →, color #4A7C72, no underline, hover adds underline
- Shadow: 0 4px 20px rgba(107, 66, 38, 0.12)
- Hover: translateY(-4px), shadow expands to 0 8px 32px rgba(107, 66, 38, 0.18)
- Transition: all 0.3s ease
```

**Navigation Bar:**
```
- Semi-transparent warm cream: rgba(242, 230, 208, 0.9) with backdrop-blur: 12px
- Height: 72px
- Logo: hand-lettered or serif wordmark, positioned left
- Nav links: humanist sans, 14px, weight 600, uppercase, letter-spacing 0.08em
- Active state: underline in accent teal (#4A7C72), 2px, offset 6px below text
- Mobile: slide-in drawer from right with warm cream background, full-height
```

**Hero Section:**
```
- Full-width illustration or image with painterly quality
- Overlaid text positioned in lower-third or center
- Text has subtle warm text-shadow: 0 2px 8px rgba(61, 43, 31, 0.3)
- Optional: animated floating elements (leaves, clouds) using gentle CSS keyframes
- Height: 80vh–100vh
- Scroll indicator: hand-drawn arrow SVG, gentle bounce animation
```

**Button:**
```
- Primary: background #4A7C72, color #F2E6D0, border-radius 12px
- Padding: 12px 28px, font-size 15px, weight 600
- Hover: background #3A6B62, slight scale(1.02)
- Secondary: background transparent, border 2px solid #6B4226, color #6B4226
- Hover: background rgba(107, 66, 38, 0.08)
- All buttons have transition: all 0.25s ease
- Optional: tiny decorative SVG flourish beside text (leaf, star, swirl)
```

**Divider/Section Break:**
```
- Never a plain <hr>
- Use SVG ornamental divider: scrollwork, vine, or leaf motif
- Color: #C5A23E at 40% opacity, or #D4C9B8
- Width: 120px–200px, centered
- Margin: 40px auto
```

### Architectural Detail Reference (for illustrations/visual content)

**Roofing:** Overlapping clay or slate tiles, slightly varied in color (±10% lightness variation tile-to-tile). Ridge tiles are rounded. Dormers and turrets common. Moss or lichen patches on north-facing surfaces.

**Walls:** Combination of exposed stone (ground floor), plastered upper floors (cream/warm white), and half-timbered framing (dark brown timber with cream infill). Walls show age — subtle cracks, slight discoloration, water staining below windowsills.

**Windows:** Multi-pane with leading (6-12 panes per window). Deep-set in thick walls (visible depth of 8-12 inches). Shutters in muted colors (forest green, brick red, slate blue). Some windows are arched at top.

**Doors:** Arched or pointed-arch tops. Heavy wood planking with visible iron hardware (strap hinges, ring pulls). Often recessed within a stone or plastered archway.

**Exterior Details:** Wrought iron lanterns, flower boxes on windowsills (geraniums, trailing ivy), hanging shop signs (hand-painted on wood), cobblestone or flagstone paths, wooden barrels and crates as set dressing, weathervanes and chimney pots.

### Do's and Don'ts

**Do:**
- Use warm, golden lighting in all compositions — even overcast scenes should feel cozy, not cold
- Include at least 3 types of vegetation in any scene (ground cover, climbing plants, trees/shrubs)
- Layer textures: paper grain on backgrounds, brush-like rendering on illustrations, subtle noise on solid colors
- Make every structure look lived-in and loved — slight weathering, patina, personal touches
- Use gentle curves and organic shapes in layout and illustration — arches, rounded forms, flowing lines
- Include small delightful details that reward close inspection (a cat in a window, a bird on a chimney, a tiny garden)
- Create visual hierarchy through scale and warmth rather than contrast and bold color
- Apply atmospheric perspective in layered scenes (distant elements are lighter, bluer, softer)

**Don't:**
- Use pure black (`#000000`) anywhere — darkest value should be around `#2D2118`
- Use pure white (`#FFFFFF`) — lightest value should be around `#FAF7F2`
- Apply hard geometric shapes, sharp corners, or grid-perfect alignment — everything should feel organic
- Use neon, saturated, or cool-dominant color schemes
- Create flat, textureless surfaces — every surface needs material quality
- Include modern/industrial materials: concrete, steel, glass curtain walls, plastic
- Use aggressive typography: ultra-bold weights, tight tracking, all-caps body text
- Apply stark, high-contrast lighting with hard shadows
- Make scenes feel empty or sterile — the world should feel populated, even without visible people
- Use stock photography aesthetic — everything should look illustrated, painted, or artfully crafted

## Examples

### Example 1: Fantasy Village Landing Page

**Generic input:** "Create a landing page for a fantasy-themed tourist attraction"

**Styled output applying this skill:**
```
- Hero: Full-bleed illustration of a hilltop village at golden hour, rendered in gouache-style.
  Warm sky gradient (#87AECC → #F0EDE4 → #F2D9A0 near horizon). Village features 
  clustered buildings with terracotta and slate roofs, half-timber facades, a central 
  clock tower with conical copper-patina roof (#4A7C72). Foreground: wildflower meadow 
  with swaying grass. Midground: cobblestone path winding uphill between buildings. 
  Background: rolling green hills fading into atmospheric haze.

- Heading overlay: "Welcome to Meadowbrook" in EB Garamond, 48px, weight 700, 
  color #FAF7F2 with text-shadow: 0 3px 12px rgba(45, 33, 24, 0.4).
  Subhead in Nunito, 18px, weight 400: "Where every path leads to wonder"

- Section below: 3 cards in a row (responsive to single column on mobile)
  Each card: 24px radius, #F2E6D0 background, arch-shaped image mask at top,
  hand-drawn section divider between image and text. Card titles in Cormorant 
  Garamond. Subtle vine SVG ornament in corners.

- Footer: Dark warm tone (#3D2B1F), with muted cream text, hand-drawn map 
  illustration, and ornamental vine border at top edge.
```

### Example 2: Mobile App Onboarding Screen

**Generic input:** "Design an onboarding screen for a nature exploration app"

**Styled output applying this skill:**
```
- Background: Subtle canvas-textured warm cream (#F2E6D0) with 3% warm noise overlay
- Top 55%: Circular illustration frame (hand-drawn irregular circle border in 
  #C5A23E, 2px stroke, slightly wobbly path) containing a scene of a cottage 
  nestled among old-growth trees, rendered in soft watercolor style. Light 
  filtering through canopy. Moss on stone walls. Smoke curling from chimney.

- Below illustration: 
  Title: "Discover Hidden Paths" — EB Garamond, 28px, weight 700, color #3D2B1F
  Body: "Every forest holds secrets for those who wander with wonder." — 
  Nunito, 16px, weight 400, color #6B5D4F, max-width 280px centered, 
  line-height 1.65

- Pagination dots: 3 dots, active dot is leaf-shaped SVG in #4A7C72, 
  inactive dots are circles in #D4C9B8

- CTA Button: "Begin Your Journey →" — background #4A7C72, color #F2E6D0, 
  border-radius 12px, padding 14px 32px, Nunito 15px weight 600.
  Tiny leaf SVG before the arrow.

- Bottom safe area: #F2E6D0 with faint vine watermark at 5% opacity
```

### Example 3: Data Dashboard with Ghibli Aesthetic

**Generic input:** "Style a park visitor analytics dashboard"

**Styled output applying this skill:**
```
- Background: #FAF7F2 with paper texture at 3% opacity
- Sidebar: #3D2B1F with cream text, navigation icons are hand-drawn line 
  illustrations (a compass, a map, a lantern, a leaf), active item has 
  warm highlight bar in #C5A23E

- Stat cards: 24px radius, #F2E6D0 fill, shadow 0 4px 20px rgba(107,66,38,0.12)
  Each card has a tiny watercolor illustration icon (visitors = footprints on 
  a path, revenue = a treasure chest, satisfaction = a smiling sun).
  Numbers: Cormorant Garamond, 36px, weight 700, color #3D2B1F
  Labels: Nunito, 13px, weight 600, color #6B5D4F, letter-spacing 0.06em

- Charts: Line charts use organic, slightly curved interpolation (cardinal spline)
  — never angular. Line color #4A7C72 with gradient fill fading to transparent.
  Grid lines: #D4C9B8 at 30% opacity. Axes labels in Nunito 12px #8B7D6F.
  Data points marked with small circles, not squares or diamonds.

- Table: No harsh grid lines. Rows separated by 1px #E8DFD0 dividers. 
  Alternating row tint: transparent / rgba(196, 181, 159, 0.08).
  Header row: Nunito 12px weight 700 uppercase, letter-spacing 0.08em, 
  color #6B5D4F, bottom border 2px #C5A23E.
```

## Implementation Notes

### CSS Custom Properties Setup
```css
:root {
  /* Colors */
  --ghibli-cream: #F2E6D0;
  --ghibli-cream-light: #FAF7F2;
  --ghibli-timber: #6B4226;
  --ghibli-terracotta: #A0522D;
  --ghibli-slate: #5C5C52;
  --ghibli-forest: #3A5F0B;
  --ghibli-meadow: #6B8E23;
  --ghibli-leaf: #8FBC3B;
  --ghibli-sky: #87AECC;
  --ghibli-sky-white: #F0EDE4;
  --ghibli-shadow: #7A8B99;
  --ghibli-teal: #4A7C72;
  --ghibli-red: #8B3A3A;
  --ghibli-gold: #C5A23E;
  --ghibli-dark: #3D2B1F;
  --ghibli-dark-max: #2D2118;
  --ghibli-text: #3D2B1F;
  --ghibli-text-secondary: #6B5D4F;
  --ghibli-border: #D4C9B8;
  
  /* Typography */
  --font-heading: 'EB Garamond', 'Cormorant Garamond', 'Playfair Display', Georgia, serif;
  --font-body: 'Nunito', 'Quicksand', 'Lato', sans-serif;
  --font-accent: 'Caveat', 'Patrick Hand', cursive;
  
  /* Spacing */
  --space-xs: 4px;
  --space-sm: 8px;
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 40px;
  --space-xxl: 64px;
  
  /* Radii */
  --radius-sm: 12px;
  --radius-md: 20px;
  --radius-lg: 32px;
  
  /* Shadows */
  --shadow-card: 0 4px 20px rgba(107, 66, 38, 0.12);
  --shadow-elevated: 0 8px 32px rgba(107, 66, 38, 0.18);
  --shadow-text: 0 2px 8px rgba(61, 43, 31, 0.3);
}
```

### Background Texture Technique
Apply a subtle paper texture using CSS pseudo-elements or an SVG noise filter:
```css
.ghibli-surface::after {
  content: '';
  position: absolute;
  inset: 0;
  background-image: url("data:image/svg+xml,..."); /* SVG turbulence noise */
  opacity: 0.03;
  mix-blend-mode: multiply;
  pointer-events: none;
}
```
Alternatively, use a semi-transparent warm-tinted noise PNG tile at 3-4% opacity with `mix-blend-mode: multiply`.

### Recommended Font Loading
```html
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:wght@400;600;700&family=Nunito:wght@400;600;700&family=Caveat:wght@400;700&display=swap" rel="stylesheet">
```

### Animation Guidelines
- All transitions: `0.25s–0.4s ease` or `cubic-bezier(0.25, 0.1, 0.25, 1)`
- Hover effects: subtle lift (translateY -2px to -4px) + shadow expansion
- Page transitions: gentle fade (300ms) or soft slide (400ms)
- Decorative animations (floating leaves, drifting clouds): very slow (8s–20s), subtle movement (10-30px travel), infinite loop with `ease-in-out`
- Never use bounce or elastic easing — movement should feel like a gentle breeze, not mechanical

### Framework-Specific Notes
- **Tailwind CSS:** Create a custom theme extending the default config with the color/spacing tokens above. Use `@apply` for component classes. The organic shapes will require custom SVG clip-paths or mask utilities.
- **React/Next.js:** Create a `<GhibliProvider>` theme context. Use CSS Modules or styled-components with the token variables. SVG ornaments should be React components for reusability.
- **Figma:** Set up a Ghibli Style Library with color styles, text styles, and effect styles matching the tokens. Create ornamental divider and frame components as reusable assets.

### Illustration/Image Guidance
When generating or sourcing images for this aesthetic:
- Prefer painterly, hand-rendered styles over photorealism
- If using AI image generation, prompt for "gouache painting," "watercolor illustration," "Studio Ghibli style," "Hayao Miyazaki background art"
- Post-process photographs with warm color grading: lift shadows to warm brown, shift highlights to cream, reduce overall saturation by 15-20%, add subtle grain
- Aspect ratios for hero images: 16:9 or 21:9 for panoramic landscape feel
- Minimum illustration detail density: include at least 5 distinct texture types visible in any architectural scene