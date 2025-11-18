# FERN-STYLE PRODUCTION GUIDE
## For 3D Artists: Complete Workflow

**Your Advantage**: You have 3D skills - this is 80% of what Fern does  
**This Guide**: Step-by-step production pipeline for "The Crypto King"

---

## PART 1: SOFTWARE STACK

### PRIMARY TOOLS (Choose Your Weapon)

**3D SOFTWARE OPTIONS:**

**Option A: Blender (FREE - Recommended)**
```
WHY BLENDER:
✅ Free and open source
✅ Powerful rendering (Cycles/Eevee)
✅ Built-in compositing
✅ Good for photorealism
✅ Active community
✅ Can do everything Fern needs

BLENDER PIPELINE:
1. Model scenes/objects
2. Light with area lights + HDRIs
3. Render with Cycles (quality) or Eevee (speed)
4. Composite in Blender's compositor
5. Export for After Effects
```

**Option B: Cinema 4D**
```
WHY C4D:
✅ Industry standard for motion graphics
✅ Intuitive interface
✅ Great for product visualization
✅ Octane/Redshift integration
✅ Smooth After Effects workflow

C4D PIPELINE:
1. Model in C4D
2. Light with Octane/Redshift
3. Render passes
4. Export to After Effects
5. Composite and animate
```

**Option C: Unreal Engine 5 (FAST)**
```
WHY UNREAL:
✅ Real-time rendering (HUGE time saver)
✅ Photorealistic Lumen lighting
✅ Film-quality output
✅ Virtual camera system
✅ Free for video production

UNREAL PIPELINE:
1. Import assets
2. Build scenes
3. Light with Lumen
4. Virtual camera cinematics
5. Render in real-time
6. Export sequences
```

### SUPPORTING SOFTWARE:

**After Effects** (Essential)
- Motion graphics
- Text animations
- Compositing layers
- Final assembly

**Premiere Pro** (Essential)
- Timeline editing
- Audio sync
- Final cut

**DaVinci Resolve** (Essential)
- Color grading
- Final polish
- Export

**Substance Painter** (Optional)
- Texture creation
- PBR materials
- Realistic surfaces

**Photoshop** (Essential)
- Graphic design
- Photo manipulation
- Textures

---

## PART 2: ASSET PIPELINE

### MODELING STRATEGY

**For "The Crypto King" you need:**

#### CATEGORY 1: Architecture/Environments
```
HOTEL ROOM (Oberoi Rajvilas):
- Model: Simple room geometry
- Detail level: Medium (won't see everything)
- Key elements:
  * Bed (just shapes, won't see detail)
  * Window frame (important - light source)
  * Door
  * Walls with texture
- Time: 2-3 hours
- Poly count: 50k-100k total

HOSPITAL CORRIDOR:
- Model: Straight corridor
- Detail level: Low-medium
- Key elements:
  * Walls with panels
  * Ceiling lights (practical models)
  * Floor tiles
  * Door at end
  * Simple props (fire extinguisher, signs)
- Time: 1-2 hours
- Poly count: 30k-50k

MANSION INTERIOR:
- Model: Single room
- Detail level: Medium
- Key elements:
  * Furniture (covered in sheets)
  * Window
  * Walls
  * Floor
- Time: 2-3 hours
- Poly count: 75k-100k

TIP: Use kitbash libraries
- Get pre-made assets
- Modify for your needs
- Sites: Gumroad, TurboSquid, CGTrader
- Or: Blender Asset Library, Quixel Megascans
```

#### CATEGORY 2: Hero Objects
```
LAPTOP (Gerald's evidence):
- Model: Detailed laptop
- Detail level: High (will be close-up)
- Key elements:
  * Accurate proportions
  * Keyboard detail
  * Screen (emissive material)
  * Apple or generic logo
- Time: 3-4 hours OR buy model ($10-30)
- Poly count: 200k-500k (it's hero object)

BITCOIN COIN (Title sequence):
- Model: Detailed coin both sides
- Detail level: Very high (extreme close-up)
- Key elements:
  * BTC logo engraved
  * Surface scratches/wear
  * Edge ridges
  * Reflective material
- Time: 2-3 hours
- Poly count: 500k-1M (with subdivision)

SMARTPHONE (Reddit scenes):
- Model: iPhone or generic
- Detail level: Medium-high
- Key elements:
  * Screen (emissive)
  * Camera bump
  * Buttons
- Time: 2 hours OR buy model
- Poly count: 100k-300k
```

