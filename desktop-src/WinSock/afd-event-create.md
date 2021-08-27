---
description: 適用于通訊端建立作業的 Winsock 網路追蹤事件。
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 7ae6f50646ad863be711ab6d48e775aeac9023a053e29044f3921e1dee8c9948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121478"
---
# <a name="afd_event_create-event"></a>AFD \_ 事件 \_ 建立事件

**AFD \_ 事件 \_ 建立** 事件是通訊端建立作業的 Winsock 網路追蹤事件。


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>參數

<dl> <dt>

*EnterExit* 
</dt> <dd>

此事件的資訊。

下表列出 *EnterExit* 參數的可能值：



| 值                                                                        | 意義                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Winsock 要求的開始。<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Winsock 要求已完成。<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Winsock AFD 驅動程式採取內部動作 (中止連線，例如) 。<br/>      |
| <dl> <dt>3</dt> </dl> | TCP/IP 驅動程式導致此事件發生。 這通常表示資料通知。<br/> |
| <dl> <dt>4</dt> </dl> | Winsock AFD 驅動程式會導致此事件發生 (設定 socket 選項，例如) 。<br/> |



 

</dd> <dt>

*位置* 
</dt> <dd>

內部使用的私用欄位。

</dd> <dt>

*處理* 
</dt> <dd>

擁有相關通訊端之進程的 [EPROCESS](/windows-hardware/drivers/kernel/eprocess) 位址。 這是一個不透明的結構，可作為進程的處理常式物件。 如需詳細資訊，請參閱[EPROCESS](/windows-hardware/drivers/kernel/eprocess)結構的 Windows 驅動程式套件檔。

</dd> <dt>

*端點* 
</dt> <dd>

\_通訊端的 AFD 端點位址。

</dd> <dt>

*AddressFamily* 
</dt> <dd>

通訊端的位址系列規格。 位址家族的可能值定義于 *Ws2def .h* 標頭檔中。 請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

目前支援的值為 AF \_ INET 或 af \_ INET6，也就是 IPv4 和 IPv6 的網際網路位址家族格式。 位址家族的其他選項 (AF \_ netbios 搭配 netbios 使用，例如，如果已安裝位址家族的 Windows 通訊端服務提供者，則支援) 。

下表列出位址家族的一般值，雖然可能有許多其他值。



| Af                                                                                                                                                                                                                 | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_UNSPEC**</dt> <dt>0</dt> </dl>           | 未指定位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_INET**</dt> <dt>2</dt> </dl>                 | 第四版網際網路協定 (IPv4) 位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_IPX**</dt> <dt>6</dt> </dl>                    | IPX/SPX 位址系列。 只有在安裝了 NWLink IPX/SPX NetBIOS 相容的傳輸通訊協定時，才支援此位址系列。 <br/> Windows Vista 和更新版本不支援此位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_APPLETALK**</dt> <dt>16</dt> </dl> | AppleTalk 位址系列。 只有在已安裝 AppleTalk 通訊協定的情況下，才支援此位址系列。 <br/> Windows Vista 和更新版本不支援此位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_NETBIOS**</dt> <dt>17</dt> </dl>       | NetBIOS 位址系列。 只有在已安裝適用于 NetBIOS 的 Windows 通訊端提供者時，才支援此位址系列。 <br/> 32 Windows 的位版本支援 NetBIOS 的 Windows 通訊端提供者。 根據預設，此提供者會安裝在32位版本的 Windows 上。 <br/> 64位版本的 Windows 不支援 NetBIOS 的 Windows 通訊端提供者。 <br/> 適用于 NetBIOS 的 Windows 通訊端提供者僅支援將 *type* 參數設定為 **SOCK \_ DGRAM** 的通訊端。<br/> netbios 的 Windows 通訊端提供者與[netbios](/previous-versions/windows/desktop/netbios/portal)程式設計介面不直接相關。 Windows Vista、Windows Server 2008 及更新版本不支援 NetBIOS 程式設計介面。<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_INET6**</dt> <dt>23</dt> </dl>             | 網際網路通訊協定第6版 (IPv6) 位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_IRDA**</dt> <dt>26</dt> </dl>                | 紅外線資料關聯 (IrDA) 位址系列。 <br/> 只有在電腦已安裝紅外線埠和驅動程式時，才支援此位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_BTH**</dt> <dt>32</dt> </dl>                   | 藍牙位址系列。 <br/> 只有在電腦已安裝藍牙介面卡和驅動程式時，才支援此位址系列。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

新通訊端的類型規格。 可能會在 *Winsock2* 標頭檔中定義通訊端類型的值。

下表列出 Windows 通訊端2支援之 *類型* 參數的可能值：



