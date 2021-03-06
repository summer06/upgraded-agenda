# Agenda-v2
---
### fork 项目地址
https://github.com/summer06/upgraded-agenda

---
### 个人工作摘要

- 第一次提交：完成了API的设计并使用API Blueprint完成API文档的编写。

- 第二次提交：修改了.apib文件的bug，修改好agenda版本1的cmd部分，并且完成了客户端的user部分的代码编写。

- 第三次提交：修改了.apib文件返回的格式，完成了客户端meeting部分的代码编写。

- 第四次提交：修改了引入文件路径，修改了.travis.yml文件，增加了测试部分的部署，完成了客户端测试部分的代码编写

- 第五次提交：编写了部分README文件。

### 个人项目小结

在这个项目里，我主要负责API的设计编写，客户端实现，客户端测试以及持续集成文件.travis.yml的编写。

第一次使用API的设计工具来编写与设计API，刚开始的时候没有充分了解API Blueprint这个工具，耽误了不少时间。在了解之后，编写过程并不困难。但是API Blueprint提供的mock server好像是有点不稳定的，出现了好几次启动mock server但是call resource fail的情况，让我一直以为是编写的语法有问题，但是后来发现确实是它的服务器不稳定。后来改用直接在浏览器输入地址，情况好很多。在设计API的过程中，浅略地学习到了一些设计的准则。

客户端cli的部分主要是对上一个版本的agenda进行修改，这部分的工作不难，但是还是很花时间。主要修改的部分是将原本的本地处理controller改成向服务器端发送http请求。请求有GET请求也有POST请求，这两个需要做不同的处理。POST的处理稍微复杂一点。由于上一次的json和对象的转换处理是同伴在写，因此这次通过编写这部分的代码重新补上了这部分的内容。json格式和对象的转换在go里面做起来挺方便的，但是这个也确实是重要的。

最后是关于持续集成。这次用的是Travis CI进行持续集成。一开始我对这个概念是陌生的，后来在网上查阅博客之后才知道原来是一个帮助我们自动部署自动测试的工具。一开始，我经历了n个build fail，可以说是很扎心了。后来发现是因为我在本地编写的时候用的import路径和在github上用travis自动部署的不一样，因此总是失败。改掉了这个问题之后，就成功地pass了！

至于dockerfile，虽然这部分不是我负责，不过我还是稍微看了一下。dockerfile的文件编写似乎不是很难，不过看同伴的反应，在docker hub上部署，拉文件等会出现各种奇怪的问题。但是真的觉得docker是个很棒很好用的东西，学会用它应该会方便不少。

因为我们小组只有两个人，还都不是什么原本就很厉害的大腿，因此做这个项目真的花了我们不少时间，我们最终也没有说做得多好，不过感觉大家都尽力了。学习到了就是进步。从一开始想要退课到坚持到现在，在这门课里收获的应该不仅是知识，还有一段努力坚持的经历了。
