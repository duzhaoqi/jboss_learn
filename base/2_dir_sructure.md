# jboss7的目录结构





<p><span style="font-size:18px;"><span style="color:rgb(35,35,35);"><strong>                                        主目录结构</strong></span></span><span style="font-size:18px;">  </span><span style="font-size:18px;"> </span></p>
<table border="1" cellspacing="0" cellpadding="0" width="658" style="text-align:center;"><tbody><tr><td valign="top">
<p align="center"><strong><span style="color:#232323;"><span style="font-size:18px;">目录</span></span></strong></p>
</td>
<td valign="top">
<p align="center"><strong><span style="color:#232323;"><span style="font-size:18px;">描述</span></span></strong></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">bin</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">Unix</span><span style="color:#444444;">和win</span>环境下的启动脚本和启动配置文件</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">bundles</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">存放OSGI bundle</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">docs/schema</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">存放XML schema</span>定义文件</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">domain</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">domain</span><span style="color:#444444;">模式的配置文件、部署内容和可写区域等</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">modules</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">存放各种模块，AS7</span>是基于模块化的类加载架构</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">standalone</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">standalone</span><span style="color:#444444;">模式的配置文件，部署内容和可写区域等</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">welcome-content</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">欢迎页面</span></span></p>
</td>
</tr></tbody></table><p align="left" style="text-align:center;"><span style="color:#444444;"><span style="font-size:18px;"> </span></span></p>
<p><span style="font-size:18px;"><span style="color:rgb(68,68,68);"><strong>                                                               standalone</strong></span><span style="color:rgb(68,68,68);"><strong>目录结构</strong></span><br /></span>
</p><table border="1" cellspacing="0" cellpadding="0" width="653"><tbody><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">目录</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">描述</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">configuration</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">standalone</span><span style="color:#444444;">模式的配置文件</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">data</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">服务器写入的持久化信息，如通过web</span>管理控制台或CLI部署的项目存放在content目录下</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">deployments</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">用户部署内容存放目录，服务器运行时能自动侦测和部署这些内容。</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">lib/ext</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">利用扩展列表机制安装的library jar</span>的存放位置</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">log</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">日志文件</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">tmp</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">临时文件</span></span></p>
</td>
</tr></tbody></table><span style="font-size:18px;"><br /></span>
<p><span style="font-size:18px;"><span style="color:rgb(68,68,68);"><strong>                                                                domain</strong></span><span style="color:rgb(68,68,68);"><strong>目录结构</strong></span><br /></span>
</p><table border="1" cellspacing="0" cellpadding="0" width="660"><tbody><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">目录          </span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">描述</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">configuration</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">domain</span><span style="color:#444444;">模式的所有配置文件</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">data/content</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">主机控制器内部工作区。内部存储部署内容的地方，用户不能操作这个目录，注：域模式不支持扫描文件系统来部署内容</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">lib/ext</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">利用扩展列表机制安装的library jar</span>的存放位置</span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">log</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">日志文件</span></span></p>
</td>
</tr><tr><td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">servers</span></span></p>
</td>
<td valign="top">
<p align="left"><span style="color:#444444;"><span style="font-size:18px;">应用服务器实例可写区域，每一个应用服务器实例都有它自己的目录，当服务器第一次启动时创建。在每个服务器的目录内包含以下的子目录：</span></span></p>
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">data  </span><span style="color:#444444;">服务器写入信息区</span></span></p>
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">log   </span>
<span style="color:#444444;">日志文件</span></span></p>
<p align="left"><span style="font-size:18px;"><span style="color:#444444;">tmp  </span>
<span style="color:#444444;">临时文件</span></span></p>
</td>
</tr></tbody></table>