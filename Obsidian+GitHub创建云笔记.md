## 首次安装流程
#### 1. 安装 Git
   - 访问网址：[Git 下载地址](https://git-scm.com/downloads)
   - 选择您的操作系统（Windows、macOS 或 Linux）并下载 Git 的安装包。
   - 下载完成后，打开安装包，按照提示一步步完成安装。
#### 2. 安装 TortoiseGit
   - 访问网址：[TortoiseGit 下载地址](https://tortoisegit.org/download/)
   - 下载并安装 TortoiseGit，这是一个 Git 的图形化客户端，更适合不熟悉命令行的用户。
#### 3. 安装 Obsidian
   - 访问网址：[Obsidian 下载地址](https://obsidian.md/download)
   - 下载适用于您的操作系统的 Obsidian 安装包安装。
#### 4. 注册 GitHub 账号
   - 访问网址：[GitHub 官网](https://github.com/)
   - 在 GitHub 网站上点击 “Sign up” 注册新账号，填写邮箱、密码等信息。
#### 5. 新建 GitHub 私有仓库
   - 登录 GitHub 后，点击右上角的 “+” 号并选择 “New repository” 创建新仓库。
   - 在仓库名称下方，选择 **Private**（私有），这样您的仓库内容只有您和邀请的人可以看到，Add .gitignore 任意选择一个模板，点击创建。
#### 6. 生成 SSH Key
   - 打开命令行（Windows 的 “命令提示符” 或 macOS 的 “终端”）
   - 输入以下命令，替换 `"你的邮箱地址"` 为您注册 GitHub 时使用的邮箱地址：
     ```bash
     ssh-keygen -t rsa -b 4096 -C "你的邮箱地址"
     ```
   - 按照提示，生成一个 SSH 密钥。一路回车即可，直到密钥生成完成。
   - 生成的 SSH Key 会保存在您的用户目录下的 `.ssh` 文件夹中，一般是 `id_rsa` 和 `id_rsa.pub` 文件。用记事本打开 `id_rsa.pub` 文件，复制里面的内容。
#### 7. 在 GitHub 中添加 SSH Key
   - 打开 GitHub，点击右上角头像，选择 “Settings”。
   - 在左侧菜单中选择 “SSH and GPG keys”，点击 “New SSH key”。
   - 将第 6 步中复制的 SSH 公钥粘贴到 “Key” 输入框中，设置一个名字（如：我的电脑）。
   - 点击 “Add SSH key” 保存。
#### 8. 本地克隆 GitHub 仓库并配置 `.gitignore` 文件
   - 打开 TortoiseGit 或命令行工具，克隆您在 GitHub 上创建的仓库。     ```
   - 配置 `.gitignore` 文件：在仓库文件夹中修改 `.gitignore` 的文件内容为`/.obsidian/`，确保 Obsidian 的配置文件不会上传到 GitHub。
   - 仓库文件夹中右键选择git提交，选择修改的文件，填写日志信息，点击提交并推送
#### 9. 在 Obsidian 中导入仓库文件夹
   - 打开 Obsidian，点击 “打开文件夹为库”，选择第 8 步中克隆的 GitHub 仓库文件夹。


## 日常使用操作

新增或者修改了笔记后要及时提交，提交流程如下：
1. 仓库文件夹中右键TortoiseGit，选择拉取
2. 点击提交，选择修改的文件，填写日志信息，点击提交并推送

