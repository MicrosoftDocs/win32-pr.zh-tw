---
title: MenuItem 控制項類型
description: 本主題提供 MenuItem 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- 消費者介面自動化，MenuItem 控制項類型的支援
- 消費者介面自動化，MenuItem 控制項類型
- 消費者介面自動化，MenuItem 控制項類型的樹狀結構
- 消費者介面自動化，MenuItem 控制項類型的屬性
- 消費者介面自動化，MenuItem 控制項類型的控制項模式
- 消費者介面自動化，MenuItem 控制項類型的事件
- 樹狀結構，MenuItem 控制項類型
- 屬性，MenuItem 控制項類型
- 控制項模式、MenuItem 控制項類型
- events、MenuItem 控制項類型
- MenuItem 控制項類型的支援
- MenuItem 控制項類型
- MenuItem 控制項類型的控制項類型、樹狀結構
- 控制項類型，MenuItem 控制項類型的控制項模式
- 控制項類型，支援 MenuItem
- 控制項類型，MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24033866f749974a41d39094b416e70f3c40f796
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300791"
---
# <a name="menuitem-control-type"></a><span data-ttu-id="11464-119">MenuItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="11464-119">MenuItem Control Type</span></span>

<span data-ttu-id="11464-120">本主題提供 **MenuItem** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="11464-120">This topic provides information about Microsoft UI Automation support for the **MenuItem** control type.</span></span>

<span data-ttu-id="11464-121">功能表控制項可將命令和事件處理常式的關聯項目以階層方式組織。</span><span class="sxs-lookup"><span data-stu-id="11464-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="11464-122">在一般 Windows 應用程式中，功能表列會包含數個功能表項目 (例如 [檔案]、[**編輯**] 和 [**視窗) ]** **，而** 每個功能表項目會顯示功能表。</span><span class="sxs-lookup"><span data-stu-id="11464-122">In a typical Windows application, a menu bar contains several menu items (such as **File**, **Edit**, and **Window**), and each menu item displays a menu.</span></span> <span data-ttu-id="11464-123">功能表又包含一組功能表項目 (例如 [開新檔案] 、[開啟舊檔] 和 [關閉檔案] )，這些項目可展開顯示更多的功能表項目，或在按一下時可執行特定的動作。</span><span class="sxs-lookup"><span data-stu-id="11464-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or perform a specific action when clicked.</span></span>

