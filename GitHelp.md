# 帮助

```bash
# python3 运行http服务
python -m http.server 8000
# python2 运行http服务
python -m SimpleHTTPServer 8000

gitbook init //初始化目录文件
gitbook help //列出gitbook所有的命令
gitbook --help //输出gitbook-cli的帮助信息
gitbook install //安装插件
gitbook build //生成静态网页
gitbook serve //生成静态网页并运行服务器
gitbook build --gitbook=2.0.1 //生成时指定gitbook的版本, 本地没有会先下载
gitbook ls //列出本地所有的gitbook版本
gitbook ls-remote //列出远程可用的gitbook版本
gitbook fetch 标签/版本号 //安装对应的gitbook版本
gitbook update //更新到gitbook的最新版本
gitbook uninstall 2.0.1 //卸载对应的gitbook版本
gitbook build --log=debug //指定log的级别
gitbook builid --debug //输出错误信息
https://blog.csdn.net/liudongdong19/article/details/80034835
```

```cach
插件 ,"copy-code-button" 复制代码功能 没用不如用code,可以复制和显行号
```

[mermaid 图](https://github.com/knsv/mermaid)
[mermaid 帮助](http://knsv.github.io/mermaid/#/sequenceDiagram)

%accordion% mermaid示例 %accordion%

```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;

  id1(Start)-->id2(Stop)
  style id1 fill:#f9f,stroke:#333,stroke-width:4px
  style id2 fill:#ccf,stroke:#f66,stroke-width:2px,stroke-dasharray: 5, 5

  BB["fa:fa-twitter for peace"]
  BB---CC[fa:fa-ban forbidden]
  BB-.->DD(fa:fa-spinner);
  BB-->EE(A fa:fa-camera-retro perhaps?);

  A1[Hard edge] -->|Link text| B1(Round edge)
  B1 --> C1{Decision}
  C1 -->|One| D1[Result one]
  C1 -->|Two| E1[Result two]

  A3((This is the text in the circle))

  A4>This is the text in the box]

  A5{This is the text in the box}
```

%/accordion%

```mermaid

sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!

```

```mermaid

gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d

```

```mermaid

classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label

```

```mermaid

sequenceDiagram
    Alice ->> Bob: Hello Bob, how are you?
    Bob-->>John: How about you John?
    Bob--x Alice: I am good thanks!
    Bob-x John: I am good thanks!
    Note right of John: Bob thinks a long<br/>long time, so long<br/>that the text does<br/>not fit on a row.

    Bob-->Alice: Checking with John...
    Alice->John: Yes... John, how are you?

```

```mermaid


```

```mermaid


```

```mermaid


```

```mermaid


```

```mermaid


```

```mermaid


```

```mermaid


```
