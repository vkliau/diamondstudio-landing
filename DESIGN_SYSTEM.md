# Octopus Game - Design System Export

**Export Date:** December 19, 2025  
**Use for:** Landing page and future Diamond Studio projects

---

## 🎨 Color Palette

### Primary Background
- **Main BG:** `#0f172a` (slate-900)
- **Card BG:** `#1e293b` (slate-800) with 50-80% opacity
- **Overlay BG:** `bg-slate-800/50` + `backdrop-blur-lg`

### Accent Colors
- **Primary Accent (Cyan):** `#06b6d4` (cyan-500) to `#0891b2` (cyan-600)
- **Secondary Accent (Purple):** `#a855f7` (purple-500) to `#7c3aed` (purple-600)
- **Gradient Text:** `from-cyan-400 to-purple-400`
- **Success:** `#22c55e` (green-500)
- **Error/Warning:** `#ef4444` (red-500)
- **Caution:** `#eab308` (yellow-500)

### Text Colors
- **Primary Text:** `#e2e8f0` (slate-200) / `#ffffff` (white)
- **Secondary Text:** `#94a3b8` (slate-400)
- **Muted Text:** `#64748b` (slate-500)
- **Mono/Code:** `#475569` (slate-600) for labels

### Borders
- **Default Border:** `#334155` (slate-700)
- **Focus Border:** `#06b6d4` (cyan-500)
- **Accent Borders:** Various opacity variants (e.g., `border-yellow-500/30`)

### Tier Colors
- **POSEIDON:** `bg-yellow-500/20 text-yellow-400 border-yellow-500/50` 👑
- **KRAKEN:** `bg-red-500/20 text-red-400 border-red-500/50` 🔱
- **TENTACLE:** `bg-purple-500/20 text-purple-400 border-purple-500/50` 🐙
- **INKLING:** `bg-slate-700 text-slate-400` 🦑
- **PLANKTON:** Default slate 🦠

---

## 🔤 Typography

### Fonts
```html
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
```

- **Primary Font:** `'Inter', sans-serif` (body, headings, UI)
- **Monospace Font:** `'Space Mono', monospace` (stats, code, labels)

### Text Styles
- **Hero Title:** `text-4xl font-black uppercase tracking-tighter`
- **Section Headers:** `text-2xl font-black uppercase`
- **Labels:** `text-xs font-bold uppercase tracking-wider text-slate-500`
- **Body:** `text-sm text-slate-400`
- **Mono Stats:** `font-mono text-xs text-slate-500`

### Gradient Text
```css
bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent
```

---

## 🎭 UI Components

### Buttons

**Primary CTA (Cyan):**
```tsx
className="w-full bg-gradient-to-r from-cyan-600 to-cyan-500 hover:from-cyan-500 hover:to-cyan-400 text-white font-bold py-4 rounded-xl shadow-lg shadow-cyan-900/20 transform transition-all hover:scale-[1.02] active:scale-[0.98] flex items-center justify-center gap-2"
```

**Secondary (Outlined):**
```tsx
className="w-full bg-transparent border border-slate-700 hover:bg-slate-800 text-slate-400 hover:text-white font-bold py-3 rounded-xl transition-all flex items-center justify-center gap-2"
```

**Danger (Red/Reset):**
```tsx
className="w-full bg-transparent border border-red-900/30 hover:bg-red-900/20 text-red-900 hover:text-red-500 font-bold py-3 rounded-xl transition-all opacity-60 hover:opacity-100"
```

### Cards

**Main Card:**
```tsx
className="bg-slate-800/50 backdrop-blur-lg p-8 rounded-3xl shadow-2xl border border-slate-700"
```

**Stat Card:**
```tsx
className="p-4 bg-slate-900/50 rounded-2xl border border-slate-700"
```

**Top Accent Bar:**
```tsx
className="absolute top-0 left-0 w-full h-1 bg-gradient-to-r from-cyan-500 to-purple-500"
```

### Input Fields

```tsx
className="w-full bg-slate-900/80 border border-slate-600 rounded-xl px-4 py-3 text-white placeholder-slate-600 focus:outline-none focus:border-cyan-500 transition-colors"
```

### Badges/Pills

**Tier Badge:**
```tsx
className="px-2 py-1 rounded text-[10px] font-bold uppercase tracking-wider bg-purple-500/20 text-purple-400 border border-purple-500/50"
```

