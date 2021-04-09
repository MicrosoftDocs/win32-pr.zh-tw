---
title: 標題列控制項類型
description: 本主題提供標題列控制項類型的 Microsoft 消費者介面自動化支援相關資訊。 標題列控制項代表視窗中的標題或標題列。
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- 消費者介面自動化，標題控制項類型的支援
- 消費者介面自動化，標題列控制項類型
- 消費者介面自動化，標題列控制項類型的樹狀結構
- 消費者介面自動化，標題列控制項類型的屬性
- 消費者介面自動化，標題列控制項類型的控制項模式
- 消費者介面自動化，標題列控制項類型的事件
- 樹狀結構，標題控制項類型
- 屬性、標題列控制項類型
- 控制項模式、標題列控制項類型
- 事件、標題列控制項類型
- 標題列控制項類型的支援
- 標題列控制項類型
- 控制項類型，標題列控制項類型的樹狀結構
- 控制項類型，標題列控制項類型的控制項模式
- 控制項類型，支援標題列
- 控制項類型，標題列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932542"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="0ac5d-120">標題列控制項類型</span><span class="sxs-lookup"><span data-stu-id="0ac5d-120">TitleBar Control Type</span></span>

<span data-ttu-id="0ac5d-121">本主題提供 **標題列** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="0ac5d-122">標題列控制項代表視窗中的標題或標題列。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="0ac5d-123">下列章節會定義 **標題列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="0ac5d-124">消費者介面自動化需求適用于所有的標題列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="0ac5d-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0ac5d-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0ac5d-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="0ac5d-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0ac5d-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="0ac5d-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0ac5d-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="0ac5d-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0ac5d-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="0ac5d-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ac5d-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="0ac5d-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="0ac5d-131">Typical Tree Structure</span></span>

<span data-ttu-id="0ac5d-132">下表描述標題列控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="0ac5d-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0ac5d-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="0ac5d-134">Control View</span></span></th>
<th><span data-ttu-id="0ac5d-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="0ac5d-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="0ac5d-136">標題列</span><span class="sxs-lookup"><span data-stu-id="0ac5d-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="0ac5d-137">功能表 (0 或 1 個)</span><span class="sxs-lookup"><span data-stu-id="0ac5d-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="0ac5d-138">按鈕 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="0ac5d-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="0ac5d-139"> (不適用;標題列控制項沒有內容) </span><span class="sxs-lookup"><span data-stu-id="0ac5d-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="0ac5d-140">相關屬性</span><span class="sxs-lookup"><span data-stu-id="0ac5d-140">Relevant Properties</span></span>

<span data-ttu-id="0ac5d-141">下表列出消費者介面自動化屬性，其值或定義與 **標題列** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="0ac5d-142">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="0ac5d-143">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="0ac5d-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="0ac5d-144">值</span><span class="sxs-lookup"><span data-stu-id="0ac5d-144">Value</span></span>        | <span data-ttu-id="0ac5d-145">注意</span><span class="sxs-lookup"><span data-stu-id="0ac5d-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ac5d-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="0ac5d-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-147">See notes.</span></span>   | <span data-ttu-id="0ac5d-148">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="0ac5d-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="0ac5d-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-150">See notes.</span></span>   | <span data-ttu-id="0ac5d-151">這個屬性所公開的值必須包含所有內含的控制項。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="0ac5d-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="0ac5d-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-153">See notes.</span></span>   | <span data-ttu-id="0ac5d-154">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="0ac5d-155">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="0ac5d-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0ac5d-157">**標題列**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-157">**TitleBar**</span></span> | <span data-ttu-id="0ac5d-158">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0ac5d-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0ac5d-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ac5d-160">FALSE</span></span>        | <span data-ttu-id="0ac5d-161">標題列控制項絕不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="0ac5d-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="0ac5d-163">true</span><span class="sxs-lookup"><span data-stu-id="0ac5d-163">TRUE</span></span>         | <span data-ttu-id="0ac5d-164">標題列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="0ac5d-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="0ac5d-166">FALSE</span><span class="sxs-lookup"><span data-stu-id="0ac5d-166">FALSE</span></span>        | <span data-ttu-id="0ac5d-167">標題列控制項永遠不會有鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="0ac5d-168">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="0ac5d-169">相依</span><span class="sxs-lookup"><span data-stu-id="0ac5d-169">Depends</span></span>      | <span data-ttu-id="0ac5d-170">標題列控制項會根據畫面上是否可見來傳回值。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="0ac5d-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="0ac5d-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-172">See notes.</span></span>   | <span data-ttu-id="0ac5d-173">標題列控制項通常沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="0ac5d-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="0ac5d-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-175">See notes.</span></span>   | <span data-ttu-id="0ac5d-176">對應到標題列控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="0ac5d-177">預設值為 en-us 或英文 (美國) 的「標題列」。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="0ac5d-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="0ac5d-179">""</span><span class="sxs-lookup"><span data-stu-id="0ac5d-179">""</span></span>           | <span data-ttu-id="0ac5d-180">標題列不是內容;其文字資訊會以父視窗的名稱來公開。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="0ac5d-181">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="0ac5d-181">Required Control Patterns</span></span>

<span data-ttu-id="0ac5d-182">**標題列** 控制項類型不需要支援任何控制項模式。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="0ac5d-183">它的功能是透過[window 控制項類型](uiauto-supportwindowcontroltype.md)上的[window](uiauto-implementingwindow.md)控制項模式來公開。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="0ac5d-184">必要的事件</span><span class="sxs-lookup"><span data-stu-id="0ac5d-184">Required Events</span></span>

<span data-ttu-id="0ac5d-185">下表列出支援的標題列控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="0ac5d-186">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="0ac5d-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="0ac5d-187">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="0ac5d-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="0ac5d-188">備註</span><span class="sxs-lookup"><span data-stu-id="0ac5d-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ac5d-189">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="0ac5d-190">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="0ac5d-191">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="0ac5d-192">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="0ac5d-193">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="0ac5d-194">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="0ac5d-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="0ac5d-195">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="0ac5d-196">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ac5d-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="0ac5d-197">**概念**</span><span class="sxs-lookup"><span data-stu-id="0ac5d-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0ac5d-198">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="0ac5d-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="0ac5d-199">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="0ac5d-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




