---
description: COM + 佇列元件服務完全支援分割區的概念。 也就是說，在分割區中執行已排入佇列的元件時，會將訊息排入佇列，而元件最後會在元件分割區中執行。
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: COM + 佇列元件和分割區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0296119d32eafefd3212ae37e32543b8fd14b884ff6401c16827717a9a6960b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129070"
---
# <a name="com-queued-components-and-partitions"></a>COM + 佇列元件和分割區

COM + 佇列元件服務完全支援分割區的概念。 也就是說，在分割區中執行已排入佇列的元件時，會將訊息排入佇列，而且最後會在元件的磁碟分割內執行該元件。

## <a name="queue-names-for-partitioned-components"></a>分割區元件的佇列名稱

傳統上，已排入佇列的元件服務會使用應用程式名稱做為佇列名稱。 這表示在非資料分割的情況下，只有一個應用程式名稱實例存在於電腦上，每個應用程式名稱都有自己的訊息佇列。

不過，在資料分割的情況下，相同應用程式名稱的多個實例可以存在於電腦上，佇列元件服務會針對任何共用相同應用程式名稱的已佇列元件使用相同的佇列。

## <a name="activating-queued-components"></a>啟用已排入佇列的元件

分割區識別碼用來啟動非佇列元件的相同規則適用于已排入佇列的元件，如下所示：

-   如果使用了「標記」來啟動已排入佇列的元件，並包含分割區識別碼，則會使用此資料分割識別碼來找出資料分割。 此分割識別碼的優先順序高於任何可能存在於正在啟動的元件之內容中的分割區識別碼。
-   如果未使用任何標記來啟用元件，則會使用物件內容中的分割區識別碼。
-   如果物件的內容中沒有任何資料分割識別碼，則會使用 Active Directory 內的預設使用者對分割區對應。

> [!Note]  
> 如果伺服器電腦與網路中斷連線，而且當伺服器中斷連線時，使用者對分割集的對應已變更，則磁碟分割快取可能會包含過期的使用者對資料分割集對應。 如果使用者對分割集對應是用來啟動元件的機制，這可能會導致啟用錯誤。

 

COM + 事件會完全整合到資料分割中。 這表示訂閱者可以訂閱其應用程式位於資料分割內的發行者。 若要允許此訂閱，訂閱者類別集合包含兩個與資料分割相關的屬性：事件類別資料分割識別碼和事件類別應用程式識別碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式設計限制](application-design-restrictions.md)
</dt> <dt>

[分割區執行](partition-implementation.md)
</dt> <dt>

[在分割區中註冊和啟用元件](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[什麼是 COM + 磁碟分割？](what-are-com--partitions-.md)
</dt> </dl>

 

 



