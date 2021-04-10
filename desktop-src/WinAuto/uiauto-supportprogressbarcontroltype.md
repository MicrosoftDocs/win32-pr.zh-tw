---
title: ProgressBar 控制項類型
description: 本主題提供 ProgressBar 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- 消費者介面自動化，ProgressBar 控制項類型的支援
- 消費者介面自動化，ProgressBar 控制項類型
- 消費者介面自動化，ProgressBar 控制項類型的樹狀結構
- 消費者介面自動化，ProgressBar 控制項類型的屬性
- 消費者介面自動化，ProgressBar 控制項類型的控制項模式
- 消費者介面自動化，ProgressBar 控制項類型的事件
- 樹狀結構，ProgressBar 控制項類型
- properties、ProgressBar 控制項類型
- 控制項模式，ProgressBar 控制項類型
- events、ProgressBar 控制項類型
- ProgressBar 控制項類型的支援
- ProgressBar 控制項類型
- 控制項類型，ProgressBar 控制項類型的樹狀結構
- 控制項類型，ProgressBar 控制項類型的控制項模式
- 控制項類型，支援 ProgressBar
- 控制項類型，ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/06/2019
ms.locfileid: "104092487"
---
# <a name="progressbar-control-type"></a><span data-ttu-id="c07ce-119">ProgressBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="c07ce-119">ProgressBar Control Type</span></span>

<span data-ttu-id="c07ce-120">本主題提供 **ProgressBar** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c07ce-120">This topic provides information about Microsoft UI Automation support for the **ProgressBar** control type.</span></span>

<span data-ttu-id="c07ce-121">進度列控制項指出冗長作業的進度。</span><span class="sxs-lookup"><span data-stu-id="c07ce-121">Progress bar controls indicate the progress of a lengthy operation.</span></span> <span data-ttu-id="c07ce-122">此控制項包含一個矩形，隨著作業的進度，會逐漸填滿系統的醒目提示色彩。</span><span class="sxs-lookup"><span data-stu-id="c07ce-122">The control consists of a rectangle that is gradually filled with the system highlight color as an operation progresses.</span></span>

