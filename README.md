# qq-guild-keyword-recall-bot
A QQ Guild Keyword Recall Bot based on BotPy. 基于官方 BotPy 框架构建的 QQ 频道关键词检测撤回机器人程序。
本程序仅支持私域QQ频道机器人。

<center><img src="https://github.com/sonicspinforum/qq-guild-keyword-recall-bot/blob/main/img/preview.jpg?raw=true" width="30%" /></center>

## 使用方法

1. 准备 Python 3.8 及以上版本的环境，确保已安装 pip。运行 pip install qq-botpy
2. 建立关键词名单
新建 sonicbotDetectWord.txt，通过换行分割关键词

例如: 

>关键词1
>
>关键词2
>
>关键词3

机器人会自动检测所有消息是否匹配关键词。

3. 加密关键词名单
运行 python encodeSecrets.py

目录下会自动生成 secrets.txt。记得检查 secrets.txt 末尾是否有空行，若有请删除。

4. 修改 sonicbot.py，将 appid="", token="" 分别修改成您在 q.qq.com 注册机器人的 BotAppID 与机器人令牌
5. (可选) 删除 sonicbotDetectWord.txt 以保障安全

## 恢复 sonicbotDetectWord.txt
运行 python decodeSecrets.py 即可

## 关于关键词匹配
- 关键词匹配采用 UTF-8 编码方式，支持中文
- 经过验证，"关键词" 可匹配于任何包含该关键词的内容，例如 "关键词233w" 与 "abcd关键词"，其他语言亦是如此
