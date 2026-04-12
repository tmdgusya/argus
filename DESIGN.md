# Design System Inspired by Sentry

## 1. Visual Theme & Atmosphere

Sentry's website is a dark-mode-first developer tool interface that speaks the language of code editors and terminal windows. The entire aesthetic is rooted in deep purple-black backgrounds (`#1f1633`, `#150f23`) that evoke the late-night debugging sessions Sentry was built for. Against this inky canvas, a carefully curated set of purples, pinks, and a distinctive lime-green accent (`#c2ef4e`) create a visual system that feels simultaneously technical and vibrant.

The typography pairing is deliberate: "Dammit Sans" appears at hero scale (88px, weight 700) as a display font with personality and attitude that matches Sentry's irreverent brand voice ("Code breaks. Fix it faster."), while Rubik serves as the workhorse UI font across all functional text — headings, body, buttons, captions, and navigation. Monaco provides the monospace layer for code snippets and technical content, completing the developer-tool trinity.

What makes Sentry distinctive is its embrace of the "dark IDE" aesthetic without feeling cold or sterile. Warm purple tones replace the typical cool grays of developer tools, and bold illustrative elements (3D characters, colorful product screenshots) punctuate the dark canvas. The button system uses a signature muted purple (`#79628c`) with inset shadows that creates a tactile, almost physical quality — buttons feel like they could be pressed into the surface.

**Key Characteristics:**
- Dark purple-black backgrounds (`#1f1633`, `#150f23`) — never pure black
- Warm purple accent spectrum: from deep (`#362d59`) through mid (`#79628c`, `#6a5fc1`) to vibrant (`#422082`)
- Lime-green accent (`#c2ef4e`) for high-visibility CTAs and highlights
- Pink/coral accents (`#ffb287`, `#fa7faa`) for focus states and secondary highlights
- "Dammit Sans" display font for brand personality at hero scale
- Rubik as primary UI font with uppercase letter-spaced labels
- Monaco monospace for code elements
- Inset shadows on buttons creating tactile depth
- Frosted glass effects with `blur(18px) saturate(180%)`

## 2. Color Palette & Roles

### Primary Brand
- **Deep Purple** (`#1f1633`): Primary background, the defining color of the brand
- **Darker Purple** (`#150f23`): Deeper sections, footer, secondary backgrounds
- **Border Purple** (`#362d59`): Borders, dividers, subtle structural lines

### Accent Colors
- **Sentry Purple** (`#6a5fc1`): Primary interactive color — links, hover states, focus rings
- **Muted Purple** (`#79628c`): Button backgrounds, secondary interactive elements
- **Deep Violet** (`#422082`): Select dropdowns, active states, high-emphasis surfaces
- **Lime Green** (`#c2ef4e`): High-visibility accent, special links, badge highlights
- **Coral** (`#ffb287`): Focus state backgrounds, warm accent
- **Pink** (`#fa7faa`): Focus outlines, decorative accents

### Text Colors
- **Pure White** (`#ffffff`): Primary text on dark backgrounds
- **Light Gray** (`#e5e7eb`): Secondary text, muted content
- **Code Yellow** (`#dcdcaa`): Syntax highlighting, code tokens

### Surface & Overlay
- **Glass White** (`rgba(255, 255, 255, 0.18)`): Frosted glass button backgrounds
- **Glass Dark** (`rgba(54, 22, 107, 0.14)`): Hover overlay on glass elements
- **Input White** (`#ffffff`): Form input backgrounds (light context)
- **Input Border** (`#cfcfdb`): Form field borders

### Shadows
- **Ambient Glow** (`rgba(22, 15, 36, 0.9) 0px 4px 4px 9px`): Deep purple ambient shadow
- **Button Hover** (`rgba(0, 0, 0, 0.18) 0px 0.5rem 1.5rem`): Elevated hover state
- **Card Shadow** (`rgba(0, 0, 0, 0.1) 0px 10px 15px -3px`): Standard card elevation
- **Inset Button** (`rgba(0, 0, 0, 0.1) 0px 1px 3px 0px inset`): Tactile pressed effect

## 3. Typography Rules

### Font Families
- **Display**: `Dammit Sans` — brand personality font for hero headings
- **Primary UI**: `Rubik`, with fallbacks: `-apple-system, system-ui, Segoe UI, Helvetica, Arial`
- **Monospace**: `Monaco`, with fallbacks: `Menlo, Ubuntu Mono`

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|------|--------|-------------|----------------|-------|
| Display Hero | Dammit Sans | 88px (5.50rem) | 700 | 1.20 (tight) | normal | Maximum impact, brand voice |
| Display Secondary | Dammit Sans | 60px (3.75rem) | 500 | 1.10 (tight) | normal | Secondary hero text |
| Section Heading | Rubik | 30px (1.88rem) | 400 | 1.20 (tight) | normal | Major section titles |
| Sub-heading | Rubik | 27px (1.69rem) | 500 | 1.25 (tight) | normal | Feature section headers |
| Card Title | Rubik | 24px (1.50rem) | 500 | 1.25 (tight) | normal | Card and block headings |
| Feature Title | Rubik | 20px (1.25rem) | 600 | 1.25 (tight) | normal | Emphasized feature names |
| Body | Rubik | 16px (1.00rem) | 400 | 1.50 | normal | Standard body text |
| Body Emphasis | Rubik | 16px (1.00rem) | 500–600 | 1.50 | normal | Bold body, nav items |
| Nav Label | Rubik | 15px (0.94rem) | 500 | 1.40 | normal | Navigation links |
| Uppercase Label | Rubik | 15px (0.94rem) | 500 | 1.25 (tight) | normal | `text-transform: uppercase` |
| Button Text | Rubik | 14px (0.88rem) | 500–700 | 1.14–1.29 (tight) | 0.2px | `text-transform: uppercase` |
| Caption | Rubik | 14px (0.88rem) | 500–700 | 1.00–1.43 | 0.2px | Often uppercase |
| Small Caption | Rubik | 12px (0.75rem) | 600 | 2.00 (relaxed) | normal | Subtle annotations |
| Micro Label | Rubik | 10px (0.63rem) | 600 | 1.80 (relaxed) | 0.25px | `text-transform: uppercase` |
| Code | Monaco | 16px (1.00rem) | 400–700 | 1.50 | normal | Code blocks, technical text |

