---
title: 檔控制項類型
description: 本主題提供檔控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- 消費者介面自動化，檔控制項類型的支援
- 消費者介面自動化，檔控制項類型
- 消費者介面自動化，Document 控制項類型的樹狀結構
- 消費者介面自動化，Document 控制項類型的屬性
- 消費者介面自動化，檔控制項類型的控制項模式
- 消費者介面自動化，Document 控制項類型的事件
- 樹狀結構，檔控制項類型
- 屬性，檔控制項類型
- 控制項模式，檔控制項類型
- 事件，檔控制項類型
- Document 控制項類型的支援
- Document 控制項類型
- 控制項類型，檔控制項類型的樹狀結構
- 控制項類型，檔控制項類型的控制項模式
- 控制項類型，支援檔
- 控制項類型，檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021342"
---
# <a name="document-control-type"></a><span data-ttu-id="aea37-119">檔控制項類型</span><span class="sxs-lookup"><span data-stu-id="aea37-119">Document Control Type</span></span>

<span data-ttu-id="aea37-120">本主題提供 **檔** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aea37-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="aea37-121">控制項可讓使用者檢視和操作多個頁面的文字。</span><span class="sxs-lookup"><span data-stu-id="aea37-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="aea37-122">不同于僅支援簡單的未格式化文字的編輯控制項，document 控制項可以裝載豐富樣式和格式化的文字。</span><span class="sxs-lookup"><span data-stu-id="aea37-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="aea37-123">下列章節會定義 **檔** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="aea37-124">消費者介面自動化需求適用于所有檔控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="aea37-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="aea37-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="aea37-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aea37-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="aea37-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="aea37-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="aea37-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="aea37-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="aea37-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="aea37-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="aea37-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="aea37-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="aea37-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="aea37-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="aea37-131">Typical Tree Structure</span></span>

<span data-ttu-id="aea37-132">下表描述的是與檔控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="aea37-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="aea37-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="aea37-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aea37-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="aea37-134">Control View</span></span></th>
<th><span data-ttu-id="aea37-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="aea37-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="aea37-136">文件</span><span class="sxs-lookup"><span data-stu-id="aea37-136">Document</span></span>
<ul>
<li><span data-ttu-id="aea37-137">不定</span><span class="sxs-lookup"><span data-stu-id="aea37-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="aea37-138">文件</span><span class="sxs-lookup"><span data-stu-id="aea37-138">Document</span></span>
<ul>
<li><span data-ttu-id="aea37-139">不定</span><span class="sxs-lookup"><span data-stu-id="aea37-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="aea37-140">相關屬性</span><span class="sxs-lookup"><span data-stu-id="aea37-140">Relevant Properties</span></span>

<span data-ttu-id="aea37-141">下表列出消費者介面自動化屬性，其值或定義與檔控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="aea37-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="aea37-142">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="aea37-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="aea37-143">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="aea37-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="aea37-144">值</span><span class="sxs-lookup"><span data-stu-id="aea37-144">Value</span></span>        | <span data-ttu-id="aea37-145">注意</span><span class="sxs-lookup"><span data-stu-id="aea37-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aea37-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="aea37-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-147">See notes.</span></span>   | <span data-ttu-id="aea37-148">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="aea37-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="aea37-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="aea37-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-150">See notes.</span></span>   | <span data-ttu-id="aea37-151">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="aea37-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="aea37-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="aea37-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-153">See notes.</span></span>   | <span data-ttu-id="aea37-154">文件具有可按的點，它會使文件容器中其中一個項目的文件具有焦點。</span><span class="sxs-lookup"><span data-stu-id="aea37-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="aea37-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="aea37-156">**文件**</span><span class="sxs-lookup"><span data-stu-id="aea37-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="aea37-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aea37-158">true</span><span class="sxs-lookup"><span data-stu-id="aea37-158">TRUE</span></span>         | <span data-ttu-id="aea37-159">檔控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="aea37-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="aea37-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aea37-161">true</span><span class="sxs-lookup"><span data-stu-id="aea37-161">TRUE</span></span>         | <span data-ttu-id="aea37-162">檔控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="aea37-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="aea37-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="aea37-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-164">See notes.</span></span>   | <span data-ttu-id="aea37-165">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="aea37-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="aea37-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="aea37-167">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-167">See notes.</span></span>   | <span data-ttu-id="aea37-168">這個屬性的值應該是文件控制項的標籤。</span><span class="sxs-lookup"><span data-stu-id="aea37-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="aea37-169">通常會使用文件的標題。</span><span class="sxs-lookup"><span data-stu-id="aea37-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="aea37-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="aea37-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-171">See notes.</span></span>   | <span data-ttu-id="aea37-172">對應至 **檔** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="aea37-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="aea37-173">預設值為 en-us 或英文 (美國) 的「檔」。</span><span class="sxs-lookup"><span data-stu-id="aea37-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="aea37-174">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aea37-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="aea37-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="aea37-175">See notes.</span></span>   | <span data-ttu-id="aea37-176">Document 控制項通常會從載入它的檔案名中取得其名稱。</span><span class="sxs-lookup"><span data-stu-id="aea37-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="aea37-177">這通常會顯示在包含視窗或框架標題。</span><span class="sxs-lookup"><span data-stu-id="aea37-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="aea37-178">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="aea37-178">Required Control Patterns</span></span>

