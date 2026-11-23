# 一句成套：wechat-sticker-skill

这是 `undefined-zzk` 的个人微信表情制作 Skill。

给 AI 助手一句需求和一张用户有权使用的角色参考图，就可以制作一套微信表情专辑素材。默认先生成 1 张动态预览，用户确认后再补齐至 8 张，并准备封面、聊天面板图标和详情页横幅。也支持用户指定 8–24 张表情，或制作静态 PNG 表情。

## 使用

将本仓库安装为 AI 助手的 Skill。安装后，Skill 名称为：

> `wechat-sticker-skill`

例如，对支持 Skill 安装的 Codex 说：

> 请把这个 GitHub 仓库安装为本地 Skill：
> https://github.com/undefined-zzk/wechat-sticker-skill

安装后提供角色参考图，并说明风格、聊天场景以及是否配字。例如：

> 使用 wechat-sticker-skill，根据这张我有权使用的小狗照片制作 8 张有趣的微信动态表情。先生成一张给我确认，文字或符号跟随动作出现。

如果参考图涉及他人肖像、商业角色或来源不明的作品，应先确认使用权。没有授权时，可以改为只借鉴抽象风格并创作全新的角色。

GIF 或图片生成能力取决于实际使用的 AI 环境。本 Skill 不包含生图模型或 API 密钥，也不代替微信投稿，不保证平台审核或上架。涉及图片上传、外部服务、计费或发布时，应遵守用户授权和运行环境权限。

## 导出与检查

需要 Python 3.9+ 和 Pillow。可先安装依赖：

```bash
python3 -m pip install Pillow
```

按 `SKILL.md` 准备 `pack.json`、表情素材和配套素材，然后运行：

```bash
python3 scripts/sticker.py build <工作目录>
python3 scripts/sticker.py check <工作目录>
```

`submit/` 包含已整理的投稿素材；`预览.html` 可播放动图并查看静态表情；`交付给客户.zip` 包含 `submit/` 和 `上架文案.md`。缺失素材不会自动补齐。机器检查不替代文字、动作、版权、授权及微信审核的人工核对。微信规格见 `references/wechat-rules.md`，实际投稿时以平台当前要求为准。

## 许可

本项目采用 MIT 许可证。

维护者：`undefined-zzk`

仓库地址：<https://github.com/undefined-zzk/wechat-sticker-skill>
