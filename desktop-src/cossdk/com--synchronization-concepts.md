---
description: 一般而言，如果您有單一執行緒的單元 (STA) ，就不需要同步處理，因為該單元會為您提供同步處理。
ms.assetid: a05de040-0115-44aa-80e2-55eff2ec894d
title: COM + 同步處理概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4153c02a5fcd9a0990459e360d239396e7de30cff22316da70f73002e73d6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129000"
---
# <a name="com-synchronization-concepts"></a>COM + 同步處理概念

一般而言，如果您有單一執行緒的單元 (STA) ，就不需要同步處理，因為該單元會為您提供同步處理。 當您有多執行緒單元 (MTA) 和無限制執行緒物件時，同步處理就會變得很重要。 在過去，無限制執行緒物件必須處理鎖定。 您可以藉由設定元件的同步處理屬性，來消除使用鎖定的需求。

同步處理具有下列屬性：

-   允許一個呼叫者一次輸入元件。
-   禁止跨進程或跨電腦的流程。
-   流程中的元件至元件。
-   允許來自相同呼叫端的重新進入。

不同于單元，活動會跨越多個進程和主機的內容。 同步處理會決定哪個活動會包含物件。 物件可以位於下列任何活動中：

-   Creator 的活動
-   新增活動
-   沒有活動

COM + 可針對每個活動的一連串鎖定來確保並行。 如果呼叫端嘗試輸入已由另一個呼叫者使用的 COM + 同步處理元件，呼叫會被封鎖直到釋放鎖定為止。 此封鎖行為不會有時間，而且無法設定為超時。如果鎖定未在使用中，則會取得鎖定並處理呼叫。 完成之後，就會釋放鎖定給下一個呼叫者。 為了防止鎖死，COM + 會透過整個網路中連結的一連串呼叫來管理跨活動的所有物件存取。

COM + 提供下列同步處理設定：

-   已停用
-   不支援
-   支援
-   必要
-   必須是新交易

> [!Note]  
> 某些同步處理設定會與其他 COM + 元件設定一起使用。 例如，如果已啟用 [Com + 及時 (JIT) ](com--just-in-time-activation.md) 啟用服務，則需要同步處理。 如果您啟用交易，則需要 JIT;因此，COM + [交易處理](com--transactions.md) 也需要進行同步處理。 因此，具有 JIT = True 設定的類別，也必須設定為 [同步] = [必要] 或 [同步處理 = RequiresNew]。

 

如需使用 [元件服務] 系統管理工具設定同步處理選項的指示，請參閱 [設定同步處理屬性](setting-the-synchronization-attribute.md)。

若要取得有關使用 COM + 管理程式庫來設定同步處理選項的詳細資訊，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 同步處理工作](com--synchronization-tasks.md)
</dt> </dl>

 

 



