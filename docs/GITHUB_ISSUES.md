# GitHub Issues - Ready to Create

This file contains all 14 Game V3 features formatted for easy creation as GitHub issues. Simply copy the content between the dividers for each issue and paste into GitHub's "New Issue" form.

---

## Issue 1: Add Sound Effects

**Labels:** `enhancement`, `audio`, `high-priority`

**Title:**
```
Add Sound Effects
```

**Description:**
```markdown
## Priority
High

## Category
Audio

## Description
Add sound effects throughout the game to enhance the player experience and provide audio feedback for game events.

## Acceptance Criteria
- [ ] Unit spawning sounds (different sound for each unit type)
- [ ] Combat/attack sounds
- [ ] Unit death/destruction sounds
- [ ] Base damage sounds
- [ ] Victory sound effect
- [ ] Defeat sound effect
- [ ] Gold collection/earning sound
- [ ] Button click/UI interaction sounds
- [ ] Sound effects respect the mute toggle setting
- [ ] Volume levels are balanced and not overwhelming

## Technical Notes
- Use Phaser's sound system for audio management
- Consider using a sound sprite for efficiency
- Ensure sounds are properly preloaded
- Add sound effects to existing SoundFX.js or create new sound management module

## Dependencies
None

## Estimated Effort
Medium (3-5 hours)
```

---

## Issue 2: Add Unit and Combat Animations

**Labels:** `enhancement`, `visuals`, `high-priority`

**Title:**
```
Add Unit and Combat Animations
```

**Description:**
```markdown
## Priority
High

## Category
Visuals

## Description
Add animations to units to make the game more visually appealing and dynamic. Currently units are static stickman sprites.

## Acceptance Criteria
- [ ] Walking/marching animation for units
- [ ] Attack animations (melee and ranged)
- [ ] Death/destruction animations
- [ ] Idle animations when units are waiting/not moving
- [ ] Projectile animations for archers (arrow flight)
- [ ] Base damage/destruction visual effects
- [ ] Animations are smooth and don't impact performance
- [ ] Each unit type has unique animations appropriate to their class

## Technical Notes
- Use Phaser's animation system
- Consider using sprite sheets for frame-based animations
- May need to update the procedural stickman sprite generation or replace with pre-made sprites
- Ensure animations sync with game logic (attacks happen when animation plays)

## Dependencies
None

## Estimated Effort
Large (8-12 hours)
```

---

## Issue 3: Add Background Graphics

**Labels:** `enhancement`, `visuals`, `medium-priority`

**Title:**
```
Add Background Graphics
```

**Description:**
```markdown
## Priority
Medium

## Category
Visuals

## Description
Replace the current plain background with proper background graphics to make the game more visually appealing.

## Acceptance Criteria
- [ ] Layered parallax background (multiple layers moving at different speeds)
- [ ] Ground/terrain graphics
- [ ] Sky graphics with clouds
- [ ] Environmental details (trees, rocks, etc.)
- [ ] Background should match the current age/era theme
- [ ] Background scrolls properly with camera movement
- [ ] Performance is maintained with background graphics

## Technical Notes
- Use Phaser's tilesprite or image layers for background
- Implement parallax scrolling at different rates for depth
- Consider creating different backgrounds for each age (ties into Issue 5)
- Background should be behind all game elements

## Dependencies
- May tie into Issue 5 (Age Progression) for age-specific backgrounds

## Estimated Effort
Medium (4-6 hours)
```

---

## Issue 4: Marble Simulator Mode

**Labels:** `experimental`, `low-priority`

**Title:**
```
Research and Implement Marble Simulator Mode
```

**Description:**
```markdown
## Priority
Low

## Category
Experimental, Game Mode

## Description
Research and potentially implement a "Marble Simulator" concept. This appears to be an experimental idea that may refer to a physics-based game mode or mini-game.

## Acceptance Criteria
- [ ] Research what "Marble Simulator" concept means in this context
- [ ] Design document outlining the proposed feature
- [ ] Determine if this should be a separate game mode, mini-game, or alternative gameplay mechanic
- [ ] If greenlit, implement basic prototype

## Questions to Clarify
- What is the intended "Marble Simulator" concept?
- Is this a physics-based mode where units behave like marbles?
- Is this a reference to another game or genre?
- Should this be integrated into the main game or be a separate mode?

## Technical Notes
- May require physics engine enhancements
- Could be implemented as an alternative game mode accessible from the menu
- Needs further specification before implementation

## Dependencies
None

## Estimated Effort
Unknown - requires clarification
```

