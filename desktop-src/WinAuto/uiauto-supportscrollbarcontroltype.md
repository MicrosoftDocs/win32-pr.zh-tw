---
title: 捲軸控制項類型
description: 本主題提供捲軸控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- 消費者介面自動化、捲軸控制項類型的支援
- 消費者介面自動化、捲軸控制項類型
- 消費者介面自動化、捲軸控制項類型的樹狀結構
- 消費者介面自動化、捲軸控制項類型的屬性
- 消費者介面自動化、捲軸控制項類型的控制項模式
- 消費者介面自動化、捲軸控制項類型的事件
- 樹狀結構、捲軸控制項類型
- 屬性、捲軸控制項類型
- 控制項模式、捲軸控制項類型
- 事件、捲軸控制項類型
- 捲軸控制項類型的支援
- 捲軸控制項類型
- 控制項類型、捲軸控制項類型的樹狀結構
- 控制項類型、捲軸控制項類型的控制項模式
- 控制項類型、捲軸支援
- 控制項類型、捲軸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2168401c313dd9139f44ba615de945802b307d64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106991289"
---
# <a name="scrollbar-control-type"></a><span data-ttu-id="84f0a-119">捲軸控制項類型</span><span class="sxs-lookup"><span data-stu-id="84f0a-119">ScrollBar Control Type</span></span>

<span data-ttu-id="84f0a-120">本主題提供 **捲軸** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="84f0a-120">This topic provides information about Microsoft UI Automation support for the **ScrollBar** control type.</span></span>

<span data-ttu-id="84f0a-121">捲軸控制項可讓使用者捲動視窗或項目容器內的內容。</span><span class="sxs-lookup"><span data-stu-id="84f0a-121">Scroll bar controls enable a user to scroll content within a window or item container.</span></span> <span data-ttu-id="84f0a-122">此控制項是由一組按鈕和 thumb 控制項所組成。</span><span class="sxs-lookup"><span data-stu-id="84f0a-122">The control consists of a set of buttons and a thumb control.</span></span>

<span data-ttu-id="84f0a-123">下列章節會定義 **捲軸** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ScrollBar** control type.</span></span> <span data-ttu-id="84f0a-124">消費者介面自動化需求適用于所有捲軸控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="84f0a-124">The UI Automation requirements apply to all scroll bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="84f0a-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="84f0a-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="84f0a-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="84f0a-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="84f0a-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="84f0a-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="84f0a-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="84f0a-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="84f0a-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="84f0a-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="84f0a-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="84f0a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="84f0a-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="84f0a-131">Typical Tree Structure</span></span>

