# Cobalt Strike Malleable C2 设计与参考指南

该项目旨在为设计 **Cobalt Strike Malleable C2** 配置文件提供参考。

在使用配置文件前，请务必通过 `./c2lint [/path/to/my.profile]` 验证其正确性！

## Malleable C2 配置文件指南

以下资源可帮助深入理解 Malleable C2：

- [MalleableExplained.md](https://github.com/threatexpress/malleable-c2/blob/master/MalleableExplained.md)：快速参考指南
- [ThreatExpress - 深入探讨 Cobalt Strike Malleable C2](http://threatexpress.com/blogs/2018/a-deep-dive-into-cobalt-strike-malleable-c2/)：最初创建 jQuery 参考配置文件的博客文章
- [Understanding Cobalt Strike Profiles](https://blog.zsec.uk/cobalt-strike-profiles/)：修订后的（当前）配置文件指南
- [随机配置文件生成器](https://github.com/threatexpress/random_c2_profile)：带有更多示例和设置选项的配置文件生成器

## 更新日志

### 2023-10-17 - 支持 CS 4.9

- 添加 4.9 参考配置文件
- 更新 MalleableExplained.md，新增 4.9 功能选项：
  - `post-ex.cleanup`
  - `.http-beacon.library`

### 2023-08-01 - 支持 CS 4.8

- 添加 4.8 参考配置文件
- 更新 MalleableExplained.md，新增 4.8 功能选项：
  - `stage.syscall_method`

### 2022-10-22 - 支持 CS 4.7

- 添加 4.7 参考配置文件
- 更新 MalleableExplained.md，补充 4.7 相关内容

### 2022-04-21 - 支持 CS 4.6

- 添加 4.6 参考配置文件

- 移除 "1MB" 限制

  - 新增 "Task 和 Proxy 最大尺寸" 设置选项：

    ```bash
    set tasks_max_size "1048576";  
    set tasks_proxy_max_size "921600";  
    set tasks_dns_proxy_max_size "71680";  
    ```

  - [任务相关设置的额外说明](https://hstechdocs.helpsystems.com/manuals/cobaltstrike/current/userguide/content/topics/malleable-c2_profile-language.htm#_Toc65482837)

- 更新 MalleableExplained.md，补充 4.6 相关内容

### 2021-12 - 支持 CS 4.5

- 添加 4.5 参考配置文件
- 更新 MalleableExplained.md，补充 4.5 相关内容

### 2021-08 - 添加 [MalleableExplained.md](https://github.com/threatexpress/malleable-c2/blob/master/MalleableExplained.md)

- 参考来源：Andy Gill (@ZephrFish)
- 参考博客：[zsec.uk 博客](https://blog.zsec.uk/cobalt-strike-profiles/)

### 2021-03 - 支持 CS 4.3

- 添加 CS 4.3 的最新 Malleable C2 配置选项
- 将 `dns` 设置移动至新的 `dns-beacon` 部分
- CS 4.3 新增功能：
  - dns-beacon
    - beacon
    - get_A
    - get_AAAA
    - get_TXT
    - put_metadata
    - put_output
    - ns_response
  - http-config
    - block_useragents

### 2020-11 - 支持 CS 4.2

- 添加 CS 4.1 和 4.2 的最新 MalleablePE 和 MalleableC2 选项
- CS 4.1 新增功能：`tcp_frame_header`，`smb_frame_header`，`ssh_banner`
- CS 4.2 新增功能：
  - global
    - `data_jitter`
    - `headers_remove`
    - `ssh_pipename`
  - postex
    - `pipename`
    - `thread_hint`
    - `keylogger`
  - stage
    - `allocator`
    - `magic_mz_86|magic_mz_64`
    - `magic_pe`

### 2020-03 - 支持 CS 4.0

- 添加 CS 4.0 的参考配置文件及可用的 Malleable C2 配置选项
- 移除已废弃的功能（如 `amsi_disable`，`disable` 等进程注入技术）

## 作者

- @joevest
- @001SPARTaN
- @andrewchiles
- @Charles-Foster-Kane

## 许可证

本项目及其所有脚本均采用 GNU GPL v3.0 许可证。