---

## Issue 5: Implement 4-Age Progression System

**Labels:** `enhancement`, `gameplay`, `high-priority`

**Title:**
```
Implement 4-Age Progression System
```

**Description:**
```markdown
## Priority
High

## Category
Progression, Core Gameplay

## Description
Create an age progression system where players advance through 4 distinct historical eras, each with unique units, visuals, and increasing difficulty.

## Ages
1. **Stone Age** - Primitive weapons and units (clubs, rocks, cavemen)
2. **Middle Ages** - Medieval units and weapons (swords, knights, castles)
3. **Modern Age** - Contemporary warfare (soldiers, guns, tanks)
4. **Future Age** - Futuristic units and technology (robots, lasers, sci-fi)

## Acceptance Criteria
- [ ] Design unique unit types for each age
- [ ] Create age-specific visual themes and aesthetics
- [ ] Implement progression system that advances ages based on levels completed
- [ ] Each age has appropriate difficulty scaling
- [ ] Age advancement is clearly communicated to the player
- [ ] UI reflects the current age theme
- [ ] Balance units across ages for fair progression

## Technical Notes
- Consider how existing units map to different ages
- May need to create 4 sets of unit sprites/animations
- Age progression could trigger after completing certain levels
- Store current age in game state
- Update unit spawning logic to use age-appropriate units

## Dependencies
- Ties into Issue 6 (Age-Specific Buildings)
- Affects Issue 3 (Backgrounds should match age)
- May affect Issue 8 (Music could be age-specific)

## Estimated Effort
Very Large (16-24 hours)

Note: Wide estimate range due to:
- Uncertainty in whether age progression requires completely new unit types or can reuse existing units with visual changes
- Scale of visual asset creation needed (4 full sets vs. themed variants)
- Complexity of progression logic and state management
- Potential need for rebalancing entire game economy across ages

Consider breaking into sub-tasks:
1. Design and implement age progression system (4-6 hours)
2. Create age-specific units and balance (8-12 hours)
3. Implement age-specific visuals and UI (4-6 hours)
```

---

## Issue 6: Create Age-Specific Building Types

**Labels:** `enhancement`, `visuals`, `medium-priority`

**Title:**
```
Create Age-Specific Building Types
```

**Description:**
```markdown
## Priority
Medium

## Category
Progression, Visuals

## Description
Design different base/building appearances for each age to enhance the visual progression and thematic consistency as players advance through eras.

## Building Types by Age
1. **Stone Age** - Cave entrance or primitive hut
2. **Middle Ages** - Castle or fortress
3. **Modern Age** - Military bunker or command center
4. **Future Age** - High-tech facility or space station

## Acceptance Criteria
- [ ] Create visual designs for 4 different base types
- [ ] Each base type is visually distinct and appropriate to its age
- [ ] Base graphics are used for both player and enemy bases
- [ ] Bases scale appropriately and maintain hitbox consistency
- [ ] Base destruction animations fit the theme
- [ ] HP bars and UI elements work with all base types

## Technical Notes
- Replace or extend current base rendering code
- May use sprite sheets or separate images for each age
- Ensure collision detection works consistently across all base types
- Consider whether bases upgrade visually as they take damage

## Dependencies
- Requires Issue 5 (Age Progression System) to be implemented

## Estimated Effort
Medium (5-7 hours)
```

---

## Issue 7: Add Difficulty Level Options

**Labels:** `enhancement`, `gameplay`, `high-priority`

**Title:**
```
Add Difficulty Level Options
```

