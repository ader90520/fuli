福利吧论坛腾讯云
介绍
源代码参考地址：
https://www.wnflb2023.com/forum.php?mod=viewthread&tid=182298

设置环境变量

fuliba_cookie

fuliba_username

pushplus_token(推送方式可根据自己需要从pusher.py内查看参数更换)

（推送可选择自己需要的推送方式）

设置自定触发器：0 9 5 * * * *（举例）

阿里云函数教程
需修改入口参数为index.main_handler
其他步骤与腾讯云一样
打包的代码内需设置环境变量
特殊情况
部分用户名是中文，如遇到变量无法添加，可将index.py倒数第二行

user_name = os.environ.get("fuliba_username")

修改成

user_name = "中文用户名"

并且删除环境变量fuliba_username