### Principles
- **Dual personality**: Dammit Sans brings irreverent brand character at display scale; Rubik provides clean professionalism for everything functional.
- **Uppercase as system**: Buttons, captions, labels, and micro-text all use `text-transform: uppercase` with subtle letter-spacing (0.2px–0.25px), creating a systematic "technical label" pattern throughout.
- **Weight stratification**: Rubik uses 400 (body), 500 (emphasis/nav), 600 (titles/strong), 700 (buttons/CTAs) — a clean four-tier weight system.
- **Tight headings, relaxed body**: All headings use 1.10–1.25 line-height; body uses 1.50; small captions expand to 2.00 for readability at tiny sizes.

## 4. Component Stylings

### Buttons

**Primary Muted Purple**
- Background: `#79628c` (rgb(121, 98, 140))
- Text: `#ffffff`, uppercase, 14px, weight 500–700, letter-spacing 0.2px
- Border: `1px solid #584674`
- Radius: 13px
- Shadow: `rgba(0, 0, 0, 0.1) 0px 1px 3px 0px inset` (tactile inset)
- Hover: elevated shadow `rgba(0, 0, 0, 0.18) 0px 0.5rem 1.5rem`

**Glass White**
- Background: `rgba(255, 255, 255, 0.18)` (frosted glass)
- Text: `#ffffff`
- Padding: 8px
- Radius: 12px (left-aligned variant: `12px 0px 0px 12px`)
- Shadow: `rgba(0, 0, 0, 0.08) 0px 2px 8px`
- Hover background: `rgba(54, 22, 107, 0.14)`
- Use: Secondary actions on dark surfaces

**White Solid**
- Background: `#ffffff`
- Text: `#1f1633`
- Padding: 12px 16px
- Radius: 8px
- Hover: background transitions to `#6a5fc1`, text to white
- Focus: background `#ffb287` (coral), outline `rgb(106, 95, 193) solid 0.125rem`
- Use: High-visibility CTA on dark backgrounds

**Deep Violet (Select/Dropdown)**
- Background: `#422082`
- Text: `#ffffff`
- Padding: 8px 16px
- Radius: 8px

### Inputs

**Text Input**
- Background: `#ffffff`
- Text: `#1f1633`
- Border: `1px solid #cfcfdb`
- Padding: 8px 12px
- Radius: 6px
- Focus: border-color stays `#cfcfdb`, shadow `rgba(0, 0, 0, 0.15) 0px 2px 10px inset`

### Links
- **Default on dark**: `#ffffff`, underline decoration
- **Hover**: color transitions to `#6a5fc1` (Sentry Purple)
- **Purple links**: `#6a5fc1` default, hover underline
- **Lime accent links**: `#c2ef4e` default, hover to `#6a5fc1`
- **Dark context links**: `#362d59`, hover to `#ffffff`

### Cards & Containers
- Background: semi-transparent or dark purple surfaces
- Radius: 8px–12px
- Shadow: `rgba(0, 0, 0, 0.1) 0px 10px 15px -3px`
- Backdrop filter: `blur(18px) saturate(180%)` for glass effects

### Navigation
- Dark transparent header over hero content
- Rubik 15px weight 500 for nav links
- White text, hover to Sentry Purple (`#6a5fc1`)
- Uppercase labels with 0.2px letter-spacing for categories
- Mobile: hamburger menu, full-width expanded

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 1px, 2px, 4px, 5px, 6px, 8px, 12px, 16px, 24px, 32px, 40px, 44px, 45px, 47px

### Grid & Container
- Max content width: 1152px (XL breakpoint)
- Responsive padding: 2rem (mobile) → 4rem (tablet+)
- Content centered within container
- Full-width dark sections with contained inner content

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | < 576px | Single column, stacked layout |
| Small Tablet | 576–640px | Minor width adjustments |
| Tablet | 640–768px | 2-column begins |
| Small Desktop | 768–992px | Full nav visible |
| Desktop | 992–1152px | Standard layout |
| Large Desktop | 1152–1440px | Max-width content |