<span data-ttu-id="c07ce-123">下列章節會定義 **ProgressBar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ProgressBar** control type.</span></span> <span data-ttu-id="c07ce-124">消費者介面自動化需求適用于所有進度列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="c07ce-124">The UI Automation requirements apply to all progress bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c07ce-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="c07ce-125">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c07ce-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="c07ce-126">Typical Tree Structure</span></span>](#typical-tree-structure)
- [<span data-ttu-id="c07ce-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="c07ce-127">Relevant Properties</span></span>](#relevant-properties)
- [<span data-ttu-id="c07ce-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="c07ce-128">Required Control Patterns</span></span>](#required-control-patterns)
- [<span data-ttu-id="c07ce-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="c07ce-129">Required Events</span></span>](#required-events)
- [<span data-ttu-id="c07ce-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="c07ce-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c07ce-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="c07ce-131">Typical Tree Structure</span></span>

<span data-ttu-id="c07ce-132">下表描述與進度列控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="c07ce-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to progress bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c07ce-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="c07ce-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c07ce-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="c07ce-134">Control View</span></span></th>
<th><span data-ttu-id="c07ce-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="c07ce-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c07ce-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="c07ce-136">ProgressBar</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c07ce-137">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="c07ce-137">ProgressBar</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c07ce-138">進度列控制項在消費者介面自動化樹狀結構的控制項或內容視圖中沒有任何子系。</span><span class="sxs-lookup"><span data-stu-id="c07ce-138">The progress bar controls do not have any children in the control or content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="c07ce-139">相關屬性</span><span class="sxs-lookup"><span data-stu-id="c07ce-139">Relevant Properties</span></span>

<span data-ttu-id="c07ce-140">下表列出消費者介面自動化屬性，其值或定義與進度列特別相關。</span><span class="sxs-lookup"><span data-stu-id="c07ce-140">The following table lists the UI Automation properties whose value or definition is especially relevant to progress bars.</span></span> <span data-ttu-id="c07ce-141">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="c07ce-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

| <span data-ttu-id="c07ce-142">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="c07ce-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c07ce-143">值</span><span class="sxs-lookup"><span data-stu-id="c07ce-143">Value</span></span>           | <span data-ttu-id="c07ce-144">注意</span><span class="sxs-lookup"><span data-stu-id="c07ce-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c07ce-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c07ce-146">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-146">See notes.</span></span>      | <span data-ttu-id="c07ce-147">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c07ce-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="c07ce-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c07ce-149">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-149">See notes.</span></span>      | <span data-ttu-id="c07ce-150">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="c07ce-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="c07ce-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c07ce-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-152">See notes.</span></span>      | <span data-ttu-id="c07ce-153">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="c07ce-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="c07ce-154">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="c07ce-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="c07ce-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c07ce-156">**進度列**</span><span class="sxs-lookup"><span data-stu-id="c07ce-156">**ProgressBar**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="c07ce-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c07ce-158">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c07ce-158">**TRUE**</span></span>        | <span data-ttu-id="c07ce-159">進度列控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="c07ce-159">The progress bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                           |
| [<span data-ttu-id="c07ce-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c07ce-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c07ce-161">**TRUE**</span></span>        | <span data-ttu-id="c07ce-162">進度列控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="c07ce-162">The progress bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                           |
| [<span data-ttu-id="c07ce-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c07ce-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-164">See notes.</span></span>      | <span data-ttu-id="c07ce-165">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="c07ce-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="c07ce-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c07ce-167">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-167">See notes.</span></span>      | <span data-ttu-id="c07ce-168">如果有靜態文字標籤，這個屬性必須公開該控制項的參考。</span><span class="sxs-lookup"><span data-stu-id="c07ce-168">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                              |
| [<span data-ttu-id="c07ce-169">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c07ce-170">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-170">See notes.</span></span>      | <span data-ttu-id="c07ce-171">對應到 **ProgressBar** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="c07ce-171">Localized string corresponding to the **ProgressBar** control type.</span></span> <span data-ttu-id="c07ce-172">預設值為 en-us 或英文 (美國) 的「進度列」。</span><span class="sxs-lookup"><span data-stu-id="c07ce-172">The default value is "progress bar" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="c07ce-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c07ce-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-174">See notes.</span></span>      | <span data-ttu-id="c07ce-175">進度列控制項的名稱通常來自靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="c07ce-175">The progress bar control typically gets its name from a static text label.</span></span> <span data-ttu-id="c07ce-176">如果沒有靜態文字標籤，應用程式開發人員就必須公開 Name 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="c07ce-176">If there is not a static text label the application developer must expose a value for the Name property.</span></span>                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c07ce-177">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="c07ce-177">Required Control Patterns</span></span>

<span data-ttu-id="c07ce-178">下表列出進度列控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c07ce-178">The following table lists the UI Automation control patterns required to be supported by progress bar controls.</span></span> <span data-ttu-id="c07ce-179">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="c07ce-179">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c07ce-180">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="c07ce-180">Control Pattern/Pattern Property</span></span>                              | <span data-ttu-id="c07ce-181">支援/值</span><span class="sxs-lookup"><span data-stu-id="c07ce-181">Support/Value</span></span> | <span data-ttu-id="c07ce-182">備註</span><span class="sxs-lookup"><span data-stu-id="c07ce-182">Notes</span></span>                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c07ce-183">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="c07ce-183">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | <span data-ttu-id="c07ce-184">相依</span><span class="sxs-lookup"><span data-stu-id="c07ce-184">Depends</span></span>       | <span data-ttu-id="c07ce-185">使用數值範圍的進度列控制項必須執行 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c07ce-185">Progress bar controls that take a numeric range must implement the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>        |
| [<span data-ttu-id="c07ce-186">**最小值**</span><span class="sxs-lookup"><span data-stu-id="c07ce-186">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="c07ce-187">相依</span><span class="sxs-lookup"><span data-stu-id="c07ce-187">Depends</span></span>           | <span data-ttu-id="c07ce-188">這個屬性的值是控制項可以設定的最小值。</span><span class="sxs-lookup"><span data-stu-id="c07ce-188">The value of this property is the minimum value that the control can be set to.</span></span> <span data-ttu-id="c07ce-189">此值應小於 [**最大**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)值。</span><span class="sxs-lookup"><span data-stu-id="c07ce-189">This value should be less than [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).</span></span>                                                      |
| [<span data-ttu-id="c07ce-190">**最大**</span><span class="sxs-lookup"><span data-stu-id="c07ce-190">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="c07ce-191">相依</span><span class="sxs-lookup"><span data-stu-id="c07ce-191">Depends</span></span>         | <span data-ttu-id="c07ce-192">這個屬性的值是控制項可以設定的最大值。</span><span class="sxs-lookup"><span data-stu-id="c07ce-192">The value of this property is the maximum value that the control can be set to.</span></span> <span data-ttu-id="c07ce-193">此值應大於 [**最小**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)值。</span><span class="sxs-lookup"><span data-stu-id="c07ce-193">This value should be greater than [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum).</span></span>                                                        |
| [<span data-ttu-id="c07ce-194">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="c07ce-194">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="c07ce-195">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c07ce-195">**NaN**</span></span>       | <span data-ttu-id="c07ce-196">這個屬性不是必要項，因為進度列控制項是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c07ce-196">This property is not required because progress bar controls are read-only.</span></span>                                                                 |
| [<span data-ttu-id="c07ce-197">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="c07ce-197">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="c07ce-198">**NaN**</span><span class="sxs-lookup"><span data-stu-id="c07ce-198">**NaN**</span></span>       | <span data-ttu-id="c07ce-199">這個屬性不是必要項，因為進度列控制項是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c07ce-199">This property is not required because progress bar controls are read-only.</span></span>                                                                 |
| [<span data-ttu-id="c07ce-200">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="c07ce-200">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | <span data-ttu-id="c07ce-201">相依</span><span class="sxs-lookup"><span data-stu-id="c07ce-201">Depends</span></span>       | <span data-ttu-id="c07ce-202">提供進度文字指示的進度列控制項必須執行實 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="c07ce-202">Progress bar controls that give a textual indication of progress must implement the [Value](uiauto-implementingvalue.md) control pattern.</span></span> |
| [<span data-ttu-id="c07ce-203">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="c07ce-203">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | <span data-ttu-id="c07ce-204">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="c07ce-204">**TRUE**</span></span>      | <span data-ttu-id="c07ce-205">這個屬性的值一律為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c07ce-205">The value for this property is always **TRUE**.</span></span>                                                                                            |
| [<span data-ttu-id="c07ce-206">**值**</span><span class="sxs-lookup"><span data-stu-id="c07ce-206">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | <span data-ttu-id="c07ce-207">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="c07ce-207">See notes.</span></span>    | <span data-ttu-id="c07ce-208">此屬性會公開進度列控制項的文字進度。</span><span class="sxs-lookup"><span data-stu-id="c07ce-208">This property exposes textual progress of a progress bar control.</span></span>                                                                          |



 

## <a name="required-events"></a><span data-ttu-id="c07ce-209">必要的事件</span><span class="sxs-lookup"><span data-stu-id="c07ce-209">Required Events</span></span>

<span data-ttu-id="c07ce-210">下表列出支援進度列所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-210">The following table lists the UI Automation events that progress bars are required to support.</span></span> <span data-ttu-id="c07ce-211">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="c07ce-211">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c07ce-212">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="c07ce-212">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="c07ce-213">備註</span><span class="sxs-lookup"><span data-stu-id="c07ce-213">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c07ce-214">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-214">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="c07ce-215">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-215">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="c07ce-216">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-216">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="c07ce-217">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-217">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="c07ce-218">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-218">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="c07ce-219">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-219">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="c07ce-220">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-220">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="c07ce-221">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c07ce-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="c07ce-222">[**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-222">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="c07ce-223">如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-223">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="c07ce-224">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="c07ce-225">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="c07ce-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="c07ce-226">相關主題</span><span class="sxs-lookup"><span data-stu-id="c07ce-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c07ce-227">**概念**</span><span class="sxs-lookup"><span data-stu-id="c07ce-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c07ce-228">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="c07ce-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c07ce-229">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="c07ce-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




