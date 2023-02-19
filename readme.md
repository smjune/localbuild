```
## create hugo project
$ hugo new site localbuild  
$ cd localbuild  

## git init
localbuild $ git init  

## add theme as a submodule
localbuild $ git submodule add https://github.com/alex-shpak/hugo-book themes/hugo-book  
**update baseURL and theme of config.toml**

## create a page 
localbuild $ cp -R themes/hugo-book/exampleSite/content.en/* ./content  

## push source (hugo project) repo
localbuild $ git remote add origin https://github.com/smjune/localbuild.git  
localbuild $ git add .  
localbuild $ git commit -m 'initiate project'  
localbuild $ git push origin main  

## add submodule to deploy public folder  
localbuild $ git submodule add https://github.com/smjune/Webdoploy.git public  

## build hugo project
localbuild $ hugo

## upload public 
localbuild $ cd public
localbuild/public $ git add .
localbuild/public $ git commit -m 'first deploy'
localbuild/public $ git push 
localbuild/public $ cd ..
localbuild $

## workflow
1. update pages
2. build on                      (localbuild)
3. add/commit/push public folder (localbuild/public)
4. add/commit/push hugo project  (localbuild) ( echo 'public/' >> .gitignore )


```

[public submodule 오류](https://stackoverflow.com/questions/12218420/add-a-submodule-which-cant-be-removed-from-the-index/39189599)
