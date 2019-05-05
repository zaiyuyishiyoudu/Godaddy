# 获取openwrt官方源码
● git clone https://github.com/openwrt/openwrt.git
![git clone](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/获取openwrt官方源码.png)

# 查看分支
● git branch     查看本地分支
![git branch](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/查看本地分支.png)
● git branch -a  查看远程分支 对应github的Branches 开发版
![git branch](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/查看远程分支.png)
![github](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/Branches.png)
● git tag		查看tag 对应github的Tags 稳定版
![git tag](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/查看tag.png)
![github](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/Tags.png)

● git checkout -b 希望的名称(任意取) origin/Branches分支名 签出分支 大写-B为强制
● 例如1：git checkout -b 18.06 origin/openwrt-18.06
● 例如2：git checkout -b 18.06 openwrt-18.06
![git checkout](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/签出18.06分支.png)

● git checkout -B 希望的名称(任意取) tags分支名 强制创建一个基于指定的tag的分支。
● 例如：git checkout -B 17.01.6 v17.01.6
![git checkout](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/签出17.01.6分支.png)

● git checkout master  签回主分支
![git checkout](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/签回主分支.png)

# 直接获取开发版源码
# 优点：简单直接
# 缺点：不能切换其它分支
# 直接获取开发版源码18.06分支
● git clone -b openwrt-18.06 https://github.com/openwrt/openwrt.git

# 直接获取稳定版源码18.06.2分支
● git clone -b v18.06.2 https://github.com/openwrt/openwrt.git

# 更新源码
● 未切换分支可以直接运行 git pull
● 如已切换分支请参考
**[参考1](https://blog.csdn.net/u010059669/article/details/82670484)**
**[参考2](https://www.cnblogs.com/phpper/p/7136048.html)**
**[参考3](https://www.yiibai.com/git/git_pull.html)**

# 对本地代码库进行回滚
● git log 查看提交历史，找出要回滚到的commit-id
![git log](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/4.14.106.png)
● git reset --hard commit-id :回滚到commit-id
● 比如回滚到openwrt 4.14.106内核时的源码
● git reset --hard a8cfef6c4584b1cf3e334c6d43a850b86d536d7d
![git log](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/回滚.png)
● 这时include/kernel-version.mk内显示的就是4.14.106的内核了
![git log](https://github.com/zaiyuyishiyoudu/Godaddy/blob/master/回滚后内核.png)