#### CATEGORY 3: Vehicles (If needed)
```
YACHT:
- Option A: Buy model ($50-100)
- Option B: Stock footage + 3D text overlay
- Option C: Simple 3D shape from distance
- Recommendation: BUY - too complex to model

CESSNA PLANE:
- Same as yacht: BUY or stock footage
- If modeling: 10+ hours for quality
- Better: Use stock footage + graphics
```

### TEXTURING STRATEGY

**PBR WORKFLOW (Physically Based Rendering):**

```
FOR EVERY MATERIAL YOU NEED:
1. Base Color (Albedo)
2. Roughness map
3. Metallic map (if metal)
4. Normal map (surface detail)
5. (Optional) Displacement/Height

WHERE TO GET TEXTURES:
- Quixel Megascans (free with Unreal)
- Poliigon (subscription)
- Substance Source (subscription)
- CGTrader (free/paid)
- Make your own in Substance Painter

FERN'S MATERIAL STYLE:
- Slightly worn (not pristine)
- Realistic imperfections
- Good reflections
- Proper metalness
- Dust/dirt in crevices
```

---

## PART 3: LIGHTING TECHNIQUES (The Critical Part)

### FERN'S LIGHTING PHILOSOPHY

**RULE #1: Single Dominant Source**
Every scene has ONE main light. Everything else is fill/ambient.

**RULE #2: High Contrast**
Ratio: 1:16 or higher (key to fill)
Blacks should be BLACK
Whites should be WHITE
Minimal mid-tones

**RULE #3: Motivated Lighting**
Every light has a source:
- Window → Sun
- Lamp → Practical
- Screen → Emissive material
- Ceiling → Overhead fixture

**RULE #4: Color Temperature Matters**
- Warm (2700K-3200K) = Past, safe, comfortable
- Cool (5000K-7000K) = Present, clinical, sad
- Blue = Night, technology, cold
- Orange = Fire, danger, urgency

### LIGHTING SETUPS BY SCENE TYPE

#### SETUP 1: Hotel Room (Dawn Light)
```
BLENDER SETUP:

PRIMARY LIGHT:
- Type: Area Light (large, 2m x 3m)
- Position: Outside window, angled 45°
- Color: Warm orange (sunrise, 2800K)
- Strength: 500W
- Purpose: Simulates dawn sun

SECONDARY (Fill):
- Type: Area Light (small, 0.5m x 0.5m)
- Position: Bathroom doorway
- Color: Warm white (2700K)
- Strength: 25W (1/20th of primary)
- Purpose: Practical bathroom light

ENVIRONMENT:
- HDRI: Sunrise sky (low on horizon)
- Strength: 0.2 (subtle)
- Purpose: Ambient fill, reflections

ATMOSPHERE:
- Volumetric fog: Light density
- Purpose: Make light beams visible

MATERIALS:
- Curtain: Translucent (light passes through)
- Window glass: Slight tint
- Walls: Slight roughness (0.6-0.7)

ANIMATION:
- Key 0s: Light strength 200W, color 4000K (pre-dawn)
- Key 5s: Light strength 500W, color 2800K (sunrise)
- Key 10s: Light strength 800W, color 3200K (full morning)
- Purpose: Shows time passing via light change
```

#### SETUP 2: Hospital Corridor (Fluorescent)
```
BLENDER SETUP:

PRIMARY LIGHTS:
- Type: Area Lights (rectangular, 0.2m x 1.5m)
- Count: 8-10 lights (overhead, in line)
- Pattern: Every other light ON
- Color: Cool white (5000K)
- Strength: 100W each
- Purpose: Institutional fluorescent

KEY TECHNIQUE - Light ON/OFF animation:
- Lights 1,3,5,7,9: Always ON
- Lights 2,4,6,8,10: ON at start
- Animation: Lights 2,4,6,8,10 fade to OFF
- Timing: One by one, 0.5s apart
- Final state: Only 1,3,5,7,9 remain
- End: All lights OFF (death moment)

ENVIRONMENT:
- HDRI: None (interior)
- Ambient: Near black (0.05)

ATMOSPHERE:
- Volumetric fog: Medium density
- Purpose: Light tubes visible in haze

CAMERA ANIMATION:
- Start: End of corridor
- End: OR door
- Movement: Linear dolly, 15 seconds
- Speed: 1 foot per second
- Smooth: Constant velocity

LIGHTING SYNCED TO CAMERA:
- As camera passes each light, that light dims
- Creates: "Lights going out behind you" feel
- Ominous, inevitable, death approaching
```

