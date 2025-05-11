# Cloud Chatbot

Cloud Chatbot 是一个集成了 **Telegram 机器人**、**电影评论系统** 和 **菜谱信息管理** 的多功能聊天机器人项目。  
本项目基于 **Python** 开发，结合 **Redis** 和 **MySQL** 数据库，实现灵活扩展和高效数据管理。

---

## 🎯 功能特点

### 1. Telegram 聊天机器人
- **文本消息处理**：支持文本消息回声功能。
- **图片与视频处理**：支持用户上传图片与视频，并基于上下文提供响应。
- **命令支持**：
  - `/add <keyword>`：记录关键词出现次数。
  - `/help`：显示帮助信息。
  - `/who`：显示机器人的身份。
  - `/cook`：获取菜谱信息。
  - `/upload`：上传菜谱信息。
  - `/find <movie_name>`：根据电影名查找电影。
  - `/write <comment>`：添加电影评论。
  - `/read`：查看电影评论。

### 2. 菜谱管理
- 上传菜谱，包括 **菜名、视频、描述**。
- 查询菜谱信息。
- 菜谱数据存储至 **MySQL** 数据库。

### 3. 电影评论系统
- 查询电影信息。
- 添加/查询电影评论。
- 上传电影海报。

### 4. 数据库集成
- **MySQL**：存储电影、评论和菜谱信息。
- **Redis**：缓存和存储关键词统计等临时数据。

---

## 🚀 安装与使用

### 📚 环境要求
- Python 3.7+
- MySQL 数据库
- Redis 数据库
- Telegram Bot API Token

### 📦 安装步骤

1. 克隆项目代码：
    ```bash
    git clone https://github.com/PTGWong/cloud-chatbot.git
    cd cloud-chatbot
    ```

2. 安装依赖：
    ```bash
    pip install -r requirements.txt
    ```

3. 配置文件：

    编辑 `config.ini`，填写以下内容：

    ```ini
    [TELEGRAM]
    ACCESS_TOKEN = your-access-token

    [REDIS]
    HOST = your-redis-host
    PASSWORD = your-redis-password
    REDISPORT = your-redis-port
    ```

4. 设置 MySQL 数据库：

    确保 MySQL 已启动，并创建相应的表结构（具体表结构请参考项目代码）。

5. 运行项目：

    启动 Telegram 机器人：

    ```bash
    python projectchatbot.py
    ```

    交互模式运行：

    ```bash
    python mall.py
    ```

---

## 📁 项目结构

```plaintext
cloud-chatbot/
├── projectchatbot.py    # Telegram 机器人的主程序
├── mall.py              # 交互模式功能实现
├── config.ini           # 配置文件
├── requirements.txt     # 依赖库列表
```

---

## 💡 使用示例

### 上传菜谱

```plaintext
1. 使用 /upload 命令开始上传菜谱。
2. 使用 /cname 提供菜名。
3. 使用 /cdescribe 提供菜谱描述。
4. 上传菜谱视频。
```
### 电影评论
```plaintext
1. 使用 /find <movie_name> 查找电影。
2. 使用 /write <comment> 为电影添加评论。
3. 使用 /read 查看电影评论。
```
