# Linux命令笔记

## 命令检索

https://wangchujiang.com/linux-command/

## Linux搜索文件

1. **搜索文件名**

```
#搜索服务器里面所有文件名包含`redirect`的php文件
find / -name \*.php | grep redirect
```

2. **搜索内容**

- 搜索服务器里面所有`php`文件，文件里面包含`RestoreConfig`,显示文件名

  ```
  find / -name \*.php -exec grep -l  "RestoreConfig" {} \;
  ```

  

- 搜索服务器里面所有`php`文件，文件里面包含`RestoreConfig`,显示行数和内容

  ```
  find / -name \*.php -exec grep -n  "RestoreConfig" {} \;
  ```

  

- 搜索服务器里面所有`php`文件，文件里面包含`RestoreConfig`,显示文件名，行数和内容

  ```
  find / -name \*.php | xargs grep -n  "RestoreConfig" {} \;
  ```

