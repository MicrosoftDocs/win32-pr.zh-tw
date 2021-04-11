---
title: IPaperSink 方法
description: COPaper 會公開 IConnectionPointContainer 介面，讓用戶端可以連線到 COPaper，以便接收 COPaper 中所發生之指定事件的通知。
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104186056"
---
# <a name="ipapersink-methods"></a>IPaperSink 方法

COPaper 會公開 [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) 介面，讓用戶端可以連線到 COPaper，以便接收 COPaper 中所發生之指定事件的通知。 藉由公開這個介面，COPaper 會變成可連接的物件。 用戶端可以呼叫這個介面的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，並用它來取得物件的連接點。 相關聯的 **StoClien** 範例涵蓋了此配置的用戶端參與。

基本上，用戶端會使用接收介面，以接收物件的形式來實作為接收器。 當用戶端將接收端正確連接到 COPaper 實例之後，接收介面會接收來自 COPaper 的傳出事件通知呼叫。 用戶端會使用由 COPaper 管理的連接點物件來進行連接。 單一可連接的 COM 物件上可以有多個連接點。 在 **StoServe** 範例中，COPaper 只有一個連接點，它會處理繪圖的紙事件。

任何數目的用戶端都可以連接到單一連接點。 \_COPaper 中的 CONNPOINT PAPERSINK 連接點會維護一組可在執行時間動態成長的連接。 COPaper 可連線物件支援的完整詳細資料，是以檔案連接來撰寫。H 和 CONNECT。並不會在此討論。 此結構非常類似于保存程式碼範例中的研究。

**StoClien** 用戶端會針對預期在 COPaper 中找到的連接點，執行適當的接收物件。 從 COPaper 的內容中， **StoClien** 所實行的重要接收物件會公開 **IPaperSink** 介面。 這是 COPaper 用來通知 **StoClien** COPaper 中各種事件的連出介面。

以下是從 IPAPER **IPaperSink** 的方法摘要。H \\ ： inc. 的同級目錄。



| 方法   | 描述                                                   |
|----------|---------------------------------------------------------------|
| 已鎖定   | 用戶端已取得和鎖定紙張的控制權。           |
| 已解除鎖定 | 用戶端具有紙張的 relinquished 控制。               |
| 已載入   | 用戶端已從自己的複合檔案載入紙張內容。 |
| 已儲存    | 用戶端已將書面內容儲存至它自己的複合檔案。    |
| InkStart | 用戶端已啟動紙張的色彩筆墨繪圖順序。   |
| InkDraw  | 用戶端會將筆墨資料點放在紙張表面上。     |
| InkStop  | 用戶端已停止紙張的筆墨繪圖順序。   |
| 刪除   | 用戶端已從紙張中清除所有筆墨資料。              |
| 調整  | 用戶端已調整紙張大小。                               |



 

這些方法大多容易理解。 雖然接收必須以某種方式執行所有這些方法，但是許多會實作為存根，而且不會用於 **StoServe** / **StoClien** 範例中。

這些範例中使用的重要方法是已載入的方法。 當用戶端告知 COPaper 從檔案載入新的繪圖時，它需要一種方法，在載入新資料時通知用戶端。 若要這樣做，COPaper 會呼叫 **IPaperSink：：** 在用戶端接收上載入。 然後，用戶端可以呼叫 [**IPaper：：重繪**](ipaper--redraw.md) ，要求 COPaper 播放新資料給用戶端。 重新繪製會導致在用戶端的顯示器中重新繪製載入的繪圖。 當載入完成時，新載入的繪圖會自動顯示在用戶端提供的視窗中。

如需此 IPaper 方法與 **IPaperSink** 連線的完整資訊，請參閱 [**IPaper：：重繪**](ipaper--redraw.md)。

**InkStart**、 **InkDraw** 和 **InkStop** 的 **IPaperSink** 方法可用來將個別的筆墨資料封包傳送回用戶端。 在接收時，用戶端會在其顯示中繪製它們，就像最初將它們傳送至 COPaper 的方式一樣。 上述邏輯的一般功能足以讓多個用戶端全都接聽相同的 CONNPOINT \_ PAPERSINK 連接點。 如果這些用戶端共用了一般 COPaper 實例，則這些用戶端可能會藉由連接到此連接點來顯示相同的繪圖。

 

 