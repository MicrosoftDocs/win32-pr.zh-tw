---
title: Text 控制項類型
description: 本主題提供 Text 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- 消費者介面自動化，文字控制項類型的支援
- 消費者介面自動化，文字控制項類型
- 消費者介面自動化，Text 控制項類型的樹狀結構
- 消費者介面自動化，Text 控制項類型的屬性
- 消費者介面自動化，文字控制項類型的控制項模式
- 消費者介面自動化，Text 控制項類型的事件
- 樹狀結構，文字控制項類型
- 屬性，文字控制項類型
- 控制項模式，文字控制項類型
- events、Text 控制項類型
- Text 控制項類型的支援
- Text 控制項類型
- 控制項類型，文字控制項類型的樹狀結構
- 控制項類型，文字控制項類型的控制項模式
- 控制項類型，支援文字
- 控制項類型，文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301428"
---
# <a name="text-control-type"></a><span data-ttu-id="3123f-119">Text 控制項類型</span><span class="sxs-lookup"><span data-stu-id="3123f-119">Text Control Type</span></span>

<span data-ttu-id="3123f-120">本主題提供 **Text** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3123f-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="3123f-121">文字控制項是代表螢幕上某段文字的基本使用者介面專案。</span><span class="sxs-lookup"><span data-stu-id="3123f-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="3123f-122">下列章節會定義 **Text** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="3123f-123">消費者介面自動化需求適用于所有的樹狀目錄控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="3123f-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="3123f-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="3123f-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3123f-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="3123f-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3123f-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="3123f-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3123f-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="3123f-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="3123f-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="3123f-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3123f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="3123f-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3123f-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="3123f-130">Typical Tree Structure</span></span>

<span data-ttu-id="3123f-131">下表描述文字控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="3123f-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="3123f-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="3123f-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3123f-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="3123f-133">Control View</span></span></th>
<th><span data-ttu-id="3123f-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="3123f-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3123f-135">Text</span><span class="sxs-lookup"><span data-stu-id="3123f-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3123f-136">Text (如果內容)</span><span class="sxs-lookup"><span data-stu-id="3123f-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3123f-137">控制項可以單獨用來當做標籤或當做表單上的靜態文字。</span><span class="sxs-lookup"><span data-stu-id="3123f-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="3123f-138">它也可以包含在下列其中一個專案的結構內：</span><span class="sxs-lookup"><span data-stu-id="3123f-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="3123f-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="3123f-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="3123f-140">ListItem</span><span class="sxs-lookup"><span data-stu-id="3123f-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="3123f-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="3123f-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="3123f-142">文字控制項可能不會出現在消費者介面自動化樹狀結構的內容視圖中，因為文字通常是透過另一個控制項的 [ **名稱** ] 屬性來顯示。</span><span class="sxs-lookup"><span data-stu-id="3123f-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="3123f-143">例如，用來為下拉式方塊控制項加上標籤的文字，會透過控制項的 [ **名稱** ] 屬性來公開。</span><span class="sxs-lookup"><span data-stu-id="3123f-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="3123f-144">因為下拉式方塊控制項位於消費者介面自動化樹狀結構的內容視圖中，所以不需要有文字控制項。</span><span class="sxs-lookup"><span data-stu-id="3123f-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="3123f-145">如果有内嵌物件（例如超連結），則文字控制項在內容視圖中可能會有子系。</span><span class="sxs-lookup"><span data-stu-id="3123f-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="3123f-146">相關屬性</span><span class="sxs-lookup"><span data-stu-id="3123f-146">Relevant Properties</span></span>

