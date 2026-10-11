# 编辑与维护说明

[← 返回个人主页](../README.md)

## 修改已经写好的内容

| 要修改什么 | 打开哪里 |
| --- | --- |
| 个人简介、关注主题、文章入口 | [编辑个人主页](https://github.com/patienceeeeeeeee/test/edit/main/README.md) |
| 《坂本龙马与孙正义》正文 | [编辑文章](https://github.com/patienceeeeeeeee/test/edit/main/articles/ryoma-masayoshi-ambition.md) |
| 文章目录 | [编辑目录](https://github.com/patienceeeeeeeee/test/edit/main/articles/README.md) |
| GitHub Pages网页中的文章内容 | [编辑notes.json](https://github.com/patienceeeeeeeee/test/edit/main/notes.json) |

登录GitHub，修改文字后点击 **Commit changes**。提交后，GitHub中的文章会更新；Pages如已开启，会在部署完成后更新。

常用排版：`# 标题`、`## 小标题`、空行分段、`**重点**`、`[文字](链接)`。

## 新增文章

1. 在 `articles/` 下新建 `.md` 文件，写上标题、发布与修订日期、正文和必要来源。
2. 在 [文章目录](../articles/README.md) 加入一行，并按需要更新 [个人主页](../README.md) 的推荐文章。
3. 若要同步到GitHub Pages，向 `notes.json` 的数组新增一条记录。

`articles/` 是GitHub阅读版；`notes.json` 是网页阅读版。目前二者需要手动同步。

下面仅为格式示例：

```json
{
  "id": "my-note",
  "title": "一篇文章的标题",
  "category": "阅读",
  "updated": "2026-10-11T11:15:08+08:00",
  "source": "articles/my-note.md",
  "body": "第一段。\n\n第二段。"
}
```

分类可用：工作、创业、阅读、生活、随想。记录放在数组 `[ ... ]` 内，多条之间使用逗号分隔。`source` 指向已经创建的Markdown原文。

## 开启GitHub Pages

GitHub里的Markdown文章已经可以直接阅读和分享，不需要开启Pages。

如果希望访问独立网页，打开 [Settings → Pages](https://github.com/patienceeeeeeeee/test/settings/pages)：

- Source：**Deploy from a branch**
- Branch：**main**
- Folder：**/ (root)**
- 点击 **Save**

以GitHub设置页在部署成功后显示的地址为准。配置内容已准备好，但不要将准备好的源文件等同于Pages已经上线。

## 公开内容与私人草稿

本仓库是公开的，文章、文件和Git历史都可能被别人查看。私人草稿留在本地或下方的云端作者后台。

- [现有云端网站](https://wong-miles-notebook.eager-otter-5187.chatgpt.site)
- [云端作者后台](https://wong-miles-notebook.eager-otter-5187.chatgpt.site/studio)

云端网站和GitHub版本的数据独立，不会自动同步。`cloud-version/worker.js` 保留云端实现代码；运行需要R2的 `BUCKET` 绑定、服务器端 `OWNER_EMAIL` 配置以及可信登录身份头。GitHub Pages只运行静态网页，不能直接运行这个后台。

## 更新前检查

确认日期、来源与正文一致，文章入口能打开；修订观点时保留必要的适用条件。不把尚未完成的文章列为已有成果。
