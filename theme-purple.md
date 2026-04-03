# VibeLive Design Guide (Standard)

**Theme / Brand color:** Purple  
**Primary accent:** `#6E6282`  
**Style:** calm, thoughtful, creator-centric  
**Default radius:** `16px`  
**Max content width:** `980px`  
**Font stack:** `ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial`

**Version:** 1.0.0  
**Last Updated (PST):** 2026-01-27 15:10 PST

---

## 1) Core Principles

1. **Neutral first, accent second** – most UI remains soft and light; purple signals intent.
2. **One primary action per screen** – avoid visual competition.
3. **Calm hierarchy** – strong headings, gentle body text, quiet metadata.
4. **Presence over urgency** – this palette is reflective, not loud.

---

## 2) Essential Color Tokens (Purple Theme)

### Surfaces

| Token | Hex | Usage |
|------|-----|------|
| `--bg` | `#F5FAFC` | Main page background |
| `--card` | `#FFFFFF` | Cards, panels, modals |
| `--soft` | `#F7F5FA` | Hover surfaces, subtle sections |
| `--border` | `#E0E8F0` | Default borders |
| `--borderSoft` | `#DBE2EA` | Hover / emphasis borders |

---

### Text

| Token | Hex | Usage |
|------|-----|------|
| `--text` | `#1E293B` | Primary text |
| `--muted` | `#607088` | Secondary text |
| `--muted2` | `#9CA3AF` | Tertiary / helper text |

---

### Brand Accent (Primary)

| Token | Value | Usage |
|------|------|------|
| `--accent` | `#6E6282` | Primary buttons, links, highlights |
| `--accentHover` | `#585070` | Hover / active state |
| `--accentSoft` | `rgba(110,98,130,.12)` | Selected / highlight background |
| `--accentBorder` | `rgba(110,98,130,.30)` | Focus ring / outline |

---

### Status Colors (Semantic)

**Live / Online / Enabled**  
(Use sparingly; semantic only)

| Token | Hex |
|------|-----|
| `--liveBg` | `#E8F4ED` |
| `--liveBorder` | `#A6C5A3` |
| `--liveText` | `#324252` |

**Disabled / Inactive**

| Token | Hex |
|------|-----|
| `--disabledBg` | `#F3F4F6` |
| `--disabledBorder` | `#E5E7EB` |
| `--disabledText` | `#6B7280` |

---

## 3) Component Rules

### Buttons

**Primary (CTA)**
- Background: `--accent`
- Text: `#FFFFFF`
- Hover: `--accentHover`
- Use for: Join Room, Create Room, Confirm

**Secondary**
- Background: `--soft`
- Text: `--text`
- Border: `--border`

**Danger (Rare)**
- Background: `#FEF2F2`
- Border: `#FCA5A5`
- Text: `#B91C1C`

---

### Links
- Default: `--accent`
- Hover: underline only

### Inputs
- Background: `--card`
- Border: `--border`
- Focus ring: `--accentBorder`
- Error state: use Danger colors

### Cards
- Background: `--card`
- Border: `1px solid --border`
- Hover: subtle shadow or `--borderSoft`

### Pills / Badges

| Type | Colors |
|----|----|
| Live | `--liveBg / --liveBorder / --liveText` |
| Primary | `--accentSoft` bg + `--accent` text |
| Disabled | `--disabledBg / --disabledBorder / --disabledText` |

---

## 4) Modals, Toasts, Alerts

**Overlay:** `rgba(30, 41, 59, 0.5)`  
**Container:** `--card` with `--border`, radius `16px`

### Alert Types
- **Success / Live:** use Live palette
- **Error:** use Danger palette
- **Info:** `--soft` background + `--text`

---

## 5) Iconography

- No emojis
- Stroke-based SVG icons (Lucide / Heroicons style)
- Sizes: 20px / 24px
- Color: `currentColor`
- Active: `--accent`
- Muted: `--muted`

---

## 6) CSS Variables (Copy-Paste)

```css
:root{
  --radius: 16px;
  --max: 980px;
  --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;

  --bg: #F5FAFC;
  --card: #FFFFFF;
  --soft: #F7F5FA;
  --border: #E0E8F0;
  --borderSoft: #DBE2EA;

  --text: #1E293B;
  --muted: #607088;
  --muted2: #9CA3AF;

  --accent: #6E6282;
  --accentHover: #585070;
  --accentSoft: rgba(110,98,130,.12);
  --accentBorder: rgba(110,98,130,.30);

  --liveBg: #E8F4ED;
  --liveBorder: #A6C5A3;
  --liveText: #324252;

  --disabledBg: #F3F4F6;
  --disabledBorder: #E5E7EB;
  --disabledText: #6B7280;

  --overlay: rgba(30, 41, 59, 0.5);
}
```

---

## 7) Do / Don’t

**Do**
- Use purple for intent and emphasis.
- Keep most surfaces neutral and bright.
- Maintain generous whitespace.

**Don’t**
- Use purple for error states.
- Introduce additional accent colors casually.
- Stack multiple primary CTAs on one screen.

---

**Summary**  
This purple theme is best for creator tools, reflective conversations, coaching, learning, and personal-brand driven VibeLive apps.