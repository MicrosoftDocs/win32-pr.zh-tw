---
title: DataItem 控制項類型
description: 本主題提供 DataItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- 消費者介面自動化，DataItem 控制項類型的支援
- 消費者介面自動化，DataItem 控制項類型
- 消費者介面自動化，DataItem 控制項類型的樹狀結構
- 消費者介面自動化，DataItem 控制項類型的屬性
- 消費者介面自動化，DataItem 控制項類型的控制項模式
- 消費者介面自動化，DataItem 控制項類型的事件
- 消費者介面自動化、大型清單和 DataItem 控制項類型
- 樹狀結構，DataItem 控制項類型
- properties、DataItem 控制項類型
- 控制項模式，DataItem 控制項類型
- events、DataItem 控制項類型
- 大型清單
- DataItem 控制項類型的支援
- DataItem 控制項類型
- 控制項類型，DataItem 控制項類型的樹狀結構
- 控制項類型，DataItem 控制項類型的控制項模式
- 控制項類型、大型清單和 DataItem 控制項類型
- 控制項類型，支援 DataItem
- 控制項類型，DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021343"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="4d52c-122">DataItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="4d52c-122">DataItem Control Type</span></span>

<span data-ttu-id="4d52c-123">本主題提供 **DataItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="4d52c-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="4d52c-124">連絡人清單中的項目即是資料項目控制項的範例。</span><span class="sxs-lookup"><span data-stu-id="4d52c-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="4d52c-125">資料項目控制項包含與使用者相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="4d52c-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="4d52c-126">由於包含更為豐富的資訊，這種控制項比簡單的清單項目複雜。</span><span class="sxs-lookup"><span data-stu-id="4d52c-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="4d52c-127">下列章節會定義 **DataItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="4d52c-128">消費者介面自動化需求適用于所有資料項目控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="4d52c-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4d52c-129">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="4d52c-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d52c-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4d52c-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4d52c-131">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4d52c-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4d52c-132">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4d52c-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4d52c-133">在大型清單中使用 Dataitem</span><span class="sxs-lookup"><span data-stu-id="4d52c-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="4d52c-134">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4d52c-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4d52c-135">DataItem 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="4d52c-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="4d52c-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d52c-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4d52c-137">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="4d52c-137">Typical Tree Structure</span></span>

<span data-ttu-id="4d52c-138">下表描述與資料項目控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的專案。</span><span class="sxs-lookup"><span data-stu-id="4d52c-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4d52c-139">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4d52c-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d52c-140">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="4d52c-140">Control View</span></span></th>
<th><span data-ttu-id="4d52c-141">內容檢視</span><span class="sxs-lookup"><span data-stu-id="4d52c-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4d52c-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="4d52c-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="4d52c-143">視情況而定 (0 個以上；可以結構化為階層)</span><span class="sxs-lookup"><span data-stu-id="4d52c-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d52c-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="4d52c-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="4d52c-145">視情況而定 (0 個以上；可以結構化為階層)</span><span class="sxs-lookup"><span data-stu-id="4d52c-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d52c-146">資料格中資料項目 (Item) 的項目 (Element) 可裝載各種不同的物件，包括另一層資料項目，或是特定資料格項目 (Element) 如文字、影像或編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="4d52c-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="4d52c-147">如果資料項目專案具有特定的物件角色，則元素應該公開為特定的控制項類型;例如，方格中可選取 [資料項目的專案類型控制項類型](uiauto-supportlistitemcontroltype.md) 。</span><span class="sxs-lookup"><span data-stu-id="4d52c-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="4d52c-148">相關屬性</span><span class="sxs-lookup"><span data-stu-id="4d52c-148">Relevant Properties</span></span>

