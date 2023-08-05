# 小米路由器 API 文档

-----

> 因本人已不再使用小米路由器，所以本文档无限期搁置中... 欢迎大佬 Fork 之后继续扒 API

-----

## 1. 登录

**调用地址**: `/api/xqsystem/login`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
username | `True` | admin | 无
password | `True` | 无 | 需要加密
nonce | `True` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
url | 指向后台管理的主页 | 无 |
token | 即 `stok` | 无 |

-----

## 2. 获取初始化信息

**调用地址**: `/api/xqsystem/init_info`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
isSupportMesh | 是否支持 Mesh | `1.True  0.False` |
secAcc | 未知 | `1.True  0.False`|
inited | 已初始化 | `1.True  0.False` |
connect | 未知 | `1.True  0.False` |
modules | 未知 | `1.True  0.False` |
replacement_assistant | 未知 | `1.True  0.False` |
hardware | 硬件 | 当前硬件 |
language | 系统语言 | 当前系统语言 |
romversion | 固件版本 | 当前固件版本 |
countrycode | 国家代码 | 当前国家代码 |
id | 路由器序列号 | 当前路由器序列号 |
routername | 路由器名称 | 当前路由器名称 |
displayName | 显示名称 | 当前显示名称 |
maccel | 未知 | `1.True  0.False` |
model | 机型 | 当前机型 |
DisableTencent | 未知 | `1.True  0.False` |
bound | 未知 | `1.True  0.False` |
routerId | 设备 ID | 当前路由器的设备 ID (米家) |
isRedmi | 是否为 Redmi | `1.True  0.False` |

-----

## 3. 获取工厂信息

**调用地址**: `/api/xqsystem/fac_info`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
init | 是否初始化 | `1.True  0.False` |
wl0_ssid | 网卡 `wlan0` 上的 SSID | 当前 SSID |
wl1_ssid | 网卡 `wlan1` 上的 SSID | 当前 SSID |
telnet | 是否开启 Telnet | `1.True  0.False` |
ssh | 是否开启 SSH | `1.True  0.False` |
facmode | 是否为工厂模式 | `1.True  0.False` |
4kblock | 是否为 4K Block | `Boolean` |
secboot | 是否开启安全启动 | `Boolean` |
uart | 是否开启 UART | `Boolean` |

-----

## 4. Farewell (未知)

**调用地址**: `/api/xqsystem/farewell`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |

-----

## 5. 获取 Token 信息

**调用地址**: `/api/xqsystem/token`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
id | 路由器序列号 | 当前路由器序列号 |
name | 路由器名称 | 当前路由器名称 |
token | 即 `stok` | 无 |

-----

## 6. 设置 Init 状态

**调用地址**: `/api/xqsystem/set_inited`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
client | `False` | `ios, android, other` | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |

-----

## 7. 获取系统信息

**调用地址**: `/api/xqsystem/sys_info`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
hardware | 硬件 | 当前硬件 |
routerName | 路由器名称 | 当前路由器名称 |
romVersion | 固件版本 | 当前固件版本 |
romChannel | 固件类型 | 当前固件类型 (`release.稳定版  stable.开发版  current.测试版`) |

-----

## 8. 置 Init 状态

**调用地址**: `/api/xqsystem/set_inited`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
client | `False` | `ios, android, other` | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |

-----

## 9. 设置密码

**调用地址**: `/api/xqsystem/set_name_password`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
nonce | `True` | 无 | 无
oldPwd | `True` | 无 | 旧的密码
newPwd | `True` | 无 | 要设置的密码

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 10. 检查固件更新

**调用地址**: `/api/xqsystem/check_rom_update`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
needUpdate | 是否需要更新 | `1.True  0.False` |
changeLog | 新版本更新日志 | 新版本更新日志 |
version | 最新版本 | 当前最新版本 |
status - status | 未知 | 未知 |
status - percent | 未知 | 未知 |

-----

## 11. WAN、LAN 口状态

**调用地址**: `/api/xqsystem/lan_wan`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
downspeed | 当前下载速度 | 当前下载速度 (Bit/s) |
maxdownloadspeed | 最高下载速度 | 最高下载速度 (Bit/s) |
download | 已下载的数据量 | 已下载的数据量 (Bit) |
upspeed | 当前上传速度 | 当前上传速度 (Bit/s) |
maxuploadspeed | 最高上传速度 | 最高上传速度 (Bit/s) |
upload | 已上传的数据量 | 已上传的数据量 (Bit) |
devname | 接口名称 | WAN/LAN 口对应的接口名称 |

