---
description: 下表說明 IPPROTO 適用于為 \_ IPv4 位址系列建立之通訊端的 RM 通訊端選項， (AF \_ INET) ，其中通訊端函式的通訊協定參數指定為可靠多播 (IPPROTO \_ RM) 。
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: 'IPPROTO_RM 通訊端選項 (Wsrm. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977676"
---
# <a name="ipproto_rm-socket-options"></a>IPPROTO \_ RM 通訊端選項

下表說明 IPPROTO 適用于為 IPv4 位址系列建立之通訊端的 **\_ RM** 通訊端選項， (AF \_ INET) ，其中 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函式的 *通訊協定* 參數指定為可靠多播 (IPPROTO \_ RM) 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

**WINDOWS XP：** 不支援可靠的多播程式設計 (的 PGM) 。

有些通訊端選項需要比這些資料表可以傳達的更多說明;這類選項包含其他頁面的連結。

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**IPPROTO \_ RM 通訊端選項**</dt> <dd> <dl> <dt> 

| 選項                              | Get | 設定 | Optval 類型                                      | Description                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ 新增 \_ 接收（ \_ 如果                |     | 是 | ULONG                                            | 僅限接收者。 新增要接聽的介面 (預設值為第一個列舉) 的本機介面。 Optval 參數會指定要新增的網路介面（以網路位元組順序表示）。 指定的值會在第一次呼叫指定的通訊端時取代預設介面，並在後續的呼叫中新增其他介面。 若要取得 INADDR \_ 任何行為，則必須個別新增每個網路介面。 |
| RM \_ DEL \_ 接收 \_                |     | 是 | ULONG                                            | 僅限接收者。 移除使用 RM ADD RECEIVE 新增的介面（若為） \_ \_ \_ 。 Optval 參數會以網路位元組順序指定要刪除的網路介面。                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | 是 | N/A                                              | 未實作。                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM \_ 高速 \_ \_ 內部網路 \_ 選擇      | 是 | 是 | ULONG                                            | 僅限接收者。 指定是否使用高頻寬 LAN (100Mbps +) 連接。                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | 是 | 是 | ULONG                                            | 僅限寄件者。 會話接受時，延遲聯結接收者允許要求的視窗大小百分比。 最大值為 75% (預設值為零) 。 使用設定為零的值再次呼叫，以停用此設定。                                                                                                                                                                                                |
| RM \_ 速率 \_ 視窗 \_ 大小              | 是 | 是 | [**RM \_ 傳送 \_ 視窗**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | 僅限寄件者。 設定傳輸速率限制、視窗提前時間和視窗大小。                                                                                                                                                                                                                                                                                                                                   |
| RM \_ 接收器 \_ 統計資料            | 是 |     | [**RM \_ 接收器 \_ 統計資料**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | 僅限接收者。 抓取接收會話的統計資料。                                                                                                                                                                                                                                                                                                                                                         |
| RM \_ 傳送 \_ 視窗 \_ 進階 \_ 率         | 是 | 是 | ULONG                                            | 僅限寄件者。 指定尾端 edge 傳送視窗的累加式提前速率 (預設值為 15% ) 。 最大值為50%。                                                                                                                                                                                                                                                                                          |
| RM 傳送者 \_ \_ 統計資料              | 是 |     | [**RM 傳送者 \_ \_ 統計資料**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | 僅限寄件者。 抓取傳送會話的統計資料。                                                                                                                                                                                                                                                                                                                                                             |
| RM 傳送者 \_ \_ 視窗 \_ 前進 \_ 方法 | 是 | 是 | ULONG                                            | 僅限寄件者。 Optval 參數會指定向前移動尾端 edge 傳送視窗時所使用的方法。 Optval 參數只能透過 \_ \_ \_ (預設) 的時間，以電子視窗前進 \_ 。 請注意， \_ \_ 不支援使用 E 視窗 \_ 作為資料快取 \_ \_ 。                                                                                                                                                                     |
| RM \_ SET \_ MCAST \_ TTL                 |     | 是 | ULONG                                            | 僅限寄件者。 設定多播封包的即時 (TTL) 設定的最長時間。 最大值和預設值為255。                                                                                                                                                                                                                                                                                                      |
| RM \_ 設定 \_ 訊息 \_ 界限          |     | 是 | ULONG                                            | 僅限寄件者。 指定要傳送下一個訊息的大小（以位元組為單位）。 僅對訊息模式通訊端有意義， (SOCK \_ RDM) 。 可以在會話進行期間設定。                                                                                                                                                                                                                                                |
| RM \_ 設定 \_ 傳送 \_ IF                   | 是 | 是 | ULONG                                            | 僅限寄件者。 以網路位元組順序設定傳送介面 IP 位址。                                                                                                                                                                                                                                                                                                                                              |
| RM \_ 使用 \_ FEC                        | 是 | 是 | [**RM \_ FEC \_ 資訊**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | 僅限寄件者。 通知寄件者套用轉寄錯誤更正技術以傳送修復資料。 FEC 有三種模式：僅限 pro-主動同位封包、僅限 OnDemand 同位封包或兩者。 如需詳細資訊，請參閱 [**RM \_ FEC \_ 資訊**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) 結構。                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**IPPROTO RM 選項的 Windows 支援 \_**</dt> <dd> <dl> <dt> 

| 選項                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/我 |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ 新增 \_ 接收（ \_ 如果                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ DEL \_ 接收 \_                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 高速 \_ \_ 內部網路 \_ 選擇      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 速率 \_ 視窗 \_ 大小              | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 接收器 \_ 統計資料            | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 傳送 \_ 視窗 \_ 進階 \_ 率         | x         | x                   | x             | x                   | x          |              |             |               |
| RM 傳送者 \_ \_ 統計資料              | x         | x                   | x             | x                   | x          |              |             |               |
| RM 傳送者 \_ \_ 視窗 \_ 前進 \_ 方法 | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 設定 \_ 訊息 \_ 界限          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 設定 \_ 傳送 \_ IF                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ 使用 \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**IPPROTO \_ RM** 通訊端選項以及這些通訊端選項所使用的結構會定義于 *Wsrm* 標頭檔中。

**IPPROTO \_ Rm** 或 IPPROTO 的 **\_ PGM** 常數可以用來指定要使用 RM 通訊端選項之 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket)函數的 *通訊協定* 參數。 在 Windows Vista （含）以後版本的 Microsoft Windows 軟體開發套件 (SDK) 上， **IPPROTO 的 \_ PGM** 常數定義于 *Ws2def .h* 標頭檔中，與 *Wsrm. h* 標頭檔中定義的 **IPPROTO \_ RM** 常數值相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wsrm。h</dt> </dl> |



 

 




