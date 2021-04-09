---
title: 行事曆控制項類型
description: 本主題提供行事曆控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 行事曆控制項可讓使用者輕鬆地判斷日期並選取其他日期。
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- 消費者介面自動化，行事曆控制項類型的支援
- 消費者介面自動化，行事曆控制項類型
- 消費者介面自動化，行事曆控制項類型的樹狀結構
- 消費者介面自動化，行事曆控制項類型的屬性
- 消費者介面自動化，行事曆控制項類型的控制項模式
- 消費者介面自動化，行事曆控制項類型的事件
- 樹狀結構，行事曆控制項類型
- 屬性、行事曆控制項類型
- 控制項模式，行事曆控制項類型
- 事件、行事曆控制項類型
- 行事曆控制項類型的支援
- Calendar 控制項類型
- 月曆控制項類型的控制項類型、樹狀結構
- 控制項類型、行事曆控制項類型的控制項模式
- 控制項類型、行事曆支援
- 控制項類型，行事曆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef936848f764c6937bfe36e6ed919f0a88dac78c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022104"
---
# <a name="calendar-control-type"></a><span data-ttu-id="701ee-120">行事曆控制項類型</span><span class="sxs-lookup"><span data-stu-id="701ee-120">Calendar Control Type</span></span>

<span data-ttu-id="701ee-121">本主題提供行事 **曆** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="701ee-121">This topic provides information about Microsoft UI Automation support for the **Calendar** control type.</span></span> <span data-ttu-id="701ee-122">行事曆控制項可讓使用者輕鬆地判斷日期並選取其他日期。</span><span class="sxs-lookup"><span data-stu-id="701ee-122">A calendar control allows the user to easily determine the date and select other dates.</span></span>

<span data-ttu-id="701ee-123">下列章節會定義 **Calendar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Calendar** control type.</span></span> <span data-ttu-id="701ee-124">消費者介面自動化需求適用于所有行事曆控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="701ee-124">The UI Automation requirements apply to all calendar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="701ee-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="701ee-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="701ee-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="701ee-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="701ee-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="701ee-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="701ee-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="701ee-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="701ee-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="701ee-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="701ee-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="701ee-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="701ee-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="701ee-131">Typical Tree Structure</span></span>

