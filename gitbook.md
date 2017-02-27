##在MAC上面书写GITBOOK
* 首先git clone 到本地

  `git clone https://git.gitbook.com/visite/note-of-front-end.git`

* 然后需要添加验证，有两种方法
	* 第一种 
	
	  ```
	  git remote add gitbook https://username:apitoken@git.gitbook.com/marshallshen/ruby-api-best-practices.git
	 git push -u -f gitbook master
	 ```
	 
	  username: visite
	  apitoken 在这里取得，点击 generate token, 添加新的API TOKEN
	
	  ![test](image/apitoken.png)
	  
	* 第二种 在根目录先建一个.netrc文件， 如果已经存在，直接在里面修改
	
	 ```
	machine git.gitbook.com
  	login USERNAME-or-EMAIL
  	password API-TOKEN-or-PASSWORD
  	```   
	然后
	
		```
   git remote add gitbook https://git.gitbook.com/{{UserName}}/{{Book}}.git
 	git push -u -f gitbook master
  	```
  	
	**第二种方法有问题， 待解决**

## Gitbook 同步 github
首先 安装 GitHub Integration， 在settings的github选项里安装

![test](image/gitbook.png)

然后在book里面的settings，同步书到github的项目，最好新建一个空的PROJET


![test](image/gitbook1.png)
	
	
**还有一种从github里面的项目建一个BOOK， 新建BOOK的时候选择github.**
	