### Whitespace Philosophy
- **Dark breathing room**: Generous vertical spacing between sections (64px–80px+) lets the dark background serve as a visual rest.
- **Content islands**: Feature sections are self-contained blocks floating in the dark purple sea, each with its own internal spacing rhythm.
- **Asymmetric padding**: Buttons use asymmetric padding patterns (12px 16px, 8px 12px) that feel organic rather than rigid.

### Border Radius Scale
- Minimal (6px): Form inputs, small interactive elements
- Standard (8px): Buttons, cards, containers
- Comfortable (10px–12px): Larger containers, glass panels
- Rounded (13px): Primary muted buttons
- Pill (18px): Image containers, badges

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Sunken (Level -1) | Inset shadow `rgba(0, 0, 0, 0.1) 0px 1px 3px inset` | Primary buttons (tactile pressed feel) |
| Flat (Level 0) | No shadow | Default surfaces, dark backgrounds |
| Surface (Level 1) | `rgba(0, 0, 0, 0.08) 0px 2px 8px` | Glass buttons, subtle cards |
| Elevated (Level 2) | `rgba(0, 0, 0, 0.1) 0px 10px 15px -3px` | Cards, floating panels |
| Prominent (Level 3) | `rgba(0, 0, 0, 0.18) 0px 0.5rem 1.5rem` | Hover states, modals |
| Ambient (Level 4) | `rgba(22, 15, 36, 0.9) 0px 4px 4px 9px` | Deep purple ambient glow around hero |

**Shadow Philosophy**: Sentry uses a unique combination of inset shadows (buttons feel pressed INTO the surface) and ambient glows (content radiates from the dark background). The deep purple ambient shadow (`rgba(22, 15, 36, 0.9)`) is the signature — it creates a bioluminescent quality where content seems to emit its own purple-tinted light.

## 7. Do's and Don'ts

### Do
- Use deep purple backgrounds (`#1f1633`, `#150f23`) — never pure black (`#000000`)
- Apply inset shadows on primary buttons for the tactile pressed effect
- Use Dammit Sans ONLY for hero/display headings — Rubik for everything else
- Apply `text-transform: uppercase` with `letter-spacing: 0.2px` on buttons and labels
- Use the lime-green accent (`#c2ef4e`) sparingly for maximum impact
- Employ frosted glass effects (`blur(18px) saturate(180%)`) for layered surfaces
- Maintain the warm purple shadow tones — shadows should feel purple-tinted, not neutral gray
- Use Rubik's 4-tier weight system: 400 (body), 500 (nav/emphasis), 600 (titles), 700 (CTAs)

### Don't
- Don't use pure black (`#000000`) for backgrounds — always use the warm purple-blacks
- Don't apply Dammit Sans to body text or UI elements — it's display-only
- Don't use standard gray (`#666`, `#999`) for borders — use purple-tinted grays (`#362d59`, `#584674`)
- Don't drop the uppercase treatment on buttons — it's a system-wide pattern
- Don't use sharp corners (0px radius) — minimum 6px for all interactive elements
- Don't mix the lime-green accent with the coral/pink accents in the same component
- Don't use flat (non-inset) shadows on primary buttons — the tactile quality is signature
- Don't forget letter-spacing on uppercase text — 0.2px minimum

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <576px | Single column, hamburger nav, stacked CTAs |
| Tablet | 576–768px | 2-column feature grids begin |
| Small Desktop | 768–992px | Full navigation, side-by-side layouts |
| Desktop | 992–1152px | Max-width container, full layout |
| Large | >1152px | Content max-width maintained, generous margins |

### Collapsing Strategy
- Hero text: 88px Dammit Sans → 60px → mobile scales
- Navigation: horizontal → hamburger with slide-out
- Feature sections: side-by-side → stacked cards
- Buttons: inline → full-width stacked on mobile
- Container padding: 4rem → 2rem

## 9. Dashboard Architecture

> Argus는 모니터링 대시보드입니다. 마케팅 랜딩 페이지가 아닙니다.
> 모든 뷰는 "데이터를 빠르게 읽고 상태를 파악"하는 것에 최적화되어야 합니다.
> Sentry Issues Dashboard, Grafana, Datadog을 시각 참조로 삼으세요.

### 9.1 전체 레이아웃 구조

```
┌──────────────────────────────────────────────────────────┐
│  Sidebar Nav (240px, 고정)  │  Main Content Area         │
│  ─────────────────────────  │  ─────────────────────     │
│                            │                            │
│  ◆ Argus (logo)            │  [Breadcrumb / View Title]  │
│                            │                            │
│  ── Profiles ──            │  ┌──────────────────────┐  │
│  > default                 │  │                      │  │
│    backend                 │  │   Active View        │  │
│    frontend                │  │   Content            │  │
│                            │  │                      │  │
│  ── Views ──               │  │                      │  │
│  [Status] [Activity]       │  │                      │  │
│  [Cost]    [Tools]         │  └──────────────────────┘  │
│  [Overview]                │                            │
│                            │                            │
│  ── System ──              │                            │
│  [Settings]                │                            │
│                            │                            │
└──────────────────────────────────────────────────────────┘
```

**제약 규칙:**
- Sidebar는 항상 고정(fixed), 스크롤되지 않음. 프로필이 많아지면 sidebar 내부만 스크롤
- Main Content Area만 스크롤. sidebar는 viewport에 고정
- Sidebar 배경: `#150f23` (더 어두운 퍼플), Main Content 배경: `#1f1633`
- Sidebar ↔ Main 구분선: `1px solid #362d59`
- 모바일(< 768px): sidebar는 햄버거 메뉴로 접힘, main content가 전체 폭 사용

