---
title: ToolBar 控制項類型
description: 本主題提供工具列控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 工具列控制項可讓使用者啟動應用程式內所含的命令和工具。
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- 消費者介面自動化，ToolBar 控制項類型的支援
- 消費者介面自動化，ToolBar 控制項類型
- 消費者介面自動化，工具列控制項類型的樹狀結構
- 消費者介面自動化，工具列控制項類型的屬性
- 消費者介面自動化，工具列控制項類型的控制項模式
- 消費者介面自動化，ToolBar 控制項類型的事件
- 樹狀結構，工具列控制項類型
- 屬性、工具列控制項類型
- 控制項模式、工具列控制項類型
- 事件、工具列控制項類型
- ToolBar 控制項類型的支援
- ToolBar 控制項類型
- 控制項類型、工具列控制項類型的樹狀結構
- 控制項類型、工具列控制項類型的控制項模式
- 控制項類型，支援工具列
- 控制項類型，工具列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372569"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="421ea-120">ToolBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="421ea-120">ToolBar Control Type</span></span>

<span data-ttu-id="421ea-121">本主題提供 **工具列** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="421ea-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="421ea-122">工具列控制項可讓使用者啟動應用程式內所含的命令和工具。</span><span class="sxs-lookup"><span data-stu-id="421ea-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="421ea-123">下列章節會定義 **工具列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="421ea-124">消費者介面自動化需求適用于所有工具列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="421ea-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="421ea-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="421ea-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="421ea-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="421ea-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="421ea-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="421ea-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="421ea-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="421ea-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="421ea-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="421ea-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="421ea-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="421ea-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="421ea-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="421ea-131">Typical Tree Structure</span></span>

<span data-ttu-id="421ea-132">下表描述的是與工具列控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="421ea-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="421ea-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="421ea-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="421ea-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="421ea-134">Control View</span></span></th>
<th><span data-ttu-id="421ea-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="421ea-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="421ea-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="421ea-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="421ea-137">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="421ea-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="421ea-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="421ea-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="421ea-139">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="421ea-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="421ea-140">工具列控制項可以在其子樹內包含任何類型的控制項。</span><span class="sxs-lookup"><span data-stu-id="421ea-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="421ea-141">通常包含按鈕、下拉式方塊與分割按鈕。</span><span class="sxs-lookup"><span data-stu-id="421ea-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="421ea-142">相關屬性</span><span class="sxs-lookup"><span data-stu-id="421ea-142">Relevant Properties</span></span>

<span data-ttu-id="421ea-143">下表列出消費者介面自動化屬性，其值或定義與 **工具列** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="421ea-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="421ea-144">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="421ea-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="421ea-145">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="421ea-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="421ea-146">值</span><span class="sxs-lookup"><span data-stu-id="421ea-146">Value</span></span>       | <span data-ttu-id="421ea-147">注意</span><span class="sxs-lookup"><span data-stu-id="421ea-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="421ea-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="421ea-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="421ea-149">See notes.</span></span>  | <span data-ttu-id="421ea-150">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="421ea-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="421ea-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="421ea-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="421ea-152">See notes.</span></span>  | <span data-ttu-id="421ea-153">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="421ea-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="421ea-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="421ea-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="421ea-155">See notes.</span></span>  | <span data-ttu-id="421ea-156">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="421ea-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="421ea-157">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="421ea-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="421ea-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="421ea-159">**工具 欄**</span><span class="sxs-lookup"><span data-stu-id="421ea-159">**ToolBar**</span></span> | <span data-ttu-id="421ea-160">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="421ea-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="421ea-161">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="421ea-162">true</span><span class="sxs-lookup"><span data-stu-id="421ea-162">TRUE</span></span>        | <span data-ttu-id="421ea-163">工具列控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="421ea-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="421ea-164">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="421ea-165">true</span><span class="sxs-lookup"><span data-stu-id="421ea-165">TRUE</span></span>        | <span data-ttu-id="421ea-166">工具列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="421ea-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="421ea-167">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="421ea-168">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="421ea-168">See notes.</span></span>  | <span data-ttu-id="421ea-169">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="421ea-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="421ea-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="421ea-171">NULL</span><span class="sxs-lookup"><span data-stu-id="421ea-171">NULL</span></span>        | <span data-ttu-id="421ea-172">工具列控制項永遠沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="421ea-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="421ea-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="421ea-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="421ea-174">See notes.</span></span>  | <span data-ttu-id="421ea-175">對應到 **ToolBar** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="421ea-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="421ea-176">預設值為 "tool bar" （適用于 en-us）或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="421ea-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="421ea-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="421ea-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="421ea-178">相依</span><span class="sxs-lookup"><span data-stu-id="421ea-178">Depends</span></span>     | <span data-ttu-id="421ea-179">除非在應用程式中使用一個以上的工具列控制項，否則它不需要名稱。</span><span class="sxs-lookup"><span data-stu-id="421ea-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="421ea-180">如果有一個以上的名稱，每個都必須有區別的名稱 (例如，「格式化」或「大綱」 ) 。</span><span class="sxs-lookup"><span data-stu-id="421ea-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="421ea-181">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="421ea-181">Required Control Patterns</span></span>

<span data-ttu-id="421ea-182">下表列出 toolbar 控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="421ea-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="421ea-183">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="421ea-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="421ea-184">控制項模式</span><span class="sxs-lookup"><span data-stu-id="421ea-184">Control Pattern</span></span>                                                   | <span data-ttu-id="421ea-185">支援</span><span class="sxs-lookup"><span data-stu-id="421ea-185">Support</span></span> | <span data-ttu-id="421ea-186">注意</span><span class="sxs-lookup"><span data-stu-id="421ea-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="421ea-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="421ea-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="421ea-188">相依</span><span class="sxs-lookup"><span data-stu-id="421ea-188">Depends</span></span> | <span data-ttu-id="421ea-189">如果工具列可停駐在螢幕的不同部分，則必須支援 [Dock](uiauto-implementingdock.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="421ea-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="421ea-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="421ea-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="421ea-191">相依</span><span class="sxs-lookup"><span data-stu-id="421ea-191">Depends</span></span> | <span data-ttu-id="421ea-192">如果工具列可以展開和折迭以顯示更多專案，它必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="421ea-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="421ea-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="421ea-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="421ea-194">相依</span><span class="sxs-lookup"><span data-stu-id="421ea-194">Depends</span></span> | <span data-ttu-id="421ea-195">如果工具列可以調整大小、旋轉或移動，它必須支援 [轉換](uiauto-implementingtransform.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="421ea-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="421ea-196">必要的事件</span><span class="sxs-lookup"><span data-stu-id="421ea-196">Required Events</span></span>

<span data-ttu-id="421ea-197">下表列出工具列控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="421ea-198">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="421ea-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="421ea-199">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="421ea-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="421ea-200">備註</span><span class="sxs-lookup"><span data-stu-id="421ea-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="421ea-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="421ea-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="421ea-202">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="421ea-203">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="421ea-204">如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="421ea-205">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="421ea-206">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="421ea-207">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="421ea-208">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="421ea-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="421ea-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="421ea-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="421ea-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="421ea-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="421ea-211">**概念**</span><span class="sxs-lookup"><span data-stu-id="421ea-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="421ea-212">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="421ea-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="421ea-213">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="421ea-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




