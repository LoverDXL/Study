### 2021/8/11更新

**Windows系统通过git上传文件到GitHub**

```markdown
1.在github上创建一个仓库，然后将仓库的链接复制下来
2.在本地上执行git clone 链接
3.在clone下来的文件夹中git init和配置user.name和user.email
	git config user.name "yourname"
	git config user.email "youremail"
4.把你要上传的文件全都复制到这个文件夹内
5.执行命令
	git add .
	git commit -m "describe"
    git remote add origin git@github.com:LoverDXL/Study.git 
在将本地仓库与GitHub网站上的仓库进行关联后，便可进行推送了，但是在第一次进行推送时，需要注意的是，GitHub网站上的仓库并非是空的，我们在创建时创建了一个README文档，因此需要将两者进行合并才行。
    git pull --rebase origin main
最后，在进行推送即可。
	git push -u origin main
	
	
注意点：这个带有-u这个参数是指，将master分支的所有内容都提交，第一次关联之后后边你再提交就可以不用这个参数了，之后你的每一次修改，你就可以只将你修改push就好了。
```



回到GitHub网站刷新下我们的GitHub仓库，便可看到已经将windows上文件夹的内容全部同步过来了。

### **定期维护**

在完成第一次上传后，之后在本地做的修改，都可以通过如下命令进行同步。

```
git add -A               #将文件的修改上传到暂存区
git add *                #用于更新所有代码

git commit -m '说明'      #提交到本地仓库

git push origin master   #推送到GitHub网站上
```

相关出现问题参考：

### 一、Git 常见错误 之 error: src refspec xxx does not match any / error: failed to push some refs to 简单解决方法

参考链接：[(19条消息) Git 常见错误 之 error: src refspec xxx does not match any / error: failed to push some refs to 简单解决方法_仙魁XAN-CSDN博客](https://blog.csdn.net/u014361280/article/details/109703556)

### 二、GitHub_git push出现[rejected] master -＞ master (non-fast-forward)问题解决

参考链接：[(19条消息) GitHub_git push出现[rejected\] master -＞ master (non-fast-forward)问题解决_huU丶-CSDN博客](https://blog.csdn.net/hu18315778112/article/details/89487688)

### 三、[git pull origin master与git pull --rebase origin master的区别](https://www.cnblogs.com/ellen-mylife/p/12794245.html)

### 四、更新仓库遇到的问题

参考链接：[(19条消息) git仓库push最新文件_上传本地文件（夹）到GitHub和更新仓库文件_weixin_39581964的博客-CSDN博客](https://blog.csdn.net/weixin_39581964/article/details/113896393?utm_medium=distribute.pc_relevant.none-task-blog-2~default~baidujs_utm_term~default-0.control&spm=1001.2101.3001.4242)
