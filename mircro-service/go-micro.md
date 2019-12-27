# go-micro

## 前言

  Go Micro是微服务开发的框架。
  Go Micro提供了分布式系统开发的核心要求，包括RPC和事件驱动的通信。
  所述微理念是明智的默认值与一个可插入体系结构。
  
## 功能

Go Micro提取了分布式系统的详细信息。以下是主要功能。

**服务发现**  - 自动服务注册和名称解析。服务发现是微服务开发的核心。当服务A需要与服务B通话时，它需要该服务的位置。默认发现机制是多播DNS（mdns），一种零配置系统。

**负载平衡**  - 基于服务发现的客户端负载平衡。一旦获得了服务的任意数量的实例的地址，我们现在需要一种方法来确定要路由到的节点。我们使用随机散列负载平衡来提供服务之间的平均分配，并在出现问题时重试其他节点。

**消息编码**  - 基于内容类型的动态消息编码。客户端和服务器将使用编解码器以及内容类型为您无缝编码和解码Go类型。各种消息可以被编码并从不同的客户端发送。客户端和服务器默认情况下会处理此问题。默认情况下，这包括protobuf和json。

**请求/响应** - 基于RPC的请求/响应，支持双向流。我们为同步通信提供了一个抽象。对服务的请求将被自动解决，负载均衡，拨号和流式传输。启用tls时，默认传输为http / 1.1或http2。

**异步消息传递**  - PubSub作为异步通信和事件驱动的体系结构的一流公民而内置。事件通知是微服务开发中的核心模式。启用tls时，默认消息传递是点对点http / 1.1或http2。

**可插拔接口**  - Go Micro对每个分布式系统抽象都使用Go接口。因此，这些接口是可插拔的，并允许Go Micro与运行时无关。可以插入任何基础技术。在[官方插件库](github.com/micro/go-plugins)中找到插件 。


## 教程

[go-micro使用范例&教程](https://github.com/micro-in-cn/tutorials/tree/master/examples)