### 9.2 Profile Selector

Sidebar 상단의 프로필 목록. 클릭하면 해당 프로필의 데이터를 main content에 로드.

```
┌─ Profiles ─────────────┐
│ ● default        ← 선택됨 (lime-green dot) │
│ ○ backend              │
│ ○ frontend             │
└────────────────────────┘
```

- 프로필명: Rubik 15px weight 500, `#e5e7eb`
- 선택된 프로필: `#ffffff`, 좌측에 `2px solid #c2ef4e` (lime-green) 인디케이터
- 선택된 프로필 좌측 dot: `#c2ef4e` 8px circle, 미선택은 `#362d59` 8px circle
- 호버: 배경 `rgba(255,255,255,0.05)`, radius 8px
- 프로필 옆에 상태 아이콘: gateway alive면 `●` green, stopped면 `●` `#584674`

### 9.3 View Navigation

Sidebar 하단의 뷰 탭. Profile과 독립적으로 뷰를 전환.

```
┌─ Views ────────────────┐
│  Status                │
│  Activity              │
│  Cost                  │
│  Tools                 │
│  ◉ Overview            │  ← 크로스 프로필 뷰 (항상 활성)
└────────────────────────┘
```

- 뷰명: Rubik 13px weight 500, `#e5e7eb`, uppercase, letter-spacing 0.2px
- 활성 뷰: `#ffffff`, 배경 `rgba(106, 95, 193, 0.15)`, radius 8px
- Overview는 프로필 선택과 무관하게 항상 모든 프로필 데이터를 보여줌
- 호버: `rgba(255,255,255,0.05)`

---

## 10. View별 상세 스펙

### 10.1 Status View — "이 에이전트는 지금 뭐 하는가?"

> **시각 참조**: Sentry의 "Project → Issues" 화면. 상단에 요약 카드 행, 하단에 상세 리스트.
> 카드는 그리드로 배치되되, 각 카드가 하나의 "상태 지표"를 담당.

```
┌─ Status ──────────────────────────────────────────────────┐
│                                                          │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐ │
│  │ GATEWAY  │  │ SESSIONS │  │  MODEL   │  │ PROVIDER │ │
│  │  ● ALIVE │  │    3     │  │ glm-5    │  │ zai      │ │
│  │  Uptime  │  │  active  │  │  turbo   │  │ ● OK     │ │
│  │  2h 14m  │  │          │  │          │  │ pool: 3  │ │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘ │
│                                                          │
│  Recent Sessions                                         │
│  ┌──────────────────────────────────────────────────────┐│
│  │ ● Debug API timeout issue        5m ago   In Progress││
│  │ ● Review PR #42                  2h ago   Done       ││
│  │ ● Setup cron for ticket polling  1d ago   Done       ││
│  └──────────────────────────────────────────────────────┘│
└──────────────────────────────────────────────────────────┘
```

**상태 카드 행 (Summary Cards):**
- 4개 카드, 그리드 `1fr 1fr 1fr 1fr`, gap 16px
- 카드 내부 padding: 20px
- 카드 배경: `rgba(255,255,255,0.04)`, border `1px solid #362d59`, radius 12px
- 카드 라벨: Rubik 12px weight 600, `#e5e7eb`, uppercase, letter-spacing 0.25px
- 카드 값: Rubik 28px weight 700, `#ffffff`
- 카드 보조값: Rubik 13px weight 400, `#79628c`
- Gateway 상태: alive면 `#c2ef4e`, stopped면 `#fa7faa`
- Credential 상태: 정상이면 `#c2ef4e`, exhausted면 `#ffb287`

**Recent Sessions 리스트:**
- 리스트 배경: 카드와 동일한 스타일, radius 12px
- 각 행: padding 12px 16px, border-bottom `1px solid rgba(54,45,89,0.5)`
- 마지막 행은 border-bottom 없음
- 세션 제목: Rubik 14px weight 500, `#ffffff`
- 시간: Rubik 12px weight 400, `#79628c`
- 상태 배지: radius 8px, padding 2px 8px
  - In Progress: 배경 `rgba(194,239,78,0.15)`, 텍스트 `#c2ef4e`
  - Done: 배경 `rgba(106,95,193,0.15)`, 텍스트 `#6a5fc1`
  - Error: 배경 `rgba(250,127,170,0.15)`, 텍스트 `#fa7faa`

**Status View 체크리스트:**
- [ ] 상태 카드 4개가 한 줄에 배치 (desktop)
- [ ] 카드 hover 시 `rgba(255,255,255,0.06)` 배경으로 미세 변화
- [ ] Gateway 상태가 실시간 갱신 (polling 또는 SSE)
- [ ] 세션 리스트는 최신 10개까지만 표시, 스크롤 없음

### 10.2 Activity View — "지금 무슨 일이 일어나고 있는가?"

> **시각 참조**: Sentry의 "Project → Stream" (실시간 이벤트 스트림).
> 타임라인 형식이 아닌 테이블 형식 — 밀도 높은 정보 전달.

