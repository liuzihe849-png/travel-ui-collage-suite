# Travel UI Collage Suite

把用户上传的旅行照片制作成「真实照片 × 系统界面」风格的社交媒体海报。Skill 会保留照片中的人物、服装、姿态与场景关系，并根据画面自动选择保留原景或干净点阵画布。

> 这不是纸张拼贴模板，也不会重新生成一个相似的人物。它强调原照片、人物遮挡关系和可读的系统 UI。

## 效果模式

### 1. Photo Overlay｜保留原图

- 保留建筑、风景、光线和拍摄透视。
- 将 AirDrop 风格界面放在人物身后。
- 可让消息输入框等前景 UI 有意识地穿过人物下半身。
- 适合地标、海边、草原、夜景等背景本身有旅行信息的照片。

### 2. Freeform Cutout｜点阵画布

- 从原图中完整提取人物，保留头发、手指、包、鞋和原始动态模糊。
- 使用浅色规则点阵画布。
- 在人物周围安排少量编辑菜单、消息气泡或日历类系统组件。
- 适合背景杂乱，或用户明确要求干净无边画布的照片。

## 核心特性

- 人物身份、脸部、服装、姿态和比例保持不变。
- 自动判断两种画面模式，也可以由用户指定。
- 支持地点、问候语、聊天气泡和 1–3 个用户确认的城市物品。
- UI 与人物具有明确的前后遮挡关系。
- 新增物品不添加投影、发光、深色描边或贴纸边框。
- 不擅自编造日期、航班、价格、预订信息或发送者姓名。
- 默认交付竖版 PNG、分享用 JPG 和简短 QC 记录。

## 安装

### 使用 Skill Installer

在 Codex 中运行：

```text
$skill-installer Install https://github.com/liuzihe849-png/travel-ui-collage-suite
```

### 手动安装

```bash
git clone https://github.com/liuzihe849-png/travel-ui-collage-suite.git \
  "$HOME/.agents/skills/travel-ui-collage-suite"
```

重新启动 Codex 后即可调用。Codex 官方支持从个人 Skills 目录发现 `SKILL.md`。

## 怎么使用

1. 上传一张包含人物的旅行照片。
2. 调用 `$travel-ui-collage-suite`。
3. 写明地点、想加入的物品和文案。`mode` 可以省略，让 Skill 根据照片自动判断。

### 最简调用

```text
$travel-ui-collage-suite
地点：北京
物品：青花瓷茶杯、铜火锅
文案：你来想
```

### 完整调用

```yaml
source_photo: "已上传的旅行照片"
city: "成都"
mode: "auto" # photo-overlay | freeform-cutout | auto
props: ["熊猫", "火锅"]
greeting: "hello Chengdu!!"
question: "where are we going next?"
layout: "portrait 3:4"
```

### 不添加物品

```text
$travel-ui-collage-suite
地点：若尔盖草原
物品：无
文案：你来想
```

## 输入建议

- 尽量使用清晰、完整的人像旅行照片。
- 如果需要保留原场景，确保地标或风景在人物周围仍有可用空间。
- 物品建议控制在 1–3 个，并写具体名称，例如“老北京铜火锅”，不要只写“特色物品”。
- 对文字有严格要求时，请提供最终文案；如果写“你来想”，Skill 可以创作短文案，但不会虚构旅行事实。

## 输出检查

正式交付前应确认：

- 人物脸部、服装、姿态、比例及原始模糊未被重画。
- Photo Overlay 模式中，人物确实遮挡后方界面。
- Freeform Cutout 模式中，背景已移除且人物边缘无白边、光晕或矩形残留。
- 用户选择的物品数量正确，且没有人为投影。
- 所有可见文字拼写正确，没有虚构日期、价格、航班或订单信息。
- 输出尺寸和格式符合用户要求。

## 项目结构

```text
travel-ui-collage-suite/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── confirmed-objects.md
    ├── intake-schema.md
    ├── interface-components.md
    ├── person-compositing.md
    └── style-system.md
```

## 隐私与素材权利

- 仓库不包含用户照片、生成成图或模型权重。
- 使用者应确保自己有权处理和发布上传的照片及其中人物肖像。
- 不要把私人照片、临时文件或输出目录提交到公开仓库。

## 商标说明

本项目是独立创作工具，与 Apple Inc. 无隶属、赞助或认可关系。Apple、AirDrop、iOS、macOS 和 Freeform 是其各自权利人的商标。相关名称仅用于描述界面设计语言与兼容的创作场景。

## License

本项目以 [MIT License](LICENSE) 开源。