<span data-ttu-id="11464-124">下列章節會定義 **MenuItem** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="11464-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuItem** control type.</span></span> <span data-ttu-id="11464-125">消費者介面自動化需求適用于所有的功能表項目控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="11464-125">The UI Automation requirements apply to all menu item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="11464-126">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="11464-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="11464-127">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="11464-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="11464-128">相關屬性</span><span class="sxs-lookup"><span data-stu-id="11464-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="11464-129">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="11464-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="11464-130">必要的事件</span><span class="sxs-lookup"><span data-stu-id="11464-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="11464-131">舊版問題</span><span class="sxs-lookup"><span data-stu-id="11464-131">Legacy Issues</span></span>](#legacy-issues)
-   [<span data-ttu-id="11464-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="11464-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="11464-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="11464-133">Typical Tree Structure</span></span>

<span data-ttu-id="11464-134">下表描述的是與功能表項目控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="11464-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="11464-135">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="11464-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11464-136">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="11464-136">Control View</span></span></th>
<th><span data-ttu-id="11464-137">內容檢視</span><span class="sxs-lookup"><span data-stu-id="11464-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="11464-138">MenuItem &quot; 說明&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-138">MenuItem &quot;Help&quot;</span></span>
<ul>
<li><span data-ttu-id="11464-139">[說明] 功能表項目的功能表 (子功能表) </span><span class="sxs-lookup"><span data-stu-id="11464-139">Menu (submenu of Help menu item)</span></span>
<ul>
<li><span data-ttu-id="11464-140">MenuItem &quot; 說明主題&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-140">MenuItem &quot;Help Topics&quot;</span></span></li>
<li><span data-ttu-id="11464-141">&quot;關於記事本的 MenuItem&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-141">MenuItem &quot;About Notepad&quot;</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="11464-142">MenuItem &quot; 說明&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-142">MenuItem &quot;Help&quot;</span></span>
<ul>
<li><span data-ttu-id="11464-143">MenuItem &quot; 說明主題&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-143">MenuItem &quot;Help Topics&quot;</span></span></li>
<li><span data-ttu-id="11464-144">&quot;關於記事本的 MenuItem&quot;</span><span class="sxs-lookup"><span data-stu-id="11464-144">MenuItem &quot;About Notepad&quot;</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="11464-145">功能表項目控制項的控制項視圖具有上面所示的消費者介面自動化樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="11464-145">The control view of the menu item control has the UI Automation tree structure shown above.</span></span> <span data-ttu-id="11464-146">請注意，已新增功能表 **欄上的** [說明] 功能表項目來更清楚地說明此結構。</span><span class="sxs-lookup"><span data-stu-id="11464-146">Note that the menu item for **Help** on the menu bar has been added to better illustrate the structure.</span></span>

<span data-ttu-id="11464-147">針對內容視圖，消費者介面自動化樹狀目錄中不存在 **功能表** ，因為它不會將有意義的資訊傳遞給使用者。</span><span class="sxs-lookup"><span data-stu-id="11464-147">For the content view, **Menu** is absent from the UI Automation tree because it does not convey meaningful information to the end user.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="11464-148">相關屬性</span><span class="sxs-lookup"><span data-stu-id="11464-148">Relevant Properties</span></span>

<span data-ttu-id="11464-149">下表列出消費者介面自動化屬性，其值或定義與 **MenuItem** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="11464-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuItem** control type.</span></span> <span data-ttu-id="11464-150">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="11464-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="11464-151">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="11464-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="11464-152">值</span><span class="sxs-lookup"><span data-stu-id="11464-152">Value</span></span>        | <span data-ttu-id="11464-153">注意</span><span class="sxs-lookup"><span data-stu-id="11464-153">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11464-154">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="11464-155">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-155">See notes.</span></span>   | <span data-ttu-id="11464-156">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="11464-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span> <span data-ttu-id="11464-157">如果已知專案在使用者介面的不同實例之間是一致的，則配置功能表項目的 **AutomationId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="11464-157">Allocate the **AutomationId** property for a menu item if the element is known to be consistent across different instances of the user interface.</span></span> <span data-ttu-id="11464-158">如果功能表項目動態填入且不可預測，請將 **AutomationId** 屬性保留空白。</span><span class="sxs-lookup"><span data-stu-id="11464-158">If the menu item is dynamically populated and not predictable, leave the **AutomationId** property blank.</span></span> |
| [<span data-ttu-id="11464-159">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-159">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="11464-160">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-160">See notes.</span></span>   | <span data-ttu-id="11464-161">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="11464-161">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="11464-162">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-162">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="11464-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-163">See notes.</span></span>   | <span data-ttu-id="11464-164">如果有週框即受支援。</span><span class="sxs-lookup"><span data-stu-id="11464-164">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="11464-165">如果無法按下周框中的每個點，而且專案會執行特製化的點擊測試，請覆寫並提供可按一下的點。</span><span class="sxs-lookup"><span data-stu-id="11464-165">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                                     |
| [<span data-ttu-id="11464-166">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="11464-167">**MenuItem**</span><span class="sxs-lookup"><span data-stu-id="11464-167">**MenuItem**</span></span> |                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="11464-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="11464-169">true</span><span class="sxs-lookup"><span data-stu-id="11464-169">TRUE</span></span>         | <span data-ttu-id="11464-170">功能表項目控制項一律會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="11464-170">The menu item control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="11464-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="11464-172">true</span><span class="sxs-lookup"><span data-stu-id="11464-172">TRUE</span></span>         | <span data-ttu-id="11464-173">功能表項目控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="11464-173">The menu item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="11464-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="11464-175">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-175">See notes.</span></span>   | <span data-ttu-id="11464-176">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="11464-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="11464-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="11464-178">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-178">See notes.</span></span>   | <span data-ttu-id="11464-179">對應至 **MenuItem** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="11464-179">Localized string corresponding to the **MenuItem** control type.</span></span> <span data-ttu-id="11464-180">預設值為「功能表項目」，適用于 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="11464-180">The default value is "menu item" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                  |
| [<span data-ttu-id="11464-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="11464-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="11464-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="11464-182">See notes.</span></span>   | <span data-ttu-id="11464-183">功能表項目控制項的名稱是用來加上標籤的文字。</span><span class="sxs-lookup"><span data-stu-id="11464-183">The name of the menu item control is the text used to label it.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="11464-184">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="11464-184">Required Control Patterns</span></span>

<span data-ttu-id="11464-185">下表列出功能表項目控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="11464-185">The following table lists the UI Automation control patterns required to be supported by menu item controls.</span></span> <span data-ttu-id="11464-186">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="11464-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="11464-187">控制項模式</span><span class="sxs-lookup"><span data-stu-id="11464-187">Control Pattern</span></span>                                                   | <span data-ttu-id="11464-188">支援</span><span class="sxs-lookup"><span data-stu-id="11464-188">Support</span></span> | <span data-ttu-id="11464-189">注意</span><span class="sxs-lookup"><span data-stu-id="11464-189">Notes</span></span>                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11464-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="11464-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="11464-191">相依</span><span class="sxs-lookup"><span data-stu-id="11464-191">Depends</span></span> | <span data-ttu-id="11464-192">如果可以展開或折迭控制項，請執行 [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)。</span><span class="sxs-lookup"><span data-stu-id="11464-192">If the control can be expanded or collapsed, implement [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).</span></span>                            |
| [<span data-ttu-id="11464-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="11464-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="11464-194">相依</span><span class="sxs-lookup"><span data-stu-id="11464-194">Depends</span></span> | <span data-ttu-id="11464-195">如果控制項執行單一動作或命令，請執行 [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)。</span><span class="sxs-lookup"><span data-stu-id="11464-195">If the control executes a single action or command, implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).</span></span>                                     |
| [<span data-ttu-id="11464-196">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="11464-196">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="11464-197">相依</span><span class="sxs-lookup"><span data-stu-id="11464-197">Depends</span></span> | <span data-ttu-id="11464-198">如果控制項是用來從功能表項目中的選項清單中選取，請執行 [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)。</span><span class="sxs-lookup"><span data-stu-id="11464-198">If the control is used to select from a list of options among menu items, implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span> |
| [<span data-ttu-id="11464-199">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="11464-199">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="11464-200">相依</span><span class="sxs-lookup"><span data-stu-id="11464-200">Depends</span></span> | <span data-ttu-id="11464-201">如果控制項代表可以開啟或關閉的選項，請執行 [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)。</span><span class="sxs-lookup"><span data-stu-id="11464-201">If the control represents an option that can be turned on or off, implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>                       |



 

## <a name="required-events"></a><span data-ttu-id="11464-202">必要的事件</span><span class="sxs-lookup"><span data-stu-id="11464-202">Required Events</span></span>

<span data-ttu-id="11464-203">下表列出支援的功能表項目控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="11464-203">The following table lists the UI Automation events that menu item controls are required to support.</span></span> <span data-ttu-id="11464-204">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="11464-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="11464-205">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="11464-205">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="11464-206">備註</span><span class="sxs-lookup"><span data-stu-id="11464-206">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11464-207">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-207">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="11464-208">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="11464-208">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="11464-209">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="11464-209">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="11464-210">如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-210">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="11464-211">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-211">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="11464-212">如果控制項支援 [Invoke](uiauto-implementinginvoke.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-212">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="11464-213">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="11464-213">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="11464-214">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-214">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="11464-215">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="11464-215">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="11464-216">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-216">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="11464-217">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-217">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="11464-218">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-218">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="11464-219">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-219">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="11464-220">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-220">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="11464-221">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-221">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="11464-222">如果控制項支援 [SelectionItem](uiauto-implementingselectionitem.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-222">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="11464-223">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="11464-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="11464-224">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="11464-224">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="11464-225">如果控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="11464-225">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |



 

## <a name="legacy-issues"></a><span data-ttu-id="11464-226">舊版問題</span><span class="sxs-lookup"><span data-stu-id="11464-226">Legacy Issues</span></span>

<span data-ttu-id="11464-227">若為 Microsoft Win32 功能表項目，只有在選取功能表項目時才支援 [切換](uiauto-implementingtoggle.md) 控制項模式，而您可以透過程式設計方式判斷是否需要切換控制項模式的支援。</span><span class="sxs-lookup"><span data-stu-id="11464-227">For Microsoft Win32 menu items, the [Toggle](uiauto-implementingtoggle.md) control pattern is supported only when a menu item is checked and it is possible to programmatically determine whether support for the Toggle control pattern is required.</span></span> <span data-ttu-id="11464-228">因為 Win32 功能表項目不會公開是否可以進行檢查，所以不檢查功能表項目時，就會支援 Invoke 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="11464-228">Because a Win32 menu item does not expose whether it can be checked, the Invoke control pattern is supported when the menu item is not checked.</span></span> <span data-ttu-id="11464-229">除了支援切換控制項模式所需的功能表項目之外，也一律支援 Invoke 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="11464-229">The Invoke control pattern is always supported, even for menu items that are only required to support the Toggle control pattern.</span></span> <span data-ttu-id="11464-230">如此一來，當功能表項目未核取時，用戶端就不[](uiauto-implementinginvoke.md)會混淆 (當功能表項目未核取時，) 不會再于檢查時再支援該模式。</span><span class="sxs-lookup"><span data-stu-id="11464-230">This is so clients do not become confused when a menu item that was supporting the [Invoke](uiauto-implementinginvoke.md) control pattern (when the menu item was unchecked) no longer supports that pattern when it becomes checked.</span></span>

## <a name="related-topics"></a><span data-ttu-id="11464-231">相關主題</span><span class="sxs-lookup"><span data-stu-id="11464-231">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="11464-232">**概念**</span><span class="sxs-lookup"><span data-stu-id="11464-232">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="11464-233">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="11464-233">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="11464-234">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="11464-234">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




