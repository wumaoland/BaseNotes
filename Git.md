# GIT基本命令

## 一.	初始化并建立远程连接

```powershell
git init
```

> **在本地初始化后在远端（github, gitgee）建立项目**

```powershell
git remote add origin git@github.com:username/project.git
```

```powershell
git remote -rm origin  # 删除远程链接
```



## 二.	拉取远程项目

```powershell
git pull origin main
```

## 三.	检查/创建/切换/删除分支

```powershell
git branch
```

```powershell
git checkout branch_name  #切换分支,若无分支便建立新分支
```

```powershell
git branch -d branch_name
```

## 四.	编辑提交修改文件

```powershell
git add filename  # add. 为添加所有修改文件
```

```powershell
git commit -m "message"
```

```powershell
git push origin main
```

## 五.	Git版本回退

```powershell
git log
```

```poweshell
git reset ...
```