---
title: 滑杆控制項類型
description: 本主題提供滑杆控制項類型的 Microsoft 消費者介面自動化支援相關資訊。
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- 消費者介面自動化，滑杆控制項類型的支援
- 消費者介面自動化，滑杆控制項類型
- 消費者介面自動化，滑杆控制項類型的樹狀結構
- 消費者介面自動化，滑杆控制項類型的屬性
- 消費者介面自動化，滑杆控制項類型的控制項模式
- 消費者介面自動化，滑杆控制項類型的事件
- 樹狀結構，滑杆控制項類型
- 屬性、滑杆控制項類型
- 控制項模式、滑杆控制項類型
- events、Slider 控制項類型
- 滑杆控制項類型的支援
- Slider 控制項類型
- 滑杆控制項類型的控制項類型、樹狀結構
- 控制項類型、滑杆控制項類型的控制項模式
- 控制項類型，支援滑杆
- 控制項類型，滑杆
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932343"
---
# <a name="slider-control-type"></a><span data-ttu-id="d12c9-119">滑杆控制項類型</span><span class="sxs-lookup"><span data-stu-id="d12c9-119">Slider Control Type</span></span>

<span data-ttu-id="d12c9-120">本主題提供 **滑杆** 控制項類型的 Microsoft 消費者介面自動化支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="d12c9-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="d12c9-121">滑杆控制項是具有按鈕的複合控制項，可讓使用者設定數位範圍，或從一組專案中選取。</span><span class="sxs-lookup"><span data-stu-id="d12c9-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="d12c9-122">下列章節會定義 **滑杆** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="d12c9-123">消費者介面自動化需求適用于所有滑杆控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="d12c9-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d12c9-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d12c9-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d12c9-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d12c9-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d12c9-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="d12c9-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d12c9-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="d12c9-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d12c9-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="d12c9-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d12c9-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="d12c9-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d12c9-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="d12c9-130">Typical Tree Structure</span></span>

<span data-ttu-id="d12c9-131">下表描述滑杆控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="d12c9-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d12c9-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d12c9-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d12c9-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="d12c9-133">Control View</span></span></th>
<th><span data-ttu-id="d12c9-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="d12c9-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d12c9-135">滑桿</span><span class="sxs-lookup"><span data-stu-id="d12c9-135">Slider</span></span>
<ul>
<li><span data-ttu-id="d12c9-136">按鈕 (2 或 4)</span><span class="sxs-lookup"><span data-stu-id="d12c9-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="d12c9-137">Thumb (1) </span><span class="sxs-lookup"><span data-stu-id="d12c9-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="d12c9-138">清單專案 (0 或更多) </span><span class="sxs-lookup"><span data-stu-id="d12c9-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d12c9-139">滑桿</span><span class="sxs-lookup"><span data-stu-id="d12c9-139">Slider</span></span>
<ul>
<li><span data-ttu-id="d12c9-140">清單專案 (0 或更多) </span><span class="sxs-lookup"><span data-stu-id="d12c9-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="d12c9-141">相關屬性</span><span class="sxs-lookup"><span data-stu-id="d12c9-141">Relevant Properties</span></span>

