# undefined-zzk 的 wechat-sticker-pack Skill

这是 `undefined-zzk` 维护的个人微信表情创作 Skill。根据用户需求和用户有权使用的角色参考图，制作动态或静态微信表情及投稿素材。支持动态 GIF 和静态 PNG 表情，默认先生成第 1 张预览，用户确认后再补齐整套。

## 能力

- 设计角色设定和聊天场景表
- 生成 8–24 张动态或静态表情
- 生成封面、聊天面板图标和详情页横幅
- 按需生成赞赏引导语、赞赏引导图和赞赏致谢图
- 使用 Pillow 构建和检查投稿素材
- 输出预览、上架文案和交付压缩包

## 使用方式

将本目录作为 Agent Skill 安装，并提供一句制作需求和一张用户有权使用的角色参考图。例如：

> 使用 wechat-sticker-pack，做 8 张原创小动物动态表情，先生成一张“收到”预览。

## 本地检查

需要 Python 3.9+ 和 Pillow：

```bash
python3 scripts/sticker.py build <工作目录>
python3 scripts/sticker.py check <工作目录>
```

`SKILL.md` 是完整工作流程；微信尺寸和大小规则见 `references/wechat-rules.md`。

项目地址：<https://github.com/undefined-zzk/wechat-sticker-skill>

## 作者

维护者：`undefined-zzk`

## 许可

本项目采用 MIT License。表情内容、参考图、角色形象及字体等仍需由使用者自行确认版权和授权。
