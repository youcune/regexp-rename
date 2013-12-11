# regexp_rename

## これは何？

カレントディレクトリ内のファイル名を正規表現で置き換えできます。

## 注意

あまりセキュリティ考えずに eval するので、外から悪意のありそうな人が実行することのないようにしてください。

## 使い方

```
$ rename.pl [-dgis] PATTERN REPLACE
  -d: dry run
  -g: find globally
  -i: ignore case
  -s: rename silently
```

