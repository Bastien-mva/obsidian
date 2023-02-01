devices:
# change this to a keyboard device
- "/dev/input/by-path/pci-0000:00:14.0-usb-0:2.3:1.0-event-kbd" 
- "/dev/input/by-path/pci-0000:00:14.0-usb-0:2.2.3:1.0-event-kbd"
- "/dev/input/by-path/platform-i8042-serio-0-event-kbd"
### the above keyboard is the left keyboard
# this is executed when mouseless starts
# startCommand: ""
# the default speed for mouse movement
baseMouseSpeed: 600.0
# the default speed for scrolling
baseScrollSpeed: 20.0
layers:
# the first layer is active at start
- name: initial
  bindings:
    # when tab is held and another key pressed, activate mouse layer
    tab: tap-hold-next tab ; toggle-layer mouse ; 500
    # when a is held for 300ms, activate mouse layer
    a: tap-hold a ; toggle-layer mouse ; 300
    t: tap-hold t ; toggle-layer arrows ; 300
    # right alt key toggles arrows layer
    # switch escape with capslock
# a layer for mouse movement
- name: mouse
  # when true, keys that are not mapped keep their original meaning
  passThrough: true
  bindings:
    # quit mouse layer
    esc: layer initial
    # keep the mouse layer active
    d: speed 3.0 
    r: reload-config
    l: move  1  0
    j: move  0  1 
    k: move  0 -1
    h: move -1 0 
    p: scroll up
    n: scroll down
    s: speed 0.37
    o: scroll left
    b: scroll right
    f: button left
    r: button right
    # move to the top left corner
    k0: "exec xdotool mousemove 0 0"
# another layer for arrows and some other keys
- name: arrows
  passThrough: true
  bindings:
    h: left 
    j: down
    k: up
    l: right
    i: esc
    u: backspace
    o: delete



