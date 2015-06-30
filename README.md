# firefly
Electronic firefly


## Lessons

- Verify precise geometry and pinout for any custom Eagle library packages. The firefly v1's uses a CR1220 battery holder, and because I could not find a suitable Eagle footprint I designed my own. I accidentally reversed the polarity, and was only able to make the resulting boards work by soldering the holders on backwards, which in turn required clipping off plastic registration pins that no longer fit their assigned holes.
- Ensure that there are thermal reliefs for all pads that touch a ground plane. The ground end of the firefly v1's CR1220 battery holder is very hard to solder because it requires heating the entire ground plane (and doing so then risks unseating SMT components already mounted using lower-temp reflow.
- Eagle's grid settings can be tricky. Using a 0.1" primary grid when moving a component does not force its position to fall on that grid with respect to the origin, only that movements are constrained to 0.1" increments. Misunderstanding this resulted in a board with test points that aren't all on the same 0.1" grid, and therefore hard to target using pogo pins set in a generic protoboard.
