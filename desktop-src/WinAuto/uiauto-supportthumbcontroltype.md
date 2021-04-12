---
title: Thumb 控制項類型
description: 本主題提供有關 Microsoft 消費者介面自動化 Thumb 控制項類型支援的相關資訊。
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- 消費者介面自動化，Thumb 控制項類型的支援
- 消費者介面自動化，Thumb 控制項類型
- 消費者介面自動化，Thumb 控制項類型的樹狀結構
- 消費者介面自動化，Thumb 控制項類型的屬性
- 消費者介面自動化、Thumb 控制項類型的控制項模式
- 消費者介面自動化，Thumb 控制項類型的事件
- 樹狀結構，Thumb 控制項類型
- properties、Thumb 控制項類型
- 控制項模式、Thumb 控制項類型
- 事件、Thumb 控制項類型
- Thumb 控制項類型的支援
- Thumb 控制項類型
- 控制項類型，Thumb 控制項類型的樹狀結構
- 控制項類型、Thumb 控制項類型的控制項模式
- 控制項類型，支援 Thumb
- 控制項類型、Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372570"
---
# <a name="thumb-control-type"></a><span data-ttu-id="ccf0e-119">Thumb 控制項類型</span><span class="sxs-lookup"><span data-stu-id="ccf0e-119">Thumb Control Type</span></span>

<span data-ttu-id="ccf0e-120">本主題提供有關 Microsoft 消費者介面自動化 **Thumb** 控制項類型支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="ccf0e-121">Thumb 控制項提供移動 (或拖曳) 控制項的功能 (如捲軸按鈕)，或是調整控制項大小的功能 (如會調整 Widget 大小的視窗)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="ccf0e-122">請注意，thumb 控制項不會提供拖放功能。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="ccf0e-123">Thumb 控制項可以接收滑鼠焦點，而不是鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="ccf0e-124">控制項開發人員必須正確實作控制項，使其能夠適當運作 (可供拖曳或調整大小)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="ccf0e-125">下列章節會定義 **Thumb** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="ccf0e-126">消費者介面自動化需求適用于所有的 thumb 控制項，UI 架構/平臺會將控制項類型和控制項模式的消費者介面自動化支援全部整合在一起。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ccf0e-127">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ccf0e-128">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ccf0e-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ccf0e-129">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ccf0e-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ccf0e-130">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ccf0e-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ccf0e-131">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ccf0e-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ccf0e-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccf0e-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ccf0e-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ccf0e-133">Typical Tree Structure</span></span>

<span data-ttu-id="ccf0e-134">下表描述的是與 thumb 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ccf0e-135">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ccf0e-136">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="ccf0e-136">Control View</span></span></th>
<th><span data-ttu-id="ccf0e-137">內容檢視</span><span class="sxs-lookup"><span data-stu-id="ccf0e-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ccf0e-138">Thumb</span><span class="sxs-lookup"><span data-stu-id="ccf0e-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="ccf0e-139">(不適用)</span><span class="sxs-lookup"><span data-stu-id="ccf0e-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ccf0e-140">Thumb 控制項不會出現在內容視圖中，因為它們只會在使用滑鼠操作時存在。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="ccf0e-141">它們是由 thumb 控制項容器支援的另一個控制項模式（例如 [滾動](uiauto-implementingscroll.md) 條控制項模式、 [轉換](uiauto-implementingtransform.md) 控制項模式或 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式）所公開。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ccf0e-142">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ccf0e-142">Relevant Properties</span></span>

<span data-ttu-id="ccf0e-143">下表列出消費者介面自動化屬性，其值或定義與 thumb 控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="ccf0e-144">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ccf0e-145">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="ccf0e-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ccf0e-146">值</span><span class="sxs-lookup"><span data-stu-id="ccf0e-146">Value</span></span>      | <span data-ttu-id="ccf0e-147">注意</span><span class="sxs-lookup"><span data-stu-id="ccf0e-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf0e-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ccf0e-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-149">See notes.</span></span> | <span data-ttu-id="ccf0e-150">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ccf0e-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ccf0e-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-152">See notes.</span></span> | <span data-ttu-id="ccf0e-153">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="ccf0e-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ccf0e-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-155">See notes.</span></span> | <span data-ttu-id="ccf0e-156">Thumb 控制項之可見工作區內的某個點。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="ccf0e-157">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ccf0e-158">**拇指**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="ccf0e-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ccf0e-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="ccf0e-160">FALSE</span></span>      | <span data-ttu-id="ccf0e-161">Thumb 控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="ccf0e-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ccf0e-163">true</span><span class="sxs-lookup"><span data-stu-id="ccf0e-163">TRUE</span></span>       | <span data-ttu-id="ccf0e-164">Thumb 控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="ccf0e-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ccf0e-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-166">See notes.</span></span> | <span data-ttu-id="ccf0e-167">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="ccf0e-168">如果 thumb 控制項是用來做為視窗大小調整視窗或窗格的「控制手柄」物件，就可以接收焦點。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="ccf0e-169">滑杆或捲軸中的 thumb 控制項絕對不會收到焦點。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="ccf0e-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ccf0e-171">NULL</span><span class="sxs-lookup"><span data-stu-id="ccf0e-171">NULL</span></span>       | <span data-ttu-id="ccf0e-172">Thumb 控制項一律沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="ccf0e-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ccf0e-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-174">See notes.</span></span> | <span data-ttu-id="ccf0e-175">對應至 **Thumb** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="ccf0e-176">預設值為 "thumb"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="ccf0e-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ccf0e-178">NULL</span><span class="sxs-lookup"><span data-stu-id="ccf0e-178">NULL</span></span>       | <span data-ttu-id="ccf0e-179">由於 thumb 控制項無法在消費者介面自動化樹狀結構的內容視圖中使用，因此不需要名稱。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ccf0e-180">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ccf0e-180">Required Control Patterns</span></span>

<span data-ttu-id="ccf0e-181">下表列出 thumb 控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="ccf0e-182">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ccf0e-183">控制項模式</span><span class="sxs-lookup"><span data-stu-id="ccf0e-183">Control Pattern</span></span>                                         | <span data-ttu-id="ccf0e-184">支援</span><span class="sxs-lookup"><span data-stu-id="ccf0e-184">Support</span></span>  | <span data-ttu-id="ccf0e-185">注意</span><span class="sxs-lookup"><span data-stu-id="ccf0e-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf0e-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="ccf0e-187">必要</span><span class="sxs-lookup"><span data-stu-id="ccf0e-187">Required</span></span> | <span data-ttu-id="ccf0e-188">使畫面上的 Thumb 控制項可以移動。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="ccf0e-189">由於 thumb 控制項通常無法調整大小或旋轉，因此 [轉換](uiauto-implementingtransform.md) 控制項模式主要支援 [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) 函數。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ccf0e-190">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ccf0e-190">Required Events</span></span>

<span data-ttu-id="ccf0e-191">下表列出支援的控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="ccf0e-192">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="ccf0e-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ccf0e-193">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="ccf0e-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ccf0e-194">備註</span><span class="sxs-lookup"><span data-stu-id="ccf0e-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ccf0e-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ccf0e-196">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ccf0e-197">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ccf0e-198">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ccf0e-199">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ccf0e-200">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ccf0e-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="ccf0e-201">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ccf0e-202">相關主題</span><span class="sxs-lookup"><span data-stu-id="ccf0e-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ccf0e-203">**概念**</span><span class="sxs-lookup"><span data-stu-id="ccf0e-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ccf0e-204">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="ccf0e-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ccf0e-205">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="ccf0e-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




