---
description: COM + 事件提供兩種方式來控制哪些事件可抵達哪些訂閱者：發行者篩選和參數篩選。
ms.assetid: dfc82a57-5587-462d-a43d-516b7d70e25e
title: 在 COM + 中篩選事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3a7d152813e4806a9cfb6a342255e0981ecf37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689108"
---
# <a name="filtering-events-in-com"></a>在 COM + 中篩選事件

COM + 事件提供兩種方式來控制哪些事件可抵達哪些訂閱者： *發行者篩選* 和 *參數篩選*。

## <a name="publisher-filtering"></a>發行者篩選

發行者篩選會依據 [事件類別](the-com--event-class-object.md) 物件，控制事件方法的順序和引發。 發行者篩選可讓發行者判斷哪些訂閱者會收到特定的事件。

發行者篩選的有效使用範例是股票交換。 大部分的訂閱者都想要知道何時新增股票。 但是，其中許多相同的訂閱者可能不想要在每次股價變更時都知道。 「發行者篩選」提供將事件有效傳遞給只需要此資訊的「訂閱者」所需的資料細微性。

在具現化事件類別物件上叫用方法時，它會收集該方法上的任何發行者篩選準則。 篩選準則會強制事件物件將事件方法引發至特定的訂閱者。 篩選準則會決定要引發哪些訂用帳戶，以及要引發這些訂閱的順序。 例如，篩選器可以讀取訂用帳戶清單，並根據某些應用程式準則建立訂單，然後依該順序呼叫「訂閱者」。

如需建立發行者篩選準則的詳細指示，請參閱 [建立發行者篩選](creating-a-publisher-filter.md)。

## <a name="parameter-filtering"></a>參數篩選

相較于發行者篩選，COM + 事件服務會針對每個訂閱及每個事件方法調用，提供選擇性的訂閱者參數篩選。 參數篩選會根據事件方法的參數來評估訂閱 >filtercriteria 屬性。 這種類型的篩選適用于個別方法、每個訂用帳戶，並在事件來源提供訂閱者篩選層級。 篩選準則字串會辨識檢查相等 (=、= =、!,! =、~、~ =、 <>) 、嵌套括弧和邏輯關鍵字 **and**、 **or** 或 **NOT** 的關係運算子。

參數篩選會在任何發行者篩選之後，以及針對指定的訂用帳戶引發標準事件物件時進行。 如果使用發行者篩選，只有當發行者篩選準則叫用 [**IFiringControl：： FireSubscription**](/windows/desktop/api/EventSys/nf-eventsys-ifiringcontrol-firesubscription)時，才會進行參數篩選。 基於這個原因，發行者篩選和參數篩選可以一起撰寫，但發行者篩選會優先使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[訂用帳戶](subscriptions.md)
</dt> <dt>

[COM + 事件類別物件](the-com--event-class-object.md)
</dt> <dt>

[使用 com + 事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



