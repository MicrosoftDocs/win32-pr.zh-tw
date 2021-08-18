---
description: 系統事件通知服務適用于 COM + 事件系統。
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: SENS 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ad8ae9c5ec50f4f36c07ed592599cf5e09775bd7f450844c83cc42a4c580f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890407"
---
# <a name="sens-architecture"></a>SENS 架構

系統事件通知服務適用于 COM + 事件系統。 SENS 是它所監視的事件類別的事件發行者：網路、登入和電源/電池事件。 接收通知的應用程式稱為「事件訂閱者」。

當應用程式訂閱接收通知時，也可以指定與訂閱的事件相關聯的篩選準則。 SENS 和 COM + 事件會使用篩選器，進一步判斷應用程式應該收到通知的時機。

通知是非同步，因此在傳送通知時，接收通知的應用程式不一定要處於作用中狀態。 當應用程式訂閱接收通知時，它可以指定事件發生時是否應該啟動，或稍後在活動啟用時通知。

只有在應用程式停止執行之前，訂用帳戶可以是暫時性且有效的，否則它可能會一直有效，直到從系統移除應用程式為止。

COM + 事件資料存放區包含事件發行者 (SENS) 、事件訂閱者和篩選器的相關資訊。 SENS 也會針對類型程式庫中的每個事件類別預先定義輸出介面。



| 事件類別    | GUID                          | 介面    |
|----------------|-------------------------------|--------------|
| 網路事件 | SENSGUID \_ EVENTCLASS \_ 網路 | ISensNetwork |
| 登入事件   | SENSGUID \_ EVENTCLASS \_ 登入   | ISensLogon   |
| 電源活動   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

若要接收任何這些事件的通知，您的應用程式必須執行下列兩項作業：

-   訂閱您感興趣的 SENS 事件。 若要訂閱事件，請在 COM + 事件中使用 **IEventSubscription** 和 **IEventSystem** 介面。 您必須提供事件類別的識別碼和 SENS 發行者識別碼 SENSGUID \_ 發行者。 訂用帳戶在每個事件層級上，因此訂閱應用程式也必須指定類別中的哪些事件有興趣。 每個事件都會對應至介面中對應至其事件類別的方法。
-   針對您處理的每個介面，建立具有執行的接收物件。 如需這些介面和各介面所支援之事件的詳細資訊，請參閱 [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork)、 [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)和 [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) 。

當其中一個受監視的事件發生時，SENS 會使用任何相關聯的篩選來處理每個訂閱，並透過 COM + 事件系統通知訂閱者。

 

 



