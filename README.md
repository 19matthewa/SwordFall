# Swordfall - Game Design Document

## Problem Definition and User Research

### Does the product meet qualifications for good ideas?
Swordfall is a compelling concept, delivering an exciting 2D local multiplayer sword-fighting experience with a refined combat system. Built in Unity, it balances consistent core mechanics across all swords with unique special moves—such as a directional katana dash or a curved sword throw—adding layers of tactical depth. The health system, where players withstand 2 regular hits or 1 special move hit, strikes a perfect balance between accessibility and intensity, while upgrades like wings or wall-phasing introduce progression and creativity. This combination ensures the game is approachable yet rich, offering engaging gameplay and vast potential for competitive expansion.

### Identify the target audience and why it's engaging/useful

#### Target Audience:
- Age Group: Ages 10 and up (intuitive controls, strategic depth)
- Interests: Multiplayer action fans, swordplay enthusiasts, and players who enjoy aimable, tactical combat

#### Why It's Engaging:
- Directional specials (e.g., katana dash, curved sword throw) blend melee and ranged skill
- Multiplayer (2-4 players) creates chaotic, social fun
- Upgrades like wall-phasing or extra life reward clever play

#### Why It's Useful:
- Sharpens reflexes, aiming, and decision-making
- Provides a competitive, group-friendly experience

## Conceptualization and Design

### List the Main Features or Functionalities

1. **Weapon System:**
   - Short Sword: Fast swing, short range. Special: Auto-Parry (automatic block for 2s, non-directional, 8s cooldown)
   - Katana: Moderate speed, longer reach. Special: Dash Strike (ranged dash with slash, directional/aimable, 6s cooldown)
   - Curved Sword: Fast combos, medium range. Special: Sword Throw (throws sword for 1 damage, directional/aimable, 4s cooldown)
   - Light Greatsword: Slow swing, high damage. Special: Iron Might (take 50% less damage, deal 50% more damage for 5s, non-directional, 10s cooldown)
   - All swords share base attack (slash, 1 damage) and parry stats; katana and curved sword specials are directional/ranged

2. **Core Mechanics:**
   - Hit: Melee slash (1 damage)
   - Parry: Blocks melee hits and specials (no reflection, brief invulnerability)
   - Dodge: Roll or dash to evade
   - Move Around: Run and jump on 2D platforms
   - Special Hit: Unique effect (2 damage/instant kill unless noted, e.g., curved sword = 1 damage), directional for katana/curved sword

3. **Health System:**
   - Players take 2 regular hits (1 damage each) or 1 special hit (2 damage, instant kill) to be defeated

4. **Upgrades:**
   - Less Visible: 50% transparency
   - Wings: Fly (vertical mobility)
   - Attack Through Walls: attacks can phase through obstacles
   - Extra Life: Revive once with full health

5. **Multiplayer:**
   - 2-4 players, local split-screen or online via Unity's Netcode

6. **Levels:**
   - 2D arenas with platforms, traps (e.g., lava pits), and cover

### Explain the User Flow / Progression (Game)

1. **Start Screen:**
   - Players pick swords, skins, and mode (PvP or co-op)

2. **PvP Gameplay:**
   - 2-4 players spawn on one screen, fight with slashes and specials. Last player wins

3. **Co-op Gameplay:**
   - 2-4 players spawn, face monster waves (e.g., 5 goblins, then 2 ogres). Clear waves to progress; all dying ends the game

4. **Mid-Game:**
   - Upgrades (e.g., wings) spawn mid-screen, aiding PvP dominance or co-op survival

5. **Endgame:**
   - PvP: Last player wins. Co-op: Defeat final wave (e.g., boss monster) or lose. Stats show kills and upgrades

## Behaviors

### What key behaviors or mechanisms make this engaging?

1. **Directional Specials:**
   - Katana's Dash Strike and curved sword's Sword Throw reward aim and positioning, adding a ranged twist

2. **Parry Dynamics:**
   - Blocking specials (no reflection) encourages defensive play—e.g., parrying a Dash Strike to survive

3. **Upgrade Impact:**
   - Wings or wall-phasing paired with specials (e.g., Sword Throw from invisibility) create surprise tactics

4. **Multiplayer Frenzy:**
   - 2-4 player battles blend melee duels with directional specials, sparking chaos and skill showcases

