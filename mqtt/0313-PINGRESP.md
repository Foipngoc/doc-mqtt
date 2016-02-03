# 第三章 MQTT控制报文

- [3.1 CONNECT – 连接服务端 20](0301-CONNECT.md)
- [3.2 CONNACK – 确认连接请求 28](0302-CONNACK.md)
- [3.3 PUBLISH – 发布消息 30](0303-PUBLISH.md)
- [3.4 PUBACK –发布确认 33](0304-PUBACK.md)
- [3.5 PUBREC – 发布收到（QoS 2，第一步） 34](0305-PUBREC.md)
- [3.6 PUBREL – 发布释放（QoS 2，第二步） 35](0306-PUBREL.md)
- [3.7 PUBCOMP – 发布完成（QoS 2，第三步） 36](0307-PUBCOMP.md)
- [3.8 SUBSCRIBE - 订阅主题 37](0308-SUBSCRIBE.md)
- [3.9 SUBACK – 订阅确认 40](0309-SUBACK.md)
- [3.10 UNSUBSCRIBE –取消订阅 41](0310-UNSUBSCRIBE.md)
- [3.11 UNSUBACK – 取消订阅确认 43](0311-UNSUBACK.md)
- [3.12 PINGREQ – 心跳请求 44](0312-PINGREQ.md)
- [3.13 PINGRESP – 心跳响应 45](0313-PINGRESP.md)
- [3.14 DISCONNECT –断开连接 45](0314-DISCONNECT.md)

## 3.13 PINGRESP – 心跳响应

服务端发送PINGRESP报文响应客户端的PINGREQ报文。表示服务端还活着。

保持连接（Keep Alive）处理中用到这个报文，详情请查看 3.1.2.10节。

### 3.13.1 固定报头

##### 图例 3.34 – PINGRESP报文固定报头

| **Bit** | **7**                 | **6**  | **5** | **4** | **3** | **2** | **1** | **0** |
|---------|-----------------------|--------|-------|-------|-------|-------|-------|-------|
| byte 1  | MQTT控制报文类型 (13) | 保留位 |
|         | 1                     | 1      | 0     | 1     | 0     | 0     | 0     | 0     |
| byte 2  | 剩余长度 (0)          |
|         | 0                     | 0      | 0     | 0     | 0     | 0     | 0     | 0     |

### 3.13.2 可变报头

PINGRESP报文没有可变报头。

### 3.13.3 有效载荷

PINGRESP报文没有有效载荷。