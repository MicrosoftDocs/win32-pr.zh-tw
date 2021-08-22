---
description: 儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 IEventSubscription 介面。
ms.assetid: f153afb7-c897-40f8-81ed-50308844cac5
title: IEventSubscription2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 332f123756d1340352524852aa5bcb38fce09612f52554facaf6e5c8c2398e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047478"
---
# <a name="ieventsubscription2-interface"></a>IEventSubscription2 介面

儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 [**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription) 介面。

## <a name="when-to-implement"></a>執行時機

您不需要執行 **IEventSubscription2** 介面。 系統提供的事件物件類別 (CLSID \_ CEventSubscription) 實行 **IEventSubscription2**。

## <a name="when-to-use"></a>使用時機

[Com + 事件](com--events.md)系統會使用此介面來取得個別訂閱的相關資訊。

## <a name="members"></a>成員

**IEventSubscription2** 介面繼承自 **IEventSubscription**。 **IEventSubscription2** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IEventSubscription2** 介面具有這些屬性。



| 屬性                                                                      | 存取類型           | 描述                                                |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**>filtercriteria**](ieventsubscription2-filtercriteria.md)<br/>       | 讀取/寫入<br/> | 管理訂用帳戶的篩選準則。<br/> |
| [**SubscriberMoniker**](ieventsubscription2-subscribermoniker.md)<br/> | 讀取/寫入<br/> | 訂閱者的名字。<br/>                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEventSubscription**](/windows/desktop/api/EventSys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 




