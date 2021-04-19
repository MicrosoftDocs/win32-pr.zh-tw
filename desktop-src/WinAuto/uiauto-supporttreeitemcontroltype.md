---
title: TreeItem 控制項類型
description: 本主題提供 TreeItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- 消費者介面自動化，TreeItem 控制項類型的支援
- 消費者介面自動化，TreeItem 控制項類型
- 消費者介面自動化，TreeItem 控制項類型的樹狀結構
- 消費者介面自動化，TreeItem 控制項類型的屬性
- 消費者介面自動化，TreeItem 控制項類型的控制項模式
- 消費者介面自動化，TreeItem 控制項類型的事件
- 樹狀結構，TreeItem 控制項類型
- properties、TreeItem 控制項類型
- 控制項模式，TreeItem 控制項類型
- events、TreeItem 控制項類型
- TreeItem 控制項類型的支援
- TreeItem 控制項類型
- 控制項類型，TreeItem 控制項類型的樹狀結構
- 控制項類型，TreeItem 控制項類型的控制項模式
- 控制項類型，支援 TreeItem
- 控制項類型，TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966814"
---
# <a name="treeitem-control-type"></a><span data-ttu-id="46d53-119">TreeItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="46d53-119">TreeItem Control Type</span></span>

<span data-ttu-id="46d53-120">本主題提供 **TreeItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="46d53-120">This topic provides information about Microsoft UI Automation support for the **TreeItem** control type.</span></span>

<span data-ttu-id="46d53-121">**TreeItem** 控制項類型代表樹狀結構容器內的節點。</span><span class="sxs-lookup"><span data-stu-id="46d53-121">The **TreeItem** control type represents a node within a tree container.</span></span> <span data-ttu-id="46d53-122">每個節點都可能包含其他節點，稱為「子節點」。</span><span class="sxs-lookup"><span data-stu-id="46d53-122">Each node might contain other nodes, called child nodes.</span></span> <span data-ttu-id="46d53-123">父節點或包含子節點的節點可以顯示為展開或摺疊。</span><span class="sxs-lookup"><span data-stu-id="46d53-123">Parent nodes, or nodes that contain child nodes, can be displayed as expanded or collapsed.</span></span>

<span data-ttu-id="46d53-124">下列章節會定義 **TreeItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TreeItem** control type.</span></span> <span data-ttu-id="46d53-125">消費者介面自動化需求適用于所有樹狀結構專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="46d53-125">The UI Automation requirements apply to all tree item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="46d53-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="46d53-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="46d53-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="46d53-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="46d53-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="46d53-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="46d53-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="46d53-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="46d53-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="46d53-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="46d53-131">備註</span><span class="sxs-lookup"><span data-stu-id="46d53-131">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="46d53-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="46d53-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="46d53-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="46d53-133">Typical Tree Structure</span></span>

