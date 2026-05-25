window需要使用 winget install Hugo.Hugo.Extended
下载好了之后
重新打开终端窗口 运行 hugo version测试是否安装成功

在你所想的目录中打开cmd 运行

hugo new project quickstart
cd quickstart
git init

设置主题

git clone https://github.com/raindayan/hugo-theme-nightfall.git themes/nightfall

echo "theme = 'ananke'" >> hugo.toml
这个有坑 会导致乱码 建议在原文件上使用记事本编辑
总之就在hugo.toml文件中加上主题配置

hugo server

运行好之后打开localhost的1313端口服务就可以了

接下来你会发现网页中什么都没有 这个时候就需要配置一些配置比如hugo.toml


用hugo部署主题的时候有很多细节盲点，不知不觉几个小时就过去了，比如配置文件参数怎么配置，文档要在哪里建，实际上在content中，还有主题作者提醒的路径配置方式

现在把主页菜单的导航会配置了，还有个问题就是，怎么样可以生成一个文章，带有默认的日期作者信息，然后如何把obsidian中的文档无缝迁过去

到时候看能不能自动化一键部署，我这边在ob上写文章，写完以后，一键同步到本地的hugo里边然后打包自动部署到cf上，这样能实现的话就会方便很多
