---
title: 微調控制項類型
description: 本主題提供微調控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- 消費者介面自動化，微調控制項類型的支援
- 消費者介面自動化，微調控制項類型
- 微調控制項類型的樹狀結構消費者介面自動化
- 消費者介面自動化，微調控制項類型的屬性
- 消費者介面自動化，微調控制項類型的控制項模式
- 消費者介面自動化，微調控制項類型的事件
- 樹狀結構，微調控制項類型
- 屬性、微調控制項類型
- 控制項模式，微調控制項類型
- 事件、微調控制項類型
- 微調控制項類型的支援
- Spinner 控制項類型
- 微調控制項類型的控制項類型、樹狀結構
- 控制項類型，微調控制項類型的控制項模式
- 控制項類型，支援微調
- 控制項類型，微調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674667"
---
# <a name="spinner-control-type"></a><span data-ttu-id="2869f-119">微調控制項類型</span><span class="sxs-lookup"><span data-stu-id="2869f-119">Spinner Control Type</span></span>

<span data-ttu-id="2869f-120">本主題提供 **微調** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2869f-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="2869f-121">微調控制項可用來選取某個範圍的項目或數字。</span><span class="sxs-lookup"><span data-stu-id="2869f-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="2869f-122">下列章節會定義 **微調** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="2869f-123">消費者介面自動化需求適用于所有 UI 架構/平臺整合控制項類型和控制項模式消費者介面自動化支援的微調控制項。</span><span class="sxs-lookup"><span data-stu-id="2869f-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2869f-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="2869f-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2869f-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="2869f-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2869f-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="2869f-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2869f-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="2869f-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2869f-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="2869f-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2869f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="2869f-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2869f-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="2869f-130">Typical Tree Structure</span></span>

<span data-ttu-id="2869f-131">下表描述在支援 **RangeValue** 和 **選取** 控制項模式時，與微調控制項相關的消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="2869f-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="2869f-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="2869f-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="2869f-133">**RangeValue 控制項模式**</span><span class="sxs-lookup"><span data-stu-id="2869f-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2869f-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="2869f-134">Control View</span></span></th>
<th><span data-ttu-id="2869f-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="2869f-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2869f-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="2869f-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="2869f-137">編輯 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="2869f-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="2869f-138">按鈕 (2 個)</span><span class="sxs-lookup"><span data-stu-id="2869f-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2869f-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="2869f-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2869f-140">**Selection 控制項模式**</span><span class="sxs-lookup"><span data-stu-id="2869f-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2869f-141">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="2869f-141">Control View</span></span></th>
<th><span data-ttu-id="2869f-142">內容檢視</span><span class="sxs-lookup"><span data-stu-id="2869f-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2869f-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="2869f-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="2869f-144">編輯 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="2869f-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="2869f-145">按鈕 (2 個)</span><span class="sxs-lookup"><span data-stu-id="2869f-145">Button (2)</span></span></li>
<li><span data-ttu-id="2869f-146">清單專案 (0 或更多) </span><span class="sxs-lookup"><span data-stu-id="2869f-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2869f-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="2869f-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="2869f-148">ListItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="2869f-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2869f-149">若要確保「控制視圖」子樹中的兩個按鈕可以透過自動化測試控管來辨別，請適當地將 **ScrollAmount \_ SmallIncrement** 或 [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) 值指派給 **AutomationId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="2869f-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="2869f-150">針對某些執行，相關聯的編輯控制項可能是微調控制項的對等。</span><span class="sxs-lookup"><span data-stu-id="2869f-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="2869f-151">相關屬性</span><span class="sxs-lookup"><span data-stu-id="2869f-151">Relevant Properties</span></span>

