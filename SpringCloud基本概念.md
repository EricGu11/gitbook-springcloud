<h2>Spring Cloud基本概念</h2>

<hr style="height:2px"/>

<h4>1. 什么是SpringCloud</h4>

<p style="text-indent:2em">分布式微服务架构下的一站式解决方案，是各个微服务架构落地技术的集合体，俗称微服务全家桶。</p>

<h4>2. SpringCloud与Spring Boot的关系</h4>

<p style="text-indent:2em">SpringBoot专注于快速方便的开发单个个体微服务。</p>

<p style="text-indent:2em">SpringCloud是关注全局的微服务协调整理治理框架，它将SpringBoot开发的一个个单体微服务整合并管理起来，为各个微服务之间提供：配置管理、服务发现、断路器、路由、微代理、事件总线、全局锁、决策竞选、分布式会话等等集成服务</p>

<p style="text-indent:2em;color:red">SpringBoot可以离开SpringCloud独立使用开发项目，但是SpringCloud离不开SpringBoot，属于依赖的关系。</p>

<p style="text-indent:2em;color:red">SpringBoot专注于快速、方便的开发单个微服务个体，SpringCloud关注全局的服务治理框架。</p>

<h4>3. SpringCloud与Dubbo的区别</h4>

<img src="./pic/3D138060-0DA8-4620-A9DE-D04D33E81340.png" alt="img" style="zoom:45%;" />

<p style="text-indent:2em;color:red">最大区别：SpringCloud抛弃了Dubbo的RPC通信，采用的是基于HTTP的REST方式。</p>

<p style="text-indent:2em">严格来说，这两种方式各有优劣。虽然从一定程度上来说，后者牺牲了服务调用的性能，但也避免了上面提到的原生RPC带来的问题。而且REST相比RPC更为灵活，服务提供方和调用方的依赖只依靠一纸契约，不存在代码级别的强依赖，这在强调快速演化的微服务环境下，显得更加合适。</p>

品牌机与组装机的区别

<p style="text-indent:2em">很明显，Spring Cloud的功能比DUBBO更加强大，涵盖面更广，而且作为Spring的拳头项目，它也能够与Spring Framework、Spring Boot、Spring Data、Spring Batch等其他Spring项目完美融合，这些对于微服务而言是至关重要的。使用Dubbo构建的微服务架构就像组装电脑，各环节我们的选择自由度很高，但是最终结果很有可能因为一条内存质量不行就点不亮了，总是让人不怎么放心，但是如果你是一名高手，那这些都不是问题；而Spring Cloud就像品牌机，在Spring Source的整合下，做了大量的兼容性测试，保证了机器拥有更高的稳定性，但是如果要在使用非原装组件外的东西，就需要对其基础有足够的了解。</p>

社区支持与更新力度

<p style="text-indent:2em">最为重要的是，DUBBO停止了5年左右的更新，虽然2017.7重启了。对于技术发展的新需求，需要由开发者自行拓展升级（比如当当网弄出了DubboX），这对于很多想要采用微服务架构的中小软件组织，显然是不太合适的，中小公司没有这么强大的技术能力去修改Dubbo源码+周边的一整套解决方案，并不是每一个公司都有阿里的大牛+真实的线上生产环境测试过。</p>

