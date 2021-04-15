---
description: 由 Microsoft Internet Explorer 系統事件通知服務使用 (SENS) 來存取事件資料存放區。 這個介面會擴充 IEventSystem 介面。
ms.assetid: ad3c38a6-fa2d-4fcd-8782-1fac7595e829
title: IEventSystem2 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3a174c9457dc347257677e8111772ad14f0dc9fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468385"
---
# <a name="ieventsystem2-interface"></a>IEventSystem2 介面

由 Microsoft Internet Explorer 系統事件通知服務使用 (SENS) 來存取事件資料存放區。 這個介面會擴充 [**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem) 介面。

## <a name="when-to-implement"></a>執行時機

您不需要執行 **IEventSystem2** 介面。 系統提供的事件系統物件 (CLSID \_ CEventSystem) 實行 **IEventSystem2**。

## <a name="when-to-use"></a>使用時機

如果您使用 SENS，您可以呼叫 **IEventSystem2** 的方法，在事件存放區中新增和移除物件，以及從事件存放區取得物件。

因為不再支援 [**IEventPublisher**](/windows/desktop/api/eventsys/nn-eventsys-ieventpublisher)和發行者物件，所以不會在 [**ChangedPublisher**](/windows/desktop/api/Eventsys/nf-eventsys-ieventobjectchange-changedpublisher)方法上呼叫 [**IEventObjectChange**](/windows/desktop/api/Eventsys/nn-eventsys-ieventobjectchange) 。

## <a name="members"></a>成員

**IEventSystem2** 介面繼承自 **IEventSystem**。 **IEventSystem2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IEventSystem2** 介面具有這些方法。



| 方法                                                                         | 描述                                                                       |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetVersion**](ieventsystem2-getversion.md)                                 | 捕獲事件系統的版本號碼。<br/>                      |
| [**VerifyTransientSubscribers**](ieventsystem2-verifytransientsubscribers.md) | 確認資料存放區中的所有暫時性訂閱者是否存在。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEventSystem**](/windows/desktop/api/EventSys/nn-eventsys-ieventsystem)
</dt> </dl>

 

