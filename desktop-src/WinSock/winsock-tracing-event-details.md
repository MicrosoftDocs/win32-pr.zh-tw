---
description: Winsock 網路事件追蹤詳細資料
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Winsock 網路事件追蹤詳細資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194029"
---
# <a name="winsock-network-event-tracing-details"></a>Winsock 網路事件追蹤詳細資料

以下將詳細說明每個可追蹤的 Winsock 網路事件，以及描述所記錄的參數和資訊。

## <a name="socket-creation"></a>通訊端建立

事件識別碼 = 1

層級 = 4 (資訊) 

下列 Winsock 事件會針對通訊端建立進行追蹤：

-   由呼叫 [**通訊端**](/windows/desktop/api/Winsock2/nf-winsock2-socket) 或 [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) 函式所建立的通訊端控制碼。
-   已接受接聽通訊端的通訊端控制碼。
-   呼叫 [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) 函數所建立的通訊端控制碼。
-   呼叫 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 或 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) 函式時，會重複使用通訊端控制碼。

針對通訊端建立事件，會記錄下列參數：



| 參數                                                                                                        | Description                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                 | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>             | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | 通訊端的型別。<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>協定<br/>             | 通訊端的通訊協定。<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>UserModePid<br/> | 建立通訊端的使用者模式處理序識別碼。<br/>                           |



 

## <a name="socket-bind"></a>通訊端系結

事件識別碼 = 2 (IPv4) ，事件識別碼 = 3 (IPv6) 

層級 = 4 (資訊) 

以下是針對系結作業追蹤的 Winsock 事件：

-   通訊端控制碼的隱含或明確系結。

以下是針對系結事件記錄的參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>     | 本機 IP 位址。<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                 | 本機 IP 埠號碼。<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>地位<br/>         | 針對系結作業傳回的狀態或錯誤碼。<br/>                   |



 

## <a name="failed-bind"></a>失敗的系結

事件識別碼 = 40

層級 = 4 (資訊) 

針對失敗的系結作業，會追蹤下列 Winsock 事件：

-   失敗之通訊端控制碼的隱含或明確系結。

針對失敗的系結事件，會記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 失敗系結作業傳回的錯誤碼。<br/>                     |



 

## <a name="socket-connect"></a>通訊端連接

事件識別碼 = 4 (IPv4) ，事件識別碼 = 5 (IPv6) 

層級 = 4 (資訊) 

下列 Winsock 事件會針對 connect 作業要求進行追蹤， (對 [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)、 [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)、 [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)、 [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)或 [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) 函數的呼叫) ：

-   將通訊端連接至連接導向或不需連線的通訊端的目的地。

下列參數會針對 connect 事件進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>     | 遠端 IP 位址。<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                 | 遠端 IP 埠號碼。<br/>                                                  |



 

## <a name="connect-completed"></a>連接完成

事件識別碼 = 6

層級 = 4 (資訊) 

以下是針對 connect 完成追蹤的 Winsock 事件：

-   連接操作已完成。

已針對 connect completed 事件記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對連接作業傳回的錯誤碼。<br/>                          |



 

## <a name="afd-initiated-abort"></a>AFD-Initiated 中止

事件識別碼 = 7

層級 = 4 (資訊) 

下列 Winsock 事件會針對 Winsock 起始的中止或取消作業進行追蹤：

-   因為未讀取的接收資料在關閉後緩衝，所以會中止。
-   在呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown)函式之後中止，並 *將參數設定* 為 SD RECEIVE，以及對導致 closesocket 函式的 \_ 呼叫擱置的接收資料。 [](/windows/desktop/api/winsock/nf-winsock-closesocket)
-   在嘗試排清端點失敗之後中止。
-   發生內部 Winsock 錯誤之後，就會中止。
-   因為連接有錯誤，而應用程式先前要求在某些情況下中止連接，所以會中止。 這種情況的其中一個範例，就是將 timeout 設定為延遲的應用程式 \_ ，並在連線上仍有未認可的資料。
-   未完全與接受端點相關聯的連接上的中止。
-   在對 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) 或 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) 函式的呼叫失敗時中止。
-   因為接收作業失敗而中止。
-   由於隨插即用事件而中止。
-   因為排清要求失敗而中止。
-   因為快速的資料接收要求失敗而中止。
-   因為傳送要求失敗而中止。
-   因為取消的傳送要求而中止。
-   因為已取消呼叫 [**TransmitPackets**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) 函式而中止。

系統會針對 Winsock 起始的中止或取消作業記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因<br/>         | 中止或取消作業的原因。<br/>                               |



 

## <a name="transport-initiated-abort"></a>Transport-Initiated 中止

