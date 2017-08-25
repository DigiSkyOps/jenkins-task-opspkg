# 插件名称 

opspkg

# 功能说明

组装包插件

# 参数说明

| 参数名称 | 类型 | 默认值 | 是否必须 | 含义 |
|---|---|---|---|---|
| artifact.id | string | 空 | **必须** | 打包归档产物名称 |
| fileset.dir | string | ${ws.dir} | **必须** | 需要打包的文件目录 |
| fileset.includes | string | 空 | **必须** | 需要包含的文件通配符 |
| fileset.excludes | string | 空 | **必须** | 需要包含的文件通配符 |
| pkg.sub.dir | string | 空 | **非必须** | 如果需要创建子目录，子目录名称需提供 |
| is.pkg | boolean | true | **必须** | 是否进行打包，如果为false，只进行文件拷贝 |

# 配置使用样例

```yml
stages:
- name: pkg
  tasks:
    - task.id: opspkg
      fileset.includes: hello.jar
```