-----

## 12. 刷入固件

**调用地址**: `/api/xqsystem/flash_rom`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

**备注**: 刷入位于事先上传的固件

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 13. 获取路由器名称

**调用地址**: `/api/xqsystem/router_name`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
routerName | 路由器名称 | 当前路由器名称 |

-----

## 14. 获取设备列表

**调用地址**: `/api/xqsystem/device_list`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
all | `False` | 0 | `1.显示所有连接过的设备  0.显示当前连接的设备`

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
mac | MAC 地址 | 用作请求的设备 / List 成员的设备的 MAC 地址 |
isap | 是否为 AP | `1.True  0.False` |
parent | 未知 | 未知 |
port | 端口 | 未知 |
hostname | 主机名 | 设备的主机名 |
mac | MAC 地址 | 设备的 MAC 地址 |
origin_name | 原始名称 | 设备的原始名称 |
ptype | 未知 | 未知 |
authority - wan | 可访问 `wan` 网络 | `1.True  0.False` |
authority - lan | 可访问 `lan` 网络 | `1.True  0.False` |
authority - admin | 可以管理员身份访问 | `1.True  0.False` |
authority - pridisk | 可访问隐私盘 (如果支持挂载磁盘) | `1.True  0.False` |
company - priority | 未知 | 未知 |
company - type | 未知 | 未知 |
company - type - p | 未知 | 未知 |
company - type - c | 未知 | 未知 |
company - name | 制造商名称 | 设备的制造商名称 |
company - icon | 制造商 Logo | 设备巅峰制造商 Logo |
push | 未知 | 未知 |
name | 名称 | 设备的名称 (自定义) |
times | 未知 | 未知 |
type | 连接方式 | 设备连接方式 (`line.有线连接  wifi.无线连接`) |
statistics - mac | MAC 地址 | 设备的 MAC 地址 |
statistics - ip | DHCP IP 地址 | 设备的 DHCP IP 地址 |
statistics - online | 已在线时长 | 设备的已在线时长 (秒) |
statistics - downspeed | 当前下载速度 | 设备当前下载速度 (Bit/s) |
statistics - maxdownloadspeed | 最大下载速度 | 设备最大下载速度 (Bit/s) |
statistics - download | 已下载的数据量 | 设备已下载的数据量 (Bit) |
statistics - upspeed | 当前上传速度 | 设备当前上传速度 (Bit/s) |
statistics - maxuploadspeed | 最大上传速度 | 设备最大上传速度 (Bit/s) |
statistics - upload | 已上传的数据量 | 设备已上传的数据量 (Bit) |
ctype | 未知 | 未知 |
online | 是否在线 | 设备当前是否在线 (`1.True  0.False`) |

-----

## 15. 设置设备名称

**调用地址**: `/api/xqsystem/set_device_nickname`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
mac | `True` | 无 | 要修改名称的设备的 MAC 地址
name | `True` | 无 | 要设置的名称
owner | `False` | 无 | 未知
device | `False` | 无 | 未知

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 16. 是否联网成功

**调用地址**: `/api/xqsystem/internet_connect`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
connect | 联网状态 | `0.True  1.False` |

-----

## 17. 上传 ROM 文件 ([参见: 刷入固件](#刷入固件))

**调用地址**: `/api/xqsystem/upload_rom`  

**必须 Token**: `True`   

**请求方式**: `POST / PUT`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
UPLOADFILE | `True` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |
downgrade | 是否为降级固件 | `Boolean`

-----

## 18. 获取可用语言

**调用地址**: `/api/xqsystem/get_languages`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
list - lang | 可用语言代码 | 可用语言代码 |
list - name | 可用语言 | 可用语言 |
lang | 当前语言 | 当前语言 |

-----

## 19. 获取当前语言

**调用地址**: `/api/xqsystem/get_main_language`  

**必须 Token**: `False`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
lang | 当前语言代码 | 当前语言代码 |

-----

## 20. 设置语言

**调用地址**: `/api/xqsystem/set_language`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
language | `True` | 无 | 语言代码

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 21. 上传日志

**调用地址**: `/api/xqsystem/upload_log`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 22. 设置基本信息 (初始化)

