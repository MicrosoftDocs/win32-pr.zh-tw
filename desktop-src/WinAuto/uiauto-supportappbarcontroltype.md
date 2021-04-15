---
title: AppBar 控制項類型
description: 本主題提供 AppBar 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- 消費者介面自動化，AppBar 控制項類型的支援
- 消費者介面自動化，AppBar 控制項類型
- 消費者介面自動化，AppBar 控制項類型的控制項模式
- 控制項模式，AppBar 控制項類型
- AppBar 控制項類型的支援
- AppBar 控制項類型
- 控制項類型，AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463516"
---
# <a name="appbar-control-type"></a><span data-ttu-id="b2a63-110">AppBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="b2a63-110">AppBar Control Type</span></span>

<span data-ttu-id="b2a63-111">本主題提供 **AppBar** 控制項類型之 Microsoft 消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b2a63-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="b2a63-112">應用程式行是 UI 元素，可向使用者呈現導覽、命令和工具。</span><span class="sxs-lookup"><span data-stu-id="b2a63-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="b2a63-113">針對 Windows Store 應用程式，您可以按下 Windows 鍵 + Z 來顯示應用程式的應用程式列。</span><span class="sxs-lookup"><span data-stu-id="b2a63-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="b2a63-114">下列章節會定義 **AppBar** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="b2a63-115">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b2a63-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b2a63-116">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="b2a63-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b2a63-117">相關屬性</span><span class="sxs-lookup"><span data-stu-id="b2a63-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b2a63-118">必要的事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b2a63-119">相關事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="b2a63-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2a63-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b2a63-121">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="b2a63-121">Typical Tree Structure</span></span>

