# Padavan-build说明

直接fork，修改好编译型号及插件之后，点击右上角的 Star 星星按钮即可开始自动编译（自己点击才会编译）。

来自chongshengB大佬的Padavan-build项目。

## 编译

修改workflows文件：`Padavan-build/.github/workflows/build-padavan.yml`

- 修改内核：第35、48行（默认为3.4，也可修改成4.4，根据需要修改）
- 修改机型：第47行（根据目录rt-n56u/trunk/configs/templates/下的配置文件名，例如：`RM2100.config`，则修改为RM2100即可）
- 修改名称：第131行（按照130行的建议修改固件包名称）
- 保存提交：以上内容修改完成之后，保存提交
- 开始编译：最后点击页面的右上角的Sraeeed

## 更改内容

- 修改源码：第42行，将3.4内核版本的源码改称我自己的源码，4.4内核版本为MeIsReallyBa大佬的padavan-4.4项目
- 本人的rt-n56u源码地址：https://github.com/Ryukarin/rt-n56u.git
  - fork自chongshengB大佬的rt-n56u项目
  - 添加了`htop-3.0.2.tar.gz`文件，解决编译失败问题
  - 添加了`rt-n56u/trunk/change_logo.sh`替换logo脚本文件及logo图片，根据机型自动替换logo
  
    比如你要编译K2P固件，那么编译完成刷入路由进入后台，则显示PHICOMM的logo
