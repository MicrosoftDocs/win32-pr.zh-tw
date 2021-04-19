---
description: 儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 IEventSubscription2 介面。
ms.assetid: fd1c136e-6e4e-42ca-a951-4aa5fcdfaa49
title: IEventSubscription3 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3
api_type:
- COM
api_location: ''
ms.openlocfilehash: 94225faf957b2eac3388422d74df3cfdb8bf6d90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973978"
---
# <a name="ieventsubscription3-interface"></a>IEventSubscription3 介面

儲存和捕獲事件訂閱的相關資訊。 這個介面會擴充 [**IEventSubscription2**](ieventsubscription2.md) 介面。

## <a name="when-to-implement"></a>執行時機

您不需要執行 **IEventSubscription3** 介面。 系統提供的事件物件類別 (CLSID \_ CEventSubscription) 實行 **IEventSubscription3**。

## <a name="when-to-use"></a>使用時機

[Com + 事件](com--events.md)系統會使用此介面來取得個別訂閱的相關資訊。

## <a name="members"></a>成員

**IEventSubscription3** 介面繼承自 **IEventSubscription2**。 **IEventSubscription3** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IEventSubscription3** 介面具有這些屬性。



| 屬性                                                                                  | 存取類型           | Description                                                |
|:------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------|
| [**EventClassApplicationID**](ieventsubscription3-eventclassapplicationid.md)<br/> | 讀取/寫入<br/> | 事件類別物件的應用程式 GUID。<br/> |
| [**EventClassPartitionID**](ieventsubscription3-eventclasspartitionid.md)<br/>     | 讀取/寫入<br/> | 事件類別物件的資料分割 GUID。<br/>   |
| [**SubscriberApplicationID**](ieventsubscription3-subscriberapplicationid.md)<br/> | 讀取/寫入<br/> | 訂閱者的應用程式 GUID。<br/>         |
| [**SubscriberPartitionID**](ieventsubscription3-subscriberpartitionid.md)<br/>     | 讀取/寫入<br/> | 訂閱者的資料分割 GUID。<br/>           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEventSubscription2**](ieventsubscription2.md)
</dt> </dl>

 

 