### Utility of the Game / App
- Purpose: Delivers a tactical, sword-based multiplayer experience
- Learning: Enhances aiming, timing, and spatial strategy

### User Experience
- Controls: Hit (left-click), parry (right-click), dodge (space), special (shift + aim with mouse/joystick for katana/curved sword)—smooth and precise
- Feedback: Slash sparks, special trails (e.g., Dash Strike's red line), health flashes (red at 1 HP)

### Visual Aesthetics
- Style: 2D pixel art with Unity's animations and lighting
- Color Scheme: Red (volcanic maps), orange (lava), blue (specials)
- Typography: Bold, pixelated font for UI (e.g., cooldowns)

### Performance and Reliability
- Unity's 2D physics and Netcode ensure 60 FPS and stable online sync

### Accessibility
- Options: Custom controls, colorblind mode, aim assist for directional specials
- Ease: Core mechanics are simple, specials/upgrades add complexity

### Updatable
- New swords (e.g., rapier with a piercing shot), maps, or modes (e.g., survival) via Unity

### Engagement
- Replayability: Sword variety and upgrades keep matches fresh
- Social: Local and online play drive rivalry

## Deployment and Maintenance

### Explain how the product will be deployed

- **Platform:** Swordfall will be deployed as a standalone game for PC and Mac, built in Unity to leverage its cross-platform capabilities for computers. It's designed for local multiplayer on a single screen, requiring no online infrastructure.

- **Distribution:**
  - Digital Stores: Released on Steam and itch.io, with Steam as the primary platform for visibility and itch.io for indie appeal and free demos
  - Downloadable Executable: A direct download option from a simple game website (e.g., hosted via GitHub Pages) for players who prefer avoiding stores

- **Controller Setup:** Since you're unsure about connecting controllers, here's how it works:
  - Keyboard Support: Default controls for up to 4 players using keyboard sections (e.g., WASD for Player 1, arrow keys for Player 2, etc.)
  - Controller Connection: Unity's Input System supports USB or Bluetooth controllers (e.g., Xbox, PlayStation, generic gamepads). Players plug in controllers via USB or pair them via Bluetooth in their computer's settings—Unity auto-detects them. A "Controls" menu lets players assign controllers or use keyboard if no controllers are available (e.g., 2 on keyboard, 2 on controllers)
  - Guidance: In-game tooltips and a PDF manual (bundled with the download) explain setup: "Plug in your controller, press any button to assign it, or use keyboard with WASD."

- **Launch:** Initial release includes PvP and co-op modes, 4 swords, 3 maps, and 5 monster types. A free demo (1 map, PvP-only) on itch.io builds early interest.

### Outline plans for updates or maintenance

- **Updates:**
  - Post-Launch (1-3 Months): Fix initial bugs (e.g., controller detection failures), add 1 new map (e.g., desert ruins), and introduce 1 new sword (e.g., spear with a ranged stab)
  - Quarterly Updates: Release new content like co-op monsters (e.g., a giant spider), PvP/co-op challenges (e.g., survive 5 minutes), or upgrades (e.g., speed burst). Updates deploy via Steam's patching system or itch.io file replacements
  - Player Input: Gather feedback via a Discord server or Steam community hub—e.g., adjust katana dash range if players find it too strong

- **Maintenance:**
  - Bug Fixes: Use Unity's built-in analytics to track crashes (e.g., physics errors from wall-phasing) and release hotfixes via Steam or itch.io. Test updates on Windows and macOS to ensure compatibility
  - Balance Tweaks: Monitor play data (e.g., win rates per sword) and tweak mechanics—e.g., increase curved sword throw cooldown from 4s to 5s if it dominates. Patch notes will detail changes
  - Controller Support: Regularly test with common controllers (Xbox, PS4/5, etc.) as OS updates (e.g., Windows 11, macOS Ventura) roll out, fixing detection issues via Unity Input System updates
  - Long-Term Care: Ensure compatibility with new OS versions (e.g., Windows 12) by updating Unity's engine version annually. Maintain a lightweight game (low storage, <1GB) for easy downloads
  - Content Expansion: Optional free updates every 6-12 months (e.g., "Beast Pack" with 3 new co-op monsters) to keep players engaged, distributed via Steam/itch.io