**Description:**
```markdown
## Priority
High

## Category
Gameplay, Settings

## Description
Implement selectable difficulty levels to accommodate different player skill levels and provide replay value.

## Difficulty Levels

### Easy
- Lower enemy HP (e.g., 75% of normal)
- Lower enemy damage (e.g., 75% of normal)
- More starting gold (e.g., 150 instead of 100)
- Slower enemy spawn rate
- Player earns more gold per kill

### Medium (Default)
- Current balanced gameplay
- Standard values

### Hard
- Higher enemy HP (e.g., 125% of normal)
- Higher enemy damage (e.g., 125% of normal)
- Less starting gold (e.g., 75 instead of 100)
- Faster enemy spawn rate
- Player earns less gold per kill

## Acceptance Criteria
- [ ] Difficulty selection in menu or settings screen
- [ ] Difficulty affects enemy stats appropriately
- [ ] Difficulty affects gold economy
- [ ] Difficulty affects spawn rates
- [ ] Difficulty setting is saved/persisted
- [ ] Visual indicator of current difficulty
- [ ] Balance testing for each difficulty level

## Technical Notes
- Add difficulty setting to game configuration
- Create multipliers for stats based on difficulty
- Store difficulty selection in localStorage or game state
- May want to display difficulty in UI during gameplay
- Consider adding achievements or rewards for harder difficulties

## Dependencies
None

## Estimated Effort
Small (2-4 hours)
```

---

## Issue 8: Implement Song Selection System with In-Game Shop

**Labels:** `enhancement`, `audio`, `medium-priority`

**Title:**
```
Implement Song Selection System with In-Game Shop
```

**Description:**
```markdown
## Priority
Medium

## Category
Audio, Progression

## Description
Create a music selection system where players can purchase and choose from multiple background songs using gold earned from gameplay.

## Acceptance Criteria
- [ ] Multiple background music tracks available
- [ ] Shop interface where players can browse songs
- [ ] Songs can be purchased with leftover gold from completed levels
- [ ] Preview/listen to songs before purchasing
- [ ] Music selection menu accessible from main menu or settings
- [ ] Selected music plays during gameplay
- [ ] Purchased songs are saved/persisted
- [ ] Clear indication of which songs are owned vs. locked
- [ ] Song purchase prices are balanced

## Technical Notes
- Extend existing SoundFX.js or create MusicManager
- Store purchased songs in localStorage
- Integrate with shop system (Issue 11)
- Preload all music files or load on demand
- Consider music file sizes for performance
- Respect existing mute toggle functionality

## Dependencies
- Related to Issue 11 (In-Game Shop System)
- Songs could be themed by age (Issue 5)

## Estimated Effort
Medium (5-7 hours)
```

---

## Issue 9: Design Better Game Title

**Labels:** `branding`, `low-priority`

**Title:**
```
Design Better Game Title
```

**Description:**
```markdown
## Priority
Low

## Category
Branding, UI

## Description
Create a more compelling and memorable game title that better reflects the game's theme and mechanics.

## Current Title
"Stickman"

## Suggested Alternatives to Consider
- "Age of Stickmen"
- "Stickman Evolution Wars"
- "Era Defense"
- "Stickman Ages"
- "Stick Wars: Through the Ages"
- "Evolution War"
- "Base Defense: Age of Stickmen"

## Acceptance Criteria
- [ ] Brainstorm multiple title options
- [ ] Get feedback from team/players
- [ ] Select final title
- [ ] Update title in all locations:
  - [ ] README.md
  - [ ] index.html (page title)
  - [ ] Menu screen
  - [ ] package.json
  - [ ] Any documentation
  - [ ] Favicon/icon if applicable

## Technical Notes
- This is primarily a branding/marketing decision
- Should consider the age progression theme (Issue 5)
- Title should be memorable and searchable
- Consider domain name availability if hosting publicly

## Dependencies
- May want to wait for Issue 5 (Age Progression) implementation to inform title choice

## Estimated Effort
Small (1-2 hours for implementation after decision is made)
```

---

## Issue 10: Implement Dynamic Weather Conditions

**Labels:** `enhancement`, `visuals`, `low-priority`

**Title:**
```
Implement Dynamic Weather Conditions
```

