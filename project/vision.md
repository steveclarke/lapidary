# Gemcraft - Vision Document

Build beautiful, interactive CLI/TUI applications in Crystal with the same power that Go developers get from Charmbracelet.

## Table of Contents

- [Problem](#problem)
- [Solution](#solution)
- [User Needs](#user-needs)
- [Future Possibilities](#future-possibilities)
- [Scope](#scope)

## Problem

Crystal developers who want to build beautiful, interactive terminal applications face a difficult choice:

**Learn Go or settle for less.** The Charmbracelet ecosystem (Bubble Tea, Lip Gloss, Bubbles, Glamour) gives Go developers an incredible toolkit for building modern CLI/TUI apps with interactive forms, selectors, styled components, and markdown rendering. But if you prefer Crystal's Ruby-like syntax, you're out of luck. Crystal doesn't have an equivalent ecosystem.

**The current workaround is painful.** Crystal developers who want these capabilities must either:
- Learn Go and abandon the Ruby-style syntax they love
- Build CLI tools in TypeScript and deal with Node dependencies
- Settle for basic, unpolished command-line interfaces in Crystal

This affects Crystal developers who are building:
- Developer tooling and DX utilities (like interactive work tree managers)
- Business applications with CLI interfaces (like accounting transaction browsers)
- Any terminal application where user experience matters

The consequence: Crystal developers miss out on the convenience and beauty of interactive forms, multi-selectors, spinners, and TUI-style applications. Their CLI tools remain basic and less polished than what's possible with Charmbracelet.

## Solution

Port Charmbracelet's proven architecture to Crystal using a disciplined, 1:1 translation approach.

**Core Philosophy:** Stand on the shoulders of giants. Charmbracelet has already solved the hard problems of building beautiful terminal UIs. Rather than reinvent the wheel, we translate their battle-tested architecture directly to Crystal. Think of it like translating Lord of the Rings from English to French - we're not trying to improve the story, just make it readable in a different language.

**Key Technical Approach:**
- Follow Charmbracelet's file structure exactly (Go's `tea.go` becomes Crystal's `sea.cr`)
- Mirror their module organization and API design
- Validate the port by getting their example programs working in Crystal
- Use Crystal's native C bindings for terminal control (similar to Go's approach)

**The Gemcraft Ecosystem:**

| Charmbracelet | Gemcraft | Purpose |
|---------------|----------|---------|
| **Charmbracelet** | **Gemcraft** 💎 | Ecosystem/toolkit brand |
| **Bubble Tea** | **gem** 💎 | Core event loop implementing The Elm Architecture |
| **Bubbles** | **facets** 🔷 | Interactive components (lists, inputs, spinners) |
| **Lip Gloss** | **setting** 💍 | Styling system (colors, borders, layout) |
| **Glamour** | **shimmer** 🌟 | Markdown rendering for help text and docs |

**Conceptual Unity:** A gem is cut into facets, placed in a setting, and shimmers in the light.

**What Makes This Work:**
- Charmbracelet is MIT-licensed, so the architecture is freely adaptable
- Crystal and Go have similar capabilities (fibers vs goroutines, channels, C bindings)
- A systematic, module-by-module porting approach prevents divergence and guesswork
- We're translating proven solutions, not experimenting with new approaches

## User Needs

### Crystal Developers (End Users)
Crystal developers building CLI/TUI applications need:
- Access to beautiful, interactive terminal components (lists, selectors, input forms, spinners)
- A proven architecture that works reliably without having to learn Go
- The ability to build polished command-line tools while staying in Ruby-style syntax
- Components that feel natural in Crystal's ecosystem

### Product Team (Maintainers)
The maintainers building and evolving Gemcraft need:
- A structured porting process that minimizes decision-making and guesswork
- Clear mapping from Charmbracelet's Go code to Crystal equivalents
- Validation through working example programs (port their examples, prove it works)
- The ability to reference upstream Charmbracelet when questions arise

## Future Possibilities

See [future.md](future.md) for detailed future enhancements including:
- Additional Bubbles/facets components (table, file picker, text area, paginator, progress bar)
- setting (Lip Gloss) styling system
- shimmer (Glamour) markdown rendering
- Mouse support
- Windows platform support

## Scope

### What v1 Delivers

**gem (Bubble Tea Core) - Minimum Viable Implementation:**
- Core type system (Model, Msg, Cmd)
- Program event loop and initialization
- Key input handling and ANSI escape sequences
- Built-in commands (Quit, Batch, Sequence, Tick)
- Terminal control (raw mode, rendering)
- Basic renderer implementation
- Signal handling (resize, interrupts)
- Fiber-based concurrency for async commands
- Unix/macOS platform support only

**facets (Bubbles Components) - Three Core Components:**
- **List** - Interactive list selection and navigation (keyboard-driven)
- **Text Input** - Single-line text entry with editing
- **Spinner** - Animated loading indicator (demonstrates async/animation)

**Example Program:**
- At least one complete working example demonstrating all three components
- Following Charmbracelet's example structure

**Development Approach:**
- Follow Bubble Tea's file structure 1:1 (e.g., `tea.go` → `src/gem.cr`)
- Mirror Go's module organization in Crystal
- Validate by porting and running Charmbracelet's examples

### What v1 Does NOT Include

- Remaining Bubbles components (table, file picker, text area, paginator, progress bar, viewport, stopwatch, timer, help, key bindings)
- setting (Lip Gloss) styling system - basic output only, no styled components
- shimmer (Glamour) markdown rendering
- Mouse input support
- Windows platform support
- Advanced features (focus management, external command execution)

