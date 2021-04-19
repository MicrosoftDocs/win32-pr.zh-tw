---
description: COM + 事件服務是用來管理將發行者的事件傳遞給訂閱者。
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: 使用 com + 事件與 COM + 佇列元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973788"
---
# <a name="using-com-events-with-com-queued-components"></a>使用 com + 事件與 COM + 佇列元件

COM + 事件服務是用來管理將發行者的事件傳遞給訂閱者。 COM + 佇列的元件服務可以用來將發行者和訂閱者的訊息排入佇列，讓發行者和訂閱者的處理時間獨立，並在稍後將它重新顯示給訂閱者。 您是否需要使用已排入佇列的元件服務，取決於您應用程式的基礎商務邏輯。 如果您需要與時間無關的事件，您可以使用 COM + 事件服務與 COM + 佇列元件服務來建立它們。

> [!Note]  
> 如需使用 COM + 佇列元件服務的詳細資訊，請參閱 [Com + 佇列元件](com--queued-components.md)。

 

排入佇列的元件服務會維護單一訊息內的方法調用順序。 錄製器會將所有方法調用都批次處理到訊息中，然後播放程式在處理訊息時依序叫用這些方法。

排入佇列的元件錄製器和播放機可放置在下列兩個位置的其中一個位置：

-   在發行者和事件物件之間
-   在事件物件和訂閱者之間

如果您在「發行者」和「事件」物件之間放置錄製器和播放機，則會讓 [事件類別](the-com--event-class-object.md) 元件 queuable。 事件類別元件必須標示為排入佇列，並且由播放程式在與發行者不同的進程中啟動。

若要以非同步方式傳遞事件，請在事件物件和訂閱者之間撰寫錄製器和播放機，並設定訂閱物件的佇列屬性。 這會設定 SubscriberMoniker，如下所示： "queue：/new：/ {12345678-1234-1234-1234-123456789012} "。

在事件情況下使用佇列元件時，會有隱含的行程順序。 由於已排入佇列的元件服務會在單一物件的存留期內記錄並播放所有呼叫，因此所有呼叫都會依發出的順序重新執行。 但是，如果有多個會話有一個以上的物件，則無法保證順序。 如果順序很重要，請確定需要依序播放的呼叫位於相同的物件實例上。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> <dt>

[在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[訂用帳戶](subscriptions.md)
</dt> <dt>

[COM + 事件類別物件](the-com--event-class-object.md)
</dt> </dl>

 

 



