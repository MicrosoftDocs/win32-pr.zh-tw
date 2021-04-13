---
title: 狀態列控制項類型
description: 本主題提供關於狀態列控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- 消費者介面自動化，支援狀態列控制項類型
- 消費者介面自動化，狀態列控制項類型
- 消費者介面自動化，狀態列控制項類型的樹狀結構
- 消費者介面自動化，狀態列控制項類型的屬性
- 消費者介面自動化，狀態列控制項類型的控制項模式
- 消費者介面自動化，狀態列控制項類型的事件
- 樹狀結構，狀態列控制項類型
- 屬性、狀態列控制項類型
- 控制項模式、狀態列控制項類型
- 事件、狀態列控制項類型
- 狀態列控制項類型的支援
- StatusBar 控制項類型
- 控制項類型，狀態列控制項類型的樹狀結構
- 控制項類型，狀態列控制項類型的控制項模式
- 控制項類型，支援狀態列
- 控制項類型，狀態列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301431"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="ca9ba-119">狀態列控制項類型</span><span class="sxs-lookup"><span data-stu-id="ca9ba-119">StatusBar Control Type</span></span>

<span data-ttu-id="ca9ba-120">本主題提供關於 **狀態列** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="ca9ba-121">狀態列控制項可以顯示多項資訊：在應用程式的視窗中檢視的物件、物件的元件，或是與物件的作業相關的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="ca9ba-122">下列章節會定義 **狀態列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="ca9ba-123">消費者介面自動化需求適用于所有狀態列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="ca9ba-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ca9ba-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ca9ba-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="ca9ba-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ca9ba-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="ca9ba-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ca9ba-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="ca9ba-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ca9ba-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="ca9ba-129">備註</span><span class="sxs-lookup"><span data-stu-id="ca9ba-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="ca9ba-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca9ba-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="ca9ba-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="ca9ba-131">Typical Tree Structure</span></span>

<span data-ttu-id="ca9ba-132">下表說明與狀態列控制項相關的消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="ca9ba-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca9ba-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="ca9ba-134">Control View</span></span></th>
<th><span data-ttu-id="ca9ba-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="ca9ba-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ca9ba-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="ca9ba-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="ca9ba-137">編輯 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="ca9ba-138">進度列 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="ca9ba-139">影像 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="ca9ba-140">按鈕 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="ca9ba-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="ca9ba-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="ca9ba-142">編輯 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="ca9ba-143">進度列 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="ca9ba-144">影像 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="ca9ba-145">按鈕 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="ca9ba-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="ca9ba-146">相關屬性</span><span class="sxs-lookup"><span data-stu-id="ca9ba-146">Relevant Properties</span></span>

