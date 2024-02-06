# scrambiliare
yacht-fisherman array scrambler

[bite here](https://queviva.github.io/yacht-fisher/)

this single line:

```
    const yacht = (v, r=[...v]) => v.map(() =>
        r.splice(~~(Math.random() * r.length), 1)[0]
    );
```

will produce a scrambled array _without_ bias;
[find out why!](https://queviva.github.io/yacht-fisher/)

<img src="yacht.png" width="100px">

this silly thing:
```
    const yacht-stenshuffeld = v =>
        
        v.map((x, i, r,
        
            j = ~~(Math.random() * (r.length - i)) + i
            
        ) => ([x, r[j]] = [r[j], x], x)
        
    );
```
also one line, will produce a _forward running_,
more conventional,
[durstenshuffle](https://queviva.github.io/yacht-fisher/)
which does _not_ destroy the original array - incase you
should want such a thing

[discover why](https://queviva.github.io/yacht-fisher/)



