# 这是什么
用于 GitHub 操作的自动化工作流程，可为 Windows、Linux 和 macOS 构建 Aseprite。
使用 GitHub 操作无需手动编译，也不包含恶意软件。
为了遵守 Aseprite 的 EULA，本工作流程不会像 artifacts 那样将二进制文件上传到可公开访问的空间。
该版本可作为草案在版本库中找到（仅对版本库所有者可见）。

# 使用说明

1. `Clone`或者`Fork`本仓库
2. 编辑`/.github/workflows/aseprite_build_deploy.yml`
3. 找到并编辑 **os** 这一行，删除你不需要的系统
```yaml
        strategy:
            matrix:
                os: [windows-latest, ubuntu-latest, macOS-latest]
```
4. 保存并提交`commit`.
5. 工作流将会在每天以及每次`Push`时检测`Aseprite`最新发布版本

TODO
