---
description: 事件是 TAPI 3 下呼叫處理的重要部分。 事件處理包含四個階段。
ms.assetid: db43f4e0-f2f5-49b1-a03d-3df3de0e5611
title: " (電話語音 API) 的事件"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3b2cf181f10373505a0fe50d3c9efa7358b3ccb749acb723d8314dee27ff9aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660858"
---
# <a name="events-telephony-api"></a> (電話語音 API) 的事件

事件是 TAPI 3 下呼叫處理的重要部分。 事件處理包含四個階段。

**若要註冊並啟用事件的接收**

1.  執行 [**ITTAPIEventNotification：：事件**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) 方法。  (TAPI 會在事件發生時呼叫這個方法。 ) 通常，此實 **AddRef** 不會超過 **IDispatch** 介面指標，然後張貼至應用程式的訊息提取。
2.  使用 COM 標準 [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer)和 [**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)介面註冊 [**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)輸出介面，然後將 [**IConnectionPoint：： Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise)方法的指標傳遞至 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)。
3.  呼叫 [**ITTAPI：:p \_ >eventfilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) 方法，讓 TAPI 知道應用程式將處理的事件。 事件篩選器包含 [**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)列舉的 **或** ed 成員。
    > [!Note]  
    > 您必須呼叫 **ITTAPI：:p 的 \_ >eventfilter** 方法來設定事件篩選器遮罩，並啟用事件的接收。 如果您未呼叫 **ITTAPI：:p] \_ >eventfilter**，您的應用程式將不會收到任何事件。

     

您也必須針對應用程式將處理呼叫的每個位址物件，呼叫 [**ITTAPI：： RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications) 方法。

請參閱 [事件介面](./event-interfaces.md) ，以取得所有事件介面的清單。 如需示範註冊程式的程式碼範例，請參閱 [註冊事件](register-events.md) ，並接收顯示一次使用事件之程式碼範例的 [呼叫](receive-a-call.md) 。

 

 
