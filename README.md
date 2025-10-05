# 🚀 纯小白huggingface空间上部署自己容器内的项目：从零到一，打造你的私人AI万能API (保姆级实战) ✨

<p align="center">
  <a href="https://github.com/lzA6/huggingface-spaces-tutorial/stargazers"><img src="https://img.shields.io/github/stars/lzA6/huggingface-spaces-tutorial?style=for-the-badge&logo=github&color=FFC107" alt="GitHub Stars"></a>
  <a href="https://github.com/lzA6/huggingface-spaces-tutorial/network/members"><img src="https://img.shields.io/github/forks/lzA6/huggingface-spaces-tutorial?style=for-the-badge&logo=github&color=4CAF50" alt="GitHub Forks"></a>
  <a href="https://github.com/lzA6/huggingface-spaces-tutorial/blob/main/LICENSE"><img src="https://img.shields.io/github/license/lzA6/huggingface-spaces-tutorial?style=for-the-badge&color=2196F3" alt="License"></a>
  <img src="https://img.shields.io/badge/状态-持续更新-brightgreen?style=for-the-badge" alt="Status">
</p>
<p align="center">
  「小白轻松部署自己的项目。🔥」
</p>

## 第一步：准备工作 (软件与源代码)

### 🎯 本步目标
在你的电脑上安装必备软件，并下载本项目的完整源代码。

### 🧠 原理速览
*   **Git**：一个“版本控制系统”，是程序员用来管理代码和上传代码到服务器的“快递工具”。
*   **VS Code**：一个强大的“代码编辑器”，能让代码看起来更漂亮，写起来更轻松。
*   **源代码**：就是运行我们这个“AI万能转换器”所需要的所有程序文件。