<span data-ttu-id="aea37-179">下表列出檔控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="aea37-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="aea37-180">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="aea37-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="aea37-181">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="aea37-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="aea37-182">支援/值</span><span class="sxs-lookup"><span data-stu-id="aea37-182">Support/Value</span></span> | <span data-ttu-id="aea37-183">備註</span><span class="sxs-lookup"><span data-stu-id="aea37-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aea37-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="aea37-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="aea37-185">相依</span><span class="sxs-lookup"><span data-stu-id="aea37-185">Depends</span></span>       | <span data-ttu-id="aea37-186">文件控制項的跨越範圍可能大於檢視區的跨越範圍。</span><span class="sxs-lookup"><span data-stu-id="aea37-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="aea37-187">如果內容為可滾動的，則控制項應支援 [滾動](uiauto-implementingscroll.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="aea37-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="aea37-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="aea37-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="aea37-189">必要</span><span class="sxs-lookup"><span data-stu-id="aea37-189">Required</span></span>      | <span data-ttu-id="aea37-190">所有檔控制項都必須支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="aea37-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="aea37-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="aea37-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="aea37-192">相依</span><span class="sxs-lookup"><span data-stu-id="aea37-192">Depends</span></span>       | <span data-ttu-id="aea37-193">雖然消費者介面自動化用戶端可以使用 [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) 取得檔的文字資訊，但是它們需要 [值](uiauto-implementingvalue.md) 控制項模式來設定內部值。</span><span class="sxs-lookup"><span data-stu-id="aea37-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="aea37-194">只有透過值控制項模式才能使用簡單的文字專案。</span><span class="sxs-lookup"><span data-stu-id="aea37-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="aea37-195">必要的事件</span><span class="sxs-lookup"><span data-stu-id="aea37-195">Required Events</span></span>

<span data-ttu-id="aea37-196">下表列出檔控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="aea37-197">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="aea37-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="aea37-198">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="aea37-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="aea37-199">備註</span><span class="sxs-lookup"><span data-stu-id="aea37-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aea37-200">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aea37-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="aea37-201">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="aea37-202">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="aea37-203">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="aea37-204">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="aea37-205">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="aea37-206">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aea37-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="aea37-207">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="aea37-208">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="aea37-209">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="aea37-210">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="aea37-211">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="aea37-212">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="aea37-213">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="aea37-214">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="aea37-215">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="aea37-216">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="aea37-217">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="aea37-218">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="aea37-219">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="aea37-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="aea37-220">如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="aea37-221">**UIA \_ 文字 \_ TextSelectionChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aea37-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="aea37-222">**UIA \_ 文字 \_ TextChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aea37-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="aea37-223">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="aea37-224">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="aea37-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="aea37-225">相關主題</span><span class="sxs-lookup"><span data-stu-id="aea37-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aea37-226">**概念**</span><span class="sxs-lookup"><span data-stu-id="aea37-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aea37-227">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="aea37-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="aea37-228">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="aea37-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