事件識別碼 = 8

層級 = 4 (資訊) 

下列 Winsock 事件會針對傳輸起始的中止或取消作業進行追蹤：

-   由傳輸指示的重設。

系統會針對 Winsock 起始的中止或取消作業記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因<br/>         | 中止或取消作業的原因。<br/>                               |



 

## <a name="failed-send-request"></a>傳送要求失敗

事件識別碼 = 9

層級 = 4 (資訊) 

針對 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 或 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 要求的錯誤，會追蹤下列 Winsock 事件：

-   失敗的 [**傳送**](/windows/desktop/api/Winsock2/nf-winsock2-send) 或 [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) 要求傳回的錯誤。

下列參數會針對產生錯誤的傳送要求進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對作業傳回的錯誤碼。<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>失敗的 WsaSendMsg 要求

事件識別碼 = 10

層級 = 4 (資訊) 

針對 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 要求的錯誤，會追蹤下列 Winsock 事件：

-   失敗的 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 要求傳回的錯誤。

下列參數會針對產生錯誤的傳送要求進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對作業傳回的錯誤碼。<br/>                                  |



 

## <a name="failed-recv-request"></a>失敗的接收要求

事件識別碼 = 11

層級 = 4 (資訊) 

針對 [**接收**](/windows/desktop/api/winsock/nf-winsock-recv)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)或 [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) 要求的錯誤，會追蹤下列 Winsock 事件：

-   失敗的接收要求傳回的錯誤。

下列參數會針對產生錯誤的傳送要求進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對作業傳回的錯誤碼。<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>失敗的 Recvfrom 要求

事件識別碼 = 12

層級 = 4 (資訊) 

針對 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求的錯誤，會追蹤下列 Winsock 事件：

-   失敗的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求傳回的錯誤。

系統會針對導致錯誤的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 或 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) 要求記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對作業傳回的錯誤碼。<br/>                                  |



 

## <a name="socket-close"></a>通訊端關閉

事件識別碼 = 13

層級 = 4 (資訊) 

以下是針對通訊端關閉作業追蹤的 Winsock 事件：

-   通訊端控制碼已關閉。

通訊端關閉事件會記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 通訊端關閉作業的傳回值。<br/>                            |



 

## <a name="socket-cleanup"></a>通訊端清除

事件識別碼 = 14

層級 = 4 (資訊) 

下列 Winsock 事件會針對通訊端清除 (關機) 作業進行追蹤：

-   在通訊端上呼叫 [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) 函數。
-   傳輸表示失敗的正常中斷連線。

下列參數會針對通訊端清除 (關機) 或通訊端關閉事件進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 通訊端清除 (關閉) 作業的傳回值。<br/>               |



 

## <a name="socket-accept"></a>通訊端接受

事件識別碼 = 15 (IPv4) ，事件識別碼 = 16 (IPv6) 

層級 = 4 (資訊) 

針對 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數要求，會追蹤下列 Winsock 事件：

-   在通訊端控制碼上的 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 函數要求。

下列參數會針對 accept 事件進行記錄：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>     | 遠端 IP 位址。<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                 | 遠端 IP 埠號碼。<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>地位<br/>         | 針對接受操作傳回的狀態或錯誤碼。<br/>                 |



 

## <a name="accept-failed"></a>接受失敗

事件識別碼 = 17

層級 = 4 (資訊) 

針對失敗的接受作業，會追蹤下列 Winsock 事件：

-   通訊端控制碼上的 [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)、 [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex)或 [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) 要求失敗。

針對失敗的接受事件，會記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對失敗的接受作業傳回的錯誤碼。<br/>                   |



 

## <a name="send-posted"></a>傳送已張貼

事件識別碼 = 18

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端傳送和接收緩衝區 post 作業，會追蹤下列 Winsock 事件：

-   應用程式張貼傳送。
-   傳送作業完成至 Winsock。

針對通訊端傳送作業，會記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | 布林值，指出是否使用快速路徑 i/o。<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 緩衝區的長度。 針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。<br/>  |



 

當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。 當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。

## <a name="receive-posted"></a>已張貼接收

事件識別碼 = 19

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端接收緩衝區 post 作業，會追蹤下列 Winsock 事件：

-   應用程式張貼接收。
-   接收作業會完成至 Winsock。

針對通訊端接收作業，會記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | 布林值，指出是否使用快速路徑 i/o。<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 緩衝區的長度。 針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。<br/>  |



 

當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。 當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。

## <a name="recvfrom-posted"></a>張貼的 RecvFrom

事件識別碼 = 20

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端上的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 緩衝區 post 作業，會追蹤下列 Winsock 事件：

