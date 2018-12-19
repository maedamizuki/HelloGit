# 簡単なManual

実際にGitHub内でリポジトリを作成し、自分自身のPCでデータをどのようにGitHubに公開するかを簡単に説明する。

### GitHubにリポジトリを作成する
自分のGitHubのアカウントにログインし、リポジトリを作る。  
Create a new Repository ページにて[Repository name]、[public]をクリックし、[Create repository]をクリックしてレポジトリを作成する。  
作成した際に、そのリポジトリを指定しているURLが表示されるが、その後リポジトリ内に入っているときのURLと同じなので、必要なときに随時コピー[`command + c`]して良い。  
リポジトリのURLは`https://github.com/自分のGitHubのID/リポジトリ名.git`になっている。

### ローカル環境にGitHubに反映するファイルを作成する
次に自分のPC上にローカルリポジトリを作成する。
macOSであれば、ターミナルを開いて自分のHOMEディレクトリに[github]というディレクトリを作る。
```php:terminal
$ mkdir github
$ cd github
$ mkdir gittest
$ cd gittest
$ git init
```

`git init`についてはこれを行うことでローカルリポジトリを作成される。

### 自分の作成したファイル（データ）をローカルリポジトリに登録（commit）する

実際にローカルリポジトリにcommitするやり方を説明する。今回はテキストファイルでこのファイルをローカルリポジトリに登録してみる。
先ほど作った`自分のHOMEディレクトリ/github/gittest/`の場所に、macOSであればテキストエディットというソフトを使用して「Hello git!」と書いたtest.txtを作成する。
```php:terminal
$ touch test.txt
$ open test.txt
```

```php:test.txt
hello git!
```

テキストエディット内でのショートカットは以下の通りである。
|command|内容|  
|`cmmmand+s`|ファイルの保存|  
|`command+w`|ファイルを終了|  
|`command+q`|ソフトの終了|

次にデータ（ファイル）の変更てんをローカルリポジトリに反映させるために、インデックスに追加を行う。
`$ git add test.txt`または`$ git add .`  
上記のコマンドでインデックスに変更点が反映される。
