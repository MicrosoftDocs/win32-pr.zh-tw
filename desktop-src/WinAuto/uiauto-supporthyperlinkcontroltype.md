---
title: Hyperlink 控制項類型
description: 本主題提供超連結控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- 消費者介面自動化，支援 Hyperlink 控制項類型
- 消費者介面自動化，超連結控制項類型
- 消費者介面自動化，超連結控制項類型的樹狀結構
- 消費者介面自動化，超連結控制項類型的屬性
- 消費者介面自動化，超連結控制項類型的控制項模式
- 消費者介面自動化，超連結控制項類型的事件
- 樹狀結構，超連結控制項類型
- 屬性，超連結控制項類型
- 控制項模式，超連結控制項類型
- 事件，超連結控制項類型
- Hyperlink 控制項類型的支援
- Hyperlink 控制項類型
- 控制項類型，超連結控制項類型的樹狀結構
- 控制項類型，超連結控制項類型的控制項模式
- 控制項類型，支援超連結
- 控制項類型，超連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673075"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="0257a-119">Hyperlink 控制項類型</span><span class="sxs-lookup"><span data-stu-id="0257a-119">Hyperlink Control Type</span></span>

<span data-ttu-id="0257a-120">本主題提供 **超連結** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0257a-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="0257a-121">超連結控制項可建立連結，讓使用者在同一個頁面中或從一個頁面流覽至另一個頁面。</span><span class="sxs-lookup"><span data-stu-id="0257a-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="0257a-122">下列章節會定義 **超連結** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="0257a-123">消費者介面自動化需求適用于所有超連結控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="0257a-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0257a-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0257a-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0257a-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0257a-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0257a-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0257a-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0257a-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0257a-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0257a-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0257a-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0257a-129">備註</span><span class="sxs-lookup"><span data-stu-id="0257a-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="0257a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0257a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0257a-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0257a-131">Typical Tree Structure</span></span>

<span data-ttu-id="0257a-132">下表描述超連結控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="0257a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0257a-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="0257a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0257a-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="0257a-134">Control View</span></span></th>
<th><span data-ttu-id="0257a-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="0257a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0257a-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="0257a-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0257a-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="0257a-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0257a-138">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0257a-138">Relevant Properties</span></span>

<span data-ttu-id="0257a-139">下表列出消費者介面自動化屬性，其值或定義與超連結控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="0257a-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="0257a-140">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="0257a-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0257a-141">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="0257a-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0257a-142">值</span><span class="sxs-lookup"><span data-stu-id="0257a-142">Value</span></span>         | <span data-ttu-id="0257a-143">注意</span><span class="sxs-lookup"><span data-stu-id="0257a-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0257a-144">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0257a-145">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-145">See notes.</span></span>    | <span data-ttu-id="0257a-146">這個屬性的值在應用程式中的所有控制項之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0257a-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="0257a-147">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0257a-148">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-148">See notes.</span></span>    | <span data-ttu-id="0257a-149">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="0257a-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="0257a-150">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0257a-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-151">See notes.</span></span>    | <span data-ttu-id="0257a-152">如果按一下滑鼠指標，超連結控制項的可按點必須是啟動超連結的點。</span><span class="sxs-lookup"><span data-stu-id="0257a-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="0257a-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0257a-154">**超連結**</span><span class="sxs-lookup"><span data-stu-id="0257a-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="0257a-155">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0257a-156">true</span><span class="sxs-lookup"><span data-stu-id="0257a-156">TRUE</span></span>          | <span data-ttu-id="0257a-157">此超連結控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="0257a-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="0257a-158">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0257a-159">true</span><span class="sxs-lookup"><span data-stu-id="0257a-159">TRUE</span></span>          | <span data-ttu-id="0257a-160">此超連結控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="0257a-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="0257a-161">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0257a-162">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-162">See notes.</span></span>    | <span data-ttu-id="0257a-163">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="0257a-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="0257a-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0257a-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-165">See notes.</span></span>    | <span data-ttu-id="0257a-166">如果有靜態文字標籤，這個屬性必須公開該控制項的參考。</span><span class="sxs-lookup"><span data-stu-id="0257a-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="0257a-167">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0257a-168">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-168">See notes.</span></span>    | <span data-ttu-id="0257a-169">對應至 **超連結** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="0257a-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="0257a-170">預設值為 en-us 或英文 (美國) 的 [超連結]。</span><span class="sxs-lookup"><span data-stu-id="0257a-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="0257a-171">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0257a-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0257a-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0257a-172">See notes.</span></span>    | <span data-ttu-id="0257a-173">超連結控制項的名稱是顯示在畫面上以加上底線的文字。</span><span class="sxs-lookup"><span data-stu-id="0257a-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0257a-174">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0257a-174">Required Control Patterns</span></span>