<span data-ttu-id="d12c9-142">下表列出消費者介面自動化屬性，其值或定義與滑杆控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="d12c9-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="d12c9-143">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="d12c9-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d12c9-144">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="d12c9-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d12c9-145">值</span><span class="sxs-lookup"><span data-stu-id="d12c9-145">Value</span></span>      | <span data-ttu-id="d12c9-146">注意</span><span class="sxs-lookup"><span data-stu-id="d12c9-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d12c9-147">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d12c9-148">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-148">See notes.</span></span> | <span data-ttu-id="d12c9-149">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d12c9-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="d12c9-150">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d12c9-151">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-151">See notes.</span></span> | <span data-ttu-id="d12c9-152">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="d12c9-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="d12c9-153">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d12c9-154">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-154">See notes.</span></span> | <span data-ttu-id="d12c9-155">大部分的滑杆控制項都必須傳回 [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) 錯誤，因為滑杆控制項的整個周框控制項是由子控制項所佔用。</span><span class="sxs-lookup"><span data-stu-id="d12c9-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="d12c9-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d12c9-157">**滑桿**</span><span class="sxs-lookup"><span data-stu-id="d12c9-157">**Slider**</span></span> | <span data-ttu-id="d12c9-158">此值與所有架構的值相同。</span><span class="sxs-lookup"><span data-stu-id="d12c9-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="d12c9-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d12c9-160">true</span><span class="sxs-lookup"><span data-stu-id="d12c9-160">TRUE</span></span>       | <span data-ttu-id="d12c9-161">滑杆控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="d12c9-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="d12c9-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d12c9-163">true</span><span class="sxs-lookup"><span data-stu-id="d12c9-163">TRUE</span></span>       | <span data-ttu-id="d12c9-164">滑杆控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="d12c9-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="d12c9-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d12c9-166">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-166">See notes.</span></span> | <span data-ttu-id="d12c9-167">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="d12c9-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="d12c9-168">滑杆控制項 (按鈕和 thumb) 的子系不應取得焦點。</span><span class="sxs-lookup"><span data-stu-id="d12c9-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="d12c9-169">焦點應該一律保留在滑杆控制項本身。</span><span class="sxs-lookup"><span data-stu-id="d12c9-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="d12c9-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d12c9-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-171">See notes.</span></span> | <span data-ttu-id="d12c9-172">如果有與控制項相關聯的靜態文字標籤，則此屬性必須公開該控制項的參考。</span><span class="sxs-lookup"><span data-stu-id="d12c9-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="d12c9-173">如果文字控制項是另一個控制項的子元件，則不會設定 **LabeledBy** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d12c9-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="d12c9-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d12c9-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-175">See notes.</span></span> | <span data-ttu-id="d12c9-176">對應至 **滑杆** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="d12c9-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="d12c9-177">預設值為 "slider"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="d12c9-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="d12c9-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d12c9-179">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="d12c9-179">See notes.</span></span> | <span data-ttu-id="d12c9-180">滑杆控制項的名稱通常會從靜態文字標籤產生。</span><span class="sxs-lookup"><span data-stu-id="d12c9-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="d12c9-181">如果沒有靜態文字標籤，則應用程式開發人員必須指派 **名稱** 的屬性值。</span><span class="sxs-lookup"><span data-stu-id="d12c9-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d12c9-182">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="d12c9-182">Required Control Patterns</span></span>

<span data-ttu-id="d12c9-183">下表列出所有滑杆控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d12c9-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="d12c9-184">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="d12c9-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d12c9-185">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="d12c9-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="d12c9-186">支援/值</span><span class="sxs-lookup"><span data-stu-id="d12c9-186">Support/Value</span></span> | <span data-ttu-id="d12c9-187">備註</span><span class="sxs-lookup"><span data-stu-id="d12c9-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d12c9-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d12c9-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="d12c9-189">相依</span><span class="sxs-lookup"><span data-stu-id="d12c9-189">Depends</span></span>       | <span data-ttu-id="d12c9-190">如果內容可以設定為數值範圍內的值，則滑杆應支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d12c9-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="d12c9-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="d12c9-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="d12c9-192">相依</span><span class="sxs-lookup"><span data-stu-id="d12c9-192">Depends</span></span>       | <span data-ttu-id="d12c9-193">如果內容代表一組不同選項中的一個值，則滑杆應支援 [選取](uiauto-implementingselection.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d12c9-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="d12c9-194">支援選取控制項模式時，對應的選項必須公開為滑桿的一個或多個子清單項目。</span><span class="sxs-lookup"><span data-stu-id="d12c9-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="d12c9-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d12c9-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="d12c9-196">相依</span><span class="sxs-lookup"><span data-stu-id="d12c9-196">Depends</span></span>       | <span data-ttu-id="d12c9-197">如果內容代表一組離散選項中的一個值，則滑杆應支援 [值](uiauto-implementingvalue.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="d12c9-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="d12c9-198">必要的事件</span><span class="sxs-lookup"><span data-stu-id="d12c9-198">Required Events</span></span>

<span data-ttu-id="d12c9-199">下表列出滑杆控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="d12c9-200">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="d12c9-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d12c9-201">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="d12c9-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d12c9-202">備註</span><span class="sxs-lookup"><span data-stu-id="d12c9-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d12c9-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d12c9-204">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d12c9-205">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d12c9-206">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d12c9-207">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d12c9-208">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="d12c9-209">[**UIA \_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="d12c9-210">如果控制項支援 [RangeValue](uiauto-implementingrangevalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="d12c9-211">**UIA \_ 選取專案 \_ InvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="d12c9-212">如果控制項支援 [選取](uiauto-implementingselection.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="d12c9-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d12c9-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="d12c9-214">[**UIA \_ValueValuePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="d12c9-215">如果控制項支援 [值](uiauto-implementingvalue.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="d12c9-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="d12c9-216">相關主題</span><span class="sxs-lookup"><span data-stu-id="d12c9-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d12c9-217">**概念**</span><span class="sxs-lookup"><span data-stu-id="d12c9-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d12c9-218">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="d12c9-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d12c9-219">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="d12c9-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




