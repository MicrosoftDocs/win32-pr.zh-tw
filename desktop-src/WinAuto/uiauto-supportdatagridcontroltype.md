---
title: DataGrid 控制項類型
description: 本主題提供 DataGrid 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- 消費者介面自動化，DataGrid 控制項類型的支援
- 消費者介面自動化，DataGrid 控制項類型
- DataGrid 控制項類型的消費者介面自動化、樹狀結構
- 消費者介面自動化，DataGrid 控制項類型的屬性
- 消費者介面自動化，DataGrid 控制項類型的控制項模式
- 消費者介面自動化，DataGrid 控制項類型的事件
- 樹狀結構，DataGrid 控制項類型
- properties、DataGrid 控制項類型
- 控制項模式、DataGrid 控制項類型
- events、DataGrid 控制項類型
- DataGrid 控制項類型的支援
- DataGrid 控制項類型
- DataGrid 控制項類型的控制項類型、樹狀結構
- 控制項類型，DataGrid 控制項類型的控制項模式
- 控制項類型，支援 DataGrid
- 控制項類型，DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932149"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="0b7d7-119">DataGrid 控制項類型</span><span class="sxs-lookup"><span data-stu-id="0b7d7-119">DataGrid Control Type</span></span>

<span data-ttu-id="0b7d7-120">本主題提供 **DataGrid** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="0b7d7-121">**DataGrid** 控制項型別可讓使用者輕鬆地使用包含資料的專案或資料列中所呈現的自動化元素。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="0b7d7-122">資料格控制項具有項目資料列和關於這些項目的資訊資料行。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="0b7d7-123">Windows Vista Explorer 中的清單視圖控制項是支援 **DataGrid** 控制項類型的範例。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="0b7d7-124">下列章節會定義 **DataGrid** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="0b7d7-125">消費者介面自動化需求適用于所有資料格控制項，其中 UI framework/平臺會將控制項類型和控制項模式的消費者介面自動化支援整合。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0b7d7-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0b7d7-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0b7d7-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0b7d7-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0b7d7-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0b7d7-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0b7d7-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0b7d7-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0b7d7-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0b7d7-131">DataGrid 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="0b7d7-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="0b7d7-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b7d7-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0b7d7-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0b7d7-133">Typical Tree Structure</span></span>

<span data-ttu-id="0b7d7-134">下表描述與資料格控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0b7d7-135">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b7d7-136">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="0b7d7-136">Control View</span></span></th>
<th><span data-ttu-id="0b7d7-137">內容檢視</span><span class="sxs-lookup"><span data-stu-id="0b7d7-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0b7d7-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="0b7d7-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="0b7d7-139">標頭 (0、1 或 2)</span><span class="sxs-lookup"><span data-stu-id="0b7d7-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="0b7d7-140">HeaderItem (行數或列數)</span><span class="sxs-lookup"><span data-stu-id="0b7d7-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="0b7d7-141">DataItem (0 或以上;可以結構化在階層中) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0b7d7-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="0b7d7-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="0b7d7-143">DataItem (0 或以上;可以結構化在階層中) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0b7d7-144">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0b7d7-144">Relevant Properties</span></span>

