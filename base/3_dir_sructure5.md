# jboss5.1.0目录结构

现在对我使用的JBoss5.1.0版本的目录结构进行简单介绍.

     

## bin目录 
这个文件夹大家应该熟悉,大部分软件都包含bin文件,我们常用的Tomcat也有,这个文件夹里包含了服务器启动，关闭和系统相关的脚本。基本上所有jar文件的进入点和启动脚本都在这个目录里面。通过该文件中的run.bat来启动服务，关闭该文件来关闭服务。

## client目录  
这个文件夹用来保存Java客户端应用或外部web容器（在JBoss之外运行），所需的配置文件和Jar文件。是客户端与JBoss通信所需的的Java库,方便客户端的使用。我们客户端如果要使用Jboss服务器的bean等，需要引入这个文件夹里所有的Jar包才可以。

## docs目录 
包含一些jboss的XML DTD文件，还有一些案例和文档。

## lib目录
 包含JBoss所需的jar文件。JBoss启动时加载，且被所有JBoss配置共享，这个属于JBoss自身需要的jar文件，所以不要把我们自己的jar文件放在这个目录。

## common目录
这个文件夹在JBoss4里没有，在JBoss5中新加的，里面都是一些jar文件，包括log4j和Hibernate等包，个人认为这些包是可以与JBoss结合使用的，是我们使用JBoss是可选用的功能，JBoss应该是为了给我们使用者方便，把这些它支持的功能jar也一起加了进来。

## server目录
　包含JBoss服务器实例的配置集合。这里的每个子目录就是一个不同的服务器实例配置。每个配置必须放在不同的子目录。子目录的名字表示配置的名字。JBoss4里面默认有三个配置集合：minimial，default和all，默认使用的是default。JBoss5之后，里除了有以上三个配置外，又加入了web和standard两项。下面看server里的主要内容：
- all      
这个配置是JBoss的完全配置，启动所有服务，包括集群和IIOP。 
- default     
这个是JBoss的默认配置。 通常使用的是这个配置，不包括集群和IIOP。在没有在JBoss命令航中指定配置名称时使用。   
 - conf   
 JBoss的配置文件。conf目录中包含了这个服务器的启动描述文件jboss-service.xml。这个文件定义了服务器运行时间内提供那些固定的核心服务。
 
 - data    
 JBoss的数据库文件。服务中需要存储内容到文件系统的都会保存到data目录。比如，嵌入的数据库，或者JBossMQ。 JBoss内嵌的Hypersonic database的数据也是保存到这里的。
  - deploy   
  JBoss的热部署目录。deploy中包含可热部署的服务（可以在服务器运行时动态添加和删除）。我们可以发布应用程序代码的压缩包（JAR，WAR和EAR文件）到这里。这里目录会被搜索更新，所有修改的组件都会被自动重新部署。 (这个文件夹的作用很像Tomcat里的webapps)

 - lib         
 这个目录中包含这个服务器配置需要的JAR文件，JBoss在启动特定配置时加载他们。这些java库不会被热部署，所以我们可以添加我们自己需要的库文件到这里（使用default的情况下），如JDBC驱动，程序所需接口等。所有的jar文件将在服务器启动的时候被加载到共享的classpath中。 因为是启服务时加载的，所以属于用户级别的。(all和minimial，web，standerd配置都包含以上四个目录。） 

 - log   
 JBoss的日志文件。 如果我们要修改日志输出目录，可以通过配置conf/log4j.xml实现。可通过改文件夹内容的记录来查看每天的日志输出情况。
 - tmp   
 JBoss的临时文件。用来提供JBoss服务的临时存储。

 - work  
 提供给jboss web编译jsp文件用。 log、tmp和work是default配置独有的。 

Server文件夹里的文件夹介绍完了，现在来看`server/default`文件夹中的主要文件的含义。
      

`server/default/config`目录里面的内容介绍: 

- jboss-service.xml      定义核心服务及其配置。
- jndi.properties           定义了InitialContext属性，当一个InitialContext被无参数构造函数创建时会被使用到。
- jboss-log4j.xml         包含了jboss使用的log4j日志配置。
- login-config.xml         这个文件包含了服务器端验证的配置的样例，当使用基于JAAS验证时会被用到。
- props/*       这个文件夹目录包含了jmx-console所需的用户和角色配置文件。 
- standardjboss.xml    提供了JBoss默认容器配置。
- standardjbosscmp-jdbc.xml     这个文件提供了JBoss CMP 引擎的默认配置文件。
- xmdesc/*           包含了jboss-service.xml 中定义的服务的XMBean描述文件。


`server/default/deploy`目录里面的主要内容介绍:  

- cache-invalidation-service.xml     这个服务允许自定义的提除EJB cache。JBoss的Cahche invalidation机制。

----------------ejb3-interceptors-aop.xml         EJB拦截器的配置。

- hsqldb-ds.xml           Hypersonic embedded database服务的配置文件。
- *-ds.xml其服务时，连接数据库文件，可以是mysql-ds.xml或者oracle-ds.xml,每个文件均支持多数据源。


其他的也基本上都是服务的配置文件，例如mail，jmx等，不再一一介绍，水平有限，现在项目功能比较简单，很多现在还没用用到，先了解基本配置信息，其他配置等用到的时候可以再细查。