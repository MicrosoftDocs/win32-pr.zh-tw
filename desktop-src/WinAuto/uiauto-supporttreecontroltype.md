---
title: 樹狀目錄控制項類型
description: 本主題提供樹狀結構控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- 消費者介面自動化，支援樹狀目錄控制項類型
- 消費者介面自動化，樹狀目錄控制項類型
- 消費者介面自動化，樹狀結構控制項類型的樹狀結構
- 消費者介面自動化，樹狀目錄控制項類型的屬性
- 消費者介面自動化，樹狀結構控制項類型的控制項模式
- 消費者介面自動化，樹狀目錄控制項類型的事件
- 樹狀結構，樹狀目錄控制項類型
- 屬性，樹狀目錄控制項類型
- 控制項模式，樹狀目錄控制項類型
- 事件，樹狀目錄控制項類型
- 樹狀目錄控制項類型的支援
- Tree 控制項類型
- 控制項類型，樹狀結構控制項類型的樹狀結構
- 控制項類型，樹狀結構控制項類型的控制項模式
- 控制項類型，支援樹狀結構
- 控制項類型，樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4679af32f974cd1611cbd31c71e66db62631391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023914"
---
# <a name="tree-control-type"></a><span data-ttu-id="cfb28-119">樹狀目錄控制項類型</span><span class="sxs-lookup"><span data-stu-id="cfb28-119">Tree Control Type</span></span>

<span data-ttu-id="cfb28-120">本主題提供 **樹狀結構** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cfb28-120">This topic provides information about Microsoft UI Automation support for the **Tree** control type.</span></span>