<span data-ttu-id="0b7d7-145">下表列出消費者介面自動化屬性，其值或定義與 **DataGrid** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="0b7d7-146">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0b7d7-147">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="0b7d7-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0b7d7-148">值</span><span class="sxs-lookup"><span data-stu-id="0b7d7-148">Value</span></span>        | <span data-ttu-id="0b7d7-149">注意</span><span class="sxs-lookup"><span data-stu-id="0b7d7-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b7d7-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0b7d7-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-151">See notes.</span></span>   | <span data-ttu-id="0b7d7-152">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="0b7d7-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0b7d7-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-154">See notes.</span></span>   | <span data-ttu-id="0b7d7-155">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="0b7d7-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0b7d7-157">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-157">See notes.</span></span>   | <span data-ttu-id="0b7d7-158">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0b7d7-159">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="0b7d7-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0b7d7-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="0b7d7-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0b7d7-163">true</span><span class="sxs-lookup"><span data-stu-id="0b7d7-163">TRUE</span></span>         | <span data-ttu-id="0b7d7-164">這個屬性的值必須一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="0b7d7-165">這表示資料格控制項必須一律位於消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="0b7d7-166">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0b7d7-167">true</span><span class="sxs-lookup"><span data-stu-id="0b7d7-167">TRUE</span></span>         | <span data-ttu-id="0b7d7-168">這個屬性的值必須一律 **為 TRUE**。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="0b7d7-169">這表示資料格控制項必須一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="0b7d7-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0b7d7-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-171">See notes.</span></span>   | <span data-ttu-id="0b7d7-172">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="0b7d7-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0b7d7-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-174">See notes.</span></span>   | <span data-ttu-id="0b7d7-175">如果有靜態文字標籤，這個屬性必須公開該控制項的參考。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="0b7d7-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0b7d7-177">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-177">See notes.</span></span>   | <span data-ttu-id="0b7d7-178">對應至 **DataGrid** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="0b7d7-179">預設值為 en-us 或英文 (美國) 的「資料方格」。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="0b7d7-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0b7d7-181">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-181">See notes.</span></span>   | <span data-ttu-id="0b7d7-182">資料格控制項通常會從靜態文字標籤取得其 **Name** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="0b7d7-183">如果沒有靜態文字標籤，應用程式開發人員必須為 **Name** 屬性指派值。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="0b7d7-184">**Name** 屬性的值絕對不能是編輯控制項的文字內容。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0b7d7-185">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0b7d7-185">Required Control Patterns</span></span>

<span data-ttu-id="0b7d7-186">下表列出所有資料格控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="0b7d7-187">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0b7d7-188">控制項模式</span><span class="sxs-lookup"><span data-stu-id="0b7d7-188">Control Pattern</span></span>                                         | <span data-ttu-id="0b7d7-189">支援</span><span class="sxs-lookup"><span data-stu-id="0b7d7-189">Support</span></span>  | <span data-ttu-id="0b7d7-190">注意</span><span class="sxs-lookup"><span data-stu-id="0b7d7-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b7d7-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="0b7d7-192">必要</span><span class="sxs-lookup"><span data-stu-id="0b7d7-192">Required</span></span> | <span data-ttu-id="0b7d7-193">資料格控制項本身一律支援 [方格](uiauto-implementinggrid.md) 控制項模式，因為它所包含的專案具有在方格中配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="0b7d7-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="0b7d7-195">相依</span><span class="sxs-lookup"><span data-stu-id="0b7d7-195">Depends</span></span>  | <span data-ttu-id="0b7d7-196">資料格可捲動與否，會視內容以及是否有捲軸而定。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="0b7d7-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="0b7d7-198">相依</span><span class="sxs-lookup"><span data-stu-id="0b7d7-198">Depends</span></span>  | <span data-ttu-id="0b7d7-199">資料格可選取與否，視內容而定。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="0b7d7-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="0b7d7-201">相依</span><span class="sxs-lookup"><span data-stu-id="0b7d7-201">Depends</span></span>  | <span data-ttu-id="0b7d7-202">具有標頭的資料格控制項應支援 [Table](uiauto-implementingtable.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="0b7d7-203">資料格容器內的資料項目至少會支援：</span><span class="sxs-lookup"><span data-stu-id="0b7d7-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="0b7d7-204">[SelectionItem](uiauto-implementingselectionitem.md) 控制項模式 (如果資料格可供選取) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="0b7d7-205">[ScrollItem](uiauto-implementingscrollitem.md) 控制項模式 (如果資料格為可滾動) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="0b7d7-206">[GridItem](uiauto-implementinggriditem.md) 控制項模式</span><span class="sxs-lookup"><span data-stu-id="0b7d7-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="0b7d7-207">[TableItem](uiauto-implementingtableitem.md) 控制項模式 (如果資料格有標頭) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="0b7d7-208">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0b7d7-208">Required Events</span></span>

