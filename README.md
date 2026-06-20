# 🎬 AI 短剧生成器 - 森林奇兵

基于 Agnes AI + Hermes Agent 的 AI 短剧全流程生成项目。

## 项目简介

**《森林奇兵》** 是一部 3D 卡通风格的幽默搞笑短剧，讲述翠花森林里熊大、熊二、光头强和小松鼠果果的欢乐故事。

- **类型**: 3D 卡通冒险喜剧
- **时长**: 第一集 1 分钟
- **风格**: 幽默搞笑，适合 6-12 岁儿童
- **生成方式**: Agnes AI 文本+图片+视频生成 + FFmpeg 拼接

## 角色介绍

| 角色 | 描述 |
|------|------|
| 🐻 熊大 | 森林守护者队长，聪明勇敢，肚子上有个"哥"字标贴 |
| 🐻 熊二 | 憨厚贪吃，口头禅"哎呀妈呀"，肚子上有个"东"字标贴 |
| 👷 光头强 | 戴橙色安全帽的伐木工，发明总出故障 |
| 🐿️ 小松鼠果果 | 机灵的情报员，穿着黄色叶子披风 |

## 工作流程

```
剧本 → 角色设定(9宫格) → 场景图(12场) → 视频片段(12个) → FFmpeg拼接
```

### 技术栈

- **文本生成**: Agnes AI (agnes-2.0-flash)
- **图片生成**: Agnes AI (agnes-image-2.1-flash)
- **视频生成**: Agnes AI (agnes-video-v2.0)
- **视频拼接**: FFmpeg
- **自动化**: Hermes Agent

## 项目结构

```
short-drama-web/
├── index.html          # 主页面
├── characters/         # 角色设定图
│   ├── xiongda_9panel_hd.png
│   ├── xionger_9panel_simple.png
│   ├── guangtouqiang_9panel_simple.png
│   └── guoguo_9panel_simple.png
├── scenes/             # 场景参考图 (12张)
│   ├── scene_01_翠花林清晨.png
│   └── ...
└── videos/             # 成片
    └── output.mp4
```

## 使用方法

直接在浏览器中打开 `index.html` 即可查看完整项目展示：

1. 角色设定九宫格
2. 12场场景参考图（点击可放大）
3. 剧本详情
4. 成片视频播放

## 生成过程

1. **剧本创作**: 12场戏，幽默搞笑风格
2. **角色设定**: 每个角色生成 9 宫格设定图（全身/背面/特写/三视图/细节/服装/表情/动态/色卡）
3. **场景图**: 每场戏生成一张 1920×1080 场景参考图
4. **视频片段**: 每场戏生成 5 秒视频片段
5. **成片拼接**: FFmpeg 拼接所有片段，输出 1 分钟成片

## 关于

本项目由 [Hermes Agent](https://github.com/NousResearch/hermes-agent) + [Agnes AI](https://agnes-ai.com) 驱动生成。
