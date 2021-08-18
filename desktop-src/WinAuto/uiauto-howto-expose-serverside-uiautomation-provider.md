---
title: 如何公開 Server-Side 消費者介面自動化提供者
description: 本主題包含範例程式碼，示範如何公開自訂控制項的伺服器端 Microsoft 消費者介面自動化提供者。
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133311"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>如何公開 Server-Side 消費者介面自動化提供者

本主題包含範例程式碼，示範如何公開自訂控制項的伺服器端 Microsoft 消費者介面自動化提供者。

Microsoft 消費者介面自動化將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送給提供者應用程式，以取得提供者所支援之可存取物件的相關資訊。 當用戶端呼叫 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)、 [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)和 [**system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)，以及處理用戶端已註冊的事件時，消費者介面自動化傳送 **WM \_ GETOBJECT** 。

當提供者收到 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息時，它應該會檢查 *LParam* 參數是否等於 **UiaRootObjectId**。 如果是，則提供者應該傳回物件的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面。 提供者會藉由呼叫 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函數來傳回介面。

下列範例示範如何回應 [**WM \_ GETOBJECT**](wm-getobject.md)。


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[執行 Server-Side 消費者介面自動化提供者](uiauto-serversideprovider.md)
</dt> <dt>

[WM \_ GETOBJECT 訊息](the-wm-getobject-message.md)
</dt> <dt>

[消費者介面自動化提供者的使用說明主題](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




