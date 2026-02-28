# 打地鼠游戏 - 自动构建 APK

一个有趣的 HTML5 打地鼠游戏,支持在 Android 手机上运行。

## 🎮 游戏特性

- 三种难度模式(简单/中等/困难)
- 本地最高分记录
- 响应式设计,完美适配手机
- 触摸优化,流畅动画
- 打击音效反馈
- 30秒限时挑战

## 📱 如何获取 APK

### 方法 1: 从 GitHub Actions 下载 (推荐)

1. **创建 GitHub 仓库并推送代码:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Whack-a-Mole game"
   # 在 GitHub 上创建一个新仓库,然后:
   git remote add origin https://github.com/你的用户名/仓库名.git
   git branch -M master
   git push -u origin master
   ```

2. **触发构建:**
   - 代码推送到 GitHub 后,会自动触发构建
   - 访问你的仓库页面
   - 点击 "Actions" 标签
   - 等待构建完成(约 5-10 分钟)
   - 在构建任务的 "Artifacts" 部分下载 `WhackAMole-APK`

3. **安装到手机:**
   - 将下载的 APK 传输到 Android 手机
   - 在手机上打开 APK 文件
   - 允许安装未知来源应用
   - 安装并开始游戏!

### 方法 2: 手动触发构建

1. 推送代码到 GitHub 后
2. 访问仓库的 "Actions" 页面
3. 选择 "Build Android APK" 工作流
4. 点击 "Run workflow" 按钮
5. 等待构建完成
6. 在 Artifacts 中下载 APK

## 🛠️ 本地构建

如果你想本地构建 APK:

```bash
# 安装依赖 (macOS)
brew install android-sdk openjdk

# 配置环境变量
export ANDROID_HOME=$HOME/Library/Android/sdk
export JAVA_HOME=$(/usr/libexec/java_home -v 17)

# 安装 Cordova
npm install -g cordova

# 复制游戏文件
cp whack-a-mole.html www/index.html

# 添加 Android 平台
cordova platform add android

# 构建 APK
cordova build android

# APK 位于: platforms/android/app/build/outputs/apk/debug/app-debug.apk
```

## 📖 游戏玩法

1. 选择难度(简单/中等/困难)
2. 点击"开始游戏"
3. 地鼠会从 9 个洞中随机出现
4. 快速点击地鼠得分(+10 分)
5. 在 30 秒内尽可能获得高分!

## 🎯 自定义游戏

### 修改游戏时间
在 `whack-a-mole.html` 中:
```javascript
timeLeft = 30;  // 改为你想要的秒数
```

### 修改难度
```javascript
const difficultySettings = {
    easy: { moleInterval: 1500, moleStayTime: 1200 },
    medium: { moleInterval: 1000, moleStayTime: 900 },
    hard: { moleInterval: 700, moleStayTime: 600 }
};
```

### 修改得分
```javascript
score += 10;  // 改为你想要的分数
```

## 📋 系统要求

- Android 5.0 (API 22) 或更高版本
- 支持触摸屏设备

## 📄 许可证

MIT License - 自由使用和修改

## 🙏 致谢

使用纯 HTML5、CSS3 和 JavaScript 构建,通过 Apache Cordova 打包为 Android 应用。

---

**享受游戏! 🎮**