```
┌─ Activity ────────────────────────────────────────────────┐
│                                                          │
│  Filter: [All ▾] [Errors ▾] [Tools ▾]     Search [___]   │
│                                                          │
│  ┌──────────────────────────────────────────────────────┐│
│  │ 14:32:05  user     message              model: glm-5 ││
│  │ 14:32:06  agent    tool:terminal          exec ls    ││
│  │ 14:32:08  agent    tool:read_file         config.yaml││
│  │ 14:32:12  agent    message              response...  ││
│  │ 14:32:15  agent    tool:terminal          npm test   ││
│  │ 14:33:01  agent    message              done. PR...  ││
│  └──────────────────────────────────────────────────────┘│
└──────────────────────────────────────────────────────────┘
```

**필터 바:**
- 배경: 없음, main content 배경에 직접 배치
- 필터 버튼: Glass White 스타일 (`rgba(255,255,255,0.08)`, radius 8px, padding 6px 12px)
- 활성 필터: 배경 `rgba(106,95,193,0.2)`, 텍스트 `#ffffff`
- 서치: Input 스타일 (Section 4 참조), placeholder "Search activity..."

**이벤트 행:**
- 폰트: Monaco 13px weight 400 (monospace — 이 뷰는 터미널 로그처럼 읽혀야 함)
- 행 높이: 32px, padding 0 16px
- 타임스탬프: `#79628c`, 고정 폭 70px
- 롤(user/agent): `#e5e7eb`, 고정 폭 50px
- 타입(message/tool): message는 텍스트, tool은 `#c2ef4e` + tool 이름 bold
- 툴 인자: `#584674`
- 행 호버: 배경 `rgba(255,255,255,0.03)`
- message 타입 행: 줄바꿈 허용, 최대 3줄까지만 표시 (truncate with "...")
- tool 타입 행: 단일 줄, overflow hidden + text-overflow ellipsis

**Activity View 체크리스트:**
- [ ] 폰트가 Monaco (monospace) — 터미널 느낌
- [ ] 최신 이벤트가 상단에 표시 (reverse chronological)
- [ ] 자동 스크롤: 새 이벤트 도착 시 맨 위로 고정 (사용자가 위로 스크롤하면 자동 스크롤 일시정지)
- [ ] message 행과 tool 행이 시각적으로 구분 가능 (tool은 좌측에 `→` 아이콘)

### 10.3 Cost View — "얼마를 쓰고 있는가?"

> **시각 참조**: Vercel Dashboard의 Usage 페이지.
> 상단에 요약 숫자 카드, 하단에 시계열 차트 + 테이블.
> 숫자가 주인공인 뷰 — 차트가 장식이 아니라 핵심 정보.

```
┌─ Cost ────────────────────────────────────────────────────┐
│                                                          │
│  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐   │
│  │ TOTAL TOKENS │  │ EST. COST    │  │ CACHE HIT    │   │
│  │   142,850    │  │   $2.34      │  │    67.2%     │   │
│  │  ↑ 12% vs day│  │  ↑ 8% vs day │  │  ↓ 3% vs day│   │
│  └──────────────┘  └──────────────┘  └──────────────┘   │
│                                                          │
│  Token Usage (7d)                                        │
│  ┌──────────────────────────────────────────────────────┐│
│  │     ╱╲                                                ││
│  │   ╱  ╲  ╱╲                                           ││
│  │  ╱    ╲╱  ╲  ╱╲                                     ││
│  │ ╱           ╲╱  ╲                                    ││
│  │ Mon  Tue  Wed  Thu  Fri  Sat  Sun                   ││
│  └──────────────────────────────────────────────────────┘│
│                                                          │
│  Cost by Model                          Cost by Day       │
│  ┌────────────────┐  ┌─────────────────────────────────┐│
│  │ glm-5-turbo    │  │ Apr 10  $0.42                   ││
│  │ ████████████ 78%│  │ Apr 11  $0.91                   ││
│  │ gemini-3-flash │  │ Apr 12  $1.01                   ││
│  │ ██        22%  │  │ Apr 13  $0.00                   ││
│  └────────────────┘  └─────────────────────────────────┘│
└──────────────────────────────────────────────────────────┘
```

**요약 카드:**
- 3개 카드, 그리드 `1fr 1fr 1fr`, gap 16px
- 카드 스타일: Status View와 동일
- 메인 숫자: Rubik 32px weight 700, `#ffffff`
- 트렌드 화살표: Rubik 13px weight 500
  - 증가(`↑`): `#fa7faa` (비용 증가는 경고)
  - 감소(`↓`): `#c2ef4e` (캐시 적중률 증가는 긍정)
- "vs day" 텍스트: `#79628c`

**차트 영역:**
- 차트 배경: 카드와 동일 (`rgba(255,255,255,0.04)`, border `#362d59`, radius 12px)
- 차트 제목: Rubik 14px weight 600, `#e5e7eb`, uppercase, letter-spacing 0.2px
- 라인 차트 색상: `#6a5fc1` (Sentry Purple) — 라인 2px, fill `rgba(106,95,193,0.1)`
- X축 라벨: Rubik 11px weight 400, `#79628c`
- Y축 라벨: Rubik 11px weight 400, `#79628c`
- 그리드 라인: `rgba(54,45,89,0.3)`, dashed
- tooltip: 배경 `#150f23`, border `1px solid #362d59`, radius 8px, Rubik 12px