<span data-ttu-id="3123f-147">下表列出消費者介面自動化屬性，其值或定義與文字控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="3123f-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="3123f-148">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="3123f-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="3123f-149">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="3123f-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="3123f-150">值</span><span class="sxs-lookup"><span data-stu-id="3123f-150">Value</span></span>      | <span data-ttu-id="3123f-151">注意</span><span class="sxs-lookup"><span data-stu-id="3123f-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3123f-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="3123f-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-153">See notes.</span></span> | <span data-ttu-id="3123f-154">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3123f-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="3123f-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="3123f-156">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-156">See notes.</span></span> | <span data-ttu-id="3123f-157">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="3123f-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="3123f-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="3123f-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-159">See notes.</span></span> | <span data-ttu-id="3123f-160">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="3123f-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="3123f-161">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="3123f-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="3123f-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3123f-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="3123f-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="3123f-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3123f-165">相依</span><span class="sxs-lookup"><span data-stu-id="3123f-165">Depends</span></span>    | <span data-ttu-id="3123f-166">如果文字控制項包含未在另一個控制項的名稱屬性中公開的資訊，則為內容。</span><span class="sxs-lookup"><span data-stu-id="3123f-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="3123f-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3123f-168">true</span><span class="sxs-lookup"><span data-stu-id="3123f-168">TRUE</span></span>       | <span data-ttu-id="3123f-169">文字控制項必須一律為控制項。</span><span class="sxs-lookup"><span data-stu-id="3123f-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="3123f-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="3123f-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-171">See notes.</span></span> | <span data-ttu-id="3123f-172">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="3123f-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3123f-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3123f-174">NULL</span><span class="sxs-lookup"><span data-stu-id="3123f-174">NULL</span></span>       | <span data-ttu-id="3123f-175">文字控制項沒有靜態文字標籤。</span><span class="sxs-lookup"><span data-stu-id="3123f-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3123f-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="3123f-177">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-177">See notes.</span></span> | <span data-ttu-id="3123f-178">對應至 **文字** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="3123f-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="3123f-179">預設值為 "text" 代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="3123f-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="3123f-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3123f-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="3123f-181">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3123f-181">See notes.</span></span> | <span data-ttu-id="3123f-182">文字控制項的名稱可以是它所顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="3123f-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="3123f-183">但是，如果控制項也支援 [文字](uiauto-implementingtextandtextrange.md) 模式，且文字很廣泛，請不要使用全文檢索內容作為 **名稱** 值。</span><span class="sxs-lookup"><span data-stu-id="3123f-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="3123f-184">請改為提供較短的 **名稱** 值，其衍生自您的控制項的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="3123f-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="3123f-185">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="3123f-185">Required Control Patterns</span></span>

<span data-ttu-id="3123f-186">下表列出文字控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="3123f-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="3123f-187">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="3123f-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="3123f-188">控制項模式</span><span class="sxs-lookup"><span data-stu-id="3123f-188">Control Pattern</span></span>                                         | <span data-ttu-id="3123f-189">支援</span><span class="sxs-lookup"><span data-stu-id="3123f-189">Support</span></span> | <span data-ttu-id="3123f-190">注意</span><span class="sxs-lookup"><span data-stu-id="3123f-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3123f-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3123f-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="3123f-192">相依</span><span class="sxs-lookup"><span data-stu-id="3123f-192">Depends</span></span> | <span data-ttu-id="3123f-193">如果文字控制項包含在資料表控制項中，則必須支援 [GridItem](uiauto-implementinggriditem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="3123f-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="3123f-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3123f-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="3123f-195">相依</span><span class="sxs-lookup"><span data-stu-id="3123f-195">Depends</span></span> | <span data-ttu-id="3123f-196">如果文字控制項包含在資料表控制項中，則必須支援 [TableItem](uiauto-implementingtableitem.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="3123f-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="3123f-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="3123f-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="3123f-198">相依</span><span class="sxs-lookup"><span data-stu-id="3123f-198">Depends</span></span> | <span data-ttu-id="3123f-199">文字應該支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，以提供更好的協助工具;不過，這不是必要的。</span><span class="sxs-lookup"><span data-stu-id="3123f-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="3123f-200">當文字有豐富的樣式和屬性 (例如色彩、粗體和斜體) 時，這種文字控制項模式相當有用。</span><span class="sxs-lookup"><span data-stu-id="3123f-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="3123f-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="3123f-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="3123f-202">永不</span><span class="sxs-lookup"><span data-stu-id="3123f-202">Never</span></span>   | <span data-ttu-id="3123f-203">文字控制項永遠不支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="3123f-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="3123f-204">如果文字是可編輯的，則為 [編輯](uiauto-supporteditcontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="3123f-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="3123f-205">必要的事件</span><span class="sxs-lookup"><span data-stu-id="3123f-205">Required Events</span></span>

<span data-ttu-id="3123f-206">下表列出文字控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="3123f-207">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="3123f-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3123f-208">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="3123f-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="3123f-209">備註</span><span class="sxs-lookup"><span data-stu-id="3123f-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3123f-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3123f-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="3123f-211">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="3123f-212">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="3123f-213">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="3123f-214">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="3123f-215">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="3123f-216">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="3123f-217">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3123f-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="3123f-218">**UIA \_ 文字 \_ TextChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3123f-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="3123f-219">如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="3123f-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="3123f-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="3123f-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3123f-221">**概念**</span><span class="sxs-lookup"><span data-stu-id="3123f-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3123f-222">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="3123f-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3123f-223">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="3123f-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




