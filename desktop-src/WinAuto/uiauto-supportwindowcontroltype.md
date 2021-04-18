---
title: Window 控制項類型
description: 本主題提供 Window 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- 消費者介面自動化，Window 控制項類型的支援
- 消費者介面自動化，Window 控制項類型
- 消費者介面自動化，Window 控制項類型的樹狀結構
- 消費者介面自動化，Window 控制項類型的屬性
- 消費者介面自動化，視窗控制項類型的控制項模式
- 消費者介面自動化，Window 控制項類型的事件
- 樹狀結構，視窗控制項類型
- 屬性、視窗控制項類型
- 控制項模式，視窗控制項類型
- 事件、視窗控制項類型
- 視窗控制項類型的支援
- Window 控制項類型
- 控制項類型，視窗控制項類型的樹狀結構
- 控制項類型，視窗控制項類型的控制項模式
- 控制項類型、視窗支援
- 控制項類型，視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422742381cd501d295e4cb7e354ca07e10c13360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301655"
---
# <a name="window-control-type"></a><span data-ttu-id="2c140-119">Window 控制項類型</span><span class="sxs-lookup"><span data-stu-id="2c140-119">Window Control Type</span></span>

<span data-ttu-id="2c140-120">本主題提供 **Window** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c140-120">This topic provides information about Microsoft UI Automation support for the **Window** control type.</span></span>

<span data-ttu-id="2c140-121">視窗控制項由視窗框架組成，而視窗框架包含子物件，如標題列、用戶端和其他物件。</span><span class="sxs-lookup"><span data-stu-id="2c140-121">The window control consists of the window frame, which contains child objects such as title bar, client, and other objects.</span></span>

<span data-ttu-id="2c140-122">下列章節會定義 **Window** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Window** control type.</span></span> <span data-ttu-id="2c140-123">消費者介面自動化需求適用于所有的視窗控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="2c140-123">The UI Automation requirements apply to all window controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2c140-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="2c140-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2c140-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="2c140-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2c140-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="2c140-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2c140-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="2c140-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="2c140-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="2c140-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2c140-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c140-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2c140-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="2c140-130">Typical Tree Structure</span></span>

<span data-ttu-id="2c140-131">下表描述與 window 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="2c140-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to window controls and describes what can be contained in each view.</span></span> <span data-ttu-id="2c140-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="2c140-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c140-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="2c140-133">Control View</span></span></th>
<th><span data-ttu-id="2c140-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="2c140-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2c140-135">時間範圍</span><span class="sxs-lookup"><span data-stu-id="2c140-135">Window</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2c140-136">時間範圍</span><span class="sxs-lookup"><span data-stu-id="2c140-136">Window</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="2c140-137">相關屬性</span><span class="sxs-lookup"><span data-stu-id="2c140-137">Relevant Properties</span></span>