**모델별 분포 (가로 바):**
- 바 색상: `#6a5fc1`
- 바 배경(트랙): `rgba(255,255,255,0.06)`, radius 4px
- 모델명: Rubik 13px weight 500, `#ffffff`
- 퍼센트: Rubik 13px weight 400, `#79628c`

**일별 비용 테이블:**
- 헤더: Rubik 12px weight 600, `#e5e7eb`, uppercase, letter-spacing 0.2px
- 행: Rubik 13px weight 400, `#ffffff`
- 날짜: `#e5e7eb`, 금액: `#ffffff` weight 600
- 행 호버: `rgba(255,255,255,0.03)`

**Cost View 체크리스트:**
- [ ] 숫자 카드에서 퍼센트/금액 변화가 즉시 파악 가능
- [ ] 차트는 Recharts AreaChart 사용, 반응형 (컨테이너 폭에 맞춤)
- [ ] 모델별 바 차트는 항상 내림차순 정렬 (가장 많이 쓰는 모델이 위)
- [ ] 날짜 범위 선택 가능 (7d / 30d / 90d) — 필터 바에 배치

### 10.4 Tools View — "어떤 도구를 얼마나 쓰는가?"

> **시각 참조**: Sentry의 "Performance → Transactions" 테이블 + 차트.
> 툴 사용 빈도를 한눈에 비교 가능해야 함.

```
┌─ Tools ───────────────────────────────────────────────────┐
│                                                          │
│  Tool Usage Distribution                                 │
│  ┌──────────────────────────────────────────────────────┐│
│  │                                                      ││
│  │       terminal ████████████████████████  1,247  48%  ││
│  │      read_file ████████████████           623  24%  ││
│  │        search ██████████                  412  16%  ││
│  │     patch       ████                      189   7%  ││
│  │       write     ██                         85   3%  ││
│  │       vision    █                          42   2%  ││
│  │                                                      ││
│  └──────────────────────────────────────────────────────┘│
│                                                          │
│  Tool Calls Over Time                                    │
│  ┌──────────────────────────────────────────────────────┐│
│  │  ╱╲  ╱╲                                              ││
│  │ ╱  ╲╱  ╲  ╱╲                                        ││
│  │╱        ╲╱  ╲  ╱╲                                   ││
│  └──────────────────────────────────────────────────────┘│
└──────────────────────────────────────────────────────────┘
```

**분포 바 차트:**
- 가로 바, 전체 폭을 100%로 사용
- 바 라벨 (tool명): Monaco 13px weight 400, `#e5e7eb`, 고정 폭 100px, 우측 정렬
- 바 색상: 단일 색 `#6a5fc1` (색상으로 구분하지 않음 — 길이로만 구분)
- 바 높이: 28px, radius 4px
- 바 트랙: `rgba(255,255,255,0.06)`, radius 4px
- 카운트: Rubik 13px weight 600, `#ffffff`, 고정 폭 60px
- 퍼센트: Rubik 12px weight 400, `#79628c`, 고정 폭 40px
- 행 간격: 8px

**시계열 차트:**
- Stacked AreaChart — 툴별로 다른 색상 사용 (이 경우만 색상 구분)
- 색상 팔레트 (툴용): `#6a5fc1`, `#c2ef4e`, `#ffb287`, `#fa7faa`, `#422082`, `#79628c`
- 범례(legend): 차트 하단, Rubik 12px, 각 색상에 대응

**Tools View 체크리스트:**
- [ ] 바 길이가 실제 비율을 정확히 반영
- [ ] 툴명은 코드에서 사용하는 실제 함수명 (terminal, read_file, search_files 등)
- [ ] 카운트 클릭 시 해당 툴의 최근 사용 세션으로 이동 (필터링)

### 10.5 Overview — "전체 팀 상태는?"

> **시각 참조**: Grafana의 Home Dashboard.
> 모든 프로필을 한 화면에 비교 — PM이 한눈에 파악하기 위한 뷰.
> Profile Selector 선택과 무관하게 항상 모든 프로필 표시.

```
┌─ Overview ────────────────────────────────────────────────┐
│                                                          │
│  Team Summary                                            │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐               │
│  │ PROFILES │  │  ACTIVE  │  │TOTAL COST│               │
│  │    4     │  │    2     │  │   $8.72  │               │
│  └──────────┘  └──────────┘  └──────────┘               │
│                                                          │
│  Profile Comparison                                      │
│  ┌──────────────────────────────────────────────────────┐│
│  │ Profile    │ Sessions │ Tokens  │ Cost  │ Status     ││
│  │ ─────────  │ ──────── │ ─────── │ ───── │ ───────── ││
│  │ default    │   142    │ 285,420 │ $4.21 │ ● Alive   ││
│  │ backend    │    67    │  98,300 │ $1.89 │ ● Alive   ││
│  │ frontend   │    23    │  42,100 │ $0.82 │ ○ Stopped ││
│  │ dba        │    15    │  31,200 │ $0.61 │ ○ Stopped ││
│  └──────────────────────────────────────────────────────┘│
│                                                          │
│  Cost by Profile (7d)          Activity Heatmap (7d)     │
│  ┌─────────────────────┐  ┌─────────────────────────┐   │
│  │ ▓▓▓ default  $4.21  │  │ Mo Tu We Th Fr Sa Su   │   │
│  │ ▓▓ backend   $1.89  │  │ ██ ▓▓ ██ ░░ ░░ ░░ ░░  │ default│
│  │ ▒ frontend  $0.82  │  │ ▓▓ ▒▒ ▓▓ ░░ ░░ ░░ ░░  │ backend│
│  │ ░ dba       $0.61  │  │ ██ ░░ ██ ░░ ░░ ░░ ░░  │ frontend│
│  └─────────────────────┘  │ ▒▒ ░░ ▒▒ ░░ ░░ ░░ ░░  │ dba    │
│                           └─────────────────────────┘   │
└──────────────────────────────────────────────────────────┘
```

