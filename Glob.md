### サポートされている Glob

| 特殊文字 | 挙動                                                  |
| -------- | ----------------------------------------------------- |
| \*       | スラッシュ（/）を除く、ゼロ文字以上の文字列にマッチ   |
| \*\*     | スラッシュ（/）を含むて、ゼロ文字以上の文字列にマッチ |
| ?        | 直前に指定した文字に対し、ゼロ文字か一文字にマッチ    |
| +        | 直前に指定した文字に対し、一文字以上でマッチ          |
| []       | 指定した文字範囲のみ含まれる文字列にマッチ            |
| !        | 手前でマッチしたパターンを、「!」以降の定義で否定     |

### Glob の記述例

| パターン        | 挙動                                                            |
| --------------- | --------------------------------------------------------------- |
| go/\*.go        | go ディレクトリ直下で拡張子が go のファイル                     |
| go/\*_/_.go     | サブディレクトリを含めた、go ディレクトリ配下の全 go ファイル   |
| .github/\*ya?ml | .github ディレクトリ直下で、拡張子が yml または yaml のファイル |
| !README.md      | README.md ファイルを除外                                        |