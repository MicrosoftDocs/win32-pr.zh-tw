---
title: 存取 Microsoft Active Accessibility 伺服器
description: 消費者介面自動化 Proxy 的 Microsoft Active Accessibility 是一種軟體元件，可讓 Microsoft 消費者介面自動化用戶端與原生執行 IAccessible 介面的 Microsoft Active Accessibility 伺服器互動。
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- 消費者介面自動化，存取 Active Accessibility
- 消費者介面自動化，Active Accessibility
- 消費者介面自動化 Proxy
- 消費者介面自動化，消費者介面自動化 Proxy
- LegacyIAccessible 控制項模式
- 消費者介面自動化，LegacyIAccessible 控制項模式
- Microsoft Active Accessibility
- Active Accessibility
- 用戶端，存取 Active Accessibility 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97319028203351cd9f45b39d133fa38727d6861e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021147"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a><span data-ttu-id="5248e-112">存取 Microsoft Active Accessibility 伺服器</span><span class="sxs-lookup"><span data-stu-id="5248e-112">Accessing Microsoft Active Accessibility Servers</span></span>

<span data-ttu-id="5248e-113">消費者介面自動化 Proxy 的 Microsoft Active Accessibility 是一種軟體元件，可讓 Microsoft 消費者介面自動化用戶端與原生執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面的 Microsoft Active Accessibility 伺服器互動。</span><span class="sxs-lookup"><span data-stu-id="5248e-113">The Microsoft Active Accessibility to UI Automation Proxy is a software component that enables Microsoft UI Automation clients to interact with Microsoft Active Accessibility servers that implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface natively.</span></span> <span data-ttu-id="5248e-114">Proxy 支援 [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) 控制項模式，並為每個偵測到的 Microsoft Active Accessibility 伺服器提供 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) 介面的實例。</span><span class="sxs-lookup"><span data-stu-id="5248e-114">The proxy supports the [LegacyIAccessible](uiauto-implementinglegacyiaccessible.md) control pattern, and supplies an instance of the [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface for each Microsoft Active Accessibility server detected.</span></span> <span data-ttu-id="5248e-115">消費者介面自動化用戶端會使用 **IUIAutomationLegacyIAccessiblePattern** 所公開的方法來存取伺服器所支援的 Microsoft Active Accessibility 屬性和物件。</span><span class="sxs-lookup"><span data-stu-id="5248e-115">UI Automation clients use the methods exposed by **IUIAutomationLegacyIAccessiblePattern** to access the Microsoft Active Accessibility properties and objects supported by the server.</span></span>

<span data-ttu-id="5248e-116">如果消費者介面自動化專案具有基礎 Microsoft Active Accessibility 執行，則用戶端可以藉由將 [**UIA \_ LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md)控制項模式識別碼傳遞至下列其中一個 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)方法，來取得元素的 [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面指標：</span><span class="sxs-lookup"><span data-stu-id="5248e-116">If a UI Automation element has an underlying Microsoft Active Accessibility implementation, a client can obtain an [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface pointer for the element by passing the [**UIA\_LegacyIAccessiblePatternId**](uiauto-controlpattern-ids.md) control pattern ID to one of the following [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) methods:</span></span>

-   [<span data-ttu-id="5248e-117">**GetCachedPattern**</span><span class="sxs-lookup"><span data-stu-id="5248e-117">**GetCachedPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [<span data-ttu-id="5248e-118">**GetCachedPatternAs**</span><span class="sxs-lookup"><span data-stu-id="5248e-118">**GetCachedPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [<span data-ttu-id="5248e-119">**GetCurrentPattern**</span><span class="sxs-lookup"><span data-stu-id="5248e-119">**GetCurrentPattern**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [<span data-ttu-id="5248e-120">**GetCurrentPatternAs**</span><span class="sxs-lookup"><span data-stu-id="5248e-120">**GetCurrentPatternAs**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

<span data-ttu-id="5248e-121">[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面無法針對以消費者介面自動化為基礎的控制項使用。</span><span class="sxs-lookup"><span data-stu-id="5248e-121">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface is not available for controls based on UI Automation.</span></span>

<span data-ttu-id="5248e-122">[**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern)介面可讓消費者介面自動化用戶端存取 Microsoft Active Accessibility 專案的基礎 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)執行。</span><span class="sxs-lookup"><span data-stu-id="5248e-122">The [**IUIAutomationLegacyIAccessiblePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) interface enables UI Automation clients to access the underlying [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation of an Microsoft Active Accessibility element.</span></span> <span data-ttu-id="5248e-123">不過，介面並不支援消費者介面自動化功能所淘汰或多餘的方法。</span><span class="sxs-lookup"><span data-stu-id="5248e-123">However, the interface does not support methods that are obsolete or redundant with UI Automation features.</span></span> <span data-ttu-id="5248e-124">例如， **IUIAutomationLegacyIAccessiblePattern** 沒有相當於 [**IAccessible：： accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) 的方法，因為 UI 元素的目前位置可從消費者介面自動化 BoundingRectangle 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="5248e-124">For example, **IUIAutomationLegacyIAccessiblePattern** does not have a method that is equivalent to [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) because the current location of a UI element is available from the UI Automation BoundingRectangle property.</span></span>

<span data-ttu-id="5248e-125">[**IUIAutomationLegacyIAccessiblePattern：： GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible)方法可讓用戶端從消費者介面自動化元素取出 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面指標。</span><span class="sxs-lookup"><span data-stu-id="5248e-125">The [**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) method enables a client to retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer from an UI Automation element.</span></span> <span data-ttu-id="5248e-126">您也可以使用 [**IUIAutomation：： ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) 和 [**IUIAutomation：： ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) 方法來反轉反向。</span><span class="sxs-lookup"><span data-stu-id="5248e-126">The reverse is also possible by using the [**IUIAutomation::ElementFromIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) and [**IUIAutomation::ElementFromIAccessibleBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) methods.</span></span>

<span data-ttu-id="5248e-127">如果元素的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)介面是由 OLEACC.dll 的 proxy 物件或從消費者介面自動化到 Microsoft Active Accessibility 橋接器的 proxy 物件提供，則 [**IUIAutomationLegacyIAccessiblePattern：： GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible)會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="5248e-127">[**IUIAutomationLegacyIAccessiblePattern::GetIAccessible**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) returns **NULL** if the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element is provided by a proxy object from OLEACC.dll or from the UI Automation to Microsoft Active Accessibility Bridge.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5248e-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="5248e-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5248e-129">**概念**</span><span class="sxs-lookup"><span data-stu-id="5248e-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5248e-130">消費者介面自動化和 Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="5248e-130">UI Automation and Active Accessibility</span></span>](uiauto-msaa.md)
</dt> <dt>

[<span data-ttu-id="5248e-131">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="5248e-131">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




