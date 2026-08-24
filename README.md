--------------------------------------------------------------------------------
ASTRONAV -- INCIDENT TERMINAL -- A TN's OUT IN THE BLACKNESS COMPANION
Ship Telemetry / Cargo Manifest / Flight Incident Logging for Starfield
--------------------------------------------------------------------------------

--------------------------------------------------------------------------------
Author\Creator: Mp5lng, a Starfield lover since the first teaser announcement
and a die hard bethesda fan since forever ago.
--------------------------------------------------------------------------------


WHAT IS ASTRONAV?
--------------------------------------------------------------------------------
AstroNAV is a desktop companion terminal for Starfield, built specifically to
operate with TN's Out in The Blackness creation.
It gives you a tactical, out-of-game dashboard for tracking your ship's health,
logging and diagnosing malfunctions, managing repairs against your actual
cargo stock, and keeping tabs on your whole fleet without needing to board
your ship to open OiTB's terminal, or checking with a ship technician.

Under the hood, a small SFSE plugin shipped with AstroNAV keeps the app fed
with live player and ship cargo data (see CARGO SYNC below). Everything
else -- incident logging, fleet management, filtering, requisitions,
themes -- lives entirely in the AstroNAV terminal itself.


--------------------------------------------------------------------------------
 MODULE 01 -- CORE HUD (DASHBOARD)
--------------------------------------------------------------------------------
The dashboard is the first thing you see, and it's built to tell you where
things stand.

  - Live tallies for nodes, modules, and their status, recalculated the
    instant anything changes.
  - A System Integrity bar that rolls everything up into one health
    readout, so overall severity is legible at a glance.
  - Retractable node cards, so a long service history stays manageable
    instead of turning into an unreadable wall of entries.


--------------------------------------------------------------------------------
 MODULE 02 -- SHIP STATUS (MODULE TICKETS)
--------------------------------------------------------------------------------
Every incident is logged through a standardized, error-resistant format:
six dropdown-driven fields per module --

  System | Severity | Replicability | Diagnostics | Repair Task | Status

  - Stack as many diagnostic modules as needed under a single incident.
  - Color-coded status makes unresolved modules easy to spot at a glance.
  - Module tickets are linked directly to your cargo hold -- if the
    materials required for a repair task are available, the ticket is
    automatically flagged as ready for repairs.


--------------------------------------------------------------------------------
 MODULE 03 -- FLIGHT LOGS (INCIDENT NODES)
--------------------------------------------------------------------------------
A dedicated logging suite for documenting malfunctions, systems failures,
diagnostic anomalies, and repair actions over time.

  - File a New Incident: creates a timestamped log entry for your current
    star system and vessel location.
  - Informative Tags: attach details about the incident's location and
    environment, making later filtering and tracking easier.
  - Operational Record: registering an incident turns it into a trackable
    item that persists in your logs going forward.


--------------------------------------------------------------------------------
 MODULE 04 -- FLEET LOGGING (FLEET MANAGEMENT)
--------------------------------------------------------------------------------
AstroNAV isn't limited to a single ship.

  - Switch your active ship to isolate its nodes and telemetry from the
    rest of your fleet.
  - Register a brand-new vessel the moment it joins service.
  - Rename or retire a ship at any time. Retiring a ship wipes its
    incident history automatically.
  - Telemetry and node lists are filtered instantly based on whichever
    ship is currently selected.


--------------------------------------------------------------------------------
 MODULE 05 -- FILTER LOGIC
--------------------------------------------------------------------------------
Built to narrow a long incident log down to exactly the entry you're
chasing.

  - Free-text fields for details unique to a single incident.
  - Structured dropdowns for fields that repeat across your whole log
    (System, Severity, Status, etc).
  - Mix and match free-text and dropdown filters freely.
  - Clear every active filter in a single click.


--------------------------------------------------------------------------------
 MODULE 06 -- REPAIR REQUISITION
--------------------------------------------------------------------------------
Every repair task is attached to its real material cost, so you know
what's required before you commit to a repair.

  - Red        -- you're under-stocked for that repair.
  - Amber      -- you're cutting it close.
  - Green/Cyan -- you're covered, with units to spare.


--------------------------------------------------------------------------------
 MODULE 07 -- CARGO MANIFEST (LIVE CARGO TRACKING)
--------------------------------------------------------------------------------
Your cargo is tracked live by the AstroNAV system, fed by a small SFSE
plugin bundled with the app. The plugin reads your player and ship
inventories directly from the game in the background and hands them off
to the terminal.

  - If AstroNAV ever loses track of your ship's cargo, simply board the
    ship and tracking will pick right back up.
  - To keep the manifest uncluttered, it's programmed to only surface
    materials that are actually relevant to your open repair tasks,
    rather than your full cargo hold.