### 👇 操作步骤

 **安装必备软件**
    *   **Git**: [点击下载Git for Windows](https://git-scm.com/downloads)。下载后一路点击 `Next` 安装。
    *   **VS Code**:  [点击下载Visual Studio Code](https://code.visualstudio.com/)。同样，一路 `下一页` 安装即可。
    *   **重要提示**：安装完后，**重启电脑**，确保所有设置都生效了！

### 第 1 步：获取项目代码

打开您的命令行（终端），克隆本项目到您的电脑上。

```bash
git clone https://github.com/lzA6/Qwen-2api.git
cd Qwen-2api
```

---

## 第二步：创建Hugging Face Space (云端基地)

### 🎯 本步目标
免费申请一个用于托管我们项目的云端服务器，官方称之为 **Space (空间)**。

### 👇 操作步骤

1.  **注册与登录**：访问  [**Hugging Face 官网**](https://huggingface.co/)，登录（如未注册请自行注册）

2.  **创建新 Space**
    *   登录后，点击右上角**圆形头像** -> `New Space`。
    *   或者你可以按照下方这样快速创建
    *   <img width="2422" height="1145" alt="7eea2916e9d1522a6aa6581a2aab3e64" src="https://github.com/user-attachments/assets/22ff9843-6457-410a-a48d-613776795946" />

    *   在 “Create a new Space” 页面，按以下说明填写：
        *   **Space name**: 起一个**纯英文小写**的名字，例如 `my-translator`。
        *   **License**: 选择 `mit`。
        *   **Select the Space SDK**: **【‼️关键‼️】** 点击那个**蓝色小鲸鱼 🐳 图标的 `Docker`**。
        *   **Template**: 确保选中的是 `Blank`。
     
        *   <img width="1893" height="1320" alt="839a6e55ccc15202a22887f9afdefa37" src="https://github.com/user-attachments/assets/f0dd453d-031b-407e-9150-2ab3866c7389" />

    *   最后，点击蓝色的 `Create Space` 按钮。

3.  **复制你的 `git clone` 命令**
    *   创建成功后，页面会跳转。你会看到类似下图的界面，在 `HTTPS` 标签下，有一行 `git clone https://...` 的命令。
    *   点击这行命令最右侧的**复制图标 📋**，把它完整地复制下来。
  
    *   <img width="1035" height="537" alt="2d8504298cc4c2ae7c9e380202c731af" src="https://github.com/user-attachments/assets/3f342cdc-15cd-4895-a611-9c701350c136" />


---

## 第三步：本地施工 (同步并填充文件)

### 🎯 本步目标
将云端的空Space同步到本地，并将我们下载的源代码放进去。

### 👇 操作步骤

1.  **打开命令终端**
    *   在你的电脑上找个地方（比如D盘），新建一个文件夹，命名为 `MyProjects`。
    *   **进入这个 `MyProjects` 文件夹**。在顶部的**地址栏**里，删掉原来的文字，输入 `cmd`，然后按**回车**。一个黑色命令行窗口会弹出。
  
    *   <img width="1035" height="429" alt="image" src="https://github.com/user-attachments/assets/62a58903-496b-4c31-a954-59749bd6e8cf" />


2.  **克隆(Clone)你的 Space**
    *   在黑色终端里，**右键单击**，粘贴上一步复制的 `git clone` 命令，然后按**回车**。
    *   下载完成后，你的 `MyProjects` 文件夹里会多出一个和你Space同名的新文件夹（例如 `my-translator`）。

3.  **进入本地项目目录**
    *   继续在终端里，输入 `cd` 命令进入这个新文件夹：
        ```bash
        # 将 my-translator 替换成你自己的Space名称
        cd my-translator
        ```

4.  **迁移项目代码到huggingface空间的文件夹下**
    *   直接把你的项目源码复制并跳过过来：
    *   <img width="1124" height="805" alt="image" src="https://github.com/user-attachments/assets/038c4a4c-fb96-4cb1-8f69-56b067491949" />


---

## 第四步：核心配置 (端口与秘密)

### 🎯 本步目标
配置项目运行所必需的端口和个人凭证。

### 👇 操作步骤

1.  **【‼️重中之重‼️】配置 `README.md` 的端口**
    *   在你的本地项目文件夹 (`my-translator`) 中，找到 `README.md` 文件，用 VS Code 打开它。
    *   **删除里面的所有内容**，然后将以下配置**完整地复制粘贴**进去：
        ```yaml
        ---
        title: Qwen 2API
        emoji: 🚀
        colorFrom: blue
        colorTo: green
        sdk: docker
        app_port: 8082
        ---
        ```
    *   **🧠 原理速览**：`sdk: docker` 告诉Hugging Face这是一个Docker项目。`app_port: 8082` 是在告诉Hugging Face的“网络管理员”：“请把所有访问我这个网站的外部流量，都引导到我程序内部的8082端口！” **如果没有这一行，你的应用将无法被外界访问！**
    *   **保存并关闭** `README.md` 文件。

2.  **在 Hugging Face 云端设置 Secrets (秘密)**
    *   回到你的Hugging Face Space页面，点击 `Settings` 标签页 -> `Variables and secrets`。
    *   点击 `New secret` 按钮，添加以下几个秘密：
        *   **秘密 1：主访问密码**
            *   **Name**: `API_MASTER_KEY`
            *   **Value**: `设置一个你自己的复杂密码` (例如: `MySuperSecretKey_2024!`)
        *   **秘密 2 & 3：通义千问身份凭证**
            *   **如何获取？** 登录  [通义千问官网](https://tongyi.aliyun.com/qianwen/)，按 `F12` 打开开发者工具，在 `Application` -> `Cookies` 中找到 `cookie` 和 `x-xsrf-token` 的值，然后分别创建名为 `CN_ACCOUNT_1_COOKIE` 和 `CN_ACCOUNT_1_XSRF_TOKEN` 的Secret并粘贴进去。

---

## 第五步：上传与激活 (含终极排错)

### 🎯 本步目标
将配置好的项目上传到Hugging Face，并解决所有可能遇到的上传问题。

### 👇 操作步骤

1.  **获取 Hugging Face 上传令牌 (Access Token)**
    *   点击HF页面右上角头像 -> `Settings` -> `Access Tokens` -> `New token`。
    *   起个名字，`Role` (角色) 选择 `write`，然后生成并**立刻复制好这串 `hf_` 开头的令牌**。
  
    *   <img width="2349" height="1243" alt="68147375a4f3f98a64697c43ea7bcdb9" src="https://github.com/user-attachments/assets/4b92c127-c699-4893-9472-28cb9de6ae96" />


2.  **执行上传**
    *   回到你的黑色终端窗口（确保路径仍在你的项目文件夹下）。
    *   **A. 设置Git身份** (首次使用需要，这个为全局设置的必要)
        *   如果你在后续步骤遇到 `Author identity unknown` 的错误，就执行这两条命令，否则可以跳过：
            ```bash
            git config --global user.name "YourName"
            git config --global user.email "you@example.com"
            ```

            <img width="885" height="268" alt="image" src="https://github.com/user-attachments/assets/c165404f-d07c-4fd4-94bb-0e97221c2866" />

    *   **B. 添加文件并创建记录**
        ```bash
        git add .
        git commit -m "Deploy my first AI translator"
        ```
    *   **C. 【‼️终极上传命令‼️】**
        *   **🧠 原理速览**：直接使用 `git push` 可能会在Windows上遇到一个 `git-credential-manager.exe` 的弹窗错误（“字符串绑定无效”）。为了“一石二鸟”，我们使用一个更强大的命令，它将用户名和令牌直接包含在URL中，从而绕过这个烦人的弹窗。
        *   **命令模板**:
            `git push https://你的HF用户名:你的HF令牌@huggingface.co/spaces/你的HF用户名/你的Space名 main`
        *   **举例**: 假设你的HF用户名是 `xiaobai`，Space名是 `my-translator`，令牌是 `hf_abc123def456`。
            你的完整命令就是：
            ```bash
            git push https://xiaobai:hf_abc123def456@huggingface.co/spaces/xiaobai/my-translator main
            ```
  
  <img width="1446" height="641" alt="image" src="https://github.com/user-attachments/assets/4ad9ad91-fa2a-44f8-b3e0-a63dc9d8abca" />

  具体参考：[L站2级帖](https://linux.do/t/1005372)

        *   **请仔细对照例子，替换成你自己的信息，然后复制到终端里，按下回车！**

### 🤔 疑难排解
*   **问题**：执行 `git push` 后，弹出一个 `git-credential-manager.exe - 系统错误` 的窗口，提示“字符串绑定无效”。
*   **解答**：这正是我们推荐使用“终极上传命令”的原因！请直接使用第五步 C 部分的命令格式，它能完美解决这个问题。

---

## 第六步：最终测试与使用

### 🎯 本步目标
确认服务正常运行，并学会如何在其他AI软件中使用它。

### 👇 操作步骤

1.  **查看应用状态**
    *   回到你的Hugging Face Space页面。状态会经历 `Building` (正在构建) -> `Starting` (正在启动) -> **`Running` (正在运行)**。当看到绿色的 `Running` 时，你就成功了！🎉

2.  **如何在AI客户端中使用？**
    *   任何支持OpenAI API的客户端（如Chatterbox, LobeChat, NextChat等），通常都需要你填写三个信息。你的信息如下：
        *   **API 地址 / API Base URL**: `https://你的HF用户名-你的Space名.hf.space`
        *   **API 密钥 / API Key**: `你在第四步设置的API_MASTER_KEY的值`
        *   **模型名称 / Model Name**: `qwen-plus` (或其他通义千问支持的模型，如 `qwen-turbo`, `qwen-max`)
     
        *   <img width="675" height="345" alt="image" src="https://github.com/user-attachments/assets/fb57a26c-375c-4d3b-8e15-a6bafdb6c101" />

      <img width="715" height="750" alt="image" src="https://github.com/user-attachments/assets/df7e1ae0-f8a7-467d-a1e8-bf28a9766c6e" />

      <img width="993" height="489" alt="image" src="https://github.com/user-attachments/assets/dbd738f3-2333-45b6-a3dc-d8beae91c71d" />



        


3.  **使用 `curl` 快速自测**
    *   打开终端，复制并修改以下命令进行测试：
        ```bash
        curl --location 'https://你的HF用户名-你的Space名.hf.space/v1/chat/completions' \
        --header 'Content-Type: application/json' \
        --header 'Authorization: Bearer 你的API_MASTER_KEY' \
        --data '{
            "model": "qwen-plus",
            "messages": [{"role": "user", "content": "你好，我的第一个AI！"}],
            "stream": false
        }'
        ```
    *   如果返回了AI的回答，那么一切完美！你的私人AI万能API正式上线！
