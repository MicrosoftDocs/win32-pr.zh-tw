---
description: 有幾個選項可用來接收完成指示，因此提供應用程式適當的彈性層級。 這些包括：等候 (或封鎖事件物件、輪詢事件物件和通訊端 i/o 完成常式的) 。
ms.assetid: 071cf198-6b4c-445e-9bd9-044f57f994a3
title: 接收完成指示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0ea3d46707eb31d803362f327c309d3c9d948812c0eb3a810e31b896e895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569248"
---
# <a name="receiving-completion-indications"></a>接收完成指示

有幾個選項可用來接收完成指示，因此提供應用程式適當的彈性層級。 這些包括：等候 (或封鎖事件物件、輪詢事件物件和通訊端 i/o 完成常式的) 。

## <a name="blocking-and-waiting-for-completion-indication"></a>封鎖並等候完成指示

應用程式可以在等候一個或多個事件物件變成使用 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 函式設定時封鎖。 在 Windows 的執行中，進程或執行緒真正會封鎖。 由於 Windows 通訊端2事件物件會實作為 Windows 事件，因此原生 Windows 函數 [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects)也可用於此用途。 如果執行緒需要等待通訊端和 nonsocket 事件，這會特別有用。

## <a name="polling-for-completion-indication"></a>輪詢完成指示

偏好不封鎖的應用程式可以使用 [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) 函數來輪詢與任何特定事件物件相關聯的完成狀態。 此函式指出重迭的作業是否已完成，如果已完成，則會排列 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) 函式，以取得重迭作業的錯誤狀態。

## <a name="using-socket-io-completion-routines"></a>使用通訊端 i/o 完成常式

用來起始重迭 i/o 的函式 ( [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)、 [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)、 [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)、 [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)) 全部採用 *lpCompletionRoutine* 做為選擇性的輸入參數。 這是應用程式特定函式的指標，該函式會在成功起始重迭的 i/o 作業完成 (成功或) 的情況下呼叫。 完成常式會遵循 Windows 檔案 i/o 完成常式的約定相同規則。 也就是說，線上程處於可提供警示等候狀態之前，不會叫用完成常式，例如，使用旗標設定叫用函數 [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) 時 `fAlertable` 。 針對特定重迭 i/o 要求使用完成常式選項的應用程式，可能不會針對相同的重迭 i/o 要求使用 [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) 的 wait 選項。

傳輸可讓應用程式從通訊端 i/o 完成常式的內容中叫用傳送和接收作業，並保證指定的通訊端、i/o 完成常式不會進行嵌套。 這可讓時間緊迫的資料傳輸完全在先占式內容中發生。

## <a name="summary-of-overlapped-completion-indication-mechanisms"></a>重迭完成指示機制的摘要

指定重迭作業所要使用的特定重迭 i/o 完成指示，取決於應用程式是否提供完成函式的指標、是否參考 [**WSAOVERLAPPED**](/windows/desktop/api/Winsock2/ns-winsock2-wsaoverlapped)結構，以及 **WSAOVERLAPPED** 結構內 **hEvent** 成員的值（如果有提供的話） (（如果有提供) ）。 下表摘要說明重迭通訊端的完成語義，並顯示 *lpOverlapped*、 **hEvent** 和 *lpCompletionRoutine* 的各種組合：

| *lpOverlapped* | hEvent         | *lpCompletionRoutine* | 完成指示                                                                                                                                                                                                    |
|----------------|----------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | 不適用 | 忽略               | 作業以同步方式完成。 它的行為就像是 nonoverlapped 通訊端一樣。                                                                                                                                      |
| !空          | NULL           | NULL                  | 作業已完成重迭，但沒有 Windows 通訊端2支援的完成機制。 完成埠機制 (是否可在此情況下使用支援的) 。 否則，就不會有完成通知。 |
| !空          | !空          | NULL                  | 作業完成重迭，由訊號事件物件發出通知。                                                                                                                                                  |
| !空          | 忽略        | !空                 | 作業完成重迭，藉由排程完成常式來通知。                                                                                                                                           |



 

 

 