#### SETUP 3: Screen Glow (Reddit Scene)
```
BLENDER SETUP:

PRIMARY LIGHT:
- Type: Emissive plane (monitor screen)
- Size: 24" monitor (0.53m x 0.30m)
- Color: Cool blue (7000K)
- Strength: Varies by content
  * Bright content: 10W
  * Dark content: 3W
- Purpose: Only light source in scene

ANIMATION - Content Changes:
- Screen shows Reddit page (image texture)
- Texture changes: Different posts appear
- Each change = slight brightness flicker
- Frequency: Every 1-2 seconds
- Purpose: Anxiety, information overload

ENVIRONMENT:
- Completely black (no HDRI)
- Ambient: 0.0
- Purpose: Screen is ONLY light

MATERIALS NEARBY:
- Desk surface: Slight gloss (reflects screen)
- Keyboard: Matte (catches side light)
- Wall behind: Matte white (shows blue cast)

CAMERA:
- Start: Wide shot (monitor in environment)
- End: Close on screen (fills frame)
- Movement: Slow push-in, 15 seconds
- Purpose: Drawing viewer into panic

ATMOSPHERE:
- No volumetrics (screen light doesn't scatter)
- Clean, digital feel
```

#### SETUP 4: Silhouette Figure (Control Room)
```
BLENDER SETUP:

BACKGROUND LIGHT:
- Type: Emissive plane (large, 4m x 3m)
- Position: Behind figures (projection screen)
- Content: Flight path diagram (animated texture)
- Color: White with graphics
- Strength: 50W
- Purpose: Backlight for silhouettes

MONITOR LIGHTS:
- Type: Emissive planes (0.5m x 0.3m each)
- Count: 5 (one per workstation)
- Color: Blue (6000K)
- Strength: 5W each
- Purpose: Secondary fill, blue glow

FIGURES:
- Models: Simple human shapes OR
- Real footage: Green screen silhouettes
- Position: Seated at workstations
- Animation: Minimal (slight head turns)
- Material: Matte black (absorbs light)

KEY TECHNIQUE:
- NO front light on figures
- They stay pure silhouettes
- Readable only by outline
- Body language tells story

CAMERA:
- Position: Locked, facing screen
- No movement (creates tension via stillness)

ANIMATION:
- Screen content changes (flight path updates)
- Time indicator counts up: 9:35 → 9:40
- Small figure movements (mouse clicks, head turns)
- Blue monitors flicker slightly
```

#### SETUP 5: Object in Void (Bitcoin Coin)
```
BLENDER SETUP - Title Sequence:

ENVIRONMENT:
- Pure black (no HDRI)
- Ambient: 0.0

PRIMARY LIGHT:
- Type: Area Light (large, 2m x 2m)
- Position: Starts left of coin
- Color: Warm gold (3000K)
- Strength: 200W
- Purpose: Dramatic side light

SECONDARY LIGHT:
- Type: Area Light (small, 0.5m x 0.5m)
- Position: Top, slightly behind
- Color: Cool white (5500K)
- Strength: 50W
- Purpose: Rim light, separation from black

ANIMATION - "Light Passing Over Time":
Frame 0-120 (5 seconds):
- Light position: Rotates around coin
- Start: 90° left
- End: 90° right
- Movement: Smooth arc
- Purpose: Reveals different coin details
- Shadows move across surface
- Creates: Time passing feeling

COIN MATERIAL:
- Base: Gold metal
- Roughness: 0.3 (semi-polished)
- Scratches: Normal map
- Tarnish: Dirt mask in crevices
- Logo: Bump map for depth

CAMERA:
- Start: Wide (coin small in frame)
- End: Extreme close-up (coin fills frame)
- Movement: Slow push-in (5 seconds)
- Combined with light rotation
- Creates: Discovery, examination

FINAL MOMENT:
- Light dims to near-black
- Just rim light remains
- Title appears over darkening coin
- "THE CRYPTO KING"
```

---

## PART 4: RENDERING STRATEGY

