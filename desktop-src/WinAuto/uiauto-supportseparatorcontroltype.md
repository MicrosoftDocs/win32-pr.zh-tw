---
title: 分隔符號控制項類型
description: 本主題提供分隔符號控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- 消費者介面自動化、分隔符號控制項類型的支援
- 消費者介面自動化、分隔符號控制項類型
- 消費者介面自動化，分隔符號控制項類型的樹狀結構
- 消費者介面自動化，分隔符號控制項類型的屬性
- 消費者介面自動化，分隔符號控制項類型的控制項模式
- 消費者介面自動化，分隔符號控制項類型的事件
- 樹狀結構、分隔符號控制項類型
- 屬性、分隔符號控制項類型
- 控制項模式、分隔符號控制項類型
- 事件、分隔符號控制項類型
- 分隔符號控制項類型的支援
- Separator 控制項類型
- 控制項類型、分隔符號控制項類型的樹狀結構
- 控制項類型、分隔符號控制項類型的控制項模式
- 控制項類型，支援分隔符號
- 控制項類型，分隔符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507344"
---
# <a name="separator-control-type"></a><span data-ttu-id="5c555-119">分隔符號控制項類型</span><span class="sxs-lookup"><span data-stu-id="5c555-119">Separator Control Type</span></span>

<span data-ttu-id="5c555-120">本主題提供 **分隔符號** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5c555-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="5c555-121">分隔符號控制項是用來以視覺方式將空間分隔成兩個區域。</span><span class="sxs-lookup"><span data-stu-id="5c555-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="5c555-122">例如，分隔符號控制項可以是定義視窗中兩個窗格的分隔線。</span><span class="sxs-lookup"><span data-stu-id="5c555-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="5c555-123">如果分隔符號是可移動的，控制項就應公開為控制項類型 Thumb。</span><span class="sxs-lookup"><span data-stu-id="5c555-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="5c555-124">下列章節會定義 **分隔符號** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="5c555-125">消費者介面自動化需求適用于所有的分隔符號控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="5c555-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5c555-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="5c555-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5c555-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="5c555-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5c555-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="5c555-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5c555-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="5c555-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5c555-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="5c555-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5c555-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c555-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5c555-132">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="5c555-132">Typical Tree Structure</span></span>

<span data-ttu-id="5c555-133">下表描述的是與分隔符號控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="5c555-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5c555-134">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="5c555-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c555-135">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="5c555-135">Control View</span></span></th>
<th><span data-ttu-id="5c555-136">內容檢視</span><span class="sxs-lookup"><span data-stu-id="5c555-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5c555-137">Separator</span><span class="sxs-lookup"><span data-stu-id="5c555-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5c555-138"><strong>分隔符號</strong>控制項類型永遠不會有內容。</span><span class="sxs-lookup"><span data-stu-id="5c555-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="5c555-139">相關屬性</span><span class="sxs-lookup"><span data-stu-id="5c555-139">Relevant Properties</span></span>

<span data-ttu-id="5c555-140">下表列出消費者介面自動化屬性，其值或定義與分隔符號控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="5c555-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="5c555-141">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="5c555-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5c555-142">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="5c555-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5c555-143">值</span><span class="sxs-lookup"><span data-stu-id="5c555-143">Value</span></span>         | <span data-ttu-id="5c555-144">注意</span><span class="sxs-lookup"><span data-stu-id="5c555-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c555-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5c555-146">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5c555-146">See notes.</span></span>    | <span data-ttu-id="5c555-147">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5c555-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="5c555-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5c555-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5c555-149">See notes.</span></span>    | <span data-ttu-id="5c555-150">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="5c555-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="5c555-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5c555-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5c555-152">See notes.</span></span>    | <span data-ttu-id="5c555-153">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="5c555-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5c555-154">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="5c555-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="5c555-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5c555-156">**Separator**</span><span class="sxs-lookup"><span data-stu-id="5c555-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="5c555-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5c555-158">FALSE</span><span class="sxs-lookup"><span data-stu-id="5c555-158">FALSE</span></span>         | <span data-ttu-id="5c555-159">分隔符號控制項絕不會是內容。</span><span class="sxs-lookup"><span data-stu-id="5c555-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="5c555-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5c555-161">true</span><span class="sxs-lookup"><span data-stu-id="5c555-161">TRUE</span></span>          | <span data-ttu-id="5c555-162">分隔符號控制項必須一律是控制項。</span><span class="sxs-lookup"><span data-stu-id="5c555-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="5c555-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5c555-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5c555-164">See notes.</span></span>    | <span data-ttu-id="5c555-165">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="5c555-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="5c555-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5c555-167">NULL</span><span class="sxs-lookup"><span data-stu-id="5c555-167">NULL</span></span>          | <span data-ttu-id="5c555-168">分隔符號控制項沒有靜態標籤。</span><span class="sxs-lookup"><span data-stu-id="5c555-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="5c555-169">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5c555-170">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5c555-170">See notes.</span></span>    | <span data-ttu-id="5c555-171">對應至 **分隔符號** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="5c555-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="5c555-172">預設值為 en-us 或英文 (美國) 的「分隔符號」。</span><span class="sxs-lookup"><span data-stu-id="5c555-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="5c555-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5c555-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5c555-174">""</span><span class="sxs-lookup"><span data-stu-id="5c555-174">""</span></span>            | <span data-ttu-id="5c555-175">分隔符號控制項不需要 **Name** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c555-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5c555-176">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="5c555-176">Required Control Patterns</span></span>

<span data-ttu-id="5c555-177">分隔符號控制項不必支援任何控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5c555-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="5c555-178">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="5c555-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="5c555-179">必要的事件</span><span class="sxs-lookup"><span data-stu-id="5c555-179">Required Events</span></span>

<span data-ttu-id="5c555-180">下表列出需要分隔符號控制項的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="5c555-181">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="5c555-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5c555-182">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="5c555-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5c555-183">備註</span><span class="sxs-lookup"><span data-stu-id="5c555-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c555-184">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5c555-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5c555-185">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5c555-186">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5c555-187">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5c555-188">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5c555-189">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5c555-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5c555-190">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5c555-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5c555-191">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c555-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c555-192">**概念**</span><span class="sxs-lookup"><span data-stu-id="5c555-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5c555-193">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="5c555-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5c555-194">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="5c555-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




