# Repository Consolidation Manifest

## Source Repositories

This consolidated repository integrates content from the following 6 source repositories:

### 1. dna-deep-dive
- **ID**: 1246204527
- **Language Composition**: JavaScript (68.5%), Python (26.8%), HTML (3.5%), CSS (1.2%)
- **Default Branch**: main
- **Key Content**: Design guidelines (Lab Instrument aesthetic), test results, design system
- **Status**: Private

### 2. DNA-app-site
- **ID**: 1246215736
- **Description**: Merger
- **Language Composition**: Python (68.2%), JavaScript (30.2%), CSS (1.2%), HTML (0.4%)
- **Default Branch**: main
- **Key Content**: Integrated DNA applications, merged projects structure
- **Status**: Public

### 3. bundus-with-your-hidden-insights
- **ID**: 1259921330
- **Language Composition**: JavaScript (66%), Python (31.1%), CSS (2.4%), HTML (0.5%)
- **Default Branch**: main
- **Key Content**: Design guidelines (Bio-Tech variant), privacy-focused features
- **Status**: Private

### 4. Bundus-Genetical-Insight
- **ID**: 1248140089
- **Description**: A user friendly, cost effective DNA exploration sites for everything
- **Default Branch**: main
- **Status**: Private (minimal content)

### 5. Merger
- **ID**: 1259924342
- **Default Branch**: main
- **Status**: Public (NEW - consolidation target)

### 6. bundus-genetic-insights
- **ID**: 1246206576
- **Language Composition**: JavaScript (78.4%), Python (14.5%), HTML (3.7%), CSS (3.4%)
- **Default Branch**: master
- **Key Content**: Design guidelines (Bio-Tech variant), genetic analysis components
- **Status**: Private

## Language Composition Summary

**Aggregate Across All Repositories**:
- JavaScript: ~65% (primary frontend language)
- Python: ~26% (backend/data processing)
- HTML: ~3% (templates/markup)
- CSS: ~2% (styling)

## Design Guidelines Consolidated

### Two Primary Design Systems Identified:

#### System A: Lab Instrument (from dna-deep-dive)
- Theme: Dark
- Archetype: Swiss & High-Contrast / Modern Lab Instrument
- Primary: Amber (#F59E0B)
- Secondary: Crimson (#E11D48)
- Background: #050505
- Fonts: Chivo, IBM Plex Sans, IBM Plex Mono

#### System B: Bio-Tech (from bundus-with-your-hidden-insights, bundus-genetic-insights)
- Theme: Dark
- Archetype: Swiss & High-Contrast / Dark Mode Bio-Tech
- Primary: Blue (#3366FF)
- Accent: Green (#00E676), Warning (#FFC400), Alert (#FF2A55)
- Background: #0A0A0C
- Fonts: Cabinet Grotesk, IBM Plex Sans, IBM Plex Mono

## Consolidated File Structure

```
apps/
├── dna-deep-dive/
│   ├── design_guidelines.json
│   ├── test_result.md
│   ├── frontend/
│   ├── backend/
│   └── tests/
├── dna-app-site/
│   ├── auth_testing.md
│   ├── frontend/
│   ├── backend/
│   └── bundus-genetic-insights/
├── bundus-genetic-insights/
│   ├── design_guidelines.json
│   ├── auth_testing.md
│   ├── frontend/
│   ├── backend/
│   └── tests/
├── bundus-hidden-insights/
│   ├── design_guidelines.json
│   ├── auth_testing.md
│   ├── frontend/
│   └── backend/
└── bundus-genetical-insight/
    └── README.md

shared/
├── design-system/
│   ├── DESIGN_GUIDELINES.md
│   ├── lab-instrument-theme.json
│   └── biotech-theme.json
├── config/
│   └── shared-config.json
└── utils/
    └── genetic-data-utils.js

docs/
├── API.md
├── TESTING.md
├── CONTRIBUTING.md
└── MIGRATION.md
```

## Key Corrections Made During Consolidation

1. **Design System Unification**: Consolidated two design themes into a unified system with multiple supported themes
2. **Branch Standardization**: Standardized on `main` branch (bundus-genetic-insights was on `master`)
3. **Directory Organization**: Created logical app-based structure to avoid confusion
4. **Documentation**: Created comprehensive README with unified project vision
5. **Testing Standards**: Established data-testid requirements across all apps
6. **Authentication**: Documented auth_testing.md from multiple sources in unified location

## Migration Notes

- All private repositories maintained as separate source backups
- Public repositories (DNA-app-site, Merger) can serve as primary access points
- Design guidelines JSON files preserved for each theme variant
- Test results aggregated for cross-project analysis
- Authentication testing documentation consolidated

## Next Steps for Completion

1. [ ] Merge backend code from all repositories
2. [ ] Consolidate frontend components into shared component library
3. [ ] Unified API specification document
4. [ ] Cross-app integration tests
5. [ ] Update CI/CD pipeline for consolidated build
6. [ ] Migrate issue tracking to single repository
7. [ ] Archive original 6 repositories after confirmation

---

**Consolidated**: June 5, 2026
**Consolidation Point**: SMuculj9/Merger (primary)
**Source Repositories**: 6 (archived for reference)