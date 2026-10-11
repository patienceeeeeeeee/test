# Wong / Miles · 思考与记忆

记录当下的观察、阅读后的思考，以及尚未想清楚的问题。

我更希望认识一些愿意独立思考、认真做事，也敢于修正自己判断的人。

## 文章

### [坂本龙马与孙正义：我开始重新理解“志向”这两个字](articles/ryoma-masayoshi-ambition.md)

2026年10月11日 · 阅读与思考

> 志向不仅是想去哪里，更是为了抵达那里，愿意长期做出什么选择、承担什么代价。

从坂本龙马与孙正义的经历出发，思考想法如何变成行动，以及信念为什么仍然需要现实检验。

[阅读全文 →](articles/ryoma-masayoshi-ambition.md)

---

<details>
<summary>编辑笔记与网站设置（作者使用）</summary>

关于制造业、经营、阅读与职业成长的个人网站。主张从具体问题出发，留下判断依据，再用行动修正认识。

## 开启 GitHub Pages

打开本仓库 **Settings → Pages**：

- Source：Deploy from a branch
- Branch：main
- Folder：/ (root)
- 点击 Save

部署完成后，GitHub 会在 Pages 设置页提供真实访问地址。预计地址为 `https://patienceeeeeeeee.github.io/test/`，未完成部署前不能视为已上线。

## 编辑主页与文章

- 主页文案：编辑 `index.html`，点击铅笔图标修改并 Commit changes。
- 公开文章：编辑 `notes.json`。首页的「编辑文章」直接通向这个文件。
- 所有仓库文件都是公开的，**不要在这里存私人草稿**。删除文件也不会自动清除 Git 历史。

`notes.json` 是文章数组，每篇文章采用以下结构（这是格式示例，不是已经发布的文章）：

```json
[
  {
    "id": "my-first-note",
    "title": "一个让我改变判断的问题",
    "category": "工作",
    "updated": "2026-10-11T11:00:00+08:00",
    "body": "发生了什么？\n\n我掌握了什么信息？\n\n我为什么这样判断？\n\n下一步准备验证什么？"
  }
]
```

分类建议：工作、创业、阅读、生活、随想。正文换行在 JSON 字符串中写 `\n`。保存时保持有效 JSON；更新日期后，文章按日期从新到旧排序。

## 云端编辑版本

- [现有公开主页](https://wong-miles-notebook.eager-otter-5187.chatgpt.site)
- [云端作者后台](https://wong-miles-notebook.eager-otter-5187.chatgpt.site/studio)

`cloud-version/worker.js` 保留云端版本的服务端与页面源码，供后续迁移参考。运行需要 R2 的 `BUCKET` 绑定、服务器端 `OWNER_EMAIL` 配置，以及平台提供的可信登录身份头；不能直接在 GitHub Pages 运行。

GitHub Pages 版本和现有云端版本的数据独立，不会自动同步。GitHub Pages 不运行服务端，不提供 ChatGPT 登录后台或私密草稿存储。

## 文件结构

- `index.html`：响应式个人主页、分类搜索、文章阅读
- `notes.json`：公开文章
- `.nojekyll`：直接发布静态文件
- `cloud-version/worker.js`：现有云端实现源码（不含运行时密钥）

文章原文保存在 `articles/` 目录；网站列表使用 `notes.json`。修改文章时，请同步这两处内容。


</details>