<span data-ttu-id="0257a-175">下表列出超連結控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0257a-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="0257a-176">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="0257a-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="0257a-177">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="0257a-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="0257a-178">支援/值</span><span class="sxs-lookup"><span data-stu-id="0257a-178">Support/Value</span></span>                | <span data-ttu-id="0257a-179">備註</span><span class="sxs-lookup"><span data-stu-id="0257a-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0257a-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="0257a-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="0257a-181">必要</span><span class="sxs-lookup"><span data-stu-id="0257a-181">Required</span></span>                     | <span data-ttu-id="0257a-182">所有超連結控制項都必須支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0257a-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="0257a-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="0257a-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="0257a-184">相依</span><span class="sxs-lookup"><span data-stu-id="0257a-184">Depends</span></span>                      | <span data-ttu-id="0257a-185">當連結包含可供使用者使用且有意義的資訊時，超連結控制項應支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0257a-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="0257a-186">**值**</span><span class="sxs-lookup"><span data-stu-id="0257a-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="0257a-187">例如，"https://www..."</span><span class="sxs-lookup"><span data-stu-id="0257a-187">For example, "https://www..."</span></span> | <span data-ttu-id="0257a-188">網際網路或內部網路位址的 URL 是超連結的範例，其中包含對使用者有意義的資訊。</span><span class="sxs-lookup"><span data-stu-id="0257a-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="0257a-189">不過，程式設計連結只對應用程式有意義，因此不建議用於 **Value** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0257a-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="0257a-190">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0257a-190">Required Events</span></span>

<span data-ttu-id="0257a-191">下表列出超連結控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="0257a-192">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="0257a-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0257a-193">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="0257a-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="0257a-194">備註</span><span class="sxs-lookup"><span data-stu-id="0257a-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0257a-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0257a-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="0257a-196">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="0257a-197">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="0257a-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="0257a-198">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="0257a-199">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0257a-200">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0257a-201">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0257a-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0257a-202">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0257a-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="0257a-203">備註</span><span class="sxs-lookup"><span data-stu-id="0257a-203">Remarks</span></span>

<span data-ttu-id="0257a-204">Hyperlink 控制項類型應該只套用至物件，當按下時，就會導致導覽。它不應該套用至超連結的容器。</span><span class="sxs-lookup"><span data-stu-id="0257a-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="0257a-205">例如，只有影像地圖內可按的「作用點」才會有 **超連結** 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="0257a-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="0257a-206">文字欄位或檔容器中的超連結也是如此。</span><span class="sxs-lookup"><span data-stu-id="0257a-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="0257a-207">在此情況下，只有超連結文字或影像應該有 **超連結** 控制項類型，而不是容器。</span><span class="sxs-lookup"><span data-stu-id="0257a-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="0257a-208">[文字](uiauto-implementingtextandtextrange.md)控制項模式非常適合用來支援文字或檔元素中的內嵌超連結。</span><span class="sxs-lookup"><span data-stu-id="0257a-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0257a-209">相關主題</span><span class="sxs-lookup"><span data-stu-id="0257a-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0257a-210">**概念**</span><span class="sxs-lookup"><span data-stu-id="0257a-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0257a-211">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="0257a-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0257a-212">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="0257a-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




