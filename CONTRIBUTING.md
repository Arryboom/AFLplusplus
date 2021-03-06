# How to submit a Pull Request to AFLplusplus

Each modified source file, before merging, must be formatted.

```
make code-formatter
```

This should be fine if you modified one of the files already present in the
project, otherwise run:

```
./.custom-format.py -i file-that-you-have-created.c
```

Regarding the coding style, please follow the AFL style.
No camel case at all and use the AFL's macros when possible (e.g. WARNF, FATAL, ...).

Remember that AFLplusplus has to build and run on many platforms, so generalize your Makefiles (or your patches to our pre-existing Makefiles) to be as much general as possible.
