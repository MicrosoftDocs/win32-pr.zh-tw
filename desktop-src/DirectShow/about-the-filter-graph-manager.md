---
description: 關於篩選圖形管理員
ms.assetid: a227539a-7f9a-4f8d-99fe-f9ab67df9ef4
title: 關於篩選圖形管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedf716b84ee62818e323bfaa082b6252e5faad0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510221"
---
# <a name="about-the-filter-graph-manager"></a>關於篩選圖形管理員

[篩選圖形管理員](filter-graph-manager.md)是一個 COM 物件，可控制篩選圖形中的篩選。 它會執行許多功能，包括下列各項：

-   協調篩選之間的狀態變更。
-   建立參考時鐘。
-   將事件傳達回應用程式。
-   提供應用程式用來建立篩選圖形的方法。

其中每個函式都會在這裡簡短描述。 您可以在檔的其他位置找到詳細資料。

**狀態變更**。 篩選準則內的狀態變更必須以特定順序發生。 因此，應用程式不會直接對篩選發出狀態變更命令。 相反地，它會為篩選圖形管理員提供單一命令，此命令會將命令散發給每個篩選準則。 搜尋的運作方式類似：應用程式會向篩選圖形管理員提供搜尋命令，該命令會將其散發至篩選。

**參考時鐘**。 圖形中的所有篩選都使用相同的時鐘，稱為 *參考時鐘*。 參考時鐘可確保同步處理所有的資料流程。 應轉譯影片畫面或音訊樣本的時間，稱為呈現 *時間*。 呈現時間是相對於參考時鐘來測量。 篩選圖形管理員選擇參考時鐘，通常是音效卡上的時鐘或系統時鐘。

**圖形事件**。 篩選圖形管理員會使用事件佇列來通知應用程式發生在篩選圖形中的事件。 這項機制類似于 Windows 訊息迴圈。

**圖形建立方法**。 篩選圖形管理員會提供方法，讓應用程式將篩選準則新增至圖形、將篩選連接至其他篩選，以及中斷篩選。

篩選圖形管理員未處理的一個函式，是將資料從一個篩選準則移至下一個篩選準則。 這是由篩選準則本身透過其 pin 連接來完成。 處理一律會在個別的執行緒上發生。

> [!Note]  
> 篩選準則一律是無限制執行緒、位於與篩選圖形管理員相同的進程中，並從同進程伺服器載入。 因此，方法呼叫不會在篩選之間，或在篩選器和篩選圖形管理員之間進行封送處理。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[篩選圖形中的資料流程](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> <dt>

[設定圖形時鐘](setting-the-graph-clock.md)
</dt> <dt>

[DirectShow 中的時間和時鐘](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



