---
description: 下列程式碼範例將示範如何處理新的呼叫通知，例如尋找或建立適當的終端機來呈現媒體。
ms.assetid: 77f6e1b5-b60e-4e8d-b747-7eceae8b0611
title: 接收來電
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a78ebf5b77569f8468a8b2c0a30217f4f7430e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985492"
---
# <a name="receive-a-call"></a><span data-ttu-id="191ce-103">接收來電</span><span class="sxs-lookup"><span data-stu-id="191ce-103">Receive a Call</span></span>

<span data-ttu-id="191ce-104">下列程式碼範例將示範如何處理新的呼叫通知，例如尋找或建立適當的終端機來呈現媒體。</span><span class="sxs-lookup"><span data-stu-id="191ce-104">The following code example demonstrates handling of new call notifications, such as finding or creating appropriate terminals to render the media.</span></span> <span data-ttu-id="191ce-105">這個範例是應用程式必須針對事件處理執行的 switch 語句的一部分。</span><span class="sxs-lookup"><span data-stu-id="191ce-105">This example is a portion of the switch statement an application must implement for event handling.</span></span> <span data-ttu-id="191ce-106">程式碼本身可能包含在 [**ITTAPIEventNotification：：事件**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)的執行中，或者 **事件** 方法可能會將訊息張貼至包含參數的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="191ce-106">The code itself may be contained in the implementation of [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event), or the **Event** method may post a message to a worker thread that contains the switch.</span></span>

<span data-ttu-id="191ce-107">使用此程式碼範例之前，您必須在 [初始化 TAPI](initialize-tapi.md)中執行作業、 [選取位址](select-an-address.md)，以及 [註冊事件](register-events.md)。</span><span class="sxs-lookup"><span data-stu-id="191ce-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md), [Select an Address](select-an-address.md), and [Register Events](register-events.md).</span></span>

<span data-ttu-id="191ce-108">此外，您必須執行在 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)和 [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)介面指標抓取之後，[選取 [終端](select-a-terminal.md)機] 中所示的作業。</span><span class="sxs-lookup"><span data-stu-id="191ce-108">Also, you must perform the operations illustrated in [Select a Terminal](select-a-terminal.md) following the retrieval of the [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) and [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) interface pointers.</span></span>

> [!Note]  
> <span data-ttu-id="191ce-109">此範例沒有適用于實際執行程式碼的錯誤檢查和發行。</span><span class="sxs-lookup"><span data-stu-id="191ce-109">This example does not have the error checking and releases appropriate for production code.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="191ce-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="191ce-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="191ce-111">事件</span><span class="sxs-lookup"><span data-stu-id="191ce-111">Events</span></span>](events.md)
</dt> <dt>

[<span data-ttu-id="191ce-112">**ITTAPIEventNotification**</span><span class="sxs-lookup"><span data-stu-id="191ce-112">**ITTAPIEventNotification**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-ittapieventnotification)
</dt> <dt>

[<span data-ttu-id="191ce-113">**ITTAPI::RegisterCallNotifications**</span><span class="sxs-lookup"><span data-stu-id="191ce-113">**ITTAPI::RegisterCallNotifications**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications)
</dt> <dt>

[<span data-ttu-id="191ce-114">**ITCallNotificationEvent**</span><span class="sxs-lookup"><span data-stu-id="191ce-114">**ITCallNotificationEvent**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)
</dt> <dt>

[<span data-ttu-id="191ce-115">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="191ce-115">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="191ce-116">**ITBasicCallControl**</span><span class="sxs-lookup"><span data-stu-id="191ce-116">**ITBasicCallControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)
</dt> <dt>

[<span data-ttu-id="191ce-117">**ITTerminalSupport**</span><span class="sxs-lookup"><span data-stu-id="191ce-117">**ITTerminalSupport**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)
</dt> </dl>

 

 
