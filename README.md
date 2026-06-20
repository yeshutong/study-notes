# 叶舒桐 (Ye Shutong) 学习仓库

个人学习笔记、代码练习与知识整理，涵盖软件开发各方面的学习与实践。

---

## 目录结构

```
yeshutong-notes/
├── README.md              # 本说明文件
├── LICENSE               # MIT 许可证
├── architecture/         # 架构设计学习笔记
│   ├── docs/             # 架构文档、设计模式
│   └── resources/       # 相关资源与链接
├── cpp/                  # C++ 学习与练习
│   ├── notes/            # C++ 笔记
│   ├── code/             # C++ 代码练习
│   └── projects/         # C++ 项目
└── resources/           # 通用参考资料
```

---

## 使用说明

### 1. 克隆仓库到本地

如果你换了一台电脑，想把这个仓库下载到本地：

```bash
git clone git@github.com:yeshutong/learn_cpp.git
cd learn_cpp
```

> 注意：如果你还没有配置 SSH key，请先按下方"SSH 配置"部分操作。

### 2. 日常编辑与推送

每次学习后，按以下步骤更新：

```bash
# 1. 进入仓库目录
cd github\yeshutong-notes

# 2. 查看文件状态（哪些文件被修改了）
git status

# 3. 将修改的文件添加到暂存区
git add .

# 4. 提交修改，写上说明
git commit -m "今天学习了 XXX"

# 5. 推送到 GitHub
git push
```

> 如果 SSH key 已配置好，`git push` 不需要输入密码。

---

## 后续操作

### 添加新笔记

1. 根据内容类型，将文件放入对应文件夹
   - 架构设计内容 → `architecture/docs/`
   - C++ 笔记 → `cpp/notes/`
   - C++ 代码 → `cpp/code/`
   - C++ 项目 → `cpp/projects/`
2. 按上方"日常编辑与推送"步骤提交

### 从 GitHub 获取最新内容

如果你在其他电脑上更新了内容，想在当前电脑同步：

```bash
git pull
```

### 查看历史提交

```bash
git log --oneline
```

### 撤销修改（谨慎使用）

```bash
# 撤销尚未 add 的修改
git checkout -- 文件名

# 撤销已 add 但尚未 commit 的修改
git reset HEAD 文件名
```

---

## SSH 配置（首次使用）

如果你还没有配置 SSH key，请参考以下步骤：

### 1. 生成 SSH key

```bash
ssh-keygen -t ed25519 -C "hitadao@163.com" -f C:\Users\hr\.ssh\id_ed25519 -N '"'
```

### 2. 启动 ssh-agent 并添加私钥

以管理员身份打开 PowerShell：

```powershell
Get-Service ssh-agent | Set-Service -StartupType Manual
Start-Service ssh-agent
ssh-add C:\Users\hr\.ssh\id_ed25519
```

### 3. 将公钥添加到 GitHub

1. 打开 `C:\Users\hr\.ssh\id_ed25519.pub`，复制内容
2. 登录 [GitHub](https://github.com) → 头像 → Settings → SSH and GPG keys → New SSH key
3. 粘贴公钥，保存

### 4. 测试连接

```bash
ssh -T git@github.com
```

看到 `Hi yeshutong! You've successfully authenticated...` 即成功。

---

## 许可证

本项目采用 [MIT 许可证](LICENSE)。
