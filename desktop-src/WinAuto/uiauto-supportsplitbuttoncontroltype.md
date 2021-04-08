---
title: SplitButton 控制項類型
description: 本主題提供 SplitButton 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- 消費者介面自動化，SplitButton 控制項類型的支援
- 消費者介面自動化，SplitButton 控制項類型
- 消費者介面自動化，SplitButton 控制項類型的樹狀結構
- 消費者介面自動化，SplitButton 控制項類型的屬性
- 消費者介面自動化，SplitButton 控制項類型的控制項模式
- 消費者介面自動化，SplitButton 控制項類型的事件
- 樹狀結構，SplitButton 控制項類型
- properties、SplitButton 控制項類型
- 控制項模式，SplitButton 控制項類型
- events、SplitButton 控制項類型
- SplitButton 控制項類型的支援
- SplitButton 控制項類型
- 控制項類型，SplitButton 控制項類型的樹狀結構
- 控制項類型，SplitButton 控制項類型的控制項模式
- 控制項類型，支援 SplitButton
- 控制項類型，SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674664"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="4b83e-119">SplitButton 控制項類型</span><span class="sxs-lookup"><span data-stu-id="4b83e-119">SplitButton Control Type</span></span>

<span data-ttu-id="4b83e-120">本主題提供 **SplitButton** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4b83e-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="4b83e-121">分割按鈕控制項可讓您在控制項上執行動作，以及展開控制項以查看其他可能執行的動作清單。</span><span class="sxs-lookup"><span data-stu-id="4b83e-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="4b83e-122">下列章節會定義 **SplitButton** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="4b83e-123">消費者介面自動化需求適用于所有的分割按鈕控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="4b83e-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4b83e-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="4b83e-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4b83e-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4b83e-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4b83e-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4b83e-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4b83e-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4b83e-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4b83e-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4b83e-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4b83e-129">SplitButton 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="4b83e-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="4b83e-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b83e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4b83e-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4b83e-131">Typical Tree Structure</span></span>

