# MerchantBlacklist / 商店黑名单

> Slay the Spire 2 mod — local-only merchant inventory blacklist for relics & potions.
> 本机商店遗物 / 药水黑名单过滤器。

**Compatible with STS2 0.107** · **MIT License** · `affects_gameplay = false`

---

## English

### What it does

Filters blacklisted relics and potions out of **the local player's** merchant
inventory (normal merchant + ancient merchant).

- View-only, local-only filter — never modifies world state.
- Never touches elite / boss / chest / event rewards.
- Sends no network messages, the other player sees nothing.
- Multiplayer-safe.

### Features

- **Pause menu entry** — adds a "Shop Blacklist" button to the pause menu, right
  under "Settings". Clones the native pause-menu button so the visuals match
  the rest of the menu.
- **Native compendium-style panel** — relics and potions are rendered via the
  game's own `NRelic` / `NPotion` widgets, so hover tooltips and shaders work
  exactly like the in-game compendium. Each rarity group has *Allow all* /
  *Ban all* shortcuts.
- **Right-click to ban inside the shop** — at any merchant, right-click a relic
  or potion in stock to ban it. The slot is hidden immediately.
- **Default hotkey: `F10`** — toggles the panel. Rebindable through
  [ModConfig](https://github.com/CursedStudio/ModConfig) and integrated with
  [STS2-RitsuLib](https://github.com/CursedStudio/STS2-RitsuLib)'s runtime
  hotkey router (text-input / dev-console aware).
- **Localized UI** — follows the client language (English / Simplified Chinese
  / Traditional Chinese). Switching language in-game live-updates the ModConfig
  panel labels.

### Install

1. Subscribe / install dependencies:
   - **STS2-RitsuLib** (any 0.4.24 variant pack version that targets your game version)
   - **ModConfig** v0.2.3 *(optional, only needed if you want to rebind the hotkey)*
2. Drop the contents of `MerchantBlacklist_v0.1.0.zip` into:
   ```
   <Steam>/steamapps/common/Slay the Spire 2/mods/MerchantBlacklist/
   ```
   So the folder ends up containing `MerchantBlacklist.dll` and
   `mod_manifest.json` directly.
3. Launch the game, enable the mod from the mod list.

### Usage

| Action | Where |
| --- | --- |
| Open / close the blacklist panel | Pause menu → "Shop Blacklist", or press `F10` |
| Ban a relic / potion | Click its icon in the panel, **or** right-click it in any merchant |
| Unban | Click its (greyed) icon in the panel again |
| Allow / ban a whole rarity group | Use the *Allow all* / *Ban all* buttons in each group |
| Rebind hotkey | Settings → ModConfig → "Shop Blacklist" → *Toggle Shop Blacklist* |

### Build from source

```powershell
# Debug build + deploy to your local mods folder
.\build.ps1 -Configuration Debug

# Release build (writes torelease/ snapshot)
.\build.ps1 -Configuration Release
```

`torelease/` and `release/` are local-only and never committed.

---

## 简体中文

### 功能简述

仅在 **本机玩家自己的商店**（普通商人 + 先古商人）库存生成时，把已拉黑的遗物和
药水筛掉。

- 纯视图过滤，不改世界状态。
- 不影响精英 / Boss / 宝箱 / 事件奖励。
- 不发任何网络消息，对端零感知，联机安全。

### 特性

- **暂停菜单入口**：在「设置」按钮正下方注入「商店黑名单」按钮，复用原生
  Material，外观与暂停菜单一致。
- **原生百科风面板**：遗物 / 药水使用游戏自己的 `NRelic` / `NPotion` 组件渲染，
  悬浮 tooltip、shader 高亮与百科一致。每个稀有度组带「全启用 / 全 ban」快捷按钮。
- **商店内右键即时拉黑**：在商人界面，对任意遗物或药水图标按右键即可拉黑，
  对应槽位会立即隐藏。
- **默认热键 `F10`**：切换面板。可通过
  [ModConfig](https://github.com/CursedStudio/ModConfig) 改键，并与
  [STS2-RitsuLib](https://github.com/CursedStudio/STS2-RitsuLib) 的运行时热键路由器
  对接（文本输入 / 开发控制台时自动屏蔽）。
- **跟随客户端语言显示中 / 英文**：游戏内切换语言时，ModConfig 面板里的标签会
  实时刷新。

### 安装

1. 安装依赖：
   - **STS2-RitsuLib**（与你的游戏版本匹配的 variant-pack 版本）
   - **ModConfig** v0.2.3（可选，需要改键时安装）
2. 把 `MerchantBlacklist_v0.1.0.zip` 解压到：
   ```
   <Steam>/steamapps/common/Slay the Spire 2/mods/MerchantBlacklist/
   ```
   该目录下应直接包含 `MerchantBlacklist.dll` 和 `mod_manifest.json`。
3. 启动游戏，在 mod 列表里启用即可。

### 使用方式

| 操作 | 位置 |
| --- | --- |
| 打开 / 关闭黑名单面板 | 暂停菜单 →「商店黑名单」，或按 `F10` |
| 拉黑遗物 / 药水 | 在面板里点击它，**或**在商人界面对它按右键 |
| 取消拉黑 | 在面板里再次点击对应（变暗）的图标 |
| 整组启用 / 拉黑 | 每个稀有度组里有「全启用 / 全 ban」按钮 |
| 改键 | 设置 → ModConfig → 「商店黑名单」→「切换商店黑名单」 |

### 从源码构建

```powershell
# Debug 构建并部署到本机 mods 目录
.\build.ps1 -Configuration Debug

# Release 构建（同时写入 torelease/ 快照）
.\build.ps1 -Configuration Release
```

`torelease/` 和 `release/` 仅本地保留，不会进 Git。

---

## License

MIT — see [LICENSE](./LICENSE).