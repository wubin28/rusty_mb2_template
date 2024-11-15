# An embedded Rust project template for the micro:bit v2

## How to generate a new project
```
cargo generate wubin28/rusty_mb2_template
```

## How to run the code

### On Ubuntu and macOS:
```
cargo run
```

### On Windows 11:
```
cargo run --probe <VID:PID:SN>
```

## How to debug the code on Ubuntu

### On terminal 1:
```
cd {{project-name}}
cargo embed
```

### On terminal 2:
```
cd {{project-name}}
gdb-multiarch target/thumbv7em-none-eabihf/debug/{{project-name}}
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```

## How to debug the code on macOS

### On terminal 1:
```
cd {{project-name}}
cargo embed
```

### On terminal 2:
```
cd {{project-name}}
arm-none-eabi-gdb target/thumbv7em-none-eabihf/debug/{{project-name}}
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```

## How to debug the code on Windows 11

### On PowerShell 1:
```
cd {{project-name}}
cargo embed --probe <VID:PID:SN>
```

### On PowerShell 2:
```
cd {{project-name}}
arm-none-eabi-gdb target/thumbv7em-none-eabihf/debug/{{project-name}}
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```