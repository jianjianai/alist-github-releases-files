> ### 更好用的项目，也是差不多的功能
> Flist - 将 GitHub Releases 以类似网盘的形式展示在网页上，方便用户下载开源软件。 支持视频、音频、图片、PDF 等文件的在线预览。
> https://github.com/jianjianai/FList

# alist-github-releases-files
当 GitHub Releases 更新时，自动获取 Github Releases 中的文件，生成地址树并更新 AList 驱动。只需Fork本仓库后简单设置就可以实现此功能了。

## 功能描述
将文件上传到 Releases(发行版) 上 Actions 就会自动运行并生成 AList 地址树，并自动更新到配置的网盘上。

文件夹按照 tag 名称生成 如果tag名称为 ```root``` 则文件放在根目录 例:

tag名称：1.1.2
``` text
1.1.2
  xxx:xxx:http://xxx
  xxx:xxx:http://xxx
  ...
```

tag名称：test/test2
``` text
test
  test2
    xxx:xxx:http://xxx
    xxx:xxx:http://xxx
    ...
```

tag名称：root
``` text
xxx:xxx:http://xxx
xxx:xxx:http://xxx
...
```


## 环境变量
| 名称         | 作用                                     |
|------------|----------------------------------------|
| AListToken | AList token 令牌 可在alist设置中查看            |
| AListUrl   | 你的 AList 网盘链接 例如:https://you.alist.com |

### 获取方法
#### AListToken
<details>

![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/8c333f66-4971-4b6e-9983-05b0389000a3)

<details>

- [神奇小破站](https://jjaw.cn/)

</details>

</details>


### 设置环境变量方法
<details>

![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/e5898202-0bdc-4f83-8192-871f0e94ff01)

![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/e96d91b9-0d77-437e-8f55-768462c486ae)

</details>


## 配置文件

### AListStorageConfig.json
AListApi,可以自己查询

https://alist.nn.ci/zh/guide/api/admin/storage.html#post-%E6%9B%B4%E6%96%B0%E5%AD%98%E5%82%A8

#### 驱动id获取

<details>
<summary>展开查看</summary>
  
![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/0db08751-f207-4582-b93a-0477b640bde8)

</details>

``` javascript
{
  "id":0, //驱动id
  "mount_path":"/", //挂载目录
  "driver":"UrlTree",
  "status":"work",
  "remark":"", //备注名称
  "enable_sign":false,
  "order_by":"",
  "order_direction":"",
  "extract_folder":"",
  "web_proxy":false, //是否开启下载代理
  "down_proxy_url":"", //下载代理url
  "addition": {
    "head_size":false
  }
}
```
