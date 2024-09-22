## `&`について
コマンドをバックグランドジョブとして使うためのコマンドのこと。
https://eng-entrance.com/linux-basic-background

## `$!`
バックグラウンドで実行された直前のプロセスのプロセス番号を保持する。
https://qiita.com/a_yasui/items/ec4f75b300410af8958d

## `$?`
シェルが最後に実行したコマンドの終了状態を保持している。ほとんどのコマンドは成功時には「０」を返す。

## `&&`について
「&&」はAND制御演算子となっている。
例えば、以下の例では、コマンド1が成功したらコマンド2を実行する。
```bash
$ コマンド1 && コマンド2
```
https://eng-entrance.com/linux-basic-and
