---
title: 選項按鈕控制項類型
description: 本主題提供 [選項按鈕] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- 消費者介面自動化，支援選項按鈕控制項類型
- 消費者介面自動化，選項按鈕控制項類型
- 消費者介面自動化，選項按鈕控制項類型的樹狀結構
- 消費者介面自動化，選項按鈕控制項類型的屬性
- 消費者介面自動化，選項按鈕控制項類型的控制項模式
- 消費者介面自動化，選項按鈕控制項類型的事件
- 樹狀結構，選項按鈕控制項類型
- 屬性，選項按鈕控制項類型
- 控制項模式，選項按鈕控制項類型
- 事件、選項按鈕控制項類型
- 選項按鈕控制項類型的支援
- RadioButton 控制項類型
- 選項按鈕控制項類型的控制項類型、樹狀結構
- 控制項類型，選項按鈕控制項類型的控制項模式
- 控制項類型，支援選項按鈕
- 控制項類型，選項按鈕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674668"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="00d7b-119">選項按鈕控制項類型</span><span class="sxs-lookup"><span data-stu-id="00d7b-119">RadioButton Control Type</span></span>

<span data-ttu-id="00d7b-120">本主題提供 [ **選項按鈕** ] 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="00d7b-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="00d7b-121">選項按鈕包含一個圓形按鈕和應用程式定義的文字 (標籤)、圖示或點陣圖，其中會指出使用者可以藉由選取按鈕所進行的選擇。</span><span class="sxs-lookup"><span data-stu-id="00d7b-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="00d7b-122">應用程式通常會在群組方塊中使用選項按鈕，讓使用者選擇一組相關但彼此互斥的選項。</span><span class="sxs-lookup"><span data-stu-id="00d7b-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="00d7b-123">例如，應用程式可能會顯示一組選項按鈕，讓使用者可以針對用戶端區域所選取的文字選取偏好的格式。</span><span class="sxs-lookup"><span data-stu-id="00d7b-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="00d7b-124">使用者可以選取對應的選項按鈕，決定要靠左對齊、靠右對齊或置中對齊的格式。</span><span class="sxs-lookup"><span data-stu-id="00d7b-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="00d7b-125">使用者通常一次只能從一組選項按鈕選取一個選項。</span><span class="sxs-lookup"><span data-stu-id="00d7b-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="00d7b-126">按鈕的另一個控制項一般化，其中只有一個群組中的按鈕可以選取切換按鈕的內容。</span><span class="sxs-lookup"><span data-stu-id="00d7b-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="00d7b-127">某些 UI 架構會將選項按鈕視為特製化切換按鈕。</span><span class="sxs-lookup"><span data-stu-id="00d7b-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="00d7b-128">下列章節會定義 **選項按鈕** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="00d7b-129">消費者介面自動化需求適用于所有按鈕控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="00d7b-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="00d7b-130">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="00d7b-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="00d7b-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="00d7b-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="00d7b-132">相關屬性</span><span class="sxs-lookup"><span data-stu-id="00d7b-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="00d7b-133">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="00d7b-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="00d7b-134">必要的事件</span><span class="sxs-lookup"><span data-stu-id="00d7b-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="00d7b-135">備註</span><span class="sxs-lookup"><span data-stu-id="00d7b-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="00d7b-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="00d7b-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="00d7b-137">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="00d7b-137">Typical Tree Structure</span></span>

<span data-ttu-id="00d7b-138">下表描述的是與選項按鈕控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="00d7b-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="00d7b-139">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="00d7b-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d7b-140">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="00d7b-140">Control View</span></span></th>
<th><span data-ttu-id="00d7b-141">內容檢視</span><span class="sxs-lookup"><span data-stu-id="00d7b-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="00d7b-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="00d7b-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="00d7b-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="00d7b-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="00d7b-144">控制項檢視或內容檢視中沒有任何子系。</span><span class="sxs-lookup"><span data-stu-id="00d7b-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="00d7b-145">相關屬性</span><span class="sxs-lookup"><span data-stu-id="00d7b-145">Relevant Properties</span></span>

