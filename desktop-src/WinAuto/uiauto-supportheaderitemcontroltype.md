---
title: HeaderItem 控制項類型
description: 本主題提供 HeaderItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- 消費者介面自動化，HeaderItem 控制項類型的支援
- 消費者介面自動化，HeaderItem 控制項類型
- 消費者介面自動化，HeaderItem 控制項類型的樹狀結構
- 消費者介面自動化，HeaderItem 控制項類型的屬性
- 消費者介面自動化，HeaderItem 控制項類型的控制項模式
- 消費者介面自動化，HeaderItem 控制項類型的事件
- 樹狀結構，HeaderItem 控制項類型
- properties、HeaderItem 控制項類型
- 控制項模式，HeaderItem 控制項類型
- events、HeaderItem 控制項類型
- HeaderItem 控制項類型的支援
- HeaderItem 控制項類型
- 控制項類型，HeaderItem 控制項類型的樹狀結構
- 控制項類型，HeaderItem 控制項類型的控制項模式
- 控制項類型，支援 HeaderItem
- 控制項類型，HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968222"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="5b72c-119">HeaderItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5b72c-119">HeaderItem Control Type</span></span>

<span data-ttu-id="5b72c-120">本主題提供 **HeaderItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5b72c-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="5b72c-121">**HeaderItem** 控制項類型提供資料列或資料行的視覺標籤。</span><span class="sxs-lookup"><span data-stu-id="5b72c-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="5b72c-122">下列章節會定義 **HeaderItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="5b72c-123">消費者介面自動化需求適用于所有的標題專案控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="5b72c-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5b72c-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="5b72c-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5b72c-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="5b72c-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5b72c-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="5b72c-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5b72c-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="5b72c-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5b72c-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="5b72c-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5b72c-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b72c-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5b72c-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="5b72c-130">Typical Tree Structure</span></span>

<span data-ttu-id="5b72c-131">下表描述標題專案控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的專案。</span><span class="sxs-lookup"><span data-stu-id="5b72c-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5b72c-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="5b72c-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b72c-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="5b72c-133">Control View</span></span></th>
<th><span data-ttu-id="5b72c-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="5b72c-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5b72c-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="5b72c-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="5b72c-136">(不適用)</span><span class="sxs-lookup"><span data-stu-id="5b72c-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="5b72c-137">相關屬性</span><span class="sxs-lookup"><span data-stu-id="5b72c-137">Relevant Properties</span></span>

<span data-ttu-id="5b72c-138">下表列出消費者介面自動化屬性，其值或定義與 **HeaderItem** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="5b72c-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="5b72c-139">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="5b72c-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5b72c-140">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="5b72c-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5b72c-141">值</span><span class="sxs-lookup"><span data-stu-id="5b72c-141">Value</span></span>          | <span data-ttu-id="5b72c-142">注意</span><span class="sxs-lookup"><span data-stu-id="5b72c-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b72c-143">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5b72c-144">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-144">See notes.</span></span>     | <span data-ttu-id="5b72c-145">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="5b72c-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="5b72c-146">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5b72c-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-147">See notes.</span></span>     | <span data-ttu-id="5b72c-148">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="5b72c-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="5b72c-149">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5b72c-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-150">See notes.</span></span>     | <span data-ttu-id="5b72c-151">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="5b72c-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5b72c-152">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="5b72c-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="5b72c-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5b72c-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="5b72c-154">**HeaderItem**</span></span> | <span data-ttu-id="5b72c-155">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="5b72c-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="5b72c-156">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5b72c-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="5b72c-157">FALSE</span></span>          | <span data-ttu-id="5b72c-158">標題專案控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="5b72c-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="5b72c-159">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5b72c-160">true</span><span class="sxs-lookup"><span data-stu-id="5b72c-160">TRUE</span></span>           | <span data-ttu-id="5b72c-161">標題專案控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="5b72c-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="5b72c-162">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5b72c-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-163">See notes.</span></span>     | <span data-ttu-id="5b72c-164">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="5b72c-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="5b72c-165">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="5b72c-166">請參閱附註</span><span class="sxs-lookup"><span data-stu-id="5b72c-166">See notes</span></span>      | <span data-ttu-id="5b72c-167">這個屬性會提供依照標題項目之排序次序的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5b72c-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="5b72c-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5b72c-169">NULL</span><span class="sxs-lookup"><span data-stu-id="5b72c-169">NULL</span></span>           | <span data-ttu-id="5b72c-170">標題專案控制項沒有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="5b72c-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="5b72c-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5b72c-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-172">See notes.</span></span>     | <span data-ttu-id="5b72c-173">對應到 **HeaderItem** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="5b72c-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="5b72c-174">預設值為 en-us 或英文 (美國) 的「標頭專案」。</span><span class="sxs-lookup"><span data-stu-id="5b72c-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="5b72c-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5b72c-176">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="5b72c-176">See notes.</span></span>     | <span data-ttu-id="5b72c-177">標題項目控制項一律自行設定標籤。</span><span class="sxs-lookup"><span data-stu-id="5b72c-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5b72c-178">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="5b72c-178">Required Control Patterns</span></span>

<span data-ttu-id="5b72c-179">下表列出所有標題專案控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5b72c-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="5b72c-180">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="5b72c-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="5b72c-181">控制項模式</span><span class="sxs-lookup"><span data-stu-id="5b72c-181">Control Pattern</span></span>                                         | <span data-ttu-id="5b72c-182">支援</span><span class="sxs-lookup"><span data-stu-id="5b72c-182">Support</span></span> | <span data-ttu-id="5b72c-183">注意</span><span class="sxs-lookup"><span data-stu-id="5b72c-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b72c-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="5b72c-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="5b72c-185">相依</span><span class="sxs-lookup"><span data-stu-id="5b72c-185">Depends</span></span> | <span data-ttu-id="5b72c-186">如果可以按一下標頭專案控制項來排序資料，請執行 [Invoke](uiauto-implementinginvoke.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5b72c-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="5b72c-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="5b72c-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="5b72c-188">相依</span><span class="sxs-lookup"><span data-stu-id="5b72c-188">Depends</span></span> | <span data-ttu-id="5b72c-189">如果標頭專案控制項可以調整大小，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="5b72c-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="5b72c-190">必要的事件</span><span class="sxs-lookup"><span data-stu-id="5b72c-190">Required Events</span></span>

<span data-ttu-id="5b72c-191">下表列出支援的標題專案控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="5b72c-192">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="5b72c-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5b72c-193">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="5b72c-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5b72c-194">備註</span><span class="sxs-lookup"><span data-stu-id="5b72c-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b72c-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5b72c-196">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="5b72c-197">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="5b72c-198">如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="5b72c-199">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5b72c-200">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5b72c-201">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5b72c-202">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="5b72c-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5b72c-203">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5b72c-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5b72c-204">相關主題</span><span class="sxs-lookup"><span data-stu-id="5b72c-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5b72c-205">**概念**</span><span class="sxs-lookup"><span data-stu-id="5b72c-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5b72c-206">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="5b72c-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5b72c-207">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="5b72c-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




