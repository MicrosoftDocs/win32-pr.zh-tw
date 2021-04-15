---
description: Ws2spi 所公開的資料傳輸函數。
ms.assetid: 6900faa3-79bb-4ed8-b83e-148eb10425a0
title: 一般資料傳輸函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63de41b90148210ea8a99d5271b62c5d8bc0c08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511444"
---
# <a name="generic-data-transport-functions"></a>一般資料傳輸函數

此區段會列出 Ws2spi 所公開的資料傳輸函數。



| 函式                                                   | 描述                                                                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)                           | 系統會確認連入連線，並與立即建立的通訊端建立關聯。 原始通訊端會回到接聽狀態。 此函數也允許接受條件式接受。 |
| [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))                 | 執行 [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))的非同步版本。                                                                                                                                      |
| [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))                               | 將本機名稱指派給未命名的通訊端。                                                                                                                                                              |
| [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85))   | 取消未完成的封鎖 Windows 通訊端呼叫。                                                                                                                                                   |
| [**WSPCleanup**](/previous-versions/windows/hardware/network/ff566270(v=vs.85))                         | 登出基礎 Windows 通訊端服務提供者。                                                                                                                                         |
| [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                 | 從每個處理常式的物件參考資料表中移除通訊端。 只有在 \_ 封鎖通訊端上設定了非零超時時，才會封鎖。                                                            |
| [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))                         | 初始化指定之通訊端上的連接。 此函式也允許 exchange connect 資料和 QoS 規格。                                                                           |
| [**WSPDuplicateSocket**](/previous-versions/windows/hardware/network/ff566282(v=vs.85))         | 傳回 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構，可用來為共用通訊端建立新的通訊端描述項。                                                             |
| [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85))     | 探索網路事件的出現次數。                                                                                                                                                                |
| [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))                 | 將網路事件與事件物件產生關聯。                                                                                                                                                         |
| [**WSPGetOverlappedResult**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetoverlappedresult) | 取得重迭運算的完成狀態。                                                                                                                                                         |
| [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85))                 | 抓取連接到指定之通訊端的對等名稱。                                                                                                                                       |
| [**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85))                 | 抓取指定之通訊端所系結的本機位址。                                                                                                                                     |
| [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))                   | 抓取與指定之通訊端相關聯的選項。                                                                                                                                                 |
| [**WSPGetQOSByName**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspgetqosbyname)               | 根據已知的服務名稱提供 QoS 參數。                                                                                                                                             |
| [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))                             | 提供通訊端的控制權。                                                                                                                                                                           |
| [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf)                       | 將分葉節點加入 multipoint 會話。                                                                                                                                                            |
| [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))                           | 接聽指定之通訊端上的傳入連接。                                                                                                                                                 |
| [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))                               | 從連線或未連接的通訊端接收資料。 此函式會容納散佈/收集 i/o、重迭通訊端，並將旗標參數提供為 IN/OUT。                                    |
| [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85))           | 在通訊端上終止接收，如果通訊端為連線導向，則會取出中斷連接資料。                                                                                                |
| [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))                       | 從已連接或未連接的通訊端接收資料。 此函式會容納散佈/收集 i/o、重迭的通訊端，並將旗標參數提供為 IN/OUT。                              |
| [**WSPSelect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))                           | 執行同步的 i/o 多工。                                                                                                                                                                  |
| [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))                               | 將資料傳送到已連線的通訊端。 此函式也會容納散佈/收集 i/o 和重迭通訊端。                                                                                            |
| [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85))           | 起始通訊端連線終止，並選擇性地傳送中斷連接資料。                                                                                                                       |
| [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))                           | 將資料傳送至已連線或未連接的通訊端。 此函式也會容納散佈/收集 i/o 和重迭通訊端。                                                                      |
| [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85))                   | 儲存與指定之通訊端相關聯的選項。                                                                                                                                                    |
| [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85))                       | 關閉全雙工連接的一部分。                                                                                                                                                            |
| [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)                           | 通訊端建立函式，它會採用 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構作為輸入，並允許建立重迭的通訊端。                                                |
| [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup)                         | 初始化基礎 Windows 通訊端服務提供者。                                                                                                                                            |



 

 

 
