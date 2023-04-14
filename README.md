## 配置'github-pages'
在 vue.config.js 中设置正确的 publicPath。

如果打算将项目部署到 https://<USERNAME>.github.io/ 上, publicPath 将默认被设为 "/"，你可以忽略这个参数。
  如果打算将项目部署到 https://<USERNAME>.github.io/<REPO>/ 上 (即仓库地址为 https://github.com/<USERNAME>/<REPO>)，可将 publicPath 设为 "/<REPO>/"。举个例子，如果仓库名字为“my-project”，那么 vue.config.js 的内容应如下所示：
""""JavaScarpt
module.exports = {
  publicPath: process.env.NODE_ENV === 'production'
  ? '/my-project/'
  : '/'
}
""""

""""
# deploy.sh
# 错误时停止
set -e
# 打包
npm run build
# 进入目标文件夹
cd dist
# 提交到本地仓库
git init
git add -A
git commit -m 'deploy'
# 提交到 https://github.com:nusr/resume-vue 项目的 gh-pages 分支
git push -f git@github.com:annacode747/mall-manage.git master:gh-pages
cd -
""""

""""
npm run build
cd dist
git init
git add -A
git commit -m 'deploy'
git push -f git@github.com:annacode747/mall-manage.git master:gh-pages
""""