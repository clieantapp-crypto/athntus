# Al Thenayan Farms - Design Guidelines

## Design Approach
**Reference-Based E-commerce Approach**: Drawing inspiration from modern Middle Eastern e-commerce platforms with strong emphasis on product photography, cultural authenticity, and bilingual navigation patterns similar to Noon.com and Careem.

## Core Design Principles
- **Agricultural Authenticity**: Natural, farm-fresh aesthetic with warm earth tones
- **Cultural Duality**: Seamless Arabic-first RTL design with English support
- **Product-Centric**: Large, appetizing product imagery takes precedence
- **Trust & Transparency**: Clear pricing, availability status, farm origin emphasis

---

## Typography System

**Font Family**: Open Sans (via Google Fonts CDN)
- **Headings (H1)**: 46px, weight 700, line-height 1.2
- **Subheadings (H2)**: 28px, weight 600, line-height 1.3
- **Body Text**: 21px, weight 400, line-height 1.6
- **Product Prices**: 24px, weight 700
- **Buttons**: 18px, weight 600
- **Navigation**: 16px, weight 500

**RTL Typography Notes**: Ensure proper Arabic text rendering with appropriate line-height adjustments (1.8 for Arabic body text)

---

## Layout System

**Spacing Primitives**: Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24
- Container max-width: 1440px with px-4 on mobile, px-8 on tablet, px-12 on desktop
- Section vertical padding: py-12 (mobile), py-16 (tablet), py-24 (desktop)
- Card spacing: gap-6 (mobile), gap-8 (desktop)
- Grid columns: 1 column (mobile), 2 columns (tablet), 3-4 columns (desktop)

---

## Component Library

### Navigation Header
- **Sticky header** with logo (left for English, right for Arabic)
- **Search icon, user account icon, cart icon** with item count badge
- **Language toggle** (AR/EN) in top-right corner
- **Transparent background** with slight blur when scrolled, white background at top
- Height: 80px desktop, 64px mobile

### Hero Carousel
- **5 full-width slides** featuring product categories (Fish, Duck, Eggs, Goat, Pigeon)
- Each slide: **High-quality farm product photography** with subtle dark overlay (opacity 0.2)
- **CTA buttons** centered on each slide with blurred background (backdrop-blur-md, bg-white/20)
- Auto-rotate every 5 seconds with manual navigation dots
- Height: 70vh desktop, 50vh mobile

### Product Grid
- **12+ products** displayed in responsive grid
- Each product card includes:
  - Square product image (1:1 ratio) with subtle hover scale effect
  - Arabic product name (primary), English name (secondary, smaller)
  - Price in KWD with "السعر العادي" label
  - Stock status badge ("نفذ" for out of stock in accent blue)
  - "أضف إلى السلة" button (primary orange when available, disabled gray when out of stock)
- Card style: Clean white background, subtle shadow on hover, no border radius

### Shopping Cart
- **Slide-out panel** from right (Arabic) or left (English)
- Empty state: Icon, "سلة التسوق الخاصة بك فارغة" message, "متابعة التسوق" link
- Cart items: Product thumbnail, name, quantity stepper, remove button
- Sticky footer: Subtotal, "الدفع" checkout button
- Overlay backdrop with opacity 0.5

### Category Cards
- **5 category cards** in horizontal scroll (mobile) or grid (desktop)
- Each card: Category image, Arabic label, icon overlay
- Size: 280px × 360px with rounded corners (8px)
- Categories: سمك, بط, حمام, بيض, خروف

### Instagram Feed
- **Grid layout**: 3 columns (mobile), 4 columns (tablet), 6 columns (desktop)
- Square image tiles (1:1 ratio)
- Instagram icon overlay on hover
- Section title: "@althenayanfarms" in brand orange
- Last 15-18 posts displayed

### Footer
- **Three-column layout** (mobile stacks)
- Column 1: Farm logo, brief description in Arabic
- Column 2: Quick links (من نحن, سياسة الخصوصية, شروط الاستخدام)
- Column 3: Contact info, social media icons
- Bottom bar: Copyright text, payment method icons

### Buttons
**Primary Button** (اشتر الآن, أضف إلى السلة):
- Background: #E37E16, Text: #1A1A1A
- Border-radius: 41px (fully rounded pill shape)
- Padding: py-3 px-8
- No shadow, bold weight
- Hover: Darken background by 10%, scale 1.02

**Secondary Button** (انتقل إلى المحتوى):
- Background: #4770DB, Text: #EFF0F5
- Same styling as primary but with accent color

**On-Image Buttons**: Apply backdrop-blur-md with bg-white/20 background, white text

### Form Inputs
- Border: 1px solid #CCCCCC
- Border-radius: 0px (sharp corners)
- Padding: py-3 px-4
- Focus state: Border color changes to primary orange

---

## Images

### Hero Section Images
**Five rotating hero slides** featuring:
1. **Tilapia Fish**: Fresh fish on ice in farm setting
2. **French Duck**: Ducks in pastoral environment
3. **Chicken Eggs**: Basket of farm-fresh eggs
4. **Goat/Sheep**: Livestock in farm pasture
5. **Pigeon**: Pigeons in coop setting

All images should be **high-resolution (1920×1080+)**, naturally lit, warm color grading emphasizing freshness and quality.

### Product Images
- **12 product images** for grid: Clean, white/neutral background
- Square format (800×800px minimum)
- Professional food photography with appetizing presentation
- Consistent lighting and styling across all products

### Instagram Feed
- **15-18 square images** pulled from farm's social media
- Mix of: finished dishes, farm scenes, livestock close-ups, behind-the-scenes content

---

## Animations

**Minimal, purposeful animations only**:
- Carousel slide transitions: Fade with 0.6s duration
- Product card hover: Scale 1.03, shadow increase (0.3s ease)
- Cart slide-in: 0.4s ease-out from right/left
- Button hover: Background darken with 0.2s transition
- Image lazy loading: Fade-in on scroll (0.4s)

**No scroll-triggered animations or parallax effects**

---

## Bilingual & RTL Considerations

- **Default language**: Arabic (RTL)
- **Layout mirroring**: All directional properties flip (margin-left becomes margin-right, etc.)
- **Logo placement**: Right side for Arabic, left for English
- **Number formatting**: Keep Arabic numerals (0-9) even in Arabic mode for prices
- **Icon directions**: Flip chevrons, arrows in RTL mode
- **Text alignment**: Right-aligned for Arabic, left-aligned for English