<span data-ttu-id="84f0a-132">下表描述捲軸控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="84f0a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to scroll bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="84f0a-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="84f0a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84f0a-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="84f0a-134">Control View</span></span></th>
<th><span data-ttu-id="84f0a-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="84f0a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="84f0a-136">ScrollBar</span><span class="sxs-lookup"><span data-stu-id="84f0a-136">ScrollBar</span></span>
<ul>
<li><span data-ttu-id="84f0a-137">按鈕 (0、2或 4) </span><span class="sxs-lookup"><span data-stu-id="84f0a-137">Button (0, 2, or 4)</span></span></li>
<li><span data-ttu-id="84f0a-138">Thumb (0 或 1) </span><span class="sxs-lookup"><span data-stu-id="84f0a-138">Thumb (0 or 1)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="84f0a-139">不適用。</span><span class="sxs-lookup"><span data-stu-id="84f0a-139">Not applicable.</span></span> <span data-ttu-id="84f0a-140"> (捲軸控制項沒有內容。 ) </span><span class="sxs-lookup"><span data-stu-id="84f0a-140">(The scroll bar control has no content.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="84f0a-141">捲軸控制項可以有零到五個子系。</span><span class="sxs-lookup"><span data-stu-id="84f0a-141">The scroll bar control can have zero to five children.</span></span> <span data-ttu-id="84f0a-142">因為子樹有一個以上的按鈕控制項，所以元素必須將特定的 [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md) 值設定為每個專案，才能讓自動化測試控管可以找到它們。</span><span class="sxs-lookup"><span data-stu-id="84f0a-142">Because the subtree has more than one button control, the element must set a specific [**UIA\_AutomationIdPropertyId**](uiauto-automation-element-propids.md) value to each item to make them discoverable for automated testing tools.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="84f0a-143">相關屬性</span><span class="sxs-lookup"><span data-stu-id="84f0a-143">Relevant Properties</span></span>

<span data-ttu-id="84f0a-144">下表列出消費者介面自動化屬性，其值或定義與捲軸控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="84f0a-144">The following table lists the UI Automation properties whose value or definition is especially relevant to scroll bar controls.</span></span> <span data-ttu-id="84f0a-145">請注意，捲軸控制項永遠沒有內容;它的功能是透過 [滾動](uiauto-implementingscroll.md) 條控制項模式來公開的，此模式在滾動的容器上受到支援。</span><span class="sxs-lookup"><span data-stu-id="84f0a-145">Note that a scroll bar control never has content; its functionality is exposed through the [Scroll](uiauto-implementingscroll.md) control pattern, which is supported on the container being scrolled.</span></span>

<span data-ttu-id="84f0a-146">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="84f0a-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="84f0a-147">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="84f0a-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="84f0a-148">值</span><span class="sxs-lookup"><span data-stu-id="84f0a-148">Value</span></span>         | <span data-ttu-id="84f0a-149">注意</span><span class="sxs-lookup"><span data-stu-id="84f0a-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84f0a-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="84f0a-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="84f0a-151">See notes.</span></span>    | <span data-ttu-id="84f0a-152">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="84f0a-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="84f0a-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="84f0a-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="84f0a-154">See notes.</span></span>    | <span data-ttu-id="84f0a-155">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="84f0a-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="84f0a-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="84f0a-157">NaN</span><span class="sxs-lookup"><span data-stu-id="84f0a-157">NaN</span></span>           | <span data-ttu-id="84f0a-158">捲軸控制項沒有可點選的點。</span><span class="sxs-lookup"><span data-stu-id="84f0a-158">The scroll bar control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="84f0a-159">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="84f0a-160">**ScrollBar**</span><span class="sxs-lookup"><span data-stu-id="84f0a-160">**ScrollBar**</span></span> | <span data-ttu-id="84f0a-161">此值與所有架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="84f0a-161">This value is the same for all frameworks.</span></span> <span data-ttu-id="84f0a-162">作為滑杆運作的捲軸必須使用 [滑杆](uiauto-supportslidercontroltype.md) 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="84f0a-162">Scroll bars that function as sliders must use the [Slider](uiauto-supportslidercontroltype.md) control type.</span></span>                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="84f0a-163">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-163">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84f0a-164">FALSE</span><span class="sxs-lookup"><span data-stu-id="84f0a-164">FALSE</span></span>         | <span data-ttu-id="84f0a-165">捲軸控制項不是內容項目。</span><span class="sxs-lookup"><span data-stu-id="84f0a-165">The scroll bar control is never a content element.</span></span> <span data-ttu-id="84f0a-166">如果捲軸是獨立控制項，則必須滿足 [滑杆](uiauto-supportslidercontroltype.md)控制項類型，並傳回 [**IUIAutomationElement：： CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (或 [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) 屬性的 [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) 。</span><span class="sxs-lookup"><span data-stu-id="84f0a-166">If the scroll bar is a standalone control, it must fulfill the [Slider](uiauto-supportslidercontroltype.md) control type and return [**UIA\_SliderControlTypeId**](uiauto-controltype-ids.md) for the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property.</span></span> |
| [<span data-ttu-id="84f0a-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84f0a-168">true</span><span class="sxs-lookup"><span data-stu-id="84f0a-168">TRUE</span></span>          | <span data-ttu-id="84f0a-169">捲軸控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="84f0a-169">The scroll bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="84f0a-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="84f0a-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="84f0a-171">See notes.</span></span>    | <span data-ttu-id="84f0a-172">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="84f0a-172">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="84f0a-173">捲軸控制項很少會取得焦點，但在此情況下，焦點應該留在捲軸控制項本身，而不是子按鈕或 thumb。</span><span class="sxs-lookup"><span data-stu-id="84f0a-173">A scroll bar control rarely takes the focus, but when it does, the focus should remain on the scroll bar control itself, not on the child buttons or the thumb.</span></span> <span data-ttu-id="84f0a-174">使用者應該能夠使用向上箭號和向下箭號， (或向右箭號和向下箭號) 按鍵，或 PAGE UP 和 PAGE DOWN 鍵來執行所有滾動動作。</span><span class="sxs-lookup"><span data-stu-id="84f0a-174">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW (or RIGHT ARROW and LEFT ARROW) keys, or the PAGE UP and PAGE DOWN keys.</span></span>                                                                |
| [<span data-ttu-id="84f0a-175">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-175">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="84f0a-176">NULL</span><span class="sxs-lookup"><span data-stu-id="84f0a-176">NULL</span></span>          | <span data-ttu-id="84f0a-177">捲軸沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="84f0a-177">Scroll bars do not have labels.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="84f0a-178">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-178">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="84f0a-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="84f0a-179">See notes.</span></span>    | <span data-ttu-id="84f0a-180">對應到 **捲軸** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="84f0a-180">Localized string corresponding to the **ScrollBar** control type.</span></span> <span data-ttu-id="84f0a-181">預設值為 en-us 或英文 (美國) 的「捲軸」。</span><span class="sxs-lookup"><span data-stu-id="84f0a-181">The default value is "scroll bar" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="84f0a-182">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-182">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="84f0a-183">NULL</span><span class="sxs-lookup"><span data-stu-id="84f0a-183">NULL</span></span>          | <span data-ttu-id="84f0a-184">捲軸控制項沒有 content 元素，而且不需要設定 [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="84f0a-184">The scroll bar control does not have content elements and the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property is not required to be set.</span></span>                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="84f0a-185">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-185">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="84f0a-186">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="84f0a-186">See notes.</span></span>    | <span data-ttu-id="84f0a-187">捲軸控制項必須一律公開其水平或垂直的方向。</span><span class="sxs-lookup"><span data-stu-id="84f0a-187">The scroll bar control must always expose its horizontal or vertical orientation.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="84f0a-188">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="84f0a-188">Required Control Patterns</span></span>

<span data-ttu-id="84f0a-189">下表列出所有捲軸控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="84f0a-189">The following table lists the UI Automation control patterns required to be supported by all scroll bar controls.</span></span> <span data-ttu-id="84f0a-190">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="84f0a-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

> [!Note]  
> <span data-ttu-id="84f0a-191">使用捲軸作為僅限滑鼠操作的控制項時，不支援控制項模式。</span><span class="sxs-lookup"><span data-stu-id="84f0a-191">When a scroll bar is used as a control for mouse manipulation only, it does not support control patterns.</span></span> <span data-ttu-id="84f0a-192">如果用來作為應用程式內的滑杆控制項，則必須提供 [滑杆](uiauto-supportslidercontroltype.md) 控制項類型給它。</span><span class="sxs-lookup"><span data-stu-id="84f0a-192">If it is used as a slider control within an application, it must be given the [Slider](uiauto-supportslidercontroltype.md) control type.</span></span>

 



| <span data-ttu-id="84f0a-193">控制項模式</span><span class="sxs-lookup"><span data-stu-id="84f0a-193">Control Pattern</span></span>                                           | <span data-ttu-id="84f0a-194">支援</span><span class="sxs-lookup"><span data-stu-id="84f0a-194">Support</span></span> | <span data-ttu-id="84f0a-195">注意</span><span class="sxs-lookup"><span data-stu-id="84f0a-195">Notes</span></span>                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84f0a-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="84f0a-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="84f0a-197">相依</span><span class="sxs-lookup"><span data-stu-id="84f0a-197">Depends</span></span> | <span data-ttu-id="84f0a-198">只有在具有捲軸的容器不支援[滾動](uiauto-implementingscroll.md)條控制項模式時，才需要支援[RangeValue](uiauto-implementingrangevalue.md)控制項模式。</span><span class="sxs-lookup"><span data-stu-id="84f0a-198">The [RangeValue](uiauto-implementingrangevalue.md) control pattern is required to be supported only if the [Scroll](uiauto-implementingscroll.md) control pattern is not supported on the container that has the scroll bar.</span></span> |
| [<span data-ttu-id="84f0a-199">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="84f0a-199">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | <span data-ttu-id="84f0a-200">永不</span><span class="sxs-lookup"><span data-stu-id="84f0a-200">Never</span></span>   | <span data-ttu-id="84f0a-201">捲軸不直接支援 [滾動](uiauto-implementingscroll.md) 條控制項模式。</span><span class="sxs-lookup"><span data-stu-id="84f0a-201">The [Scroll](uiauto-implementingscroll.md) control pattern is never directly supported on the scroll bar.</span></span>                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="84f0a-202">必要的事件</span><span class="sxs-lookup"><span data-stu-id="84f0a-202">Required Events</span></span>

<span data-ttu-id="84f0a-203">下表列出捲軸控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-203">The following table lists the UI Automation events that scroll bar controls are required to support.</span></span> <span data-ttu-id="84f0a-204">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="84f0a-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="84f0a-205">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="84f0a-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="84f0a-206">備註</span><span class="sxs-lookup"><span data-stu-id="84f0a-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84f0a-207">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-207">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="84f0a-208">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-208">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="84f0a-209">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-209">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="84f0a-210">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-210">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="84f0a-211">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-211">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="84f0a-212">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-212">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="84f0a-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="84f0a-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="84f0a-214">[**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-214">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="84f0a-215">如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="84f0a-215">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="84f0a-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="84f0a-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="84f0a-217">**概念**</span><span class="sxs-lookup"><span data-stu-id="84f0a-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84f0a-218">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="84f0a-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="84f0a-219">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="84f0a-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