-   應用程式會從作業張貼接收。

Recvfrom 作業會記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | 布林值，指出是否使用快速路徑 i/o。<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 緩衝區的長度。 針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。<br/>  |



 

當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。 當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。

## <a name="sendto-posted"></a>SendTo 張貼

事件識別碼 = 21 (IPv4) ，事件識別碼 = 22 (IPv6) 

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端上的 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 緩衝區 post 作業，會追蹤下列 Winsock 事件：

-   應用程式張貼傳送的來源。

針對 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 作業記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | 布林值，指出是否使用快速路徑 i/o。<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 緩衝區的長度。 針對連結的緩衝區，此參數是鏈中所有緩衝區的總位元組數。<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>                     | 通訊端的遠端 IP 位址。<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                                 | 通訊端的遠端 IP 埠號碼。<br/>                                                                                        |



 

當 FastPath 為 true 時，緩衝區陣列中第一個緩衝區的 usermode 位址會記錄在緩衝區參數中。 當 FastPath 為 false 時，會在緩衝區參數中記錄 Winsock 核心緩衝區位址。

## <a name="recv-completed"></a>已完成接收

事件識別碼 = 23

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端接收完成的作業，會追蹤下列 Winsock 事件：

-   傳送作業會完成傳輸。
-   接收作業會完成傳輸。

系統會針對傳送完成或接收完成記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 收到的位元組緩衝區長度。 針對連結的緩衝區，此參數是在鏈中的所有緩衝區內接收的位元組總數。<br/> |



 

## <a name="send-completed"></a>傳送完成

事件識別碼 = 24

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 針對通訊端傳送完成的作業，會追蹤下列 Winsock 事件：

-   傳送作業會完成傳輸。

系統會針對傳送完成記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 傳送位元組緩衝區的長度。 針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。<br/> |



 

## <a name="sendmsg-completed"></a>SendMsg 已完成

事件識別碼 = 25

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 當通訊端上的 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 緩衝區 post 操作完成時，會追蹤下列 Winsock 事件：

-   應用程式完成 [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) 作業。

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)完成時會記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 傳送位元組緩衝區的長度。 針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>                     | 通訊端的遠端 IP 位址。<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                                 | 通訊端的遠端 IP 埠號碼。<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>RecvFrom 已完成

事件識別碼 = 26 (IPv4) ，事件識別碼 = 27 (IPv6) 

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 當通訊端上的 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 緩衝區 post 操作完成時，會追蹤下列 Winsock 事件：

-   應用程式完成 [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) 作業。

[**Recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom)完成時會記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 收到的位元組緩衝區長度。 針對連結的緩衝區，此參數是在鏈中的所有緩衝區內接收的位元組總數。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>                     | 通訊端的遠端 IP 位址。<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                                 | 通訊端的遠端 IP 埠號碼。<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>SendTo 已完成

事件識別碼 = 28

層級 = 5 (詳細資訊) 

為了診斷使用者緩衝區損毀 (例如，當應用程式在另一個傳送或接收呼叫中重複使用相同的緩衝區時，當它仍在使用) 時，會在張貼到 Winsock 時記錄資料緩衝區，並在基礎傳輸完成時記錄資料緩衝區。 在通訊端上完成 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 緩衝區 post 作業時，會追蹤下列 Winsock 事件：

-   應用程式完成 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 操作。

針對 [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) 完成記錄下列參數：



| 參數                                                                                                            | Description                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                     | 進程的核心 EPROCESS 結構位址。<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                 | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | 緩衝區計數。<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>緩衝區<br/>                         | 緩衝區的虛擬位址。 針對連結的緩衝區，此參數是鏈中第一個緩衝區的虛擬位址。<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>BufferLength<br/> | 傳送位元組緩衝區的長度。 針對連結的緩衝區，此參數是從鏈中的所有緩衝區傳送的位元組總數。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>                     | 通訊端的遠端 IP 位址。<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                                 | 通訊端的遠端 IP 埠號碼。<br/>                                                                                           |



 

## <a name="socket-option-set"></a>通訊端選項群組

事件識別碼 = 29

層級 = 5 (詳細資訊) 

每當應用程式變更特定通訊端選項值和 Ioctls 時，就會記錄新的值。 記錄的選項可以用來診斷應用程式中的效能不佳或奇怪的行為。 下列 Winsock 事件會針對某些通訊端選項和 Ioctls 進行追蹤：

-   \_SNDBUF 變更。
-   \_RCVBUF 變更。
-   FIONBIO
-   SIO \_ 啟用 \_ 迴圈 \_ 佇列
-   SIO \_ UDP \_ CONNRESET
-   \_OOBINLINE

