# scrambiliare
yacht-fisherman array scrambler

[bite here](https://queviva.github.io/scramble/)

this single line:

```
    const yacht = (v, r=[...v]) => v.map(() =>
        r.splice(~~(Math.random() * r.length), 1)[0]
    );
```

will produce a scrambled array _without_ bias;
[find out why!](https://queviva.github.io/scramble/)

this silly thing:
```
    const durstenshuffeld = (v, r=[...v], j) =>
        
        r.map((x, i, _,
            j = ~~(Math.random() * (r.length - i)) + i
        ) => ([x, r[j]] = [r[j], x], x)
        
    );
```
also one line, will produce a _forward running_,
more conventional,  [durstenshuffle!](https://queviva.github.io/scramble/)
which does _not_ destroy the original array - incase you
should want such a thing