<span data-ttu-id="0b7d7-209">下表列出需要資料格控制項才能支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="0b7d7-210">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="0b7d7-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0b7d7-211">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="0b7d7-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="0b7d7-212">備註</span><span class="sxs-lookup"><span data-stu-id="0b7d7-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b7d7-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="0b7d7-214">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="0b7d7-215">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="0b7d7-216">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="0b7d7-217">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="0b7d7-218">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="0b7d7-219">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="0b7d7-220">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="0b7d7-221">[**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0b7d7-222">如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md) 控制項模式的 CurrentView 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="0b7d7-223">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="0b7d7-224">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0b7d7-225">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="0b7d7-226">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0b7d7-227">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="0b7d7-228">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0b7d7-229">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="0b7d7-230">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0b7d7-231">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="0b7d7-232">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="0b7d7-233">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="0b7d7-234">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="0b7d7-235">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="0b7d7-236">DataGrid 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="0b7d7-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="0b7d7-237">下圖說明可執行 **DataGrid** 控制項類型的清單視圖控制項。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![具有 datagrid 控制項類型之清單視圖控制項的螢幕擷取畫面](images/datagridxmpl.jpg)

<span data-ttu-id="0b7d7-239">以下顯示與清單視圖控制項相關之消費者介面自動化樹狀結構的控制項視圖和內容視圖。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="0b7d7-240">每個自動化項目的控制項模式顯示在括號中。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b7d7-241">消費者介面自動化樹狀結構控制項視圖</span><span class="sxs-lookup"><span data-stu-id="0b7d7-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="0b7d7-242">消費者介面自動化樹狀結構-內容視圖</span><span class="sxs-lookup"><span data-stu-id="0b7d7-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b7d7-243">DataGrid (排序、資料表、選取專案、格線) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="0b7d7-244">標頭</span><span class="sxs-lookup"><span data-stu-id="0b7d7-244">Header</span></span>
<ul>
<li><span data-ttu-id="0b7d7-245">HeaderItem &quot; Name &quot; (Invoke) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="0b7d7-246">HeaderItem &quot; 修改日期 &quot; (叫用) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="0b7d7-247">HeaderItem &quot; 大小 &quot; (叫用) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="0b7d7-248">群組 &quot; Contoso &quot; (TableItem、GridItem、SelectionItem、Table *、Grid*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="0b7d7-249">DataItem &quot; 帳戶 Receivable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="0b7d7-250">DataItem &quot; 帳戶 Payable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="0b7d7-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="0b7d7-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="0b7d7-252">群組 &quot; Contoso &quot; (TableItem、GridItem、SelectionItem、Table *、Grid*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="0b7d7-253">DataItem &quot; 帳戶 Receivable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="0b7d7-254">DataItem &quot; 帳戶 Payable.doc&quot; (SelectionItem、Invoke、TableItem *、GridItem*) </span><span class="sxs-lookup"><span data-stu-id="0b7d7-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="0b7d7-255">\*上述範例顯示包含多個控制項層級的資料格。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="0b7d7-256">**群組** ( "Contoso" ) 控制項包含兩個 **DataItem** 控制項 ( "accounts Receivable.doc" 和 "accounts Payable.doc" ) 。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="0b7d7-257">**DataGrid** / **GridItem** 組與另一個層級的配對無關。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="0b7d7-258">群組底下的 **DataItem** 控制項也可以公開為專案 **組合** 控制項 [類型](uiauto-supportlistitemcontroltype.md) ，讓它們更清楚地呈現為可選取的物件，而不是簡單的資料元素。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="0b7d7-259">本範例不包含群組資料項目的子項目。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="0b7d7-260">如需多個控制項層級的另一個範例，請參閱 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="0b7d7-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b7d7-261">相關主題</span><span class="sxs-lookup"><span data-stu-id="0b7d7-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0b7d7-262">**概念**</span><span class="sxs-lookup"><span data-stu-id="0b7d7-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0b7d7-263">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="0b7d7-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0b7d7-264">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="0b7d7-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




