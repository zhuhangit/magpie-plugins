# Zoo Code (IDEA)

将 magpie 模型接入 Zoo Code 的 JetBrains 插件。连接后，可在 Zoo Code 内切换 magpie 提供的模型。

## 安装

```sh
magpie plugin add /path/to/magpie-plugins/zoo-code-idea
```

Windows PowerShell：

```powershell
magpie plugin add "$env:USERPROFILE\.config\magpie-plugins\zoo-code-idea"
```

## 使用

1. 在 magpie 的 **Agents** 页面，为 **Zoo Code (IDEA)** 选择模型。
2. 重启 Zoo Code 会话或 IDEA，使配置生效。
3. 断开并还原原配置：

```sh
magpie zoo-code-idea default
```

## 配置说明

- 连接时，Zoo Code 的模型档位表会替换为 magpie 当前提供的模型；magpie 选中的模型作为默认档位。该档位表不会与原有档位合并。
- 其它供应商的 API key 等配置保持不变。断开时，magpie 会还原连接前保存的原配置（包括原模型档位表）。
- 配置写入 `~/.zoo-code/secrets.json`，不会即时刷新；切换模型或连接状态后需重启 Zoo Code 会话或 IDEA。
- 本插件接入的是 JetBrains 版 Zoo Code；magpie 内置的 Zoo Code 接线适用于 VS Code，不由本插件配置。
