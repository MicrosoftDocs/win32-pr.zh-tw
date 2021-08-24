---
title: 藍牙並連接
description: 藍牙使用 connect 函式連接到目標藍牙裝置，並使用先前建立的藍牙通訊端。
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- 藍牙藍牙
- 連接藍牙
- 藍牙並連接藍牙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588458"
---
# <a name="bluetooth-and-connect"></a>藍牙並連接

藍牙使用 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函式連接到目標藍牙裝置，並使用先前建立的藍牙通訊端。 **Connect** 函式的 *name* 參數，也就是 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構，必須指定目標藍牙裝置。 使用兩種機制來識別目標裝置：

-   [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構可以直接指定要求連接的埠號碼。 這種機制要求應用程式在嘗試 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 作業之前，先執行自己的 SDP 查詢。
-   [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構可以指定要連接之服務的唯一服務類別識別碼。 如果對等裝置有一個以上的埠對應至服務類別識別碼，則 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函式呼叫會連接到第一個有效的服務。 在沒有先前的 SDP 查詢的情況下，可以使用此機制。

搭配 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函式使用 [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)結構時，適用下列需求：

-   **BtAddr** 成員必須是有效的遠端無線電位址。
-   針對 **serviceClassId** 成員，如果埠成員為零，系統會嘗試使用 **serviceClassId** 來解析對應至服務的遠端埠。 服務類別是標準化的128位 GUID （由藍牙規格所定義）。 一般 Guid 是由藍牙指派的數位檔所定義。 或者，您也可以針對特定領域的應用程式使用唯一的 GUID。
-   **埠** 成員必須是有效的遠端埠，如果指定了 **serviceClassId** 成員，則為零。

下表列出藍牙和 [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)函數的結果碼。

| 錯誤/錯誤\#                    | 描述                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | 針對已連接的通訊端呼叫的 [**連接**](/windows/desktop/api/winsock2/nf-winsock2-connect) 函數。 |
| WSAEACCES10013<br/>        | 連接應用程式要求的驗證，但驗證失敗。        |
| WSAENOBUFS10055<br/>       | 無法復原的記憶體不足錯誤。                                                 |
| WSAEADDRINUSE10048<br/>    | 要求的埠/頻道號碼正在使用中。                                       |
| WSAETIMEDOUT10060<br/>     | I/o 會在藍牙的無線電層級超時， (頁面 \_ 超時) 。                    |
| WSAEDISCON10101<br/>       | 遠端對等互連的 RFCOMM 通道已中斷連線。                                    |
| WSAECONNRESET10054<br/>    | RFCOMM 多重傳送器 (會話) 由遠端對等互連中斷連線。                      |
| WSAECONNABORTED10053<br/>  | 應用程式關閉通訊端。                                                   |
| WSAENETUNREACH10051<br/>   | L2CAP 或藍牙的收音機層級以外的錯誤。                       |
| WSAEHOSTDOWN10064<br/>     | RFCOMM 收到 DM 回應。                                                   |
| WSAENETDOWN10050<br/>      | 未預期的網路錯誤。                                                          |
| WSAESHUTDOWN10058<br/>     | 遠端對等互連的 L2CAP 通道已中斷連線。                                     |
| WSAEADDRNOTAVAIL10049<br/> | 藍牙埠/通道或裝置位址無效。                                |
| WSAEINVAL10022<br/>        | 隨插即用、驅動程式堆疊事件或其他錯誤導致失敗。                  |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**連線**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