### RENDER SETTINGS (Blender Cycles)

```
QUALITY SETTINGS:
Samples: 512-1024 (higher for stills)
Bounces: 
  - Max: 12
  - Diffuse: 4
  - Glossy: 4
  - Transmission: 8
  - Volume: 2

RESOLUTION:
- 1920x1080 (HD) OR
- 3840x2160 (4K - if you can)
- Aspect: 16:9
- Frame rate: 24fps (cinematic)

MOTION BLUR:
- Enable: Yes
- Shutter: 0.5
- Purpose: Smooth movement, cinematic

DENOISING:
- Enable: Yes (Intel Open Image Denoise)
- Purpose: Faster renders, clean result
```

### RENDER PASSES (For Compositing)

```
ESSENTIAL PASSES:
1. Beauty (final render)
2. Ambient Occlusion (depth/crevices)
3. Shadow (separate shadow pass)
4. Emission (glowing screens)
5. Mist (depth fog)
6. Z-depth (focus effects in post)

ADVANCED PASSES:
7. Diffuse Direct
8. Diffuse Indirect
9. Glossy Direct
10. Glossy Indirect

WHY PASSES:
- Adjust lighting in post
- Fix problems without re-render
- Add effects (bloom on screens)
- Depth of field in post
- Color grade specific elements
```

### RENDER TIME OPTIMIZATION

```
SPEED TRICKS:

1. RENDER IN SECTIONS:
   - Scene 1-5 today
   - Scene 6-10 tomorrow
   - Etc.

2. USE EEVEE FOR TESTS:
   - Preview lighting fast
   - Render Eevee first
   - If good → switch to Cycles
   - Saves hours

3. RENDER LOWER RES FIRST:
   - Test at 720p
   - Check lighting/composition
   - Only render 1080p/4K when final

4. RENDER OVERNIGHT:
   - Long scenes render while sleeping
   - Wake up to finished frames

5. USE RENDER FARMS (If desperate):
   - SheepIt (free, community)
   - Render Street (paid, fast)
   - Cost: $0.02-0.10 per frame
   - For 5-second shot (120 frames): $2.40-12
```

---

## PART 5: SCENE-BY-SCENE BREAKDOWN

### THE CRYPTO KING - 3D Production Breakdown

#### SCENE 1: Opening - Hotel Dawn (0:00-0:50)

**3D REQUIREMENTS:**
```
MODELS NEEDED:
- Hotel room interior (simple)
- Bed with figure (silhouette or simple model)
- Window frame
- Door

TEXTURES:
- Wall paint (slightly textured)
- Bedsheet (fabric, wrinkled)
- Window glass (slight tint)
- Floor tiles

LIGHTING SETUP:
- Sunrise through window (area light, animated brightness)
- Bathroom practical (small area light)
- HDRI environment (dawn sky)
- Volumetric atmosphere

CAMERA ANIMATION:
Shot 1: Outside building
- Virtual camera descending
- 15 seconds, smooth
- Approach window 147

Shot 2: Inside room
- Slow push toward figure on bed
- 15 seconds
- Figure remains still (silhouette)

Shot 3: Close-up
- Hand on stomach
- Macro lens effect (shallow DOF)
- Hold 5 seconds

RENDER TIME ESTIMATE:
- 3 shots × 15 seconds = 45 seconds total
- At 24fps = 1,080 frames
- At 5 min/frame (Cycles) = 90 hours
- Solution: Render overnight for 4 nights OR use Eevee (4 hours)
```

#### SCENE 2: Airplane Sequence (If Needed)

**3D REQUIREMENTS:**
```
MODELS NEEDED:
- None! Use stock footage OR
- Buy 3D airplane model ($50-100)
- Cloud environment (volumetrics OR stock)

IF USING 3D:
LIGHTING:
- Sun light (directional, from above)
- Sky dome (HDRI with clouds)
- Plane material (painted metal, slight wear)

CAMERA:
- Orbital around plane
- Slow, cinematic
- 30-second shot

RENDER:
- 720 frames
- Beautiful but time-consuming
- Alternative: Use stock footage of airplane
- Composite crypto graphics over it

RECOMMENDATION:
- Use stock footage
- Add "QUADRIGACX" logo on plane via 3D text
- Composite together
- Saves 40+ hours of rendering
```

#### SCENE 3: Computer Screen Reveal (0:50-1:20)

