# Copilot Instructions for StudioPinVice_Web Portfolio

## Project Overview
- This is a static portfolio web project for StudioPinVice, built with a single `index.html` file and organized image folders for each project.
- All dynamic logic, image rendering, and UI updates are handled in JavaScript within `index.html`.
- Project images are grouped in numbered folders (e.g., `1.1-5/`, `2.MMA/`, etc.), and referenced by arrays in the script section.

## Key Patterns & Conventions
- **Project Data**: The `PROJECTS` array in `index.html` defines all project metadata and order. Update this array to add, remove, or reorder projects.
- **Image Arrays**: Each project with images has a corresponding array (e.g., `oneLifeWelfareImages`) in the script. Images are sorted and referenced by filename order.
- **Image Rendering**: The main content area dynamically renders images using a `.images-column` flex container. Special alignment and scaling for certain images (e.g., 5-2, 5-3) is handled by custom logic in the image rendering loop.
- **Styling**: Most layout is controlled by inline styles and CSS in the `<style>` block. For special cases, inline `style` attributes and `data-align` attributes are used to override alignment.
- **No Build Step**: There is no build process, bundler, or external dependencies. All logic is in `index.html`.

## Developer Workflows
- **To update projects or images**: Edit the `PROJECTS` array and the relevant image arrays in `index.html`. Place new images in the correct numbered folder.
- **To change image alignment or scaling**: Modify the image rendering logic in the JavaScript section of `index.html`. Look for custom blocks handling special cases (e.g., 5-2, 5-3).
- **Debugging**: Open `index.html` in a browser and use DevTools for layout/CSS debugging. All errors will be in the browser console.
- **No tests or build commands**: This project is static and does not use a test framework or build system.

## Examples
- To left-align a specific image, add a custom rendering block in the image loop with `data-align="left"` and strong inline styles.
- To add a new project, update the `PROJECTS` array and create a new image array if needed.

## Key Files & Directories
- `index.html`: All logic, data, and UI.
- `1.1-5/`, `2.MMA/`, ...: Image folders for each project.
- `.github/copilot-instructions.md`: (this file) AI agent guidance.

## Special Notes
- Folder and file naming is significant for image ordering and project mapping.
- All project-specific logic is centralized in `index.html`.
- There are no external scripts, frameworks, or package managers.

---
For any non-obvious UI or alignment issues, always check for custom rendering logic in the image loop in `index.html`.
