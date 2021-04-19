---
description: 下表說明適用于 \_ 針對 ipx/SPX 位址系列 (AF ipx) 所建立之通訊端的 NSPROTO IPX 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 getsockopt 和 setsockopt 函數參考頁面。
ms.assetid: 0d5c8299-14d7-41e5-8ff6-f57a732acb26
title: 'NSPROTO_IPX 通訊端選項 (Wsnwlink .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e1fabed1963c3549d2d5a34fb432cac795e07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984820"
---
# <a name="nsproto_ipx-socket-options"></a>NSPROTO \_ IPX 通訊端選項

下表說明適用于針對 IPX/SPX 位址系列 (AF ipx) 所建立之通訊端的 **NSPROTO \_ IPX** 通訊端選項 \_ 。 如需取得和設定通訊端選項的詳細資訊，請參閱 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 和 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 函數參考頁面。

若要列舉通訊協定，並針對每個已安裝的通訊協定探索支援的屬性，請使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)、 [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)或 [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) 函數。

<dl> <dt><span id="NSPROTO_IPX_Socket_Options"></span><span id="nsproto_ipx_socket_options"></span><span id="NSPROTO_IPX_SOCKET_OPTIONS"></span>**NSPROTO \_ IPX 通訊端選項**</dt> <dd> <dl> <dt> 

| 選項                      | Get | 設定 | Optval 類型                  | Description                                                                                                                                                                                                                                                                     |
|-----------------------------|-----|-----|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX \_ 位址                | 是 |     | **IPX \_ 位址 \_ 資料**       | 傳回已啟用 IPX 的特定介面卡相關資訊。                                                                                                                                                                                                          |
| IPX \_ 位址 \_ 通知        | 是 |     | **IPX \_ 位址 \_ 資料**       | 當 IPX 介面卡的狀態變更時，以非同步方式通知。                                                                                                                                                                                                              |
| IPX \_ DSTYPE                 | 是 | 是 | DWORD                        | 取得或設定要用來傳送封包的 SPX 標頭中資料流程欄位的值。                                                                                                                                                                                          |
| IPX \_ 延伸 \_ 位址      |     | 是 | DWORD (布林值)               | 啟用 IPX 封包的擴充定址選項。                                                                                                                                                                                                                          |
| IPX \_ FILTERPTYPE            | 是 | 是 | DWORD                        | 取得或設定目前的 IPX 接收篩選封包類型。 只會傳回封包類型等於 optval 參數中指定之值的 IPX 封包。 封包類型不相符的封包會被捨棄。 這僅適用于資料包通訊端。 |
| IPX \_ GETNETINFO             | 是 |     | **IPX \_ NETNUM \_ 資料**        | 傳回特定 IPX 網路編號的相關資訊。 **Ipx \_ netnum \_ 資料** 結構的 netnum 成員必須設定為要傳回的 ipx 網路編號。                                                                                                     |
| IPX \_ GETNETINFO \_ NORIP      | 是 |     | **IPX \_ NETNUM \_ 資料**        | 傳回特定 IPX 網路編號的相關資訊，而不需要傳送 RIP 要求。 **Ipx \_ netnum \_ 資料** 結構的 netnum 成員必須設定為要傳回的 ipx 網路編號。                                                                       |
| IPX \_ IMMEDIATESPXACK        |     | 是 | DWORD (布林值)               | 如果設定為 **TRUE**，請勿延遲在 SPX 連接上傳送 ack。                                                                                                                                                                                                             |
| IPX \_ 最大 \_ 介面卡 \_ 數目      | 是 |     | DWORD                        | 傳回目前已啟用 IPX 的介面卡數目。                                                                                                                                                                                                                             |
| IPX \_ MAXSIZE                | 是 |     | DWORD                        | 傳回可以傳送的最大 IPX 資料包大小（以位元組為單位）。                                                                                                                                                                                                                |
| IPX \_ PTYPE                  | 是 | 是 | DWORD                        | 取得或設定封包類型。 在 optval 參數中指定的值將會設定為每個從這個通訊端傳送的 IPX 封包上的封包類型。                                                                                                                             |
| IPX \_ 接收 \_ 廣播     |     | 是 | DWORD (布林值)               | 如果設定為 **TRUE**，則會接收廣播 IPX 封包。                                                                                                                                                                                                                              |
| IPX \_ RECVHDR                |     | 是 | DWORD (布林值)               | 如果設定為 **TRUE**，則會接收包含資料的 IPX 通訊協定標頭。                                                                                                                                                                                                                     |
| IPX \_ RERIPNETNUMBER         | 是 |     | **IPX \_ NETNUM \_ 資料**        | 使用新的 RIP 要求傳回有關指定 IPX 網路編號的資訊。 **Ipx \_ netnum \_ 資料** 結構的 netnum 成員必須設定為要傳回的 ipx 網路編號。                                                                            |
| IPX \_ SPXGETCONNECTIONSTATUS | 是 |     | **IPX \_ SPXCONNSTATUS \_ 資料** | 傳回連線的 SPX 通訊端統計資料相關資訊。                                                                                                                                                                                                                |
| IPX \_ STOPFILTERPTYPE        |     | 是 | DWORD                        | 移除篩選，並停止篩選 optval 參數中指定的封包類型。                                                                                                                                                                                        |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_NSPROTO_IPX_options"></span><span id="windows_support_for_nsproto_ipx_options"></span><span id="WINDOWS_SUPPORT_FOR_NSPROTO_IPX_OPTIONS"></span>**NSPROTO IPX 的 Windows 支援 \_ 選項**</dt> <dd> <dl> <dt> 

