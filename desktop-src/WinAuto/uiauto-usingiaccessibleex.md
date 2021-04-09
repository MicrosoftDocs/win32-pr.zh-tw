---
title: 將消費者介面自動化功能新增至 Active Accessibility 伺服器
description: 沒有 Microsoft 消費者介面自動化提供者，但可執行 IAccessible 的控制項，可以透過執行 IAccessibleEx 介面，輕鬆地升級以提供某些消費者介面自動化功能。
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- 消費者介面自動化，Active Accessibility 伺服器
- 消費者介面自動化，Microsoft Active Accessibility 伺服器
- 消費者介面自動化、IAccessible
- 消費者介面自動化、IAccessibleEx
- 消費者介面自動化，公開 IAccessibleEx
- 消費者介面自動化，執行 IAccessibleEx
- IAccessible
- IAccessibleEx
- Microsoft Active Accessibility
- Active Accessibility
- 公開 IAccessibleEx
- 執行 IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933295"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="1ed0d-115">將消費者介面自動化功能新增至 Active Accessibility 伺服器</span><span class="sxs-lookup"><span data-stu-id="1ed0d-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="1ed0d-116">沒有 Microsoft 消費者介面自動化提供者，但可執行 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 的控制項，可以透過執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面，輕鬆地升級以提供某些消費者介面自動化功能。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="1ed0d-117">這個介面可讓控制項公開消費者介面自動化屬性和控制項模式，而不需要完整地執行消費者介面自動化提供者介面（例如 [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment)）。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="1ed0d-118">若要執行 **IAccessibleEx**，基準 Microsoft Active Accessibility 物件階層必須不包含任何錯誤或不一致的 (例如，父物件的父物件不會將它列為子) ，且不能與消費者介面自動化規格衝突。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="1ed0d-119">如果 Microsoft Active Accessibility 的物件階層符合這些需求，則這是使用 **IAccessibleEx** 來新增功能的絕佳候選。否則，您必須單獨或 Microsoft Active Accessibility 執行來執行消費者介面自動化。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="1ed0d-120">採用具有範圍值的自訂控制項案例。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="1ed0d-121">控制項的 Microsoft Active Accessibility 伺服器會定義其角色，而且能夠傳回其目前值，但缺少傳回控制項最小值和最大值的方法，因為這些屬性未在 Microsoft Active Accessibility 中定義。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="1ed0d-122">消費者介面自動化的用戶端能夠取得控制項的角色、目前的值和其他 Microsoft Active Accessibility 屬性，因為消費者介面自動化 core 可以透過 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)取得這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="1ed0d-123">但是，若沒有物件的 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) 介面存取權，消費者介面自動化也無法取得最大值和最小值。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="1ed0d-124">控制項開發人員可以為控制項提供完整的消費者介面自動化提供者，但這表示複製了許多現有的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 執行功能：例如，導覽和通用屬性。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="1ed0d-125">相反地，開發人員可以繼續依賴 **IAccessible** 來提供此功能，同時透過 [**system.windows.automation.provider.irangevalueprovider>**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)新增對控制項特定屬性的支援。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="1ed0d-126">更新自訂控制項需要下列主要步驟：</span><span class="sxs-lookup"><span data-stu-id="1ed0d-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="1ed0d-127">在可存取的物件上執行 [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) ，以便在這個或個別的物件上找到 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 介面。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="1ed0d-128">在可存取的物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="1ed0d-129">針對任何 Microsoft Active Accessibility 子專案建立相異的可存取物件，Microsoft Active Accessibility 可能已在父物件上以 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面表示 (例如，) 清單專案。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="1ed0d-130">在這些物件上執行 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="1ed0d-131">在所有可存取的物件上執行 [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) 。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="1ed0d-132">在可存取的物件上，執行適當的控制項模式介面。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="1ed0d-133">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1ed0d-134">公開 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1ed0d-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="1ed0d-135">執行 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1ed0d-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="1ed0d-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ed0d-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="1ed0d-137">公開 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1ed0d-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="1ed0d-138">由於控制項的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 執行可能位於不同的物件中，因此用戶端應用程式無法依賴 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="1ed0d-139">相反地，用戶端應該呼叫 [**IServiceProvider：： QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="1ed0d-140">在這個方法的下列範例中，假設 **IAccessibleEx** 不是在另一個物件上執行;因此，此方法只會對 **QueryInterface** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="1ed0d-141">執行 IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="1ed0d-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="1ed0d-142">最感興趣的 [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) 方法為 [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="1ed0d-143">此方法可讓 Microsoft Active Accessibility 伺服器有機會建立可存取的物件， (一個公開的子專案 **IAccessibleEx**) 。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="1ed0d-144">在 Microsoft Active Accessibility 中，子專案通常不會表示為可存取的物件，而是可存取物件的子系。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="1ed0d-145">不過，因為消費者介面自動化要求每個專案都以個別的可存取物件來表示，所以 **GetObjectForChild** 必須為每個子系視需要建立個別的物件。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="1ed0d-146">下列範例執行會傳回自訂清單視圖中專案的可存取物件。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="1ed0d-147">如需完整的範例執行，請參閱 [讓自訂控制項可供存取，第5部分：使用 IAccessibleEx 將消費者介面自動化支援新增至 MSDN 上的自訂控制項](/previous-versions/msdn10/cc307850(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="1ed0d-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ed0d-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="1ed0d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ed0d-149">消費者介面自動化提供者程式設計人員指南</span><span class="sxs-lookup"><span data-stu-id="1ed0d-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 