**3D REQUIREMENTS:**
```
MODELS NEEDED:
- Laptop (detailed, buy model or make)
- Desk
- Dark room environment

LIGHTING:
- Screen only (emissive material)
- Blue glow on keyboard
- Everything else black

SCREEN CONTENT:
- Not 3D - use After Effects
- Create fake file structure
- "Quadriga_Real_Books" folder
- "Fake_Accounts.xlsx" file
- Animate appearance

CAMERA:
Shot 1: Laptop closed on desk (10 seconds)
- Locked camera
- Dramatic lighting (side light)
- Light changes (sunrise effect)

Shot 2: Laptop opens (2 seconds)
- Simple rig animation in Blender
- Screen light turns on (emissive ramps up)

Shot 3: Push into screen (8 seconds)
- Virtual camera slow push
- Screen content becomes readable
- Blue glow intensifies

RENDER TIME:
- 480 frames
- Laptop is hero object: 10 min/frame
- 80 hours total OR
- Eevee: 8 hours
```

#### SCENE 4: Hospital Corridor (1:35-1:50)

**3D REQUIREMENTS:**
```
MODELS NEEDED:
- Corridor (walls, floor, ceiling)
- Ceiling lights (rectangular fixtures)
- OR door at end
- Simple props (optional)

TEXTURES:
- Hospital tiles (clean, reflective)
- Painted walls (slight dirt/wear)
- Ceiling (acoustic tiles)

LIGHTING - THE KEY PART:
- 10 ceiling lights (area lights)
- Every other ON (pattern)
- Animation: Lights turn OFF one by one
- Final: OR light turns OFF (death)

ATMOSPHERE:
- Volumetric fog (medium)
- Makes light beams visible
- Institutional feel

CAMERA:
- Tracking shot down corridor
- 15 seconds, smooth
- Ends at OR door

SPECIAL EFFECT:
- Light going out = death
- Simple animation (brightness to 0)
- Powerful metaphor

RENDER TIME:
- 360 frames
- Volumetrics slow down render: 8 min/frame
- 48 hours OR
- Eevee: 5 hours
```

#### SCENE 5: Silhouette Control Room (2:05-2:30)

**3D REQUIREMENTS:**
```
MODELS NEEDED:
- Control room (simple)
- Workstations (desks with monitors)
- Large projection screen
- Chairs with figures OR
- Green screen silhouettes composited

LIGHTING:
- Projection screen (large emissive plane)
- 5 monitor screens (small emissive planes)
- NO other lights

SCREEN CONTENT:
- Flight path diagram (After Effects)
- Applied as texture to emissive plane
- Can animate (path extending)

FIGURES:
Option A: Simple 3D models (seated)
- Minimal detail (will be silhouettes)
- Slight animation (mouse movements)

Option B: Film real people on green screen
- Backlit silhouettes
- Composite into 3D scene

CAMERA:
- Locked position (no movement)
- Creates tension through stillness
- Time passing shown via screen changes

TIME INDICATOR:
- "9:35" → "9:40"
- Simple text in After Effects
- Composited over render

RENDER TIME:
- 600 frames (25 seconds)
- Simple scene: 2 min/frame
- 20 hours OR
- Eevee: 2 hours
```

---

## PART 6: COMPOSITING WORKFLOW

### BLENDER COMPOSITOR (Built-in)

```
NODE SETUP FOR TYPICAL SCENE:

INPUT:
[Render Layers]
   ↓
CORRECTIONS:
[Color Balance] → Adjust shadows/midtones/highlights
   ↓
[Curves] → Fine-tune contrast
   ↓
EFFECTS:
[Glare] → Bloom on bright spots (screens, sun)
   ↓
[Lens Distortion] → Slight barrel distortion (realism)
   ↓
DEPTH EFFECTS:
[Defocus] → (Uses Z-depth pass)
   ↓
ATMOSPHERE:
[Mix] → Blend with fog/mist pass
   ↓
OUTPUT:
[Composite] → Final image
[Viewer] → Preview
```

### AFTER EFFECTS WORKFLOW

