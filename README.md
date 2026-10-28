# ActivityEnergyCounter

根据头显和控制器的运动估算活动能量，并通过 Counters+ 显示。

## 安装

关闭游戏，从 [Releases](https://github.com/StarsWhere/ActivityEnergyCounter/releases) 下载模组包，将包内目录合并到游戏根目录。另需安装兼容版本的 BSIPA、BeatSaberMarkupLanguage、SiraUtil、Counters+，以及单独下载的 [LocalModUI](https://github.com/StarsWhere/LocalModUI/releases)；依赖版本见 [manifest.json](scripts/training_mods/ActivityEnergyCounter/manifest.json)。

## 构建

准备 Windows x64、PowerShell 7、.NET 8 SDK 或更新版本，以及包含上述依赖的 Beat Saber 1.45.2_28848：

~~~powershell
git clone --recurse-submodules https://github.com/StarsWhere/ActivityEnergyCounter
Set-Location ActivityEnergyCounter
pwsh -File scripts/build_release.ps1 -GameRoot 'C:\Games\Beat Saber'
~~~

发布包和校验文件生成在 `releases/`。目标依赖包含本地移植版本；本次拆分未追加游戏内运行或 VR 验证。

原创代码采用 [MIT 许可](LICENSE)，第三方说明见 [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)。
