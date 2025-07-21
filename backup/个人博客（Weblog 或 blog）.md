本文在 https://breathiness.github.io/ 获得最佳体验

个人博客（Weblog 或 blog）是一种在网络上发布的个人日记或出版物，用以分享个人的想法、经验、知识、评论等。它是一个平台，让个人能够在网上表达自己，记录生活点滴，或是就特定主题提供深入分析和见解。个人博客相当相比起其他社交工具，没有推送，也没有内容的限制，是个更加强调其私人属性的内容分享方式。  

传统的个人博客搭建需要有服务器、要买域名。在过去的门槛是比较高的。GitHub 后来推出了个非常好用的功能，是 GitHub pages。可以说是搭建个人博客最方便的方式之一了。域名和服务器都能直接白嫖。并且有很多成熟的项目可以直接调用，我之前搭建的个人博客就是使用的 mirror 博客框架。  


mirror 相比起传统的方式接触代码和命令行的数量大大减少了。安装和后续维护简单，可以只在手机上用 termux 就能完成布置。后面就能通过在该仓库提交 issues 的方式来新建文章。  

这个工具搭建好的博客我是使用了很长时间的。在当时这个工具很好地解决了有无的问题。让我快速的开始了在博客上分享的过程。  

但是 mirror 在功能上其实是有缺失的。比如说缺少了切换夜间模式的功能。以及大部分个人博客都有的 RSS 功能。并且因为我搭建博客的时间比较早，GitHub 的 token 还是用的旧版本的。GitHub 有段时间会经常发邮件提醒我更新 token。这使得我一直很想替换掉 mirror，但一直以来却苦于没有什么好的替代品。直到这篇文章的主角登场。  

最近，一个叫 Gmeek 的博客框架吸引了我的注意。新建文章的方式依然是提交 issue，支持标签、支持评论、支持夜间模式、支持 RSS、支持使用个人域名、可自动更新版本。得益于 Github Actions 的存在，配置方式比起 mirror 还要更加简单。据官网的说法是：  

>一个博客框架，超轻量级个人博客模板。完全基于`Github Pages` 、 `Github Issues` 和 `Github Actions`。不需要本地部署，从搭建到写作，只需要 18 秒，2 步搭建好博客，第 3 步就是写作。

- Demo 页面：http://meekdai.github.io

- Gmeek 更新日志：https://meekdai.github.io/post/Gmeek-geng-xin-ri-zhi.html

- Gmeek 快速上手；https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html


看到如此符合我需求的工具，我果断就用起来了。实际体验下来，搭建和使用都是符合预期的方便。

2 安装方式

如果你是之前没有在 GitHub 建过个人博客的新人的话，那新建一个 Gmeek 博客的流程就相当简单了。跟官网的介绍说法一样，只要你有 GitHub 账号，就可以在两步后直接开始写作。甚至速通玩家来还能再压一下时间。具体流程就和官网介绍的一样。

2.1 从模板创建仓库

在登录了 GitHub 账号的情况下，点击通过模板创建仓库：https://github.com/new?template_name=Gmeek-template&template_owner=Meekdai  

建议仓库名称为`XXX.github.io`，其中`XXX`为你的 github 用户名。




2.2 仓库设置调整

在仓库的`Settings`中`Pages->Build and deployment->Source`下面选择`Github Actions`。  




这一步做完就算是部署完成了。下面按照正常流程开始写作即可。

2.3 开始写作

在 issue 页面点击绿色新建按钮即可开始写作。


> [!TIP]
> issue 使用的是 markdown 语法，推荐查看 GitHub 官方的教程：基本撰写和格式语法：https://docs.github.com/zh/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax

issue 编辑相比起其他编辑器，有个很方便的功能。在 MarkDown 文件里如果想添加图片，通常来说需要在图床上先上传。之后再将对应的图片链接粘贴进来。但是在 issue 里可以直接拖入图片。编辑器会自动上传然后生成链接。相当方便。