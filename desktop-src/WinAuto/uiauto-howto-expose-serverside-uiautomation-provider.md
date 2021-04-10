---
title: 如何公開 Server-Side 消費者介面自動化提供者
description: 本主題包含範例程式碼，示範如何公開自訂控制項的伺服器端 Microsoft 消費者介面自動化提供者。
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183715"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="ad776-103">如何公開 Server-Side 消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="ad776-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="ad776-104">本主題包含範例程式碼，示範如何公開自訂控制項的伺服器端 Microsoft 消費者介面自動化提供者。</span><span class="sxs-lookup"><span data-stu-id="ad776-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="ad776-105">Microsoft 消費者介面自動化將 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息傳送給提供者應用程式，以取得提供者所支援之可存取物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ad776-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="ad776-106">當用戶端呼叫 [**IUIAutomation：： ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle)、 [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)和 [**system.windows.input.focusmanager.getfocusedelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)，以及處理用戶端已註冊的事件時，消費者介面自動化傳送 **WM \_ GETOBJECT** 。</span><span class="sxs-lookup"><span data-stu-id="ad776-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="ad776-107">當提供者收到 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息時，它應該會檢查 *LParam* 參數是否等於 **UiaRootObjectId**。</span><span class="sxs-lookup"><span data-stu-id="ad776-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="ad776-108">如果是，則提供者應該傳回物件的 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 介面。</span><span class="sxs-lookup"><span data-stu-id="ad776-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="ad776-109">提供者會藉由呼叫 [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) 函數來傳回介面。</span><span class="sxs-lookup"><span data-stu-id="ad776-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="ad776-110">下列範例示範如何回應 [**WM \_ GETOBJECT**](wm-getobject.md)。</span><span class="sxs-lookup"><span data-stu-id="ad776-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ad776-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad776-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ad776-112">**概念**</span><span class="sxs-lookup"><span data-stu-id="ad776-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ad776-113">執行 Server-Side 消費者介面自動化提供者</span><span class="sxs-lookup"><span data-stu-id="ad776-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="ad776-114">WM \_ GETOBJECT 訊息</span><span class="sxs-lookup"><span data-stu-id="ad776-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="ad776-115">消費者介面自動化提供者的使用說明主題</span><span class="sxs-lookup"><span data-stu-id="ad776-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