<span data-ttu-id="2c140-138">下表列出消費者介面自動化屬性，其值或定義與視窗控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="2c140-138">The following table lists the UI Automation properties whose value or definition is especially relevant to window controls.</span></span> <span data-ttu-id="2c140-139">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="2c140-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="2c140-140">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="2c140-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="2c140-141">值</span><span class="sxs-lookup"><span data-stu-id="2c140-141">Value</span></span>      | <span data-ttu-id="2c140-142">注意</span><span class="sxs-lookup"><span data-stu-id="2c140-142">Notes</span></span>                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c140-143">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="2c140-144">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-144">See notes.</span></span> | <span data-ttu-id="2c140-145">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2c140-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                            |
| [<span data-ttu-id="2c140-146">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="2c140-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-147">See notes.</span></span> | <span data-ttu-id="2c140-148">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="2c140-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                |
| [<span data-ttu-id="2c140-149">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="2c140-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-150">See notes.</span></span> | <span data-ttu-id="2c140-151">視窗控制項必須具有可點按的點，讓視窗變成已選取或未選取狀態。</span><span class="sxs-lookup"><span data-stu-id="2c140-151">The window control must have a clickable point that causes the window to become selected or unselected.</span></span>                                                 |
| [<span data-ttu-id="2c140-152">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-152">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="2c140-153">**Window**</span><span class="sxs-lookup"><span data-stu-id="2c140-153">**Window**</span></span> | <span data-ttu-id="2c140-154">此值與所有使用者介面架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="2c140-154">This value is the same for all UI frameworks.</span></span>                                                                                                           |
| [<span data-ttu-id="2c140-155">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2c140-156">true</span><span class="sxs-lookup"><span data-stu-id="2c140-156">TRUE</span></span>       | <span data-ttu-id="2c140-157">視窗控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="2c140-157">The window control is always included in the content view of the UI Automation tree.</span></span>                                                                    |
| [<span data-ttu-id="2c140-158">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="2c140-159">true</span><span class="sxs-lookup"><span data-stu-id="2c140-159">TRUE</span></span>       | <span data-ttu-id="2c140-160">視窗控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="2c140-160">The window control is always included in the control view of the UI Automation tree.</span></span>                                                                    |
| [<span data-ttu-id="2c140-161">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="2c140-162">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-162">See notes.</span></span> | <span data-ttu-id="2c140-163">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="2c140-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                               |
| [<span data-ttu-id="2c140-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="2c140-165">NULL</span><span class="sxs-lookup"><span data-stu-id="2c140-165">NULL</span></span>       | <span data-ttu-id="2c140-166">視窗控制項沒有靜態視窗標籤。</span><span class="sxs-lookup"><span data-stu-id="2c140-166">Window controls do not have a static window label.</span></span>                                                                                                      |
| [<span data-ttu-id="2c140-167">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="2c140-168">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-168">See notes.</span></span> | <span data-ttu-id="2c140-169">對應至 **視窗** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="2c140-169">Localized string corresponding to the **Window** control type.</span></span> <span data-ttu-id="2c140-170">預設值為 "window"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="2c140-170">The default value is "window" for en-US or English (United States).</span></span>                      |
| [<span data-ttu-id="2c140-171">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="2c140-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="2c140-172">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="2c140-172">See notes.</span></span> | <span data-ttu-id="2c140-173">視窗控制項一律會包含主要視窗專案，此專案與使用者要建立為專案最多語義識別碼的關聯性。</span><span class="sxs-lookup"><span data-stu-id="2c140-173">The window control always contains a primary window element that relates to what the user would associate as the most semantic identifier for the item.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="2c140-174">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="2c140-174">Required Control Patterns</span></span>

<span data-ttu-id="2c140-175">下表列出視窗控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2c140-175">The following table lists the UI Automation control patterns required to be supported by window controls.</span></span> <span data-ttu-id="2c140-176">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="2c140-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2c140-177">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="2c140-177">Control Pattern/Pattern Property</span></span>                        | <span data-ttu-id="2c140-178">支援/值</span><span class="sxs-lookup"><span data-stu-id="2c140-178">Support/Value</span></span> | <span data-ttu-id="2c140-179">備註</span><span class="sxs-lookup"><span data-stu-id="2c140-179">Notes</span></span>                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c140-180">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="2c140-180">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="2c140-181">條件式</span><span class="sxs-lookup"><span data-stu-id="2c140-181">Conditional</span></span>   | <span data-ttu-id="2c140-182">如果視窗可以停駐，就必須支援 [Dock](uiauto-implementingdock.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="2c140-182">The [Dock](uiauto-implementingdock.md) control pattern must be supported if the window can be docked.</span></span>                                                                       |
| [<span data-ttu-id="2c140-183">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="2c140-183">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="2c140-184">必要</span><span class="sxs-lookup"><span data-stu-id="2c140-184">Required</span></span>      | <span data-ttu-id="2c140-185">[轉換](uiauto-implementingtransform.md)控制項模式可讓視窗在螢幕上移動、調整大小或旋轉。</span><span class="sxs-lookup"><span data-stu-id="2c140-185">The [Transform](uiauto-implementingtransform.md) control pattern enables the window to be moved, resized, or rotated on the screen.</span></span> <span data-ttu-id="2c140-186"> (不適用於 Windows Store 應用程式。 ) </span><span class="sxs-lookup"><span data-stu-id="2c140-186">(Does not apply to Windows Store apps.)</span></span> |
| [<span data-ttu-id="2c140-187">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="2c140-187">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="2c140-188">必要</span><span class="sxs-lookup"><span data-stu-id="2c140-188">Required</span></span>      | <span data-ttu-id="2c140-189">[視窗](uiauto-implementingwindow.md)控制項模式會啟用視窗的特定作業。</span><span class="sxs-lookup"><span data-stu-id="2c140-189">The [Window](uiauto-implementingwindow.md) control pattern enables specific operations for the window.</span></span>                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="2c140-190">必要的事件</span><span class="sxs-lookup"><span data-stu-id="2c140-190">Required Events</span></span>

<span data-ttu-id="2c140-191">下表列出支援的 **視窗** 控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-191">The following table lists the UI Automation events that **Window** controls are required to support.</span></span> <span data-ttu-id="2c140-192">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="2c140-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2c140-193">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="2c140-193">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="2c140-194">備註</span><span class="sxs-lookup"><span data-stu-id="2c140-194">Notes</span></span>                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c140-195">**UIA \_ AsyncContentLoadedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-195">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [<span data-ttu-id="2c140-196">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-196">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| <span data-ttu-id="2c140-197">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-197">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                                                                                           |
| <span data-ttu-id="2c140-198">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="2c140-199">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                                                                                  |
| <span data-ttu-id="2c140-200">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="2c140-201">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                                                                                |
| [<span data-ttu-id="2c140-202">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-202">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| <span data-ttu-id="2c140-203">[**UIA \_NamePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-203">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                |                                                                                                                                                                                                                           |
| <span data-ttu-id="2c140-204">[**UIA \_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-204">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="2c140-205">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-205">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| <span data-ttu-id="2c140-206">[**UIA \_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-206">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="2c140-207">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-207">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| <span data-ttu-id="2c140-208">[**UIA \_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-208">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="2c140-209">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-209">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| <span data-ttu-id="2c140-210">[**UIA \_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-210">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="2c140-211">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-211">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| <span data-ttu-id="2c140-212">[**UIA \_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-212">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="2c140-213">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-213">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| <span data-ttu-id="2c140-214">[**UIA \_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-214">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="2c140-215">如果控制項支援 [滾動](uiauto-implementingscroll.md) 條控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-215">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                                                                                          |
| [<span data-ttu-id="2c140-216">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-216">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [<span data-ttu-id="2c140-217">**UIA \_ 視窗 \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-217">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [<span data-ttu-id="2c140-218">**UIA \_ 視窗 \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="2c140-218">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| <span data-ttu-id="2c140-219">[**UIA \_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-219">[**UIA\_WindowWindowVisualStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="2c140-220">如果控制項支援 [Window](uiauto-implementingwindow.md)控制項模式的 [**WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate)屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="2c140-220">If the control supports the [**WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) property of the [Window](uiauto-implementingwindow.md) control pattern, this event must be supported.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2c140-221">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c140-221">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2c140-222">**概念**</span><span class="sxs-lookup"><span data-stu-id="2c140-222">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2c140-223">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="2c140-223">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2c140-224">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="2c140-224">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