```
LAYER STRUCTURE:

TOP LAYERS:
- Text overlays (titles, subtitles)
- Graphics (lower thirds, stats)
- Vignette (subtle)

MIDDLE LAYERS:
- 3D renders from Blender
- Adjustment layers (color correction)
- Effects (glow, grain)

BOTTOM LAYERS:
- Background elements
- Solid black (if needed)

EFFECTS STACK (Per Layer):
1. Lumetri Color (color grade)
2. Glow (on screens/lights)
3. Film Grain (subtle, 2-5%)
4. Sharpening (if needed)

ANIMATION:
- Text: Fade in, slide in, type-on
- Graphics: Build on, wipe in
- Transitions: Cross-dissolve (1-2 seconds)
```

---

## PART 7: MOTION GRAPHICS

### GRAPHIC ELEMENTS NEEDED

#### TYPE 1: Lower Thirds
```
AFTER EFFECTS SETUP:

DESIGN:
- Clean, modern sans-serif (Montserrat, Gotham)
- Dark gradient background (subtle)
- White text
- Simple line accent

ANIMATION:
- Slide in from left (0.5s)
- Hold (3-5s)
- Fade out (0.5s)

INFO DISPLAYED:
- Names: "GERALD COTTEN"
- Dates: "DECEMBER 8, 2018"
- Locations: "JAIPUR, INDIA"
- Stats: "$250 MILLION MISSING"

TIMING:
- Appears 2 seconds after person/location appears
- Synced to narration
```

#### TYPE 2: Data Visualizations
```
"WHERE THE MONEY WENT" PIE CHART:

AFTER EFFECTS TECHNIQUE:
1. Create circles (shape layers)
2. Animate trim paths (reveal slices)
3. Color code:
   - Red: Lost through trading
   - Dark red: Lost on exchanges
   - Orange: Personal spending
4. Text labels animate in
5. Numbers count up (expression: 
   n = effect("Slider Control")("Slider");
   Math.round(n)
   )

TIMING:
- Build on over 5 seconds
- Each slice 1 second
- Hold complete 3 seconds

STYLE:
- Clean, minimalist
- No 3D (flat design)
- High contrast on black
```

#### TYPE 3: Timeline Graphics
```
"GERALD'S SCAM HISTORY" TIMELINE:

AFTER EFFECTS:
1. Horizontal line (center)
2. Date markers (vertical lines)
3. Event labels (above/below)
4. Photos (circular, small)

ANIMATION:
- Line draws left to right (3 seconds)
- Markers appear in sequence
- Labels fade in
- Photos pop in

DATES:
- 1998: First HYIP scam
- 2013: Quadriga founded
- 2018: Death in India

COLOR:
- Line: White
- Markers: Gold
- Text: White
- Photos: Color (stands out)
```

#### TYPE 4: Connection Diagrams
```
"MONEY FLOW" DIAGRAM:

AFTER EFFECTS:
1. Node boxes (person/company)
2. Arrow paths connecting
3. Dollar amounts flowing

ANIMATION:
- Boxes appear (stagger, 0.2s apart)
- Lines draw connecting them
- Arrows animate along lines
- Dollar amounts appear at end

STYLE:
- Black background
- White boxes with photos
- Red arrows (money leaving)
- Green text (amounts)

TECHNICAL:
- Use shape layers for arrows
- Trim paths for drawing effect
- Expressions for dollar count-up
```

---

## PART 8: PRACTICAL FILMING (Minimal)

### WHAT YOU NEED TO FILM (Not 3D)

#### GREEN SCREEN SILHOUETTES

```
SETUP:
Equipment:
- Green screen (9ft x 20ft)
- 2x LED panels (backlight only)
- Camera (DSLR/mirrorless)
- Tripod

Lighting:
- Behind subject: 2 large LED panels
- Illuminate green screen evenly
- NO front light on subject
- Subject stays dark (silhouette)

Shoot:
- Actor sits/stands still
- Minimal movement (just body language)
- Multiple takes (different poses)
- 4K resolution (for flexibility)

Purpose:
- Control room figures
- Prison scenes
- Any silhouette needed
- Will composite into 3D scenes
```

#### REAL SCREENS

```
SETUP:
Equipment:
- Monitor/laptop
- Dark room
- Camera locked position

Lighting:
- ONLY the screen
- Everything else black

Content:
- Display Reddit page
- Display fake emails
- Display code/files
- Record screen 30 seconds each

Purpose:
- Real screen glow looks better
- Saves render time
- Can composite into 3D
- Or use as reference for 3D emissive
```

---

