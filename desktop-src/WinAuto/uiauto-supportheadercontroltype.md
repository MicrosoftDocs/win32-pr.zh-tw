---
title: 標題控制項類型
description: 本主題提供標題控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- 消費者介面自動化，標題控制項類型的支援
- 消費者介面自動化，標題控制項類型
- 消費者介面自動化，標題控制項類型的樹狀結構
- 消費者介面自動化，標題控制項類型的屬性
- 消費者介面自動化，適用于標題控制項類型的控制項模式
- 消費者介面自動化，標題控制項類型的事件
- 樹狀結構，標題控制項類型
- 屬性、標題控制項類型
- 控制項模式，標題控制項類型
- 事件，標題控制項類型
- 標題控制項類型的支援
- Header 控制項類型
- 控制項類型，標題控制項類型的樹狀結構
- 控制項類型，標題控制項類型的控制項模式
- 控制項類型，支援標頭
- 控制項類型，標頭
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372125"
---
# <a name="header-control-type"></a><span data-ttu-id="54a53-119">標題控制項類型</span><span class="sxs-lookup"><span data-stu-id="54a53-119">Header Control Type</span></span>

<span data-ttu-id="54a53-120">本主題提供 **標題** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="54a53-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="54a53-121">標題控制項可為資料列或資料行資訊的標籤提供視覺容器。</span><span class="sxs-lookup"><span data-stu-id="54a53-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="54a53-122">下列章節會定義 **標題** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="54a53-123">消費者介面自動化需求適用于所有的標頭控制項，其中 UI 架構/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="54a53-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="54a53-124">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="54a53-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="54a53-125">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="54a53-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="54a53-126">相關屬性</span><span class="sxs-lookup"><span data-stu-id="54a53-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="54a53-127">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="54a53-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="54a53-128">必要的事件</span><span class="sxs-lookup"><span data-stu-id="54a53-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="54a53-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="54a53-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="54a53-130">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="54a53-130">Typical Tree Structure</span></span>

<span data-ttu-id="54a53-131">下表描述標題控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="54a53-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="54a53-132">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="54a53-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54a53-133">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="54a53-133">Control View</span></span></th>
<th><span data-ttu-id="54a53-134">內容檢視</span><span class="sxs-lookup"><span data-stu-id="54a53-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="54a53-135">標頭</span><span class="sxs-lookup"><span data-stu-id="54a53-135">Header</span></span>
<ul>
<li><span data-ttu-id="54a53-136">HeaderItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="54a53-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="54a53-137">(不適用)</span><span class="sxs-lookup"><span data-stu-id="54a53-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="54a53-138">標題控制項在消費者介面自動化樹狀結構的控制視圖中一律會有一或多個子系。</span><span class="sxs-lookup"><span data-stu-id="54a53-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="54a53-139">標題控制項在消費者介面自動化樹狀結構的內容視圖中有零個子系。</span><span class="sxs-lookup"><span data-stu-id="54a53-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="54a53-140">相關屬性</span><span class="sxs-lookup"><span data-stu-id="54a53-140">Relevant Properties</span></span>

<span data-ttu-id="54a53-141">下表列出消費者介面自動化屬性，其值或定義與標題控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="54a53-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="54a53-142">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="54a53-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="54a53-143">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="54a53-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="54a53-144">值</span><span class="sxs-lookup"><span data-stu-id="54a53-144">Value</span></span>                                                            | <span data-ttu-id="54a53-145">注意</span><span class="sxs-lookup"><span data-stu-id="54a53-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a53-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="54a53-147">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-147">See notes.</span></span>                                                       | <span data-ttu-id="54a53-148">這個屬性的值在應用程式中的所有控制項之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="54a53-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="54a53-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="54a53-150">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-150">See notes.</span></span>                                                       | <span data-ttu-id="54a53-151">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="54a53-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="54a53-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="54a53-153">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-153">See notes.</span></span>                                                       | <span data-ttu-id="54a53-154">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="54a53-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="54a53-155">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="54a53-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="54a53-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="54a53-157">**標頭**</span><span class="sxs-lookup"><span data-stu-id="54a53-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="54a53-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="54a53-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="54a53-159">FALSE</span></span>                                                            | <span data-ttu-id="54a53-160">標題控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="54a53-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="54a53-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="54a53-162">true</span><span class="sxs-lookup"><span data-stu-id="54a53-162">TRUE</span></span>                                                             | <span data-ttu-id="54a53-163">標題控制項一律包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="54a53-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="54a53-164">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="54a53-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-165">See notes.</span></span>                                                       | <span data-ttu-id="54a53-166">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="54a53-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="54a53-167">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="54a53-168">NULL</span><span class="sxs-lookup"><span data-stu-id="54a53-168">NULL</span></span>                                                             | <span data-ttu-id="54a53-169">標題控制項沒有靜態標籤。</span><span class="sxs-lookup"><span data-stu-id="54a53-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="54a53-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="54a53-171">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-171">See notes.</span></span>                                                       | <span data-ttu-id="54a53-172">預設值為 "header"，代表 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="54a53-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="54a53-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="54a53-174">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="54a53-174">See notes.</span></span>                                                       | <span data-ttu-id="54a53-175">如果有一個以上的資料列標題或資料行標題，標題控制項就需要名稱。</span><span class="sxs-lookup"><span data-stu-id="54a53-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="54a53-176">如此可識別標題內的資訊。</span><span class="sxs-lookup"><span data-stu-id="54a53-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="54a53-177">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54a53-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="54a53-178">**OrientationType \_水準** 或 **OrientationType \_ 垂直**</span><span class="sxs-lookup"><span data-stu-id="54a53-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="54a53-179">這個屬性的值會公開標題控制項的位置，也就是它是否為數據列標頭， (**OrientationType \_ 水準**) 或資料行標頭 (**OrientationType \_ 垂直**) 。</span><span class="sxs-lookup"><span data-stu-id="54a53-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="54a53-180">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="54a53-180">Required Control Patterns</span></span>

<span data-ttu-id="54a53-181">下表列出標題控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="54a53-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="54a53-182">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="54a53-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="54a53-183">控制項模式</span><span class="sxs-lookup"><span data-stu-id="54a53-183">Control Pattern</span></span>                                         | <span data-ttu-id="54a53-184">支援</span><span class="sxs-lookup"><span data-stu-id="54a53-184">Support</span></span> | <span data-ttu-id="54a53-185">注意</span><span class="sxs-lookup"><span data-stu-id="54a53-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a53-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="54a53-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="54a53-187">相依</span><span class="sxs-lookup"><span data-stu-id="54a53-187">Depends</span></span> | <span data-ttu-id="54a53-188">如果標頭控制項可以調整大小，請執行 [轉換](uiauto-implementingtransform.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="54a53-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="54a53-189">必要的事件</span><span class="sxs-lookup"><span data-stu-id="54a53-189">Required Events</span></span>

<span data-ttu-id="54a53-190">下表列出支援的標題控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="54a53-191">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="54a53-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="54a53-192">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="54a53-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="54a53-193">備註</span><span class="sxs-lookup"><span data-stu-id="54a53-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54a53-194">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="54a53-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="54a53-195">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="54a53-196">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="54a53-197">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="54a53-198">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="54a53-199">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="54a53-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="54a53-200">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="54a53-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="54a53-201">相關主題</span><span class="sxs-lookup"><span data-stu-id="54a53-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="54a53-202">**概念**</span><span class="sxs-lookup"><span data-stu-id="54a53-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54a53-203">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="54a53-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="54a53-204">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="54a53-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




