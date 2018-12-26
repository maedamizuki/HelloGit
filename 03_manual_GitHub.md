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
