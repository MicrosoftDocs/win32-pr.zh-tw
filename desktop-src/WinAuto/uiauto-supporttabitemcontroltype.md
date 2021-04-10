---
title: TabItem 控制項類型
description: 本主題提供 TabItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- 消費者介面自動化，TabItem 控制項類型的支援
- 消費者介面自動化，TabItem 控制項類型
- 消費者介面自動化，TabItem 控制項類型的樹狀結構
- 消費者介面自動化，TabItem 控制項類型的屬性
- 消費者介面自動化，TabItem 控制項類型的控制項模式
- 消費者介面自動化，TabItem 控制項類型的事件
- 樹狀結構，TabItem 控制項類型
- properties、TabItem 控制項類型
- 控制項模式，TabItem 控制項類型
- events、TabItem 控制項類型
- TabItem 控制項類型的支援
- TabItem 控制項類型
- 控制項類型，TabItem 控制項類型的樹狀結構
- 控制項類型，TabItem 控制項類型的控制項模式
- 控制項類型，支援 TabItem
- 控制項類型，TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183938"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="d6220-119">TabItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="d6220-119">TabItem Control Type</span></span>

<span data-ttu-id="d6220-120">本主題提供 **TabItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d6220-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="d6220-121">索引標籤項目控制項是做為索引標籤控制項內的控制項，可選取要顯示在視窗中的特定頁面。</span><span class="sxs-lookup"><span data-stu-id="d6220-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="d6220-122">下列章節會定義 **TabItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="d6220-123">消費者介面自動化需求適用于所有的索引標籤專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="d6220-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d6220-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d6220-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d6220-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d6220-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d6220-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="d6220-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d6220-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="d6220-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d6220-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="d6220-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d6220-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6220-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d6220-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d6220-130">Typical Tree Structure</span></span>

<span data-ttu-id="d6220-131">下表描述的是與索引標籤專案控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="d6220-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d6220-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d6220-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d6220-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="d6220-133">Control View</span></span></th>
<th><span data-ttu-id="d6220-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="d6220-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d6220-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="d6220-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="d6220-136">Image (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="d6220-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="d6220-137">Text</span><span class="sxs-lookup"><span data-stu-id="d6220-137">Text</span></span></li>
<li><span data-ttu-id="d6220-138">窗格</span><span class="sxs-lookup"><span data-stu-id="d6220-138">Pane</span></span>
<ul>
<li><span data-ttu-id="d6220-139">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="d6220-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d6220-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="d6220-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="d6220-141">窗格</span><span class="sxs-lookup"><span data-stu-id="d6220-141">Pane</span></span>
<ul>
<li><span data-ttu-id="d6220-142">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="d6220-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="d6220-143">相關屬性</span><span class="sxs-lookup"><span data-stu-id="d6220-143">Relevant Properties</span></span>

<span data-ttu-id="d6220-144">下表列出消費者介面自動化屬性，其值或定義與 **TabItem** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="d6220-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="d6220-145">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="d6220-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d6220-146">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="d6220-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d6220-147">值</span><span class="sxs-lookup"><span data-stu-id="d6220-147">Value</span></span>       | <span data-ttu-id="d6220-148">注意</span><span class="sxs-lookup"><span data-stu-id="d6220-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6220-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d6220-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-150">See notes.</span></span>  | <span data-ttu-id="d6220-151">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d6220-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="d6220-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d6220-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-153">See notes.</span></span>  | <span data-ttu-id="d6220-154">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="d6220-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="d6220-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d6220-156">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-156">See notes.</span></span>  | <span data-ttu-id="d6220-157">索引標籤項目控制項必須具有能讓項目成為選取項目的可點選的點。</span><span class="sxs-lookup"><span data-stu-id="d6220-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="d6220-158">**UIA \_ ControllerForPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="d6220-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-159">See notes.</span></span>  | <span data-ttu-id="d6220-160">此屬性可做為相關聯索引標籤窗格的指標。</span><span class="sxs-lookup"><span data-stu-id="d6220-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="d6220-161">這在無法以索引標籤項目物件子系來裝載窗格時非常有用。</span><span class="sxs-lookup"><span data-stu-id="d6220-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="d6220-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d6220-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="d6220-163">**TabItem**</span></span> | <span data-ttu-id="d6220-164">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="d6220-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="d6220-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d6220-166">true</span><span class="sxs-lookup"><span data-stu-id="d6220-166">TRUE</span></span>        | <span data-ttu-id="d6220-167">索引標籤專案控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="d6220-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="d6220-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d6220-169">true</span><span class="sxs-lookup"><span data-stu-id="d6220-169">TRUE</span></span>        | <span data-ttu-id="d6220-170">索引標籤專案控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="d6220-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="d6220-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d6220-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-172">See notes.</span></span>  | <span data-ttu-id="d6220-173">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="d6220-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="d6220-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d6220-175">Null</span><span class="sxs-lookup"><span data-stu-id="d6220-175">Null</span></span>        | <span data-ttu-id="d6220-176">索引標籤項目控制項沒有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="d6220-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="d6220-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d6220-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-178">See notes.</span></span>  | <span data-ttu-id="d6220-179">對應到 **TabItem** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="d6220-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="d6220-180">預設值為 en-us 或英文 (美國) 的「tab 專案」。</span><span class="sxs-lookup"><span data-stu-id="d6220-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="d6220-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d6220-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d6220-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d6220-182">See notes.</span></span>  | <span data-ttu-id="d6220-183">索引標籤專案控制項自行加上標籤。</span><span class="sxs-lookup"><span data-stu-id="d6220-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d6220-184">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="d6220-184">Required Control Patterns</span></span>

<span data-ttu-id="d6220-185">下表列出所有索引標籤專案控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d6220-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="d6220-186">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d6220-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d6220-187">控制項模式</span><span class="sxs-lookup"><span data-stu-id="d6220-187">Control Pattern</span></span>                                                 | <span data-ttu-id="d6220-188">支援</span><span class="sxs-lookup"><span data-stu-id="d6220-188">Support</span></span>  | <span data-ttu-id="d6220-189">注意</span><span class="sxs-lookup"><span data-stu-id="d6220-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6220-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d6220-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="d6220-191">必要</span><span class="sxs-lookup"><span data-stu-id="d6220-191">Required</span></span> | <span data-ttu-id="d6220-192">索引標籤專案控制項必須支援 [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern)。</span><span class="sxs-lookup"><span data-stu-id="d6220-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="d6220-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="d6220-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="d6220-194">永不</span><span class="sxs-lookup"><span data-stu-id="d6220-194">Never</span></span>    | <span data-ttu-id="d6220-195">索引標籤專案控制項永遠不支援 [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)。</span><span class="sxs-lookup"><span data-stu-id="d6220-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="d6220-196">必要的事件</span><span class="sxs-lookup"><span data-stu-id="d6220-196">Required Events</span></span>

<span data-ttu-id="d6220-197">下表列出索引標籤專案控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="d6220-198">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d6220-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d6220-199">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="d6220-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="d6220-200">備註</span><span class="sxs-lookup"><span data-stu-id="d6220-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6220-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d6220-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="d6220-202">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="d6220-203">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="d6220-204">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d6220-205">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="d6220-206">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d6220-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="d6220-207">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="d6220-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="d6220-208">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="d6220-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="d6220-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d6220-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="d6220-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="d6220-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d6220-211">**概念**</span><span class="sxs-lookup"><span data-stu-id="d6220-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d6220-212">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="d6220-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d6220-213">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="d6220-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




