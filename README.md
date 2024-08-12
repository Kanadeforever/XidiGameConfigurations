# Readme说明

本文档仅为主分支的英译中版，如有更新以主分支内容为准。

# Xidi 游戏配置

此存储库包含用于 [Xidi](https://www.github.com/samuelgr/Xidi) 的特定游戏配置文件。每个配置文件都包括推荐的映射器配置以及有关如何最好地使游戏与 Xidi 一起工作的文档。


## 使用

要使用此存储库中包含的配置文件：

1. 下载 Xidi 的[最新版本](https://github.com/samuelgr/Xidi/releases)。

1. 在此存储库的 [GameConfigurations 目录](https://github.com/samuelgr/XidiGameConfigurations/tree/master/GameConfigurations) 中查找所需的游戏标题。

1. 检查其中包含的名为 `Xidi.ini` 的配置文件，以了解所需的 Xidi 版本和形式。
   - 通常所需的版本至少为 v3.0.0。
   - 形式将是 DInput、DInput8、WinMM 或 HookModule + 其他形式之一。有关如何安装不同形式的 Xidi 的更多信息，请参见 [Xidi 的形式](https://github.com/samuelgr/Xidi#forms-of-xidi)。

1. 下载配置文件并将其放置在与游戏形式的 Xidi 相同的目录中。
   - 例如，如果游戏可执行文件位于 `C:\MyFancyGame\App.exe`，而 Xidi 的形式位于 `C:\MyFancyGame\dinput8.dll`，则配置文件应为 `C:\MyFancyGame\Xidi.ini`。
   - 有关配置文件及其放置位置的更多信息，请参见 [配置 Xidi](https://github.com/samuelgr/Xidi#configuring-xidi)。


## 贡献

欢迎并鼓励向此存储库贡献游戏配置！有两种方式可以做到这一点。

1. **提交拉取请求。** 这需要使用 `git` 命令克隆此存储库，提交一个或多个更改，将更改推送回 GitHub，然后在 GitHub 上创建拉取请求。

2. **创建一个问题**，使用“配置文件提交”问题模板。填写所需的详细信息，并将建议的配置文件直接粘贴到问题本身中。

选项 1 是首选的，并且对于较多的配置文件来说是最好的，但选项 2 也适用于那些不熟悉 `git` 工作流程或更喜欢简单操作的人。

无论选择哪种提交方式，作为作者列在任何提交的配置上的贡献者都需要同意将他们的贡献根据与此存储库使用的相同的 3 条款 BSD 许可证授权给我（samuelgr）。


### 格式说明

此存储库中的配置文件必须以顶部的注释块开头，配置本身在其下方。注释块标识游戏、Xidi 形式、测试的 Xidi 版本、作者等。

以下是顶部注释部分的模板，可以直接复制粘贴作为开始的简便方法。

中文版：

```ini
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; （在此处填写应用程序/游戏名称）
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; Xidi 版本:     （你用于测试的 Xidi 版本？）
; Xidi 形式:     （此游戏使用的 Xidi 形式？ - 参见说明）
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; 作者:          （贡献者的名字/GitHub 用户名，逗号分隔）
; 最后修改:      （最后编辑日期，格式为 M/D/YYYY）
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
```

原英文版：

```ini
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; (application/game name here)
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; Xidi Version:     (which Xidi version did you use for testing?)
; Xidi Form:        (which form of Xidi does this game use? - see instructions)
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
; Authors:          (comma-separated lsit of names/GitHub usernames for anyone who contributed)
; Last Modified:    (last edit date in M/D/YYYY)
;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;;
```

 - 对于 **Xidi 版本**，仅使用裸版本，例如“4.1.1”。只允许官方发布的版本，不允许开发或其他一次性构建。
 - 对于 **Xidi 形式**，指明此应用程序需要哪种形式的 Xidi。根据需要选择以下之一。
    - `DInput`
    - `DInput8`
    - `WinMM`
    - `HookModule + DInput`
    - `HookModule + DInput8`
    - `HookModule + WinMM`

在注释部分之后是**两个空行**，然后是配置文件内容的其余部分。有关行间距和格式的具体期望，请参阅此存储库中现有配置文件的格式，但一般规则是**部分之间有两个空行**，**相关设置组之间有一个空行**，例如相关应用内控件的元素映射器配置。
