# SCPmask

本ツールはSCP財団管轄下の█████████より██████████████の旨通達があり、███████████としたものです。
そのため████████████における██████████████████████████████として公開しています。

## Easy installation

```bash
$ git clone https://github.com/kanata2003/SCPFmask
$ cd SCPFmask
$ chmod u+x SCPFmask
$ cp SCPFmask /usr/local/bin/SCPFmask
```

Ubuntu 22.04.2 LTSでの正常動作を確認しています。

## Usage

```bash
$ ./SCPFmask -w メロス melos.txt          # 特定用語のマスク
████████は激怒した。必ず、かの邪智暴虐の王を除かなければならぬと決意した。██████には政治がわからぬ。██████は、村の牧人である。笛を吹き、羊と遊んで暮して来た。けれども邪悪に対しては、人一倍に敏感であった。
$ cat melos.txt |./SCPFmask -c 1-8        # 文字範囲指定によるマスク
████████████████。必ず、かの邪智暴虐の王を除かなければならぬと決意した。メロスには政治がわからぬ。メロスは、村の牧人である。笛を吹き、羊と遊んで暮して来た。けれども邪悪に対しては、人一倍に敏感であった。
$ ./SCPFmask -w メロス -c 18-21 melos.txt # 両方指定可
██████は激怒した。必ず、かの████████の王を除かなければならぬと決意した。██████には政治がわからぬ。██████は、村の牧人である。笛を吹き、羊と遊んで暮して来た。けれども邪悪に対しては、人一倍に敏感であった。
$ cat melos.txt |./SCPFmask -c 1-8|./SCPFmask -w メロス|./SCPFmask -w 敏感 # 組み合わせ可
████████████████████。必ず、かの邪智暴虐の王を除かなければならぬと決意した。██████には政治がわからぬ。██████は、村の牧人である。笛を吹き、羊と遊んで暮して来た。けれども邪悪に対しては、人一倍に████であった。
```

# 既知のプロトコル収容違反

* cオプションによる文字範囲指定の範囲に改行コードが含まれる場合、その改行コードは失われます。
* 一部の古い環境では正常な動作が期待できません。

# Author

[@kanata2003](https://twitter.com/kanata201612)

# SCPF

[SCP財団](http://scp-jp.wikidot.com/)

[A painter and a black cat - SCPmask](https://raintrees.net/projects/a-painter-and-a-black-cat/wiki/SCPFmask)