**Description:**
```markdown
## Priority
Low

## Category
Visuals, Gameplay

## Description
Add weather effects to create visual variety and atmosphere. Weather could be cosmetic or potentially affect gameplay.

## Weather Types
- **Clear/Sunny** - Default, good visibility
- **Rain** - Droplets falling, puddles forming
- **Snow** - Snowflakes falling, snow accumulation
- **Fog** - Reduced visibility
- **Storm** - Heavy rain, lightning flashes, darker atmosphere

## Acceptance Criteria
- [ ] Multiple weather conditions implemented
- [ ] Smooth weather transitions
- [ ] Weather effects don't significantly impact performance
- [ ] Weather can be randomly selected for levels or tied to specific levels/ages
- [ ] Weather effects are visually appealing
- [ ] Weather respects the current age theme (e.g., no rain in space for Future Age)

## Optional Gameplay Impact
- [ ] Fog could reduce visibility range
- [ ] Storm could slow unit movement
- [ ] Snow could create slippery terrain

## Technical Notes
- Use Phaser particle systems for weather effects (rain, snow)
- Use overlays or filters for fog
- Consider weather as a level property or random element
- May tie into age themes (Issue 5)
- Keep performance impact minimal

## Dependencies
- Works well with Issue 3 (Background Graphics)
- Could tie into Issue 5 (Age-specific weather)

## Estimated Effort
Medium (4-6 hours)
```

---

## Issue 11: Implement In-Game Shop System

**Labels:** `enhancement`, `ui`, `medium-priority`

**Title:**
```
Implement In-Game Shop System
```

**Description:**
```markdown
## Priority
Medium

## Category
UI, Progression

## Description
Create a shop interface where players can spend gold earned from completing levels to purchase various items, upgrades, and unlockables.

## Shop Items
- New background music tracks (Issue 8)
- Unit upgrades (increased stats)
- Special abilities or power-ups
- Cosmetic items (different unit skins, base decorations)
- Permanent gold multipliers
- Special/rare units

## Acceptance Criteria
- [ ] Shop UI accessible from main menu or between levels
- [ ] Display available items with prices and descriptions
- [ ] Show player's current gold balance
- [ ] Items can be purchased if player has enough gold
- [ ] Purchased items are saved/persisted
- [ ] Visual feedback when purchasing items
- [ ] Clear indication of owned vs. locked items
- [ ] Shop inventory is organized by category

## Technical Notes
- Create ShopScene or shop UI overlay
- Store purchased items in localStorage
- Deduct gold from player balance on purchase
- Track persistent gold across game sessions
- May need economy balancing to ensure gold earning rate supports shop prices
- Consider adding "leftover gold" system mentioned in notes

## Dependencies
- Related to Issue 8 (Song purchases)
- Related to Issue 14 (Special character unlocks)

## Estimated Effort
Medium-Large (6-8 hours)
```

---

## Issue 12: Implement Blocking with Certain Characters

**Labels:** `enhancement`, `gameplay`, `low-priority`

**Title:**
```
Implement Blocking Mechanic for Certain Characters
```

**Description:**
```markdown
## Priority
Low

## Category
Gameplay, Units

## Description
Add a blocking mechanic for specific unit types, allowing them to reduce incoming damage by blocking attacks.

## Blocking Units
- **Spearman** - Medium block effectiveness (e.g., 30% damage reduction)
- **Giant** - High block effectiveness (e.g., 50% damage reduction)
- Potentially other defensive unit types

## Acceptance Criteria
- [ ] Designated units can block attacks
- [ ] Blocking reduces damage based on unit type (30-50% range across different units)
- [ ] Visual indicator when unit is blocking (shield effect, animation)
- [ ] Block mechanic has cooldown or stamina system to prevent constant blocking
- [ ] AI enemies also use blocking when appropriate
- [ ] Balance testing to ensure blocking isn't overpowered
- [ ] Clear feedback to player when blocks occur

## Technical Notes
- Add block state to unit behavior
- Modify damage calculation to account for blocking
- Consider when AI should trigger blocks (e.g., when taking damage, randomly)
- May need block animation (ties into Issue 2)
- Add block cooldown timer to prevent spam
- Consider if blocking affects unit movement/attacks

## Dependencies
- Works well with Issue 2 (Animations for blocking)
- May affect Issue 5 (Age-specific block mechanics)

## Estimated Effort
Medium (4-5 hours)
```

