# Create comprehensive README.md
readme = '''# 🔒 KSP Crime Intelligence Copilot

[![CI/CD](https://github.com/karnataka-police/ksp-crime-intelligence-copilot/actions/workflows/ci-cd.yml/badge.svg)](https://github.com/karnataka-police/ksp-crime-intelligence-copilot/actions/workflows/ci-cd.yml)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.4-blue.svg)](https://www.typescriptlang.org/)
[![React](https://img.shields.io/badge/React-18.3-61DAFB.svg)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Vite-5.3-646CFF.svg)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38B2AC.svg)](https://tailwindcss.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **GeoShield · Conversational Crime Intelligence Dashboard**
>
> An AI-powered investigative interface for the Karnataka State Police (KSP) that enables natural language querying of crime records, visualizes criminal network relationships, and identifies geographic crime hotspots.

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Database Schema](#-database-schema)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

### 💬 Conversational AI Chat
- **Bilingual Support**: Query in English or Kannada (ಕನ್ನಡ)
- **Contextual Memory**: AI remembers previous questions about suspects
- **Source Attribution**: Every response includes verifiable source records
- **Quick Prompts**: One-click common investigative queries

### 🕸️ Criminal Network Analysis
- **Relationship Mapping**: Visualize connections between accused persons
- **Cluster Detection**: Automatic identification of repeat offender networks
- **Interactive SVG Graph**: Click nodes to view detailed profiles
- **Pulse Animation**: Flagged suspects have animated indicators

### 🔥 Crime Hotspot Visualization
- **Density Heat Map**: 7×10 grid showing incident concentration
- **Trend Analysis**: 6-month case volume line chart
- **Sector Alerts**: Automatic hotspot cluster identification
- **Responsive Charts**: Built with Recharts for smooth interactions

---

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Framework** | React 18.3 + TypeScript 5.4 |
| **Build Tool** | Vite 5.3 |
| **Styling** | Tailwind CSS 3.4 |
| **Charts** | Recharts 2.12 |
| **Icons** | Lucide React |
| **Linting** | ESLint + Prettier |
| **Testing** | Vitest |
| **CI/CD** | GitHub Actions |
| **Deployment** | GitHub Pages |

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** ≥ 18.0.0
- **npm** ≥ 9.0.0

### Installation

```bash
# Clone the repository
git clone https://github.com/karnataka-police/ksp-crime-intelligence-copilot.git
cd ksp-crime-intelligence-copilot

# Install dependencies
npm ci

# Start development server
npm run dev
```

The application will be available at `http://localhost:3000`

### Build for Production

```bash
npm run build
```

Output will be in the `dist/` directory.

---

## 📁 Project Structure

```
ksp-crime-intelligence-copilot/
├── .github/
│   ├── workflows/
│   │   └── ci-cd.yml          # CI/CD pipeline
│   └── dependabot.yml         # Dependency updates
├── docs/
│   └── ER-Diagram.md          # Database schema documentation
├── public/
│   └── shield-check.svg       # Favicon
├── scripts/
│   └── verify-build.sh        # Pre-deployment verification
├── src/
│   ├── components/
│   │   ├── Bubble.tsx         # Chat message bubble
│   │   ├── CaseRow.tsx        # Case record row
│   │   ├── ChatPanel.tsx      # Chat interface
│   │   ├── HotspotPanel.tsx   # Heat map & trends
│   │   ├── NetworkPanel.tsx   # Criminal network graph
│   │   ├── SourceChip.tsx     # Expandable source attribution
│   │   └── TypingDots.tsx     # AI typing indicator
│   ├── data/
│   │   └── cases.ts           # Synthetic demo data
│   ├── styles/
│   │   └── index.css          # Global styles + Tailwind
│   ├── utils/
│   │   ├── constants.ts       # Design tokens
│   │   └── types.ts           # TypeScript interfaces
│   ├── App.tsx                # Main application
│   ├── main.tsx               # Entry point
│   └── vite-env.d.ts          # Vite type declarations
├── .eslintrc.cjs              # ESLint configuration
├── .prettierrc                # Prettier configuration
├── index.html                 # HTML entry point
├── package.json               # Dependencies & scripts
├── postcss.config.js          # PostCSS configuration
├── tailwind.config.js         # Tailwind theme customization
├── tsconfig.json              # TypeScript configuration
├── tsconfig.node.json         # Vite TS config
└── vite.config.ts             # Vite build configuration
```

---

## 🗄️ Database Schema

This application interfaces with the **Karnataka Police FIR System** database. The ER diagram is documented in [`docs/ER-Diagram.md`](docs/ER-Diagram.md).

### Core Tables

| Table | Description |
|-------|-------------|
| `CaseMaster` | Primary FIR/case records |
| `Accused` | Accused person details |
| `Victim` | Victim information |
| `ComplainantDetails` | Complainant records |
| `ActSectionAssociation` | Legal act & section mappings |
| `ArrestSurrender` | Arrest and surrender events |
| `Employee` | Police personnel records |
| `Unit` | Police station/unit hierarchy |

### Key Relationships

- **One-to-Many**: One FIR → Multiple accused, victims, complainants
- **Many-to-One**: Multiple FIRs → Same police station, court, crime head
- **Junction Table**: `inv_arrestsurrenderaccused` links arrests to multiple accused

---

## 🚀 Deployment

### Automatic Deployment

Every push to `main` branch triggers:
1. **Lint & Type Check** — ESLint + TypeScript validation
2. **Unit Tests** — Vitest with coverage reporting
3. **Production Build** — Optimized Vite build
4. **GitHub Pages Deploy** — Automatic deployment

### Manual Deployment

```bash
# Build and preview locally
npm run build
npm run preview

# Deploy to GitHub Pages (requires setup)
npm run deploy
```

### Environment Requirements

| Environment | Node Version | Status |
|-------------|-------------|--------|
| Development | 18.x / 20.x | ✅ Supported |
| Production | 20.x LTS | ✅ Recommended |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'feat: add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation
- `style:` Formatting
- `refactor:` Code restructuring
- `test:` Tests
- `chore:` Maintenance

---

## 📄 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

> ⚠️ **Confidential**: This application contains sensitive law enforcement interfaces. Unauthorized access is prohibited.

---

<div align="center">
  <sub>Built with 🔒 for the Karnataka State Police Department</sub>
</div>
'''

with open(f"{base_dir}/README.md", "w") as f:
    f.write(readme)

print("✅ README.md created")
