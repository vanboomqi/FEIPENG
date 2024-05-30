# 飞蓬 - Cobalt Strike 插件

## 简介

飞蓬是一款为 Cobalt Strike 设计的插件，集成了多种 PowerShell 脚本和 C# 程序，所有文件均支持不落地执行。通过远程加载 DLL 实现这一功能，需要在 web 目录中开启网页服务，并在 config 文件中配置对应的地址。

## 功能

- 集成多种 PowerShell 脚本和 C# 程序
- 支持不落地执行，增强隐蔽性（如 frp, fscan）
- 通过远程加载 DLL 实现高效部署
- 便于在 Cobalt Strike 中快速使用

## 使用说明

1. **开启网页服务**：确保 web 目录开启网页服务，以便插件能远程加载 DLL。

2. **配置地址**：在插件的 config 文件中，将地址修改为 web 目录的地址，以便正确加载所需文件。

    ```plaintext
    # config 文件示例
    $url = "http://example.com";
    ```

## 参考

- 远程加载 DLL 功能参考了 [DInvoke](https://github.com/TheWover/DInvoke) 项目。
- Cobalt Strike 插件部分参考了 [LSTAR](https://github.com/lintstar/LSTAR) 项目。

## 注意事项

- 请在使用前测试脚本和程序，以确保其在目标环境中能够正常运行。
- 部分文件来源于网络，使用前请自行进行安全性测试。
- 使用不落地执行技术时，注意防止脚本和程序被检测和拦截。

## 贡献

欢迎贡献和反馈！如果你有任何改进建议或发现任何问题，请提交 issue 或 pull request。

