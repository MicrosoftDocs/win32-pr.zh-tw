---
description: 建立 Publisher 篩選
ms.assetid: d91efecc-f02a-41c6-acf7-37b74723e7e8
title: 建立 Publisher 篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2cf3391cd331f7d81c3bb7ff467c140a78b0c8e30fb609ea655596dfe745a74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128790"
---
# <a name="creating-a-publisher-filter"></a>建立 Publisher 篩選

有兩種方法可以建立發行者篩選器：使用事件類別的 MultiPublisherFilterCLSID 屬性，或使用 [**IEventControl：： SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)。

-   因為它可讓您使用 [Com + 佇列元件](com--queued-components.md) 服務來撰寫事件物件，所以慣用的方法是使用事件類別中的 MultiPublisherFilterCLSID 屬性來設定發行者篩選。 這會為事件物件的事件介面的所有方法建立一個篩選物件。 當事件類別物件是使用 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)具現化時，事件物件會啟動發行者篩選器。
-   您也可以使用 [**SetPublisherFilter**](/windows/desktop/api/Eventsys/nf-eventsys-ieventcontrol-setpublisherfilter)。 但是，如果您選擇此方法，則不會 queuable 介面，因此無法在發行者和事件類別物件之間使用事件物件與 COM + 佇列元件服務。 如需搭配使用佇列元件服務與 COM + 事件的詳細資訊，請參閱使用 com + [事件與 com + 佇列元件](using-com--events-with-com--queued-components.md)。

一個事件可以有一個或多個篩選物件，也可以是 none。 發行者篩選物件必須支援 [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) 或 [**IMultiInterfacePublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-imultiinterfacepublisherfilter)，視您是否有單一引發介面或事件類別物件上的多個引發介面而定。 **IPublisherFilter** 和 **IMultiInterfacePublisherFilter** 介面都會指定 **Initialize** 方法。 建立篩選物件之後，事件類別物件會立即呼叫 **Initialize** 方法。

COM + 事件會嘗試在篩選準則上叫用兩個方法。 首先，它會呼叫 [**IPublisherFilter：:P reparetofire**](/windows/desktop/api/EventSys/nf-eventsys-ipublisherfilter-preparetofire) ，並將 [**IFiringControl**](/windows/desktop/api/EventSys/nn-eventsys-ifiringcontrol) 介面指標傳遞至篩選準則。 然後，它會查詢事件介面的篩選物件。 如果篩選支援事件介面，則會在其上叫用方法。 這可讓您存取事件的發行者參數。 篩選可以使用這些參數來判斷要引發的訂閱。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> </dl>

 

 
