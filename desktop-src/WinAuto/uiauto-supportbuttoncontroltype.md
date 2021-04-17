---
title: Button 控制項類型
description: 本主題提供按鈕控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- 消費者介面自動化，Button 控制項類型的支援
- 消費者介面自動化，Button 控制項類型
- 消費者介面自動化，Button 控制項類型的樹狀結構
- 消費者介面自動化，Button 控制項類型的屬性
- 消費者介面自動化，Button 控制項類型的控制項模式
- 消費者介面自動化，Button 控制項類型的事件
- 樹狀結構，按鈕控制項類型
- 屬性，按鈕控制項類型
- 控制項模式，按鈕控制項類型
- 事件、按鈕控制項類型
- Button 控制項類型的支援
- Button 控制項類型
- 控制項類型、按鈕控制項類型的樹狀結構
- 控制項類型、按鈕控制項類型的控制項模式
- 控制項類型、支援按鈕
- 控制項類型，按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184186"
---
# <a name="button-control-type"></a><span data-ttu-id="551cb-119">Button 控制項類型</span><span class="sxs-lookup"><span data-stu-id="551cb-119">Button Control Type</span></span>

<span data-ttu-id="551cb-120">本主題提供 **按鈕** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="551cb-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="551cb-121">按鈕是可供使用者互動的物件，能在對話方塊執行如 [確定] 和 [取消] 按鈕等動作。</span><span class="sxs-lookup"><span data-stu-id="551cb-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="551cb-122">按鈕控制項的公開方式很簡單，因為它對應的是使用者想要完成的單一命令。</span><span class="sxs-lookup"><span data-stu-id="551cb-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="551cb-123">下列章節會定義 **按鈕** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="551cb-124">消費者介面自動化需求適用于所有按鈕控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="551cb-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="551cb-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="551cb-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="551cb-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="551cb-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="551cb-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="551cb-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="551cb-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="551cb-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="551cb-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="551cb-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="551cb-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="551cb-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="551cb-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="551cb-131">Typical Tree Structure</span></span>

<span data-ttu-id="551cb-132">下表描述按鈕控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="551cb-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="551cb-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="551cb-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="551cb-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="551cb-134">Control View</span></span></th>
<th><span data-ttu-id="551cb-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="551cb-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="551cb-136">按鈕</span><span class="sxs-lookup"><span data-stu-id="551cb-136">Button</span></span>
<ul>
<li><span data-ttu-id="551cb-137">影像 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="551cb-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="551cb-138">文字 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="551cb-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="551cb-139">按鈕</span><span class="sxs-lookup"><span data-stu-id="551cb-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="551cb-140">相關屬性</span><span class="sxs-lookup"><span data-stu-id="551cb-140">Relevant Properties</span></span>

<span data-ttu-id="551cb-141">下表列出消費者介面自動化屬性，其值或定義與執行 **按鈕** 控制項 (類型的控制項（例如按鈕控制項) ）特別相關。</span><span class="sxs-lookup"><span data-stu-id="551cb-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="551cb-142">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="551cb-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="551cb-143">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="551cb-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="551cb-144">值</span><span class="sxs-lookup"><span data-stu-id="551cb-144">Value</span></span>      | <span data-ttu-id="551cb-145">注意</span><span class="sxs-lookup"><span data-stu-id="551cb-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="551cb-146">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="551cb-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-147">See notes.</span></span> | <span data-ttu-id="551cb-148">按鈕控制項通常支援快速鍵，讓使用者能夠快速地從鍵盤執行按鈕所代表的動作。</span><span class="sxs-lookup"><span data-stu-id="551cb-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="551cb-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="551cb-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-150">See notes.</span></span> | <span data-ttu-id="551cb-151">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="551cb-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="551cb-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="551cb-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-153">See notes.</span></span> | <span data-ttu-id="551cb-154">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="551cb-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="551cb-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="551cb-156">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-156">See notes.</span></span> | <span data-ttu-id="551cb-157">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="551cb-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="551cb-158">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="551cb-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="551cb-159">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="551cb-160">**按鈕**</span><span class="sxs-lookup"><span data-stu-id="551cb-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="551cb-161">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="551cb-162">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-162">See notes.</span></span> | <span data-ttu-id="551cb-163">解說文字應該會指出啟用按鈕的最終結果是什麼。</span><span class="sxs-lookup"><span data-stu-id="551cb-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="551cb-164">這通常是透過工具提示顯示的相同類型資訊。</span><span class="sxs-lookup"><span data-stu-id="551cb-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="551cb-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="551cb-166">true</span><span class="sxs-lookup"><span data-stu-id="551cb-166">TRUE</span></span>       | <span data-ttu-id="551cb-167">按鈕控制項必須一律為內容。</span><span class="sxs-lookup"><span data-stu-id="551cb-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="551cb-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="551cb-169">true</span><span class="sxs-lookup"><span data-stu-id="551cb-169">TRUE</span></span>       | <span data-ttu-id="551cb-170">按鈕控制項必須一律為控制項。</span><span class="sxs-lookup"><span data-stu-id="551cb-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="551cb-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="551cb-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-172">See notes.</span></span> | <span data-ttu-id="551cb-173">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="551cb-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="551cb-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="551cb-175">Null</span><span class="sxs-lookup"><span data-stu-id="551cb-175">Null</span></span>       | <span data-ttu-id="551cb-176">按鈕控制項會自行將其內容設為標籤。</span><span class="sxs-lookup"><span data-stu-id="551cb-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="551cb-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="551cb-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-178">See notes.</span></span> | <span data-ttu-id="551cb-179">對應到 **按鈕** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="551cb-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="551cb-180">針對 en-us 或英文 (美國) ，預設值為 "button"。</span><span class="sxs-lookup"><span data-stu-id="551cb-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="551cb-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="551cb-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="551cb-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-182">See notes.</span></span> | <span data-ttu-id="551cb-183">按鈕控制項的名稱是用來加上標籤的文字。</span><span class="sxs-lookup"><span data-stu-id="551cb-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="551cb-184">只要使用影像來標記按鈕，就必須為按鈕的 [ **名稱** ] 屬性提供替代文字。</span><span class="sxs-lookup"><span data-stu-id="551cb-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="551cb-185">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="551cb-185">Required Control Patterns</span></span>

