## 电脑环境配置

**CPU**: Dual-Core Intel i5

**macOS**: Ventura 13.6.3

**VPN**: PandaFan

## Homebrew & FFmpeg安装

在中国安装 Homebrew 时，由于访问国外服务器可能受到网络限制，您可以通过设置使用国内的镜像源来加速安装。以下是使用清华大学的镜像源进行安装的步骤：

1. **安装 Homebrew：** 打开终端应用程序，并运行以下命令以安装 Homebrew：

   ```
   /bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/Homebrew/install@master/install.sh)"
   ```

   如果您使用的是 macOS 11.0（Big Sur）或更高版本，请使用以下命令：

   ```
   /bin/bash -c "$(curl -fsSL https://cdn.jsdelivr.net/gh/Homebrew/install@master/install.sh --insecure)"
   ```

   这会下载并运行 Homebrew 安装脚本。

2. **设置镜像源：** Homebrew 默认从 GitHub 下载软件包，但您可以设置使用国内的镜像源，例如清华大学的镜像源。运行以下命令来设置：

   ```
   cd "$(brew --repo)"
   git remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/brew.git
   ```

3. **更新 Homebrew：** 更新 Homebrew，以确保使用了新的镜像源：

   ```
   brew update
   ```

   这将同步 Homebrew 的本地库信息。

4. **安装软件包：** 使用 Homebrew 安装软件包，例如 FFmpeg，可以运行：

   ```
   brew install ffmpeg
   ```

   这将使用国内的镜像源下载并安装 FFmpeg。

请注意，中国境内的网络环境可能会导致访问 GitHub 的速度较慢或被阻塞。使用国内的镜像源可以解决这个问题。如果您在将来的使用中遇到了其他软件包需要安装，同样可以通过 Homebrew 进行安装，并按照上述步骤设置镜像源。