---

## Issue 13: Display Attack Damage Numbers

**Labels:** `enhancement`, `ui`, `medium-priority`

**Title:**
```
Display Attack Damage Numbers
```

**Description:**
```markdown
## Priority
Medium

## Category
UI, Game Feel

## Description
Show floating damage numbers when units take damage to provide clear visual feedback about combat effectiveness and help players understand damage values.

## Acceptance Criteria
- [ ] Damage numbers appear above units when they take damage
- [ ] Numbers are clearly readable
- [ ] Numbers fade out and rise up (or float away) with animation
- [ ] Different colors for different damage types:
  - Normal damage (white or yellow)
  - Critical hits (red or orange) if implemented
  - Special damage (blue or purple) if applicable
- [ ] Numbers don't clutter the screen (appropriate size, duration)
- [ ] Performance is maintained with multiple damage numbers on screen
- [ ] Optional: Toggle to enable/disable damage numbers

## Technical Notes
- Create damage text objects that animate and destroy themselves
- Use Phaser text or bitmap text for performance
- Add to combat/damage calculation code
- Consider object pooling for damage number text objects
- Animation should be smooth but not distracting
- Ensure numbers appear at the correct position relative to unit

## Dependencies
None

## Estimated Effort
Small-Medium (2-4 hours)
```

---

## Issue 14: Unlock Special Bird Characters After Completing Levels

**Labels:** `enhancement`, `gameplay`, `low-priority`

**Title:**
```
Unlock Special Bird Characters After Completing Levels
```

**Description:**
```markdown
## Priority
Low

## Category
Progression, Units

## Description
Add special bird-themed character units that unlock after players complete certain levels (levels 1-4 or after beating level 8, to be clarified).

## Acceptance Criteria
- [ ] Design unique bird-based units with distinct abilities
- [ ] Bird characters have special abilities that differentiate them from regular units
- [ ] Unlock condition is clearly defined (requires clarification - see Questions section)
- [ ] Visual distinction from regular units (bird sprites/appearance)
- [ ] Bird units are balanced with existing units
- [ ] Unlock notification/celebration when birds become available
- [ ] Birds persist as unlocked after achievement

## Bird Character Ideas
- Flying bird (can avoid ground units?)
- Dive-bombing bird (high damage attack)
- Support bird (buffs nearby units)
- Eagle/hawk (strong melee)
- Parrot/crow (ranged attacks)

## Questions to Clarify
- How many bird characters should there be?
- What are their specific abilities?
- Should they cost more gold than regular units?
- Are they available in all ages or specific ages?
- Exact unlock condition: complete levels 1-4, or beat level 8?

## Technical Notes
- Add bird unit types to unit configuration
- Create bird sprites/animations
- Implement unlock system based on level completion
- Store unlock status in persistent storage
- Add to unit selection UI when unlocked
- Balance stats and gold cost appropriately

## Dependencies
- May tie into Issue 5 (Age Progression) for age-appropriate birds
- Related to Issue 11 (Could be shop items instead of level unlocks)

## Estimated Effort
Medium (5-7 hours)
```

---

## Quick Reference Guide

### How to Create These Issues in GitHub

1. Go to https://github.com/lluppesms/stickman/issues/new
2. Copy the **Title** from each section above
3. Copy the **Description** (markdown content) into the issue body
4. Add the suggested **Labels** (you may need to create some custom labels first)
5. Click "Submit new issue"

### Recommended Label Setup

Create these labels in your repository first:
- `high-priority` (red)
- `medium-priority` (yellow)
- `low-priority` (blue)
- `enhancement` (green)
- `audio` (purple)
- `visuals` (pink)
- `gameplay` (orange)
- `ui` (light blue)
- `branding` (gray)
- `experimental` (dark gray)

### Bulk Creation Tips

- You can create issues in the order listed (1-14)
- Or start with high-priority issues first (1, 2, 5, 7)
- Reference related issues in comments using #issue_number after they're created
- Consider creating a milestone called "Game V3" and assign all these issues to it

---

**Total Issues to Create: 14**

Estimated total effort: 65-97 hours across all features
