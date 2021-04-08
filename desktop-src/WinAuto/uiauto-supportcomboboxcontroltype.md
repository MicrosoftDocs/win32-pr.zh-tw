---
title: ComboBox 控制項類型
description: 本主題提供 ComboBox 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- 消費者介面自動化，ComboBox 控制項類型的支援
- 消費者介面自動化，ComboBox 控制項類型
- 消費者介面自動化，ComboBox 控制項類型的樹狀結構
- 消費者介面自動化，ComboBox 控制項類型的屬性
- 消費者介面自動化，ComboBox 控制項類型的控制項模式
- 消費者介面自動化，ComboBox 控制項類型的事件
- 樹狀結構，ComboBox 控制項類型
- 屬性、ComboBox 控制項類型
- 控制項模式，ComboBox 控制項類型
- 事件、ComboBox 控制項類型
- ComboBox 控制項類型的支援
- ComboBox 控制項類型
- ComboBox 控制項類型的控制項類型、樹狀結構
- 控制項類型，ComboBox 控制項類型的控制項模式
- 控制項類型，支援 ComboBox
- 控制項類型，ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410cca4887c04a00d6da53feb9fcf1242476a979
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673079"
---
# <a name="combobox-control-type"></a><span data-ttu-id="9eeb1-119">ComboBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="9eeb1-119">ComboBox Control Type</span></span>

<span data-ttu-id="9eeb1-120">本主題提供 **ComboBox** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-120">This topic provides information about Microsoft UI Automation support for the **ComboBox** control type.</span></span>

<span data-ttu-id="9eeb1-121">下拉式方塊是與靜態控制項結合的清單方塊，或是在下拉式方塊的清單方塊部分中顯示目前選取項目的編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-121">A combo box is a list box combined with a static control or an edit control that displays the currently selected item in the list box portion of the combo box.</span></span> <span data-ttu-id="9eeb1-122">控制項的清單方塊部分會隨時顯示，或是只在使用者選取下拉式箭號 (這是按鈕) 時出現在控制項旁邊。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-122">The list box portion of the control is displayed at all times or only appears when the user selects the drop-down arrow (which is a push button) next to the control.</span></span> <span data-ttu-id="9eeb1-123">如果選取項目欄位是編輯控制項，使用者可以輸入不在清單中的資訊，否則使用者只能選取清單中的項目。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-123">If the selection field is an edit control, the user can enter information that is not in the list; otherwise, the user can only select items in the list.</span></span>

<span data-ttu-id="9eeb1-124">下列章節會定義 **ComboBox** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ComboBox** control type.</span></span> <span data-ttu-id="9eeb1-125">消費者介面自動化需求適用于所有的下拉式方塊控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-125">The UI Automation requirements apply to all combo box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9eeb1-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9eeb1-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="9eeb1-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9eeb1-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="9eeb1-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9eeb1-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="9eeb1-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9eeb1-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="9eeb1-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9eeb1-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eeb1-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9eeb1-132">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="9eeb1-132">Typical Tree Structure</span></span>