**팀 요약 카드:**
- 3개 카드, Status View 카드와 동일 스타일
- Profiles 카드: 현재 감지된 프로필 수
- Active 카드: gateway가 alive인 프로필 수
- Total Cost 카드: 모든 프로필 합산

**프로필 비교 테이블:**
- 배경: 카드 스타일
- 헤더: Rubik 12px weight 600, `#e5e7eb`, uppercase, letter-spacing 0.2px
- 프로필명: Rubik 14px weight 500, `#ffffff`
- 숫자 컬럼: Rubik 14px weight 600, `#ffffff`, 우측 정렬
- Status: dot 아이콘 + 텍스트 (Status View와 동일)
- 행 호버: `rgba(255,255,255,0.03)`
- 프로필명 클릭 시 해당 프로필의 Status View로 이동

**히트맵:**
- 셀 크기: 24px × 24px, gap 2px
- 색상 스케일: `#150f23` (0) → `#362d59` (low) → `#6a5fc1` (mid) → `#c2ef4e` (high)
- 요일 라벨: Rubik 11px weight 500, `#79628c`, 2글자 약어 (Mo, Tu...)
- 프로필 라벨: Rubik 12px weight 500, `#e5e7eb`
- 셀 호버: tooltip에 정확한 세션 수 표시

**Overview 체크리스트:**
- [ ] 항상 모든 프로필을 표시 (Profile Selector 무관)
- [ ] 테이블 행 클릭으로 해당 프로필 상세 뷰 이동
- [ ] 히트맵 색상 스케일이 직관적 (초록=활동 많음, 어두움=활동 없음)

---

## 11. Agent Prompt Guide

> **핵심 원칙**: 에이전트에게 "무엇을 만들지"만 말하지 마세요.
> "어떻게 보여야 하는지"까지 구체적으로 지시해야 합니다.
> 제약이 타이트할수록 출력 품질이 높아집니다.
> — Emanuele Di Pietro, "Prompt Engineering for Exceptional UI"

### 11.1 프롬프트 작성 원칙

1. **레이아웃부터 명시** — "사이드바 240px + 메인 컨텐츠"처럼 구조를 먼저 정의
2. **폰트를 명확히** — "Rubik 14px weight 500"처럼 가족/크기/굵기를 모두 지정
3. **색상을 HEX로** — "보라색"이 아니라 "#6a5fc1"로
4. **간격을 px로** — "약간의 간격"이 아니라 "gap 16px, padding 20px"
5. **Do/Don't를 쌍으로** — "둥근 모서리 쓰세요"보다 "radius 최소 6px, 0px 금지"가 명확
6. **시각 참조 제공** — "Sentry Issues 화면처럼"처럼 실제 존재하는 UI를 벤치마크로 지정
7. **뷰별 체크리스트 포함** — 완료 기준을 명시하면 에이전트가 자가 검증 가능

### 11.2 Quick Color Reference

- Background: `#1f1633` (primary), `#150f23` (deeper)
- Text: `#ffffff` (primary), `#e5e7eb` (secondary)
- Muted text: `#79628c` (tertiary), `#584674` (quaternary)
- Interactive: `#6a5fc1` (links/hover), `#79628c` (buttons)
- Accent: `#c2ef4e` (lime highlight), `#ffb287` (coral focus)
- Status: `#c2ef4e` (positive/alive), `#fa7faa` (negative/error)
- Border: `#362d59` (dark), `rgba(54,45,89,0.5)` (subtle)
- Card surface: `rgba(255,255,255,0.04)`, glass: `rgba(255,255,255,0.18)`

### 11.3 View별 프롬프트 템플릿

**Status View:**
> "Build the Status view for a monitoring dashboard. Layout: 4 summary cards in a `1fr 1fr 1fr 1fr` grid (gap 16px) at top, followed by a recent sessions list below. Card style: background rgba(255,255,255,0.04), border 1px solid #362d59, radius 12px, padding 20px. Card label: Rubik 12px weight 600, #e5e7eb, uppercase, letter-spacing 0.25px. Card value: Rubik 28px weight 700, #ffffff. Gateway alive indicator: #c2ef4e dot 8px, stopped: #fa7faa. Session list rows: padding 12px 16px, border-bottom 1px solid rgba(54,45,89,0.5). Status badges: In Progress gets rgba(194,239,78,0.15) bg with #c2ef4e text, Done gets rgba(106,95,193,0.15) bg with #6a5fc1 text. Reference: Sentry Project Issues page layout."

