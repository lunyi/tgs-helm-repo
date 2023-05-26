https://www.youtube.com/watch?v=aZPvrraKT2g
# tgs-helm-repo
mkdir Charts
cd Charts
helm create appn1

# create package
helm package Charts/app01

export helm_token="ghp_SSDAFfdsfs324rFDGg"


helm repo index .