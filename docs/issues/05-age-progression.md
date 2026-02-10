# Issue 5: Implement 4-Age Progression System

## Priority
**High**

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
