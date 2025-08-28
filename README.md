# Akhil's Astrophotography Workflow Tool

A comprehensive, interactive web-based checklist guide for processing astrophotography data using Siril and related tools. This tool provides step-by-step workflows for different imaging scenarios and automatically saves your progress.

## 🌟 Features

- **Interactive Checklists**: Step-by-step guidance with progress tracking
- **Multiple Workflows**: Support for dual-band, broadband, single-night, and multi-night sessions
- **Intelligent Filtering**: Dynamic content based on your target type and setup
- **Progress Persistence**: Your progress is automatically saved in your browser
- **Project Management**: Save, load, and manage multiple imaging projects
- **Advanced Search**: Find specific steps or techniques quickly
- **Color Palette Generator**: Built-in formulas for dual-band image combination
- **Smart Navigation**: "Next Step" button to jump to uncompleted items
- **Responsive Design**: Works on desktop, tablet, and mobile devices

## 🚀 Getting Started

### Quick Start
1. Open the `akhils_siril_workflow.html` file in any modern web browser
2. Configure your imaging scenario using the three dropdown selectors:
   - **Filter**: Choose between Dual-Band or Broadband
   - **Recommendation for**: Select your target type (nebula, galaxy, etc.)
   - **Sessions**: Choose single night or multi-night workflow
3. Follow the step-by-step checklist, checking off completed items
4. Your progress is automatically saved as you work

### Using the Interface

#### Main Navigation
- **Progress Bar**: Shows overall completion percentage at the top
- **Search Bar**: Search for specific steps, tools, or techniques
- **Next Step Button**: Fixed button (bottom-right) that jumps to your next uncompleted step

#### Interactive Elements
- **Checkboxes**: Click to mark steps as complete
- **Phase Collapse/Expand**: Click the `+`/`−` buttons next to phase headers to show/hide sections
- **Highlighted Terms**: Technical terms are highlighted in blue for easy identification
- **Tip Boxes**: Blue informational boxes provide context and pro tips

## 📁 Project Management

### Creating Projects
1. Click the `+` button next to "Project Manager" to expand the section
2. Enter a descriptive name in the "Create a New Project" field (e.g., "M31 - August Session")
3. Click "Clear for New Project" to start fresh
4. Your project settings and progress will be automatically saved

### Loading Existing Projects
1. Expand the Project Manager section
2. Select a project from the "Load Existing Project" dropdown
3. Your previous progress and settings will be restored

### Project Data Management

#### Export/Import Features
- **Export Selected**: Download the currently selected/active project as a JSON file
- **Export All**: Download all your saved projects in one JSON file
- **Import JSON**: Upload a previously exported JSON file to restore projects

#### Data Storage
- **Local Storage**: All data is stored in your browser's localStorage
- **Privacy**: No data is sent to external servers - everything stays on your device
- **Backup Recommended**: Use the Export feature to backup your projects before:
  - Clearing browser data
  - Switching computers
  - Major browser updates

### Managing Projects
- **Delete Projects**: Select a project and click "Delete Selected Project"
- **Clear Current**: Click "Clear for New Project" to reset the current session
- **Reset Progress**: Use the "Reset Current Project Checklist" button at the bottom to clear all checkboxes

## 🔍 Advanced Features

### Search Functionality
- **Real-time Search**: Type in the search bar to filter steps and phases
- **Automatic Expansion**: Search results automatically expand collapsed phases
- **Highlighting**: Matching terms are highlighted in yellow
- **Clear Search**: Click "Clear" to reset and show all content

### Smart Workflows
The tool automatically adapts content based on your selections:

#### Filter Types
- **Dual-Band**: Workflows for narrowband filters (L-Extreme, DuoNarrowBand, etc.)
- **Broadband**: Workflows for standard RGB/OSC imaging

#### Target Recommendations
- **Large, Diffuse Nebula**: Gentle processing parameters for soft nebulae
- **Small/High-Detail Nebula**: More aggressive processing for detailed objects
- **Galaxy/Star Cluster**: Specialized techniques for deep-sky objects