<span data-ttu-id="4d52c-149">下表列出消費者介面自動化屬性，其值或定義與 DataItem 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="4d52c-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="4d52c-150">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="4d52c-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4d52c-151">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="4d52c-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4d52c-152">值</span><span class="sxs-lookup"><span data-stu-id="4d52c-152">Value</span></span>        | <span data-ttu-id="4d52c-153">注意</span><span class="sxs-lookup"><span data-stu-id="4d52c-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d52c-154">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4d52c-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-155">See notes.</span></span>   | <span data-ttu-id="4d52c-156">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="4d52c-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="4d52c-157">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4d52c-158">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-158">See notes.</span></span>   | <span data-ttu-id="4d52c-159">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="4d52c-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="4d52c-160">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4d52c-161">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-161">See notes.</span></span>   | <span data-ttu-id="4d52c-162">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="4d52c-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="4d52c-163">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="4d52c-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="4d52c-164">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4d52c-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="4d52c-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="4d52c-166">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4d52c-167">true</span><span class="sxs-lookup"><span data-stu-id="4d52c-167">TRUE</span></span>         | <span data-ttu-id="4d52c-168">資料項目控制項必須一律為內容。</span><span class="sxs-lookup"><span data-stu-id="4d52c-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="4d52c-169">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4d52c-170">true</span><span class="sxs-lookup"><span data-stu-id="4d52c-170">TRUE</span></span>         | <span data-ttu-id="4d52c-171">資料項目控制項必須一律為控制項。</span><span class="sxs-lookup"><span data-stu-id="4d52c-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="4d52c-172">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4d52c-173">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-173">See notes.</span></span>   | <span data-ttu-id="4d52c-174">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="4d52c-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="4d52c-175">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="4d52c-176">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-176">See notes.</span></span>   | <span data-ttu-id="4d52c-177">如果控制項包含動態更新的狀態，則必須支援此屬性，以便在元素的狀態變更時，輔助技術可以接收更新。</span><span class="sxs-lookup"><span data-stu-id="4d52c-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="4d52c-178">**UIA \_ ItemTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="4d52c-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-179">See notes.</span></span>   | <span data-ttu-id="4d52c-180">這個字串值可讓使用者知道項目所代表的物件為何。</span><span class="sxs-lookup"><span data-stu-id="4d52c-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="4d52c-181">範例包括 "Media File" 和 "Contact"。</span><span class="sxs-lookup"><span data-stu-id="4d52c-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="4d52c-182">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4d52c-183">Null</span><span class="sxs-lookup"><span data-stu-id="4d52c-183">Null</span></span>         | <span data-ttu-id="4d52c-184">資料項目控制項沒有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="4d52c-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="4d52c-185">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4d52c-186">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-186">See notes.</span></span>   | <span data-ttu-id="4d52c-187">對應到 **DataItem** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="4d52c-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="4d52c-188">預設值為 en-us 或英文 (美國) 的「資料項目」。</span><span class="sxs-lookup"><span data-stu-id="4d52c-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="4d52c-189">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4d52c-190">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="4d52c-190">See notes.</span></span>   | <span data-ttu-id="4d52c-191">資料項目控制項一律會包含主要文字專案，使用者會將它辨識為專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4d52c-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4d52c-192">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="4d52c-192">Required Control Patterns</span></span>

