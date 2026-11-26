# 发布记录与验证

通过 [GitHub Releases](https://github.com/IYNAIT0110/STArra/releases) 查看公开发布时间、安装包、便携版和 SHA-256 校验文件。[CHANGELOG](../../CHANGELOG.md) 记录版本变化，版本说明位于本目录。

当前版本：[v0.6.7 发布说明](v0.6.7.md) · [GitHub Release](https://github.com/IYNAIT0110/STArra/releases/tag/v0.6.7)。

## 历史核对

| 版本 | GitHub Release 页面显示的发布日期 | 公开标签目标 |
| --- | --- | --- |
| [v0.3.7](https://github.com/IYNAIT0110/STArra/releases/tag/v0.3.7) | 2026-11-21 | `c3720d5` |
| [v0.6.0](https://github.com/IYNAIT0110/STArra/releases/tag/v0.6.0) | 2026-11-22 | `c3720d5` |
| [v0.6.1](https://github.com/IYNAIT0110/STArra/releases/tag/v0.6.1) | 2026-11-22 | `66283d8` |
| [v0.6.3](https://github.com/IYNAIT0110/STArra/releases/tag/v0.6.3) | 2026-11-25 | `7682deb` |

公开仓库的 `v0.3.0` 至 `v0.3.7` 和 `v0.6.0` 都指向同一个归档提交。仅凭当前标签无法确定它们是什么时候创建或移动的，也无法复原各版构建所用的源码。核对公开发布时，以 GitHub Release 的 `published_at` 为准。变更记录中的日期是项目文档记载的日期，下载到的文件可对照相应 Release 的校验值。

`0.3.7 → 0.6.0` 是一次向上的版本号跳跃。现有公开发行记录中没有 `0.4.x` 或 `0.5.x` 系列。跳号沿用原始记录，今后如有跳号，应在发布说明中写明原因。

## 发布流程

1. 开发中的变更先记在 CHANGELOG 的「未发布」。以修订版处理修复，以次版本容纳新增能力，涉及兼容性变化时在发布说明中明确影响和升级方法。
2. 在私有主分支准备发布提交，统一应用版本、锁文件、变更记录和 `docs/releases/vX.Y.Z.md`。在验证通过的提交上打私有标签。私有 Windows 构建会检查标签、主分支来源和版本文件，再运行测试与打包。
3. 在私有发布记录保存对应构建、提交和校验结果。按公开发布流程，仅将批准的文档、安装包、便携版和校验文件发布到公开仓库。
4. 公开 Release 发布后，验证下载和校验文件，把实际发布日期和 Release 链接补入变更记录。修订说明可更新原 Release 正文，替换二进制则使用新修订版本。

公开标签用于定位公开发布记录，源码和构建对应关系由私有发布记录维护。
