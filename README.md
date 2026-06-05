# Bundus DNA Exploration Platform

A unified, comprehensive DNA exploration and genetic insights platform combining multiple specialized applications into one cohesive ecosystem.

## 🧬 Project Overview

This consolidated repository brings together six complementary DNA/genetic analysis applications:

- **DNA Deep Dive** - Advanced genetic analysis and visualization
- **DNA App Site** - Integrated DNA application suite
- **Bundus Genetic Insights** - Genetic trait analysis and health markers
- **Bundus with Hidden Insights** - Privacy-focused genetic exploration
- **Bundus Genetical Insight** - User-friendly DNA exploration platform
- **Merger** - Master integration and coordination layer

## 📁 Repository Structure

```
bundus-dna-platform/
├── apps/
│   ├── dna-deep-dive/              # Advanced DNA analysis engine
│   ├── dna-app-site/               # Main application interface
│   ├── bundus-genetic-insights/    # Genetic trait deep-dive analysis
│   ├── bundus-hidden-insights/     # Privacy-focused exploration
│   └── bundus-genetical-insight/   # User-friendly entry point
├── shared/
│   ├── design-system/              # Unified design guidelines & components
│   ├── design_guidelines.json       # Master design specification
│   ├── config/                     # Shared configuration
│   └── utils/                      # Common utilities
├── backend/                         # Centralized backend services
├── frontend/                        # Shared frontend infrastructure
├── tests/                           # Integration and E2E tests
├── docs/                            # Documentation
└── README.md
```

## 🎨 Design System

This project implements a **Dark Mode Bio-Tech Swiss Design** aesthetic with two complementary palettes:

### Primary Design (dna-deep-dive)
- **Archetype**: Swiss & High-Contrast / Modern Lab Instrument
- **Primary Color**: Amber (#F59E0B)
- **Accent Colors**: Crimson (#E11D48), Tertiary (#FCD34D)
- **Background**: #050505 (ultra-dark)
- **Typography**: Chivo (headings), IBM Plex Sans (body), IBM Plex Mono (data)

### Alternative Design (bundus-genetic-insights)
- **Archetype**: Swiss & High-Contrast / Dark Mode Bio-Tech
- **Primary Color**: Blue (#3366FF)
- **Accent Colors**: Green (#00E676), Warning (#FFC400), Alert (#FF2A55)
- **Background**: #0A0A0C (deep navy-black)
- **Typography**: Cabinet Grotesk (headings), IBM Plex Sans (body), IBM Plex Mono (data)

### Shared Principles
- Dense, functional grid layouts
- Minimal UI chrome for maximum data visibility
- High contrast for accessibility
- Monospace fonts for genomic coordinates and data
- No glassmorphism for dashboards
- Sharp borders (1px or less)

## 🚀 Getting Started

### Prerequisites
- Node.js 16+ / Python 3.8+
- npm or yarn
- Git

### Installation

```bash
# Clone the repository
git clone https://github.com/SMuculj9/Merger.git
cd bundus-dna-platform

# Install dependencies
npm install

# or for Python backend
pip install -r requirements.txt
```

### Development

```bash
# Start development servers
npm run dev

# Run tests
npm run test

# Build for production
npm run build
```

## 📊 Technology Stack

### Frontend
- **React** - UI framework
- **TypeScript** - Type safety
- **Tailwind CSS** - Styling
- **D3.js** - Advanced visualizations (Chromosome Ideogram)
- **react-globe.gl** - Geographic visualization
- **Recharts** - Data charts
- **Phosphor/Lucide Icons** - Icon library

### Backend
- **Node.js / Express** or **Python / Django/FastAPI**
- RESTful API design
- Genetic data processing
- User authentication & authorization

### Testing
- **Jest** - Unit testing
- **Cypress/Playwright** - E2E testing
- **React Testing Library** - Component testing

## 📋 Key Features

### 1. DNA Analysis Engine
- Chromosome visualization
- Variant calling and annotation
- Ancestry mapping
- Haplogroup migration tracking

### 2. Trait Deep Dives
- Longevity markers (FOXO3, etc.)
- Mind & Temperament analysis (COMT variants)
- Caffeine metabolism prediction
- Cellular repair indicators

### 3. DNA Explorer
- Terminal-style data table
- RSID / Chromosome / Position / Genotype columns
- Impact assessment
- Large dataset handling

### 4. User Interface
- Glassmorphism auth cards
- Bento grid dashboard
- "Bundus Assistant" AI summary panel
- Smooth data visualizations

### 5. Security & Privacy
- Encrypted data storage
- User authentication
- HIPAA-compliant architecture
- Privacy-focused data handling

## 🧪 Testing

All interactive elements must include kebab-case `data-testid` attributes for testing:

```jsx
<button data-testid="upload-dna-button">Upload DNA</button>
<input data-testid="trait-search-input" />
<div data-testid="chromosome-ideogram" />
```

## 📖 Documentation

- [Design Guidelines](./shared/design-system/DESIGN_GUIDELINES.md)
- [API Documentation](./docs/API.md)
- [Contributing Guidelines](./CONTRIBUTING.md)
- [Testing Guide](./docs/TESTING.md)

## 🔗 Component Library

### Shared Components
- **DataTable** - Dense, high-performance table component
- **ChartPanel** - Recharts wrapper with dark mode
- **GeneticVisualization** - D3 chromosome renderer
- **AuthCard** - Glassmorphism authentication
- **BundusAssistant** - AI summary panel

## 📝 License

[Your License Here]

## 👤 Author

**SMuculj9** - DNA Platform Developer

## 🤝 Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

## 📞 Support

For issues, feature requests, or questions:
- Open a GitHub issue
- Contact: [your-email@example.com]

---

**Version**: 1.0.0 (Consolidated)  
**Last Updated**: June 5, 2026
