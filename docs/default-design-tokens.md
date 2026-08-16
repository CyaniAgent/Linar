# Linar — Default Design Tokens

> **本文档定义 Linar 的默认设计令牌（Design Tokens）。**
> 所有令牌均为默认值，用户可通过设置中心或配置文件进行自定义覆盖。
> 颜色系统严格遵循 [Material Design 3 Color System](https://m3.material.io/styles/color) 规范。

---

## 1. 颜色系统

### 1.1 种子颜色（Seed Color）

默认种子颜色用于通过 `material-color-utilities` 动态生成完整配色方案。

```
Seed Color:     #405CFF
Core Primary:   #405CFF
Core Tertiary:  #B37EB6
Core Error:     #FF4F74
```

### 1.2 调色板（Palettes）

MD3 通过种子颜色生成 5 组调色板，每组包含 0–100 共 19 个色阶。调色板是颜色角色（Color Roles）的底层数据源。

#### Primary Palette

| 阶 | 值 | 阶 | 值 |
|----|-----|----|-----|
| 0 | `#000000` | 50 | `#4D67FF` |
| 5 | `#000742` | 60 | `#7487FF` |
| 10 | `#000E5E` | 70 | `#98A5FF` |
| 15 | `#001578` | 80 | `#BBC3FF` |
| 20 | `#001C94` | 90 | `#DEE0FF` |
| 25 | `#0024B1` | 95 | `#F0EFFF` |
| 30 | `#002CCE` | 98 | `#FBF8FF` |
| 35 | `#1438E2` | 99 | `#FFFBFF` |
| 40 | `#2948EE` | 100 | `#FFFFFF` |

#### Secondary Palette

| 阶 | 值 | 阶 | 值 |
|----|-----|----|-----|
| 0 | `#000000` | 50 | `#70759A` |
| 5 | `#080E2E` | 60 | `#8A8EB5` |
| 10 | `#141939` | 70 | `#A4A9D1` |
| 15 | `#1E2344` | 80 | `#C0C4ED` |
| 20 | `#292E4F` | 90 | `#DEE0FF` |
| 25 | `#34395B` | 95 | `#F0EFFF` |
| 30 | `#3F4467` | 98 | `#FBF8FF` |
| 35 | `#4B5073` | 99 | `#FFFBFF` |
| 40 | `#575C80` | 100 | `#FFFFFF` |

#### Tertiary Palette

| 阶 | 值 | 阶 | 值 |
|----|-----|----|-----|
| 0 | `#000000` | 50 | `#98659B` |
| 5 | `#24002B` | 60 | `#B47FB7` |
| 10 | `#320739` | 70 | `#D099D2` |
| 15 | `#3E1344` | 80 | `#EDB3EF` |
| 20 | `#4A1F50` | 90 | `#FFD6FE` |
| 25 | `#562A5C` | 95 | `#FFEBFB` |
| 30 | `#633568` | 98 | `#FFF7FA` |
| 35 | `#704175` | 99 | `#FFFBFF` |
| 40 | `#7D4D81` | 100 | `#FFFFFF` |

#### Neutral Palette

| 阶 | 值 | 阶 | 值 |
|----|-----|----|-----|
| 0 | `#000000` | 50 | `#78767A` |
| 5 | `#111114` | 60 | `#929094` |
| 10 | `#1B1B1F` | 70 | `#ACAAAF` |
| 15 | `#262529` | 80 | `#C8C5CA` |
| 20 | `#303034` | 90 | `#E4E1E6` |
| 25 | `#3B3B3F` | 95 | `#F3F0F4` |
| 30 | `#47464A` | 98 | `#FBF8FD` |
| 35 | `#535256` | 99 | `#FFFBFF` |
| 40 | `#5F5E62` | 100 | `#FFFFFF` |

#### Neutral Variant Palette

| 阶 | 值 | 阶 | 值 |
|----|-----|----|-----|
| 0 | `#000000` | 50 | `#767680` |
| 5 | `#101018` | 60 | `#90909A` |
| 10 | `#1A1B23` | 70 | `#ABAAB4` |
| 15 | `#25252D` | 80 | `#C7C5D0` |
| 20 | `#2F3038` | 90 | `#E3E1EC` |
| 25 | `#3A3B43` | 95 | `#F1EFFA` |
| 30 | `#46464F` | 98 | `#FBF8FF` |
| 35 | `#51525B` | 99 | `#FFFBFF` |
| 40 | `#5E5E67` | 100 | `#FFFFFF` |

### 1.3 颜色角色（Color Roles）— Light Scheme

| Token | 值 | 用途 |
|-------|-----|------|
| `primary` | `#525A92` | 主要操作、重点元素 |
| `onPrimary` | `#FFFFFF` | primary 上的文字/图标 |
| `primaryContainer` | `#DEE0FF` | primary 的容器变体 |
| `onPrimaryContainer` | `#3A4379` | primaryContainer 上的文字 |
| `secondary` | `#5B5D72` | 次要操作、辅助元素 |
| `onSecondary` | `#FFFFFF` | secondary 上的文字 |
| `secondaryContainer` | `#E0E1F9` | secondary 的容器变体 |
| `onSecondaryContainer` | `#434559` | secondaryContainer 上的文字 |
| `tertiary` | `#7B4E7F` | 第三色、强调元素 |
| `onTertiary` | `#FFFFFF` | tertiary 上的文字 |
| `tertiaryContainer` | `#FFD6FE` | tertiary 的容器变体 |
| `onTertiaryContainer` | `#613766` | tertiaryContainer 上的文字 |
| `error` | `#8F4953` | 错误状态 |
| `onError` | `#FFFFFF` | error 上的文字 |
| `errorContainer` | `#FFD9DC` | error 的容器变体 |
| `onErrorContainer` | `#72333D` | errorContainer 上的文字 |
| `background` | `#FBF8FF` | 页面背景 |
| `onBackground` | `#1B1B21` | 背景上的文字 |
| `surface` | `#FBF8FF` | 卡片、面板表面 |
| `onSurface` | `#1B1B21` | surface 上的文字 |
| `surfaceVariant` | `#E3E1EC` | surface 的变体 |
| `onSurfaceVariant` | `#46464F` | surfaceVariant 上的文字 |
| `outline` | `#767680` | 边框线 |
| `outlineVariant` | `#C7C5D0` | 次要边框线 |
| `shadow` | `#000000` | 阴影颜色 |
| `scrim` | `#000000` | 遮罩层颜色 |
| `inverseSurface` | `#303036` | 反色表面（如 Snackbar） |
| `inverseOnSurface` | `#F2EFF7` | 反色表面的文字 |
| `inversePrimary` | `#BBC3FF` | 反色表面的 primary |

#### Surface Container 系列（Light）

| Token | 值 | 用途 |
|-------|-----|------|
| `surfaceDim` | `#DBD9E0` | 较暗的 surface |
| `surfaceBright` | `#FBF8FF` | 较亮的 surface |
| `surfaceContainerLowest` | `#FFFFFF` | 最低层容器（对话框底层） |
| `surfaceContainerLow` | `#F5F2FA` | 低层容器（侧边栏） |
| `surfaceContainer` | `#EFEDF4` | 默认容器（卡片） |
| `surfaceContainerHigh` | `#E9E7EF` | 高层容器（顶栏） |
| `surfaceContainerHighest` | `#E4E1E9` | 最高层容器（搜索栏） |

#### Fixed Color 系列（Light）

| Token | 值 | 用途 |
|-------|-----|------|
| `primaryFixed` | `#DEE0FF` | 固定 primary 色（不受深浅模式影响） |
| `onPrimaryFixed` | `#0C154B` | primaryFixed 上的文字 |
| `primaryFixedDim` | `#BBC3FF` | 固定 primary 色（低饱和） |
| `onPrimaryFixedVariant` | `#3A4379` | primaryFixedDim 上的文字 |
| `secondaryFixed` | `#E0E1F9` | 固定 secondary 色 |
| `onSecondaryFixed` | `#181A2C` | secondaryFixed 上的文字 |
| `secondaryFixedDim` | `#C4C5DD` | 固定 secondary 色（低饱和） |
| `onSecondaryFixedVariant` | `#434559` | secondaryFixedDim 上的文字 |
| `tertiaryFixed` | `#FFD6FE` | 固定 tertiary 色 |
| `onTertiaryFixed` | `#310937` | tertiaryFixed 上的文字 |
| `tertiaryFixedDim` | `#EBB5ED` | 固定 tertiary 色（低饱和） |
| `onTertiaryFixedVariant` | `#613766` | tertiaryFixedDim 上的文字 |

### 1.4 颜色角色（Color Roles）— Dark Scheme

| Token | 值 | 用途 |
|-------|-----|------|
| `primary` | `#BBC3FF` | 主要操作、重点元素 |
| `onPrimary` | `#232C61` | primary 上的文字/图标 |
| `primaryContainer` | `#3A4379` | primary 的容器变体 |
| `onPrimaryContainer` | `#DEE0FF` | primaryContainer 上的文字 |
| `secondary` | `#C4C5DD` | 次要操作、辅助元素 |
| `onSecondary` | `#2D2F42` | secondary 上的文字 |
| `secondaryContainer` | `#434559` | secondary 的容器变体 |
| `onSecondaryContainer` | `#E0E1F9` | secondaryContainer 上的文字 |
| `tertiary` | `#EBB5ED` | 第三色、强调元素 |
| `onTertiary` | `#49204E` | tertiary 上的文字 |
| `tertiaryContainer` | `#613766` | tertiary 的容器变体 |
| `onTertiaryContainer` | `#FFD6FE` | tertiaryContainer 上的文字 |
| `error` | `#FFB2BA` | 错误状态 |
| `onError` | `#561D27` | error 上的文字 |
| `errorContainer` | `#72333D` | error 的容器变体 |
| `onErrorContainer` | `#FFD9DC` | errorContainer 上的文字 |
| `background` | `#131318` | 页面背景 |
| `onBackground` | `#E4E1E9` | 背景上的文字 |
| `surface` | `#131318` | 卡片、面板表面 |
| `onSurface` | `#E4E1E9` | surface 上的文字 |
| `surfaceVariant` | `#46464F` | surface 的变体 |
| `onSurfaceVariant` | `#C7C5D0` | surfaceVariant 上的文字 |
| `outline` | `#90909A` | 边框线 |
| `outlineVariant` | `#46464F` | 次要边框线 |
| `shadow` | `#000000` | 阴影颜色 |
| `scrim` | `#000000` | 遮罩层颜色 |
| `inverseSurface` | `#E4E1E9` | 反色表面 |
| `inverseOnSurface` | `#303036` | 反色表面的文字 |
| `inversePrimary` | `#525A92` | 反色表面的 primary |

#### Surface Container 系列（Dark）

| Token | 值 | 用途 |
|-------|-----|------|
| `surfaceDim` | `#131318` | 较暗的 surface |
| `surfaceBright` | `#39393F` | 较亮的 surface |
| `surfaceContainerLowest` | `#0D0E13` | 最低层容器 |
| `surfaceContainerLow` | `#1B1B21` | 低层容器 |
| `surfaceContainer` | `#1F1F25` | 默认容器 |
| `surfaceContainerHigh` | `#29292F` | 高层容器 |
| `surfaceContainerHighest` | `#34343A` | 最高层容器 |

#### Fixed Color 系列（Dark）

| Token | 值 | 用途 |
|-------|-----|------|
| `primaryFixed` | `#DEE0FF` | 固定 primary 色（与 Light 相同） |
| `onPrimaryFixed` | `#0C154B` | primaryFixed 上的文字 |
| `primaryFixedDim` | `#BBC3FF` | 固定 primary 色（低饱和） |
| `onPrimaryFixedVariant` | `#3A4379` | primaryFixedDim 上的文字 |
| `secondaryFixed` | `#E0E1F9` | 固定 secondary 色 |
| `onSecondaryFixed` | `#181A2C` | secondaryFixed 上的文字 |
| `secondaryFixedDim` | `#C4C5DD` | 固定 secondary 色（低饱和） |
| `onSecondaryFixedVariant` | `#434559` | secondaryFixedDim 上的文字 |
| `tertiaryFixed` | `#FFD6FE` | 固定 tertiary 色 |
| `onTertiaryFixed` | `#310937` | tertiaryFixed 上的文字 |
| `tertiaryFixedDim` | `#EBB5ED` | 固定 tertiary 色（低饱和） |
| `onTertiaryFixedVariant` | `#613766` | tertiaryFixedDim 上的文字 |

### 1.5 高对比度变体（High Contrast Variants）

Linar 支持 **Medium Contrast** 和 **High Contrast** 两档无障碍对比度增强，可通过系统设置切换。

#### Medium Contrast — Light

| Token | 值 |
|-------|-----|
| `primary` | `#293267` |
| `onPrimary` | `#FFFFFF` |
| `primaryContainer` | `#6169A2` |
| `onPrimaryContainer` | `#FFFFFF` |
| `secondary` | `#333548` |
| `tertiary` | `#4F2654` |
| `error` | `#5D222D` |
| `outline` | `#52525B` |
| `outlineVariant` | `#6C6C76` |

#### High Contrast — Light

| Token | 值 |
|-------|-----|
| `primary` | `#1F275C` |
| `onPrimary` | `#FFFFFF` |
| `primaryContainer` | `#3D457B` |
| `onPrimaryContainer` | `#FFFFFF` |
| `secondary` | `#282B3D` |
| `tertiary` | `#441C49` |
| `error` | `#511823` |
| `outline` | `#2B2C34` |
| `outlineVariant` | `#484851` |

#### Medium Contrast — Dark

| Token | 值 |
|-------|-----|
| `primary` | `#D7DAFF` |
| `onPrimary` | `#172055` |
| `primaryContainer` | `#848DC8` |
| `onPrimaryContainer` | `#000000` |
| `secondary` | `#DADAF3` |
| `tertiary` | `#FFCCFF` |
| `error` | `#FFD1D5` |
| `outline` | `#B2B1BB` |
| `outlineVariant` | `#908F99` |

#### High Contrast — Dark

| Token | 值 |
|-------|-----|
| `primary` | `#EFEEFF` |
| `onPrimary` | `#000000` |
| `primaryContainer` | `#B6BFFD` |
| `onPrimaryContainer` | `#000533` |
| `secondary` | `#EFEEFF` |
| `tertiary` | `#FFEAFB` |
| `error` | `#FFEBEC` |
| `outline` | `#F1EFFA` |
| `outlineVariant` | `#C3C1CC` |

### 1.6 扩展颜色（Extended Colors）

Linar 支持用户自定义扩展颜色，以下为默认扩展色。

| 名称 | 值 | 协调化 | 用途 |
|------|-----|--------|------|
| Miku Green | `#39C5BB` | 否 | 品牌色 / 强调色 |

> 扩展颜色在运行时通过 `material-color-utilities` 的 Harmonization 算法自动协调到当前配色方案中。

---

## 2. 排版系统（Typography）

MD3 排版比例尺基于 Roboto / Noto Sans 字族，默认字体可在配置中替换。

### 2.1 Display

| 规模 | 字号 | 字距 | 字重 | 行高 |
|------|------|------|------|------|
| Display Large | 57px | -0.25px | 400 (Regular) | 64px |
| Display Medium | 45px | 0px | 400 | 52px |
| Display Small | 36px | 0px | 400 | 44px |

### 2.2 Headline

| 规模 | 字号 | 字距 | 字重 | 行高 |
|------|------|------|------|------|
| Headline Large | 32px | 0px | 400 | 40px |
| Headline Medium | 28px | 0px | 400 | 36px |
| Headline Small | 24px | 0px | 400 | 32px |

### 2.3 Title

| 规模 | 字号 | 字距 | 字重 | 行高 |
|------|------|------|------|------|
| Title Large | 22px | 0px | 400 | 28px |
| Title Medium | 16px | 0.15px | 500 (Medium) | 24px |
| Title Small | 14px | 0.1px | 500 | 20px |

### 2.4 Body

| 规模 | 字号 | 字距 | 字重 | 行高 |
|------|------|------|------|------|
| Body Large | 16px | 0.5px | 400 | 24px |
| Body Medium | 14px | 0.25px | 400 | 20px |
| Body Small | 12px | 0.4px | 400 | 16px |

### 2.5 Label

| 规模 | 字号 | 字距 | 字重 | 行高 |
|------|------|------|------|------|
| Label Large | 14px | 0.1px | 500 | 20px |
| Label Medium | 12px | 0.5px | 500 | 16px |
| Label Small | 11px | 0.5px | 500 | 16px |

---

## 3. 形状系统（Shape）

圆角比例尺，从 Sharp 到 Extra Large 逐级增大。

| Token | 值 | 典型用途 |
|-------|-----|----------|
| `none` | 0dp | 无圆角 |
| `extraSmall` | 4dp | 按钮内部元素 |
| `small` | 8dp | 按钮、Chip、搜索栏 |
| `medium` | 12dp | 卡片、底栏 |
| `large` | 16dp | 侧边栏、底部 Sheet |
| `extraLarge` | 28dp | 对话框、底部 Sheet |
| `full` | 9999dp | 药丸形元素（FAB、头像） |

---

## 4. 阴影与高度（Elevation）

MD3 使用高度层级（Elevation Level）而非具体 dp 值来表达层级关系。在 MD3 中，Elevation 主要通过 **Tinted Surface** 实现，而非传统阴影。

| Level | 值 | 用途 | Tint 不透明度 |
|-------|-----|------|--------------|
| Level 0 | 0dp | 纯平表面 | 0% |
| Level 1 | 1dp | 按钮、卡片（resting） | 5% |
| Level 2 | 3dp | 卡片（hover）、底部导航栏 | 8% |
| Level 3 | 6dp | 菜单、侧边栏 | 11% |
| Level 4 | 8dp | 对话框、浮动面板 | 12% |
| Level 5 | 12dp | 导航抽屉、底部 Sheet | 14% |

---

## 5. 状态层（State Layers）

交互状态通过叠加半透明层实现。

| 状态 | 不透明度 | 说明 |
|------|----------|------|
| Hover | 8% | 鼠标悬停 |
| Focus | 10% | 键盘聚焦 |
| Pressed | 10% | 点击/触摸 |
| Dragged | 16% | 拖拽中 |
| Disabled | 12% (容器) / 38% (文字) | 禁用状态 |

---

## 6. 动效系统（Motion）

### 6.1 曲线（Curves）

| Token | 值 | 用途 |
|-------|-----|------|
| `standard` | `cubic-bezier(0.2, 0, 0, 1)` | 标准过渡（位移、缩放） |
| `standardDecelerate` | `cubic-bezier(0, 0, 0, 1)` | 进入动画 |
| `standardAccelerate` | `cubic-bezier(0.3, 0, 1, 1)` | 退出动画 |
| `emphasized` | `cubic-bezier(0.2, 0, 0, 1)` | 强调过渡（大面积变化） |
| `emphasizedDecelerate` | `cubic-bezier(0.05, 0.7, 0.1, 1)` | 强调进入 |
| `emphasizedAccelerate` | `cubic-bezier(0.3, 0, 0.8, 0.15)` | 强调退出 |

### 6.2 持续时间（Duration）

| Token | 值 | 用途 |
|-------|-----|------|
| `durationShort1` | 50ms | 微小状态变化 |
| `durationShort2` | 100ms | 小元素交互反馈 |
| `durationShort3` | 150ms | 按钮状态变化 |
| `durationShort4` | 200ms | 短暂过渡 |
| `durationMedium1` | 250ms | 中等过渡（展开/折叠） |
| `durationMedium2` | 300ms | 卡片展开、页面切换 |
| `durationMedium3` | 350ms | 较大区域变化 |
| `durationMedium4` | 400ms | 大面积布局调整 |
| `durationLong1` | 450ms | 长过渡开始 |
| `durationLong2` | 500ms | 页面间导航 |
| `durationLong3` | 550ms | 复杂动画 |
| `durationLong4` | 600ms | 大型过渡 |
| `durationExtraLong1` | 700ms | 特殊场景 |
| `durationExtraLong2` | 800ms | 特殊场景 |
| `durationExtraLong3` | 900ms | 特殊场景 |
| `durationExtraLong4` | 1000ms | 特殊场景 |

---

## 7. 图标（Icons）

### 7.1 默认图标集

- **Material Symbols Rounded**（Variable Font）
- 尺寸：24dp（默认） / 20dp（小） / 40dp（大）
- 权重范围：100–700

### 7.2 图标颜色映射

| 场景 | Token |
|------|-------|
| 活动状态图标 | `primary` |
| 非活动状态图标 | `onSurfaceVariant` |
| 禁用图标 | `onSurface` × 38% |
| 图标按钮（filled） | `primary` |
| 图标按钮（outlined） | `onSurfaceVariant` |

---

## 8. 可配置性说明

### 8.1 覆盖机制

所有设计令牌均为默认值，可通过以下方式覆盖：

1. **用户设置**：通过 Linar Settings 的「外观」面板修改主题
2. **配置文件**：`~/.config/linar/theme.json` 自定义令牌
3. **壁纸提取**：启动时从壁纸自动提取种子颜色，重新生成配色方案

### 8.2 配置文件示例

```json
{
  "seedColor": "#405CFF",
  "contrastLevel": "standard",
  "themeMode": "system",
  "typography": {
    "fontFamily": "Noto Sans SC",
    "scaleFactor": 1.0
  },
  "shape": {
    "cornerRadius": "medium"
  }
}
```

### 8.3 动态主题流程

```
壁纸图片
  ↓
提取种子颜色（material-color-utilities）
  ↓
生成 Primary / Secondary / Tertiary / Neutral / Neutral-Variant 调色板
  ↓
映射到 Light / Dark / Medium-Contrast / High-Contrast 颜色角色
  ↓
应用到所有 QML 组件
```
