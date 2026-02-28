# 如何快速获得打地鼠游戏的 APK 文件

## 方法一:使用在线网站转换 (最简单,无需安装任何工具)

### 1. PWABuilder.com (推荐)

**步骤:**
1. 访问 https://www.pwabuilder.com/
2. 输入你的 HTML 文件 URL,或者选择"Upload"上传 `whack-a-mole.html`
3. 点击"Generate"
4. 选择"Android"图标
5. 下载生成的 APK 文件
6. 将 APK 传输到手机安装即可

### 2. Website 2 APK Builder (网页版)

**步骤:**
1. 访问 https://www.website2apk.com/
2. 上传你的 HTML 文件
3. 填写应用信息:
   - 应用名称: 打地鼠
   - 包名: com.whackamole.game
   - 版本: 1.0
4. 点击"Convert to APK"
5. 等待生成并下载

### 3. APK Editor Online

**步骤:**
1. 访问 https://apkeditor.com/
2. 选择"HTML to APK"
3. 上传 `whack-a-mole.html`
4. 配置应用信息
5. 生成并下载 APK

## 方法二:使用 Android App (手机上直接生成)

### Website 2 APK Builder App

**步骤:**
1. 在 Google Play 搜索 "Website 2 APK Builder"
2. 安装该应用
3. 打开应用
4. 选择"Local File"选项
5. 浏览并选择手机中的 `whack-a-mole.html`
6. 配置应用信息:
   - App Name: 打地鼠
   - Package Name: com.whackamole.game
   - Version: 1.0
   - Orientation: Portrait(竖屏)
7. 点击"Generate APK"
8. 等待生成完成
9. APK 会保存在 `Website2APK/` 文件夹中

### Web2Apk

**步骤:**
1. 在 Google Play 搜索 "Web2Apk"
2. 安装并打开应用
3. 输入应用名称"打地鼠"
4. 选择"From File"
5. 选择 `whack-a-mole.html`
6. 点击"Create APK"
7. 等待生成并安装

## 方法三:使用 GitHub + GitHub Actions (自动构建)

如果你熟悉 GitHub,可以设置自动构建:

1. 将文件上传到 GitHub 仓库
2. 在仓库设置中添加 GitHub Actions
3. 配置自动构建 APK 的工作流
4. 每次推送代码自动生成 APK

## 方法四:本地构建 (需要安装开发环境)

如果你愿意安装开发工具,可以使用:

### 使用 Cordova (最简单)

```bash
# 1. 安装 Node.js (从 nodejs.org 下载安装)

# 2. 安装 Cordova
npm install -g cordova

# 3. 创建项目
cordova create WhackAMole com.whackamole.game 打地鼠
cd WhackAMole

# 4. 添加 Android 平台
cordova platform add android

# 5. 将 whack-a-mole.html 复制到 www/ 目录并重命名为 index.html

# 6. 构建 APK
cordova build android

# 7. APK 位于 platforms/android/app/build/outputs/apk/debug/app-debug.apk
```

## 推荐方案

**最快最简单:**
- 使用 PWABuilder.com (约 5 分钟)
- 或者使用手机安装 "Website 2 APK Builder" 应用 (约 10 分钟)

**最专业:**
- 本地安装 Cordova 构建(首次安装需要 30 分钟,之后构建只需 5 分钟)

## 注意事项

1. **首次安装可能需要允许"未知来源"应用**
   - 设置 → 安全 → 允许从未知来源安装

2. **APK 签名**
   - 在线生成的 APK 可能需要签名才能在所有设备上安装
   - Cordova 构建的 debug APK 可以直接安装

3. **应用权限**
   - 游戏不需要任何特殊权限
   - 打包工具可能会添加网络权限,这是正常的

4. **文件大小**
   - 生成的 APK 通常在 5-15MB 之间
   - 主要大小来自打包的 WebView 组件

## 常见问题

**Q: APK 无法安装?**
A: 检查手机设置中是否允许安装未知来源应用

**Q: 游戏无法全屏?**
A: 某些打包工具需要在设置中启用全屏模式

**Q: 音效无法播放?**
A: Android 可能需要用户交互后才能播放声音,确保先点击屏幕

**Q: 想要发布到应用商店?**
A: 需要生成签名版本的 APK,推荐使用 Cordova 或 Capacitor 本地构建

## 快速测试

如果只是想快速测试游戏,不需要打包 APK:

1. 将 `whack-a-mole.html` 发送到手机(微信、QQ、邮件等)
2. 用手机浏览器打开该文件
3. 点击浏览器菜单 → "添加到主屏幕"
4. 就像原生应用一样使用了!
