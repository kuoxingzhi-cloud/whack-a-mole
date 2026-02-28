# 🎮 打地鼠游戏 - 快速获取 APK 指南

## ✅ 我已经为你准备好了什么

- ✅ 完整的 HTML5 打地鼠游戏代码
- ✅ GitHub Actions 自动构建工作流
- ✅ Git 仓库已初始化并提交

## 📥 现在只需要 3 步就能获得 APK

### 第 1 步:在 GitHub 上创建新仓库

1. 访问 https://github.com/new
2. 仓库名称填写: `whack-a-mole` (或其他你喜欢的名字)
3. 选择 **Public** (公开仓库)
4. **不要**勾选 "Add a README file"
5. 点击 "Create repository"

### 第 2 步:推送代码到 GitHub

在终端中运行以下命令(替换 `YOUR_USERNAME` 为你的 GitHub 用户名):

```bash
# 进入项目目录
cd /Users/ryan/ZCodeProject

# 添加 GitHub 仓库地址(替换下面的地址)
git remote add origin https://github.com/YOUR_USERNAME/whack-a-mole.git

# 推送代码到 GitHub
git push -u origin master
```

**如果遇到认证问题:**
- 使用 Personal Access Token:
  1. 访问 https://github.com/settings/tokens
  2. 点击 "Generate new token" → "Generate new token (classic)"
  3. 勾选 `repo` 权限
  4. 生成并复制 token
  5. 推送时,用户名输入你的 GitHub 用户名,密码输入这个 token

### 第 3 步:下载构建好的 APK

1. 访问你刚创建的 GitHub 仓库页面
2. 点击顶部的 **"Actions"** 标签
3. 你会看到 "Build Android APK" 工作流正在运行(黄色圆点)
4. 等待约 **5-10 分钟**直到变成绿色对勾 ✓
5. 点击进入这次构建
6. 滚动到底部的 **"Artifacts"** 部分
7. 点击 **"WhackAMole-APK"** 下载 ZIP 文件
8. 解压 ZIP 文件,里面就是 `WhackAMole-release.apk`

## 📱 安装到手机

1. 将 APK 文件传输到 Android 手机(微信、QQ、数据线等)
2. 在手机上点击 APK 文件
3. 如果提示"禁止安装未知应用",点击"设置"并允许
4. 点击"安装"
5. 安装完成后,点击"打开"开始游戏! 🎮

## 🎯 游戏操作

- **选择难度**: 简单/中等/困难
- **开始游戏**: 点击"开始游戏"按钮
- **打地鼠**: 快速点击出现的地鼠 🐹
- **得分**: 每打中一只地鼠得 10 分
- **目标**: 在 30 秒内获得尽可能高的分数!

## ⚙️ 如果需要重新构建

修改代码后,推送到 GitHub 会自动触发新的构建:

```bash
git add .
git commit -m "Update game"
git push
```

或者手动触发:
1. 访问仓库的 "Actions" 页面
2. 选择 "Build Android APK"
3. 点击 "Run workflow" → "Run workflow"

## 🔧 自定义游戏

所有代码都在 `whack-a-mole.html` 文件中,你可以修改:

- **游戏时长**: 修改 `timeLeft = 30` 为其他秒数
- **得分**: 修改 `score += 10` 为其他分数
- **难度设置**: 修改 `difficultySettings` 对象中的数值

修改后推送代码,会自动构建新的 APK!

## 📞 需要帮助?

- 如果 Actions 构建失败,查看构建日志了解错误
- 如果 APK 无法安装,确保手机允许安装未知来源应用
- 如果游戏有问题,检查 `whack-a-mole.html` 代码

---

**祝你玩得开心! 🎉**
