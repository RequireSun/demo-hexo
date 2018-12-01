# 实施步骤

1. 创建 github 项目

1. 安装 git-bash

1. 安装 node.js

1. 使用 npm 全局安装 hexo-cli

   ```
   npm i -g hexo-cli
   ```

1. hexo-cli 初始化项目

    ```
    hexo init project-name
    ```

1. 将本地项目与 github 项目合并

    先进入项目目录, 初始化 git 仓库:

    ```
    git init
    ```

    将 github 项目拉到本地:

    ```
    git pull --allow-unrelated-histories origin master
    ```

    解决项目中的文件冲突:

    ```
    ```

1. 安装依赖模块

    ```
    npm i
    ```

    如果安装很慢, 可以使用 `cnpm`

1. 使用 npm 在本项目下安装发布工具

    ```
    npm install -S hexo-deployer-git
    ```

1. 更换主题

    在 hexo 官网寻找你喜欢的主题

    [https://hexo.io/themes/](https://hexo.io/themes/)

    从 git 上将喜欢的主题以 .zip 格式下载下来

    解压到项目目录下的 themes 文件夹中 (别给解压散了) (另外目录最后的 -master / -develop 为 git 分支名称, 下载下来之后记得删掉)

    去 _config.yml 文件中修改 theme 字段, 改为你下载的主题名称

1. 部署

    请修改 `_config.yml` 文件来修改配置

    ```
    deploy:
      type: git
      repo: github 项目地址
      branch: github 分支 (github 只能选择 master 或 gh-pages 分支, 一定不要用 master 分支)
    ```

    修改一下你的域名 (url 参数)

    ```
    url: https://requiresun.github.io/demo-hexo/
    ```

    如果你的网站并不是部署在域名的根目录上 (如 http://your.host.com/xxx)
    需要修改 root 参数增加你的 path, 否则你的网站的 css js 文件将会消失 (因为目录不对加载不上)

    reference: [https://github.com/hexojs/hexo/issues/3034#issuecomment-367548333](https://github.com/hexojs/hexo/issues/3034#issuecomment-367548333)

    ```
    root: /xxx
    ```
