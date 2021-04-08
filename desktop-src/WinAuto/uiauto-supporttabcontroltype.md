---
title: 索引標籤控制項類型
description: 本主題提供索引標籤控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- 消費者介面自動化，支援索引標籤控制項類型
- 消費者介面自動化，索引標籤控制項類型
- 消費者介面自動化，索引標籤控制項類型的樹狀結構
- 消費者介面自動化，索引標籤控制項類型的屬性
- 消費者介面自動化、索引標籤控制項類型的控制項模式
- 消費者介面自動化，索引標籤控制項類型的事件
- 樹狀結構，索引標籤控制項類型
- 屬性，索引標籤控制項類型
- 控制項模式，索引標籤控制項類型
- 事件，索引標籤控制項類型
- 支援索引標籤控制項類型
- Tab 控制項類型
- 控制項類型，索引標籤控制項類型的樹狀結構
- 控制項類型，索引標籤控制項類型的控制項模式
- 控制項類型，支援 Tab
- 控制項類型，Tab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932342"
---
# <a name="tab-control-type"></a><span data-ttu-id="b8078-119">索引標籤控制項類型</span><span class="sxs-lookup"><span data-stu-id="b8078-119">Tab Control Type</span></span>

<span data-ttu-id="b8078-120">本主題提供 **選項卡** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b8078-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="b8078-121">「索引標籤控制項」類似於筆記本裡的分隔頁或檔案櫃中的標籤。</span><span class="sxs-lookup"><span data-stu-id="b8078-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="b8078-122">藉由使用索引標籤控制項，應用程式可以定義視窗或對話方塊中同一個區域的多個頁面。</span><span class="sxs-lookup"><span data-stu-id="b8078-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="b8078-123">下列章節會定義 **選項卡** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="b8078-124">消費者介面自動化需求適用于所有的索引標籤控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="b8078-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="b8078-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b8078-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b8078-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="b8078-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b8078-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="b8078-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b8078-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="b8078-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="b8078-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="b8078-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b8078-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8078-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b8078-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="b8078-131">Typical Tree Structure</span></span>

