# Git_LFS

簡報連結:
- [GitLFS](http://gitlfs.rsync.tw)
- [.Dev](http://gandi-dev.rsync.tw)

## Git LFS Install
```bash
git lfs install
```

## Getting Started
```bash
git lfs track “*.psd”
git add .gitattributes
git add file.psd
git commit -m ‘Add psd file’
git push origin master
```

## 如果不能用LFS 就用Branch
```bash
git checkout -b prod
git add file.iso
git merge master
CI push prod branch to production
```

## 利用checkout替換變數裡面內容
```bash
$ git config filter.dater.smudge [ 檔名 ]
$ git config filter.dater.clean 'perl -pe "s/\\\$Date[^\\\$]*\\\$/\\\$Date\\\$/"'
```
