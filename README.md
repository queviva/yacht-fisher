# scramble
yacht-fisherman array scrambler

[bite here](https://queviva.github.io/scramble/)

this single line:

```
    const yacht = (v, r=[...v]) => v.map(() =>
        r.splice(~~(Math.random() * r.length), 1)[0]
    );
```

will produce a scrambled array _without_ bias

pass it an array `yacht(['a','b','c'])`

this silly thing:
```
    const durstenshuffeld = (org, r=[...org], j) =>
        
        r.map((v, i, $,
            j = ~~(Math.random() * (r.length - i)) + i
        ) => ([v, r[j]] = [r[j], v], v)
        
    );
```
also one line, will produce a _forward running_,
more conventional, durstenshuffeld which does _not_
destroy the original array - incase you
should want such a thing