| 類型                                                                                                                                                                                                                    | 意義                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**SOCK \_串流**</dt> <dt>1</dt> </dl>          | 通訊端類型，提供具有 OOB 資料傳輸機制的已排序、可靠、雙向、以連接為基礎的位元組資料流程。 此通訊端類型會使用網際網路位址系列 (AF \_ INET 或 af INET6)  (TCP) 的傳輸控制通訊協定 \_ 。<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**SOCK \_DGRAM**</dt> <dt>2</dt> </dl>             | 支援資料包的通訊端型別，這些是固定 (的不可靠緩衝區通常很小) 最大長度。 此通訊端類型會針對網際網路位址系列使用使用者資料包協定 (UDP)  (AF \_ INET 或 af \_ INET6) 。<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**SOCK \_原始**</dt> <dt>3</dt> </dl>                   | 提供原始通訊端的通訊端類型，可讓應用程式操作下一個上層通訊協定標頭。 若要操作 IPv4 標頭，必須在通訊端上設定 [**IP \_ HDRINCL**](ipproto-ip-socket-options.md) 通訊端選項。 若要操作 IPv6 標頭，必須在通訊端上設定 [**ipv6 \_ HDRINCL**](ipproto-ipv6-socket-options.md) 通訊端選項。 <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**SOCK \_RDM**</dt> <dt>4</dt> </dl>                   | 提供可靠訊息資料包的通訊端類型。 這種類型的範例是在 Windows 中的實際一般多播 (PGM) 多播通訊協定，通常稱為[可靠的多播程式設計](reliable-multicast-programming--pgm-.md)。 <br/> 只有在已安裝可靠多播通訊協定的情況下，才支援此 *類型* 值。<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**SOCK \_SEQPACKET**</dt> <dt>5</dt> </dl> | 提供以資料包為基礎之虛擬資料流程封包的通訊端類型。 <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*通訊協定* 
</dt> <dd>

要使用的通訊協定。 通訊 *協定* 參數的可能選項是指定的位址系列和通訊端類型專用的。 *通訊協定* 的可能值定義于 *Wsrm* 標頭檔中，以及 *Ws2def .h* 標頭檔中定義的 **IPPROTO** 列舉類型。 請注意， *Ws2def .h* 標頭檔會自動包含在 *Winsock2* 中，而且絕不能直接使用。

如果指定0值，呼叫端不會想要指定通訊協定，而服務提供者將選擇要使用的 *通訊協定* 。

下表列出 *通訊協定* 的通用值（雖然可能有許多其他值）。



| protocol                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ICMP**</dt> <dt>1</dt> </dl>          | 網際網路控制訊息通訊協定 (ICMP) 。 如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_IGMP**</dt> <dt>2</dt> </dl>          | 網際網路群組管理通訊協定 (IGMP) 。 如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_RFCOMM**</dt> <dt>3</dt> </dl> | 藍牙的無線頻率通訊 (藍牙 RFCOMM) 通訊協定。 當 *af* 參數為 **af \_ BTH** 且 *類型* 參數為 **SOCK \_ 串流** 時，這是可能的值。 <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_TCP**</dt> <dt>6</dt> </dl>             |  (TCP) 的傳輸控制通訊協定。 當 *af* 參數為 **Af \_ INET** 或 **Af \_ INET6** 且 *類型* 參數為 **SOCK \_ 串流** 時，這是可能的值。<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_UDP**</dt> <dt>17</dt> </dl>            | 使用者資料包協定 (UDP) 。 當 *af* 參數為 **Af \_ INET** 或 **Af \_ INET6** 且 *類型* 參數為 **SOCK \_ DGRAM** 時，這是可能的值。<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ICMPV6**</dt> <dt>58</dt> </dl>   | 網際網路控制訊息通訊協定第6版 (ICMPv6) 。 如果 *af* 參數為 **af \_ UNSPEC**、 **af \_ INET** 或 **af \_ INET6** ，且 *類型* 參數為 **SOCK \_ RAW** 或未指定，則這是可能的值。<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_RM**</dt> <dt>113</dt> </dl>              | 適用于可靠多播的 PGM 通訊協定。 如果 *af* 參數為 **af \_ INET** ，且 *類型* 參數為 **SOCK \_ RDM**，則這是可能的值。 此通訊協定也稱為 **IPPROTO \_ PGM**。 <br/> 只有在已安裝可靠多播通訊協定的情況下，才支援此 *通訊協定* 值。<br/> |



 

</dd> <dt>

*進程* 
</dt> <dd>

實際的處理序識別碼或指標，如果事件是在系統進程或延遲程序呼叫中執行 Winsock 程式碼的結果， (DPC) 在使用者進程) 以外的內容 (內容。

</dd> <dt>

*狀態* 
</dt> <dd>

運算的 NTSTATUS 程式碼。

</dd> </dl>

## <a name="remarks"></a>備註

**AFD \_ 事件 \_ 建立** 事件是針對 Winsock 網路作業進行追蹤，以建立通訊端。 此事件的通道是 Winsock-AFD。 此事件的層級為資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>              |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[**事件 \_ 描述項**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

