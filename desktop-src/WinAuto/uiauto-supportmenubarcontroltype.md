---
title: 功能表列控制項類型
description: 本主題提供 Microsoft 消費者介面自動化 MenuBar 控制項類型的支援相關資訊。
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- 消費者介面自動化，功能表列控制項類型的支援
- 消費者介面自動化，功能表列控制項類型
- 功能表列控制項類型消費者介面自動化、樹狀結構
- 消費者介面自動化，功能表列控制項類型的屬性
- 消費者介面自動化，功能表列控制項類型的控制項模式
- 消費者介面自動化，功能表列控制項類型的事件
- 樹狀結構，功能表列控制項類型
- properties、MenuBar 控制項類型
- 控制項模式、功能表列控制項類型
- events、MenuBar 控制項類型
- 功能表列控制項類型的支援
- 功能表列控制項類型
- 控制項類型、功能表列控制項類型的樹狀結構
- 控制項類型、功能表列控制項類型的控制項模式
- 控制項類型，支援功能表列
- 控制項類型，功能表列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966188"
---
# <a name="menubar-control-type"></a><span data-ttu-id="a7f18-119">功能表列控制項類型</span><span class="sxs-lookup"><span data-stu-id="a7f18-119">MenuBar Control Type</span></span>

<span data-ttu-id="a7f18-120">本主題提供 Microsoft 消費者介面自動化 **MenuBar** 控制項類型的支援相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7f18-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="a7f18-121">功能表列控制項是 **執行功能表列控制項類型** 的控制項範例。</span><span class="sxs-lookup"><span data-stu-id="a7f18-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="a7f18-122">功能表列可讓使用者啟用應用程式中所包含的命令和選項。</span><span class="sxs-lookup"><span data-stu-id="a7f18-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="a7f18-123">下列章節會定義 **功能表列** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="a7f18-124">消費者介面自動化需求適用于所有的功能表列控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="a7f18-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a7f18-125">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="a7f18-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a7f18-126">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="a7f18-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a7f18-127">相關屬性</span><span class="sxs-lookup"><span data-stu-id="a7f18-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a7f18-128">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="a7f18-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a7f18-129">必要的事件</span><span class="sxs-lookup"><span data-stu-id="a7f18-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a7f18-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7f18-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a7f18-131">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="a7f18-131">Typical Tree Structure</span></span>

<span data-ttu-id="a7f18-132">下表描述功能表列控制項之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="a7f18-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a7f18-133">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="a7f18-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7f18-134">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="a7f18-134">Control View</span></span></th>
<th><span data-ttu-id="a7f18-135">內容檢視</span><span class="sxs-lookup"><span data-stu-id="a7f18-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a7f18-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="a7f18-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="a7f18-137">MenuItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="a7f18-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="a7f18-138">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="a7f18-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a7f18-139">不適用</span><span class="sxs-lookup"><span data-stu-id="a7f18-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="a7f18-140">MenuItem (1 個以上)</span><span class="sxs-lookup"><span data-stu-id="a7f18-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="a7f18-141">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="a7f18-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a7f18-142">功能表列控制項一律會出現在 [內容視圖] 中，但不會顯示在內容視圖中，因為它通常不會將有意義的資訊傳遞給使用者 (除非應用程式包含一個以上的功能表列) 。</span><span class="sxs-lookup"><span data-stu-id="a7f18-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="a7f18-143">消費者介面自動化用戶端可以接聽 [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) 事件，以確保當 UI 進入功能表模式時，這些事件會持續收到通知。</span><span class="sxs-lookup"><span data-stu-id="a7f18-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="a7f18-144">當應用程式處於功能表模式時，可能會針對功能表導覽來捕捉所有鍵盤輸入 (例如，輸入 's ' 可能會叫用 [ **儲存** ] 功能表，而不是在應用程式工作區上輸入字元) 。</span><span class="sxs-lookup"><span data-stu-id="a7f18-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="a7f18-145">**UIA \_ MenuModeStartEventId** 事件必須在第一個 [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)事件之前，以確保邏輯一致性。</span><span class="sxs-lookup"><span data-stu-id="a7f18-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="a7f18-146">[**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)事件會遵循最後一個 [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="a7f18-147">按一下功能表項目也可能會立即觸發 **UIA \_ MenuModeStartEventId** 事件，後面接著 **UIA \_ MenuOpenedEventId** 事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="a7f18-148">功能表列控制項可以在其結構內包含其他控制項，例如編輯控制項和下拉式方塊。</span><span class="sxs-lookup"><span data-stu-id="a7f18-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="a7f18-149">這些額外的控制項對應到控制項和內容檢視中列出的「其他控制項」。</span><span class="sxs-lookup"><span data-stu-id="a7f18-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="a7f18-150">相關屬性</span><span class="sxs-lookup"><span data-stu-id="a7f18-150">Relevant Properties</span></span>

