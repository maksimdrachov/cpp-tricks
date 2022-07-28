# C++ Tricks

1. Analysing `.o` files

[source: undefined reference to vtable](https://stackoverflow.com/questions/3065154/undefined-reference-to-vtable)

```
nm -C CGameModule.o | grep CGameModule::
```

Will list the methods that are defined, assuming your entire class implementation goes into the logical object file.

You can compare that with what is defined as virtual to figure out what you missed.

The nm command displays information about symbols in the specified File, which can be an object file, an executable file, or an object-file library. If the file contains no symbol information, the nm command reports the fact, but does not interpret it as an error condition. The nm command reports numerical values in decimal notation by default.

[More information](https://www.ibm.com/docs/en/aix/7.2?topic=n-nm-command)