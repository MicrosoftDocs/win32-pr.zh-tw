---
title: CheckBox 控制項類型
description: 本主題提供 [CheckBox] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- 消費者介面自動化，CheckBox 控制項類型的支援
- 消費者介面自動化，CheckBox 控制項類型
- 消費者介面自動化，CheckBox 控制項類型的樹狀結構
- 消費者介面自動化，CheckBox 控制項類型的屬性
- 消費者介面自動化，CheckBox 控制項類型的控制項模式
- 消費者介面自動化，CheckBox 控制項類型的事件
- 樹狀結構，CheckBox 控制項類型
- 屬性，CheckBox 控制項類型
- 控制項模式，CheckBox 控制項類型
- 事件，CheckBox 控制項類型
- CheckBox 控制項類型的支援
- CheckBox 控制項類型
- CheckBox 控制項類型的控制項類型、樹狀結構
- 控制項類型，CheckBox 控制項類型的控制項模式
- 控制項類型，支援核取方塊
- 控制項類型，核取方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839968"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="4f349-119">CheckBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="4f349-119">CheckBox Control Type</span></span>

<span data-ttu-id="4f349-120">本主題提供 [ **CheckBox]** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4f349-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="4f349-121">核取方塊是用來表示狀態的物件，使用者可與之互動以循環狀態。</span><span class="sxs-lookup"><span data-stu-id="4f349-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="4f349-122">對使用者來說，核取方塊會顯示成二元 (是/否) 或 (開/關) 選項或三元 (開、關、未定) 選項。</span><span class="sxs-lookup"><span data-stu-id="4f349-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="4f349-123">下列章節會定義 **CheckBox** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="4f349-124">消費者介面自動化需求適用于所有核取方塊控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="4f349-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4f349-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="4f349-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4f349-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4f349-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4f349-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4f349-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4f349-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4f349-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4f349-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4f349-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4f349-130">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4f349-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="4f349-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f349-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4f349-132">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4f349-132">Typical Tree Structure</span></span>

<span data-ttu-id="4f349-133">下表描述的是與核取方塊控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="4f349-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4f349-134">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4f349-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4f349-135">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="4f349-135">Control View</span></span></th>
<th><span data-ttu-id="4f349-136">內容檢視</span><span class="sxs-lookup"><span data-stu-id="4f349-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4f349-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="4f349-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4f349-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="4f349-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4f349-139">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4f349-139">Relevant Properties</span></span>

<span data-ttu-id="4f349-140">下表列出消費者介面自動化屬性，其值或定義與 **CheckBox** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="4f349-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="4f349-141">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="4f349-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4f349-142">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="4f349-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4f349-143">值</span><span class="sxs-lookup"><span data-stu-id="4f349-143">Value</span></span>        | <span data-ttu-id="4f349-144">注意</span><span class="sxs-lookup"><span data-stu-id="4f349-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f349-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4f349-146">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-146">See notes.</span></span>   | <span data-ttu-id="4f349-147">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="4f349-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="4f349-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4f349-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-149">See notes.</span></span>   | <span data-ttu-id="4f349-150">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="4f349-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="4f349-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4f349-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-152">See notes.</span></span>   | <span data-ttu-id="4f349-153">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="4f349-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="4f349-154">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="4f349-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="4f349-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4f349-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="4f349-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4f349-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4f349-158">true</span><span class="sxs-lookup"><span data-stu-id="4f349-158">TRUE</span></span>         | <span data-ttu-id="4f349-159">這個屬性的值必須一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4f349-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="4f349-160">這表示核取方塊控制項必須一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="4f349-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="4f349-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4f349-162">true</span><span class="sxs-lookup"><span data-stu-id="4f349-162">TRUE</span></span>         | <span data-ttu-id="4f349-163">這個屬性的值必須一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="4f349-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="4f349-164">這表示核取方塊控制項必須一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="4f349-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="4f349-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4f349-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-166">See notes.</span></span>   | <span data-ttu-id="4f349-167">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="4f349-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="4f349-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4f349-169">Null</span><span class="sxs-lookup"><span data-stu-id="4f349-169">Null</span></span>         | <span data-ttu-id="4f349-170">核取方塊控制項為自我標記。</span><span class="sxs-lookup"><span data-stu-id="4f349-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4f349-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4f349-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-172">See notes.</span></span>   | <span data-ttu-id="4f349-173">對應至 **CheckBox** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="4f349-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="4f349-174">針對 en-us 或英文 (美國) ，預設值為 [核取方塊]。</span><span class="sxs-lookup"><span data-stu-id="4f349-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="4f349-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4f349-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4f349-176">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4f349-176">See notes.</span></span>   | <span data-ttu-id="4f349-177">核取方塊控制項的 [**IUIAutomationElement：： CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (或 [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) 屬性的值是在維持切換狀態的方塊旁邊顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="4f349-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4f349-178">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4f349-178">Required Control Patterns</span></span>

<span data-ttu-id="4f349-179">下表列出所有核取方塊控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4f349-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="4f349-180">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4f349-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4f349-181">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="4f349-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="4f349-182">支援/值</span><span class="sxs-lookup"><span data-stu-id="4f349-182">Support/Value</span></span> | <span data-ttu-id="4f349-183">備註</span><span class="sxs-lookup"><span data-stu-id="4f349-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f349-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="4f349-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="4f349-185">必要</span><span class="sxs-lookup"><span data-stu-id="4f349-185">Required</span></span>      | <span data-ttu-id="4f349-186">核取方塊支援 [切換](uiauto-implementingtoggle.md) 控制項模式，可讓您透過程式設計的方式，在其內部狀態中迴圈執行核取方塊。</span><span class="sxs-lookup"><span data-stu-id="4f349-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4f349-187">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4f349-187">Required Events</span></span>

<span data-ttu-id="4f349-188">下表列出支援的核取方塊控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="4f349-189">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="4f349-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4f349-190">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="4f349-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="4f349-191">備註</span><span class="sxs-lookup"><span data-stu-id="4f349-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f349-192">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4f349-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="4f349-193">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="4f349-194">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="4f349-195">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="4f349-196">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="4f349-197">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="4f349-198">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4f349-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="4f349-199">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4f349-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="4f349-200">DefaultAction</span><span class="sxs-lookup"><span data-stu-id="4f349-200">DefaultAction</span></span>

<span data-ttu-id="4f349-201">核取方塊的預設動作是使選項按鈕成為焦點，並切換其目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="4f349-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="4f349-202">如先前所述，核取方塊會顯示二進位 (Yes/No 或 On/Off) 決策給使用者，或第三 (On、Off、不定) 。</span><span class="sxs-lookup"><span data-stu-id="4f349-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="4f349-203">如果核取方塊是二元的，那麼預設動作就會讓「開」狀態變成「關」，或是「關」狀態變成「開」。</span><span class="sxs-lookup"><span data-stu-id="4f349-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="4f349-204">在第三個核取方塊中，預設動作會依相同順序迴圈查看核取方塊的狀態，就像使用者已傳送連續的滑鼠點給控制項一樣。</span><span class="sxs-lookup"><span data-stu-id="4f349-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f349-205">相關主題</span><span class="sxs-lookup"><span data-stu-id="4f349-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4f349-206">**概念**</span><span class="sxs-lookup"><span data-stu-id="4f349-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4f349-207">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="4f349-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4f349-208">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="4f349-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




