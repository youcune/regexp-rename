# regexp-rename

は、カレントディレクトリ内のファイル名を正規表現で置き換えできるコマンドラインツールです。 [@youcune's dotfiles](https://github.com/youcune/dotfiles) にも組み込まれています。Rubyで書き直しました。

## 使い方

```
$ rename [options] <PATTERN> <REPLACE>
    -d, --dry-run                    dry run
    -g, --global                     find globally
    -i, --ignore-case                ignore case
    -s, --silent                     rename silently
```

## 例

たとえば以下のように使います。

```
$ ls -l
total 32
-rw-r--r--   1 youcune  staff   269  3 13 08:10 Gemfile
-rw-r--r--   1 youcune  staff  2953  3 13 08:10 Gemfile.lock
-rw-r--r--   1 youcune  staff    54  3 13 08:10 README.md
drwxr-xr-x   3 youcune  staff   102  3 13 08:11 bundle
-rw-r--r--   1 youcune  staff  3501  3 13 08:10 config.rb
drwxr-xr-x  12 youcune  staff   408  3 23 13:14 source
$ rename -d '\.\w+$' ''
Gemfile does not match.
Gemfile.lock -> Gemfile
README.md -> README
bundle does not match.
config.rb -> config
source does not match.
```