**调用地址**: `/api/xqsystem/router_init`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
nonce | `True` | 无 | 无
newPwd | `True` | 无 | 新的密码
oldPwd | `True` | 无 | 旧的密码
wifiPwd | `True` | 无 | WiFi 密码
wifi24Ssid | `True` | 无 | 2.4Ghz WiFi SSID
wifi50Ssid | `True` | 无 | 5Ghz WiFi SSID
wanType | `True` | 无 | `wan` 类型 `(pppoe.拨号  dhcp.自动获取)`
pppoeName | `False` | 无 | 宽带账号
pppoePwd | `False` | 无 | 宽带密码

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
msg | 状态信息 | 状态信息 (如果有) |

-----

## 23. 获取详细信息

**调用地址**: `/api/xqsystem/information`  

**必须 Token**: `True`   

**请求方式**: `Everything`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 |
-|-|-|
code | 状态码 | 0 |
connect | 联网状态 | `0.True  1.False` |
wifi - ifname | 接口内部名称 | `WiFi` 接口的内部名称 |
wifi - channelInfo - bandwidth | 频段带宽 | `WiFi` 的频段带宽 |
wifi - channelInfo - bandList | 可用频段带宽 | `WiFi` 可用的频段带宽 |
wifi - channelInfo - channel | 信道 | `WiFi` 的信道 |
wifi - encryption | 加密方式 | `WiFi` 的加密方式 |
wifi - bandwidth | 频段带宽 | `WiFi` 的频段带宽 |
wifi - kickthreshold | RSSI | `WiFi` 的RSSI 数值 |
wifi - status | 启用状态 | `WiFi` 是否启用 `(1.True  0.False)` |
wifi - mode | 模式 | `WiFi` 模式 `(参考 OpenWrt 的 Master、Bridge)` |
wifi - bsd | 未知 | 未知 |
wifi - ssid | SSID | `WiFi` 的 SSID |
wifi - weakthreshold | 保护阈值 | 未知 |
wifi - device | 设备 | `WiFi` 使用的设备 |
wifi - ax | 802.11ax | `WiFi` 是否启用 802.11ax `(1.True  0.False)` |
wifi - hidden | 隐藏 SSID | `WiFi` 是否隐藏 SSID `(1.True  0.False)` |
wifi - password | WiFi 密码 | `WiFi` 的 WiFi 密码 |
wifi - channel | 信道 | `WiFi` 的信道 |
wifi - txpwr | 发射功率 | `WiFi` 发射功率 `(max.穿墙  mid.标准  min.节能)` |
wifi - weakenable | 未知 | 未知 |
wifi - txbf | BeamForming | `WiFi` 波束成形波数 `(3.启用 BeamForming  0.关闭 BeamForming)` |
wan - mac | MAC 地址 | `wan` 口的 MAC 地址 |
wan - link | 线路数量 | `wan` 口连接的线路数量 |
wan - details - username | PPPOE 用户名 | `wan` 口的 PPPOE 用户名 |
wan - details - password |  PPPOE 密码 | `wan` 口的 PPPOE 密码 |
wan - special | 特殊拨号 | `wan` 口是否使用特殊拨号 `(1.True  0.False)` |
wan - details - ifname | 内部名称 | 内部名称 |
wan - details - wanType | 无 | `wan` 类型 `(pppoe.拨号  dhcp.自动获取)`
wan - details - mru |  Maximum Receive Unit | `wan` 口的最大接收单元 |
wan - mtu | Maximum Transmission Unit | `wan` 口的最大传输单元 |
wan - details - service |  未知 | 未知 |
wan - details - peerdns |  PeerDNS | `wan` 口的 PeerDNS `(1.True  0.False)` |
wan - status | 启用状态 | `wan` 口的启用状态 `(1.True  0.False)` |
wan - dnsAddrs | DNS 1 | `wan` 口的 DNS 1 |
wan - dnsAddrs1 | DNS 2 | `wan` 口的 DNS 2 |
wan - uptime | 已在线时长 | `wan` 口的已在线时长 (秒) |
wan - gateWay | 网关 | `wan` 口的网关 |
wan - ipv6_info - ifname | IPv6 内部名称 | IPv6 的内部名称 |
wan - ipv6_info - lan_ip6addr | LAN IPv6 地址 | LAN IPv6 地址 |
wan - ipv6_info - lan_ip6prefix | LAN IPv6 前缀 | LAN IPv6 前缀 |
wan - ipv6_info - peerdns | PeerDNS | IPv6 的 PeerDNS `(1.True  0.False)` |
wan - ipv6_info - wanType | IPv6 连接类型 | IPv6 连接类型 |
wan - ipv6_info - ip6addr | WAN IPv6 地址 | WAN IPv6 地址 |
wan - ipv4 - ip | WAN IPv4 地址 | WAN IPv4 地址 |
wan - ipv6_info - dns | IPv6 DNS 地址 | IPv6 DNS 地址 |
wan - ipv6_info - dns_conf | IPv6 DNS 地址 | IPv6 DNS 地址 |
wan - ipv6_show | 显示 IPv6 选项 | 显示 IPv6 选项 `(1.True  0.False)` |
wan - ipv4 - mask | 子网掩码 | 子网掩码 |
lan - mac | MAC 地址 | `lan` 口的 MAC 地址 |
lan - uptime | 已在线时长 | `lan` 口的已在线时长 (秒) |
lan - status | 启用状态 | `lan` 口的启用状态 `(1.True  0.False)` |
lan - dnsAddrs | DNS 1 | `lan` 口的 DNS 1 |
lan - dnsAddrs1 | DNS 2 | `lan` 口的 DNS 2 |
lan - ipv4 - mask | LAN 子网掩码 | LAN 子网掩码 |
lan - ipv4 - ip | LAN IPv4 地址 | LAN IPv4 地址 |