--------------------------------------------------------------------------------
 MODULE 08 -- PREFERENCES (THEMES)
--------------------------------------------------------------------------------
Twenty-plus looks, one terminal. From CRT phosphor green, to a classic
FreeDOS look, to constellation-inspired themes -- the whole interface
re-skins instantly, and your choice is remembered.

  - Every theme reflows the same data in the same layout -- purely
    cosmetic, nothing functional changes between themes.
  - Loading a save restores the terminal exactly as it looked the last
    time that save was active; theme and display data load automatically
    on system initiation.


--------------------------------------------------------------------------------
 MODULE 09 -- SAFETY MEASURES
--------------------------------------------------------------------------------
Destructive actions always require a second, explicit confirmation before
anything is erased -- purging a node, removing a diagnostic module,
retiring a ship, and similar actions.

  - Clear, specific warning text explaining exactly what will happen.
  - One click to abort if you change your mind.


--------------------------------------------------------------------------------
 CARGO SYNC -- HOW THE APP GETS ITS DATA
--------------------------------------------------------------------------------
AstroNAV ships with a small SFSE plugin (AstroNAV Cargo Tracking Plugin)
that runs inside Starfield itself. It keeps track of your player inventory
and your home ship's cargo hold, and writes that data out for the AstroNAV
terminal to read continuously while you play. This is what powers the live
Cargo Manifest (Module 07) and the Repair Requisition system (Module 06)
-- everything else in the terminal (incidents, fleet, filters, themes) is
handled entirely by the app itself.

You don't need to do anything to make this work beyond installing the
plugin correctly -- see REQUIREMENTS and INSTALLATION below.


REQUIREMENTS
--------------------------------------------------------------------------------
AstroNAV's cargo tracking requires the following to be installed:

  1. SFSE (Starfield Script Extender)
     Launch Starfield through SFSE (not vanilla Starfield.exe) for the
     plugin to load at all.

  2. Address Library for SFSE Plugins


INSTALLATION
--------------------------------------------------------------------------------
  1. Install SFSE and Address Library, and confirm
     the game launches normally through SFSE.

  2. Install the AstroNAV Cargo Tracking Plugin files into your Starfield
	 Data folder or through your mod manager, as with any other SFSE plugin.

  3. Extract the AstroNAV desktop app into a new folder and launch it. The app creates its own Data
     folder, it holds save files and their backups, which are generated
	 automatically with each new data save trigger. These backup saves are there
	 in case of saving or accidental deletion mistakes made by the user.

  4. Launch Starfield through SFSE and load a save. Player inventory
     appears immediately in the terminal; ship cargo appears within a few
     seconds.


USING ASTRONAV
--------------------------------------------------------------------------------
  - Start on the Dashboard to see your fleet's overall status at a
    glance -- node/module tallies and System Integrity.
  - Log incidents as they come up through Flight Logs (Module 03),
    tagging location and environment details as you go.
  - Track individual malfunctions and repairs through Module Tickets
    (Module 02) -- stack diagnostics, watch status colors, and let the
    system flag tickets as soon as you're stocked for the repair.
  - Check Repair Requisition (Module 06) before committing to a repair to
    confirm you have the materials on hand.
  - Use Fleet Management (Module 04) to switch between ships as your
    fleet grows, or to retire ships you no longer fly.
  - Use Filter Logic (Module 05) any time your incident log gets long, to
    narrow it down to exactly what you're looking for.
  - Pick a theme that suits you in Preferences (Module 08) -- purely
    cosmetic, and remembered automatically between sessions.
  - Any destructive action (purging a node, removing a module, retiring a
    ship) will always ask for confirmation first.


TROUBLESHOOTING
--------------------------------------------------------------------------------
  - Cargo Manifest / Repair Requisition show no data:
      Confirm you launched the game through SFSE (not vanilla
      Starfield.exe), and that Address Library for SFSE Plugins is
      installed and matches your game version.

  - Ship cargo stops updating:
      Board your ship. Tracking will automatically pick back up.

  - Everything else (incidents, fleet, filters, themes) is handled by the
    app itself and does not depend on the game running.


--------------------------------------------------------------------------------
 ASTRONAV TERMINAL
--------------------------------------------------------------------------------
AstroNAV Incident Terminal stands fully operational, offering complete
control over ship telemetry, cargo manifest synchronization, and flight
incident logging.

DASHBOARD - DIAGNOSTICS - FLEET - FILTERING
RESOURCES - CARGO - THEMES - SAFETY - DATA INTEGRITY



Safe travels, CMDRs.
