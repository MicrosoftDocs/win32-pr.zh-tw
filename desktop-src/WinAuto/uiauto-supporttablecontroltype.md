---
title: Table 控制項類型
description: 本主題提供 Microsoft 消費者介面自動化 Table 控制項類型支援的相關資訊。
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- 消費者介面自動化，支援 Table 控制項類型
- 消費者介面自動化，Table 控制項類型
- 消費者介面自動化，Table 控制項類型的樹狀結構
- 消費者介面自動化，Table 控制項類型的屬性
- 消費者介面自動化，資料表控制項類型的控制項模式
- 消費者介面自動化，Table 控制項類型的事件
- 樹狀結構，資料表控制項類型
- properties、Table 控制項類型
- 控制項模式，資料表控制項類型
- events、Table 控制項類型
- Table 控制項類型的支援
- Table 控制項類型
- 控制項類型，資料表控制項類型的樹狀結構
- 控制項類型，資料表控制項類型的控制項模式
- 控制項類型，支援資料表
- 控制項類型，資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507340"
---
# <a name="table-control-type"></a><span data-ttu-id="ebeca-119">Table 控制項類型</span><span class="sxs-lookup"><span data-stu-id="ebeca-119">Table Control Type</span></span>

<span data-ttu-id="ebeca-120">本主題提供 Microsoft 消費者介面自動化 **Table** 控制項類型支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ebeca-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="ebeca-121">資料表控制項包含文字的資料列和資料行，以及選擇性的資料列標頭和資料行標頭。</span><span class="sxs-lookup"><span data-stu-id="ebeca-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="ebeca-122">下列章節會定義 **資料表** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="ebeca-123">消費者介面自動化需求適用于所有資料表控制項，其中 UI 架構/平臺會將控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="ebeca-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ebeca-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ebeca-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ebeca-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ebeca-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ebeca-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ebeca-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ebeca-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ebeca-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ebeca-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ebeca-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ebeca-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebeca-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ebeca-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ebeca-130">Typical Tree Structure</span></span>

