# HabitHero 🦸‍♂️

A lightweight habit tracking web app that helps users build and maintain daily habits with streak tracking.

## Project Overview

- **Type:** Frontend web application (single-page app)
- **Architecture:** All-in-one HTML file with embedded CSS and JavaScript
- **Storage:** Browser localStorage (no backend/database)
- **Target:** Modern browsers supporting ES6+

## Features

- ✅ Add new habits with a simple text input
- ✅ Mark habits as done/undone with checkboxes
- ✅ Track consecutive day streaks (🔥 badge)
- ✅ Delete individual habits
- ✅ Reset all habits with confirmation
- ✅ Persistent storage across browser sessions

## Project Structure

```
HabitHero/
├── index.html       # Main app (HTML + CSS + JS combined)
├── main.js          # Currently unused placeholder
├── style.css        # Currently unused placeholder
└── CLAUDE.md        # This file
```

## Development Guidelines

### Code Style

- **JavaScript:** Modern ES6+ (arrow functions, const/let, template literals)
- **CSS:** CSS Grid and Flexbox for layouts; BEM-style class naming where possible
- **HTML:** Semantic HTML5; keep accessibility in mind (labels, alt text, ARIA where needed)
- **Naming:** Use camelCase for JS variables/functions, kebab-case for CSS classes

### Working with the Code

1. **Editing:** All logic currently lives in `index.html` — edit the `<script>` section for JS, `<style>` section for CSS
2. **Testing:** Open `index.html` in a browser (use Live Server extension if available)
3. **Data Flow:** Habits array → renderHabits() → DOM updates → localStorage sync

### Key Functions

- `renderHabits()` — Main render function; updates DOM and persists to localStorage
- `addHabit()` — Creates new habit with default values (done=false, streak=0)
- `toggleHabit(index)` — Toggles done status and updates streak
- `deleteHabit(index)` — Removes habit from array
- `resetAllHabits()` — Clears all habits with confirmation

## Common Tasks

### Adding a New Feature

1. Update the HTML structure in the `<body>` section
2. Add styling to the `<style>` block
3. Add logic to the `<script>` section
4. Test in browser

### Bug Fixes

- Check browser console for errors
- Verify localStorage still has the data
- Ensure all event handlers (onclick) are correctly wired

### Potential Improvements (Not Yet Implemented)

- Separate JS and CSS into external files (main.js, style.css)
- Add habit categories or tags
- Add date tracking (when habit was last completed, not just streak count)
- Dark mode
- Habit statistics/charts
- Mobile app version

## Testing

Open `index.html` in a browser and test:

- ✅ Add multiple habits
- ✅ Toggle completion on/off
- ✅ Streak increments and decrements correctly
- ✅ Delete removes only that habit
- ✅ Reset clears everything
- ✅ Reload page — data persists
- ✅ Check browser DevTools > Application > localStorage for 'habits' entry

## Browser Compatibility

- Modern browsers: Chrome, Firefox, Safari, Edge (all recent versions)
- Requires: localStorage support, ES6 JavaScript
- No external dependencies

## File Conventions

- Indent with 2 spaces
- Keep functions under 20 lines when possible
- Comment WHY, not WHAT (code should be self-explanatory)
- Avoid inline event handlers where practical (prefer addEventListener)

## Quick Commands

When working with Claude Code:

- **View structure:** `ls -la`
- **Check current state:** Open `index.html` in a browser
- **Inspect data:** Open DevTools > Application > Storage > localStorage
- **Hot reload:** Save file and refresh browser (Ctrl+R / Cmd+R)

## Notes

- The app is intentionally simple — prioritize user experience and code clarity over complex features
- localStorage has ~5-10MB limit per domain (not a concern for this project)
- No user authentication — data is local and device-specific
- Emoji usage is part of the design (🦸‍♂️🔥🗑️); keep it!)