針對會變更上述任何值的 [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 和 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式呼叫，會記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>選項<br/>         | 已變更的通訊端選項或 Ioctl。 <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值<br/>             | 通訊端選項或 Ioctl 的新值。 <br/>                              |



 

## <a name="selectpoll-posted"></a>選取/輪詢已張貼

事件識別碼 = 30

層級 = 5 (詳細資訊) 

當應用程式呼叫 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式時，會追蹤下列 Winsock 事件：

-   應用程式張貼 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 要求。

針對 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 事件記錄下列參數：



| 參數                                                                                                        | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                 | 擁有的處理序識別碼。<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | 應用程式所傳入的控制碼數目 (只有在起始事件) 上才有效。<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>超時<br/>                 | [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select)或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)函數等候的最長時間。<br/> |



 

## <a name="selectpoll-completed"></a>選取/輪詢已完成

事件識別碼 = 31

層級 = 5 (詳細資訊) 

當應用程式呼叫 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 函式時，會追蹤下列 Winsock 事件：

-   Winsock 完成 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 呼叫。

當 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 操作完成時，會記錄下列參數：



| 參數                                                                                            | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>錯誤<br/>             | 針對 [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) 或 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 作業傳回的錯誤碼。<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

事件識別碼 = 32

層級 = 5 (詳細資訊) 

當應用程式呼叫 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式時，會追蹤下列 Winsock 事件：

-   記錄在 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式中傳遞的事件遮罩。

[**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect)函式呼叫會記錄下列參數：



| 參數                                                                                                | Description                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>         | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>     | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | 事件遮罩的值。 <br/>                                              |



 

## <a name="dropped-datagram"></a>丟棄的資料包

事件識別碼 = 33 (IPv4) ，事件識別碼 = 34 (IPv6) 

層級 = 5 (詳細資訊) 

為了協助診斷資料包應用程式周圍的問題，會追蹤下列 Winsock 事件：

-   當資料包送出，而它被捨棄時，沒有足夠的緩衝區空間。
-   在連接的資料包中，如果資料從連接的目的地以外的來源進行。

已針對捨棄的資料包記錄下列參數：



| 參數                                                                                                    | Description                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>             | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>         | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize<br/> | 丟棄的封包大小。 <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>             | 封包來源的 IP 位址。 <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                         | 封包來源的 IP 埠號碼。<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>原因<br/>                 | 丟棄封包的錯誤碼或原因。<br/>                            |



 

## <a name="connection-indicated"></a>指出的連接

事件識別碼 = 35 (IPv4) ，事件識別碼 = 36 (IPv6) 

層級 = 5 (詳細資訊) 

針對連接指出的作業，會追蹤下列 Winsock 事件：

-   應用程式會收到連接要求。

系統會針對從傳輸事件指出的連接記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>     | 遠端 IP 位址。 <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                 | 遠端 IP 埠號碼。<br/>                                                  |



 

## <a name="data-indicated"></a>指出的資料

事件識別碼 = 37

層級 = 5 (詳細資訊) 

針對資料指出的作業，會追蹤下列 Winsock 事件：

-   應用程式會接收連接的通訊端上的資料。

系統會針對從傳輸事件指出的資料記錄下列參數：



| 參數                                                                                                                        | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                                 | 擁有的處理序識別碼。<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                             | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>指出的位元組<br/> | 在通訊端上收到的位元組數目。<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>從傳輸指出的資料

事件識別碼 = 38 (IPv4) ，事件識別碼 = 39 (IPv6) 

層級 = 5 (詳細資訊) 

針對傳輸作業所指出的資料，會追蹤下列 Winsock 事件：

-   應用程式會張貼接收要求並接收資料。

系統會針對從傳輸事件指出的資料記錄下列參數：



| 參數                                                                                                                        | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>                                 | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/>                             | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>位址<br/>                                 | 遠端 IP 位址。 <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>港口<br/>                                             | 遠端 IP 埠號碼。<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>指出的位元組<br/> | 在通訊端上收到的位元組數目。<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>從傳輸指出中斷連線

事件識別碼 = 41

層級 = 5 (詳細資訊) 

針對中斷連接指出的作業，會追蹤下列 Winsock 事件：

-   應用程式會收到中斷連接指示。

從傳輸事件指出的中斷連接會記錄下列參數：



| 參數                                                                                            | Description                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>過程<br/>     | 進程的核心 EPROCESS 結構位址。<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>端點<br/> | 當做通訊端唯一識別碼使用的 Winsock 核心通訊端位址。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Winsock 追蹤層級](winsock-tracing-levels.md)
</dt> </dl>

 

 
