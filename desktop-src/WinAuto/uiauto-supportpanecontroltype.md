---
title: 窗格控制項類型
description: 本主題提供窗格控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- 消費者介面自動化，窗格控制項類型的支援
- 消費者介面自動化，窗格控制項類型
- 窗格控制項類型的樹狀結構消費者介面自動化
- 消費者介面自動化，窗格控制項類型的屬性
- 消費者介面自動化，窗格控制項類型的控制項模式
- 消費者介面自動化，窗格控制項類型的事件
- 樹狀結構，窗格控制項類型
- 屬性，窗格控制項類型
- 控制項模式，窗格控制項類型
- 事件、窗格控制項類型
- 窗格控制項類型的支援
- Pane 控制項類型
- 控制項類型，窗格控制項類型的樹狀結構
- 控制項類型，窗格控制項類型的控制項模式
- 控制項類型，支援窗格
- 控制項類型，窗格
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104555122"
---
# <a name="pane-control-type"></a><span data-ttu-id="c8903-119">窗格控制項類型</span><span class="sxs-lookup"><span data-stu-id="c8903-119">Pane Control Type</span></span>

<span data-ttu-id="c8903-120">本主題提供 **窗格** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c8903-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="c8903-121">**窗格** 控制項類型適用于具有不同內容的潛在可捲動區域。</span><span class="sxs-lookup"><span data-stu-id="c8903-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="c8903-122">它是用來表示框架或文件視窗內的物件。</span><span class="sxs-lookup"><span data-stu-id="c8903-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="c8903-123">使用者可以在窗格控制項和目前窗格的內容中流覽。</span><span class="sxs-lookup"><span data-stu-id="c8903-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="c8903-124">窗格控制項表示比 windows 或檔更低的群組層級，但在個別控制項上方。</span><span class="sxs-lookup"><span data-stu-id="c8903-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="c8903-125">使用者在窗格之間巡覽的方式是依照內容而定，可按下 TAB、F6 或 CTRL+TAB 鍵。</span><span class="sxs-lookup"><span data-stu-id="c8903-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="c8903-126">下列章節會定義 **窗格** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="c8903-127">消費者介面自動化需求適用于所有窗格控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="c8903-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c8903-128">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="c8903-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c8903-129">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="c8903-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c8903-130">相關屬性</span><span class="sxs-lookup"><span data-stu-id="c8903-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c8903-131">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="c8903-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c8903-132">必要的事件</span><span class="sxs-lookup"><span data-stu-id="c8903-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c8903-133">窗格控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="c8903-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="c8903-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8903-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c8903-135">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="c8903-135">Typical Tree Structure</span></span>

<span data-ttu-id="c8903-136">下表描述的是與窗格控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="c8903-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c8903-137">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="c8903-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8903-138">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="c8903-138">Control View</span></span></th>
<th><span data-ttu-id="c8903-139">內容檢視</span><span class="sxs-lookup"><span data-stu-id="c8903-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c8903-140">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c8903-141">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c8903-142">窗格控制項一律會出現在控制項和內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="c8903-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="c8903-143">如果物件只用于視覺呈現，請勿將版面設定物件公開為控制項或內容視圖中的窗格。</span><span class="sxs-lookup"><span data-stu-id="c8903-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="c8903-144">相關屬性</span><span class="sxs-lookup"><span data-stu-id="c8903-144">Relevant Properties</span></span>

<span data-ttu-id="c8903-145">下表列出消費者介面自動化屬性，其值或定義與窗格控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="c8903-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="c8903-146">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="c8903-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c8903-147">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="c8903-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c8903-148">值</span><span class="sxs-lookup"><span data-stu-id="c8903-148">Value</span></span>      | <span data-ttu-id="c8903-149">注意</span><span class="sxs-lookup"><span data-stu-id="c8903-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8903-150">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c8903-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-151">See notes.</span></span> | <span data-ttu-id="c8903-152">如果特定的按鍵組合會讓焦點放在窗格中，則應該透過這個屬性公開該資訊。</span><span class="sxs-lookup"><span data-stu-id="c8903-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="c8903-153">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c8903-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-154">See notes.</span></span> | <span data-ttu-id="c8903-155">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c8903-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="c8903-156">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c8903-157">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-157">See notes.</span></span> | <span data-ttu-id="c8903-158">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="c8903-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c8903-159">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c8903-160">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-160">See notes.</span></span> | <span data-ttu-id="c8903-161">這個屬性會公開窗格控制項之可點選的點，當按一下該點時，窗格就會取得焦點。</span><span class="sxs-lookup"><span data-stu-id="c8903-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="c8903-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c8903-163">**窗格**</span><span class="sxs-lookup"><span data-stu-id="c8903-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="c8903-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="c8903-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-165">See notes.</span></span> | <span data-ttu-id="c8903-166">窗格控制項的解說文字應解釋框架的用途，以及它與其他畫面格的關聯方式。</span><span class="sxs-lookup"><span data-stu-id="c8903-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="c8903-167">如果畫面格的目的和關聯性不清楚來自 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性的值，就必須提供描述。</span><span class="sxs-lookup"><span data-stu-id="c8903-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="c8903-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c8903-169">true</span><span class="sxs-lookup"><span data-stu-id="c8903-169">TRUE</span></span>       | <span data-ttu-id="c8903-170">窗格控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="c8903-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c8903-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c8903-172">true</span><span class="sxs-lookup"><span data-stu-id="c8903-172">TRUE</span></span>       | <span data-ttu-id="c8903-173">窗格控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="c8903-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c8903-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c8903-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-175">See notes.</span></span> | <span data-ttu-id="c8903-176">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="c8903-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="c8903-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c8903-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-178">See notes.</span></span> | <span data-ttu-id="c8903-179">窗格控制項通常沒有靜態標籤。</span><span class="sxs-lookup"><span data-stu-id="c8903-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="c8903-180">如果有靜態文字標籤，則標籤應透過這個屬性公開。</span><span class="sxs-lookup"><span data-stu-id="c8903-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="c8903-181">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c8903-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-182">See notes.</span></span> | <span data-ttu-id="c8903-183">對應到 **窗格** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="c8903-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="c8903-184">預設值為 "pane"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="c8903-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="c8903-185">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c8903-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c8903-186">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c8903-186">See notes.</span></span> | <span data-ttu-id="c8903-187">這個屬性的值必須是清楚、精確且有意義的標題。</span><span class="sxs-lookup"><span data-stu-id="c8903-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c8903-188">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="c8903-188">Required Control Patterns</span></span>

