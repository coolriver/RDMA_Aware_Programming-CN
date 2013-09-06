RDMA网络编程用户手册1.4版
======================

###术语表
<table>
<tr><th>术语</th><th>释义</th></tr>
<tr><td>Access Layer</td><td>操作系统底层构架，用来支持访问互联的集群(VPI,InfiniBand,Ethernet,FCoE).
它包括所有支持上层网络协议的基本传输服务、中间件和管理程序</td></tr>
<tr><td>AH(Address Handle)</td><td>在UD QP中，用来描述远程路径的对象</td></tr>
<tr><td>CA(Channel Adapter)</td><td>一个InfiniBand链路的终端设备，它执行传输层的功能</td></tr>
<tr><td>CI(Channel Interface)</td><td>通过网络适配器、相关固件和设备驱动的组合，呈现给Verbs
编程用户的通信管道</td></tr>
<tr><td>CM(Communication Manager)</td><td>负责建立、维持、释放RC和UC QP服务类型连接的体系;服务ID解析协议
确保了使用UD服务的用户找到支持指定设备的QP;每个终端节点的IB端口都有一个CM.</td></tr>
<tr><td>Compare & Swap</td><td>通知远程QP读取一个64bit的值，将这个值与提供的比较对象值作比较
，如果相等，那么就把读取的这个值替换成QP提供的另一个数值。</td></tr>
<tr><td>CQ(Completion Queue)</td><td>一个包含CQE的队列（先进选出）</td></tr>
<tr><td>CQE(Completion Queue Entry)</td><td>CQ中的一个记录，它描述了已完成的WR的信息
（状态，大小等）</td></tr>
<tr><td>DMA(Direct Memory Access)</td><td>允许硬件在不经CPU参与的情况下
将数据块移进和移出内存</td></tr>
<tr><td>Fetch & add</td><td>通知远程QP读取一个64bit的数值，将它替换为它和QP提供
的待加数的和。</td></tr>
<tr><td>GUID(Globally Unique IDentifier)</td><td>在一个子网中，唯一标志一个设备或组件的
64bit数字</td></tr>
<tr><td>GID(Global IDentifier)</td><td>一个128位的标志，用来标志网络适配器上的一个端口，
路由器上或者组播里的一个端口;为了更有效地寻找、通信和路由，IBA在标准IPV6地址的基础上定义了一些额外的
特性和约束，这就形成了GID。</td></tr>
<tr><td>GRH(Global Routing Header)</td><td>用来在子网间传递数据包和传递组播信息的包头。
包头基于IPv6协议</td></tr>
<tr><td>Network Adapter</td><td>允许网络中计算机之间传递数据的硬件。</td></tr>
<tr><td>Host</td><td>一台运行着操作系统，并且控制着一个或多个network adapter的计算机。</td></tr>
<tr><td>IB</td><td>InfiniBand</td></tr>
<tr><td> </td><td> </td></tr>
<tr><td>Join operation</td><td>一个IB端口要明确地加入一个多播组，必须向SA发送请求来接收
多播数据包。</td></tr>
<tr><td>lkey</td><td>在MR注册之后接收到的一个数字，它在本地被WR用来标志内存注册和
相关权限。</td></tr>
<tr><td>LID(Local IDentifier)</td><td>
子网管理程序指定给终端节点的一个16位地址。每个LID在它所在的子网中是唯一的。</td></tr>
<tr><td>LLE(Low Latency Ethernet)</td><td>
在CEE(Converged Enhanced Ethernet聚合加强型以太网)基础之上的RDMA服务。CEE允许IB在以太网上传输。</td></tr>
<tr><td>NA(Network Adapter)</td><td>
一个网络链接的终端设备，它执行传输层功能。</td></tr>
<tr><td>MGID(Multicast Group ID)</td><td>
MGID唯一标志一个IB多播组，它由SM管理。SM将每个MGID都关联一个MLID，并对网络中的IB交换机
进行编程控制，确保加入多播组的所有端口都能接收到数据包。</td></tr>
<tr><td>MR(Memory Region)</td><td>
已被注册为被允许使用的连续内存缓冲区。为了使网络适配器能利用它们，这些缓冲区需要先被
注册。在注册期间，一个L_Key和R_Key被创建出来用来关联相应的注册缓冲区。</td></tr>
<tr><td>MTU(Maximum Transfer Unit)</td><td>
</td></tr>
</table>