<span data-ttu-id="00d7b-146">下表列出消費者介面自動化屬性，其值或定義與執行 **單選** 按鈕控制項 (類型的控制項（例如按鈕控制項) ）特別相關。</span><span class="sxs-lookup"><span data-stu-id="00d7b-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="00d7b-147">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="00d7b-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="00d7b-148">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="00d7b-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="00d7b-149">值</span><span class="sxs-lookup"><span data-stu-id="00d7b-149">Value</span></span>           | <span data-ttu-id="00d7b-150">注意</span><span class="sxs-lookup"><span data-stu-id="00d7b-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d7b-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="00d7b-152">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-152">See notes.</span></span>      | <span data-ttu-id="00d7b-153">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="00d7b-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="00d7b-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="00d7b-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-155">See notes.</span></span>      | <span data-ttu-id="00d7b-156">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="00d7b-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="00d7b-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="00d7b-158">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-158">See notes.</span></span>      | <span data-ttu-id="00d7b-159">可點按的點必須在按下時，選取選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="00d7b-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="00d7b-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="00d7b-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="00d7b-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="00d7b-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="00d7b-163">true</span><span class="sxs-lookup"><span data-stu-id="00d7b-163">TRUE</span></span>            | <span data-ttu-id="00d7b-164">選項按鈕控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="00d7b-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="00d7b-165">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="00d7b-166">true</span><span class="sxs-lookup"><span data-stu-id="00d7b-166">TRUE</span></span>            | <span data-ttu-id="00d7b-167">選項按鈕控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="00d7b-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="00d7b-168">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="00d7b-169">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-169">See notes.</span></span>      | <span data-ttu-id="00d7b-170">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="00d7b-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="00d7b-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="00d7b-172">NULL</span><span class="sxs-lookup"><span data-stu-id="00d7b-172">NULL</span></span>            | <span data-ttu-id="00d7b-173">選項按鈕控制項的內容會自行標示。</span><span class="sxs-lookup"><span data-stu-id="00d7b-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="00d7b-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="00d7b-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-175">See notes.</span></span>      | <span data-ttu-id="00d7b-176">對應至 **選項按鈕** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="00d7b-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="00d7b-177">預設值為 en-us 或英文 (美國) 的「選項按鈕」。</span><span class="sxs-lookup"><span data-stu-id="00d7b-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="00d7b-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="00d7b-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-179">See notes.</span></span>      | <span data-ttu-id="00d7b-180">選項按鈕控制項的名稱是在維持選取狀態的按鈕旁邊顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="00d7b-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="00d7b-181">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="00d7b-181">Required Control Patterns</span></span>

<span data-ttu-id="00d7b-182">下表列出所有選項按鈕控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="00d7b-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="00d7b-183">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="00d7b-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="00d7b-184">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="00d7b-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="00d7b-185">支援/值</span><span class="sxs-lookup"><span data-stu-id="00d7b-185">Support/Value</span></span> | <span data-ttu-id="00d7b-186">備註</span><span class="sxs-lookup"><span data-stu-id="00d7b-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d7b-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="00d7b-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="00d7b-188">必要</span><span class="sxs-lookup"><span data-stu-id="00d7b-188">Required</span></span>      | <span data-ttu-id="00d7b-189">所有的選項按鈕控制項都必須支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，才能讓自己選取。</span><span class="sxs-lookup"><span data-stu-id="00d7b-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="00d7b-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="00d7b-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="00d7b-191">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="00d7b-191">See notes.</span></span>    | <span data-ttu-id="00d7b-192">[**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)屬性必須一律完成，讓消費者介面自動化用戶端可以判斷特定內容中的其他選項按鈕彼此之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="00d7b-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="00d7b-193">針對 Microsoft Win32 版本的選項按鈕，不支援這個屬性，因為無法從該舊版 framework 取得這項資訊。</span><span class="sxs-lookup"><span data-stu-id="00d7b-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="00d7b-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="00d7b-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="00d7b-195">永不</span><span class="sxs-lookup"><span data-stu-id="00d7b-195">Never</span></span>         | <span data-ttu-id="00d7b-196">選項按鈕一旦設定就無法循環其狀態。</span><span class="sxs-lookup"><span data-stu-id="00d7b-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="00d7b-197">選項按鈕上永遠不支援 [切換](uiauto-implementingtoggle.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="00d7b-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="00d7b-198">必要的事件</span><span class="sxs-lookup"><span data-stu-id="00d7b-198">Required Events</span></span>

<span data-ttu-id="00d7b-199">下表列出按鈕控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="00d7b-200">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="00d7b-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="00d7b-201">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="00d7b-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="00d7b-202">備註</span><span class="sxs-lookup"><span data-stu-id="00d7b-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="00d7b-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="00d7b-204">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="00d7b-205">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="00d7b-206">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="00d7b-207">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="00d7b-208">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="00d7b-209">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="00d7b-210">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="00d7b-211">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="00d7b-212">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="00d7b-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="00d7b-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="00d7b-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="00d7b-214">備註</span><span class="sxs-lookup"><span data-stu-id="00d7b-214">Remarks</span></span>

<span data-ttu-id="00d7b-215">選項按鈕表示一組對等選項按鈕之間的單一可選取選項。</span><span class="sxs-lookup"><span data-stu-id="00d7b-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="00d7b-216">在理想的情況下，選項按鈕應該有一個說明對等選項按鈕界限的群組元素。</span><span class="sxs-lookup"><span data-stu-id="00d7b-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="00d7b-217">不過，通常 UI 元素結構會隱含界限。</span><span class="sxs-lookup"><span data-stu-id="00d7b-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="00d7b-218">例如，功能表可能包含一組連續的選項按鈕，而不是功能表項目，或是一組出現在群組標籤之後，但可採取動作的元素（例如按鈕）之前的選項按鈕。</span><span class="sxs-lookup"><span data-stu-id="00d7b-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="00d7b-219">相關主題</span><span class="sxs-lookup"><span data-stu-id="00d7b-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="00d7b-220">**概念**</span><span class="sxs-lookup"><span data-stu-id="00d7b-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00d7b-221">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="00d7b-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="00d7b-222">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="00d7b-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




