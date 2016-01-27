title: How to Build Your Personal Blog With Hexo And Github
date: 2015-12-14 18:21:23
categories: SKILLS
tags: 
- HEXO
- HowTo
- WINDOWS
- MAC
description: A Introduction of how I create my personal blog with hexo with github
---

## How to Build Your Personal Blog With Hexo And Github


####	Mission 1 : Install hexo locally

1. Install Node.js from [Node.js](https://nodejs.org/),
after installation, check Node.js version with below command	

		$ node -v
Note, NPM, a package management tool for nodejs would be installed with node.js, check it with below command
		
		$ npm -v
2. If npm is installed, use npm to install hexo, a cool blog framework with javascript

		$ npm install -g hexo
3. Create local folder for hexo, under folder execute below command
 
		$ hexo init
		$ npm install
4. Start hexo server with below command,
		
		$ hexo server
5. Now, open your browser and enter [local url](http://localhost:4000) to see what happened, WOW,  so cool, right?

6. Next, publish your personal site through github.

---

#### Mission 2 : Create your personal blog with github

   _Precondition_
   
0. You have install hexo locally

1. Create a github account if you don't have

2. Create repo with such name accountname.github.io

3. Set up SSH authentication between your computer and your github account with this link

   _Then, we can move on,_ 


1. In your computer, open terminal or shell, go to the hexo folder, and start your first post with below script

		$ hexo new "first post"
2. Generate files

		$ hexo generate
3. Start the hexo sever and check the blog locally
		
4. If everything is good, update below config in config.yml

		deploy: 
		type: github 
		repository: https://github.com/youraccountname/youraccountname.github.io.git #git託管地址 
		branch: master

5. Then we can deploy to remote site

		$ hexo deploy

6. If everything is OK, open browser, enter YourGithubAccountName.github.io


---


#### Mission 3 : Apply other themes

There are lots of hexo themes you can use, and you can also create your own.

1. if you want to use jacmen, demo, you can try this, under your hexo folder

        $ git clone blablan
2. Update the _config.yml

3. hexo s and see if the new themes applied


---

	
#### Mission 4 : Create a repo to make your blog could wrote in multiple computer
1. Under your hexo folder

		$ git init
2. Create a repo in your githug account 

3. In your computer, under the folder execute below command to link the blog repo
 
		$ git remote set-url origin https://github.com/youraccountname/yourblogrepo.git

3. You need to edit .gitignore to ignore files do not need to push, here is my [example](https://github.com/cheshiret/blog_repo/blob/master/.gitignore)

4. Add the file

		$ git add .
5. Commit the change

		$ git commit -m "first change"
6. Push the change to repo
		
		$ git push origin master

7. Next time, you can use git pull to pull the recent change, then repeat step 3 - step 5 to sync the code between repo and computer


_IMPORTTANT NOTE!!!_
<br/> Github repo is public, unless you pay for privacy repo. So DO NOT add the files that you don't want to share in .gitignore, so you can keep it private
	If you have done this, and you want to remove some files that you have already push to github, try this
	
		$ git rm -cached filename
		$ git push origin master

---


#### More Reference
[Hexo Official Site ](https://hexo.io/)
[Hexo Your Blog](http://ibruce.info/2013/11/22/hexo-your-blog/)
[Hexo Guide](http://www.jianshu.com/p/73779eacb494)
[Customising the Hexo Theme](http://jr0cket.co.uk/hexo/hexo-theme-simple-changes.html)
[How to use Jacman theme](http://wuchong.me/blog/2014/11/20/how-to-use-jacman/)
[How to make hexo theme](http://my.oschina.net/youxiachai/blog/121659?fromerr=MgG2GeKQ)