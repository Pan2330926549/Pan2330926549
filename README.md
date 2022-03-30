- 👋 Hi, I’m @Pan2330926549
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
@ -1,128 +1,129 @@
#!/usr/bin/env 红宝石
def  replace_in_file （文件， 之前， 之后， target_regexp  =  nil ）
  把 “替换在' #{文件} '中。”
  如果目标正则 表达式
    目标文件内容 =  ""
    文件. 打开（文件）。每行 做| l |
      升。gsub！（之前， 之后） 如果！升。匹配（目标正则表达式）
      我 如果！升。匹配（目标正则表达式）
      目标文件内容+= l
    结尾
  别的
    target_file_content  = 文件。打开（文件）。读
    目标文件内容。gsub！（之前， 之后）
  结尾
  文件. 打开(文件,  "w+" ) 做| f |
    f . 写（目标文件内容）
  结尾
结尾
def 流(命令, 前缀 =  " " )
  放 “”
  IO 。popen (命令) 做| io |
    while  ( line  =  io.gets )做_ _ 
      放 “ #{前缀} #{行} ”
    结尾
  结尾
  放 “”
结尾
def 红色(字符串)
  " \e [1;31m #{字符串} \e [0m"
结尾
默认 绿色（字符串）
  " \e [1;32m #{字符串} \e [0m"
结尾
def 蓝色(字符串)
  " \e [1;34m #{字符串} \e [0m"
结尾
def 黄色（字符串）
  " \e [1;33m #{字符串} \e [0m"
结尾
定义 询问（字符串）
  放 蓝 线
  返回 得到。条
结尾
# 除非 shell 当前版本的 Ruby 与应用程序需要的相同，否则我们应该标记它。
required_ruby  =  `cat ./.ruby-version` . 条
actual_ruby  =  `ruby -v` 。条
message  =  "Bullet Train 需要 Ruby #{ required_ruby }并且 `ruby -v` 返回#{ actual_ruby }。"
如果 actual_ruby 。包括？( required_ruby )
  放 绿（消息）
别的
  放 红（消息）
  出口
结尾
# 除非 shell 当前版本的 Ruby 与应用程序需要的相同，否则我们应该标记它。
必需 =  `cat ./.nvmrc` 。条
实际 =  `node -v` 。条
message  =  "Bullet Train 需要 Node.js #{ required }并且 `node -v` 返回#{ actual }。"
如果 actual_ruby 。包括？( required_ruby )
  放 绿（消息）
别的
  放 红（消息）
  出口
结尾
如果 `git远程| grep 子弹头列车` 。带。长度> 0
  将 黄色 “存储库已经有一个\`子弹列车` \遥控器。”
别的
  如果 `git远程| grep 起源` 。带。长度> 0
    将 绿色 “重命名存储库 `origin` 远程到 `bullet-train`。”
    `git远程重命名起源子弹列车`
  别的
    puts  red  "Repository 没有 `origin` 遥控器，也没有 `bullet-train` 遥控器。出了什么问题吗？"
  结尾
结尾
如果 `git远程| grep 起源` 。带。长度> 0
  将 黄色 “存储库已经有一个\`源` \远程。”
别的
  问 “点击<Return>，我们将打开一个浏览器到GitHub，您可以在其中创建一个新存储库。完成后，从新存储库复制SSH路径并返回这里。我们会要求您将其粘贴到我们在下一步。”
  `打开 https://github.com/new`
  ssh_path  = 询问 “好的，SSH 路径是什么？（应该看起来像 `git@github.com:your-account/your-new-repo.git`。）”
  将 绿色 “设置存储库的 `origin` 远程到 ` #{ ssh_path } `。”
  puts  `git remote add origin #{ ssh_path } ` 。大嚼
结尾
local_branch  =  `git 分支 | grep“*”` 。分裂。最后的
将 绿色 “将存储库推送到`origin`。”
流 “git push origin #{ local_branch } :main 2>&1”
将 绿色 “运行`捆绑安装`。”
流 “捆绑安装”
如果 `yarn -v 2> /dev/null` 。带。长度> 0
  puts  green  "Yarn is installed."
别的
  将 红色 “未安装纱线。尝试`brew install yarn`。”
  出口
结尾
将 绿色 “运行`yarn install`。”
流 “纱线安装”
# 这应该现在可用。
需要 “active_support/inflector”
human  = 询问 “您的新应用程序在标题中的名称是什么？（例如\" Some Great Application \"）”
变量 =  ActiveSupport ::变形器。参数化（人类， 分隔符：'_' ）
environment_variable  =  ActiveSupport ::变形器。参数化（人类， 分隔符：'_' ）。大写
类名 = 变量。分类
kebab_case  = 变量。tr ( "_" ,  "-" )
放 “”
 在整个代码库中放置绿色“ 用\” #{ human } \ " 替换\" Untitled Application \"的实例。”
replace_in_file ( "./.circleci/config.yml" ,  "untitled_application" , 变量)
replace_in_file ( "./config/application.rb" ,  "untitled_application" , 变量)
replace_in_file ( "./config/database.yml" ,  "untitled_application" , 变量)
replace_in_file ( "./config/database.yml" ,  "UNTITLED_APPLICATION" ,  environment_variable )
replace_in_file ( "./config/cable.yml" ,  "untitled_application" , 变量)
replace_in_file （“./c
<!---
Pan2330926549/Pan2330926549 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
