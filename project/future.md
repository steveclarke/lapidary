# Gemcraft - Future Enhancements

This document captures features and enhancements beyond v1 scope. These are valuable ideas worth preserving for future development phases.

## Table of Contents

- [Phase 2: Complete Core Components](#phase-2-complete-core-components)
- [Phase 3: Styling System](#phase-3-styling-system)
- [Phase 4: Advanced Features](#phase-4-advanced-features)
- [Strategic Vision](#strategic-vision)

## Phase 2: Complete Core Components

### Additional facets (Bubbles) Components

**Text Area**
- Multi-line text editing with line wrapping
- Scrolling support for large content
- Cursor positioning and navigation
- Use cases: log viewers, multi-line input forms, code editors

**Table**
- Column-based data display with headers
- Row selection and navigation
- Column width management
- Sorting capabilities
- Use cases: data browsers, configuration viewers

**File Picker**
- Directory navigation
- File selection (single and multi-select)
- Path filtering and search
- Use cases: file management tools, import dialogs

**Paginator**
- Page-based navigation for large datasets
- Page indicators and controls
- Use cases: paginated lists, documentation browsers

**Progress Bar**
- Determinate and indeterminate progress indicators
- Percentage display
- Custom styling for completion states
- Use cases: long-running operations, downloads, builds

**Viewport**
- Scrollable content container
- Visible area management
- Scroll position tracking
- Use cases: help text viewers, log displays

**Stopwatch & Timer**
- Time tracking components
- Formatting options
- Use cases: timing operations, countdowns

**Help & Key Bindings**
- Built-in help system
- Key binding documentation
- Custom help text rendering
- Use cases: discoverability, user guidance

### Mouse Support

**Mouse Input Handling**
- Click events
- Drag and drop
- Scroll events
- Hover states
- Use cases: enhanced interactivity for power users

### Platform Support

**Windows Platform**
- Windows terminal API integration
- ANSI escape sequence handling for Windows
- Path separator handling
- Platform-specific signal handling
- Use cases: cross-platform CLI tools

## Phase 3: Styling System

### setting (Lip Gloss) Port

**Core Styling Capabilities**
- Color support (8-color, 256-color, TrueColor/24-bit)
- Text formatting (bold, italic, underline, strikethrough)
- Borders (rounded, thick, double, custom)
- Padding and margins
- Alignment (left, center, right)
- Width and height constraints

**Layout System**
- Horizontal and vertical joins
- Layout containers
- Positioning (absolute, relative)
- Z-index layering

**Color Profiles**
- Adaptive colors for terminal capabilities
- Named color palettes
- Custom color schemes

**Advanced Styling**
- Gradients
- Background colors
- Conditional styling
- Style inheritance and composition

## Phase 4: Advanced Features

### shimmer (Glamour) Port

**Markdown Rendering**
- Full markdown syntax support
- Syntax highlighting for code blocks
- Custom themes
- Table rendering
- Link highlighting
- Use cases: README viewers, documentation browsers, help systems

### Advanced Program Features

**Focus Management**
- Focus/blur events
- Tab order management
- Focus indicators
- Use cases: complex forms with multiple input fields

**External Command Execution**
- Run external programs from TUI
- Capture output
- Restore terminal state after execution
- Use cases: git integration, shell command execution

**Advanced Rendering**

**Screen Buffer Optimization**
- Differential rendering (only update changed content)
- Performance improvements for large UIs
- Reduced flickering

**Alternative Renderers**
- Null renderer (for testing)
- String renderer (capture output for testing)
- Custom renderer implementations

### Testing & Development Tools

**Testing Utilities**
- Mock input injection for automated tests
- Output capture for assertions
- Timing control for animation tests
- Integration test helpers

**Debug Mode**
- Message logging
- State inspection
- Performance profiling

## Strategic Vision

### Long-term Goals

**Become the Charmbracelet of Crystal**
- Establish Gemcraft as the default choice for Crystal CLI/TUI development
- Build a community around the toolkit
- Maintain parity with Charmbracelet's ongoing development

**Community & Ecosystem**
- Encourage community-contributed components
- Build showcase gallery of applications using Crystal Sea
- Create educational content and tutorials
- Establish conventions and best practices

**Performance & Polish**
- Benchmark against Charmbracelet
- Optimize rendering performance
- Reduce memory footprint
- Improve startup time

**Integration with Crystal Ecosystem**
- Work well with popular Crystal shards
- Provide generators for common patterns
- CLI scaffolding tools

### Maintenance Strategy

**Stay Aligned with Upstream**
- Monitor Charmbracelet releases for new features
- Port important bug fixes and improvements
- Maintain architectural consistency

**Crystal-Specific Enhancements**
- Take advantage of Crystal's macro system
- Leverage Crystal's type system for better compile-time checks
- Explore Crystal-specific optimizations

