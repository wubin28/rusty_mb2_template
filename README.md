# How to run the code on Ubuntu

## On terminal 1:
```
cd <project root>
cargo embed
```

## On terminal 2:
```
cd <project root>
gdb-multiarch target/thumbv7em-none-eabihf/debug/rusty_mb2_template
(gdb) target remote :1337
(gdb) break main
(gdb) continue
(gdb) quit
```