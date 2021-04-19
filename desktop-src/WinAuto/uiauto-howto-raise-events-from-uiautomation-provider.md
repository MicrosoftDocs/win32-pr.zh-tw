---
title: 如何從消費者介面自動化提供者引發事件
description: 本主題包含範例程式碼，說明 Microsoft 消費者介面自動化提供者如何引發事件。
ms.assetid: 43826258-9321-4d44-bd31-6a3b42f00d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417c86771c24cc1a67fd907aaf0628037edce44d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965189"
---
# <a name="how-to-raise-events-from-a-ui-automation-provider"></a>如何從消費者介面自動化提供者引發事件

本主題包含範例程式碼，說明 Microsoft 消費者介面自動化提供者如何引發事件。

下列範例程式碼顯示應用程式中的方法，該方法會執行自訂按鈕。 每當叫用自訂按鈕時，應用程式就會呼叫方法。 方法會檢查是否有任何用戶端正在接聽事件，如果有的話，則會引發 UIA 叫用 [**\_ \_ InvokedEventId**](uiauto-event-ids.md) 事件，以通知用戶端已叫用該按鈕。


```C++
// Responds to a button click. The source of the click could 
// be the mouse, the keyboard, or a client's call to 
// IUIAutomationInvokePattern::Invoke.
void CustomButton::InvokeButton(HWND hwnd)
{
    // TODO: Perform program actions invoked by the control.

    // Check whether any clients are listening for UI Automation 
    // events.
    if (UiaClientsAreListening())
    {
        // Raise an Invoked event. GetUIAutomationProvider is an
        // application-defined method that returns a pointer to
        // the application's IRawElementProviderSimple interface.
        UiaRaiseAutomationEvent(
            GetUIAutomationProvider(hwnd), UIA_Invoke_InvokedEventId); 
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[消費者介面自動化提供者的使用說明主題](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