<span data-ttu-id="b2a63-122">下表描述 **AppBar** 控制項相關之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="b2a63-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b2a63-123">**按鈕** 是 **AppBar** 中最常見的元素，但也可能會叫用應用程式動作的其他控制項。</span><span class="sxs-lookup"><span data-stu-id="b2a63-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="b2a63-124">**AppBar** 也可以有0個或多個分隔符號 (**分隔符號** 控制項類型) ，它會出現在控制項視圖中，以放置於其他控制項之間。</span><span class="sxs-lookup"><span data-stu-id="b2a63-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="b2a63-125">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a63-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2a63-126">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="b2a63-126">Control View</span></span></th>
<th><span data-ttu-id="b2a63-127">內容檢視</span><span class="sxs-lookup"><span data-stu-id="b2a63-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b2a63-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="b2a63-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="b2a63-129">按鈕 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b2a63-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="b2a63-130">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b2a63-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b2a63-131">不適用</span><span class="sxs-lookup"><span data-stu-id="b2a63-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="b2a63-132">按鈕 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b2a63-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="b2a63-133">其他控制項 (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="b2a63-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="b2a63-134">相關屬性</span><span class="sxs-lookup"><span data-stu-id="b2a63-134">Relevant Properties</span></span>

<span data-ttu-id="b2a63-135">下表列出消費者介面自動化屬性，其值或定義與執行 **AppBar** 控制項類型的控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="b2a63-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="b2a63-136">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a63-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b2a63-137">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="b2a63-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b2a63-138">值</span><span class="sxs-lookup"><span data-stu-id="b2a63-138">Value</span></span>      | <span data-ttu-id="b2a63-139">注意</span><span class="sxs-lookup"><span data-stu-id="b2a63-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a63-140">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="b2a63-141">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b2a63-141">See notes.</span></span> | <span data-ttu-id="b2a63-142">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b2a63-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="b2a63-143">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b2a63-144">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b2a63-144">See notes.</span></span> | <span data-ttu-id="b2a63-145">這個屬性所公開的值必須包含所有內含的控制項。</span><span class="sxs-lookup"><span data-stu-id="b2a63-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="b2a63-146">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b2a63-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="b2a63-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="b2a63-148">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b2a63-149">FALSE</span><span class="sxs-lookup"><span data-stu-id="b2a63-149">FALSE</span></span>      | <span data-ttu-id="b2a63-150">應用程式的工具列控制項不會包含在消費者介面自動化樹狀結構的內容視圖中。</span><span class="sxs-lookup"><span data-stu-id="b2a63-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="b2a63-151">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b2a63-152">true</span><span class="sxs-lookup"><span data-stu-id="b2a63-152">TRUE</span></span>       | <span data-ttu-id="b2a63-153">應用程式橫條控制項一律會包含在消費者介面自動化樹狀結構的控制項視圖中。</span><span class="sxs-lookup"><span data-stu-id="b2a63-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="b2a63-154">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b2a63-155">請參閱附註</span><span class="sxs-lookup"><span data-stu-id="b2a63-155">See notes</span></span>  | <span data-ttu-id="b2a63-156">如果控制項可接收鍵盤焦點，就必定支援此屬性。</span><span class="sxs-lookup"><span data-stu-id="b2a63-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="b2a63-157">應用程式行內的控制項通常可以取得鍵盤焦點。</span><span class="sxs-lookup"><span data-stu-id="b2a63-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="b2a63-158">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b2a63-159">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b2a63-159">See notes.</span></span> | <span data-ttu-id="b2a63-160">這個屬性的值取決於此控制項是否可在畫面上檢視。</span><span class="sxs-lookup"><span data-stu-id="b2a63-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="b2a63-161">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b2a63-162">Null</span><span class="sxs-lookup"><span data-stu-id="b2a63-162">Null</span></span>       | <span data-ttu-id="b2a63-163">應用程式行控制項通常沒有標籤。</span><span class="sxs-lookup"><span data-stu-id="b2a63-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="b2a63-164">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b2a63-165">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b2a63-165">See notes.</span></span> | <span data-ttu-id="b2a63-166">對應到 **AppBar** 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="b2a63-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="b2a63-167">預設值為 "app bar" （適用于 en-us）或英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="b2a63-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="b2a63-168">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b2a63-169">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="b2a63-169">See notes.</span></span> | <span data-ttu-id="b2a63-170">除非應用程式有一個以上的應用程式行，否則應用程式行控制項不需要名稱。</span><span class="sxs-lookup"><span data-stu-id="b2a63-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="b2a63-171">如果應用程式中有一個以上的應用程式行，請使用此屬性來公開區分名稱，例如 "Top" 或 "底端"。</span><span class="sxs-lookup"><span data-stu-id="b2a63-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="b2a63-172">必要的事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-172">Required Events</span></span>

<span data-ttu-id="b2a63-173">下表列出應用程式橫條控制項必須支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="b2a63-174">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="b2a63-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b2a63-175">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="b2a63-176">備註</span><span class="sxs-lookup"><span data-stu-id="b2a63-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a63-177">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="b2a63-178">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="b2a63-179">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="b2a63-180">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="b2a63-181">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="b2a63-182">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="b2a63-183">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="b2a63-184">相關事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-184">Relevant Events</span></span>

<span data-ttu-id="b2a63-185">下表列出與執行 **AppBar** 控制項類型，但不是絕對必要的控制項特別相關的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="b2a63-186">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="b2a63-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="b2a63-187">備註</span><span class="sxs-lookup"><span data-stu-id="b2a63-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="b2a63-188">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="b2a63-189">當應用程式行控制項關閉時，平臺執行可能會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="b2a63-190">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="b2a63-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="b2a63-191">開啟應用程式行控制項時，平臺執行可能會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="b2a63-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="b2a63-192">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="b2a63-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="b2a63-193">屬性變更的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="b2a63-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="b2a63-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2a63-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b2a63-195">**概念**</span><span class="sxs-lookup"><span data-stu-id="b2a63-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b2a63-196">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="b2a63-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b2a63-197">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="b2a63-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="b2a63-198">**參考**</span><span class="sxs-lookup"><span data-stu-id="b2a63-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b2a63-199">**AppBar XAML 控制項**</span><span class="sxs-lookup"><span data-stu-id="b2a63-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="b2a63-200">[**WinJS. AppBar 物件**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="b2a63-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 