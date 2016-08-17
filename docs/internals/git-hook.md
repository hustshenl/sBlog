# Git Hook 处理方案

### 工作流程

1. git服务端hook访问hook URL，标记新hook
2. 定时任务根据hook信息读取git未更新的提交记录：`git log --pretty="%H"  --name-status --reverse <commit id>..HEAD`，循环读取信息，根据提交记录列出增/改/删文件列表；


### 日志信息示例
```
6d4c7b0489bcfd9dc807b662b5d6a5c1c499e1f7
A       a.txt
549c140d635609b849ccd532df5aadd1aea8aee1
M       a.txt
10404365d17733ea382345f43f88eb072e0b2bda
D       a.txt
```
说明：
+ A：add，新增文件
+ M：Modify，修改文件
+ D：delete，删除文件
+ commit ID 为40位随机字符串