<span data-ttu-id="a7f18-151">下表列出消費者介面自動化屬性，其值或定義與 **功能表列** 控制項類型特別有關。</span><span class="sxs-lookup"><span data-stu-id="a7f18-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="a7f18-152">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="a7f18-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a7f18-153">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="a7f18-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a7f18-154">值</span><span class="sxs-lookup"><span data-stu-id="a7f18-154">Value</span></span>       | <span data-ttu-id="a7f18-155">注意</span><span class="sxs-lookup"><span data-stu-id="a7f18-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7f18-156">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a7f18-157">NULL</span><span class="sxs-lookup"><span data-stu-id="a7f18-157">NULL</span></span>        | <span data-ttu-id="a7f18-158">功能表列通常不會有快速鍵。</span><span class="sxs-lookup"><span data-stu-id="a7f18-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="a7f18-159">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a7f18-160">"ALT"</span><span class="sxs-lookup"><span data-stu-id="a7f18-160">"ALT"</span></span>       | <span data-ttu-id="a7f18-161">按下 ALT 鍵通常應該會將焦點放在應用程式中的功能表列。</span><span class="sxs-lookup"><span data-stu-id="a7f18-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="a7f18-162">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a7f18-163">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a7f18-163">See notes.</span></span>  | <span data-ttu-id="a7f18-164">這個屬性所公開的值必須包含所有內含的控制項。</span><span class="sxs-lookup"><span data-stu-id="a7f18-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="a7f18-165">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a7f18-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="a7f18-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a7f18-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a7f18-168">FALSE</span><span class="sxs-lookup"><span data-stu-id="a7f18-168">FALSE</span></span>       | <span data-ttu-id="a7f18-169">功能表列控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="a7f18-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="a7f18-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a7f18-171">true</span><span class="sxs-lookup"><span data-stu-id="a7f18-171">TRUE</span></span>        | <span data-ttu-id="a7f18-172">功能表列控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="a7f18-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="a7f18-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a7f18-174">true</span><span class="sxs-lookup"><span data-stu-id="a7f18-174">TRUE</span></span>        | <span data-ttu-id="a7f18-175">因為功能表列控制項包含的控制項可接受鍵盤焦點，所以可設定鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="a7f18-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="a7f18-176">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a7f18-177">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a7f18-177">See notes.</span></span>  | <span data-ttu-id="a7f18-178">這個屬性的值取決於此控制項是否可在畫面上檢視。</span><span class="sxs-lookup"><span data-stu-id="a7f18-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="a7f18-179">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a7f18-180">NULL</span><span class="sxs-lookup"><span data-stu-id="a7f18-180">NULL</span></span>        | <span data-ttu-id="a7f18-181">功能表列控制項通常沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="a7f18-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="a7f18-182">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a7f18-183">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a7f18-183">See notes.</span></span>  | <span data-ttu-id="a7f18-184">對應到 **功能表列** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="a7f18-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="a7f18-185">預設值為「功能表列」，適用于 en-us 或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="a7f18-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="a7f18-186">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a7f18-187">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="a7f18-187">See notes.</span></span>  | <span data-ttu-id="a7f18-188">除非應用程式有一個以上的功能表列，否則功能表列控制項不需要名稱。</span><span class="sxs-lookup"><span data-stu-id="a7f18-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="a7f18-189">如果應用程式中有一個以上的功能表列，請使用這個屬性來公開區分名稱，例如「格式化」或「大綱」。</span><span class="sxs-lookup"><span data-stu-id="a7f18-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="a7f18-190">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a7f18-191">相依</span><span class="sxs-lookup"><span data-stu-id="a7f18-191">Depends</span></span>     | <span data-ttu-id="a7f18-192">這個屬性會公開此功能表列控制項是水平或垂直。</span><span class="sxs-lookup"><span data-stu-id="a7f18-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a7f18-193">必要的控制項模式</span><span class="sxs-lookup"><span data-stu-id="a7f18-193">Required Control Patterns</span></span>

<span data-ttu-id="a7f18-194">下表列出功能表列控制項必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="a7f18-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="a7f18-195">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="a7f18-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a7f18-196">控制項模式</span><span class="sxs-lookup"><span data-stu-id="a7f18-196">Control Pattern</span></span>                                                   | <span data-ttu-id="a7f18-197">支援</span><span class="sxs-lookup"><span data-stu-id="a7f18-197">Support</span></span> | <span data-ttu-id="a7f18-198">注意</span><span class="sxs-lookup"><span data-stu-id="a7f18-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7f18-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="a7f18-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="a7f18-200">相依</span><span class="sxs-lookup"><span data-stu-id="a7f18-200">Depends</span></span> | <span data-ttu-id="a7f18-201">如果控制項可展開或折迭，則必須執行 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="a7f18-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="a7f18-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="a7f18-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="a7f18-203">相依</span><span class="sxs-lookup"><span data-stu-id="a7f18-203">Depends</span></span> | <span data-ttu-id="a7f18-204">如果控制項可以停駐在螢幕的不同部分，則必須執行 [Dock](uiauto-implementingdock.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="a7f18-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="a7f18-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="a7f18-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="a7f18-206">相依</span><span class="sxs-lookup"><span data-stu-id="a7f18-206">Depends</span></span> | <span data-ttu-id="a7f18-207">如果控制項可以調整大小、旋轉或移動，則必須執行 [轉換](uiauto-implementingtransform.md) 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="a7f18-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="a7f18-208">必要的事件</span><span class="sxs-lookup"><span data-stu-id="a7f18-208">Required Events</span></span>

<span data-ttu-id="a7f18-209">下表列出支援的功能表列控制項所需的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="a7f18-210">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="a7f18-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a7f18-211">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="a7f18-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="a7f18-212">備註</span><span class="sxs-lookup"><span data-stu-id="a7f18-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7f18-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="a7f18-214">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="a7f18-215">[**UIA \_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="a7f18-216">如果控制項支援 [ExpandCollapse](uiauto-implementingexpandcollapse.md) 控制項模式，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="a7f18-217">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="a7f18-218">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="a7f18-219">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="a7f18-220">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="a7f18-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="a7f18-221">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a7f18-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="a7f18-222">相關主題</span><span class="sxs-lookup"><span data-stu-id="a7f18-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a7f18-223">**概念**</span><span class="sxs-lookup"><span data-stu-id="a7f18-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a7f18-224">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="a7f18-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a7f18-225">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="a7f18-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




