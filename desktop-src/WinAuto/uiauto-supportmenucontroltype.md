---
title: Menu 控制項類型
description: 本主題提供功能表控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- 消費者介面自動化，支援 Menu 控制項類型
- 消費者介面自動化，功能表控制項類型
- 消費者介面自動化，功能表控制項類型的樹狀結構
- 消費者介面自動化，功能表控制項類型的屬性
- 消費者介面自動化，功能表控制項類型的控制項模式
- 消費者介面自動化，Menu 控制項類型的事件
- 樹狀結構，功能表控制項類型
- 屬性，功能表控制項類型
- 控制項模式，功能表控制項類型
- 事件、功能表控制項類型
- Menu 控制項類型的支援
- 功能表控制項類型
- Menu 控制項類型的控制項類型、樹狀結構
- 控制項類型、功能表控制項類型的控制項模式
- 控制項類型，支援功能表
- 控制項類型，功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021340"
---
# <a name="menu-control-type"></a><span data-ttu-id="a98e0-119">Menu 控制項類型</span><span class="sxs-lookup"><span data-stu-id="a98e0-119">Menu Control Type</span></span>

<span data-ttu-id="a98e0-120">本主題提供 **功能表** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a98e0-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="a98e0-121">功能表控制項可將命令和事件處理常式的關聯項目以階層方式組織。</span><span class="sxs-lookup"><span data-stu-id="a98e0-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="a98e0-122">在一般的 Microsoft Windows 應用程式中，功能表列會包含數個功能表按鈕 **(例如 [** 檔案]、[ **編輯**] 和 [ **視窗]**) ，而且每個功能表按鈕都會顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="a98e0-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="a98e0-123">功能表又包含一組功能表項目 (例如 [開新檔案] **F:System.Windows.Automation.AutomationElementIdentifiers.IsEnabledProperty**、[開啟舊檔] **UI Automation Properties Overview** 和 [關閉檔案] **TLA#tla_win32**)，這些項目可展開顯示更多的功能表項目，或在按一下時可執行特定的動作。</span><span class="sxs-lookup"><span data-stu-id="a98e0-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="a98e0-124">下列章節會定義 **功能表** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="a98e0-125">消費者介面自動化需求適用于所有的功能表控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="a98e0-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a98e0-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a98e0-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a98e0-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="a98e0-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a98e0-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="a98e0-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a98e0-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="a98e0-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a98e0-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="a98e0-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a98e0-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="a98e0-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a98e0-132">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="a98e0-132">Typical Tree Structure</span></span>

<span data-ttu-id="a98e0-133">下表描述功能表控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="a98e0-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a98e0-134">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="a98e0-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a98e0-135">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="a98e0-135">Control View</span></span></th>
<th><span data-ttu-id="a98e0-136">內容檢視</span><span class="sxs-lookup"><span data-stu-id="a98e0-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a98e0-137">功能表</span><span class="sxs-lookup"><span data-stu-id="a98e0-137">Menu</span></span>
<ul>
<li><span data-ttu-id="a98e0-138">MenuItem (1 或多個)</span><span class="sxs-lookup"><span data-stu-id="a98e0-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="a98e0-139">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="a98e0-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a98e0-140">功能表</span><span class="sxs-lookup"><span data-stu-id="a98e0-140">Menu</span></span>
<ul>
<li><span data-ttu-id="a98e0-141">MenuItem (1 或多個)</span><span class="sxs-lookup"><span data-stu-id="a98e0-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="a98e0-142">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="a98e0-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a98e0-143">功能表控制項一律會出現在 [控制台] 和 [消費者介面自動化] 樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="a98e0-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="a98e0-144">功能表控制項應該會出現在其資訊所參考的控制項底下。</span><span class="sxs-lookup"><span data-stu-id="a98e0-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="a98e0-145">消費者介面自動化用戶端可以接聽 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) ，以確保它們持續取得功能表控制項所傳達的資訊。</span><span class="sxs-lookup"><span data-stu-id="a98e0-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="a98e0-146">內容功能表控制項是特殊案例。</span><span class="sxs-lookup"><span data-stu-id="a98e0-146">Context menu controls are a special case.</span></span> <span data-ttu-id="a98e0-147">它們可能會顯示為桌面的子系或最上層應用程式視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="a98e0-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="a98e0-148">Menu 控制項可以在其結構內包含其他控制項，例如編輯控制項和下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="a98e0-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="a98e0-149">這些額外的控制項會對應到控制項和內容視圖中上表所列的「其他控制項」。</span><span class="sxs-lookup"><span data-stu-id="a98e0-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="a98e0-150">相關屬性</span><span class="sxs-lookup"><span data-stu-id="a98e0-150">Relevant Properties</span></span>

<span data-ttu-id="a98e0-151">下表列出消費者介面自動化屬性，其值或定義與 **功能表** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="a98e0-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="a98e0-152">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="a98e0-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a98e0-153">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="a98e0-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="a98e0-154">值</span><span class="sxs-lookup"><span data-stu-id="a98e0-154">Value</span></span>      | <span data-ttu-id="a98e0-155">注意</span><span class="sxs-lookup"><span data-stu-id="a98e0-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a98e0-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="a98e0-157">**功能表**</span><span class="sxs-lookup"><span data-stu-id="a98e0-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="a98e0-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a98e0-159">true</span><span class="sxs-lookup"><span data-stu-id="a98e0-159">TRUE</span></span>       | <span data-ttu-id="a98e0-160">功能表控制項一律包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="a98e0-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="a98e0-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a98e0-162">true</span><span class="sxs-lookup"><span data-stu-id="a98e0-162">TRUE</span></span>       | <span data-ttu-id="a98e0-163">功能表控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="a98e0-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="a98e0-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="a98e0-165">NULL</span><span class="sxs-lookup"><span data-stu-id="a98e0-165">NULL</span></span>       | <span data-ttu-id="a98e0-166">典型的功能表控制項不預期有標籤。</span><span class="sxs-lookup"><span data-stu-id="a98e0-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="a98e0-167">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="a98e0-168">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a98e0-168">See notes.</span></span> | <span data-ttu-id="a98e0-169">Menu 控制項不需要設定 **name** 屬性，也可以與相關聯的控制項（例如開啟子功能表的功能表項目）有相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="a98e0-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a98e0-170">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="a98e0-170">Required Control Patterns</span></span>

<span data-ttu-id="a98e0-171">功能表控制項類型沒有必要的控制項模式。</span><span class="sxs-lookup"><span data-stu-id="a98e0-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="a98e0-172">必要的事件</span><span class="sxs-lookup"><span data-stu-id="a98e0-172">Required Events</span></span>

<span data-ttu-id="a98e0-173">當功能表控制項出現在螢幕上時，必須引發 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="a98e0-174">**UIA \_ MenuOpenedEventId** 事件將包含控制項的文字。</span><span class="sxs-lookup"><span data-stu-id="a98e0-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="a98e0-175">當功能表從畫面上消失時，必須引發 [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="a98e0-176">下表列出支援的功能表控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="a98e0-177">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="a98e0-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a98e0-178">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="a98e0-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="a98e0-179">備註</span><span class="sxs-lookup"><span data-stu-id="a98e0-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a98e0-180">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="a98e0-181">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="a98e0-182">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="a98e0-183">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="a98e0-184">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="a98e0-185">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="a98e0-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="a98e0-186">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="a98e0-187">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="a98e0-188">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a98e0-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="a98e0-189">相關主題</span><span class="sxs-lookup"><span data-stu-id="a98e0-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a98e0-190">**概念**</span><span class="sxs-lookup"><span data-stu-id="a98e0-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a98e0-191">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="a98e0-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a98e0-192">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="a98e0-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




