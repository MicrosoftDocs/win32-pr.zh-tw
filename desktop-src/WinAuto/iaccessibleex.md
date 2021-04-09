---
title: IAccessibleEx 介面
description: 沒有 Microsoft 消費者介面自動化提供者，但會執行 IAccessible 的控制項，可以輕鬆地升級，藉由實 IAccessibleEx 介面來提供一些消費者介面自動化功能。
ms.assetid: 5523156e-c9b8-4aad-b568-f3b3c402d33e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a74e7d464acf18244d91bc69199a56004b20beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092297"
---
# <a name="the-iaccessibleex-interface"></a><span data-ttu-id="99e4a-103">IAccessibleEx 介面</span><span class="sxs-lookup"><span data-stu-id="99e4a-103">The IAccessibleEx Interface</span></span>

<span data-ttu-id="99e4a-104">沒有 Microsoft 消費者介面自動化提供者，但會執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)的控制項，可以輕鬆地升級，藉由實 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面來提供一些消費者介面自動化功能。</span><span class="sxs-lookup"><span data-stu-id="99e4a-104">Controls that do not have a Microsoft UI Automation provider, but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), can easily be upgraded to provide some UI Automation functionality by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="99e4a-105">這個介面可讓控制項公開消費者介面自動化屬性和控制項模式，而不需要完整地執行消費者介面自動化提供者介面（例如 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)）。</span><span class="sxs-lookup"><span data-stu-id="99e4a-105">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="99e4a-106">若要使用 **IAccessibleEx**、 **IRawElementProviderFragment** 和其他消費者介面自動化介面，請在原始程式碼中包含 UIAutomation .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="99e4a-106">To use **IAccessibleEx**, **IRawElementProviderFragment**, and all other UI Automation interfaces, include the UIAutomation.h header file in your source code.</span></span>

<span data-ttu-id="99e4a-107">例如，假設有一個具有範圍值的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="99e4a-107">For example, consider a custom control that has a range value.</span></span> <span data-ttu-id="99e4a-108">控制項的 Microsoft Active Accessibility 伺服器會定義控制項的角色，而且能夠傳回其目前的值。</span><span class="sxs-lookup"><span data-stu-id="99e4a-108">The Microsoft Active Accessibility server for the control defines the control's role and is able to return its current value.</span></span> <span data-ttu-id="99e4a-109">不過，因為 Microsoft Active Accessibility 不會定義最小和最大屬性，所以伺服器缺少傳回控制項最小值和最大值的方法。</span><span class="sxs-lookup"><span data-stu-id="99e4a-109">However, because Microsoft Active Accessibility does not define minimum and maximum properties, the server lacks the means to return the minimum and maximum values of the control.</span></span> <span data-ttu-id="99e4a-110">消費者介面自動化的用戶端能夠取得控制項的角色、目前的值和其他 Microsoft Active Accessibility 屬性，因為消費者介面自動化 core 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)取得這些屬性。</span><span class="sxs-lookup"><span data-stu-id="99e4a-110">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="99e4a-111">但是，若沒有物件的 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面存取權，消費者介面自動化也無法取得最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="99e4a-111">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="99e4a-112">控制項開發人員可以為控制項提供完整的消費者介面自動化提供者，但這表示複製了許多現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行功能：例如，導覽和通用屬性。</span><span class="sxs-lookup"><span data-stu-id="99e4a-112">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="99e4a-113">相反地，開發人員可以繼續依賴 **IAccessible** 來提供此功能，同時透過 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)新增對控制項特定屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="99e4a-113">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99e4a-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="99e4a-114">In this section</span></span>

-   [<span data-ttu-id="99e4a-115">IAccessibleEx 實施指導方針</span><span class="sxs-lookup"><span data-stu-id="99e4a-115">IAccessibleEx Implementation Guidelines</span></span>](iaccessibleex-implementation-guidelines.md)
-   [<span data-ttu-id="99e4a-116">為提供者執行 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="99e4a-116">Implementing IAccessibleEx for Providers</span></span>](implementing-iaccessibleex-for-providers.md)
-   [<span data-ttu-id="99e4a-117">從用戶端使用 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="99e4a-117">Using IAccessibleEx from a Client</span></span>](using-iaccessibleex-from-a-client.md)

## <a name="related-topics"></a><span data-ttu-id="99e4a-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="99e4a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99e4a-119">一般基礎結構</span><span class="sxs-lookup"><span data-stu-id="99e4a-119">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




