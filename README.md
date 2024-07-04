# alist-github-releases-files
当 GitHub Releases 更新时，自动获取 Github Releases 中的文件，生成地址树并更新 AList 驱动。只需Fork本仓库后简单设置就可以实现此功能了。

## 环境变量
- ```ALISTTOKEN``` AList token 令牌

<details>
<summary>获取方法</summary>
  
![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/8c333f66-4971-4b6e-9983-05b0389000a3)

</details>

<details>
<summary>设置方法</summary>

![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/e5898202-0bdc-4f83-8192-871f0e94ff01)

![image](https://github.com/jianjianai/alist-github-releases-files/assets/59829816/e96d91b9-0d77-437e-8f55-768462c486ae)

</details>


## 配置文件
### filesConfig.json
这个配置仓库和文件夹的映射简单，就不教了。
``` javascript
{
  "owner": "panpanaw", //仓库所有者
  "name": "alist-files", //仓库名称
  "dir": {  //文件夹名称和 Releases tag 映射
    "原": "2024.7.4.11.08",
    "test/原": "2024.7.4.11.08"
  }
}
```

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
