---
title: UI 自動化屬性概觀
description: Microsoft 消費者介面自動化提供者會公開消費者介面自動化元素上的屬性。 屬性可讓用戶端應用程式抓取控制項的相關資訊。
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- 消費者介面自動化，屬性總覽
- 消費者介面自動化、屬性與事件的比較
- 消費者介面自動化、事件與屬性的比較
- 屬性，關於
- 屬性，識別碼
- 屬性、值
- 屬性、事件
- 事件，屬性
- 屬性，動態
- 動態屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182938"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="88047-114">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="88047-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="88047-115">Microsoft 消費者介面自動化提供者會公開消費者介面自動化元素上的屬性。</span><span class="sxs-lookup"><span data-stu-id="88047-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="88047-116">屬性可讓用戶端應用程式抓取控制項的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="88047-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="88047-117">消費者介面自動化會公開兩種不同的屬性： *Automation 元素屬性* 和 *控制項模式 propertes*。</span><span class="sxs-lookup"><span data-stu-id="88047-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="88047-118">Automation 元素屬性是由所有消費者介面自動化專案所公開的一組通用屬性（例如 Name、AcceleratorKey 和 ClassName）所組成，不論控制項型別為何。</span><span class="sxs-lookup"><span data-stu-id="88047-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="88047-119">大部分 automation 元素屬性都是靜態值。</span><span class="sxs-lookup"><span data-stu-id="88047-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="88047-120">控制項模式屬性是由支援特定控制項模式的控制項所公開的屬性。</span><span class="sxs-lookup"><span data-stu-id="88047-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="88047-121">每個控制項模式都有一組對應的控制項模式屬性，控制項必須公開這些屬性。</span><span class="sxs-lookup"><span data-stu-id="88047-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="88047-122">例如，支援 [方格](uiauto-implementinggrid.md) 控制項模式的控制項會公開 ColumnCount 和 RowCount 屬性。</span><span class="sxs-lookup"><span data-stu-id="88047-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="88047-123">大部分的控制項模式屬性都是動態值。</span><span class="sxs-lookup"><span data-stu-id="88047-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="88047-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="88047-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="88047-125">屬性識別項</span><span class="sxs-lookup"><span data-stu-id="88047-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="88047-126">屬性值</span><span class="sxs-lookup"><span data-stu-id="88047-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="88047-127">屬性和事件</span><span class="sxs-lookup"><span data-stu-id="88047-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="88047-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="88047-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="88047-129">屬性識別項</span><span class="sxs-lookup"><span data-stu-id="88047-129">Property Identifiers</span></span>

<span data-ttu-id="88047-130">每個屬性都是由稱為 *屬性識別碼* (識別碼) 的 **PROPERTYID** 數值來識別。</span><span class="sxs-lookup"><span data-stu-id="88047-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="88047-131">提供者和用戶端會在方法呼叫（例如 [**IRawElementProviderAdviseEvents：： AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) 和 [**IUIAutomationElement：： GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) ）中使用數值識別碼，以識別屬性要求。</span><span class="sxs-lookup"><span data-stu-id="88047-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="88047-132">如需每個消費者介面自動化屬性識別碼的詳細說明，包括每個屬性的資料類型和預設值，請參閱 [屬性識別碼](uiauto-entry-propids.md)。</span><span class="sxs-lookup"><span data-stu-id="88047-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="88047-133">屬性值</span><span class="sxs-lookup"><span data-stu-id="88047-133">Property Values</span></span>

<span data-ttu-id="88047-134">所有屬性都是唯讀的，不過某些屬性可以使用對控制項採取的方法來變更，例如 [**IDockProvider：： SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) 或 [**IUIAutomationDockPattern：： SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (用戶端) 。</span><span class="sxs-lookup"><span data-stu-id="88047-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="88047-135">如需有關如何抓取屬性值的詳細資訊，請參閱 [從消費者介面自動化元素抓取屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="88047-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="88047-136">屬性和事件</span><span class="sxs-lookup"><span data-stu-id="88047-136">Properties and Events</span></span>

<span data-ttu-id="88047-137">與消費者介面自動化中的屬性緊密相關聯，是 *屬性變更事件* 的概念。</span><span class="sxs-lookup"><span data-stu-id="88047-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="88047-138">若為動態屬性，用戶端應用程式需要一種方法來知道屬性值已變更，以便它可以更新其資訊的快取，或以其他方式回應新的資訊。</span><span class="sxs-lookup"><span data-stu-id="88047-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="88047-139">用戶端可以註冊來接聽任何屬性的屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="88047-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="88047-140">當 UI 中的某些內容變更時，提供者會引發事件。</span><span class="sxs-lookup"><span data-stu-id="88047-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="88047-141">例如，如果選取或清除核取方塊，則會由 [切換](uiauto-implementingtoggle.md) 控制項模式的提供者執行來引發屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="88047-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="88047-142">提供者可以視任何用戶端是否正在接聽事件或接聽特定事件，以選擇性地引發事件。</span><span class="sxs-lookup"><span data-stu-id="88047-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="88047-143">並非所有屬性變更都會引發事件，這完全由項目的使用者介面自動化提供者實作所決定。</span><span class="sxs-lookup"><span data-stu-id="88047-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="88047-144">例如，清單方塊的標準 proxy 提供者不會在選取專案屬性變更時引發屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="88047-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="88047-145">在此情況下，應用程式必須接聽選取範圍變更 ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) 時引發的事件。</span><span class="sxs-lookup"><span data-stu-id="88047-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="88047-146">用戶端會藉由訂閱事件來接聽事件，如 [訂閱消費者介面自動化事件](uiauto-eventsforclients.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="88047-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="88047-147">針對屬性變更的事件，用戶端必須執行 [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) 並將介面傳遞至 [**IUIAutomation：： AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) 或 [**IUIAutomation：： AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray)。</span><span class="sxs-lookup"><span data-stu-id="88047-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="88047-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="88047-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="88047-149">**參考**</span><span class="sxs-lookup"><span data-stu-id="88047-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88047-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="88047-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="88047-151">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="88047-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="88047-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="88047-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="88047-153">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="88047-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="88047-154">**概念**</span><span class="sxs-lookup"><span data-stu-id="88047-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="88047-155">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="88047-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="88047-156">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="88047-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="88047-157">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="88047-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