| 選項                      | Windows Vista 和更新版本 | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/我 |
|-----------------------------|-------------------------|---------------------|------------|--------------|-------------|---------------|
| IPX \_ 位址                |                         | x                   | x          | x            | x           | x             |
| IPX \_ 位址 \_ 通知        |                         | x                   | x          | x            | x           | x             |
| IPX \_ DSTYPE                 |                         | x                   | x          | x            | x           | x             |
| IPX \_ 延伸 \_ 位址      |                         | x                   | x          | x            | x           | x             |
| IPX \_ FILTERPTYPE            |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO             |                         | x                   | x          | x            | x           | x             |
| IPX \_ GETNETINFO \_ NORIP      |                         | x                   | x          | x            | x           | x             |
| IPX \_ IMMEDIATESPXACK        |                         | x                   | x          | x            | x           | x             |
| IPX \_ 最大 \_ 介面卡 \_ 數目      |                         | x                   | x          | x            | x           | x             |
| IPX \_ MAXSIZE                |                         | x                   | x          | x            | x           | x             |
| IPX \_ PTYPE                  |                         | x                   | x          | x            | x           | x             |
| IPX \_ 接收 \_ 廣播     |                         | x                   | x          | x            | x           | x             |
| IPX \_ RECVHDR                |                         | x                   | x          | x            | x           | x             |
| IPX \_ RERIPNETNUMBER         |                         | x                   | x          | x            | x           | x             |
| IPX \_ SPXGETCONNECTIONSTATUS |                         | x                   | x          | x            | x           | x             |
| IPX \_ STOPFILTERPTYPE        |                         | x                   | x          | x            | x           | x             |



 


</dt> </dl> </dd> </dl>

下列 **NSPROTO 的 \_ IPX** 通訊端選項定義于 windows 通訊端 2 Protocol-Specific 附錄中，但不是由 WINDOWS IPX/SPX 通訊協定所執行。

*層級* **=****NSPROTO \_IPX**



| 選項           | 類型 | 預設                         | 意義                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPX 總和 \_ 檢查碼    | Bool | 關                             | 當設定時，IPX 會對傳出封包執行總和檢查碼，並驗證連入封包的總和檢查碼。                                                          |
| IPX \_ TXPKTSIZE   | int  | 最大可達1466的媒體大小 | 設定傳送資料包的最大大小。 此大小不包括可能也會使用的 IPX 標頭或任何媒體標頭。 可能會增加至媒體大小。    |
| IPX \_ RXPKTSIZE   | int  | 最大可達1466的媒體大小 | 設定接收資料包的最大大小。 此大小不包括可能也會使用的 IPX 標頭或任何媒體標頭。 可能會增加至媒體大小。 |
| IPX \_ TXMEDIASIZE | int  | 主要面板                   | 傳回設定資料包大小上限的傳送媒體大小。                                                                                       |
| IPX \_ RXMEDIASIZE | int  | 主要面板                   | 傳回設定資料包大小上限的接收媒體大小。                                                                                    |
| IPX \_ 主要     | Bool | 主要                         | 將流量限制為主要網路板。                                                                                                               |



 

下列 **NSPROTO 的 \_ SPX** 通訊端選項定義于 windows 通訊端 2 Protocol-Specific 附錄中，但不是由 WINDOWS IPX/SPX 通訊協定在 windows 上執行。

*層級* **=****NSPROTO \_SPX**



| 選項           | 類型 | 預設                         | 意義                                                                                                                                                       |
|------------------|------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SPX 總和 \_ 檢查碼    | Bool | 關                             | 當設定時，IPX 會對傳出封包執行總和檢查碼，並驗證連入封包的總和檢查碼。 並非所有平臺都支援。                          |
| SPX \_ TXPKTSIZE   | int  | 最大可達1466的媒體大小 | 設定傳送資料包的最大大小。 此大小不包含 SPX 標頭或任何可能使用的媒體標頭。 可能會增加至媒體大小。    |
| SPX \_ RXPKTSIZE   | int  | 最大可達1466的媒體大小 | 設定接收資料包的最大大小。 此大小不包含 SPX 標頭或任何可能使用的媒體標頭。 可能會增加至媒體大小。 |
| SPX \_ TXMEDIASIZE | int  | 主要面板                   | 傳回傳送媒體大小減去 SPX 和媒體標頭。 這會設定訊息分割封包大小的上限。                                       |
| SPX \_ RXMEDIASIZE | int  | 主要面板                   | 傳回接收媒體大小減去 SPX 和媒體標頭。 這會設定接收封包大小的上限。                                                 |
| SPX \_ RAWSPX      | Bool | 關                             | 設定時，會使用資料傳遞 IPX/SPX 通訊協定標頭。                                                                                                |



 

## <a name="remarks"></a>備註

**NSPROTO \_ IPX** 通訊端選項以及這些通訊端選項所使用的結構會定義在 *Wsnwlink .h* 標頭檔中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wsnwlink。h</dt> </dl> |



 

 