------

## 24. 获取路由器状态

**调用地址**: `/api/misystem/status`  

**必须 Token**: `True`   

**请求方式**: `GET`   

### 参数说明

参数名称 | 必须 | 默认值 | 备注
-|-|-|-
无 | `False` | 无 | 无

### 返回值说明

参数名称 | 解释 | 值 
-|-|-
code | 状态码 | 0 
 dev         | 设备列表     | 数组 
mem | 内存状态     | 数组                   
temperature | 温度 | 若没有温度传感器则为0 
count | 连接设备计数 | 数组 
hardware | 路由器信息 | 数组 
upTime | 在线时长 | 路由器的运行时间（秒） 
cpu | cpu信息 | 数组 
wan | `wan`口数据 | 数组 

#### dev数组

> 内有多个数组

| 参数名称         | 解释         | 值                           |
| ---------------- | ------------ | ---------------------------- |
| mac              | mac          | 设备mac地址                  |
| maxdownloadspeed | 最大下载速度 | 数字（B/S）                  |
| upload           | 总上传量     | 数字（B）                    |
| upspeed          | 上传速度     | 数字（B/S）                  |
| downspeed        | 下载速度     | 数字（B/S）                  |
| online           | 在线时长     | 数字（S）                    |
| devname          | 设备名称     | 所连接设备的名称（自定义后） |
| maxuploadspeed   | 最大上传速度 | 数字（B/S）                  |
| download         | 总下载量     | 数字（B）                    |

#### mem数组

| 参数名称 | 解释     | 值                       |
| -------- | -------- | ------------------------ |
| usage    | 内存占用 | 小数（eg:**0.5**）       |
| total    | 内存大小 | 字符串（eg:**128MB**）   |
| hz       | 内存频率 | 字符串（eg:**1200MHz**） |
| type     | 内存类型 | 字符串（eg:**DDR3**）    |

#### count数组

| 参数名称 | 解释               | 值   |
| -------- | ------------------ | ---- |
| all      | 连接过的设备数量   | 数字 |
| online   | 当前在线的设备数量 | 数字 |

#### hardware数组

| 参数名称 | 解释           | 值     |
| -------- | -------------- | ------ |
| mac      | 路由器MAC地址  | 字符串 |
| platform | 路由器型号     | 字符串 |
| version  | 路由器系统版本 | 字符串 |
| channel  | 路由器发行版本 | 字符串 |
| sn       | 路由器**sn**码 | 字符串 |

#### cpu数组

| 参数名称 | 解释      | 值     |
| -------- | --------- | ------ |
| core     | CPU核心数 | 数字   |
| hz       | CPU频率   | 字符串 |
| load     | CPU占用   | 小数   |

#### wan数组

| 参数名称         | 解释                              | 值     |
| ---------------- | --------------------------------- | ------ |
| downspeed        | `wan`口的下载速度                 | 数字   |
| maxdownloadspeed | `wan`口的最大下载速度             | 数字   |
| history          | `wan`口的上下行速度之和的历史记录 | 数组   |
| devname          | `wan`口设备名称                   | 字符串 |
| upload           | `wan`口总上传量                   | 数字   |
| upspeed          | `wan`口的下载速度                 | 数字   |
| maxuploadspeed   | `wan`口的最大上传速度             | 数字   |
| download         | `wan`口的最大下载                 | 数字   |

##### history数组

​	有50个数字，表示速度（B/S）