<span data-ttu-id="4b83e-132">下表描述與分割按鈕控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="4b83e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4b83e-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4b83e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b83e-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="4b83e-134">Control View</span></span></th>
<th><span data-ttu-id="4b83e-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="4b83e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4b83e-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="4b83e-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="4b83e-137">Image (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="4b83e-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="4b83e-138">文字 (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="4b83e-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="4b83e-139">按鈕 (1 或 2)</span><span class="sxs-lookup"><span data-stu-id="4b83e-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="4b83e-140">功能表 (0 或 1;顯示為支援 ExpandCollapse 模式之子按鈕的子按鈕) </span><span class="sxs-lookup"><span data-stu-id="4b83e-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="4b83e-141">MenuItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="4b83e-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4b83e-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="4b83e-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="4b83e-143">按鈕 (1 或 2)</span><span class="sxs-lookup"><span data-stu-id="4b83e-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="4b83e-144">MenuItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="4b83e-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4b83e-145">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4b83e-145">Relevant Properties</span></span>

<span data-ttu-id="4b83e-146">下表列出消費者介面自動化屬性，其值或定義與 **SplitButton** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="4b83e-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="4b83e-147">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="4b83e-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4b83e-148">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="4b83e-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4b83e-149">值</span><span class="sxs-lookup"><span data-stu-id="4b83e-149">Value</span></span>           | <span data-ttu-id="4b83e-150">注意</span><span class="sxs-lookup"><span data-stu-id="4b83e-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b83e-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4b83e-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-152">See notes.</span></span>      | <span data-ttu-id="4b83e-153">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="4b83e-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="4b83e-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4b83e-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-155">See notes.</span></span>      | <span data-ttu-id="4b83e-156">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="4b83e-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="4b83e-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4b83e-158">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-158">See notes.</span></span>      | <span data-ttu-id="4b83e-159">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="4b83e-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="4b83e-160">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="4b83e-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="4b83e-161">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4b83e-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="4b83e-162">**SplitButton**</span></span> | <span data-ttu-id="4b83e-163">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="4b83e-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="4b83e-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="4b83e-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-165">See notes.</span></span>      | <span data-ttu-id="4b83e-166">說明文字可能指出啟動分割按鈕的結果，而這通常是透過工具提示顯示的相同類型資訊。</span><span class="sxs-lookup"><span data-stu-id="4b83e-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="4b83e-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4b83e-168">true</span><span class="sxs-lookup"><span data-stu-id="4b83e-168">TRUE</span></span>            | <span data-ttu-id="4b83e-169">分割按鈕控制項包含給使用者的資訊。</span><span class="sxs-lookup"><span data-stu-id="4b83e-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="4b83e-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4b83e-171">true</span><span class="sxs-lookup"><span data-stu-id="4b83e-171">TRUE</span></span>            | <span data-ttu-id="4b83e-172">使用者可以看到分割按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="4b83e-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="4b83e-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4b83e-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-174">See notes.</span></span>      | <span data-ttu-id="4b83e-175">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="4b83e-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="4b83e-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4b83e-177">NULL</span><span class="sxs-lookup"><span data-stu-id="4b83e-177">NULL</span></span>            | <span data-ttu-id="4b83e-178">分割按鈕控制項沒有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="4b83e-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="4b83e-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4b83e-180">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-180">See notes.</span></span>      | <span data-ttu-id="4b83e-181">對應到 **SplitButton** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="4b83e-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="4b83e-182">預設值為 en-us 或英文 (美國) 的「分割按鈕」。</span><span class="sxs-lookup"><span data-stu-id="4b83e-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="4b83e-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4b83e-184">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4b83e-184">See notes.</span></span>      | <span data-ttu-id="4b83e-185">用來標示分割按鈕的文字。</span><span class="sxs-lookup"><span data-stu-id="4b83e-185">The text that is used to label the split button.</span></span> <span data-ttu-id="4b83e-186">每次使用影像來標示分割按鈕時，必須提供 [分割按鈕名稱] 屬性的替代文字。</span><span class="sxs-lookup"><span data-stu-id="4b83e-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4b83e-187">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4b83e-187">Required Control Patterns</span></span>

<span data-ttu-id="4b83e-188">下表列出所有分割按鈕控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4b83e-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="4b83e-189">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4b83e-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4b83e-190">控制項模式</span><span class="sxs-lookup"><span data-stu-id="4b83e-190">Control Pattern</span></span>                                                   | <span data-ttu-id="4b83e-191">支援</span><span class="sxs-lookup"><span data-stu-id="4b83e-191">Support</span></span>  | <span data-ttu-id="4b83e-192">注意</span><span class="sxs-lookup"><span data-stu-id="4b83e-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b83e-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="4b83e-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="4b83e-194">必要</span><span class="sxs-lookup"><span data-stu-id="4b83e-194">Required</span></span> | <span data-ttu-id="4b83e-195">因為分割按鈕一律具有展開選項清單的能力，所以必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4b83e-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="4b83e-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="4b83e-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="4b83e-197">必要</span><span class="sxs-lookup"><span data-stu-id="4b83e-197">Required</span></span> | <span data-ttu-id="4b83e-198">因為分割按鈕一律具有與 [**IInvokeProvider：： invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) 方法相關聯的預設動作，所以必須支援 [invoke](uiauto-implementinginvoke.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4b83e-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4b83e-199">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4b83e-199">Required Events</span></span>

<span data-ttu-id="4b83e-200">下表列出需要支援分割按鈕控制項的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="4b83e-201">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="4b83e-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4b83e-202">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="4b83e-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="4b83e-203">備註</span><span class="sxs-lookup"><span data-stu-id="4b83e-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b83e-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="4b83e-205">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="4b83e-206">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="4b83e-207">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="4b83e-208">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="4b83e-209">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="4b83e-210">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="4b83e-211">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4b83e-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="4b83e-212">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4b83e-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="4b83e-213">SplitButton 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="4b83e-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="4b83e-214">下圖說明可實 **SplitButton** 控制項類型的控制項。</span><span class="sxs-lookup"><span data-stu-id="4b83e-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![顯示 splitbutton 控制項範例的螢幕擷取畫面](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4b83e-216">消費者介面自動化樹狀結構-控制項視圖</span><span class="sxs-lookup"><span data-stu-id="4b83e-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="4b83e-217">消費者介面自動化樹狀結構-內容視圖</span><span class="sxs-lookup"><span data-stu-id="4b83e-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4b83e-218">SplitButton &quot; Name &quot; (Invoke，ExpandCollapse) </span><span class="sxs-lookup"><span data-stu-id="4b83e-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="4b83e-219">按鈕 &quot; 更多選項 (叫用 &quot;) </span><span class="sxs-lookup"><span data-stu-id="4b83e-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="4b83e-220">功能表</span><span class="sxs-lookup"><span data-stu-id="4b83e-220">Menu</span></span>
<ul>
<li><span data-ttu-id="4b83e-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="4b83e-221">MenuItem</span></span></li>
<li><span data-ttu-id="4b83e-222">...</span><span class="sxs-lookup"><span data-stu-id="4b83e-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4b83e-223">SplitButton &quot; Name &quot; (Invoke，ExpandCollapse) </span><span class="sxs-lookup"><span data-stu-id="4b83e-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="4b83e-224">按鈕 &quot; 更多選項 (叫用 &quot;) </span><span class="sxs-lookup"><span data-stu-id="4b83e-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="4b83e-225">功能表</span><span class="sxs-lookup"><span data-stu-id="4b83e-225">Menu</span></span>
<ul>
<li><span data-ttu-id="4b83e-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="4b83e-226">MenuItem</span></span></li>
<li><span data-ttu-id="4b83e-227">...</span><span class="sxs-lookup"><span data-stu-id="4b83e-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4b83e-228">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b83e-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4b83e-229">**概念**</span><span class="sxs-lookup"><span data-stu-id="4b83e-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4b83e-230">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="4b83e-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4b83e-231">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="4b83e-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




