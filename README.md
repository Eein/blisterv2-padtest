# Padtest

All tests are assuming the position of the original PSX controller.

For example, for SNES the B button will be considered X and the Y button will be considered □

Otherwise, they will be noted (for example, NES)

https://github.com/ShendoXT/padtest/releases/tag/1.0

`lsusb`/`dmesg` output can be found [HERE](https://git.sr.ht/~eein/padtest-results/blob/master/diag.txt)

X O □ ∆


## Blister v2

![blisster v2](https://git.sr.ht/~eein/padtest-results/blob/master/blister.png)

*Below, the Bliss/LLAPI port is the weird HDMI-like Bliss-Box port on the above board.*

### Keyboard in normal port
Everything seems to map, but its acting as if its in turbo mode

### PS2 Controller on Bliss/LLAPI port
Controller does not register as analog, so some mappings may be missing

`# BLISS-BOX 4-PLAY(GP)PORT.1 (type = 0, guid = 03000000d0160000040d000010010000)
03000000d0160000040d000010010000,BLISS-BOX 4-PLAY(GP)PORT.1,a:b0,b:b1,x:b2,y:b3,back:b4,start:b5,leftstick:b14,rightstick:b15,leftshoulder:b6,rightshoulder:b7,dpup:h0.1,dpdown:h0.4,dpleft:h0.8,dpright:h0.2,leftx:a0,lefty:a1,rightx:a3,righty:a4,lefttrigger:b8,righttrigger:b9,platform:Linux,`

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

### Super Famicom/SNES on Bliss/LLAPI port

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

`03000000830500006020000010010000,iBuffalo SNES Controller,a:b1,b:b0,back:b6,dpdown:+a1,dpleft:-a0,dpright:+a0,dpup:-a1,leftshoulder:b4,rightshoulder:b5,start:b7,x:b3,y:b2,hint:SDL_GAMECONTROLLER_USE_BUTTON_LABELS:=1,platform:Linux,`

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

### NES on Bliss/LLAPI port

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

### Pokken Tournament (Switch) Controller on USB port

`030000000d0f00009200000000016800,Hori Pokken Controller,a:b1,b:b0,back:b4,dpdown:b12,dpleft:b13,dpright:b14,dpup:b11,guide:b5,leftshoulder:b9,leftstick:b7,lefttrigger:a4,leftx:a0,lefty:a1,rightshoulder:b10,rightstick:b8,righttrigger:a5,rightx:a2,righty:a3,start:b6,x:b3,y:b2,misc1:b15,platform:Linux,`

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

