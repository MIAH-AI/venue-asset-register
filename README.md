# Venue Asset Register

A single-page asset management app for the conference centre: asset register, room-by-room stock-takes, theft and loss incidents, maintenance scheduling, and supplies replenishment.

The whole app is one file: `index.html` (HTML, CSS and JavaScript, no build step).

## Features

- **Overview:** live totals, a verification ring, a progress bar for each location, and items that need attention
- **Assets:** one record per item or batch, with tag numbers, location, condition, value, serial number and photo; CSV import and export
- **Stock-take:** count each room, flag shortages as you go, then reconcile and close (updates the register and logs losses)
- **Incidents:** theft and break-in log with police reference and loss totals
- **Maintenance:** recurring and one-off jobs; marking one done moves the next due date forward
- **Supplies & orders:** reorder levels, stock movements, purchase requests, and replacements for missing items
- **Guide & setup:** stock-take procedure, locations, categories, currency
- **Appearance:** glass design with Light/Dark mode and 37 colour palettes (pairs and gradients), remembered per browser

## Where it runs

The app was built as a claude.ai artifact. Its shared database, sign-in names, photo uploads and file exports use the claude.ai artifact runtime (`window.claude`).

- **Live version:** the published claude.ai artifact (all features, data shared with your team).
- **Opened from this repo (for example with GitHub Pages or a local file):** the design, navigation and palettes work, but there is no shared database, so records can't be saved. The page shows a notice saying the register can't be reached.

To run it fully outside claude.ai, the `claude.use("db")`, `claude.use("user")`, `claude.use("assets")` and `claude.use("downloads")` calls need to be replaced with your own backend (for example Firebase or Supabase).
