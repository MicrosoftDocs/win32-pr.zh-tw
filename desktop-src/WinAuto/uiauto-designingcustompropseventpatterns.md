---
title: 設計自訂屬性、事件和控制項模式
description: 自訂屬性、事件或控制項模式的設計應該適用于各種控制項的執行。
ms.assetid: e4b224a0-3958-4ae7-96cb-fe6dc16511a7
keywords:
- 消費者介面自動化，自訂屬性
- 消費者介面自動化，事件總覽
- 消費者介面自動化，控制項模式總覽
- 消費者介面自動化，設計自訂屬性
- 消費者介面自動化，設計事件
- 消費者介面自動化，設計控制項模式
- 消費者介面自動化、WinEvents
- 自訂屬性，設計
- 事件，設計
- 事件，WinEvents
- 控制項模式，設計
- WinEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e6973356fe6be922e73eef70e5107b6dcabe0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375432"
---
# <a name="design-custom-properties-events-and-control-patterns"></a><span data-ttu-id="3a047-115">設計自訂屬性、事件和控制項模式</span><span class="sxs-lookup"><span data-stu-id="3a047-115">Design custom properties, events, and control patterns</span></span>

<span data-ttu-id="3a047-116">自訂屬性、事件或控制項模式的設計應該適用于各種控制項的執行。</span><span class="sxs-lookup"><span data-stu-id="3a047-116">The design of a custom property, event, or control pattern should be useful in a wide variety of control implementations.</span></span> <span data-ttu-id="3a047-117">只有在有限案例中才有用的控制項或應用程式特定設計，應予以避免。</span><span class="sxs-lookup"><span data-stu-id="3a047-117">Control- or application-specific designs that are useful only in limited scenarios should be avoided.</span></span> <span data-ttu-id="3a047-118">設計應該遵循現有的 Microsoft 消費者介面自動化屬性、事件和控制項模式的範例，這些都是謹慎指定的，以符合各種協助工具和自動化測試應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="3a047-118">The design should follow the example of the existing Microsoft UI Automation properties, events, and control patterns, which were carefully specified to meet the needs of a wide variety of accessibility and automated testing applications.</span></span>

