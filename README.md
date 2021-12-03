# Padtest

All tests are assuming the position of the original PSX controller.

For example, for SNES the B button will be considered X and the Y button will be considered □

Otherwise, they will be noted (for example, NES)

https://github.com/ShendoXT/padtest/releases/tag/1.0

X O □ ∆


## Blister v2

![blisster v2](https://git.sr.ht/~eein/padtest-results/blob/master/blister.png)

*Below, the LLAPI port is the weird HDMI-like Bliss-Box port on the above board.*

### Keyboard in normal port
Everything seems to map, but its acting as if its in turbo mode

### PS2 Controller on LLAPI port
Controller does not register as analog, so some mappings may be missing

```
X -> X
O -> O
∆ -> ∆
□ -> ?
L1 -> L1
L2 -> L2
R1 -> R1
R2 -> R2
Select -> □
Start -> ?
L3 -> ?
R3 -> ?
Up -> Up
Down -> Down
Left -> Left
Right -> Right
```

### PS3 Controller plugged into USB port
Controller does not activate/work - looks for bluetooth

### PS4 Controller plugged into USB port
Perfect Mapping - Controller does not register as analog

```
X -> X
O -> O
∆ -> ∆
□ -> □
L1 -> L1
L2 -> L2
R1 -> R1
R2 -> R2
Select -> Select
Start -> Start
L3 -> ?
R3 -> ?
Up -> Up
Down -> Down
Left -> Left
Right -> Right
PS button -> opens fpga menu
```

### PS5 Controller plugged into USB port
Perfect mapping - Controller does not register as analog

```
X -> X
O -> O
∆ -> ∆
□ -> □
L1 -> L1
L2 -> L2
R1 -> R1
R2 -> R2
Select -> Select
Start -> Start
L3 -> ?
R3 -> ?
Up -> Up
Down -> Down
Left -> Left
Right -> Right
PS button -> opens fpga menu
```

### Super Famicom/SNES on LLAPI port

```
X -> X
O -> O
∆ -> ∆
□ -> ?
L1 -> L1
L2 -> n/a
R1 -> R1
R2 -> n/a
Select -> □
Start -> ?
L3 -> n/a
R3 -> n/a
Up -> Up
Down -> Down
Left -> Left
Right -> Right
```

### iBuffalo SNES on USB port

```
X -> O
O -> X
∆ -> □
□ -> ∆
L1 -> L1
L2 -> n/a
R1 -> R1
R2 -> n/a
Select -> Select
Start -> Start
L3 -> n/a
R3 -> n/a
Up -> Up
Down -> Down
Left -> Left
Right -> Right
```

### NES on LLAPI port

```
X (b) -> X
O (a) -> O
∆ -> n/a
□ -> n/a
L1 -> n/a
L2 -> n/a
R1 -> n/a
R2 -> n/a
Select -> □
Start -> ?
L3 -> n/a
R3 -> n/a
Up -> Up
Down -> Down
Left -> Left
Right -> Right
```

### Pokken Tournament Controller on USB port
Controller is dpad only

```
X -> O
O -> ?
∆ -> ∆
□ -> X
L1 -> □
L2 -> n/a
R1 -> ?
R2 -> n/a
Select -> L1
Start -> R1
ZL -> L2
ZR -> R2
Up -> Up
Down -> Down
Left -> Left
Right -> Right
```

### XBOX One (PDP offbrand) in USB port
Controller does not work