**Stat Badge:**
```tsx
className="inline-block px-2 py-1 bg-slate-800 rounded text-xs font-mono text-slate-300"
```

---

## ✨ Effects & Animations

### Background Blobs
```tsx
<div className="absolute top-[-10%] left-[-10%] w-[50%] h-[50%] bg-purple-900/20 rounded-full blur-3xl"></div>
<div className="absolute bottom-[-10%] right-[-10%] w-[50%] h-[50%] bg-cyan-900/20 rounded-full blur-3xl"></div>
```

### Entrance Animation
```tsx
className="animate-in fade-in zoom-in duration-500"
```

### Custom Pulse (Octopus)
```css
@keyframes pulse-ring {
  0% { transform: scale(0.8); opacity: 0.5; }
  100% { transform: scale(2.2); opacity: 0; }
}
.animate-pulse-ring {
  animation: pulse-ring 3s cubic-bezier(0.215, 0.61, 0.355, 1) infinite;
}
```

### Hover Transforms
- **Scale up:** `hover:scale-[1.02]`
- **Active press:** `active:scale-[0.98]`
- **Rotate icon:** `group-hover:-rotate-90 transition-transform`

### Backdrop Blur
```tsx
backdrop-blur-lg
```

---

## 🧩 Layout Patterns

### Centered Full-Screen
```tsx
<div className="min-h-screen bg-slate-900 flex flex-col items-center justify-center p-4 relative overflow-hidden">
```

### Max-Width Container
```tsx
<div className="max-w-md w-full space-y-8">
  {/* or */}
  <div className="w-full max-w-2xl">
```

### Grid (2 columns)
```tsx
<div className="grid grid-cols-2 gap-4">
```

---

## 🖼️ Branding

### Logo
- **Image:** `/octopus-logo.png?v=3`
- **Size:** `w-32 h-32`
- **Animation:** `animate-bounce-slow`

### App Name
```tsx
<h1 className="text-4xl font-black text-center mb-2 bg-gradient-to-r from-cyan-400 to-purple-400 bg-clip-text text-transparent tracking-tighter uppercase">
  Octopus
</h1>
```

### Tagline
```tsx
<p className="text-center text-slate-400 mb-8 font-mono text-sm">
  AI vs Human Audio Challenge
</p>
```

---

## 🎯 Icons

**Library:** `lucide-react`

Common icons used:
- `Play`, `Pause`, `FastForward` - Playback
- `Trophy`, `Medal`, `Target` - Achievement
- `User`, `Cpu` - Source type
- `TrendingUp`, `Activity` - Stats
- `CheckCircle`, `XCircle` - Feedback
- `RotateCcw` - Replay
- `ArrowLeft`, `ArrowRight` - Navigation
- `Eraser`, `AlertTriangle` - Actions/Warnings
- `Fish` - Tier progress

**Icon sizes:**
- Small: `w-3 h-3` or `w-4 h-4`
- Medium: `w-5 h-5`
- Large: `w-6 h-6` or `w-8 h-8`

---

## 📱 Responsive Patterns

### Table Columns (Hide on Mobile)
```tsx
className="hidden md:table-cell"  // Desktop only
className="hidden sm:table-cell"  // Tablet & up
```

### Text Truncation
```tsx
max-w-xs mx-auto
```

---

## 🎨 Copy to Landing Page

### Minimal Landing Page Starter
Use this for the new Diamond Studio landing page:

**Colors to keep:**
- Background: `bg-slate-900`
- Cards: `bg-slate-800/50 backdrop-blur-lg border border-slate-700`
- Primary CTA: Cyan gradient buttons
- Text gradients: `from-cyan-400 to-purple-400`

**Typography:**
- Hero: `Inter` font-black, uppercase, tracking-tighter
- Body: `Inter` regular
- Mono: `Space Mono` for stats/labels

**Effects:**
- Background blobs (purple & cyan)
- Backdrop blur on cards
- Hover scale transforms
- Entrance fade-in animations

---

## 📋 Quick Copy-Paste Snippets

### Tailwind CDN Setup
```html
<script src="https://cdn.tailwindcss.com"></script>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:ital,wght@0,400;0,700;1,400&family=Inter:wght@400;600;800&display=swap" rel="stylesheet">
```

### Base Body Style
```css
body {
  font-family: 'Inter', sans-serif;
  background-color: #0f172a;
  color: #e2e8f0;
}
.font-mono {
  font-family: 'Space Mono', monospace;
}
```

---

**End of Design System Export**
