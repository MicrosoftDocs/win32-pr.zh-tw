---
description: 下表摘要說明 Windows 通訊端2的部分通訊端 IOCTL opcode。
ms.assetid: fb6447b4-28f5-4ab7-bbdc-5a57ed38a994
title: 通訊端 Ioctl opcode 的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f0d6163e4ef36598dad56dd4d81201bdda3c2a3b1bb0473a0ef9ffb4675b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118559658"
---
# <a name="summary-of-socket-ioctl-opcodes"></a>通訊端 Ioctl opcode 的摘要

下表摘要說明 Windows 通訊端2的部分通訊端 IOCTL opcode。 如需更詳細的資訊，請參閱 [**Winsock IOCTLs**](winsock-ioctls.md) 和 [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) 函數的 winsock 參考。 另外還有其他通訊協定專屬的 IOCTL opcode，可在特定通訊協定的附錄中找到。

Winsock 參考中提供完整的 [**Winsock IOCTLs**](winsock-ioctls.md) 清單。



| OpCode                                                      | 輸入類型                               | 輸出類型                                 | 意義                                                                                                                                                                                                            |
|-------------------------------------------------------------|------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FIONBIO                                                     | 不帶正負號的 long                            | <Not used>                            | 啟用或停用通訊端上的非封鎖模式。                                                                                                                                                                |
| FIONREAD                                                    | <Not used>                         | 不帶正負號的 long                               | 決定可從通訊端以不可部分完成的方式讀取的資料量。                                                                                                                                         |
| SIOCATMARK                                                  | <Not used>                         | BOOL                                        | 判斷是否已讀取所有 OOB 資料。                                                                                                                                                              |
| SIO \_ 關聯 \_ 控制碼                                      | 附屬 API 相依                  | <Not used>                            | 建立通訊端與指定的隨附介面控制碼之間的關聯。                                                                                                                                          |
| SIO \_ 啟用 \_ 迴圈 \_ 佇列                             | <Not used>                         | <Not used>                            | 啟用迴圈佇列。                                                                                                                                                                                          |
| SIO \_ 尋找 \_ 路線                                            | [**sockaddr**](sockaddr-2.md) 結構 | <Not used>                            | 要求要探索到指定位址的路由。                                                                                                                                                      |
| SIO \_ FLUSH                                                  | <Not used>                         | <Not used>                            | 捨棄傳送佇列的目前內容。                                                                                                                                                                    |
| SIO \_ 取得 \_ 廣播 \_ 位址                                | <Not used>                         | [**sockaddr**](sockaddr-2.md) 結構    | 抓取要在 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))中使用的通訊協定特定廣播位址。                                                                                                                  |
| SIO \_ 取得 \_ QOS                                               | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | 抓取通訊端目前的流程規格。                                                                                                                                                              |
| SIO \_ 取得 \_ 群組 \_ QOS                                        | <Not used>                         | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                          | 保留的。                                                                                                                                                                                                          |
| SIO \_ MULTIPOINT \_ 回送                                   | BOOL                                     | <Not used>                            | 控制是否也會由本機主機上的相同通訊端接收 multipoint 會話中傳送的資料。                                                                                                     |
| SIO \_ 多播 \_ 領域                                       | int                                      | <Not used>                            | 指定將進行多播傳輸的範圍。                                                                                                                                                 |
| SIO \_ 設定 \_ QOS                                               | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | 為通訊端建立新的流程規格。                                                                                                                                                                |
| SIO \_ 設定 \_ 群組 \_ QOS                                        | [**Qos**](/windows/win32/api/winsock2/ns-winsock2-qos)                       | <Not used>                            | 保留的。                                                                                                                                                                                                          |
| SIO \_ 轉譯 \_ 控制碼                                      | int                                      | 附屬-API 相依                     | 取得通訊端 *s* 的對應控制碼，該控制碼在隨附介面的內容中有效。                                                                                                               |
| SIO \_ 路由 \_ 介面 \_ 查詢                              | [**sockaddr**](sockaddr-2.md)           | [**sockaddr**](sockaddr-2.md)              | 取得應用來傳送至指定位址的本機介面位址。                                                                                                                   |
| SIO \_ 路由 \_ 介面 \_ 變更                             | [**sockaddr**](sockaddr-2.md)           | <Not used>                            | 針對指定的位址，要求透過 SIO \_ 路由 \_ 介面查詢回報的資訊變更通知 \_ 。                                                                                         |
| [**SIO \_ 位址 \_ 清單 \_ 查詢**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) | <Not used>                         | [**通訊端 \_ 位址**](/windows/desktop/api/Ws2def/ns-ws2def-socket_address) | 取得應用程式可系結之通訊端通訊協定系列的本機傳輸地址清單。 地址清單會根據地址系列而有所不同，而某些位址會從清單中排除。 |
| SIO \_ 位址 \_ 清單 \_ 變更                                  | <Not used>                         | <Not used>                            | 要求透過 SIO \_ 位址 \_ 清單 \_ 查詢回報的資訊變更通知                                                                                                                         |
| SIO \_ 查詢 \_ PNP \_ 目標 \_ 控制碼                             | <Not used>                         | 插座                                      | 取得目前通訊端相依于 PnP 的鏈中，下一個提供者的通訊端描述項。                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> <dt>

[**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))
</dt> </dl>

 

 