<span data-ttu-id="cfb28-121">**樹狀** 結構控制項類型用於其內容與節點階層具有相關性的容器，如同在 Windows 檔案總管的左窗格中顯示檔案和資料夾的方式。</span><span class="sxs-lookup"><span data-stu-id="cfb28-121">The **Tree** control type is used for containers whose contents have relevance as a hierarchy of nodes, as with the way files and folders are displayed in the left pane of Windows Explorer.</span></span> <span data-ttu-id="cfb28-122">每個節點都可能包含其他節點，稱為子節點。</span><span class="sxs-lookup"><span data-stu-id="cfb28-122">Each node has the potential to contain other nodes, called child nodes.</span></span> <span data-ttu-id="cfb28-123">父節點或包含子節點的節點可以顯示為展開或摺疊。</span><span class="sxs-lookup"><span data-stu-id="cfb28-123">Parent nodes, or nodes that contain child nodes, can be displayed as expanded or collapsed.</span></span> <span data-ttu-id="cfb28-124">[**WC \_ TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)) 所識別的 Windows 樹狀檢視控制項 (是屬於 **樹狀結構** 控制項類型的控制項範例。</span><span class="sxs-lookup"><span data-stu-id="cfb28-124">The Windows tree-view control (as identified by [**WC\_TREEVIEW**](/windows/desktop/Controls/common-control-window-classes)) is an example of a control that belongs to the **Tree** control type.</span></span>

<span data-ttu-id="cfb28-125">下列章節會定義 **樹狀** 結構控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tree** control type.</span></span> <span data-ttu-id="cfb28-126">消費者介面自動化需求適用于所有樹狀結構專案控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="cfb28-126">The UI Automation requirements apply to all tree item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="cfb28-127">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="cfb28-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="cfb28-128">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="cfb28-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="cfb28-129">相關屬性</span><span class="sxs-lookup"><span data-stu-id="cfb28-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="cfb28-130">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="cfb28-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="cfb28-131">必要的事件</span><span class="sxs-lookup"><span data-stu-id="cfb28-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="cfb28-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="cfb28-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="cfb28-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="cfb28-133">Typical Tree Structure</span></span>

<span data-ttu-id="cfb28-134">下表描述樹狀結構控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="cfb28-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to tree controls, and describes what can be contained in each view.</span></span> <span data-ttu-id="cfb28-135">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb28-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cfb28-136">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="cfb28-136">Control View</span></span></th>
<th><span data-ttu-id="cfb28-137">內容檢視</span><span class="sxs-lookup"><span data-stu-id="cfb28-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="cfb28-138">樹狀結構</span><span class="sxs-lookup"><span data-stu-id="cfb28-138">Tree</span></span>
<ul>
<li><span data-ttu-id="cfb28-139">DataItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-139">DataItem (0 or more)</span></span></li>
<li><span data-ttu-id="cfb28-140">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-140">TreeItem (0 or more)</span></span>
<ul>
<li><span data-ttu-id="cfb28-141">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-141">TreeItem (0 or more)</span></span>
<ul>
<li><span data-ttu-id="cfb28-142">...</span><span class="sxs-lookup"><span data-stu-id="cfb28-142">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="cfb28-143">捲軸 (0、1、2 個)</span><span class="sxs-lookup"><span data-stu-id="cfb28-143">ScrollBar (0, 1, 2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="cfb28-144">樹狀結構</span><span class="sxs-lookup"><span data-stu-id="cfb28-144">Tree</span></span>
<ul>
<li><span data-ttu-id="cfb28-145">DataItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-145">DataItem (0 or more)</span></span></li>
<li><span data-ttu-id="cfb28-146">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-146">TreeItem (0 or more)</span></span>
<ul>
<li><span data-ttu-id="cfb28-147">TreeItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="cfb28-147">TreeItem (0 or more)</span></span>
<ul>
<li><span data-ttu-id="cfb28-148">...</span><span class="sxs-lookup"><span data-stu-id="cfb28-148">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cfb28-149">消費者介面自動化樹狀結構的控制視圖包含：</span><span class="sxs-lookup"><span data-stu-id="cfb28-149">The control view of the UI Automation tree consists of:</span></span>

-   <span data-ttu-id="cfb28-150">容器內的許多專案中有零個 (專案可以根據) 的 [TreeItem](uiauto-supporttreeitemcontroltype.md) 或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="cfb28-150">Zero of many items within the container (items can be based on the [TreeItem](uiauto-supporttreeitemcontroltype.md) or [DataItem](uiauto-supportdataitemcontroltype.md) control types).</span></span>
-   <span data-ttu-id="cfb28-151">0、1 或 2 個捲軸控制項</span><span class="sxs-lookup"><span data-stu-id="cfb28-151">Zero, one, or two scroll bar controls</span></span>

<span data-ttu-id="cfb28-152">消費者介面自動化樹狀結構的內容視圖是由容器內的零或多個專案所組成 (專案可以) 的 [TreeItem](uiauto-supporttreeitemcontroltype.md) 或 [DataItem](uiauto-supportdataitemcontroltype.md) 控制項類型為基礎。</span><span class="sxs-lookup"><span data-stu-id="cfb28-152">The content view of the UI Automation tree consists of zero or many items within the container (items can be based on the [TreeItem](uiauto-supporttreeitemcontroltype.md) or [DataItem](uiauto-supportdataitemcontroltype.md) control types).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="cfb28-153">相關屬性</span><span class="sxs-lookup"><span data-stu-id="cfb28-153">Relevant Properties</span></span>

<span data-ttu-id="cfb28-154">下表列出消費者介面自動化屬性，其值或定義與 **樹狀結構** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="cfb28-154">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Tree** control type.</span></span> <span data-ttu-id="cfb28-155">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb28-155">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="cfb28-156">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="cfb28-156">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="cfb28-157">值</span><span class="sxs-lookup"><span data-stu-id="cfb28-157">Value</span></span>      | <span data-ttu-id="cfb28-158">注意</span><span class="sxs-lookup"><span data-stu-id="cfb28-158">Notes</span></span>                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfb28-159">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-159">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="cfb28-160">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-160">See notes.</span></span> | <span data-ttu-id="cfb28-161">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="cfb28-161">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="cfb28-162">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="cfb28-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-163">See notes.</span></span> | <span data-ttu-id="cfb28-164">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="cfb28-164">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                   |
| [<span data-ttu-id="cfb28-165">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-165">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="cfb28-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-166">See notes.</span></span> | <span data-ttu-id="cfb28-167">樹狀目錄控制項具有可點按的點，讓樹狀結構或樹狀結構中的其中一個專案接收焦點。</span><span class="sxs-lookup"><span data-stu-id="cfb28-167">Tree controls have a clickable point that causes the tree or one of the items in the tree container to receive the focus.</span></span> <span data-ttu-id="cfb28-168">只有當您可以按一下樹狀結構中的位置，而不會造成選取專案或接收焦點時，樹狀目錄控制項才可以有可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="cfb28-168">A tree control can have a clickable point only if it is possible to click a location in the tree without causing an item to be selected or to receive the focus.</span></span> |
| [<span data-ttu-id="cfb28-169">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-169">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="cfb28-170">**樹狀結構**</span><span class="sxs-lookup"><span data-stu-id="cfb28-170">**Tree**</span></span>   | <span data-ttu-id="cfb28-171">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="cfb28-171">This value is the same for all UI frameworks.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="cfb28-172">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-172">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="cfb28-173">true</span><span class="sxs-lookup"><span data-stu-id="cfb28-173">TRUE</span></span>       | <span data-ttu-id="cfb28-174">樹狀目錄控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="cfb28-174">The tree control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="cfb28-175">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-175">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="cfb28-176">true</span><span class="sxs-lookup"><span data-stu-id="cfb28-176">TRUE</span></span>       | <span data-ttu-id="cfb28-177">樹狀目錄控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="cfb28-177">The tree control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="cfb28-178">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-178">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="cfb28-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-179">See notes.</span></span> | <span data-ttu-id="cfb28-180">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb28-180">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="cfb28-181">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-181">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="cfb28-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-182">See notes.</span></span> | <span data-ttu-id="cfb28-183">如果樹狀目錄控制項有與其相關聯的標籤，則此屬性會傳回該標籤的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 指標。</span><span class="sxs-lookup"><span data-stu-id="cfb28-183">If the tree control has a label associated with it, this property returns a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pointer for that label.</span></span> <span data-ttu-id="cfb28-184">否則，屬性會傳回 null 參考。</span><span class="sxs-lookup"><span data-stu-id="cfb28-184">Otherwise, the property returns a null reference.</span></span>                                                                          |
| [<span data-ttu-id="cfb28-185">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="cfb28-186">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-186">See notes.</span></span> | <span data-ttu-id="cfb28-187">對應至 **樹狀結構** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="cfb28-187">Localized string corresponding to the **Tree** control type.</span></span> <span data-ttu-id="cfb28-188">預設值為 "tree" （適用于 en-us）或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="cfb28-188">The default value is "tree" for en-US or English (United States).</span></span>                                                                                                                                                             |
| [<span data-ttu-id="cfb28-189">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="cfb28-190">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-190">See notes.</span></span> | <span data-ttu-id="cfb28-191">樹狀結構控制項的名稱屬性值通常取自於控制項的標籤文字。</span><span class="sxs-lookup"><span data-stu-id="cfb28-191">The value of a tree control's name property usually comes from text that labels the control.</span></span> <span data-ttu-id="cfb28-192">如果沒有文字標籤，您必須提供這個屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cfb28-192">If there is no text label, you must provide a value for this property.</span></span>                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="cfb28-193">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="cfb28-193">Required Control Patterns</span></span>

<span data-ttu-id="cfb28-194">下表列出所有樹狀結構控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="cfb28-194">The following table lists the UI Automation control patterns required to be supported by all tree controls.</span></span> <span data-ttu-id="cfb28-195">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="cfb28-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="cfb28-196">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="cfb28-196">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="cfb28-197">支援/值</span><span class="sxs-lookup"><span data-stu-id="cfb28-197">Support/Value</span></span> | <span data-ttu-id="cfb28-198">備註</span><span class="sxs-lookup"><span data-stu-id="cfb28-198">Notes</span></span>                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfb28-199">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="cfb28-199">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="cfb28-200">相依</span><span class="sxs-lookup"><span data-stu-id="cfb28-200">Depends</span></span>       | <span data-ttu-id="cfb28-201">如果樹狀結構容器中的專案可以滾動，請執行 [滾動](uiauto-implementingscroll.md) 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="cfb28-201">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if items in the tree container can be scrolled.</span></span>                                                                                                                 |
| [<span data-ttu-id="cfb28-202">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="cfb28-202">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="cfb28-203">相依</span><span class="sxs-lookup"><span data-stu-id="cfb28-203">Depends</span></span>       | <span data-ttu-id="cfb28-204">包含一組可選取專案的樹狀目錄控制項必須執行 [選取](uiauto-implementingselection.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="cfb28-204">Tree controls that contain a set of selectable items must implement the [Selection](uiauto-implementingselection.md) control pattern.</span></span> <span data-ttu-id="cfb28-205">如果選取專案不會對使用者傳達有意義的資訊，則不需要執行此專案。</span><span class="sxs-lookup"><span data-stu-id="cfb28-205">It need not be implemented if selecting an item conveys no meaningful information to the user.</span></span> |
| [<span data-ttu-id="cfb28-206">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="cfb28-206">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="cfb28-207">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-207">See notes.</span></span>    | <span data-ttu-id="cfb28-208">如果樹狀結構控制項支援多重選取 (大多數樹狀結構控制項並不支援多重選取)，即實作此屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb28-208">Implement this property if the tree control supports multiple selection (most tree controls do not support multiple selection).</span></span>                                                                                                       |
| [<span data-ttu-id="cfb28-209">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="cfb28-209">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="cfb28-210">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="cfb28-210">See notes.</span></span>    | <span data-ttu-id="cfb28-211">如果控制項需要選取項目，則會公開此屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cfb28-211">The value of this property is exposed if the control requires that an item be selected.</span></span>                                                                                                                                               |



 

## <a name="required-events"></a><span data-ttu-id="cfb28-212">必要的事件</span><span class="sxs-lookup"><span data-stu-id="cfb28-212">Required Events</span></span>

<span data-ttu-id="cfb28-213">下表列出所有樹狀結構控制項都必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-213">The following table lists the UI Automation events that all tree controls must support.</span></span> <span data-ttu-id="cfb28-214">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="cfb28-214">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="cfb28-215">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="cfb28-215">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="cfb28-216">備註</span><span class="sxs-lookup"><span data-stu-id="cfb28-216">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cfb28-217">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-217">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="cfb28-218">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-218">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="cfb28-219">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-219">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="cfb28-220">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-220">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="cfb28-221">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-221">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="cfb28-222">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-222">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="cfb28-223">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="cfb28-224">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="cfb28-225">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="cfb28-226">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="cfb28-227">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="cfb28-228">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="cfb28-229">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="cfb28-230">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="cfb28-231">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="cfb28-232">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="cfb28-233">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="cfb28-234">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="cfb28-235">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="cfb28-236">如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="cfb28-236">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="cfb28-237">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="cfb28-237">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="cfb28-238">相關主題</span><span class="sxs-lookup"><span data-stu-id="cfb28-238">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cfb28-239">**概念**</span><span class="sxs-lookup"><span data-stu-id="cfb28-239">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cfb28-240">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="cfb28-240">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="cfb28-241">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="cfb28-241">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 