<span data-ttu-id="4d52c-193">下表列出所有資料項目控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="4d52c-194">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="4d52c-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4d52c-195">控制項模式</span><span class="sxs-lookup"><span data-stu-id="4d52c-195">Control Pattern</span></span>                                                   | <span data-ttu-id="4d52c-196">支援</span><span class="sxs-lookup"><span data-stu-id="4d52c-196">Support</span></span> | <span data-ttu-id="4d52c-197">注意</span><span class="sxs-lookup"><span data-stu-id="4d52c-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d52c-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="4d52c-199">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-199">Depends</span></span> | <span data-ttu-id="4d52c-200">如果資料項目目可展開或折迭以顯示和隱藏資訊，則必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="4d52c-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="4d52c-202">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-202">Depends</span></span> | <span data-ttu-id="4d52c-203">當可在空間中導覽專案的容器內有資料項目集合可供使用時，資料項目將會支援 [GridItem](uiauto-implementinggriditem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="4d52c-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="4d52c-205">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-205">Depends</span></span> | <span data-ttu-id="4d52c-206">所有資料項目都支援當其資料容器的專案數目超過螢幕上可容納的專案時，能夠使用 [ScrollItem](uiauto-implementingscrollitem.md) 控制項模式來滾動查看。</span><span class="sxs-lookup"><span data-stu-id="4d52c-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="4d52c-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="4d52c-208">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-208">Depends</span></span> | <span data-ttu-id="4d52c-209">選取資料項目的能力視內容而定。</span><span class="sxs-lookup"><span data-stu-id="4d52c-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="4d52c-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="4d52c-211">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-211">Depends</span></span> | <span data-ttu-id="4d52c-212">如果資料項目包含在具有 header 專案的 [DataGrid](uiauto-supportdatagridcontroltype.md) 控制項類型中，它應該支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="4d52c-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="4d52c-214">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-214">Depends</span></span> | <span data-ttu-id="4d52c-215">如果資料項目包含可迴圈的狀態，則它應該支援 [切換](uiauto-implementingtoggle.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="4d52c-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="4d52c-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="4d52c-217">相依</span><span class="sxs-lookup"><span data-stu-id="4d52c-217">Depends</span></span> | <span data-ttu-id="4d52c-218">如果資料項目的主要文字是可編輯的，則必須支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="4d52c-219">在大型清單中使用 Dataitem</span><span class="sxs-lookup"><span data-stu-id="4d52c-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="4d52c-220">由於大型清單通常會在 UI 架構內虛擬化以協助效能，因此消費者介面自動化用戶端無法使用消費者介面自動化查詢功能來搜尋完整樹狀結構的內容，其方式與其他專案容器中的相同。</span><span class="sxs-lookup"><span data-stu-id="4d52c-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="4d52c-221">用戶端應該將專案滾動至 view (或展開控制項，以顯示所有可用的選項) ，然後再從資料項目存取完整的資訊集。</span><span class="sxs-lookup"><span data-stu-id="4d52c-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="4d52c-222">在資料項目的消費者介面自動化專案上呼叫 [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) 時，Microsoft Windows 檔案總管會成功傳回，而且會將焦點設為數據項子樹中的編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="4d52c-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="4d52c-223">必要的事件</span><span class="sxs-lookup"><span data-stu-id="4d52c-223">Required Events</span></span>

<span data-ttu-id="4d52c-224">下表列出資料項目目控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="4d52c-225">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="4d52c-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4d52c-226">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="4d52c-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="4d52c-227">備註</span><span class="sxs-lookup"><span data-stu-id="4d52c-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d52c-228">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="4d52c-229">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="4d52c-230">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="4d52c-231">如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="4d52c-232">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="4d52c-233">如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="4d52c-234">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="4d52c-235">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="4d52c-236">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="4d52c-237">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="4d52c-238">[**UIA \_ItemStatusPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="4d52c-239">如果控制項支援 [**ItemStatus**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="4d52c-240">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="4d52c-241">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="4d52c-242">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="4d52c-243">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="4d52c-244">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="4d52c-245">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="4d52c-246">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="4d52c-247">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d52c-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="4d52c-248">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="4d52c-249">如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="4d52c-250">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="4d52c-251">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="4d52c-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="4d52c-252">DataItem 控制項類型範例</span><span class="sxs-lookup"><span data-stu-id="4d52c-252">DataItem Control Type Example</span></span>

<span data-ttu-id="4d52c-253">下圖說明清單視圖控制項中的 DataItem 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="4d52c-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![具有 dataitem 控制項類型之清單視圖控制項的螢幕擷取畫面](images/dataitemxmpl.jpg)

<span data-ttu-id="4d52c-255">與資料項目控制項相關之消費者介面自動化樹狀結構的控制項視圖和內容視圖如下所示。</span><span class="sxs-lookup"><span data-stu-id="4d52c-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="4d52c-256">每個自動化項目的控制項模式顯示在括號中。</span><span class="sxs-lookup"><span data-stu-id="4d52c-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="4d52c-257">**群組**"Contoso" 也是資料格主控制項方格的一部分。</span><span class="sxs-lookup"><span data-stu-id="4d52c-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="4d52c-258">如需更高層級方格結構的範例，請參閱 [DataGrid 控制項類型](uiauto-supportdatagridcontroltype.md)。</span><span class="sxs-lookup"><span data-stu-id="4d52c-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d52c-259">消費者介面自動化樹狀結構控制項視圖</span><span class="sxs-lookup"><span data-stu-id="4d52c-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="4d52c-260">消費者介面自動化樹狀結構-內容視圖</span><span class="sxs-lookup"><span data-stu-id="4d52c-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4d52c-261">群組 &quot; Contoso &quot; (資料表、方格) </span><span class="sxs-lookup"><span data-stu-id="4d52c-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="4d52c-262">DataItem &quot; 帳戶 Receivable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) </span><span class="sxs-lookup"><span data-stu-id="4d52c-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="4d52c-263">映射 &quot; 帳戶 Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="4d52c-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="4d52c-264">編輯 &quot; 名稱 &quot; (TableItem、GridItem、值 &quot; 帳戶 Receivable.doc&quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="4d52c-265">修改的編輯 &quot; 日期 &quot; (TableItem、GridItem、VALUE &quot; 8/25/2006 3:29 PM &quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="4d52c-266">編輯 &quot; 大小 &quot; (GridItem、TableItem、VALUE &quot; 11.0 KB &quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="4d52c-267">DataItem &quot; 帳戶 Payable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) </span><span class="sxs-lookup"><span data-stu-id="4d52c-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="4d52c-268">...</span><span class="sxs-lookup"><span data-stu-id="4d52c-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d52c-269">群組 &quot; Contoso &quot; (資料表、方格) </span><span class="sxs-lookup"><span data-stu-id="4d52c-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="4d52c-270">DataItem &quot; 帳戶 Receivable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) </span><span class="sxs-lookup"><span data-stu-id="4d52c-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="4d52c-271">映射 &quot; 帳戶 Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="4d52c-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="4d52c-272">編輯 &quot; 名稱 &quot; (TableItem、GridItem、值 &quot; 帳戶 Receivable.doc&quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="4d52c-273">修改的編輯 &quot; 日期 &quot; (TableItem、GridItem、VALUE &quot; 8/25/2006 3:29 PM &quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="4d52c-274">編輯 &quot; 大小 &quot; (GridItem、TableItem、VALUE &quot; 11.0 KB &quot;) </span><span class="sxs-lookup"><span data-stu-id="4d52c-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="4d52c-275">DataItem &quot; 帳戶 Payable.doc&quot; (TableItem、GridItem、SelectionItem、Invoke) </span><span class="sxs-lookup"><span data-stu-id="4d52c-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="4d52c-276">...</span><span class="sxs-lookup"><span data-stu-id="4d52c-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d52c-277">如果方格代表可選取專案的清單，則可以使用 [專案類型 [] 控制項類型](uiauto-supportlistitemcontroltype.md) 來公開對應的可選取 UI 元素，而不是 DataItem 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="4d52c-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="4d52c-278">在上述範例中， **DataItem** 元素 ( 群組 ( "Contoso" ) 下的「帳戶 Receivable.doc」和「帳戶 ) Payable.doc」，可以藉由將它們公開為專案 **組合** 控制項類型來獲得改善，因為該類型已支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="4d52c-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d52c-279">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d52c-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4d52c-280">**概念**</span><span class="sxs-lookup"><span data-stu-id="4d52c-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d52c-281">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="4d52c-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4d52c-282">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="4d52c-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




