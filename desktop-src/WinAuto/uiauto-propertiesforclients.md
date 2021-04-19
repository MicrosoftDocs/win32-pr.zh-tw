---
title: 從消費者介面自動化元素抓取屬性
description: IUIAutomationElement 物件上的屬性包含 UI 元素的相關資訊，通常是控制項。
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- 用戶端，取得消費者介面自動化元素
- 用戶端，消費者介面自動化元素
- 用戶端，屬性
- 用戶端，正在抓取屬性
- 用戶端，消費者介面自動化屬性
- 消費者介面自動化，取得元素
- 消費者介面自動化，元素
- 消費者介面自動化，屬性
- 消費者介面自動化，正在抓取屬性
- 正在抓取屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106996565"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="6fe1e-113">從消費者介面自動化元素抓取屬性</span><span class="sxs-lookup"><span data-stu-id="6fe1e-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="6fe1e-114">[**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement)物件上的屬性包含 UI 元素的相關資訊，通常是控制項。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="6fe1e-115">元素的屬性為泛型;亦即，不是控制項類型的特定。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="6fe1e-116">專案的控制項特定屬性是由其控制項模式介面所公開。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="6fe1e-117">Microsoft 消費者介面自動化屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="6fe1e-118">若要設定控制項的屬性，您必須使用適當控制項模式的方法。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="6fe1e-119">例如，使用 [**IUIAutomationScrollPattern：： Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) 來變更滾動視窗的位置值。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="6fe1e-120">若要改善效能，您可以在抓取專案時快取控制項和控制項模式的屬性值。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="6fe1e-121">如需詳細資訊，請參閱快取 [消費者介面自動化屬性和控制項模式](uiauto-cachingforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="6fe1e-122">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6fe1e-123">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="6fe1e-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="6fe1e-124">屬性條件</span><span class="sxs-lookup"><span data-stu-id="6fe1e-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="6fe1e-125">擷取屬性</span><span class="sxs-lookup"><span data-stu-id="6fe1e-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="6fe1e-126">預設屬性值</span><span class="sxs-lookup"><span data-stu-id="6fe1e-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="6fe1e-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fe1e-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="6fe1e-128">屬性識別碼</span><span class="sxs-lookup"><span data-stu-id="6fe1e-128">Property IDs</span></span>

<span data-ttu-id="6fe1e-129">屬性識別碼是在 Uiautomationclient.dll 中定義。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="6fe1e-130">當您訂閱屬性變更的事件、抓取屬性值和結構屬性條件時，會使用這些屬性來指定屬性。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="6fe1e-131">屬性識別碼也會識別在呼叫 [**IUIAutomationPropertyChangedEventHandler：： HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) 時已變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="6fe1e-132">如需消費者介面自動化屬性識別碼的清單，請參閱 [屬性識別碼](uiauto-entry-propids.md)。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="6fe1e-133">屬性條件</span><span class="sxs-lookup"><span data-stu-id="6fe1e-133">Property Conditions</span></span>

<span data-ttu-id="6fe1e-134">屬性識別碼是用來建立用來尋找消費者介面自動化元素的 [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) 物件。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="6fe1e-135">例如，您可能想要尋找具有特定名稱或已啟用之所有控制項的元素。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="6fe1e-136">每個屬性條件都會指定屬性識別碼和屬性必須符合的值。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="6fe1e-137">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="6fe1e-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="6fe1e-138">**IUIAutomation::CreatePropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="6fe1e-139">**IUIAutomation::CreatePropertyConditionEx**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="6fe1e-140">**IUIAutomationElement：： FindFirst**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="6fe1e-141">**IUIAutomationElement：： FindAll**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="6fe1e-142">擷取屬性</span><span class="sxs-lookup"><span data-stu-id="6fe1e-142">Retrieving Properties</span></span>

<span data-ttu-id="6fe1e-143">有些泛型屬性（以及所有控制項模式屬性）可做為 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 或控制項模式介面上的屬性，而且可以使用存取子來抓取，例如 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) 或 [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition)。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="6fe1e-144">此外，您可以使用下列其中一種方法來抓取控制項模式屬性以外的任何目前或快取屬性 () ：</span><span class="sxs-lookup"><span data-stu-id="6fe1e-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="6fe1e-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="6fe1e-146">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="6fe1e-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="6fe1e-148">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="6fe1e-149">這些方法可提供更佳的效能，並可存取完整的屬性範圍。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="6fe1e-150">不過，值會在 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 結構中傳回，而個別的屬性存取子則會將值轉換成適當的類型。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="6fe1e-151">預設屬性值</span><span class="sxs-lookup"><span data-stu-id="6fe1e-151">Default Property Values</span></span>

<span data-ttu-id="6fe1e-152">如果消費者介面自動化提供者不會執行屬性，消費者介面自動化可以提供預設值。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="6fe1e-153">例如，如果控制項的提供者不支援 [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)所識別的屬性，消費者介面自動化會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="6fe1e-154">同樣地，如果提供者不支援 [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md)所識別的屬性，消費者介面自動化會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="6fe1e-155">[**IUIAutomationElement：： GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)與 [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (之間，以及類似的方法組之間的差異) 是 "Ex" 方法可以指定不傳回預設值。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="6fe1e-156">在此情況下，傳回值是特殊的唯一常數，表示不支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="6fe1e-157">收到此值時，應用程式可以提供自己的值，或直接忽略屬性。</span><span class="sxs-lookup"><span data-stu-id="6fe1e-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fe1e-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="6fe1e-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6fe1e-159">**概念**</span><span class="sxs-lookup"><span data-stu-id="6fe1e-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6fe1e-160">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="6fe1e-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="6fe1e-161">屬性識別項</span><span class="sxs-lookup"><span data-stu-id="6fe1e-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 