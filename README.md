# grepper
```
usage: grepper [-h -c -v -q -l -ic]
                      [-fm|--filemtime +n | n | -n] [-fmm|--filemmin +n | n | -n]
                      [-fi|--fileignore expression] [-fe|--fileexpression expression] 
                      [-fn|--filename name] [-fs|--filesuffix suffix]
                      [-i|--ignore expression] [-e|--expression expression] path...
parameters:
  [options]
  -h|--help                    usageを表示する
  -c|--color                   標準出力時も検索結果に色をつける
  -v|--verbose                 冗長出力する
  -q|--quiet                   出力しない
  -l|--link                    シンボリックリンクを対象にする
  -ic|--ignorecase             大文字小文字を区別しない
  -esc|--escapecsv             csvファイルをエスケープする
  [file path search options]
  -fm|--filemtime              +n日以前に更新された|n日前に更新された|-n日前までに更新された
  -fmm|--filemmin              +n分以前に更新された|n分前に更新された|-n分前までに更新された
  -fi|--fileignore             無視（正規表現）             \|=or
  -fe|--fileexpression         検索（正規表現）             \,=and \|=or
  -fif|--fileignorefixed       無視（正規表現なし）         \|=or
  -fef|--fileexpressionfixed   検索（正規表現なし）         \,=and \|=or
  -fn|--filename               ファイル名(ワイルドカード)   \|=or
  -fs|--filesuffix             ファイルのサフィックス       \|=or
  [file content search options]
  -i|--ignore                  無視（正規表現）             \|=or
  -e|--expression              検索（正規表現）             \,=and \|=or
  -if|--ignorefixed            無視（正規表現なし）         \|=or
  -ef|--expressionfixed        検索（正規表現なし）         \,=and \|=or
  [target]
  path                        検索対象パス                  \|=or
return:
  0: hit 検索hitした
  3: miss 検索hitしなかった
  6: error エラーが発生した
examples:
  grepper -v -fi "\.git\|/target/\|\.DS_Store" -fe "\.sh$" -e export .
```
