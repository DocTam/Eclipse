# 与 Eclipse 相关

> 技巧、插件与问题解决

## 技巧

### 加速链接速度，提高更新软件的效率。

- 修改启动配置文件，如：eclipse.ini 或 studio.ini

```eclipse.ini 或 studio.ini
-Dosgi.dataAreaRequiresExplicitInit=true
-Declipse.p2.max.threads=10
-Doomph.update.url=http://download.eclipse.org/oomph/updates/milestone/latest
-Doomph.redirection.index.redirection=index:/->http://git.eclipse.org/c/oomph/org.eclipse.oomph.git/plain/setups/
-Dorg.eclipse.equinox.p2.transport.ecf.retry=15
-Dorg.eclipse.ecf.provider.filetransfer.retrieve.closeTimeout=30000
-Dorg.eclipse.ecf.provider.filetransfer.retrieve.readTimeout=30000
-Dsun.net.client.defaultReadTimeout=30000
```

## 插件

###	添加 MarkDown 支持

- 使用 Eclipse Marketplace 搜索 MarkDown 并安装插件支持
 
  - Markdown text editor
  - GitHub Flavored Markdown viewer plugin

```Eclipse 首选项设置
常规 -> 编辑器 -> 文本编辑器 -> MarkDown -> Support GitHub Syntax （勾选此项）
GFM Viewer -> Use Eclipse Console （勾选此项）
```

###	添加 Maven 支持

- 使用 Install New Soft 添加 M2E 更新链接

  - 建议使用低版本 M2E，安装成功后，在 Eclipse 首选项设置里的 Maven 选项里设置离线版本的高版本 Maven。

```
M2E - http://download.eclipse.org/technology/m2e/milestones/1.4
```

  - 更改 Maven 的 setting.xml 使其使用指定的本地仓库以及中央仓库

```setting.xml
  <localRepository>D:/Soft/Maven/.m2/repository</localRepository>
  <mirrors>
    <mirror>
      <id>nexus-aliyun</id>
      <mirrorOf>*</mirrorOf>
      <name>Nexus aliyun</name>
      <url>http://maven.aliyun.com/nexus/content/groups/public</url>
    </mirror>
  </mirrors>
```

## 问题解决

### 暂无




# 协议

[MIT](https://github.com/DocTam/Wnmp/blob/master/LICENSE)
