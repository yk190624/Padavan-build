# Padavan-build说明

直接fork，修改好编译型号及插件之后，点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。

来自chongshengB大佬的Padavan-build项目。

## 编译

修改workflows文件：`Padavan-build/.github/workflows/build-padavan.yml`

1. 修改内核：第18行（默认为3.4，也可修改成4.4，根据需要修改）
2. 修改机型：第19行（根据目录rt-n56u/trunk/configs/templates/下的配置文件名，例如：`RM2100.config`，则修改为RM2100即可）
3. 修改名称：第129行（按照130行的建议修改固件包名称）
4. 保存提交：以上内容修改完成之后，保存提交
5. 开始编译：最后点击页面的右上角的**Star**，再到本页面的Actions标签查看是否开始编译，正常30分钟左右即可完成

## 更改内容

- 修改源码：第40行，将3.4内核版本的源码改称我自己的源码；第38行，4.4内核版本也改成了本人的padavan-4.4源码
- 本人的rt-n56u源码地址：https://github.com/Ryukarin/rt-n56u.git
  - fork自chongshengB大佬的rt-n56u项目
  - 替换了`htop-2.0.2.tar.gz`为`htop-3.0.2.tar.gz`文件，解决编译失败问题
  - 添加了`rt-n56u/trunk/change_logo.sh`替换logo脚本文件及logo图片，根据机型自动替换logo
- 本人的padavan-4.4码地址：https://github.com/Ryukarin/padavan-4.4.git
  - fork自MeIsReallyBa大佬的padavan-4.4项目
  - 添加了`padavan-4.4/trunk/change_logo.sh`替换logo脚本文件及logo图片，根据机型自动替换logo
