---
title: ToolTip 控制項類型
description: 本主題提供工具提示控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。 工具提示控制項是包含文字的快顯視窗。
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- 消費者介面自動化，工具提示控制項類型的支援
- 消費者介面自動化，工具提示控制項類型
- 消費者介面自動化，工具提示控制項類型的樹狀結構
- 消費者介面自動化，工具提示控制項類型的屬性
- 消費者介面自動化，工具提示控制項類型的控制項模式
- 消費者介面自動化，工具提示控制項類型的事件
- 樹狀結構，工具提示控制項類型
- 屬性，工具提示控制項類型
- 控制項模式，工具提示控制項類型
- events、ToolTip 控制項類型
- ToolTip 控制項類型的支援
- ToolTip 控制項類型
- 工具提示控制項類型的控制項類型、樹狀結構
- 控制項類型、工具提示控制項類型的控制項模式
- 控制項類型，支援工具提示
- 控制項類型，工具提示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673071"
---
# <a name="tooltip-control-type"></a><span data-ttu-id="6d439-120">ToolTip 控制項類型</span><span class="sxs-lookup"><span data-stu-id="6d439-120">ToolTip Control Type</span></span>

<span data-ttu-id="6d439-121">本主題提供 **工具提示** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6d439-121">This topic provides information about Microsoft UI Automation support for the **ToolTip** control type.</span></span> <span data-ttu-id="6d439-122">工具提示控制項是包含文字的快顯視窗。</span><span class="sxs-lookup"><span data-stu-id="6d439-122">Tooltip controls are pop-up windows that contain text.</span></span>

<span data-ttu-id="6d439-123">下列章節會定義 **工具提示** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolTip** control type.</span></span> <span data-ttu-id="6d439-124">消費者介面自動化需求適用于所有工具提示控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="6d439-124">The UI Automation requirements apply to all tooltip controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6d439-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6d439-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6d439-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="6d439-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6d439-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="6d439-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6d439-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="6d439-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6d439-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="6d439-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6d439-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d439-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6d439-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="6d439-131">Typical Tree Structure</span></span>

