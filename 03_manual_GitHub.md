# GitHubにpushを行うやり方  

自分の作成したファイルをローカルレポジトリに登録（commit）後、実際のweb上で自分のアカウントを入力し、GitHubで確認を行うところまでのやり方を説明する。  

今回はREADME.mdのファイルを作成したとする。
* README.mdの作成  

```php:terminal  
touch README.md  
```  
* リポジトリの作成

```php:terminal  
git init  
```  
* ローカルリポジトリに追加  

```php:terminal  
git add .  
```  

* ローカルリポジトリに登録  

```php:terminal  
git commit -m "README.mdの追加"  
```  

* GitHubにpushを行う  
-- リモートリポジトリの登録    

```php:terminal  
git remote origin master "リポジトリのURL"  
```  

-- push  

```php:terminal  
git push origin master   
```  
 
