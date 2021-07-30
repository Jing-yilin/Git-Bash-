 [(7条消息) Git使用教程：最详细、最傻瓜、最浅显、真正手把手教！_一只蜗牛的博客-CSDN博客_git教程](https://blog.csdn.net/u011535541/article/details/83379151) 

 [(7条消息) 一次搞清 git checkout，git restore 和 git reset_Sweet_19BaBa的博客-CSDN博客](https://blog.csdn.net/Sweet_19BaBa/article/details/111950384?utm_medium=distribute.pc_aggpage_search_result.none-task-blog-2~aggregatepage~first_rank_v2~rank_aggregation-1-111950384.pc_agg_rank_aggregation&utm_term=git+restore和checkout&spm=1000.2123.3001.4430) 

 从2020年10月1日开始，所有“master分支”一律改名为“main分支”。 对于接触Git和GitHub已有多年的开发者来说，这个变化将需要一段时间来适应。 即使您知道变化是正确的做法，多年来手指还是习惯输入git checkout master。 现在，您要改为**git checkout main**。 我预计其他许多技术会仿而效之，所以开发者很可能会在某个时候对他们使用的许多工具进行类似的改变。 

 [(7条消息) 解决git push 错误error: src refspec master does not match any. error: failed to push some refs to_wenb1bai的博客-CSDN博客](https://blog.csdn.net/wenb1bai/article/details/89363711) 





## 如何远程连接仓库并上传所有工作内容

1. 现在github里面创建一个和本地文件夹同名的repository（仓库）

2. 需要用他的网页地址： https://github.com/Jing-yilin/Html_study

3. ```shell
   git init # 本地初始化
   git add * # 本地文件全部提交
   git commit -m "你的备注"
   git remote add origin https://github.com/Jing-yilin/Html_study # 远程连接到库
   git push -u origin master # 本地上传到库
   ```

   ![1627667396497](C:\Users\Jing Yilin\AppData\Roaming\Typora\typora-user-images\1627667396497.png)

##  如何从远程库克隆 

```shell
git clone https://github.com/Jing-yilin/Html_study
```

这样整个Html_study文件加就被克隆到本地了

## 创建于合并分支

查看分支：

```shell
git branch
```

创建分支：

```shell
git branch name
```

切换分支：

```shell
git checkout name
```

创建+切换分支：

```shell
git checkout –b name
```

合并某分支到当前分支：

```shell
git merge name
```

删除分支：

```shell
git branch –d name
```

## 错误 

### fatal: protocol '?https' is not supported

今天从github上克隆项目到本地时，我先输入：

```shell
git clone https://github.com/Jing-yilin/Html_study
```

结果返回

```shell
fatal: protocol '?https' is not supported
```

原因是https前面有其他的字符，删掉就好了！