<span data-ttu-id="2869f-152">下表列出消費者介面自動化屬性，其值或定義與微調控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="2869f-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="2869f-153">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="2869f-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2869f-154">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="2869f-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2869f-155">值</span><span class="sxs-lookup"><span data-stu-id="2869f-155">Value</span></span>       | <span data-ttu-id="2869f-156">注意</span><span class="sxs-lookup"><span data-stu-id="2869f-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2869f-157">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2869f-158">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-158">See notes.</span></span>  | <span data-ttu-id="2869f-159">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2869f-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="2869f-160">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2869f-161">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-161">See notes.</span></span>  | <span data-ttu-id="2869f-162">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="2869f-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="2869f-163">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2869f-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-164">See notes.</span></span>  | <span data-ttu-id="2869f-165">微調控制項可點選的點會將焦點置於控制項的編輯部分。</span><span class="sxs-lookup"><span data-stu-id="2869f-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2869f-166">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2869f-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="2869f-167">**Spinner**</span></span> | <span data-ttu-id="2869f-168">此值與所有架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="2869f-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2869f-169">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2869f-170">true</span><span class="sxs-lookup"><span data-stu-id="2869f-170">TRUE</span></span>        | <span data-ttu-id="2869f-171">微調控制項必須一律為內容。</span><span class="sxs-lookup"><span data-stu-id="2869f-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2869f-172">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2869f-173">true</span><span class="sxs-lookup"><span data-stu-id="2869f-173">TRUE</span></span>        | <span data-ttu-id="2869f-174">微調控制項必須一律為控制項。</span><span class="sxs-lookup"><span data-stu-id="2869f-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2869f-175">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2869f-176">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-176">See notes.</span></span>  | <span data-ttu-id="2869f-177">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2869f-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="2869f-178">微調控制項很少會取得焦點，但在這種情況下，焦點應該留在微調控制項本身，而不是子按鈕。</span><span class="sxs-lookup"><span data-stu-id="2869f-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="2869f-179">使用者應該可以使用向上鍵和向下鍵來執行所有滾動動作。</span><span class="sxs-lookup"><span data-stu-id="2869f-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="2869f-180">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2869f-181">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-181">See notes.</span></span>  | <span data-ttu-id="2869f-182">微調控制項有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="2869f-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2869f-183">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2869f-184">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-184">See notes.</span></span>  | <span data-ttu-id="2869f-185">對應至 **微調** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="2869f-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="2869f-186">針對 en-us 或英文 (美國) ，預設值為 "微調"。</span><span class="sxs-lookup"><span data-stu-id="2869f-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="2869f-187">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2869f-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2869f-188">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2869f-188">See notes.</span></span>  | <span data-ttu-id="2869f-189">微調控制項的名稱通常來自靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="2869f-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2869f-190">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="2869f-190">Required Control Patterns</span></span>

<span data-ttu-id="2869f-191">下表列出所有微調控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2869f-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="2869f-192">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="2869f-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2869f-193">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="2869f-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="2869f-194">支援/值</span><span class="sxs-lookup"><span data-stu-id="2869f-194">Support/Value</span></span> | <span data-ttu-id="2869f-195">備註</span><span class="sxs-lookup"><span data-stu-id="2869f-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2869f-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="2869f-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="2869f-197">相依</span><span class="sxs-lookup"><span data-stu-id="2869f-197">Depends</span></span>       | <span data-ttu-id="2869f-198">橫跨數值範圍的微調控制項可以支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2869f-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="2869f-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="2869f-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="2869f-200">相依</span><span class="sxs-lookup"><span data-stu-id="2869f-200">Depends</span></span>       | <span data-ttu-id="2869f-201">具有要選取之專案清單的微調控制項，必須支援 [選取](uiauto-implementingselection.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2869f-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="2869f-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="2869f-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="2869f-203">FALSE</span><span class="sxs-lookup"><span data-stu-id="2869f-203">FALSE</span></span>         | <span data-ttu-id="2869f-204">微調控制項一律是單一選擇容器。</span><span class="sxs-lookup"><span data-stu-id="2869f-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="2869f-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="2869f-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="2869f-206">相依</span><span class="sxs-lookup"><span data-stu-id="2869f-206">Depends</span></span>       | <span data-ttu-id="2869f-207">橫跨一組 descrete 選項或數位的微調控制項可以支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2869f-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="2869f-208">必要的事件</span><span class="sxs-lookup"><span data-stu-id="2869f-208">Required Events</span></span>

<span data-ttu-id="2869f-209">下表列出微調控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="2869f-210">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="2869f-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2869f-211">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="2869f-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="2869f-212">備註</span><span class="sxs-lookup"><span data-stu-id="2869f-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2869f-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2869f-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="2869f-214">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="2869f-215">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="2869f-216">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="2869f-217">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="2869f-218">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="2869f-219">[**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="2869f-220">如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="2869f-221">[**UIA \_Selection \_ InvalidatedEventId**](uiauto-event-ids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="2869f-222">如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="2869f-223">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2869f-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="2869f-224">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="2869f-225">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2869f-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="2869f-226">相關主題</span><span class="sxs-lookup"><span data-stu-id="2869f-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2869f-227">**概念**</span><span class="sxs-lookup"><span data-stu-id="2869f-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2869f-228">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="2869f-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2869f-229">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="2869f-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




