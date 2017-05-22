title: EmbedJulia On mac

date: 2015-04-13 14:18:09

tags: [julia,mac]
---
when I try embed Julia on mac following the docs on julialang.org, I failed to compile and execute.

right way:

1. set JULIA_DIR=[your julia path]

```
  JULIA_DIR=/Applications/Julia-0.3.7.app/Contents/Resources/julia/
```
2. add more gcc option(rpath)

```
gcc -o emb -I$JULIA_DIR/include/julia -L$JULIA_DIR/lib/julia -Wl,-rpath,"$JULIA_DIR/lib/julia"  -ljulia embjulia.c 
```

3.exec

```
./emb
```