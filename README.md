# kglow

Bytepatches the memory of Counter-Strike: Global Offensive in kernel space, causing the spectator glow effect to appear at all times. Can be toggled in-game with the `spec_show_xray` console variable.

## Usage

Compile and load into kernel with insmod or modprobe. Be sure to pass valid values for the `patch_offset` and `patch_size` module arguments. You can read a guide on finding these values [here](https://aixxe.net/2017/06/kernel-game-hacking).

```
# insmod kglow.ko patch_offset=13034343 patch_size=6
```

To trigger the bytepatching, simply read from /proc/kglow. It's best to do this from the main menu.

```
$ cat /proc/kglow
```


## Demonstration

[![Video](http://img.youtube.com/vi/XrPQHVXB8i0/0.jpg)](https://www.youtube.com/watch?v=XrPQHVXB8i0)

## References

* [CanSeeSpecOnlyTools Patch ESP proof-of-concept](https://www.unknowncheats.me/forum/counterstrike-global-offensive/218398-canseespeconlytools-patch-esp-proof-concept.html)