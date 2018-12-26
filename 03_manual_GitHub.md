# GitHubにpushを行うやり方  

自分の作成したファイルをローカルレポジトリに登録（commit）後、実際のweb上で自分のアカウントを入力し、GitHubで確認を行うところまでのやり方を説明する。  

今回はREADME.mdのファイルを作成したとする。
* README.mdの作成  

```ruby:terminal  
touch README.md  
```  
* リポジトリの作成

```ruby:terminal  
git init  
```  
* ローカルリポジトリに追加  

```ruby:terminal  
git add .  
```  

* ローカルリポジトリに登録  

```ruby:terminal  
git commit -m "README.mdの追加"  
```  

* GitHubにpushを行う  

-- リモートリポジトリの登録    

```ruby:terminal  
git remote origin master "リポジトリのURL"  
```  

-- リモートリポジトリの削除  

```ruby:terminal  
git remote rm origin  
```

-- push  

```ruby:terminal  
git push origin master   
```  

* pushを拒否された場合  
--あまりよくわかっていないので理解してから詳しく載せることにする。 よくみるerrorとしては、`failed to push refs to 'URL'`といったエラーである。  

  とりあえず、今のbranchや経歴を探索する。`git branch`や`git graph`で確認。  

調べたところ、方法が2つある。  
1. fetchしてmergeする。  
```ruby:terminal  
git fetch  
git merge origin/master  
```  
内容としては、リモートの変更を要請＋マージを行う。   

2. fetchしてrebaseする。  
```ruby:terminal  
git fetch  
git rebase origin/master  
```  

リモートの変更＋自分の変更を反映

#### それでもpush時にerrorが出る場合  
よくわからず、行なっているので、行うべきではないと思うが、いつも強制的にpushを行なっている。  

```ruby:terminal  
git push origin master --force  
```  