<span data-ttu-id="46d53-134">下表描述樹狀結構專案控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="46d53-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to tree item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="46d53-135">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="46d53-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="46d53-136">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="46d53-136">Control View</span></span></th>
<th><span data-ttu-id="46d53-137">內容檢視</span><span class="sxs-lookup"><span data-stu-id="46d53-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="46d53-138">TreeItem</span><span class="sxs-lookup"><span data-stu-id="46d53-138">TreeItem</span></span>
<ul>
<li><span data-ttu-id="46d53-139">核取方塊 (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="46d53-139">CheckBox (0 or 1)</span></span></li>
<li><span data-ttu-id="46d53-140">Image (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="46d53-140">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="46d53-141">按鈕 (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="46d53-141">Button (0 or 1)</span></span></li>
<li><span data-ttu-id="46d53-142">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="46d53-142">TreeItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="46d53-143">TreeItem</span><span class="sxs-lookup"><span data-stu-id="46d53-143">TreeItem</span></span>
<ul>
<li><span data-ttu-id="46d53-144">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="46d53-144">TreeItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="46d53-145">樹狀結構專案控制項在消費者介面自動化樹狀結構的內容視圖中可以有零或多個樹狀目錄專案子系。</span><span class="sxs-lookup"><span data-stu-id="46d53-145">Tree item controls can have zero or more tree item children in the content view of the UI Automation tree.</span></span> <span data-ttu-id="46d53-146">如果樹狀結構專案控制項的功能超出下列控制項模式所公開的功能，則控制項應以 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型為基礎。</span><span class="sxs-lookup"><span data-stu-id="46d53-146">If the tree item control has functionality beyond what is exposed in the control patterns listed below, the control should be based on the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

<span data-ttu-id="46d53-147">折迭樹狀結構專案在展開和可見之前都不會出現在控制項視圖或內容視圖中， (或可滾動) 。</span><span class="sxs-lookup"><span data-stu-id="46d53-147">Collapsed tree items do not appear in the control view or content view until they become expanded and visible (or can be scrolled into view).</span></span>

<span data-ttu-id="46d53-148">控制項檢視可以包含控制項的額外詳細資訊，包括相關的影像或按鈕。</span><span class="sxs-lookup"><span data-stu-id="46d53-148">The control view can contain additional details for a control, including an associated image or a button.</span></span> <span data-ttu-id="46d53-149">例如，大綱模式中的項目可能包含展開或摺疊大綱的影像以及按鈕。</span><span class="sxs-lookup"><span data-stu-id="46d53-149">For example, an item in an outline view might contain an image as well as a button to expand or collapse the outline.</span></span> <span data-ttu-id="46d53-150">這些詳細資料物件不會出現在內容視圖中，因為該資訊已經以父樹狀結構專案表示。</span><span class="sxs-lookup"><span data-stu-id="46d53-150">These detail objects do not appear in the content view because the information is already represented by the parent tree item.</span></span>

<span data-ttu-id="46d53-151">滾動畫面的樹狀目錄專案會同時出現在消費者介面自動化樹狀結構的控制項和內容視圖中，且 [**IUIAutomationElement：： CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (或 [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) 屬性必須設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="46d53-151">Tree items that are scrolled off the screen appear in both the control and content views of the UI Automation tree and should have the [**IUIAutomationElement::CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (or [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) property set to **TRUE**.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="46d53-152">相關屬性</span><span class="sxs-lookup"><span data-stu-id="46d53-152">Relevant Properties</span></span>

<span data-ttu-id="46d53-153">下表列出消費者介面自動化屬性，其值或定義與 **TreeItem** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="46d53-153">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TreeItem** control type.</span></span> <span data-ttu-id="46d53-154">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="46d53-154">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="46d53-155">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="46d53-155">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="46d53-156">值</span><span class="sxs-lookup"><span data-stu-id="46d53-156">Value</span></span>        | <span data-ttu-id="46d53-157">注意</span><span class="sxs-lookup"><span data-stu-id="46d53-157">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46d53-158">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-158">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="46d53-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-159">See notes.</span></span>   | <span data-ttu-id="46d53-160">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="46d53-160">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                  |
| [<span data-ttu-id="46d53-161">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-161">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="46d53-162">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-162">See notes.</span></span>   | <span data-ttu-id="46d53-163">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="46d53-163">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                      |
| [<span data-ttu-id="46d53-164">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-164">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="46d53-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-165">See notes.</span></span>   | <span data-ttu-id="46d53-166">這個屬性必須傳回導致樹狀目錄專案變更選取狀態或成為焦點的位置。</span><span class="sxs-lookup"><span data-stu-id="46d53-166">This property must return a location that causes the tree item to change selection state or become focused.</span></span>                                                                                   |
| [<span data-ttu-id="46d53-167">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-167">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="46d53-168">**TreeItem**</span><span class="sxs-lookup"><span data-stu-id="46d53-168">**TreeItem**</span></span> | <span data-ttu-id="46d53-169">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="46d53-169">This value is the same for all UI frameworks.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="46d53-170">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-170">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="46d53-171">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="46d53-171">**TRUE**</span></span>     | <span data-ttu-id="46d53-172">樹狀目錄專案控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="46d53-172">The tree item control is always included in the content view of the UI Automation tree.</span></span>                                                                                                       |
| [<span data-ttu-id="46d53-173">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-173">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="46d53-174">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="46d53-174">**TRUE**</span></span>     | <span data-ttu-id="46d53-175">樹狀目錄專案控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="46d53-175">The tree item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                       |
| [<span data-ttu-id="46d53-176">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-176">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="46d53-177">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-177">See notes.</span></span>   | <span data-ttu-id="46d53-178">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="46d53-178">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                     |
| [<span data-ttu-id="46d53-179">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-179">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="46d53-180">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-180">See notes.</span></span>   | <span data-ttu-id="46d53-181">這個屬性會指出樹狀目錄專案控制項是否會在螢幕上向外滾動。</span><span class="sxs-lookup"><span data-stu-id="46d53-181">This property indicates whether a tree item control is scrolled off the screen.</span></span>                                                                                                               |
| [<span data-ttu-id="46d53-182">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-182">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="46d53-183">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-183">See notes.</span></span>   | <span data-ttu-id="46d53-184">如果控制項包含動態更新的狀態，則必須支援此屬性，以便在元素的狀態變更時，輔助技術可以接收更新。</span><span class="sxs-lookup"><span data-stu-id="46d53-184">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span> |
| [<span data-ttu-id="46d53-185">**UIA \_ ItemTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-185">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="46d53-186">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-186">See notes.</span></span>   | <span data-ttu-id="46d53-187">如果樹狀結構專案控制項使用視覺化圖示來指出是特定類型的專案，就必須支援這個屬性，而且必須指定專案類型。</span><span class="sxs-lookup"><span data-stu-id="46d53-187">If the tree item control uses a visual icon to indicate that is a particular type of item, this property must be supported and must indicate the item type.</span></span>                                   |
| [<span data-ttu-id="46d53-188">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-188">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="46d53-189">**NULL**</span><span class="sxs-lookup"><span data-stu-id="46d53-189">**NULL**</span></span>     | <span data-ttu-id="46d53-190">樹狀結構項目控制項會自行設定標籤。</span><span class="sxs-lookup"><span data-stu-id="46d53-190">Tree item controls are self-labeling.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="46d53-191">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-191">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="46d53-192">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-192">See notes.</span></span>   | <span data-ttu-id="46d53-193">對應到 TreeItem 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="46d53-193">Localized string corresponding to the TreeItem control type.</span></span> <span data-ttu-id="46d53-194">預設值為 en-us 或英文 (美國) 的「樹狀專案」。</span><span class="sxs-lookup"><span data-stu-id="46d53-194">The default value is "tree item" for en-US or English (United States).</span></span>                                                           |
| [<span data-ttu-id="46d53-195">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="46d53-195">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="46d53-196">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="46d53-196">See notes.</span></span>   | <span data-ttu-id="46d53-197">此屬性會公開每個樹狀結構項目控制項顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="46d53-197">This property exposes the text displayed for each tree item control.</span></span>                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="46d53-198">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="46d53-198">Required Control Patterns</span></span>

<span data-ttu-id="46d53-199">下表列出所有樹狀專案控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="46d53-199">The following table lists the UI Automation control patterns required to be supported by all tree item controls.</span></span> <span data-ttu-id="46d53-200">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="46d53-200">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="46d53-201">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="46d53-201">Control Pattern/Pattern Property</span></span>                                                  | <span data-ttu-id="46d53-202">支援/值</span><span class="sxs-lookup"><span data-stu-id="46d53-202">Support/Value</span></span>                     | <span data-ttu-id="46d53-203">備註</span><span class="sxs-lookup"><span data-stu-id="46d53-203">Notes</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46d53-204">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="46d53-204">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | <span data-ttu-id="46d53-205">必要</span><span class="sxs-lookup"><span data-stu-id="46d53-205">Required</span></span>                          | <span data-ttu-id="46d53-206">所有樹狀目錄專案都必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，因為所有專案都可以展開或折迭。</span><span class="sxs-lookup"><span data-stu-id="46d53-206">All tree items must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern because all items can be expanded or collapsed.</span></span>                                           |
| [<span data-ttu-id="46d53-207">**ExpandCollapseState**</span><span class="sxs-lookup"><span data-stu-id="46d53-207">**ExpandCollapseState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | <span data-ttu-id="46d53-208">已展開、已摺疊或分葉節點</span><span class="sxs-lookup"><span data-stu-id="46d53-208">Expanded, Collapsed, or Leaf Node</span></span> | <span data-ttu-id="46d53-209">當樹狀目錄專案未展開或折迭時，它們就是分葉節點。</span><span class="sxs-lookup"><span data-stu-id="46d53-209">Tree items are leaf nodes when they are not expanded or collapsed.</span></span>                                                                                                                                |
| [<span data-ttu-id="46d53-210">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="46d53-210">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | <span data-ttu-id="46d53-211">相依</span><span class="sxs-lookup"><span data-stu-id="46d53-211">Depends</span></span>                           | <span data-ttu-id="46d53-212">如果樹狀結構專案可以執行命令，請執行 [Invoke](uiauto-implementinginvoke.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="46d53-212">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the tree item can perform a command.</span></span>                                                                                     |
| [<span data-ttu-id="46d53-213">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="46d53-213">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | <span data-ttu-id="46d53-214">相依</span><span class="sxs-lookup"><span data-stu-id="46d53-214">Depends</span></span>                           | <span data-ttu-id="46d53-215">如果樹狀結構容器支援[滾動](uiauto-implementingscroll.md)條控制項模式，請執行[ScrollItem](uiauto-implementingscrollitem.md)控制項模式。</span><span class="sxs-lookup"><span data-stu-id="46d53-215">Implement the [ScrollItem](uiauto-implementingscrollitem.md) control pattern if the tree container supports the [Scroll](uiauto-implementingscroll.md) control pattern.</span></span>                         |
| [<span data-ttu-id="46d53-216">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="46d53-216">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | <span data-ttu-id="46d53-217">相依</span><span class="sxs-lookup"><span data-stu-id="46d53-217">Depends</span></span>                           | <span data-ttu-id="46d53-218">如果有可能會在使用者返回樹狀結構容器時維持作用中的選取範圍，請執行 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="46d53-218">Implement the [SelectionItem](uiauto-implementingselectionitem.md) control pattern if it is possible to have an active selection that is maintained when the user returns to the tree container.</span></span> |
| [<span data-ttu-id="46d53-219">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="46d53-219">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | <span data-ttu-id="46d53-220">必要</span><span class="sxs-lookup"><span data-stu-id="46d53-220">Required</span></span>                          | <span data-ttu-id="46d53-221">這個屬性會針對容器內的所有專案公開相同的容器。</span><span class="sxs-lookup"><span data-stu-id="46d53-221">This property exposes the same container for all items within the container.</span></span>                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="46d53-222">必要的事件</span><span class="sxs-lookup"><span data-stu-id="46d53-222">Required Events</span></span>

<span data-ttu-id="46d53-223">下表列出樹狀專案控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-223">The following table lists the UI Automation events that tree item controls are required to support.</span></span> <span data-ttu-id="46d53-224">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="46d53-224">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="46d53-225">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="46d53-225">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="46d53-226">備註</span><span class="sxs-lookup"><span data-stu-id="46d53-226">Notes</span></span>                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46d53-227">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-227">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| <span data-ttu-id="46d53-228">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-228">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                |
| <span data-ttu-id="46d53-229">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-229">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                                |
| [<span data-ttu-id="46d53-230">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-230">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="46d53-231">如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-231">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>               |
| <span data-ttu-id="46d53-232">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-232">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="46d53-233">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-233">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="46d53-234">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-234">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="46d53-235">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-235">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| <span data-ttu-id="46d53-236">[**UIA \_ItemStatusPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-236">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="46d53-237">如果控制項支援 [**ItemStatus**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-237">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>      |
| <span data-ttu-id="46d53-238">[**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-238">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                     | <span data-ttu-id="46d53-239">如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-239">If the control supports the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="46d53-240">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                |
| [<span data-ttu-id="46d53-241">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="46d53-242">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="46d53-243">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="46d53-244">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="46d53-245">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="46d53-246">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="46d53-247">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="46d53-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| <span data-ttu-id="46d53-248">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="46d53-249">如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>               |
| <span data-ttu-id="46d53-250">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="46d53-251">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="46d53-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="46d53-252">備註</span><span class="sxs-lookup"><span data-stu-id="46d53-252">Remarks</span></span>

<span data-ttu-id="46d53-253">如果樹狀結構專案有子系外框節點以外的子項目，則提供者必須謹慎且清楚地處理子物件資訊。</span><span class="sxs-lookup"><span data-stu-id="46d53-253">If a tree item has subelements other than child outline nodes, the provider must handle the child object information carefully and clearly.</span></span> <span data-ttu-id="46d53-254">在消費者介面自動化中，樹狀結構本身會處理樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="46d53-254">In UI Automation, the tree structure is handled by the tree hierarchy itself.</span></span> <span data-ttu-id="46d53-255">藉由有一或多個非外框節點的子系，兩者之間的差異和實際的子外框節點會變得很明確。</span><span class="sxs-lookup"><span data-stu-id="46d53-255">By having one or more non-outline-node children, the differences between them and actual child outline nodes becomes seriously ambiguous.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46d53-256">相關主題</span><span class="sxs-lookup"><span data-stu-id="46d53-256">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="46d53-257">**概念**</span><span class="sxs-lookup"><span data-stu-id="46d53-257">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46d53-258">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="46d53-258">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="46d53-259">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="46d53-259">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