<span data-ttu-id="ebeca-131">下表描述與資料表控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="ebeca-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ebeca-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ebeca-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ebeca-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="ebeca-133">Control View</span></span></th>
<th><span data-ttu-id="ebeca-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="ebeca-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ebeca-135">資料表</span><span class="sxs-lookup"><span data-stu-id="ebeca-135">Table</span></span>
<ul>
<li><span data-ttu-id="ebeca-136">文字 (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="ebeca-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="ebeca-137">標頭 (0 或更多) </span><span class="sxs-lookup"><span data-stu-id="ebeca-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="ebeca-138">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="ebeca-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ebeca-139">資料表</span><span class="sxs-lookup"><span data-stu-id="ebeca-139">Table</span></span>
<ul>
<li><span data-ttu-id="ebeca-140">文字 (1 或更多) </span><span class="sxs-lookup"><span data-stu-id="ebeca-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="ebeca-141">不同控制項 (0 或更多)</span><span class="sxs-lookup"><span data-stu-id="ebeca-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ebeca-142">如果資料表控制項具有資料列或資料行標頭，就必須在消費者介面自動化樹狀結構的控制項視圖中公開這些標頭。</span><span class="sxs-lookup"><span data-stu-id="ebeca-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="ebeca-143">內容視圖不需要公開此資訊，因為它可以使用 [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern)存取。</span><span class="sxs-lookup"><span data-stu-id="ebeca-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="ebeca-144">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ebeca-144">Relevant Properties</span></span>

<span data-ttu-id="ebeca-145">下表列出消費者介面自動化屬性，其值或定義與資料表控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="ebeca-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="ebeca-146">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="ebeca-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ebeca-147">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="ebeca-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ebeca-148">值</span><span class="sxs-lookup"><span data-stu-id="ebeca-148">Value</span></span>      | <span data-ttu-id="ebeca-149">注意</span><span class="sxs-lookup"><span data-stu-id="ebeca-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebeca-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ebeca-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-151">See notes.</span></span> | <span data-ttu-id="ebeca-152">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ebeca-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="ebeca-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ebeca-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-154">See notes.</span></span> | <span data-ttu-id="ebeca-155">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="ebeca-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="ebeca-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ebeca-157">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-157">See notes.</span></span> | <span data-ttu-id="ebeca-158">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="ebeca-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="ebeca-159">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="ebeca-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="ebeca-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ebeca-161">**資料表**</span><span class="sxs-lookup"><span data-stu-id="ebeca-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ebeca-162">**UIA \_ DescribedByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ebeca-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-163">See notes.</span></span> | <span data-ttu-id="ebeca-164">如果此資料表是由其他使用者介面項目 (例如保留資料表描述的文字項目) 所標註，則 DescribedBy 屬性應公開對文字控制項之自動化項目的參考。</span><span class="sxs-lookup"><span data-stu-id="ebeca-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="ebeca-165">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="ebeca-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-166">See notes.</span></span> | <span data-ttu-id="ebeca-167">如需更多有關資料表用途的詳細資料，請透過此屬性公開（如果 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性未充分說明）。</span><span class="sxs-lookup"><span data-stu-id="ebeca-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="ebeca-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ebeca-169">true</span><span class="sxs-lookup"><span data-stu-id="ebeca-169">TRUE</span></span>       | <span data-ttu-id="ebeca-170">Table 控制項必須一律出現在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="ebeca-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="ebeca-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ebeca-172">true</span><span class="sxs-lookup"><span data-stu-id="ebeca-172">TRUE</span></span>       | <span data-ttu-id="ebeca-173">Table 控制項必須一律出現在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="ebeca-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="ebeca-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ebeca-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-175">See notes.</span></span> | <span data-ttu-id="ebeca-176">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ebeca-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="ebeca-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ebeca-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-178">See notes.</span></span> | <span data-ttu-id="ebeca-179">如果有靜態文字標籤，則此屬性應公開對控制項之自動化項目的參考。</span><span class="sxs-lookup"><span data-stu-id="ebeca-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="ebeca-180">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ebeca-181">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-181">See notes.</span></span> | <span data-ttu-id="ebeca-182">對應至 **Table** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="ebeca-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="ebeca-183">預設值為 "table" 代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="ebeca-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="ebeca-184">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ebeca-185">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ebeca-185">See notes.</span></span> | <span data-ttu-id="ebeca-186">Table 控制項通常會從靜態文字標籤取得其名稱的值。</span><span class="sxs-lookup"><span data-stu-id="ebeca-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="ebeca-187">如果沒有靜態文字標籤，則專案必須指派名稱屬性，該屬性必須永遠可用來說明資料表的用途。</span><span class="sxs-lookup"><span data-stu-id="ebeca-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ebeca-188">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ebeca-188">Required Control Patterns</span></span>

<span data-ttu-id="ebeca-189">下表列出所有資料表控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="ebeca-190">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ebeca-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ebeca-191">控制項模式</span><span class="sxs-lookup"><span data-stu-id="ebeca-191">Control Pattern</span></span>                                         | <span data-ttu-id="ebeca-192">支援</span><span class="sxs-lookup"><span data-stu-id="ebeca-192">Support</span></span>                     | <span data-ttu-id="ebeca-193">注意</span><span class="sxs-lookup"><span data-stu-id="ebeca-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebeca-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ebeca-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="ebeca-195">必要</span><span class="sxs-lookup"><span data-stu-id="ebeca-195">Required</span></span>                    | <span data-ttu-id="ebeca-196">因為資料表控制項包含在方格中顯示的專案，所以它一律支援 [方格](uiauto-implementinggrid.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="ebeca-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ebeca-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="ebeca-198">需要有子物件</span><span class="sxs-lookup"><span data-stu-id="ebeca-198">Required with child objects</span></span> | <span data-ttu-id="ebeca-199">資料表的內建物件應同時支援 [GridItem](uiauto-implementinggriditem.md) 和 [TableItem](uiauto-implementingtableitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="ebeca-200">除非資料表是另一個資料表的一部分，否則資料表本身不需要支援 GridItem 或 TableItem 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="ebeca-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="ebeca-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="ebeca-202">必要</span><span class="sxs-lookup"><span data-stu-id="ebeca-202">Required</span></span>                    | <span data-ttu-id="ebeca-203">Table 控制項一律可以有與內容相關聯的標頭。</span><span class="sxs-lookup"><span data-stu-id="ebeca-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="ebeca-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ebeca-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="ebeca-205">需要有子物件</span><span class="sxs-lookup"><span data-stu-id="ebeca-205">Required with child objects</span></span> | <span data-ttu-id="ebeca-206">資料表的內建物件應同時支援 [GridItem](uiauto-implementinggriditem.md) 和 [TableItem](uiauto-implementingtableitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="ebeca-207">除非此資料表是另一個資料表的一部份，否則資料表本身不需要支援 GridItem 或 TableItem 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ebeca-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ebeca-208">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ebeca-208">Required Events</span></span>

<span data-ttu-id="ebeca-209">下表列出支援資料表控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="ebeca-210">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="ebeca-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ebeca-211">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="ebeca-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ebeca-212">備註</span><span class="sxs-lookup"><span data-stu-id="ebeca-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ebeca-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="ebeca-214">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="ebeca-215">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ebeca-216">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="ebeca-217">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ebeca-218">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ebeca-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="ebeca-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ebeca-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="ebeca-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="ebeca-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ebeca-221">**概念**</span><span class="sxs-lookup"><span data-stu-id="ebeca-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ebeca-222">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="ebeca-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ebeca-223">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="ebeca-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




