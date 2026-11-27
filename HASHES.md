# Pre-registered SHA-256 hashes

Recorded on 2026-11-27 (JST), before recruitment opens.

| Item | SHA-256 |
| --- | --- |
| Allocation program (`pilot_allocation.py`) | `d9bdc2977533915597353afcd8d4be4109289b1d3376c2d8fa2dc8ab1ae5daa1` |
| Random seed (`allocation.seed`) | `773786f9beccb2739547ba2790d42d6f799d3e5e64f5d59867ba4408c12f78a4` |

## How the hashes were computed

Each hash is the SHA-256 of the file's bytes after every CRLF is replaced with LF. The values above
were produced by the program's own `hash` subcommand:

```
python scripts/pilot_allocation.py hash --seed <path to allocation.seed> --program scripts/pilot_allocation.py
```

The program is kept in a private repository (commit `a82480da4a1799f731ffe843decc4c6023a00e67`,
git blob `fa608ec7f0e4f3a27621b9a39d01014adab93042`). The seed is 256 bits from Python's
`secrets.token_hex(32)`, written directly to a private storage location and never displayed.

Allocation will be run once with this program and this seed. Any re-run will be recorded with its
reason and reported with the results. The program, the seed and the analysis code will be released
in this repository when the results are published, so that anyone can check them against these
hashes and reproduce the allocation.

## 日本語

募集の開始前（2026-11-27）に記録した、割付プログラムと乱数の種の SHA-256 です。CRLF を LF に置き換えてから計算しました。プログラムと種の中身は、論文の公表時にここで公開します。割付はこのプログラムとこの種で1回だけ行います。