<span data-ttu-id="3a047-119">執行自訂屬性、事件或控制項模式的規格，牽涉到用戶端和提供者雙方雙方的合作與合約，同時要求雙方都能以一致的方式來執行規格。</span><span class="sxs-lookup"><span data-stu-id="3a047-119">Implementing the specification for a custom property, event, or control pattern involves the cooperation and agreement of parties on both the client and provider sides, and requires both parties to implement the specification consistently.</span></span> <span data-ttu-id="3a047-120">我們鼓勵公司與產業組織合作，例如 [協助工具互通性聯盟 (AIA) ](https://www.atia.org/) 來設計和發佈自訂屬性、事件或控制項模式的規格。</span><span class="sxs-lookup"><span data-stu-id="3a047-120">Companies are encouraged to work with industry organizations such as the [Accessibility Interoperability Alliance (AIA)](https://www.atia.org/) to design and publish the specification for the custom property, event, or control pattern.</span></span> <span data-ttu-id="3a047-121">如此一來，就可以達成共識，並確保可與最廣泛的應用程式交互操作。</span><span class="sxs-lookup"><span data-stu-id="3a047-121">In this way, consensus can be reached and interoperability with the widest variety of applications can be ensured.</span></span>

<span data-ttu-id="3a047-122">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="3a047-122">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="3a047-123">使用自訂屬性和事件的時機</span><span class="sxs-lookup"><span data-stu-id="3a047-123">When to Use Custom Properties and Events</span></span>](#when-to-use-custom-properties-and-events)
-   [<span data-ttu-id="3a047-124">設計自訂屬性</span><span class="sxs-lookup"><span data-stu-id="3a047-124">Designing Custom Properties</span></span>](#designing-custom-properties)
-   [<span data-ttu-id="3a047-125">設計自訂事件</span><span class="sxs-lookup"><span data-stu-id="3a047-125">Designing Custom Events</span></span>](#designing-custom-events)
    -   [<span data-ttu-id="3a047-126">自訂消費者介面自動化事件和 WinEvents</span><span class="sxs-lookup"><span data-stu-id="3a047-126">Custom UI Automation Events and WinEvents</span></span>](#custom-ui-automation-events-and-winevents)
-   [<span data-ttu-id="3a047-127">設計自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="3a047-127">Designing Custom Control Patterns</span></span>](#designing-custom-control-patterns)
-   [<span data-ttu-id="3a047-128">自訂控制項類型</span><span class="sxs-lookup"><span data-stu-id="3a047-128">Custom Control Types</span></span>](#custom-control-types)
-   [<span data-ttu-id="3a047-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a047-129">Related topics</span></span>](#related-topics)

## <a name="when-to-use-custom-properties-and-events"></a><span data-ttu-id="3a047-130">使用自訂屬性和事件的時機</span><span class="sxs-lookup"><span data-stu-id="3a047-130">When to Use Custom Properties and Events</span></span>

<span data-ttu-id="3a047-131">在建立自訂屬性、事件或控制項模式之前，請確定消費者介面自動化不會提供現有的方案。</span><span class="sxs-lookup"><span data-stu-id="3a047-131">Before creating a custom property, event, or control pattern, make sure that UI Automation does not provide an existing solution.</span></span> <span data-ttu-id="3a047-132">例如，您不需要建立自訂的「Click」控制項模式，因為叫 [用控制項模式](uiauto-implementinginvoke.md) 已經描述該功能。</span><span class="sxs-lookup"><span data-stu-id="3a047-132">For example, creating a custom "Click" control pattern is not necessary because the [Invoke](uiauto-implementinginvoke.md) control pattern already describes that functionality.</span></span>

<span data-ttu-id="3a047-133">如果您決定需要自訂的屬性、事件或控制項模式，請確定它不太清楚或不是泛型。</span><span class="sxs-lookup"><span data-stu-id="3a047-133">If you decide that a custom property, event, or control pattern is needed, make sure that it is not too vague or generic.</span></span> <span data-ttu-id="3a047-134">例如，名為 "Show" 的控制項模式並不實用，因為控制項的可見度可由專案上的 availability 屬性指出，例如 [**UIA \_ IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) 或 [**UIA \_ IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md)。</span><span class="sxs-lookup"><span data-stu-id="3a047-134">For example, a control pattern called "Show" is not useful because the visibility of a control can be indicated by an availability property on the element, such as [**UIA\_IsExpandCollapsePatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) or [**UIA\_IsScrollItemPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md).</span></span>

<span data-ttu-id="3a047-135">在執行自訂解決方案之前，請仔細確認是否需要，然後完全設計功能。</span><span class="sxs-lookup"><span data-stu-id="3a047-135">Before implementing a custom solution, carefully confirm it is needed and then design the functionality completely.</span></span>

## <a name="designing-custom-properties"></a><span data-ttu-id="3a047-136">設計自訂屬性</span><span class="sxs-lookup"><span data-stu-id="3a047-136">Designing Custom Properties</span></span>

<span data-ttu-id="3a047-137">消費者介面自動化包含兩種基本類型的屬性： Automation 元素屬性和控制項模式屬性。</span><span class="sxs-lookup"><span data-stu-id="3a047-137">UI Automation includes two basic types of properties: automation element properties, and control pattern properties.</span></span> <span data-ttu-id="3a047-138">Automation 元素屬性是由所有消費者介面自動化專案所公開的一組通用屬性（例如 Name、AcceleratorKey 和 ClassName）所組成，不論控制項型別為何。</span><span class="sxs-lookup"><span data-stu-id="3a047-138">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="3a047-139">控制項模式屬性是由控制項透過特定的控制項模式公開。</span><span class="sxs-lookup"><span data-stu-id="3a047-139">Control pattern properties are exposed by a control through a particular control pattern.</span></span> <span data-ttu-id="3a047-140">每個控制項模式都有一組對應的控制項模式屬性，控制項必須公開這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3a047-140">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="3a047-141">例如，支援 [方格](uiauto-implementinggrid.md) 控制項模式的控制項會公開 ColumnCount 和 RowCount 屬性。</span><span class="sxs-lookup"><span data-stu-id="3a047-141">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span>

<span data-ttu-id="3a047-142">自訂 automation 元素屬性或控制項模式屬性應遵守下列設計指導方針：</span><span class="sxs-lookup"><span data-stu-id="3a047-142">A custom automation element property or control pattern property should adhere to the following design guidelines:</span></span>

-   <span data-ttu-id="3a047-143">自訂屬性必須有 [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) 列舉所指定的下列其中一種資料類型。</span><span class="sxs-lookup"><span data-stu-id="3a047-143">A custom property must have one of the following data types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="3a047-144">自訂屬性不支援其他資料類型。</span><span class="sxs-lookup"><span data-stu-id="3a047-144">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="3a047-145">**UIAutomationType \_ Bool**</span><span class="sxs-lookup"><span data-stu-id="3a047-145">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="3a047-146">**UIAutomationType \_ Double**</span><span class="sxs-lookup"><span data-stu-id="3a047-146">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="3a047-147">**UIAutomationType \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="3a047-147">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="3a047-148">**UIAutomationType \_ Int**</span><span class="sxs-lookup"><span data-stu-id="3a047-148">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="3a047-149">**UIAutomationType \_ 點**</span><span class="sxs-lookup"><span data-stu-id="3a047-149">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="3a047-150">**UIAutomationType \_ 字串**</span><span class="sxs-lookup"><span data-stu-id="3a047-150">**UIAutomationType\_String**</span></span>
-   <span data-ttu-id="3a047-151">如果自訂屬性包含字串資料 ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)) ，此規格必須指出屬性是否可當地語系化 (也就是字串是否可以轉譯成不同的 UI 語言) 。</span><span class="sxs-lookup"><span data-stu-id="3a047-151">If the custom property contains string data ([**BSTR**](/previous-versions/windows/desktop/automat/bstr)), the specification must state whether the property is localizable (that is, whether the string can be translated into different UI languages).</span></span>
-   <span data-ttu-id="3a047-152">自訂屬性不應與現有屬性的特性或功能重迭。</span><span class="sxs-lookup"><span data-stu-id="3a047-152">The custom property should not overlap with the features or functionality of existing properties.</span></span>

## <a name="designing-custom-events"></a><span data-ttu-id="3a047-153">設計自訂事件</span><span class="sxs-lookup"><span data-stu-id="3a047-153">Designing Custom Events</span></span>

<span data-ttu-id="3a047-154">應用程式會使用消費者介面自動化事件通知，來回應涉及 UI 專案的變更和動作。</span><span class="sxs-lookup"><span data-stu-id="3a047-154">Applications use UI Automation event notifications to respond to changes and actions involving UI items.</span></span> <span data-ttu-id="3a047-155">大部分屬性都有相關聯的屬性變更事件，這些事件會在屬性值變更時引發消費者介面自動化引發。</span><span class="sxs-lookup"><span data-stu-id="3a047-155">Most properties have associated property-changed events that UI Automation raises when the value of the property changes.</span></span> <span data-ttu-id="3a047-156">如果您引進自訂屬性，您應該考慮引入任何可能也需要的對應自訂事件。</span><span class="sxs-lookup"><span data-stu-id="3a047-156">If you introduce a custom property, you should consider introducing any corresponding custom events that may also be needed.</span></span>

<span data-ttu-id="3a047-157">自訂事件應遵守下列設計指導方針：</span><span class="sxs-lookup"><span data-stu-id="3a047-157">A custom event should adhere to the following design guidelines:</span></span>

-   <span data-ttu-id="3a047-158">自訂事件必須是「無狀態」。</span><span class="sxs-lookup"><span data-stu-id="3a047-158">The custom event must be "stateless."</span></span> <span data-ttu-id="3a047-159">它不能與特定屬性或值產生關聯。</span><span class="sxs-lookup"><span data-stu-id="3a047-159">It cannot be associated with a specific property or value.</span></span>
-   <span data-ttu-id="3a047-160">自訂事件不應與任何現有事件的定義或角色重迭。</span><span class="sxs-lookup"><span data-stu-id="3a047-160">The custom event should not overlap with the definition or role of any existing event.</span></span>

### <a name="custom-ui-automation-events-and-winevents"></a><span data-ttu-id="3a047-161">自訂消費者介面自動化事件和 WinEvents</span><span class="sxs-lookup"><span data-stu-id="3a047-161">Custom UI Automation Events and WinEvents</span></span>

<span data-ttu-id="3a047-162">[WinEvents](winevents-infrastructure.md) 在 Microsoft Windows 平臺中是一個有用的處理序間通訊和事件機制。</span><span class="sxs-lookup"><span data-stu-id="3a047-162">[WinEvents](winevents-infrastructure.md) are a useful interprocess communication and eventing mechanism in the Microsoft Windows platform.</span></span> <span data-ttu-id="3a047-163">不過，引入新的 New-winevent 識別碼會有風險，因為這可能會導致與其他應用程式或作業系統發生衝突，導致系統變得不穩定。</span><span class="sxs-lookup"><span data-stu-id="3a047-163">However, introducing a new WinEvent ID is risky because it can cause collisions with other applications or the operating system, resulting in the system becoming unstable.</span></span> <span data-ttu-id="3a047-164">為了避免衝突，Microsoft 定義了數種不同的 WinEvents 類別，每個類別目錄都定義了一或多個範圍的值，以做為 New-winevent 識別碼使用。</span><span class="sxs-lookup"><span data-stu-id="3a047-164">To avoid collisions, Microsoft has defined several different categories of WinEvents and, for each category, has defined one or more ranges of values for use as WinEvent IDs.</span></span> <span data-ttu-id="3a047-165">如需詳細資訊，請參閱 [配置 New-winevent 識別碼](allocation-of-winevent-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="3a047-165">For more information, see [Allocation of WinEvent IDs](allocation-of-winevent-ids.md).</span></span>

<span data-ttu-id="3a047-166">自訂消費者介面自動化事件會藉由在消費者介面自動化架構內部配置事件識別碼，來避免發生衝突。</span><span class="sxs-lookup"><span data-stu-id="3a047-166">Custom UI Automation events avoid conflicts by allocating the event ID internally in the UI Automation framework.</span></span>

## <a name="designing-custom-control-patterns"></a><span data-ttu-id="3a047-167">設計自訂控制項模式</span><span class="sxs-lookup"><span data-stu-id="3a047-167">Designing Custom Control Patterns</span></span>

<span data-ttu-id="3a047-168">控制項模式是具有屬性、方法和事件的介面，這些屬性定義了可從 automation 元素使用的離散功能。</span><span class="sxs-lookup"><span data-stu-id="3a047-168">A control pattern is an interface with properties, methods, and events that define a discrete piece of functionality available from an automation element.</span></span> <span data-ttu-id="3a047-169">控制項模式方法可讓消費者介面自動化用戶端操作控制項的特定層面。</span><span class="sxs-lookup"><span data-stu-id="3a047-169">Control pattern methods allow UI Automation clients to manipulate a particular aspect of the control.</span></span> <span data-ttu-id="3a047-170">控制項模式屬性和事件提供有關控制項某些方面的資訊，並提供可執行控制項模式之 automation 元素狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3a047-170">The control pattern properties and events provide information about some aspect of the control, and provide information about the state of the automation element that implements the control pattern.</span></span>

<span data-ttu-id="3a047-171">自訂控制項模式應遵守下列設計指導方針：</span><span class="sxs-lookup"><span data-stu-id="3a047-171">A custom control pattern should adhere to the following design guidelines:</span></span>

-   <span data-ttu-id="3a047-172">自訂控制項模式應該涵蓋特定案例。</span><span class="sxs-lookup"><span data-stu-id="3a047-172">A custom control pattern should cover a particular scenario.</span></span> <span data-ttu-id="3a047-173">例如， [>itemcontainer](uiauto-implementingitemcontainer.md) 控制項模式的目的是要查詢包含的物件（不論虛擬化狀態為何），但不會列舉或計算所包含的物件。</span><span class="sxs-lookup"><span data-stu-id="3a047-173">For example, the [ItemContainer](uiauto-implementingitemcontainer.md) control pattern is intended for querying a contained object regardless of the virtualization state, but it does not enumerate or count the contained objects.</span></span>
-   <span data-ttu-id="3a047-174">自訂控制項模式不應與現有控制項模式的功能重迭。</span><span class="sxs-lookup"><span data-stu-id="3a047-174">A custom control pattern should not overlap with the features of existing control patterns.</span></span> <span data-ttu-id="3a047-175">例如，[叫用] 和 [ [ExpandCollapse](uiauto-implementingexpandcollapse.md) ] 控制項模式不應結合[，並以](uiauto-implementinginvoke.md)新的控制項模式呈現。</span><span class="sxs-lookup"><span data-stu-id="3a047-175">For example, the [Invoke](uiauto-implementinginvoke.md) and [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns should not be combined and presented as a new control pattern.</span></span> <span data-ttu-id="3a047-176">請重複使用現有的控制項模式，或使用新的控制項模式來定義獨特的情節。</span><span class="sxs-lookup"><span data-stu-id="3a047-176">Either reuse existing control patterns or define unique scenarios with new control patterns.</span></span>
-   <span data-ttu-id="3a047-177">多個自訂控制項模式可以一起設計，以支援複雜的案例。</span><span class="sxs-lookup"><span data-stu-id="3a047-177">Multiple custom control patterns can be designed together to support complex scenarios.</span></span> <span data-ttu-id="3a047-178">例如， [選取專案](uiauto-implementingselection.md) 和 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式會一起運作，以支援一般物件選取案例。</span><span class="sxs-lookup"><span data-stu-id="3a047-178">For example, the [Selection](uiauto-implementingselection.md) and [SelectionItem](uiauto-implementingselectionitem.md) control patterns work together to support general object selection scenarios.</span></span>

## <a name="custom-control-types"></a><span data-ttu-id="3a047-179">自訂控制項類型</span><span class="sxs-lookup"><span data-stu-id="3a047-179">Custom Control Types</span></span>

<span data-ttu-id="3a047-180">雖然本主題的重點在於如何註冊自訂消費者介面自動化屬性、事件和控制項模式，但是也可以引進新的控制項類型。</span><span class="sxs-lookup"><span data-stu-id="3a047-180">Although this topic focuses on how to register custom UI Automation properties, events, and control patterns, it is also possible to introduce new control types.</span></span> <span data-ttu-id="3a047-181">和自訂屬性、事件和控制項模式不同的是，自訂控制項類型無法在執行時間以程式設計方式註冊，因為它其實只是消費者介面自動化 ControlType 屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="3a047-181">Unlike custom properties, events, and control patterns, a custom control type cannot be registered programmatically at runtime because it is actually just a potential value of the UI Automation ControlType property.</span></span> <span data-ttu-id="3a047-182">不過，您可以定義、發佈自訂控制項類型識別碼，並可讓其他用戶端和提供者使用。</span><span class="sxs-lookup"><span data-stu-id="3a047-182">However, a custom control type ID can be defined, published, and made available for other clients and providers to use.</span></span> <span data-ttu-id="3a047-183">如需控制項類型的詳細資訊，請參閱 [消費者介面自動化控制項類型總覽](uiauto-controltypesoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="3a047-183">For more information about control types, see [UI Automation Control Types Overview](uiauto-controltypesoverview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a047-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="3a047-184">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3a047-185">**概念**</span><span class="sxs-lookup"><span data-stu-id="3a047-185">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3a047-186">註冊自訂屬性、事件和控制項模式</span><span class="sxs-lookup"><span data-stu-id="3a047-186">Registering Custom Properties, Events, and Control Patterns</span></span>](uiauto-regcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="3a047-187">UI 自動化屬性概觀</span><span class="sxs-lookup"><span data-stu-id="3a047-187">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="3a047-188">UI 自動化事件概觀</span><span class="sxs-lookup"><span data-stu-id="3a047-188">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="3a047-189">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="3a047-189">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 