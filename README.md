# Heritage Condition Report Copilot

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0-blue.svg)](https://github.com/mightytonylun/heritage-condition-report-copilot/releases)
[![Browser Support](https://img.shields.io/badge/browser-all%20modern-brightgreen.svg)](#browser-support)

> A web-based companion tool for heritage property inspectors to systematically document conditions, defects, and maintenance costs while working alongside formal reports.

## Overview

Heritage Condition Report Copilot streamlines heritage property assessments by providing inspectors with a structured, field-friendly data entry system. Capture conditions, defects, and costs in grouped categories, attach photo evidence, and export findings directly to Word documents—all offline, in-browser, with zero setup required.

**Perfect for:**
- Heritage conservationists conducting property surveys
- Structural engineers documenting building conditions
- Insurance assessors preparing condition reports
- Maintenance planners prioritizing repairs

## Table of Contents

- [Features](#features)
- [Quick Start](#quick-start)
- [How It Works](#how-it-works)
- [Data Structure](#data-structure)
- [Browser Support](#browser-support)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Features

### Core Functionality
- **Structured Assessment Sections** — Electrical, plumbing, structural, hazard identification, and more
- **Grouped Entry System** — Organize findings by reference numbers + room/element categories
- **Photo Documentation** — Attach images directly to entries; stored locally in browser
- **Cost Estimation** — Calculate subtotals by defect group for budget planning
- **Word Export** — Generate formatted tables ready for condition reports
- **Offline-First** — All data persists in-browser; no internet or server required
- **Responsive Design** — Works seamlessly on desktop, tablet, and mobile devices

### User Experience
- **Zero Setup** — Open HTML file, start using immediately
- **Auto-Save** — Data persists as you type (browser localStorage)
- **Sample Data** — Pre-populated examples demonstrate structure and workflow
- **Inline Editing** — Modify entries directly in preview tables
- **Clear/Reset** — Easily clear all data to start fresh

## Quick Start

### Opening the Tool

```bash
# Option 1: Direct download
# Download heritage-property-assessment.html and open in your browser

# Option 2: Clone repository
git clone https://github.com/mightytonylun/heritage-condition-report-copilot.git
cd heritage-condition-report-copilot
# Open heritage-property-assessment.html in your browser
```

### First Use

1. **Open** `heritage-property-assessment.html` in any modern browser
2. **Review** sample data (property, inspector details, assessment examples)
3. **Modify** entries inline in the preview tables
4. **Add** new property details using form sections
5. **Export** to Word when ready for formal reports

### Field Workflow Example

```
Tablet on-site       → Browser form open, capturing photos + notes
↓
Back at office       → Review entries in grouped preview tables
↓
Reporting            → Export to Word, format final condition report
↓
Archive              → Save Word document alongside property files
```

## How It Works

### Assessment Sections

The form is organized into 10 logical sections:

| Section | Purpose | Grouped? |
|---------|---------|----------|
| **1. Property Details** | Address, date, inspector | No |
| **2. Electrical** | RCD presence, condition notes | No |
| **3. Plumbing** | Leaks, pressure, condition | No |
| **4. Moisture/Ventilation** | Dampness, condensation, hazards | No |
| **5. Hazardous Materials** | Asbestos, lead, other | No |
| **6. Structural** | Foundation, walls, movement | No |
| **7. Exterior Elements** | Roof, elevations, etc. | ✓ By location |
| **8. Interior Spaces** | Rooms, finishes, condition | ✓ By room |
| **9. Defects** | Issues, priority, repairs | ✓ By element |
| **10. Overall Summary** | Final assessment notes | No |

### Grouped Entry System (Sections 7, 8, 9)

For Exterior, Interior, and Defects sections, structure entries with:

- **Reference Number** — Unique identifier (e.g., `RM-01`, `R-01`, `D-02`)
- **Room/Element/Location** — Grouping category (e.g., `Kitchen`, `Roof`, `Window`)
- **Description** — Detailed notes
- **Priority** — (Defects only) `Urgent`, `Important`, `Routine`
- **Suggested Work** — (Defects only) Recommended repairs
- **Photos** — Attachable evidence images

**Example entry:**
```
Ref Number:  D-01
Element:     Roof
Notes:       Missing tiles on east side, exposed underlayment
Priority:    Urgent
Repair:      Replace tiles, inspect flashing
Photos:      [roof-east-01.jpg, roof-east-02.jpg]
```

### Data Storage

```
┌─────────────────────────┐
│   Browser LocalStorage  │
├─────────────────────────┤
│ • assessmentForm        │  (Sections 1-10)
│ • complexData           │  (Grouped entries 7-9)
│ • assessmentPhotos      │  (Photo data)
└─────────────────────────┘
```

**Privacy & Security:**
- All data stored locally on your device
- No cloud upload or external server
- Private until you choose to export
- Persists across browser sessions

## Browser Support

| Browser | Desktop | Tablet | Mobile |
|---------|---------|--------|--------|
| **Chrome** | ✓ | ✓ | ✓ |
| **Firefox** | ✓ | ✓ | ✓ |
| **Safari** | ✓ | ✓ | ✓ |
| **Edge** | ✓ | ✓ | ✓ |

**Requirements:**
- Modern JavaScript support (ES6+)
- localStorage enabled
- File upload capability (for photos)

## Troubleshooting

### Photos not displaying in tables

**Symptom:** Broken image icons in preview tables  
**Solutions:**
- Refresh browser (F5 or Cmd+R)
- Check browser console (F12) for errors
- Ensure browser allows file uploads
- Try a different browser

### Data disappeared after refresh

**Symptom:** Form is empty after closing/reopening  
**Solutions:**
- Check browser privacy settings (may block localStorage)
- Verify browser isn't in private/incognito mode
- Try a standard browsing window
- Keep backups of exported Word documents

### Export to Word not working

**Symptom:** Copy buttons don't transfer data to Word  
**Solutions:**
- Ensure Microsoft Word or compatible software is installed
- Try copying text manually to a new Word document
- Check browser console (F12) for JavaScript errors
- Use browser's developer tools to verify data exists

### Browser console shows storage warnings

**Symptom:** "Tracking Prevention blocked access to storage"  
**Solution:**
- Adjust browser privacy settings to allow storage for this site
- Or use a standard browsing window (not private/incognito mode)

## Tips for Best Results

### Field Work (Tablet/Mobile)
- Open form on tablet during inspection
- Capture photos directly as you assess areas
- Type ref numbers and element names following your system
- Internet not required; data syncs when needed

### Office Work (Desktop)
- Review grouped entries in preview tables
- Edit entries inline before export
- Use export buttons for Word integration
- Archive Word reports for compliance

### Data Organization
- Develop consistent ref number scheme (e.g., `RM-##` for rooms, `D-##` for defects)
- Use element names matching building terminology
- Include timestamps in notes for dated assessments
- Keep photo file names descriptive

## License

MIT License — See LICENSE file for details

**You are free to:**
- ✓ Use commercially
- ✓ Modify and distribute
- ✓ Use privately

**You must:**
- Include license and copyright notice

## Contributing

Found a bug? Have a feature suggestion? Issues and pull requests welcome!

[Report an Issue](https://github.com/mightytonylun/heritage-condition-report-copilot/issues) · [Suggest a Feature](https://github.com/mightytonylun/heritage-condition-report-copilot/issues)

---

**Made for heritage property professionals** who need practical, offline-first assessment tools.

[⬆ Back to top](#heritage-condition-report-copilot)
