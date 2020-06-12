# Ender 5

Based off notes from (here)[http://www.do-it-neat.com/install-marlin-1-1-9-at-your-creality-ender-5/]

Remeber to add:

```
compiler.c.extra_flags=-fno-tree-scev-cprop -fno-split-wide-types -Wl,--relax -mcall-prologues
compiler.cpp.extra_flags=-fno-tree-scev-cprop -fno-split-wide-types -Wl,--relax -mcall-prologues
compiler.c.elf.extra_flags=-Wl,--relax
```

Initially I did not, the bootloader got corrupted during write (I suspect regions of flash were overwritten because firmware was too big). Needed to reinstall bootloader a few times before got it to fit (and work).

Includes ABL switch (FreeABL) from (here)[https://www.thingiverse.com/thing:3468254]
