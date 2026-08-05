# MyHive 工具发布目录

此目录用于整理准备上传到 GitHub Releases 的工具发布文件。

## 文件内容

```text
github-release/
├─ catalog.json
├─ ppt-master-<version>.zip
├─ video-master-<version>.zip
└─ SHA256SUMS.txt
```

ZIP 工具包由 `.github/workflows/tools-release.yml` 生成。每个工具都是独立下载和安装的，用户不需要下载全部工具。

## 用户安装方式

1. 在 MyHive 的“个人设置 → 工具下载”中打开 GitHub 工具下载页面。

2. 根据需要下载某一个工具的 ZIP 包。

3. 将 ZIP 解压到当前用户目录：

   ```text
   %USERPROFILE%\\.myhive\\tools\\<tool-id>\\
   ```

4. 确认工具目录中存在 `manifest.json`、工具 exe 和配套文件。

5. 打开 MyHive 的“工作台 → 我的工具”。

6. 点击“重新扫描本地工具”。

7. 工具显示“启动”后即可使用。

## 注意事项

- 不要把 ZIP 文件直接放在 `.myhive\\tools` 根目录，必须先解压到工具自己的子目录。
- 不要修改 `manifest.json` 中的工具 ID。
- 工具运行数据和日志保存在工具目录的 `data`、`logs` 子目录中。
- MyHive 不会自动下载或安装工具，用户可以按需选择。
