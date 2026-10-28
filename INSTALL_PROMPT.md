# 复制给接收者 Codex 的导入请求

先在本机 Codex 打开本项目文件夹，启用 Pets 插件并查看动画预览。以下请求会创建并选中一只新宠物；请在阅读质量差异后发送。它没有默认豁免质量门禁。

---

请将当前文件夹中 `pet/spritesheet.png` 导入为我自己的 Pets 宠物并选中，名称与描述读取 `manifest.json`。这是已有成品素材导入，不需要重新生成动画，也不要修改我的其他宠物。

请先读取 README、素材声明和 qa/pet-quality.json，并让我看到动画预览。核对精灵图 SHA256 与 manifest.json 一致，使用 Pets 官方 validate_pet_spritesheet 验证；只有 valid=true 才能继续。历史综合质量检查未通过的原因是自然透明空隙误报，若适用的技能要求豁免，先向我说明并取得我自己的明确决定，不沿用创建者的历史授权。

满足适用的导入要求后，对该精灵图使用 prepare_pet_upload，把返回的 upload.upload_session_id 交给 create_pet，再用新返回的 pet.id 调用 select_pet，并用 list_pets 确认已激活。不要把文件名、历史ID、上传会话或下载链接当成新宠物ID。不要自动安装 upstream 目录里的独立桌面挂件。

如果当前没有 Pets 工具或客户端不支持导入，请报告缺少的功能，不猜测工具调用，不声称已经安装，也不尝试向未确认的应用目录写文件。