## PART 9: COMPLETE PIPELINE (Step-by-Step)

### WEEK 1: PRE-PRODUCTION
```
Day 1-2: Asset Collection
- Download/buy 3D models (laptop, phone, etc.)
- Collect reference images (hotels, hospitals)
- Gather stock footage (if using)
- Collect photos (Gerald, Jennifer, etc.)

Day 3-4: Scene Planning
- Storyboard each shot
- List all 3D scenes needed
- List all graphics needed
- Plan camera moves

Day 5: Practical Shoots
- Film green screen silhouettes
- Record real screens
- Capture any needed footage
```

### WEEK 2-3: 3D PRODUCTION
```
Day 1-3: Modeling
- Hotel room interior
- Hospital corridor
- Mansion interior
- Any needed props

Day 4-6: Texturing
- Apply materials to all models
- PBR workflow
- Test renders

Day 7-10: Lighting
- Set up each scene's lights
- Test different looks
- Animate light changes

Day 11-14: Animation
- Camera movements
- Light animations
- Object animations (laptop opening)
```

### WEEK 4: RENDERING
```
Day 1-7: Render All Scenes
- Render overnight (scenes 1-5)
- Next night (scenes 6-10)
- Continue until all done
- Use Eevee for speed if needed
- Keep Cycles for hero shots only

PARALLEL: Start compositing finished renders
```

### WEEK 5: MOTION GRAPHICS
```
Day 1-3: Create All Graphics
- Lower thirds
- Data visualizations
- Timelines
- Info cards

Day 4-5: Animate Graphics
- Entrance animations
- Build-on effects
- Number count-ups
```

### WEEK 6: COMPOSITING
```
Day 1-3: Composite 3D + Graphics
- Layer in After Effects
- Add text overlays
- Blend everything

Day 4-5: Effects Pass
- Color correction
- Glow effects
- Film grain
- Final polish
```

### WEEK 7: EDITING & SOUND
```
Day 1-3: Edit in Premiere
- Assemble timeline
- Add transitions
- Sync to music
- Add narration (voiceover or AI)

Day 4-5: Sound Design
- Background ambience
- Sound effects
- Music mixing

Day 6: Color Grade
- Final color in DaVinci
- Consistent look throughout

Day 7: Export
- H.264, High quality
- YouTube settings
- Upload
```

---

## PART 10: RENDER FARM STRATEGY (If Needed)

### WHEN TO USE RENDER FARMS

```
USE IF:
- Scene would take 50+ hours
- Deadline approaching
- Complex volumetrics/lighting
- 4K resolution needed

DON'T USE IF:
- Scene is simple (under 10 hours)
- You have time
- Eevee looks good enough
- Budget constrained
```

### RENDER FARM OPTIONS

```
OPTION 1: SheepIt (FREE)
- Community render farm
- You contribute your PC when not using
- Earn points
- Use points for your renders
- Speed: Slow (1-3 days)
- Cost: FREE (but contribute render time)

OPTION 2: Render Street (PAID)
- Professional farm
- Upload .blend file
- Choose quality/speed
- Cost: ~$0.03-0.10/frame
- Speed: Hours to 1 day
- For 5-second shot: $5-25

OPTION 3: AWS/Google Cloud
- Rent virtual machines
- Install Blender
- Render yourself
- Cost: Variable (~$1-3/hour)
- Speed: Fast (many machines)
- Technical: Requires setup
```

---

## PART 11: SHORTCUTS & TIME-SAVERS

### RAPID PRODUCTION TECHNIQUES

```
TECHNIQUE 1: Kitbashing
- Don't model everything from scratch
- Buy asset packs ($10-50 per pack)
- Mix and match
- Modify to fit your needs
- Saves: 60-80% of modeling time

TECHNIQUE 2: HDRI Lighting
- Instead of complex light setups
- Use HDRI environment maps
- Instant realistic lighting
- Free: Polyhaven.com
- Saves: Hours per scene

TECHNIQUE 3: 2.5D (Fake 3D)
- Use photos on planes
- Add depth with parallax
- Cheaper than full 3D
- Works for backgrounds
- Saves: 70% of modeling time

TECHNIQUE 4: Stock Footage
- Don't 3D everything
- Airplanes? Stock footage
- Cities? Stock footage
- Composite 3D elements over it
- Saves: Days of work

TECHNIQUE 5: Eevee Instead of Cycles
- Real-time render engine
- 10-50x faster than Cycles
- Good enough for most shots
- Use Cycles only for hero shots
- Saves: 90% of render time
```