<span data-ttu-id="701ee-132">下表描述與行事曆控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="701ee-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to calendar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="701ee-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="701ee-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="701ee-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="701ee-134">Control View</span></span></th>
<th><span data-ttu-id="701ee-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="701ee-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="701ee-136">Calendar</span><span class="sxs-lookup"><span data-stu-id="701ee-136">Calendar</span></span>
<ul>
<li><span data-ttu-id="701ee-137">DataGrid</span><span class="sxs-lookup"><span data-stu-id="701ee-137">DataGrid</span></span>
<ul>
<li><span data-ttu-id="701ee-138">標題 (0 或 1)</span><span class="sxs-lookup"><span data-stu-id="701ee-138">Header (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="701ee-139">HeaderItem (0 或7，數量取決於資料行中顯示多少天) </span><span class="sxs-lookup"><span data-stu-id="701ee-139">HeaderItem (0 or 7, quantity depends on how many days are displayed in columns)</span></span></li>
</ul></li>
<li><span data-ttu-id="701ee-140">ListItem (數量取決於要顯示多少天)</span><span class="sxs-lookup"><span data-stu-id="701ee-140">ListItem (quantity depends on how many days are displayed)</span></span></li>
<li><span data-ttu-id="701ee-141">按鈕 (0 或 2；用於分頁月曆檢視)</span><span class="sxs-lookup"><span data-stu-id="701ee-141">Button (0 or 2; for paging calendar view)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="701ee-142">Calendar</span><span class="sxs-lookup"><span data-stu-id="701ee-142">Calendar</span></span>
<ul>
<li><span data-ttu-id="701ee-143">ListItem (數量取決於要顯示多少天)</span><span class="sxs-lookup"><span data-stu-id="701ee-143">ListItem (quantity depends on how many days are displayed)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="701ee-144">月曆控制項可以在使用者介面中以許多不同的形式來表示。</span><span class="sxs-lookup"><span data-stu-id="701ee-144">Calendar controls can be represented in many different forms within the user interface.</span></span> <span data-ttu-id="701ee-145">唯一保證位於消費者介面自動化樹狀結構之控制項視圖中的控制項是資料格、標頭、標頭專案和清單專案控制項。</span><span class="sxs-lookup"><span data-stu-id="701ee-145">The only controls guaranteed to be in the control view of the UI Automation tree are the data grid, header, header item, and list item controls.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="701ee-146">相關屬性</span><span class="sxs-lookup"><span data-stu-id="701ee-146">Relevant Properties</span></span>

<span data-ttu-id="701ee-147">下表列出消費者介面自動化屬性，其值或定義與 **Calendar** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="701ee-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Calendar** control type.</span></span> <span data-ttu-id="701ee-148">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="701ee-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="701ee-149">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="701ee-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="701ee-150">值</span><span class="sxs-lookup"><span data-stu-id="701ee-150">Value</span></span>        | <span data-ttu-id="701ee-151">注意</span><span class="sxs-lookup"><span data-stu-id="701ee-151">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ee-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="701ee-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-153">See notes.</span></span>   | <span data-ttu-id="701ee-154">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="701ee-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="701ee-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="701ee-156">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-156">See notes.</span></span>   | <span data-ttu-id="701ee-157">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="701ee-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="701ee-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="701ee-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-159">See notes.</span></span>   | <span data-ttu-id="701ee-160">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="701ee-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="701ee-161">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="701ee-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="701ee-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="701ee-163">**Calendar**</span><span class="sxs-lookup"><span data-stu-id="701ee-163">**Calendar**</span></span> | <span data-ttu-id="701ee-164">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="701ee-164">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="701ee-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="701ee-166">true</span><span class="sxs-lookup"><span data-stu-id="701ee-166">TRUE</span></span>         | <span data-ttu-id="701ee-167">行事曆控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="701ee-167">The calendar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="701ee-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="701ee-169">true</span><span class="sxs-lookup"><span data-stu-id="701ee-169">TRUE</span></span>         | <span data-ttu-id="701ee-170">行事曆控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="701ee-170">The calendar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="701ee-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="701ee-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-172">See notes.</span></span>   | <span data-ttu-id="701ee-173">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="701ee-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="701ee-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="701ee-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-175">See notes.</span></span>   | <span data-ttu-id="701ee-176">這個屬性的值應該是文件控制項的標籤。</span><span class="sxs-lookup"><span data-stu-id="701ee-176">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="701ee-177">通常會使用文件的標題。</span><span class="sxs-lookup"><span data-stu-id="701ee-177">Typically, the title of the document is used.</span></span>                                                                                |
| [<span data-ttu-id="701ee-178">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-178">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="701ee-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-179">See notes.</span></span>   | <span data-ttu-id="701ee-180">對應至行事 **曆** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="701ee-180">Localized string corresponding to the **Calendar** control type.</span></span> <span data-ttu-id="701ee-181">預設值為「行事曆」，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="701ee-181">The default value is "calendar" for en-US or English (United States).</span></span>                                                               |
| [<span data-ttu-id="701ee-182">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="701ee-182">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="701ee-183">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="701ee-183">See notes.</span></span>   | <span data-ttu-id="701ee-184">行事曆控制項通常會從目前的日期取得其名稱。</span><span class="sxs-lookup"><span data-stu-id="701ee-184">The calendar control typically gets its name from the current date.</span></span>                                                                                                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="701ee-185">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="701ee-185">Required Control Patterns</span></span>

<span data-ttu-id="701ee-186">下表列出所有行事曆控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="701ee-186">The following table lists the UI Automation control patterns required to be supported by all calendar controls.</span></span> <span data-ttu-id="701ee-187">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="701ee-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="701ee-188">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="701ee-188">Control Pattern/Pattern Property</span></span>                        | <span data-ttu-id="701ee-189">支援/值</span><span class="sxs-lookup"><span data-stu-id="701ee-189">Support/Value</span></span> | <span data-ttu-id="701ee-190">備註</span><span class="sxs-lookup"><span data-stu-id="701ee-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ee-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="701ee-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="701ee-192">必要</span><span class="sxs-lookup"><span data-stu-id="701ee-192">Required</span></span>      | <span data-ttu-id="701ee-193">行事曆控制項一律支援 [方格](uiauto-implementinggrid.md) 控制項模式，因為一個月內的天數是可流覽空間的專案。</span><span class="sxs-lookup"><span data-stu-id="701ee-193">The calendar control always supports the [Grid](uiauto-implementinggrid.md) control pattern because the days within a month are items that can be navigated spatially.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="701ee-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="701ee-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="701ee-195">相依</span><span class="sxs-lookup"><span data-stu-id="701ee-195">Depends</span></span>       | <span data-ttu-id="701ee-196">大部分的月曆控制項都支援依頁面翻閱檢視。</span><span class="sxs-lookup"><span data-stu-id="701ee-196">Most calendar controls support flipping the view by page.</span></span> <span data-ttu-id="701ee-197">建議使用 [滾動](uiauto-implementingscroll.md) 條控制項模式，以便支援分頁導覽。</span><span class="sxs-lookup"><span data-stu-id="701ee-197">The [Scroll](uiauto-implementingscroll.md) control pattern is recommended in order to support paging navigation.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="701ee-198">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="701ee-198">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="701ee-199">相依</span><span class="sxs-lookup"><span data-stu-id="701ee-199">Depends</span></span>       | <span data-ttu-id="701ee-200">大部分的行事曆控制項都會保留特定的日、月或年做為子項目的選取專案。</span><span class="sxs-lookup"><span data-stu-id="701ee-200">Most of calendar controls retain a specific day, month, or year as a selection of the subelement.</span></span> <span data-ttu-id="701ee-201">某些行事曆可供多重選取，且僅限單一選取。</span><span class="sxs-lookup"><span data-stu-id="701ee-201">Some calendars are multi-selectable and other only single-selectable.</span></span> <span data-ttu-id="701ee-202">具有可選取子項目的行事曆控制項應支援 [選取](uiauto-implementingselection.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="701ee-202">Calendar control with selectable subelements should support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                         |
| [<span data-ttu-id="701ee-203">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="701ee-203">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="701ee-204">必要</span><span class="sxs-lookup"><span data-stu-id="701ee-204">Required</span></span>      | <span data-ttu-id="701ee-205">由於行事曆控制項的子樹中一律會有一個標頭，所以必須支援 [Table](uiauto-implementingtable.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="701ee-205">Because the calendar control always has a header within its subtree for the days of the week, the [Table](uiauto-implementingtable.md) control pattern must be supported.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="701ee-206">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="701ee-206">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="701ee-207">No</span><span class="sxs-lookup"><span data-stu-id="701ee-207">No</span></span>            | <span data-ttu-id="701ee-208">因為專案無法直接在控制項上設定值，所以不需要為行事曆控制項設定 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="701ee-208">The [Value](uiauto-implementingvalue.md) control pattern is not necessary for calendar controls because the element cannot set the value directly on the control.</span></span> <span data-ttu-id="701ee-209">如果特定日期與控制項相關聯，則應該透過 [選取](uiauto-implementingselection.md) 控制項模式來提供資訊。</span><span class="sxs-lookup"><span data-stu-id="701ee-209">If a specific date is associated with the control, the information should be provided by the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="701ee-210">必要的事件</span><span class="sxs-lookup"><span data-stu-id="701ee-210">Required Events</span></span>

<span data-ttu-id="701ee-211">下表列出行事曆控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-211">The following table lists the UI Automation events that calendar controls are required to support.</span></span> <span data-ttu-id="701ee-212">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="701ee-212">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="701ee-213">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="701ee-213">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="701ee-214">備註</span><span class="sxs-lookup"><span data-stu-id="701ee-214">Notes</span></span>                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701ee-215">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="701ee-215">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| <span data-ttu-id="701ee-216">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-216">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                                                                              |
| <span data-ttu-id="701ee-217">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="701ee-218">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                                                                     |
| <span data-ttu-id="701ee-219">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="701ee-220">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                                                                   |
| [<span data-ttu-id="701ee-221">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="701ee-221">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| <span data-ttu-id="701ee-222">[**UIA \_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-222">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="701ee-223">如果控制項支援 [MultipleView](uiauto-implementingmultipleview.md)控制項模式的 [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-223">If the control supports the [**CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="701ee-224">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="701ee-224">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| <span data-ttu-id="701ee-225">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-225">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="701ee-226">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| <span data-ttu-id="701ee-227">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-227">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="701ee-228">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| <span data-ttu-id="701ee-229">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-229">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="701ee-230">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| <span data-ttu-id="701ee-231">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-231">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="701ee-232">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| <span data-ttu-id="701ee-233">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-233">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="701ee-234">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| <span data-ttu-id="701ee-235">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-235">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="701ee-236">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="701ee-236">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                             |
| [<span data-ttu-id="701ee-237">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="701ee-237">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="701ee-238">相關主題</span><span class="sxs-lookup"><span data-stu-id="701ee-238">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="701ee-239">**概念**</span><span class="sxs-lookup"><span data-stu-id="701ee-239">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="701ee-240">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="701ee-240">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="701ee-241">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="701ee-241">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




