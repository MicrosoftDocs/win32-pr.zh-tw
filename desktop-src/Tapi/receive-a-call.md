---
description: 下列程式碼範例將示範如何處理新的呼叫通知，例如尋找或建立適當的終端機來呈現媒體。
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: 接收來電
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9e4ce02ec11a1373d16b9b9ebd0fba29313b1d532175894c6fd1b12a38e2bf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060466"
---
# <a name="receive-a-call"></a>接收來電

下列程式碼範例將示範如何處理新的呼叫通知，例如尋找或建立適當的終端機來呈現媒體。 這個範例是應用程式必須針對事件處理執行的 switch 語句的一部分。 程式碼本身可能包含在 [**ITTAPIEventNotification：：事件**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)的執行中，或者 **事件** 方法可能會將訊息張貼至包含參數的背景工作執行緒。

使用此程式碼範例之前，您必須在 [初始化 TAPI](initialize-tapi.md)中執行作業、 [選取位址](select-an-address.md)，以及 [註冊事件](register-events.md)。

此外，您必須執行在 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)和 [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)介面指標抓取之後，[選取 [終端](select-a-terminal.md)機] 中所示的作業。

> [!Note]  
> 此範例沒有適用于實際執行程式碼的錯誤檢查和發行。

 

``` syntax
// pEvent is an IDispatch pointer for the ITCallNotificationEvent interface of the
// call object created by TAPI, and is passed into the event handler by TAPI. 

case TE_CALLNOTIFICATION:
{
    // Get the ITCallNotification interface.
    ITCallNotificationEvent * pNotify;
    hr = pEvent->QueryInterface( 
            IID_ITCallNotificationEvent, 
            (void **)&pNotify 
            );
    // If ( hr != S_OK ) process the error here. 
    
    // Get the ITCallInfo interface.
    ITCallInfo * pCallInfo;
    hr = pNotify->get_Call( &pCallInfo);
    // If ( hr != S_OK ) process the error here. 

    // Get the ITBasicCallControl interface.
    ITBasicCallControl * pBasicCall;
    hr = pCallInfo->QueryInterface(
            IID_ITBasicCallControl,
            (void**)&pBasicCall
            );
    // If ( hr != S_OK ) process the error here. 

    // Get the ITAddress interface.
    ITAddress * pAddress;
    hr = pCallInfo->get_Address( &pAddress );
    // If ( hr != S_OK ) process the error here. 

    // Create the required terminals for this call.
    {
        // See the Select a Terminal code example.
    }
    // Complete incoming call processing.
    hr = pBasicCall->Answer();
    // If ( hr != S_OK ) process the error here. 
}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[事件](events.md)
</dt> <dt>

[**ITTAPIEventNotification**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[**ITTAPI::RegisterCallNotifications**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