<span data-ttu-id="551cb-186">下表列出所有按鈕控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="551cb-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="551cb-187">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="551cb-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="551cb-188">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="551cb-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="551cb-189">支援/值</span><span class="sxs-lookup"><span data-stu-id="551cb-189">Support/Value</span></span> | <span data-ttu-id="551cb-190">備註</span><span class="sxs-lookup"><span data-stu-id="551cb-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="551cb-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="551cb-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="551cb-192">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-192">See notes.</span></span>    | <span data-ttu-id="551cb-193">當按鈕裝載為分割按鈕的子系時，子按鈕可以支援[ExpandCollapse](uiauto-implementingexpandcollapse.md)控制項模式，而不是叫[用或](uiauto-implementinginvoke.md)[切換](uiauto-implementingtoggle.md)控制項模式。</span><span class="sxs-lookup"><span data-stu-id="551cb-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="551cb-194">ExpandCollapse 控制項模式可用來開啟或關閉功能表，或與 button 元素相關聯的其他子結構。</span><span class="sxs-lookup"><span data-stu-id="551cb-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="551cb-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="551cb-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="551cb-196">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-196">See notes.</span></span>    | <span data-ttu-id="551cb-197">所有按鈕都應該支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式或 [開關](uiauto-implementingtoggle.md) 控制項模式，但不能同時支援兩者。</span><span class="sxs-lookup"><span data-stu-id="551cb-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="551cb-198">當按鈕在要求使用者時執行命令時，必須支援 Invoke 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="551cb-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="551cb-199">此命令對應於如「剪下」、「複製」、「貼上」或「刪除」等單一作業。</span><span class="sxs-lookup"><span data-stu-id="551cb-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="551cb-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="551cb-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="551cb-201">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="551cb-201">See notes.</span></span>    | <span data-ttu-id="551cb-202">所有按鈕都應該支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式或 [開關](uiauto-implementingtoggle.md) 控制項模式，但不能同時支援兩者。</span><span class="sxs-lookup"><span data-stu-id="551cb-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="551cb-203">如果按鈕可以迴圈處理最多三個狀態的一連串，則必須支援切換控制項模式。</span><span class="sxs-lookup"><span data-stu-id="551cb-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="551cb-204">這通常是指特定功能的開關切換。</span><span class="sxs-lookup"><span data-stu-id="551cb-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="551cb-205">必要的事件</span><span class="sxs-lookup"><span data-stu-id="551cb-205">Required Events</span></span>

<span data-ttu-id="551cb-206">下表列出按鈕控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="551cb-207">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="551cb-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="551cb-208">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="551cb-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="551cb-209">備註</span><span class="sxs-lookup"><span data-stu-id="551cb-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="551cb-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="551cb-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="551cb-211">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="551cb-212">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="551cb-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="551cb-213">如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="551cb-214">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="551cb-215">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="551cb-216">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="551cb-217">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="551cb-218">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="551cb-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="551cb-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="551cb-220">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="551cb-221">如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="551cb-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="551cb-222">相關主題</span><span class="sxs-lookup"><span data-stu-id="551cb-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="551cb-223">**概念**</span><span class="sxs-lookup"><span data-stu-id="551cb-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="551cb-224">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="551cb-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="551cb-225">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="551cb-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




