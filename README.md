# 讲义

本版讲义由 **OpeningSourceORG** 与 **PCI** 合作编辑推出。<br/>
会在**Github**与**PCI**官网异步（？）不定期（？？）更新。  

------------

### 讲义格式

讲义使用**ACD**（A Complex Document，一种基于H5的更加轻量的动态文档格式）编写。初步制定格式如下：  

首先若干行，对动态渲染格式进行说明。  
每一行包含一个“版本”。按如下格式编写：
```
#version 名字 模块1 模块2 ....
```
例如，“速查手册”版本需要模块“公式定理”、“代码实现”，则对应格式为：
```
#version 速查手册 公式定理 代码实现
```

- \\ 转义  // 你们懂的
- \{大标题\}  （例如 1 ）
- \[中标题\]  （例如 1.1）
- \(小标题\)  （例如 1.1.1）
- \<code\>代码\</code\>  // 别忘了这玩意基于H5

#sec 在后面接名字，则表示一对#section中的内容对于不同的版本需要筛选。<br/>
#end 表示结束<br/>
例如：
```
#sec sec
balabala
#end
```
则表示它属于名为sec的Section。如果一段内容没有被#sec和#end环绕，则认为是属于名为'default'的模块。<br/>


不需要\par或者段尾加两个__这种操作，因为会根据自然段自动添加\<p\>\</p\>标签对。所以如果需要插入HTML请手工inline。:P  
标题中不要加入编号，Renderer会自动添加并生成目录。  
暂时不支持其他特性（例如加粗、倾斜、插图等）。需要的话暂时只能使用HTML+CSS来手工实现（至少万能的H5还是万能的）。  
如果需要使用数学公式，可以直接内嵌MarkDown，我们会使用第三方库来解析。  
按照以往的讲义编辑经验，其余的功能基本上用不着（所以就不管辣）！  

------------

### 文件目录格式

为了方便阅读，请务必按专题划分文件夹（例如机器学习，基础算法（主要是我要写），etc.）。同一专题请编号。<br/>
若有相关的素材需要上传，请自行建立子目录。除了插图需要随文档放在images子目录下以外，不作特别要求，只要能看得明白就好。<br/>
请养成良好的编辑习惯，避免git merge冲突，每人尽量在自己独立分支中进行操作，使用pull request申请合并。<br/>

------------

### 工作要求

每周至少要更新一篇讲义。
定期进行工作进度报告，可以通过WeChat，也可以直接在此处提Issue/PR。