<span data-ttu-id="ca9ba-147">下表列出消費者介面自動化屬性，其值或定義與狀態列控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="ca9ba-148">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="ca9ba-149">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="ca9ba-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="ca9ba-150">值</span><span class="sxs-lookup"><span data-stu-id="ca9ba-150">Value</span></span>         | <span data-ttu-id="ca9ba-151">注意</span><span class="sxs-lookup"><span data-stu-id="ca9ba-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca9ba-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="ca9ba-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-153">See notes.</span></span>    | <span data-ttu-id="ca9ba-154">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="ca9ba-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="ca9ba-156">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-156">See notes.</span></span>    | <span data-ttu-id="ca9ba-157">狀態列的週框必須框住其中所有控制項。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="ca9ba-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="ca9ba-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-159">See notes.</span></span>    | <span data-ttu-id="ca9ba-160">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="ca9ba-161">如果周框內有一些區域無法按下，且專案執行特製化的點擊測試，請覆寫這個專案，並提供可點按的點。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="ca9ba-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca9ba-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="ca9ba-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ca9ba-165">true</span><span class="sxs-lookup"><span data-stu-id="ca9ba-165">TRUE</span></span>          | <span data-ttu-id="ca9ba-166">狀態列控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca9ba-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="ca9ba-168">true</span><span class="sxs-lookup"><span data-stu-id="ca9ba-168">TRUE</span></span>          | <span data-ttu-id="ca9ba-169">狀態列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca9ba-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="ca9ba-171">相依</span><span class="sxs-lookup"><span data-stu-id="ca9ba-171">Depends</span></span>       | <span data-ttu-id="ca9ba-172">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="ca9ba-173">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca9ba-174">相依</span><span class="sxs-lookup"><span data-stu-id="ca9ba-174">Depends</span></span>       | <span data-ttu-id="ca9ba-175">如果目前看不到狀態列控制項，此屬性將會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="ca9ba-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="ca9ba-177">NULL</span><span class="sxs-lookup"><span data-stu-id="ca9ba-177">NULL</span></span>          | <span data-ttu-id="ca9ba-178">狀態列控制項通常沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="ca9ba-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="ca9ba-180">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-180">See notes.</span></span>    | <span data-ttu-id="ca9ba-181">對應到 **狀態列** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="ca9ba-182">預設值為 en-us 或英文 (美國) 的「狀態列」。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="ca9ba-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="ca9ba-184">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-184">See notes.</span></span>    | <span data-ttu-id="ca9ba-185">除非應用程式使用一個以上的狀態列，否則狀態列不需要名稱。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="ca9ba-186">在此情況下，請將每個條碼與名稱（例如「網際網路狀態」或「應用程式狀態」）加以區別。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="ca9ba-187">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="ca9ba-188">相依</span><span class="sxs-lookup"><span data-stu-id="ca9ba-188">Depends</span></span>       | <span data-ttu-id="ca9ba-189">指出控制項方向的值：水準或垂直。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="ca9ba-190">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="ca9ba-190">Required Control Patterns</span></span>

<span data-ttu-id="ca9ba-191">下表列出狀態列控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="ca9ba-192">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="ca9ba-193">控制項模式</span><span class="sxs-lookup"><span data-stu-id="ca9ba-193">Control Pattern</span></span>                               | <span data-ttu-id="ca9ba-194">支援</span><span class="sxs-lookup"><span data-stu-id="ca9ba-194">Support</span></span>  | <span data-ttu-id="ca9ba-195">注意</span><span class="sxs-lookup"><span data-stu-id="ca9ba-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ca9ba-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="ca9ba-197">選擇性</span><span class="sxs-lookup"><span data-stu-id="ca9ba-197">Optional</span></span> | <span data-ttu-id="ca9ba-198">狀態列控制項應支援 [方格](uiauto-implementinggrid.md) 控制項模式，以便監視和輕鬆參考個別的元件以取得資訊。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="ca9ba-199">必要的事件</span><span class="sxs-lookup"><span data-stu-id="ca9ba-199">Required Events</span></span>

<span data-ttu-id="ca9ba-200">下表列出支援的狀態列控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="ca9ba-201">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="ca9ba-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="ca9ba-202">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="ca9ba-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="ca9ba-203">備註</span><span class="sxs-lookup"><span data-stu-id="ca9ba-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ca9ba-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="ca9ba-205">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="ca9ba-206">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="ca9ba-207">如果控制項支援 **IsEnabled** 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="ca9ba-208">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="ca9ba-209">如果控制項支援 **IsOffscreen** 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="ca9ba-210">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="ca9ba-211">備註</span><span class="sxs-lookup"><span data-stu-id="ca9ba-211">Remarks</span></span>

<span data-ttu-id="ca9ba-212">建議您在狀態列中使用編輯控制項做為子格線元素。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="ca9ba-213">使用編輯控制項可讓您使用 [專案名稱] 和 [值] 屬性，更輕鬆地將 status 欄位的用途與其值產生關聯。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="ca9ba-214">因為文字控制項不應支援 **值** 控制項模式，所以不應該當做子格線元素使用。</span><span class="sxs-lookup"><span data-stu-id="ca9ba-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca9ba-215">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca9ba-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ca9ba-216">**概念**</span><span class="sxs-lookup"><span data-stu-id="ca9ba-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ca9ba-217">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="ca9ba-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="ca9ba-218">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="ca9ba-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




