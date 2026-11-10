# Space Station Survival 🚀

**COMP2000 – Object Oriented Programming Practices | Team Victory**

A Java Swing space mission simulation where two astronauts travel to Mars, manage limited resources, and explore the Martian surface. The project was developed collaboratively by Team Victory.

## Run the simulation

Requirements: a Java Development Kit (JDK) and a desktop environment that supports Java Swing. No external libraries are needed.

Open a terminal in the folder containing the `.java` files and run:

```bash
javac *.java
java SpaceMissionGame
```

The simulation opens in a graphical window. Follow the instructions displayed in the game to begin and progress through the mission.

## Gameplay

- Prepare and launch the spacecraft, travel through space, and land on Mars.
- Monitor fuel, oxygen, energy, and equipment condition.
- Switch between the two astronauts to use their different abilities.
- Walk and jump on Mars, leave footprints, take photographs, and collect three Mars samples by walking over them.
- Complete the exploration objectives: **three samples and three photographs**.

### Controls

| Key | Action |
| --- | --- |
| **Enter** | Start the mission |
| **Arrow keys** | Move during exploration; adjust landing speed with Up/Down during landing |
| **Space** | Jump during Mars exploration; respond to the space emergency when prompted |
| **Q** | Switch astronauts |
| **P** | Take a photograph as Rain (Photographer) |
| **R** | Repair equipment as Sky (Engineer) |
| **1 / 2 / 3** | Select ECO / NORMAL / BOOST travel mode in space |
| **S / D** | Choose safe / dangerous route when the emergency prompt appears |
| **N** | Restart the mission |

Some controls work only at the relevant mission stage.

## Java design

**Astronaut inheritance:** `Astronaut` is the base class for `Engineer` and `Photographer`, which have different task behaviours.

**State design pattern:** `SurfaceWalker` holds the current `MovementState`. `StandingState`, `WalkingState`, and `JumpingState` implement the movement behaviours and transitions. This separates the walking and low-gravity jumping rules.

**Streams and collectors:** The Mission Resource Report uses `groupingBy()` with `summarizingDouble()` to summarise recorded resource readings. The project also uses a parallel stream for asteroid collision checks.

**Graphical simulation:** `SpaceMissionGame` uses Java Swing to draw the mission and respond to keyboard input.

## My individual contribution — Nimesh Raj Thapa

I focused on astronaut behaviour and Mars exploration, including:

- Astronaut health, oxygen, position, and the Engineer / Photographer roles.
- Switching between astronauts, equipment repairs, and photography.
- Mars walking, low-gravity jumping, footprints, and movement-related oxygen consumption.
- The movement State pattern (`SurfaceWalker` and the movement-state classes).
- The Mission Resource Report using Java streams and collectors.

This is a **team project**; other spacecraft, mission, and simulation features were developed collaboratively by Team Victory.

## Repository and coursework

- **Personal fork:** https://github.com/nimeshrajthapa-ui/Space-Station-Survival-
- **Original team repository:** https://github.com/Miss-shrestha/Space-Station-Survival-
- **Individual development branch:** `Nimesh_branch`

This README documents the simulation. The individual COMP2000 worksheet, UML diagram, and logbook are separate assessment documents.