<span data-ttu-id="b8078-132">下表描述與索引標籤控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="b8078-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b8078-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="b8078-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8078-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="b8078-134">Control View</span></span></th>
<th><span data-ttu-id="b8078-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="b8078-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b8078-136">索引標籤</span><span class="sxs-lookup"><span data-stu-id="b8078-136">Tab</span></span>
<ul>
<li><span data-ttu-id="b8078-137">TabItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b8078-138">捲軸 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="b8078-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="b8078-139">按鈕 (0 或 2 個)</span><span class="sxs-lookup"><span data-stu-id="b8078-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b8078-140">索引標籤</span><span class="sxs-lookup"><span data-stu-id="b8078-140">Tab</span></span>
<ul>
<li><span data-ttu-id="b8078-141">TabItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b8078-142">索引標籤控制項根據 [TabItem](uiauto-supporttabitemcontroltype.md) 控制項類型，有子消費者介面自動化專案。</span><span class="sxs-lookup"><span data-stu-id="b8078-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="b8078-143">當索引標籤專案分組時 (例如 Microsoft Office 應用程式中) **選項卡** 控制項類型也可以裝載 **群組** 索引標籤專案的群組控制項類型，如下列樹狀結構所示。</span><span class="sxs-lookup"><span data-stu-id="b8078-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8078-144">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="b8078-144">Control View</span></span></th>
<th><span data-ttu-id="b8078-145">內容檢視</span><span class="sxs-lookup"><span data-stu-id="b8078-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b8078-146">索引標籤</span><span class="sxs-lookup"><span data-stu-id="b8078-146">Tab</span></span>
<ul>
<li><span data-ttu-id="b8078-147">TabItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b8078-148">Group (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="b8078-149">TabItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="b8078-150">捲軸 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="b8078-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="b8078-151">按鈕 (0 或 2 個)</span><span class="sxs-lookup"><span data-stu-id="b8078-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b8078-152">索引標籤</span><span class="sxs-lookup"><span data-stu-id="b8078-152">Tab</span></span>
<ul>
<li><span data-ttu-id="b8078-153">TabItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="b8078-154">Group (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="b8078-155">TabItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b8078-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="b8078-156">相關屬性</span><span class="sxs-lookup"><span data-stu-id="b8078-156">Relevant Properties</span></span>

<span data-ttu-id="b8078-157">下表列出消費者介面自動化屬性，其值或定義與索引標籤控制項特別有關。</span><span class="sxs-lookup"><span data-stu-id="b8078-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="b8078-158">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="b8078-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b8078-159">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="b8078-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b8078-160">值</span><span class="sxs-lookup"><span data-stu-id="b8078-160">Value</span></span>      | <span data-ttu-id="b8078-161">注意</span><span class="sxs-lookup"><span data-stu-id="b8078-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8078-162">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="b8078-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-163">See notes.</span></span> | <span data-ttu-id="b8078-164">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b8078-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b8078-165">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b8078-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-166">See notes.</span></span> | <span data-ttu-id="b8078-167">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="b8078-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="b8078-168">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="b8078-169">No</span><span class="sxs-lookup"><span data-stu-id="b8078-169">No</span></span>         | <span data-ttu-id="b8078-170">索引標籤控制項沒有可點按的點。</span><span class="sxs-lookup"><span data-stu-id="b8078-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b8078-171">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b8078-172">**Tab**</span><span class="sxs-lookup"><span data-stu-id="b8078-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b8078-173">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b8078-174">true</span><span class="sxs-lookup"><span data-stu-id="b8078-174">TRUE</span></span>       | <span data-ttu-id="b8078-175">索引標籤控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="b8078-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b8078-176">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b8078-177">true</span><span class="sxs-lookup"><span data-stu-id="b8078-177">TRUE</span></span>       | <span data-ttu-id="b8078-178">索引標籤控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="b8078-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b8078-179">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b8078-180">true</span><span class="sxs-lookup"><span data-stu-id="b8078-180">TRUE</span></span>       | <span data-ttu-id="b8078-181">索引標籤控制項類型必須能夠接收鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="b8078-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="b8078-182">一般而言，消費者介面自動化用戶端會在索引標籤控制項上呼叫 [**IUIAutomationElement：： SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) ，其中一個專案會將鍵盤焦點轉送至索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="b8078-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="b8078-183">部分索引標籤容器可以接收焦點，而無須將焦點設在容器的其中一個項目。</span><span class="sxs-lookup"><span data-stu-id="b8078-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="b8078-184">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b8078-185">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-185">See notes.</span></span> | <span data-ttu-id="b8078-186">索引標籤控制項通常會有透過此屬性公開的靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="b8078-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="b8078-187">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b8078-188">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-188">See notes.</span></span> | <span data-ttu-id="b8078-189">對應至 **選項卡** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="b8078-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="b8078-190">預設值為 "tab" 代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="b8078-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="b8078-191">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b8078-192">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-192">See notes.</span></span> | <span data-ttu-id="b8078-193">索引標籤控制項很少需要 **名稱** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b8078-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="b8078-194">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b8078-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b8078-195">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b8078-195">See notes.</span></span> | <span data-ttu-id="b8078-196">此索引標籤控制項必須一律指出是水平或垂直放置。</span><span class="sxs-lookup"><span data-stu-id="b8078-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="b8078-197">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="b8078-197">Required Control Patterns</span></span>

<span data-ttu-id="b8078-198">下表列出所有索引標籤控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="b8078-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="b8078-199">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="b8078-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="b8078-200">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="b8078-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="b8078-201">支援/值</span><span class="sxs-lookup"><span data-stu-id="b8078-201">Support/Value</span></span> | <span data-ttu-id="b8078-202">備註</span><span class="sxs-lookup"><span data-stu-id="b8078-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8078-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="b8078-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="b8078-204">必要</span><span class="sxs-lookup"><span data-stu-id="b8078-204">Required</span></span>      | <span data-ttu-id="b8078-205">所有的索引標籤控制項都必須支援 [選取](uiauto-implementingselection.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="b8078-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="b8078-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="b8078-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="b8078-207">true</span><span class="sxs-lookup"><span data-stu-id="b8078-207">TRUE</span></span>          | <span data-ttu-id="b8078-208">索引標籤控制項一律需要選取某個項目。</span><span class="sxs-lookup"><span data-stu-id="b8078-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="b8078-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="b8078-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="b8078-210">FALSE</span><span class="sxs-lookup"><span data-stu-id="b8078-210">FALSE</span></span>         | <span data-ttu-id="b8078-211">索引標籤控制項一律是單一選取容器。</span><span class="sxs-lookup"><span data-stu-id="b8078-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="b8078-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="b8078-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="b8078-213">相依</span><span class="sxs-lookup"><span data-stu-id="b8078-213">Depends</span></span>       | <span data-ttu-id="b8078-214">如果索引標籤控制項具有可讓一組索引標籤專案通過滾動的 widget，則必須支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="b8078-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="b8078-215">必要的事件</span><span class="sxs-lookup"><span data-stu-id="b8078-215">Required Events</span></span>

<span data-ttu-id="b8078-216">下表列出支援的索引標籤控制項消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="b8078-217">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="b8078-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b8078-218">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="b8078-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="b8078-219">備註</span><span class="sxs-lookup"><span data-stu-id="b8078-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b8078-220">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b8078-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="b8078-221">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="b8078-222">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="b8078-223">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="b8078-224">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="b8078-225">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="b8078-226">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="b8078-227">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b8078-228">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="b8078-229">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b8078-230">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="b8078-231">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b8078-232">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="b8078-233">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b8078-234">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="b8078-235">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b8078-236">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="b8078-237">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b8078-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="b8078-238">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b8078-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="b8078-239">相關主題</span><span class="sxs-lookup"><span data-stu-id="b8078-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b8078-240">**概念**</span><span class="sxs-lookup"><span data-stu-id="b8078-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b8078-241">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="b8078-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b8078-242">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="b8078-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




