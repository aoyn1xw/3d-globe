# 🌍 Interactive 3D Globe

A beautiful, interactive 3D globe component built with React, Next.js, and HTML5 Canvas. Features smooth animations, draggable rotation, and customizable global network visualizations.

![Demo](https://img.shields.io/badge/demo-live-brightgreen) ![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue) ![Next.js](https://img.shields.io/badge/Next.js-14-black) ![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8)

## ✨ Features

- 🎨 **Fully Customizable** - Colors, sizes, markers, and connections
- 🖱️ **Interactive** - Drag to rotate the globe
- ⚡ **Performant** - Smooth 60fps animations using Canvas API
- 🎯 **TypeScript** - Full type safety
- 🌙 **Dark Mode** - Built-in dark theme support
- 📱 **Responsive** - Adapts to any screen size
- 🎭 **Animated Arcs** - Flowing connections between locations
- 💫 **Pulsing Markers** - Eye-catching location indicators

## 🚀 Quick Start

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the globe in action.

### Build

```bash
npm run build
npm start
```

## 📦 Tech Stack

- **Framework:** Next.js 14 (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS + shadcn/ui
- **Rendering:** HTML5 Canvas API
- **Theme:** next-themes

## 🎮 Usage

### Basic Usage

```tsx
import { Component as Globe } from "@/components/ui/interactive-globe";

export default function Page() {
  return <Globe size={600} />;
}
```

### Custom Configuration

```tsx
import { Component as Globe } from "@/components/ui/interactive-globe";

export default function Page() {
  const markers = [
    { lat: 40.7128, lng: -74.0060, label: "New York" },
    { lat: 51.5074, lng: -0.1278, label: "London" },
    { lat: 35.6762, lng: 139.6503, label: "Tokyo" },
  ];

  const connections = [
    { from: [40.7128, -74.0060], to: [51.5074, -0.1278] },
    { from: [51.5074, -0.1278], to: [35.6762, 139.6503] },
  ];

  return (
    <Globe 
      size={600}
      markers={markers}
      connections={connections}
      dotColor="rgba(150, 100, 255, ALPHA)"
      arcColor="rgba(150, 100, 255, 0.5)"
      markerColor="rgba(200, 100, 255, 1)"
      autoRotateSpeed={0.003}
    />
  );
}
```

## ⚙️ Component Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `className` | `string` | `undefined` | Additional CSS classes |
| `size` | `number` | `600` | Globe size in pixels |
| `dotColor` | `string` | `"rgba(100, 180, 255, ALPHA)"` | Color of globe dots (ALPHA is replaced dynamically) |
| `arcColor` | `string` | `"rgba(100, 180, 255, 0.5)"` | Color of connection arcs |
| `markerColor` | `string` | `"rgba(100, 220, 255, 1)"` | Color of location markers |
| `autoRotateSpeed` | `number` | `0.002` | Auto-rotation speed |
| `connections` | `Array` | See default | Array of `{from: [lat, lng], to: [lat, lng]}` |
| `markers` | `Array` | See default | Array of `{lat, lng, label?}` |

## 🏗️ Project Structure

```
3d-globe/
├── app/
│   ├── layout.tsx         # Root layout with theme provider
│   ├── page.tsx           # Demo page
│   └── globals.css        # Global styles
├── components/
│   ├── ui/
│   │   └── interactive-globe.tsx  # Main globe component
│   └── theme-provider.tsx         # Dark mode provider
├── lib/
│   └── utils.ts           # Utility functions
└── ...config files
```

## 🎨 Customization

### Change Theme Colors

Edit the CSS variables in `app/globals.css`:

```css
.dark {
  --background: 222.2 84% 4.9%;
  --foreground: 210 40% 98%;
  /* ... more variables */
}
```

### Add More shadcn Components

```bash
npx shadcn-ui@latest add button
npx shadcn-ui@latest add card
```

## 🤝 Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- UI components from [shadcn/ui](https://ui.shadcn.com/)

---

Made with ❤️ using React and Canvas
