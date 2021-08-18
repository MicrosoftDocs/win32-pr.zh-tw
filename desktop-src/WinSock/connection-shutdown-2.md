---
description: 以下說明用來關閉已建立之通訊端連接的作業事件。
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: 連接關閉
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbd26716c255c83a8ecc17305d9e59676645739a6f90d18ac72b5bcda49241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898418"
---
# <a name="connection-shutdown"></a>連接關閉

以下說明用來關閉已建立之通訊端連接的作業事件。

## <a name="initiating-shutdown-sequence"></a>起始關機順序

您可以使用數種方式之一來關閉通訊端連線。 [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) *(具有等於* sd \_ SEND 或 Sd 的 \_) ，而 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) 可用來起始正常的連接關閉。 [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) 可以用來起始正常或 abortive 關機，視關閉通訊端所叫用的延遲選項而定。 請參閱下面的詳細資訊，以取得正常和 abortive 關機的詳細資訊，以及延遲選項。

## <a name="indicating-remote-shutdown"></a>指出遠端關機

服務提供者表示透過 FD CLOSE network 事件由遠端方起始的連線清除 \_ 。 當位元組串流通訊協定的讀取位元組數為0，或透過訊息導向通訊協定的 WSAEDISCON 傳回錯誤碼時，也會透過 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 來指出正常關機。 在任何情況下， **WSPRecv** 傳回錯誤碼 WSAECONNRESET 表示 abortive 關閉。

## <a name="exchanging-user-data-at-shutdown-time"></a>在關機時交換使用者資料

在連線終止時，支援此) 的通訊協定也可能 (，以便在端點之間交換使用者資料。 起始清除的結束可以呼叫 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) ，表示不會再傳送任何資料，並且會起始連接清除順序。 針對特定的通訊協定，此卸載順序的一部分是從終止啟動器傳送中斷連接的資料。 收到通知後，遠端端點已起始終止順序 (通常透過 FD \_ 關閉指示) ， [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) 函式可能會被呼叫，以接收中斷連接資料 (如果有任何) 。

若要說明如何使用中斷連線資料，請考慮下列案例。 用戶端/伺服器應用程式的用戶端一半負責終止通訊端連接。 與其終止一致，它會透過中斷連接資料來提供 (，) 它與伺服器處理的交易總數。 然後伺服器會以其使用所有用戶端處理的交易累計總計來回應。 呼叫和指示的順序可能會如下表所示。

| 用戶端                                                                                                               | 伺服器端                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
|  (1) 叫用 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) 以結束會話並提供交易總計。            |                                                                                                                                         |
|                                                                                                                           |  (2) 取得 FD \_ CLOSE 或 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) ，其傳回值為零或 WSAEDISCON，表示正常關機正在進行中。 |
|                                                                                                                           |  (3) 叫用 [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) 以取得用戶端的交易總計。                                         |
|                                                                                                                           |  (4) 計算所有交易的累積總計。                                                                                |
|                                                                                                                           |  (5) 叫用 [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) 來傳輸總計。                                                   |
|  (6) 收到 FD \_ 關閉指示。                                                                                        |  (5 ' ) 叫用 [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
|  (7) 叫用 [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) 來接收和儲存累積的交易總計。 |                                                                                                                                         |
|                                                                                                                           |  (8) 叫用 [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

步驟 (5 ' ) 必須遵循步驟 (5) ，但與步驟 (6) 、 (7) 或 (8) 之間沒有時間關聯性。

 

 