---

## PART 12: QUALITY CHECKLIST

### BEFORE RENDERING (Check Everything)

```
✅ MODELS:
- No holes in geometry
- Normals facing correct direction
- UVs unwrapped properly
- Scale is correct (real-world size)

✅ MATERIALS:
- All textures loading correctly
- PBR values reasonable (roughness 0-1)
- Normal maps oriented right (check bumps)
- Emissive strength appropriate

✅ LIGHTING:
- At least one strong key light
- Shadows falling correctly
- Color temperature makes sense
- Light intensity reasonable (not overblown)

✅ CAMERA:
- Focal length appropriate (35-50mm typical)
- Not distorted (unless intentional)
- Movement smooth (no jerks)
- Frame rate 24fps

✅ RENDER SETTINGS:
- Resolution correct (1080p minimum)
- Samples high enough (512+)
- Denoising enabled
- Motion blur enabled
- Correct frame range

✅ OUTPUT:
- Save location has space (renders are big)
- File format: PNG (for passes) or EXR
- Naming convention consistent
```

---

## PART 13: TROUBLESHOOTING

### COMMON PROBLEMS & SOLUTIONS

```
PROBLEM: Render too noisy
SOLUTION:
- Increase samples (1024+)
- Enable denoising
- Use better lighting (stronger sources)
- Increase light bounces

PROBLEM: Render too dark
SOLUTION:
- Increase light strength
- Add fill light (very low, 1:16 ratio)
- Check HDRI strength
- Adjust exposure in post

PROBLEM: Render takes forever
SOLUTION:
- Lower samples (test at 256)
- Use Eevee instead of Cycles
- Reduce resolution for tests
- Disable volumetrics (test)
- Use render farm

PROBLEM: Materials look wrong
SOLUTION:
- Check normal maps (might be flipped)
- Verify PBR values (metallic 0 or 1, not between)
- Check UV mapping
- Look at reference photos

PROBLEM: Camera movement jerky
SOLUTION:
- Add more keyframes (smoother interpolation)
- Change to "Bezier" interpolation
- Check frame rate (24fps)
- Enable motion blur

PROBLEM: Composition feels flat
SOLUTION:
- Add atmospheric haze
- Use depth of field (shallow DOF)
- Increase light contrast
- Add rim lighting (separation)
- Check camera angle (slightly off-axis better than straight-on)
```

---

## FINAL TIPS FOR SUCCESS

### THE FERN MINDSET

```
1. LESS IS MORE
   - Don't over-detail what camera won't see
   - Simple models with good lighting > Complex models with bad lighting
   - One strong light > Many weak lights

2. LIGHTING IS EVERYTHING
   - Spend 40% of time on lighting
   - Test renders constantly
   - Study how real lights work
   - Reference photos are your friend

3. PLANNING SAVES TIME
   - 1 hour planning = 10 hours saved
   - Storyboard everything
   - Know your shots before opening Blender
   - List all assets needed upfront

4. RENDER SMART
   - Test at low quality first
   - Only do final quality when approved
   - Render in sections (can restart if crash)
   - Render overnight, work during day

5. USE REFERENCES
   - Find photos of similar scenes
   - Match lighting from references
   - Copy camera angles that work
   - Study Fern videos frame-by-frame

6. EMBRACE IMPERFECTION
   - Slightly rough textures look real
   - Perfect = CG-looking
   - Add dust, scratches, variation
   - Imperfection = authenticity
```

---

## YOUR ADVANTAGE

**You have 3D skills = You can make Fern-style videos**

Most documentary creators CAN'T do this because:
- They don't know 3D software
- They can't model, texture, light
- They can't render photorealistic scenes
- They're limited to what they can film

You CAN:
- Build any scene you imagine
- Control every aspect of lighting
- Create impossible camera moves
- Render photorealistic results
- Work from home, no locations needed

**This is your superpower.**

Use it.

---

**Now go make The Crypto King. You have everything you need.**

Timeline: 7 weeks
Cost: $100-500 (models, render farm if needed)
Result: Professional Fern-style documentary

The only thing between you and a finished video is:
- Time
- Effort
- Following this guide

You got this. 🚀