<span data-ttu-id="9eeb1-133">下表描述的是與下拉式方塊控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to combo box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9eeb1-134">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9eeb1-135">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="9eeb1-135">Control View</span></span></th>
<th><span data-ttu-id="9eeb1-136">內容檢視</span><span class="sxs-lookup"><span data-stu-id="9eeb1-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9eeb1-137">ComboBox</span><span class="sxs-lookup"><span data-stu-id="9eeb1-137">ComboBox</span></span>
<ul>
<li><span data-ttu-id="9eeb1-138">編輯 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="9eeb1-138">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="9eeb1-139">列出 (0 或 1) </span><span class="sxs-lookup"><span data-stu-id="9eeb1-139">List (0 or 1)</span></span></li>
<li><span data-ttu-id="9eeb1-140">清單項目 (子系清單；0 到多個)</span><span class="sxs-lookup"><span data-stu-id="9eeb1-140">List Item (child of List; 0 to many)</span></span></li>
<li><span data-ttu-id="9eeb1-141">按鈕 (1)</span><span class="sxs-lookup"><span data-stu-id="9eeb1-141">Button (1)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9eeb1-142">ComboBox</span><span class="sxs-lookup"><span data-stu-id="9eeb1-142">ComboBox</span></span>
<ul>
<li><span data-ttu-id="9eeb1-143">清單項目 (0 到多個)</span><span class="sxs-lookup"><span data-stu-id="9eeb1-143">List Item (0 to many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9eeb1-144">只有當下拉式方塊可以編輯為採用任何輸入（如同在 [ **執行** ] 對話方塊中的下拉式方塊的情況下）時，才需要在下拉式方塊的控制項視圖中編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-144">The edit control in the control view of the combo box is necessary only if the combo box can be edited to take any input, as is the case of the combo box in the **Run** dialog box.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9eeb1-145">相關屬性</span><span class="sxs-lookup"><span data-stu-id="9eeb1-145">Relevant Properties</span></span>

<span data-ttu-id="9eeb1-146">下表列出消費者介面自動化屬性，其值或定義與 **ComboBox** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ComboBox** control type.</span></span> <span data-ttu-id="9eeb1-147">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9eeb1-148">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="9eeb1-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9eeb1-149">值</span><span class="sxs-lookup"><span data-stu-id="9eeb1-149">Value</span></span>      | <span data-ttu-id="9eeb1-150">注意</span><span class="sxs-lookup"><span data-stu-id="9eeb1-150">Notes</span></span>                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eeb1-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9eeb1-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-152">See notes.</span></span> | <span data-ttu-id="9eeb1-153">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="9eeb1-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9eeb1-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-155">See notes.</span></span> | <span data-ttu-id="9eeb1-156">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9eeb1-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9eeb1-158">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-158">See notes.</span></span> | <span data-ttu-id="9eeb1-159">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9eeb1-160">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                             |
| [<span data-ttu-id="9eeb1-161">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9eeb1-162">ComboBox</span><span class="sxs-lookup"><span data-stu-id="9eeb1-162">ComboBox</span></span>   |                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="9eeb1-163">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-163">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="9eeb1-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-164">See notes.</span></span> | <span data-ttu-id="9eeb1-165">下拉式方塊控制項的解說文字應解釋為何系統會詢問使用者如何從下拉式方塊中選擇一個選項。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-165">The help text for combo box controls should explain why the user is being asked choose an option from the combo box.</span></span> <span data-ttu-id="9eeb1-166">文字類似於透過工具提示呈現的資訊。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-166">The text is similar to information presented through a tooltip.</span></span> <span data-ttu-id="9eeb1-167">例如，「選取項目以設定顯示器的解析度。」</span><span class="sxs-lookup"><span data-stu-id="9eeb1-167">For example, "Select an item to set the display resolution of your monitor."</span></span>                                                |
| [<span data-ttu-id="9eeb1-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9eeb1-169">true</span><span class="sxs-lookup"><span data-stu-id="9eeb1-169">TRUE</span></span>       | <span data-ttu-id="9eeb1-170">下拉式方塊控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-170">Combo box controls are always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="9eeb1-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9eeb1-172">true</span><span class="sxs-lookup"><span data-stu-id="9eeb1-172">TRUE</span></span>       | <span data-ttu-id="9eeb1-173">下拉式方塊控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-173">Combo box controls are always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="9eeb1-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9eeb1-175">true</span><span class="sxs-lookup"><span data-stu-id="9eeb1-175">TRUE</span></span>       | <span data-ttu-id="9eeb1-176">下拉式方塊控制項可以接收鍵盤焦點;不過，當消費者介面自動化用戶端將焦點設為下拉式方塊時，下拉式方塊子樹中的任何專案都可以接收焦點。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-176">Combo box controls can receive keyboard focus; however, when a UI Automation client sets focus to a combo box, any item in the combo box subtree can receive the focus.</span></span>                                                                                                                                          |
| [<span data-ttu-id="9eeb1-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9eeb1-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-178">See notes.</span></span> | <span data-ttu-id="9eeb1-179">下拉式方塊控制項通常會有此屬性參考的靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-179">Combo box controls typically have a static text label that this property references.</span></span>                                                                                                                                                                                                                             |
| [<span data-ttu-id="9eeb1-180">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9eeb1-181">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-181">See notes.</span></span> | <span data-ttu-id="9eeb1-182">對應至 **ComboBox** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-182">Localized string corresponding to the **ComboBox** control type.</span></span> <span data-ttu-id="9eeb1-183">預設值為「下拉式方塊」，適用于 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-183">The default value is "combo box" for en-US or English (United States).</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="9eeb1-184">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9eeb1-185">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-185">See notes.</span></span> | <span data-ttu-id="9eeb1-186">下拉式方塊控制項的名稱通常會從靜態文字標籤產生。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-186">The name of the combo box control is typically generated from a static text label.</span></span> <span data-ttu-id="9eeb1-187">如果沒有靜態文字標籤，您必須為 [ **名稱** ] 屬性指派值。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-187">If there is not a static text label, you must assign a value for the **Name** property.</span></span> <span data-ttu-id="9eeb1-188">當下拉式方塊的內容變更時，[ **名稱** ] 屬性不應包含下拉式方塊的目前內容或變更。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-188">The **Name** property should never contain the current contents of the combo box or change when the contents of the combo box change.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9eeb1-189">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="9eeb1-189">Required Control Patterns</span></span>

<span data-ttu-id="9eeb1-190">下表列出所有下拉式方塊控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-190">The following table lists the UI Automation control patterns required to be supported by all combo box controls.</span></span> <span data-ttu-id="9eeb1-191">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-191">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9eeb1-192">控制項模式</span><span class="sxs-lookup"><span data-stu-id="9eeb1-192">Control Pattern</span></span>                                                   | <span data-ttu-id="9eeb1-193">支援</span><span class="sxs-lookup"><span data-stu-id="9eeb1-193">Support</span></span>  | <span data-ttu-id="9eeb1-194">注意</span><span class="sxs-lookup"><span data-stu-id="9eeb1-194">Notes</span></span>                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eeb1-195">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-195">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9eeb1-196">必要</span><span class="sxs-lookup"><span data-stu-id="9eeb1-196">Required</span></span> | <span data-ttu-id="9eeb1-197">必須支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，因為下拉式方塊控制項一定要包含下拉式按鈕。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-197">The [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported because a combo box control must always contain a drop-down button.</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="9eeb1-198">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-198">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | <span data-ttu-id="9eeb1-199">相依</span><span class="sxs-lookup"><span data-stu-id="9eeb1-199">Depends</span></span>  | <span data-ttu-id="9eeb1-200">在下拉式方塊中顯示目前選取範圍。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-200">Displays the current selection in the combo box.</span></span> <span data-ttu-id="9eeb1-201">[選取](uiauto-implementingselection.md)控制項模式的支援會委派給下拉式方塊下方的清單方塊，但不一定都可行。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-201">Support for the [Selection](uiauto-implementingselection.md) control pattern is delegated to the list box beneath the combo box, but may not always be feasible.</span></span>                                                                                                                               |
| [<span data-ttu-id="9eeb1-202">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-202">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="9eeb1-203">相依</span><span class="sxs-lookup"><span data-stu-id="9eeb1-203">Depends</span></span>  | <span data-ttu-id="9eeb1-204">如果下拉式方塊可以採用任意文字值，則必須支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-204">If the combo box can take arbitrary text values, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span> <span data-ttu-id="9eeb1-205">此模式可讓您以程式設計方式設定下拉式方塊的字串內容。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-205">This pattern enables the string contents of the combo box to be set programmatically.</span></span> <span data-ttu-id="9eeb1-206">如果不支援值控制項模式，使用者必須從下拉式方塊的子樹中的清單專案中選取。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-206">If the Value control pattern is not supported, the user must select from the list items within the subtree of the combo box.</span></span> |
| [<span data-ttu-id="9eeb1-207">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-207">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | <span data-ttu-id="9eeb1-208">永不</span><span class="sxs-lookup"><span data-stu-id="9eeb1-208">Never</span></span>    | <span data-ttu-id="9eeb1-209">下拉式方塊中不會直接支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-209">The [Scroll](uiauto-implementingscroll.md) control pattern is never supported directly on a combo box.</span></span> <span data-ttu-id="9eeb1-210">如果下拉式方塊中包含的清單方塊可以滾動，而且只有在畫面上看不到清單方塊時，才支援此功能。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-210">It is supported if a list box contained within a combo box can scroll, and only when the list box is visible on the screen.</span></span>                                                                                                              |



 

## <a name="required-events"></a><span data-ttu-id="9eeb1-211">必要的事件</span><span class="sxs-lookup"><span data-stu-id="9eeb1-211">Required Events</span></span>

<span data-ttu-id="9eeb1-212">下表列出支援的下拉式方塊控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-212">The following table lists the UI Automation events that combo box controls are required to support.</span></span> <span data-ttu-id="9eeb1-213">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="9eeb1-213">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9eeb1-214">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="9eeb1-214">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="9eeb1-215">備註</span><span class="sxs-lookup"><span data-stu-id="9eeb1-215">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9eeb1-216">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-216">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="9eeb1-217">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-217">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="9eeb1-218">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-218">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="9eeb1-219">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-219">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="9eeb1-220">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-220">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="9eeb1-221">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-221">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="9eeb1-222">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-222">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| <span data-ttu-id="9eeb1-223">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-223">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="9eeb1-224">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="9eeb1-225">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="9eeb1-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="9eeb1-226">相關主題</span><span class="sxs-lookup"><span data-stu-id="9eeb1-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9eeb1-227">**概念**</span><span class="sxs-lookup"><span data-stu-id="9eeb1-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9eeb1-228">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="9eeb1-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9eeb1-229">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="9eeb1-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




