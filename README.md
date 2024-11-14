# How to generate a new project for writing embedded rust code for the micro:bit v2
```
cargo generate wubin28/rusty_mb2_template
```

# How to run the code on Ubuntu after generating a new project

## On terminal 1:
```
cd {{project-name}}
cargo embed
```

## On terminal 2:
```
cd {{project-name}}
gdb-multiarch target/thumbv7em-none-eabihf/debug/{{project-name}}
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```