<span data-ttu-id="c8903-189">下表列出窗格控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c8903-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="c8903-190">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="c8903-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c8903-191">控制項模式</span><span class="sxs-lookup"><span data-stu-id="c8903-191">Control Pattern</span></span>                                         | <span data-ttu-id="c8903-192">支援</span><span class="sxs-lookup"><span data-stu-id="c8903-192">Support</span></span> | <span data-ttu-id="c8903-193">注意</span><span class="sxs-lookup"><span data-stu-id="c8903-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8903-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="c8903-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="c8903-195">相依</span><span class="sxs-lookup"><span data-stu-id="c8903-195">Depends</span></span> | <span data-ttu-id="c8903-196">如果窗格控制項可以停駐，請執行停 [駐](uiauto-implementingdock.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c8903-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="c8903-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="c8903-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="c8903-198">相依</span><span class="sxs-lookup"><span data-stu-id="c8903-198">Depends</span></span> | <span data-ttu-id="c8903-199">如果窗格控制項可以滾動，請執行 [滾動](uiauto-implementingscroll.md) 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c8903-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="c8903-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="c8903-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="c8903-201">相依</span><span class="sxs-lookup"><span data-stu-id="c8903-201">Depends</span></span> | <span data-ttu-id="c8903-202">如果窗格控制項可以在螢幕上移動、調整大小或旋轉，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c8903-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="c8903-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="c8903-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="c8903-204">永不</span><span class="sxs-lookup"><span data-stu-id="c8903-204">Never</span></span>   | <span data-ttu-id="c8903-205">如果專案需要執行 [視窗](uiauto-implementingwindow.md) 控制項模式，則控制項應以 [視窗](uiauto-supportwindowcontroltype.md) 控制項類型為基礎。</span><span class="sxs-lookup"><span data-stu-id="c8903-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="c8903-206">必要的事件</span><span class="sxs-lookup"><span data-stu-id="c8903-206">Required Events</span></span>

<span data-ttu-id="c8903-207">下表列出支援的窗格控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="c8903-208">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="c8903-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c8903-209">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="c8903-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="c8903-210">備註</span><span class="sxs-lookup"><span data-stu-id="c8903-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8903-211">**UIA \_ AsyncContentLoadedEventId**</span><span class="sxs-lookup"><span data-stu-id="c8903-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="c8903-212">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c8903-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="c8903-213">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="c8903-214">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="c8903-215">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="c8903-216">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="c8903-217">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="c8903-218">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="c8903-219">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="c8903-220">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="c8903-221">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="c8903-222">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="c8903-223">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="c8903-224">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="c8903-225">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="c8903-226">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="c8903-227">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c8903-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="c8903-228">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c8903-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="c8903-229">窗格控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="c8903-229">Pane Control Type Example</span></span>

<span data-ttu-id="c8903-230">下圖說明可執行 **窗格** 控制項類型的控制項。</span><span class="sxs-lookup"><span data-stu-id="c8903-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![顯示窗格控制項範例的螢幕擷取畫面](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c8903-232">消費者介面自動化樹狀結構-控制項視圖</span><span class="sxs-lookup"><span data-stu-id="c8903-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="c8903-233">消費者介面自動化樹狀結構-內容視圖</span><span class="sxs-lookup"><span data-stu-id="c8903-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c8903-234">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-234">Pane</span></span>
<ul>
<li><span data-ttu-id="c8903-235">樹狀結構 (捲動模式)</span><span class="sxs-lookup"><span data-stu-id="c8903-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="c8903-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="c8903-236">TreeItem</span></span></li>
<li><span data-ttu-id="c8903-237">...</span><span class="sxs-lookup"><span data-stu-id="c8903-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="c8903-238">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-238">Pane</span></span>
<ul>
<li><span data-ttu-id="c8903-239">編輯 (捲軸模式) </span><span class="sxs-lookup"><span data-stu-id="c8903-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c8903-240">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-240">Pane</span></span>
<ul>
<li><span data-ttu-id="c8903-241">樹狀結構 (捲動模式)</span><span class="sxs-lookup"><span data-stu-id="c8903-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="c8903-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="c8903-242">TreeItem</span></span></li>
<li><span data-ttu-id="c8903-243">...</span><span class="sxs-lookup"><span data-stu-id="c8903-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="c8903-244">窗格</span><span class="sxs-lookup"><span data-stu-id="c8903-244">Pane</span></span>
<ul>
<li><span data-ttu-id="c8903-245">編輯 (捲軸模式) </span><span class="sxs-lookup"><span data-stu-id="c8903-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c8903-246">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8903-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8903-247">**概念**</span><span class="sxs-lookup"><span data-stu-id="c8903-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c8903-248">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="c8903-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c8903-249">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="c8903-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




