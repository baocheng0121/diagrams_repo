### feature/p0001
> time: 2021-08-05

| platform | content | developer |
| ---- | ---- | ---- |
| all | formatting changelog sample for feature development | Baocheng Wang |

### 开发流程守则

# 项目名
> 项目简介

## 备忘

### 共 4 个项目
> api admin oapi task

### 启动服务

> 应用的配置文件目录在 config/{dev,qa,pre,prd}/application.yml

**启动命令如下**

```sh
go run app/main.go --project admin --runMode=dev --cfgPath=/path/to/application.yml
# runMode 后面可以跟 dev、qa、pre、prd
# cfgPath 如果不加次参数，则会根据 runMode 寻找 config 目录下的对应 application.yml 文件
#   如果指定则以指定的为准（本地测试用的到）
```

### 人为记录 新建分支 时间

> 因为 git 查看新建分支的日期比较麻烦（只能通过第一次推的 log 去查看）
>
> 所以原创这边作如下人为的规定：
>
> 在第一次建分支的时候，作小更改后（比如更改 version 或者 changelog）便推一次远程，且按照规定格式推送，如下：

1. 建分支
    * `git checkout -b feature/p0088`
2. 更改 version 值，后
    * `git add . && git commit -m"[newbranch] feature/p0088"`
3. 推远程（命令记不住没关系，此时输入 git push 回车后会有提示，我每次都这样）
    * `git push --set-upstream origin feature/p0088`

### 项目文档

> https://git.qutoutiao.net/newidea/writerplatform-docs


## (以上)
