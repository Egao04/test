# CLAUDE.md - AI Assistant Guide for egao04 Repository

**Last Updated**: 2025-11-18
**Repository Owner**: Egao04 (taniyama.egao.28c@st.kyoto-u.ac.jp)
**Current Branch**: claude/claude-md-mi4je8gftscdrkng-014ENk2Agp5C8i6D56Kuxw4J

---

## Table of Contents
1. [Repository Overview](#repository-overview)
2. [Current State](#current-state)
3. [Historical Context](#historical-context)
4. [Directory Structure](#directory-structure)
5. [Technology Stack](#technology-stack)
6. [Development Workflows](#development-workflows)
7. [Git Conventions](#git-conventions)
8. [Code Conventions](#code-conventions)
9. [Key Files Reference](#key-files-reference)
10. [AI Assistant Guidelines](#ai-assistant-guidelines)

---

## Repository Overview

### Purpose
This repository was originally created as a **web-based theater production website** for "FakesSpeare" (フェイクスピア - "劇団ケッペキ"), a Japanese theater play scheduled for September 28-30, 2024, at Kyoto University.

### Current State: MINIMAL
- **Status**: Repository has been stripped down to minimal content
- **Latest Commit**: c407ca0 - "Update" (deleted all website files)
- **Current Contents**: Only README.md with "# test"
- **Likely Reason**: Event concluded; repository cleared for reuse or archival

---

## Current State

### Active Files
```
egao04/
├── .DS_Store          # macOS system file (should be gitignored)
├── .git/              # Git repository metadata
└── README.md          # Minimal placeholder ("# test")
```

### Repository Statistics
- **Total Commits**: 11 (all from August 12, 2024)
- **Active Branches**: Multiple (including claude/* feature branches)
- **Remote**: Configured with local proxy (127.0.0.1:49882)
- **GPG Signing**: SSH-based signing enabled

---

## Historical Context

### Peak State (Commits a251c8e and 05f1394)
The repository previously contained a full-featured static website with:
- Responsive HTML pages (254+ lines)
- Custom CSS styling (498 lines)
- jQuery-based interactions (231 lines)
- Image assets and logos
- Multi-page navigation structure

### Evolution Timeline
1. **6108dc8** - Initial commit (README only)
2. **ae2689a** - Test commit
3. **ee2a859** - Added full HTML/CSS/JS stack
4. **5c0b795** - Major CSS refactoring (removed 684 lines)
5. **a251c8e** - CSS and JS updates
6. **fea27f3** - Deleted all files
7. **e3dd741** - Cleaned .DS_Store
8. **05f1394** - Reorganized into `docs/` folder
9. **61109bf-c407ca0** - Final cleanup to current minimal state

---

## Directory Structure

### Historical Structure (for reference)
```
egao04/
├── html/                      # HTML pages
│   ├── example.html           # Main page (254 lines)
│   └── cast.html              # Cast information
│
├── css/                       # Stylesheets
│   └── example.css            # Main styles (498 lines)
│
├── script/                    # JavaScript
│   ├── example.js             # Main functionality (231 lines)
│   └── jquery-3.7.1.min.js    # jQuery library
│
├── img/                       # Image assets
│   ├── example.jpg
│   ├── example.png
│   ├── logo-white.png
│   └── web.png
│
└── docs/                      # GitHub Pages structure (commit 05f1394)
    ├── index.html
    ├── css/
    ├── script/
    ├── img/
    └── pages/
        └── news1.html
```

### Recommended Structure (for future development)
```
egao04/
├── .gitignore                 # Should include .DS_Store
├── README.md                  # Comprehensive project documentation
├── CLAUDE.md                  # This file
│
├── src/                       # Source files
│   ├── html/
│   ├── css/
│   ├── js/
│   └── assets/
│       └── img/
│
├── docs/                      # GitHub Pages deployment
│   └── [compiled/copied files]
│
└── tests/                     # Future: testing infrastructure
```

---

## Technology Stack

### Frontend Technologies
- **HTML5**: Semantic markup, responsive meta viewport
- **CSS3**:
  - Responsive design (breakpoint at 720px)
  - Media queries
  - CSS animations
  - Pseudo-elements (::before, ::after)
  - Gradient backgrounds
- **JavaScript**:
  - jQuery 3.7.1
  - Smooth scrolling
  - Event listeners
  - DOM manipulation
  - Scroll-triggered animations

### Development Tools
- **Version Control**: Git
- **No Build System**: Static files (no webpack, gulp, etc.)
- **No Package Manager**: No npm/yarn dependencies
- **Deployment**: Likely GitHub Pages (docs/ folder pattern)

### Browser Support
- Modern browsers with ES5+ JavaScript support
- CSS3 media query support
- Smooth scrolling behavior support

---

## Development Workflows

### Git Workflow
1. **Feature Branches**: Use `claude/*` prefix for AI-assisted development
2. **Branch Naming**: `claude/claude-md-{identifier}-{session-id}`
3. **Commit Pattern**: Simple "Update" messages (historical pattern)
4. **Push Requirements**:
   - Always use `git push -u origin <branch-name>`
   - Branch must start with 'claude/' and match session ID
   - Retry up to 4 times with exponential backoff on network errors (2s, 4s, 8s, 16s)

### Development Process (Historical)
1. Create/edit HTML files in `html/` or directly in `docs/`
2. Style with CSS in `css/` directory
3. Add interactivity with JavaScript in `script/`
4. Test responsiveness at 720px breakpoint
5. Deploy to `docs/` for GitHub Pages
6. Commit and push changes

### Recommended Future Workflow
1. Add `.gitignore` file (include .DS_Store, node_modules, etc.)
2. Implement build system for optimization
3. Add testing framework (Jest, Cypress, etc.)
4. Use semantic commit messages
5. Implement CI/CD for automated deployment

---

## Git Conventions

### Current Patterns
- **Commit Messages**: Simple one-word "Update" (not descriptive)
- **Author**: Egao04 <taniyama.egao.28c@st.kyoto-u.ac.jp>
- **GPG Signing**: SSH-based signing enabled
- **No Tags**: No version tags or releases

### Recommended Conventions
```bash
# Commit message format
<type>(<scope>): <subject>

# Types: feat, fix, docs, style, refactor, test, chore
# Examples:
git commit -m "feat(navbar): add smooth scroll animation"
git commit -m "fix(css): correct mobile menu z-index"
git commit -m "docs(readme): update installation instructions"
```

### Branch Protection
- Main branch should be protected
- Require pull request reviews for main
- Use feature branches for all development

---

## Code Conventions

### HTML Conventions (Historical)
- **Structure**: Semantic HTML5 tags
- **IDs for Sections**: `#mainvisual`, `#news`, `#story`, `#cast`, `#staff`, `#ticket`, `#special`, `#guide`
- **Classes**: `.menu` (mobile), `.menu2` (desktop), `.cover` (overlay)
- **Language**: Japanese content with UTF-8 encoding
- **Indentation**: Consistent indentation (2 or 4 spaces)

### CSS Conventions (Historical)
```css
/* Mobile-first approach */
@media screen and (max-width: 720px) {
    /* Mobile styles */
    font-size: 62.5%;
}

@media screen and (min-width: 721px) {
    /* Desktop styles */
    font-size: 75%;
}
```

**Key Patterns**:
- Mobile breakpoint: ≤720px
- Desktop breakpoint: >720px
- Responsive font sizing with rem units
- Z-index layering: navigation (100), overlays (99)
- Animations: transitions for smooth effects

### JavaScript Conventions (Historical)
```javascript
// jQuery-based
$(document).ready(function() {
    // Event listeners
    $('.selector').on('click', function() {
        // Functionality
    });
});
```

**Key Patterns**:
- jQuery 3.7.1 usage
- Smooth scroll implementation
- Event delegation
- Scroll position detection
- Animation timing functions

### File Naming
- **HTML**: lowercase with hyphens (`example.html`, `cast.html`)
- **CSS**: lowercase with hyphens (`example.css`)
- **JS**: lowercase with hyphens (`example.js`)
- **Images**: lowercase with hyphens (`logo-white.png`)

---

## Key Files Reference

### Historical Files (for reference from git history)

#### `/html/example.html` (254 lines)
**Purpose**: Main landing page
**Key Sections**:
- Navigation menus (mobile + desktop)
- 8 content sections with IDs
- Cast and staff information
- Ticket purchasing details
- Venue information

**Notable Features**:
- Responsive viewport meta tag
- jQuery 3.7.1 integration
- Hamburger menu structure

#### `/css/example.css` (498 lines)
**Purpose**: Main stylesheet
**Key Features**:
- Responsive design (720px breakpoint)
- Hamburger menu animations
- Section header styling with ::before
- Smooth scroll behavior
- Gradient backgrounds
- Opacity transitions

**Code Organization**:
- Global styles
- Navigation styles
- Section-specific styles
- Media queries (mobile/desktop)

#### `/script/example.js` (231 lines)
**Purpose**: Interactive functionality
**Key Features**:
- Hamburger menu toggle
- Smooth scrolling navigation (8 items)
- Scroll-triggered header fade-in
- Underline animations on scroll
- Navigation click handlers

**Dependencies**: jQuery 3.7.1

#### `/docs/index.html`
**Purpose**: GitHub Pages deployment version
**Structure**: Mirror of main site in deployment-ready format

---

## AI Assistant Guidelines

### When Working on This Repository

#### 1. **Understand the Context**
- Repository is currently minimal (cleared after event)
- Historical commits contain full website code
- May be repurposed for new content
- Respect the original structure when adding new features

#### 2. **Code Quality Standards**
- **Responsive Design**: Always test at 720px breakpoint
- **Browser Compatibility**: Support modern browsers
- **Performance**: Optimize images, minify code for production
- **Accessibility**: Use semantic HTML, ARIA labels when needed
- **i18n**: Support Japanese language (UTF-8 encoding)

#### 3. **Git Operations**
```bash
# Create feature branch
git checkout -b claude/feature-name-{session-id}

# Stage changes
git add <files>

# Commit with descriptive message
git commit -m "feat(scope): description"

# Push with upstream tracking
git push -u origin claude/feature-name-{session-id}

# Retry logic for network failures (up to 4 times)
# Exponential backoff: 2s, 4s, 8s, 16s
```

#### 4. **File Operations Best Practices**
- Use Read tool before Edit/Write operations
- Preserve indentation and formatting
- Add .gitignore if creating new files
- Never commit .DS_Store files
- Use absolute paths for file operations

#### 5. **When Adding New Features**
- Check git history for previous implementations
- Follow established naming conventions
- Maintain responsive design principles
- Update this CLAUDE.md with new patterns
- Test mobile and desktop views

#### 6. **Common Tasks**

**Restoring Previous Version**:
```bash
# View history
git log --oneline

# Checkout specific commit
git checkout a251c8e -- html/example.html css/example.css script/example.js

# Or restore entire state
git checkout 05f1394 -- docs/
```

**Adding New Page**:
1. Create HTML in `html/` or `docs/pages/`
2. Link from main navigation
3. Follow existing structure (sections with IDs)
4. Add corresponding CSS rules
5. Update navigation JavaScript

**Updating Styles**:
1. Edit CSS in `css/example.css`
2. Test mobile (≤720px) and desktop (>720px)
3. Maintain existing z-index hierarchy
4. Use rem units for responsive sizing

#### 7. **Testing Checklist**
- [ ] Mobile view (≤720px)
- [ ] Desktop view (>720px)
- [ ] Smooth scrolling functionality
- [ ] Navigation menu (hamburger on mobile)
- [ ] All links functional
- [ ] Images load correctly
- [ ] Cross-browser compatibility
- [ ] Japanese text displays properly

#### 8. **Deployment Process**
1. Make changes in `src/` or root directories
2. Test locally
3. Copy/compile to `docs/` folder for GitHub Pages
4. Commit and push
5. Verify deployment at GitHub Pages URL

#### 9. **Code Review Standards**
- Validate HTML5 syntax
- Check CSS for cross-browser compatibility
- Ensure JavaScript has no console errors
- Verify responsive breakpoints
- Test all interactive features
- Check for accessibility issues

#### 10. **Documentation Requirements**
- Update README.md with project description
- Document any new dependencies
- Add inline comments for complex logic
- Update this CLAUDE.md with new conventions
- Include setup instructions for new developers

---

## Quick Reference Commands

### Repository Exploration
```bash
# View git history
git log --oneline --graph --all

# See what was deleted
git log --diff-filter=D --summary

# View file at specific commit
git show commit-hash:path/to/file

# Restore deleted files
git checkout commit-hash -- path/to/file
```

### Development Server (if needed)
```bash
# Python simple server
python3 -m http.server 8000

# Node.js http-server (if installed)
npx http-server
```

### File Management
```bash
# Find all HTML files in history
git log --all --full-history -- "*.html"

# Search for content in history
git log -S "search-term" --source --all
```

---

## Notes for AI Assistants

### Current Repository State
- **IMPORTANT**: Repository is essentially empty except for README.md
- All previous website code has been deleted (as of commit c407ca0)
- Code can be restored from git history if needed
- Assume this is a fresh start unless instructed otherwise

### Restoration Guidance
If user wants to restore previous website:
1. Identify target commit (a251c8e for peak features, 05f1394 for docs structure)
2. Use `git checkout <commit> -- <paths>` to restore files
3. Test restored files for functionality
4. Update dependencies if needed (jQuery version, etc.)

### Building New Features
If user wants new website/content:
1. Learn from historical structure (good responsive patterns)
2. Suggest modern improvements (build tools, testing, etc.)
3. Maintain Japanese language support
4. Follow responsive design principles (720px breakpoint)
5. Use semantic HTML and accessible markup

### Key Considerations
- **macOS Artifacts**: Add .gitignore to exclude .DS_Store
- **No Dependencies**: Currently no package.json; add if needed
- **Static Site**: No backend; pure frontend project
- **GitHub Pages**: Use `docs/` folder for deployment
- **Japanese Content**: Ensure UTF-8 encoding support

---

## Contact & Support

**Repository Owner**: Egao04
**Email**: taniyama.egao.28c@st.kyoto-u.ac.jp
**Organization**: Kyoto University (京都大学)

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| 1.0 | 2025-11-18 | Initial CLAUDE.md creation with comprehensive repository analysis |

---

**End of CLAUDE.md**
