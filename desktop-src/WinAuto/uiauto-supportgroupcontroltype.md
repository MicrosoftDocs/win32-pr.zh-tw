---
title: 群組控制項類型
description: 本主題提供有關 Microsoft 消費者介面自動化 Group 控制項類型支援的資訊。
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- 消費者介面自動化，支援 Group 控制項類型
- 消費者介面自動化，Group 控制項類型
- 消費者介面自動化，群組控制項類型的樹狀結構
- 消費者介面自動化，群組控制項類型的屬性
- 消費者介面自動化，群組控制項類型的控制項模式
- 消費者介面自動化，群組控制項類型的事件
- 樹狀結構，群組控制項類型
- 屬性，群組控制項類型
- 控制項模式，群組控制項類型
- 事件、群組控制項類型
- 群組控制項類型的支援
- Group 控制項類型
- 控制項類型，群組控制項類型的樹狀結構
- 控制項類型，群組控制項類型的控制項模式
- 控制項類型，支援群組
- 控制項類型，群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372127"
---
# <a name="group-control-type"></a><span data-ttu-id="16e87-119">群組控制項類型</span><span class="sxs-lookup"><span data-stu-id="16e87-119">Group Control Type</span></span>

<span data-ttu-id="16e87-120">本主題提供有關 Microsoft 消費者介面自動化 **Group** 控制項類型支援的資訊。</span><span class="sxs-lookup"><span data-stu-id="16e87-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="16e87-121">群組控制項代表階層內的節點。</span><span class="sxs-lookup"><span data-stu-id="16e87-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="16e87-122">**組合** 控制項類型會在消費者介面自動化樹狀結構中建立分隔，讓群組在一起的專案在消費者介面自動化樹狀結構內具有邏輯除法。</span><span class="sxs-lookup"><span data-stu-id="16e87-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="16e87-123">下列章節會定義 **Group** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="16e87-124">消費者介面自動化需求適用于所有的群組控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="16e87-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="16e87-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="16e87-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="16e87-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="16e87-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="16e87-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="16e87-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="16e87-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="16e87-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="16e87-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="16e87-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="16e87-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="16e87-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="16e87-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="16e87-131">Typical Tree Structure</span></span>

<span data-ttu-id="16e87-132">下表描述的是與群組控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="16e87-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="16e87-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="16e87-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16e87-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="16e87-134">Control View</span></span></th>
<th><span data-ttu-id="16e87-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="16e87-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="16e87-136">Group</span><span class="sxs-lookup"><span data-stu-id="16e87-136">Group</span></span>
<ul>
<li><span data-ttu-id="16e87-137">0 個以上的控制項</span><span class="sxs-lookup"><span data-stu-id="16e87-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="16e87-138">Group</span><span class="sxs-lookup"><span data-stu-id="16e87-138">Group</span></span>
<ul>
<li><span data-ttu-id="16e87-139">0 個以上的控制項</span><span class="sxs-lookup"><span data-stu-id="16e87-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="16e87-140">群組控制項通常包含子樹 [中的控制項](uiauto-supportlistitemcontroltype.md)類型消費者介面自動化支援，包括專案組合、 [TreeItem](uiauto-supporttreeitemcontroltype.md)和 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="16e87-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="16e87-141">因為群組控制項是泛型容器，所以在樹狀結構中的群組控制項下可以有任何類型的控制項。</span><span class="sxs-lookup"><span data-stu-id="16e87-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="16e87-142">相關屬性</span><span class="sxs-lookup"><span data-stu-id="16e87-142">Relevant Properties</span></span>

<span data-ttu-id="16e87-143">下表列出消費者介面自動化屬性，其值或定義與群組控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="16e87-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="16e87-144">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="16e87-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="16e87-145">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="16e87-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="16e87-146">值</span><span class="sxs-lookup"><span data-stu-id="16e87-146">Value</span></span>      | <span data-ttu-id="16e87-147">注意</span><span class="sxs-lookup"><span data-stu-id="16e87-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e87-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="16e87-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-149">See notes.</span></span> | <span data-ttu-id="16e87-150">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="16e87-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="16e87-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="16e87-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-152">See notes.</span></span> | <span data-ttu-id="16e87-153">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="16e87-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="16e87-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="16e87-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-155">See notes.</span></span> | <span data-ttu-id="16e87-156">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="16e87-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="16e87-157">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="16e87-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="16e87-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="16e87-159">**群組**</span><span class="sxs-lookup"><span data-stu-id="16e87-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="16e87-160">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="16e87-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="16e87-161">**TRUE**</span></span>   | <span data-ttu-id="16e87-162">此群組控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="16e87-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="16e87-163">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="16e87-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="16e87-164">**TRUE**</span></span>   | <span data-ttu-id="16e87-165">此群組控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="16e87-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="16e87-166">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="16e87-167">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-167">See notes.</span></span> | <span data-ttu-id="16e87-168">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="16e87-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="16e87-169">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="16e87-170">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-170">See notes.</span></span> | <span data-ttu-id="16e87-171">群組控制項通常會自行設定標籤。</span><span class="sxs-lookup"><span data-stu-id="16e87-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="16e87-172">在這些情況下，會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="16e87-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="16e87-173">如果群組具有靜態文字標籤，則會傳回標籤作為 **LabeledBy** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="16e87-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="16e87-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="16e87-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-175">See notes.</span></span> | <span data-ttu-id="16e87-176">對應至 **組合** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="16e87-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="16e87-177">預設值為 "group"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="16e87-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="16e87-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="16e87-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="16e87-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="16e87-179">See notes.</span></span> | <span data-ttu-id="16e87-180">群組控制項通常會從控制項的標籤文字取得名稱。</span><span class="sxs-lookup"><span data-stu-id="16e87-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="16e87-181">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="16e87-181">Required Control Patterns</span></span>

<span data-ttu-id="16e87-182">下表列出 **群組** 控制項類型所需的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="16e87-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="16e87-183">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="16e87-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="16e87-184">控制項模式</span><span class="sxs-lookup"><span data-stu-id="16e87-184">Control Pattern</span></span>                                                   | <span data-ttu-id="16e87-185">支援</span><span class="sxs-lookup"><span data-stu-id="16e87-185">Support</span></span> | <span data-ttu-id="16e87-186">注意</span><span class="sxs-lookup"><span data-stu-id="16e87-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e87-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="16e87-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="16e87-188">相依</span><span class="sxs-lookup"><span data-stu-id="16e87-188">Depends</span></span> | <span data-ttu-id="16e87-189">可以用來顯示或隱藏資訊的群組控制項，必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="16e87-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="16e87-190">必要的事件</span><span class="sxs-lookup"><span data-stu-id="16e87-190">Required Events</span></span>

<span data-ttu-id="16e87-191">下表列出需要支援群組控制項的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="16e87-192">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="16e87-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="16e87-193">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="16e87-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="16e87-194">備註</span><span class="sxs-lookup"><span data-stu-id="16e87-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16e87-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="16e87-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="16e87-196">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="16e87-197">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="16e87-198">如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="16e87-199">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="16e87-200">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="16e87-201">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="16e87-202">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="16e87-203">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="16e87-204">如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="16e87-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="16e87-205">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="16e87-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="16e87-206">相關主題</span><span class="sxs-lookup"><span data-stu-id="16e87-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="16e87-207">**概念**</span><span class="sxs-lookup"><span data-stu-id="16e87-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="16e87-208">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="16e87-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="16e87-209">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="16e87-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