<span data-ttu-id="6d439-132">下表描述與工具提示控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="6d439-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tooltip controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6d439-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="6d439-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d439-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="6d439-134">Control View</span></span></th>
<th><span data-ttu-id="6d439-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="6d439-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6d439-136">ToolTip</span><span class="sxs-lookup"><span data-stu-id="6d439-136">ToolTip</span></span>
<ul>
<li><span data-ttu-id="6d439-137">文字 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="6d439-137">Text (0 or more)</span></span></li>
<li><span data-ttu-id="6d439-138">影像 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="6d439-138">Image (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6d439-139">ToolTip</span><span class="sxs-lookup"><span data-stu-id="6d439-139">ToolTip</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6d439-140">只有當工具提示控制項可以接收鍵盤焦點時，才會出現在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="6d439-140">Tooltip controls appear only in the content view of the UI Automation tree if they can receive keyboard focus.</span></span> <span data-ttu-id="6d439-141">否則，您可以從工具提示所參考專案上的 [**IUIAutomationElement：： CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (或 [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) 屬性取得所有工具提示資訊。</span><span class="sxs-lookup"><span data-stu-id="6d439-141">Otherwise, all of the tooltip's information is available from the [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (or [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) property on the element that the tooltip is referring to.</span></span>

<span data-ttu-id="6d439-142">工具提示應該會出現在其資訊所參考的控制項下方。</span><span class="sxs-lookup"><span data-stu-id="6d439-142">Tooltips should appear beneath the control to which their information is referring.</span></span> <span data-ttu-id="6d439-143">用戶端必須接聽 [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) ，以確保它們持續取得工具提示中包含的資訊。</span><span class="sxs-lookup"><span data-stu-id="6d439-143">Clients must listen for the [**UIA\_ToolTipOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information contained in tooltips.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="6d439-144">相關屬性</span><span class="sxs-lookup"><span data-stu-id="6d439-144">Relevant Properties</span></span>

<span data-ttu-id="6d439-145">下表列出消費者介面自動化屬性，其值或定義與 **工具提示** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="6d439-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolTip** control type.</span></span> <span data-ttu-id="6d439-146">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="6d439-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6d439-147">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="6d439-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6d439-148">值</span><span class="sxs-lookup"><span data-stu-id="6d439-148">Value</span></span>       | <span data-ttu-id="6d439-149">注意</span><span class="sxs-lookup"><span data-stu-id="6d439-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d439-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6d439-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-151">See notes.</span></span>  | <span data-ttu-id="6d439-152">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="6d439-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="6d439-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6d439-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-154">See notes.</span></span>  | <span data-ttu-id="6d439-155">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="6d439-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="6d439-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6d439-157">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-157">See notes.</span></span>  | <span data-ttu-id="6d439-158">可點按的點應該是可關閉控制項的工具提示部分。</span><span class="sxs-lookup"><span data-stu-id="6d439-158">The clickable point should be the part of the tooltip that dismisses the control.</span></span> <span data-ttu-id="6d439-159">某些工具提示沒有這種功能，也不會有可點按的點。</span><span class="sxs-lookup"><span data-stu-id="6d439-159">Some tooltips do not have this ability and will not have a clickable point.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="6d439-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6d439-161">**ToolTip**</span><span class="sxs-lookup"><span data-stu-id="6d439-161">**ToolTip**</span></span> |                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="6d439-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6d439-163">相依</span><span class="sxs-lookup"><span data-stu-id="6d439-163">Depends</span></span>     | <span data-ttu-id="6d439-164">如果工具提示控制項可以接收鍵盤焦點，則它必須出現在樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="6d439-164">If the tooltip control can receive keyboard focus, it must appear in the content view of the tree.</span></span> <span data-ttu-id="6d439-165">如果只是文字，則會從引發它的控制項以 [**IUIAutomationElement：： CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (或 [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) 屬性的形式提供。</span><span class="sxs-lookup"><span data-stu-id="6d439-165">If it is text only, it is available as the [**IUIAutomationElement::CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (or [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) property from the control that raised it.</span></span> |
| [<span data-ttu-id="6d439-166">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6d439-167">對</span><span class="sxs-lookup"><span data-stu-id="6d439-167">True</span></span>        | <span data-ttu-id="6d439-168">工具提示控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="6d439-168">The tooltip control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="6d439-169">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-169">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6d439-170">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-170">See notes.</span></span>  | <span data-ttu-id="6d439-171">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="6d439-171">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="6d439-172">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-172">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6d439-173">NULL</span><span class="sxs-lookup"><span data-stu-id="6d439-173">NULL</span></span>        | <span data-ttu-id="6d439-174">工具提示控制項的內容一律會自行加上標籤。</span><span class="sxs-lookup"><span data-stu-id="6d439-174">Tooltip controls are always self-labeled by their contents.</span></span>                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6d439-175">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-175">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6d439-176">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-176">See notes.</span></span>  | <span data-ttu-id="6d439-177">對應到工具提示控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="6d439-177">Localized string corresponding to the ToolTip control type.</span></span> <span data-ttu-id="6d439-178">預設值為 "tooltip"，適用于 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="6d439-178">The default value is "tooltip" for en-US or English (United States).</span></span>                                                                                                                                                                                                                               |
| [<span data-ttu-id="6d439-179">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6d439-179">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6d439-180">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="6d439-180">See notes.</span></span>  | <span data-ttu-id="6d439-181">工具提示控制項的名稱是顯示在工具提示中的文字。</span><span class="sxs-lookup"><span data-stu-id="6d439-181">The name of the tooltip control is the text that is displayed within the tooltip.</span></span>                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6d439-182">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="6d439-182">Required Control Patterns</span></span>

<span data-ttu-id="6d439-183">下表列出工具提示控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="6d439-183">The following table lists the UI Automation control patterns required to be supported by tooltip controls.</span></span> <span data-ttu-id="6d439-184">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="6d439-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="6d439-185">控制項模式</span><span class="sxs-lookup"><span data-stu-id="6d439-185">Control Pattern</span></span>                                   | <span data-ttu-id="6d439-186">支援</span><span class="sxs-lookup"><span data-stu-id="6d439-186">Support</span></span> | <span data-ttu-id="6d439-187">注意</span><span class="sxs-lookup"><span data-stu-id="6d439-187">Notes</span></span>                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d439-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="6d439-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="6d439-189">相依</span><span class="sxs-lookup"><span data-stu-id="6d439-189">Depends</span></span> | <span data-ttu-id="6d439-190">為了提供更好的協助工具，工具提示控制項可以支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，雖然不是必要的。</span><span class="sxs-lookup"><span data-stu-id="6d439-190">For better accessibility, a tooltip control can support the [Text](uiauto-implementingtextandtextrange.md) control pattern, although it is not required.</span></span> <span data-ttu-id="6d439-191">當文字有豐富的樣式和屬性 (例如色彩、粗體和斜體) 時，這種文字控制項模式相當有用。</span><span class="sxs-lookup"><span data-stu-id="6d439-191">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="6d439-192">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="6d439-192">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | <span data-ttu-id="6d439-193">相依</span><span class="sxs-lookup"><span data-stu-id="6d439-193">Depends</span></span> | <span data-ttu-id="6d439-194">您可以按一下 UI 專案來關閉的工具提示，必須支援 [視窗](uiauto-implementingwindow.md) 控制項模式，才能自動關閉。</span><span class="sxs-lookup"><span data-stu-id="6d439-194">Tooltips that can be closed by clicking a UI item must support the [Window](uiauto-implementingwindow.md) control pattern so that they can closed automatically.</span></span>                                                                                                                 |



 

## <a name="required-events"></a><span data-ttu-id="6d439-195">必要的事件</span><span class="sxs-lookup"><span data-stu-id="6d439-195">Required Events</span></span>

<span data-ttu-id="6d439-196">當工具提示控制項出現在螢幕上時，必須引發 [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-196">Tooltip controls must raise the [**UIA\_ToolTipOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="6d439-197">此事件會包含工具提示本身之消費者介面自動化專案的參考。</span><span class="sxs-lookup"><span data-stu-id="6d439-197">The event will include a reference to the UI Automation element of the tooltip itself.</span></span>

<span data-ttu-id="6d439-198">下表列出支援工具提示控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-198">The following table lists the UI Automation events that tooltip controls are required to support.</span></span> <span data-ttu-id="6d439-199">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="6d439-199">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6d439-200">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="6d439-200">UI Automation Event</span></span>                                                                                                                            | <span data-ttu-id="6d439-201">備註</span><span class="sxs-lookup"><span data-stu-id="6d439-201">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d439-202">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-202">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                               |                                                                                                                            |
| <span data-ttu-id="6d439-203">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-203">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>          |                                                                                                                            |
| <span data-ttu-id="6d439-204">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-204">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                          | <span data-ttu-id="6d439-205">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-205">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="6d439-206">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-206">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      | <span data-ttu-id="6d439-207">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-207">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="6d439-208">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-208">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                    |                                                                                                                            |
| [<span data-ttu-id="6d439-209">**UIA \_ 文字 \_ TextChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-209">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                          | <span data-ttu-id="6d439-210">如果控制項支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-210">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="6d439-211">**UIA \_ ToolTipClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-211">**UIA\_ToolTipClosedEventId**</span></span>](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [<span data-ttu-id="6d439-212">**UIA \_ ToolTipOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-212">**UIA\_ToolTipOpenedEventId**</span></span>](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [<span data-ttu-id="6d439-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [<span data-ttu-id="6d439-214">**UIA \_ 視窗 \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-214">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="6d439-215">如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-215">If the control supports the [Window](uiauto-implementingwindow.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="6d439-216">**UIA \_ 視窗 \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="6d439-216">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="6d439-217">如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-217">If the control supports the [Window](uiauto-implementingwindow.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="6d439-218">[**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-218">[**UIA\_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="6d439-219">如果控制項支援 [Window](uiauto-implementingwindow.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="6d439-219">If the control supports the [Window](uiauto-implementingwindow.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="6d439-220">相關主題</span><span class="sxs-lookup"><span data-stu-id="6d439-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d439-221">**概念**</span><span class="sxs-lookup"><span data-stu-id="6d439-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6d439-222">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="6d439-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6d439-223">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="6d439-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




