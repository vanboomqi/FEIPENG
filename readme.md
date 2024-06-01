# 飞蓬 - Cobalt Strike 插件

## 简介

飞蓬是一款为 Cobalt Strike 设计的插件，集成了多种 PowerShell 脚本和 C# 程序，所有文件均支持不落地执行。通过远程加载 DLL 实现这一功能，需要在 web 目录中开启网页服务，并在 config 文件中配置对应的地址。

## 功能

- 集成多种 PowerShell 脚本和 C# 程序
- 支持不落地执行，增强隐蔽性（如 frp, fscan, HackBrowserData）
- 通过远程加载 DLL 实现高效部署
- 便于在 Cobalt Strike 中快速使用

## 使用说明

1. **开启网页服务**：确保 web 目录开启网页服务，以便插件能远程加载 DLL。

2. **配置地址**：在插件的 config 文件中，将地址修改为 web 目录的地址，以便正确加载所需文件。

    ```plaintext
    # config 文件示例
    $url = "http://example.com";
    ```

3. **远程加载 DLL 模块**：飞蓬插件包含多个远程加载 DLL 模块，如 frp、fscan 和 HackBrowserData。

## 兼容性

远程加载 DLL 模块兼容以下操作系统：

- Windows 7
- Windows 10
- Windows 11
- Windows Server 2012
- Windows Server 2016
- Windows Server 2019
- Windows Server 2022

### 系统要求

- 加载器最低要求 .NET Framework 3.5。

### Windows 7 注意事项

在 Windows 7 上使用时，可能会遇到以下错误：

Attempting to enable TLS 1.2... 

Error enabling TLS 1.2: 不支持请求的安全协议。

这是由于 Windows 7 未更新补丁导致不支持 TLS 1.2。解决方法是将网页服务设置为最低支持 TLS 1.0 即可正常使用。

## 参考

- 远程加载 DLL 功能参考了 [DInvoke](https://github.com/TheWover/DInvoke) 项目。
- Cobalt Strike 插件部分参考了 [LSTAR](https://github.com/lintstar/LSTAR) 项目。

## 注意事项

- 请在使用前测试脚本和程序，以确保其在目标环境中能够正常运行。
- 部分文件来源于网络，使用前请自行进行安全性测试。
- 使用不落地执行技术时，注意防止脚本和程序被检测和拦截。

## 贡献

欢迎贡献和反馈！如果你有任何改进建议或发现任何问题，请提交 issue 或 pull request。

