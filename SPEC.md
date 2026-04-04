# SPEC.md - Horizon Auto Import 網站規格

## 1. Concept & Vision

**Horizon Auto Import** — 專業平行進口汽車代理，專營日本電動車進口香港。

品牌形象：專業、可靠、高端但不距離感。目標係建立信任，等香港同內地嘅潛在客戶覺得「呢間公司係真係做嘢嘅」。

核心情感：從疑惑到信任嘅旅程。

---

## 2. Design Language

### Aesthetic Direction
**Industrial Premium** — 深色金屬質感，帶有專業汽車展廳嘅感覺。高對比度，間中使用橙色/金色作為點綴，暗示動力和能量。

### Color Palette
```
Primary:     #1a1a2e (深藍黑 - 背景)
Secondary:   #16213e (深海軍 - 次要背景)
Accent:      #e94560 (活力紅 - CTA, 重點)
Gold:        #d4af37 (金色 - 信任、專業)
Light:       #f5f5f5 (淺灰 - 正文)
Muted:       #8b8b8b (灰色 - 次要文字)
Success:     #4ecca3 (綠色 - 成功狀態)
```

### Typography
- **Headings:** Montserrat (粗體、現代感)
- **Body:** Noto Sans TC (中文友好)
- **Accent:** Roboto Mono (數字、標籤)

### Spatial System
- 8px base unit
- Section padding: 80px vertical
- Card padding: 32px
- Gap between elements: 24px

### Motion Philosophy
- Scroll-triggered fade-in (subtle, 400ms ease-out)
- Hover states: scale 1.02 + shadow lift
- CTA buttons: subtle pulse animation
- Form focus: border glow transition

---

## 3. Layout & Structure

### Single Page Flow (由上至下)

1. **Navigation Bar** (sticky)
   - Logo (left)
   - Menu links (center): 服務 / 流程 / 關於 / 聯絡
   - CTA button (right): 立即查詢

2. **Hero Section**
   - Full viewport height
   - Background: dark gradient with subtle car silhouette overlay
   - Headline: 大標題口號
   - Subheadline: 副標題服務描述
   - Primary CTA: 免費評估
   - Secondary CTA:了解更多
   - Trust badges (if any)

3. **Services Section**
   - Section title: 我們的服務
   - 4 service cards in 2x2 grid:
     - 汽車類型評定
     - 電動車電力安全報告
     - 汽車代理申請
     - 日本進口服務
   - Each card: icon, title, description

4. **Why Choose Us (USP Section)**
   - 3 column layout
   - Icons + short descriptions
   - Focus on: 專業 / 可靠 / 高效

5. **Process Flow**
   - Horizontal timeline/stepper
   - 4 steps: 查詢 → 評估 → 代理 → 完成
   - Each step with icon and brief description

6. **About Section**
   - Company intro
   - Mission statement
   - Brief credentials/experience

7. **Contact/Inquiry Section** ⭐ 重点
   - Form fields:
     - 姓名 (required)
     - 電話 (required)
     - 電郵 (optional)
     - 汽車類型興趣 (dropdown: 電動車 / 汽油車 / 混合動力)
     - 查詢內容 (textarea)
   - Submit button: 提交查詢
   - Success message after submission
   - Privacy note

8. **Footer**
   - Company name
   - Contact info
   - Copyright

---

## 4. Features & Interactions

### Navigation
- Smooth scroll to sections on click
- Active section highlight in nav
- Mobile hamburger menu

### Hero CTA Buttons
- "免費評估" → scrolls to contact form
- "了解更多" → scrolls to services

### Service Cards
- Hover: lift + shadow + accent border
- Click: could link to detail or scroll to contact

### Process Timeline
- Steps highlight as user scrolls past
- Mobile: vertical layout

### Contact Form
- Real-time validation
- Required field indicators
- Submit → loading state → success message
- Form data stored locally (for demo) / could integrate with backend
- Error handling: field-level error messages

### Scroll Animations
- Elements fade in on scroll
- Staggered animation for card grids

---

## 5. Component Inventory

### NavBar
- States: default, scrolled (smaller + shadow), mobile (hamburger open)
- Logo: text-based "HORIZON AUTO"

### Hero
- Background gradient with overlay pattern
- Two CTA buttons (primary filled, secondary outlined)

### Service Card
- States: default, hover (lifted), focus
- Icon (SVG or emoji), title, description

### USP Item
- Icon, heading, short text
- Hover: icon color change

### Process Step
- States: inactive, active (highlighted), completed
- Number badge, icon, title, description

### Form Input
- States: default, focus (glow border), error (red border + message), valid (green check)
- Label above, placeholder inside

### Submit Button
- States: default, hover, loading (spinner), disabled
- Full width on mobile

### Footer
- Dark background, centered content

---

## 6. Technical Approach

### Stack
- **HTML5** — semantic structure
- **CSS3** — custom properties, flexbox, grid, animations
- **Vanilla JavaScript** — form handling, scroll effects, mobile menu
- **No frameworks** — keep it simple and fast

### File Structure
```
horizon-auto/
├── index.html
├── styles.css
├── script.js
└── SPEC.md
```

### Form Handling
- Client-side validation
- On submit: show success message (no backend for now)
- Could integrate with Formspree/EmailJS later

### Responsive Breakpoints
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Performance
- Minimal external dependencies (only Google Fonts)
- Optimized SVG icons (inline)
- Lazy animation loading

---

## 7. Content (Chinese)

### Hero
- Headline: 專業平行進口汽車代理
- Subheadline: 專營日本電動車進口香港，全方位一站式服務

### Services
1. **汽車類型評估** — 專業評估進口可行性，確保符合香港法例
2. **電動車電力安全報告** — 全面檢測電動車電力系統，安全有保障
3. **汽車代理申請** — 代辦進口許可證，省時省力
4. **日本進口服務** — 從日本採購到香港交付，一站式服務

### USP
- 專業資格 — 多年汽車進口經驗，熟悉香港法例
- 可靠保障 — 完整文件流程，確保順利通關
- 高效服務 — 一星期內完成評估，快速回覆查詢

### Process
1. 查詢 — 聯絡我們講解需求
2. 評估 — 專業團隊評估可行性
3. 代理 — 代辦所有進口程序
4. 完成 — 汽車交付，客戶驗收

### About
Horizon Auto 專營平行進口汽車業務，特別專注於日本電動車市場。我們明白香港駕駛者對高質量電動車嘅需求，提供從採購、評估、代理到交付嘅全方位服務。

### Contact Form Note
- 標題: 立即查詢
- Subtitle: 填寫以下表格，我們將在24小時內回覆
- Privacy note: 我們重視您的私隱，不會向第三方透露您的資料
