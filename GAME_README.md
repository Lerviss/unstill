# Tank 1990 - Classic Arcade Game

A fully playable Tank 1990 arcade game built with HTML5 Canvas and vanilla JavaScript. This is a single-file game that captures the essence of the classic arcade experience.

## Features

### Gameplay
- **Classic Tank 1990 Mechanics**: Player-controlled tank with enemy AI
- **Multiple Enemy Tanks**: AI-controlled tanks with basic pathfinding and shooting behavior
- **Destructible Environment**: Brick and steel walls that can be destroyed by gunfire
- **Progressive Difficulty**: Increased enemies and game speed with each level
- **Score Tracking**: Points awarded for destroying enemy tanks and completing levels
- **Lives System**: 3 lives per game session

### Controls
- **Arrow Keys** or **WASD**: Move your tank in four directions
- **Spacebar** or **Mouse Click**: Fire bullets at enemies
- **Click Canvas**: Start game or fire bullets

### Game Mechanics
- **Collision Detection**: Accurate collision detection for tanks, bullets, and obstacles
- **Tank Movement**: Smooth tank movement with proper direction handling
- **Bullet Physics**: Fast-moving bullets with lifetime limits
- **Obstacle Damage**: Destructible walls that deteriorate with hits
- **Enemy AI**: 
  - Random movement patterns
  - Occasional direction changes
  - Basic shooting behavior
  - Progressive difficulty per level

## Technical Details

### Architecture
- **Rendering**: HTML5 Canvas 2D context
- **Game Loop**: `requestAnimationFrame` for smooth 60 FPS gameplay
- **Game States**: Start, Playing, Game Over
- **Object-Oriented Design**: Tank, Bullet, and Obstacle classes

### Key Classes

#### Tank Class
- Properties: Position, velocity, direction, health
- Methods: `update()`, `shoot()`, `canMove()`, `draw()`
- Supports both player and AI tanks

#### Bullet Class
- Properties: Position, direction, lifetime
- Methods: `update()`, `isOutOfBounds()`, `draw()`
- Automatic cleanup when out of bounds

#### Obstacle Class
- Properties: Position, dimensions, type (brick/steel), health
- Methods: `damage()`, `draw()`, `isAlive()`
- Two types: Destructible bricks and durable steel walls

### Game Loop
1. **Update Phase**: Process input, update entity positions, check collisions
2. **Render Phase**: Clear canvas, draw obstacles, tanks, and bullets
3. **Logic Phase**: Handle level progression, enemy spawning, game state

## Responsive Design

The game is fully responsive and adapts to different screen sizes:
- **Desktop**: Optimized for 1024x768 and larger displays
- **Tablet**: Touch-friendly controls with click-to-shoot
- **Mobile**: Scaled canvas and adjustable UI for smaller screens

## Installation

### Direct Play
1. Open `tank1990.html` in any modern web browser
2. Click "Start" or press Spacebar to begin
3. Use arrow keys or WASD to move
4. Press spacebar or click to shoot

### Web Server Deployment
1. Copy `tank1990.html` to your web server
2. Access via: `http://your-domain/tank1990.html`

### Cloudflare Pages Deployment
1. Add `tank1990.html` to your Pages project
2. Access via: `https://your-pages-domain/tank1990.html`

## Game Rules

- **Objective**: Destroy all enemy tanks to progress to the next level
- **Lives**: You start with 3 lives. Losing contact with enemy fire costs 1 life
- **Scoring**: 
  - 100 points per enemy tank destroyed
  - 500 bonus points for completing a level
- **Game Over**: When you lose all lives, the game ends with your final score

## Game Balance

- **Player Tank**: Speed 2.5 pixels/frame, responsive controls
- **Enemy Tanks**: Speed 1.5 pixels/frame, 2-5 enemies depending on level
- **Bullets**: Speed 4 pixels/frame, 200ms fire rate cooldown
- **Level Progression**: Enemies increase by 1 (capped at 5) per level

## Browser Compatibility

Tested and working on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (Chrome, Safari, Firefox)

## Performance

- Smooth 60 FPS gameplay
- Efficient collision detection using AABB (Axis-Aligned Bounding Box)
- Canvas rendering optimized for modern browsers
- Minimal memory footprint

## Future Enhancements

Possible improvements for future versions:
- Sound effects and background music
- Power-ups (rapid fire, shields, etc.)
- Multiple tank types with different abilities
- Tank-to-tank collisions
- Bonus items and special events
- High score persistence with localStorage
- Difficulty settings
- Mobile touch controls optimization

## Code Quality

- Clean, readable code with meaningful variable names
- Object-oriented design patterns
- Proper event handling and input management
- Modular function structure
- No external dependencies

## License

This game is provided as-is for educational and entertainment purposes.

## Credits

Tank 1990 - Classic Arcade Game Recreation
Built with HTML5 Canvas and Vanilla JavaScript