#### Session Types
- **Single Night**: Manual processing using Siril
- **Multi Night**: Automated processing using Sirilic for session combination

### Color Palette System (Dual-Band)
When processing dual-band images, the tool provides:
- **Pre-built Palettes**: Standard HOO, Custom HOO, SHO Hubble, etc.
- **Copy Formulas**: One-click copying of Pixel Math formulas
- **Descriptions**: Explanations of each palette's characteristics

## 🛠️ Technical Details

### Browser Compatibility
- **Recommended**: Chrome, Firefox, Safari, Edge (latest versions)
- **Minimum**: Any browser supporting ES6+ and localStorage
- **Mobile**: Fully responsive design works on smartphones and tablets

### Data Structure
Projects are stored as JSON objects containing:
```json
{
  "projectName": "Your Project Name",
  "timestamp": "2025-08-27T...",
  "checkboxStates": { /* checkbox completion states */ },
  "uiPreferences": { /* filter selections, UI state */ }
}
```

### File Structure
- **Single File**: Everything is contained in `akhils_siril_workflow.html`
- **No Dependencies**: No external libraries or internet connection required
- **Portable**: Copy the file anywhere and it works immediately

## 📋 Workflow Overview

### Dual-Band Workflows
1. **Calibration & Extraction**: File organization and channel separation
2. **Master File Creation**: OIII and Ha processing with optional drizzle
3. **Alignment & Processing**: Master alignment, background extraction, denoising
4. **Color & Enhancement**: Palette application and final processing
5. **Final Assembly**: Star processing and image composition

### Broadband Workflows
1. **Calibration**: Standard OSC preprocessing
2. **Bayer Drizzle Stacking**: Advanced color reconstruction
3. **Linear Processing**: Color calibration, background extraction, denoising
4. **Enhancement**: StarNet++, stretching, sharpening
5. **Final Assembly**: Star recomposition and final touches

## 🎯 Best Practices

### Project Organization
- **Descriptive Names**: Use clear project names like "M42 - February 2025"
- **Regular Exports**: Backup your projects monthly or before major browser changes
- **Session Notes**: Use project names to track dates, conditions, equipment

### Workflow Efficiency
- **Use Search**: Find specific techniques quickly instead of scrolling
- **Collapse Completed**: Collapse finished phases to focus on current work
- **Next Step Button**: Use the FAB button to jump between uncompleted items
- **Reference Appendix**: Check parameter recommendations in the appendix

### Data Management
- **Local Backups**: Export projects to your cloud storage or backup drive
- **Cross-Device**: Import/export to move projects between computers
- **Version Control**: Keep exports dated for different processing attempts

## 🔧 Troubleshooting

### Common Issues

**Progress Not Saving**
- Ensure cookies/localStorage are enabled in your browser
- Check that you're not in private/incognito mode
- Try refreshing the page to see if data persists

**Projects Not Loading**
- Verify the JSON file format is correct when importing
- Check browser console (F12) for error messages
- Clear localStorage and start fresh if corruption is suspected

**Search Not Working**
- Clear the search field and try again
- Refresh the page if highlighting gets stuck
- Use the "Clear" button to reset search state

**Layout Issues**
- Try zooming to 100% in your browser
- Check if you're using a supported browser version
- Disable browser extensions that might interfere with CSS

### Browser Storage Limits
- localStorage typically has a 5-10MB limit per domain
- Each project uses approximately 5-10KB of storage
- You can store hundreds of projects before reaching limits

## 🤝 Contributing

This tool is designed to be self-contained and easily customizable:

### Customization
- Edit the HTML file directly to modify workflows
- Adjust CSS variables at the top of the `<style>` section for color schemes
- Add new workflows by following the existing HTML structure patterns

### Sharing
- The tool works entirely offline - safe to share the HTML file
- All user data stays local - no privacy concerns
- Can be hosted on any web server or opened directly in browsers

## 📄 License

This tool is provided as-is for the astrophotography community. Feel free to modify, share, and improve upon it.

---

**Happy imaging! 🌌**

*For questions about astrophotography techniques, consult the Siril documentation, CloudyNights forums, or astrophotography communities.*
