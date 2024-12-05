#### 开发流程

    - 初始化时将所有的api接口生成出 api-type.d.ts 文件
      - 格式为：.apis.ts的名字作为key， 文件内的所有接口作为value
    - 监听文件的变化，当文件发生变化时，重新生成api-type.d.ts文件
      - 只改变发生变化的文件
      - 全部重新生成
    - 解析.api.ts文件中的接口，生成数组
    - 将api-type.d.ts文件中对应的key的值替换为新的数组