**Activity View:**
> "Build the Activity view — a real-time event stream. Use Monaco 13px monospace font for all rows (this should feel like reading terminal logs, not a regular UI). Each row: 32px height, padding 0 16px, columns: timestamp (#79628c, 70px fixed), role (#e5e7eb, 50px), content. Tool events: tool name in #c2ef4e, args in #584674, prefix with → icon. Message events: white text, max 3 lines with truncate. Auto-scroll to top on new events, pause if user scrolls up. Reference: Sentry Stream view."

**Cost View:**
> "Build the Cost view. Top: 3 summary cards (total tokens, estimated cost, cache hit rate) in 1fr grid, gap 16px. Main numbers: Rubik 32px weight 700, white. Trend arrows: Rubik 13px, increase in #fa7faa (warning), decrease in #c2ef4e (positive). Middle: Area chart for token usage over time, line color #6a5fc1, fill rgba(106,95,193,0.1), grid lines rgba(54,45,89,0.3) dashed, tooltip bg #150f23 border #362d59. Bottom: two-column layout — left is horizontal bar chart for model distribution (bar color #6a5fc1, track rgba(255,255,255,0.06), radius 4px), right is daily cost table. Date range selector: 7d / 30d / 90d toggle buttons. Reference: Vercel Usage page."

**Tools View:**
> "Build the Tools view — tool usage distribution. Full-width horizontal bar chart. Tool names: Monaco 13px, #e5e7eb, right-aligned, 100px fixed width. Bars: single color #6a5fc1, height 28px, radius 4px, track rgba(255,255,255,0.06). Count: Rubik 13px weight 600, #ffffff, 60px. Percentage: Rubik 12px, #79628c, 40px. Below chart: stacked area chart for tool calls over time, use palette [#6a5fc1, #c2ef4e, #ffb287, #fa7faa, #422082, #79628c]. Bars always sorted descending by count. Reference: Sentry Performance Transactions table."

**Overview:**
> "Build the Overview (cross-profile) view. Always shows ALL profiles regardless of selector. Top: 3 team summary cards (profiles count, active count, total cost). Middle: comparison table with columns: Profile (Rubik 14px weight 500), Sessions, Tokens, Cost (right-aligned, weight 600), Status (dot + text). Row hover: rgba(255,255,255,0.03). Profile name clickable → navigates to that profile's Status view. Bottom: two-column — left is horizontal bar chart for cost by profile, right is activity heatmap. Heatmap cells: 24×24px, gap 2px, color scale #150f23→#362d59→#6a5fc1→#c2ef4e. Day labels: 2-char abbreviations (Mo Tu...). Reference: Grafana Home Dashboard."

### 11.4 Iteration Guide

1. 항상 `#1f1633` 배경에서 시작 — 이 팔레트는 다크 모드용
2. Status 카드 → 리스트 → 차트 순서로 구성 (위에서 아래로 정보 밀도 증가)
3. 숫자가 주인공인 뷰(Cost, Tools)에서는 숫자를 크게, 라벨을 작게
4. Activity View만 Monaco(mono) 사용 — 나머지 모든 뷰는 Rubik
5. `#c2ef4e`는 한 뷰에서 한 곳만 (상태 인디케이터 또는 강조 포인트)
6. Frosted glass(`blur(18px) saturate(180%)`)는 sidebar overlay나 모달에만, 일반 카드에는 사용 금지
7. 모든 카드/컨테이너는 `border 1px solid #362d59` + `radius 12px`로 통일
8. 뷰별 체크리스트를 완료 기준으로 삼고, 체크리스트를 먼저 읽고 구현 시작

### 11.5 뷰별 Do/Don't

**공통 Do:**
- 카드 배경은 항상 `rgba(255,255,255,0.04)` — 더 밝은 glass 효과는 sidebar/modal에만
- 보더는 항상 `#362d59` — 회색 보더 금지
- 호버 효과는 항상 미세하게 (`rgba(255,255,255,0.03)` ~ `0.06`)
- 숫자에 콤마 구분 (1,247 not 1247)

**공통 Don't:**
- 모니터링 대시보드에 Dammit Sans 사용 금지 (이 폰트는 마케팅 전용)
- 숫자/데이터가 없는 빈 화면에 skeleton UI 대신 "No data" 메시지 표시 (`#79628c`)
- 차트에 3D 효과나 그라디언트 채우기 (flat 2D만)
- 강조색(#c2ef4e, #fa7faa)를 같은 컴포넌트 내에서 혼용

**Status View:**
- Do: 상태를 색상 + 텍스트 둘 다로 표시 (색맹 접근성)
- Don't: 카드 안에 차트 넣기 (카드 = 단일 숫자)

**Activity View:**
- Do: Monaco 폰트로 터미널 느낌 유지
- Don't: 행 간 높이를 32px 이상으로 늘리기 (밀도가 핵심)

**Cost View:**
- Do: 숫자를 가장 크고 강조 (32px weight 700)
- Don't: 차트를 요약 카드 위에 배치 (숫자가 먼저 읽혀야 함)

**Tools View:**
- Do: 단일 색 바로 정확한 비율 비교 가능하게
- Don't: 툴마다 다른 색상 사용 (길이만으로 구분)

**Overview:**
- Do: 항상 모든 프로필 표시
- Don't: 프로필 선택기의 선택에 따라 내용이 바뀌게 만들기
