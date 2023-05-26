https://www.youtube.com/watch?v=aZPvrraKT2g

# tgs-helm-repo
mkdir Charts
cd Charts
helm create app01

# create package
helm package Charts/app01 # 產生 app01-0.1.0.tgz
mv app01-0.1.0.tgz ./Packages/
export helm_token="ghp_SSDAFfdsfs324rFDGg"
helm repo index .
git push

# 設定 url
Github > Settings > Pages
helm repo add tgs-repo https://lunyi.github.io/tgs-helm-repo/
helm search repo tgs-repo -l

# 更新版本
udpate ./Charts/app01/Chart.yaml  version 欄位
helm package Charts/app01 //重新產生 app01-0.2.0.tgz
helm repo index .
git push

# 確認新版本
helm repo update
helm search repo tgs-repo -l