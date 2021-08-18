---
description: 本節列出服務提供者可能會在 Windows 通訊端用戶端中進行的 upcalls。
ms.assetid: a2069814-de95-40a2-ab09-c5187ecd56a7
title: Windows 通訊端 2 DLL 公開的 Upcalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1361a8cb7a453ecb0f6aed0f4b71f65e27fce928d147a15152fab5fa5bcd9942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993198"
---
# <a name="upcalls-exposed-by-windows-sockets-2-dll"></a>Windows 通訊端 2 DLL 公開的 Upcalls

本節列出服務提供者可能會在 Windows 通訊端用戶端中進行的 upcalls。 服務提供者會以 [**WSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-wspstartup) 函式的參數形式接收 upcall 分派資料表，並使用此資料表中的專案來進行 upcalls。 因此，用戶端不需要匯出其 WPU 函式。

提供者不一定要使用這些 upcalls。 下表指出必須使用哪些 upcalls，哪些是選擇性的。

| 函式                                                               | 描述                                                                                                              | 狀態                         | 意義                                                                                                                                                                          |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WPUCloseEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucloseevent)                               | 關閉開啟的事件物件控制碼。                                                                                      | 選擇性。                      | 提供者可能會改為使用適當的 Windows 呼叫。                                                                                                                     |
| [**WPUCloseSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosesockethandle)                 | 關閉 Windows 通訊端 DLL 所配置的通訊端控制碼。                                                             | 必要。                      | Ws2 \_32.dll 需要查詢及/或修改與 socket 控制碼相關聯的內部狀態資訊。                                                                       |
| [**WPUCloseThread**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuclosethread)                             | 關閉內部服務執行緒的執行緒識別碼。                                                                       |                                |                                                                                                                                                                                  |
| [**WPUCompleteOverlappedRequest**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucompleteoverlappedrequest) | 提供重迭的 i/o 完成通知，其中完成機制是使用者模式 APC 以外的其他作業。    |                                |                                                                                                                                                                                  |
| [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent)                             | 建立新的事件物件。                                                                                              | 選擇性。                      | 提供者可能會改為使用適當的 Windows 呼叫。                                                                                                                        |
| [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle)               | 為 nonIFS 提供者建立新的通訊端控制碼。                                                                        | NonIFS 提供者所需。 | Ws2 \_32.dll 需要查詢及/或修改與 socket 控制碼相關聯的內部狀態資訊。                                                                       |
| [**WPUFDIsSet**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpufdisset)                                     | 檢查指定之通訊端控制碼的成員資格。                                                                    | 選擇性。                      | 這只是一個便利的函式，它知道如何透過 [**fd \_ 設定**](/windows/desktop/api/winsock/nf-winsock-fd_set) 結構來深入探討。 提供者可能必須明確地深入探討這些結構。 |
| [**WPUGetProviderPath**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpugetproviderpath)                     | 抓取所指定提供者的 DLL 路徑。                                                                       | 必要。                      | 只有 Ws2 \_32.dll 知道連續的通訊協定層 (可能來自另一個廠商) 的已安裝。                                                           |
| [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle)                     | 從 Windows 通訊端 DLL 接收 (可能) 修改過的 IFS 控制碼。                                                  | IFS 提供者的必要參數。    | Ws2 \_32.dll 需要查詢及/或修改與 socket 控制碼相關聯的內部狀態資訊。                                                                       |
| [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage)                             | 以維護回溯相容性的方式執行標準 [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) 函式。 | 必要。                      | Windows 2000 和 Windows NT。 Windows 95 允許來自核心模式的 post 訊息。                                                                                               |
| [**WPUQueryBlockingCallback**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueryblockingcallback)         | 傳回執行緒封鎖攔截函式的指標。                                                                  | 必要。                      | 沒有對應的 Windows 功能。 只有 Ws2 \_32.dll 具有完成此動作的資訊。                                                                    |
| [**WPUQuerySocketHandleCoNtext**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuquerysockethandlecontext)   | 取得通訊端的內容值， (只) 的 nonIFS 提供者。                                                                   | NonIFS 提供者所需。 | Ws2 \_32.dll 需要查詢及/或修改與 socket 控制碼相關聯的內部狀態資訊。                                                                       |
| [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)                                   | 將使用者模式的 APC 佇列排入指定的執行緒。                                                                          | 選擇性。                      | 也可以使用 [**QueueUserApc**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-queueuserapc) 。                                                                                                                      |
| [**WPUResetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuresetevent)                               | 重設事件物件。                                                                                                  | 選擇性。                      | 提供者可能會改為使用適當的 Windows 呼叫。                                                                                                                        |
| [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent)                                   | 設定事件物件。                                                                                                    | 選擇性。                      | 提供者可能會改為使用適當的 Windows 呼叫。                                                                                                                        |



 

 

 
