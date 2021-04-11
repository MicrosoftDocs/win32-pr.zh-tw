---
title: SemanticZoom 控制項類型
description: 本主題提供 SemanticZoom 控制項類型之消費者介面自動化支援的相關資訊。
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- 消費者介面自動化，SemanticZoom 控制項類型的支援
- 消費者介面自動化，SemanticZoom 控制項類型
- 消費者介面自動化，SemanticZoom 控制項類型的樹狀結構
- 消費者介面自動化，SemanticZoom 控制項類型的屬性
- 消費者介面自動化，SemanticZoom 控制項類型的控制項模式
- 消費者介面自動化，SemanticZoom 控制項類型的事件
- 樹狀結構，SemanticZoom 控制項類型
- properties、SemanticZoom 控制項類型
- 控制項模式，SemanticZoom 控制項類型
- events、SemanticZoom 控制項類型
- SemanticZoom 控制項類型的支援
- SemanticZoom 控制項類型
- 控制項類型，SemanticZoom 控制項類型的樹狀結構
- 控制項類型，SemanticZoom 控制項類型的控制項模式
- 控制項類型，支援 SemanticZoom
- 控制項類型，SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092752"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="3e60d-119">SemanticZoom 控制項類型</span><span class="sxs-lookup"><span data-stu-id="3e60d-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="3e60d-120">本主題提供 **SemanticZoom** 控制項類型之消費者介面自動化支援的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3e60d-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="3e60d-121">「語義縮放」是 Windows 8 引進的一項技術，可在單一視圖內呈現和導覽大型相關資料集或內容，例如相片專輯、應用程式清單或通訊錄。</span><span class="sxs-lookup"><span data-stu-id="3e60d-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="3e60d-122">語義縮放會使用兩種不同的分類模式（或 *縮放層級*）來組織和呈現內容。</span><span class="sxs-lookup"><span data-stu-id="3e60d-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="3e60d-123">低層級 (或 *放大*) 模式會以平面、「全功能」結構顯示專案;而高階 (或 *放大*) 模式會顯示群組中的專案，讓使用者可以快速流覽和流覽內容。</span><span class="sxs-lookup"><span data-stu-id="3e60d-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="3e60d-124">例如，縮放城市清單可能會變更為包含這些城市的州清單。</span><span class="sxs-lookup"><span data-stu-id="3e60d-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="3e60d-125">縮放程式清單可能會變更為邏輯程式群組清單。</span><span class="sxs-lookup"><span data-stu-id="3e60d-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="3e60d-126">如需有關語義縮放的詳細資訊（特別是用於 Windows Store 應用程式），請參閱 [語義縮放的指導方針](/windows/uwp/controls-and-patterns/semantic-zoom)。</span><span class="sxs-lookup"><span data-stu-id="3e60d-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="3e60d-127">**SemanticZoom** 控制項類型的使用方式模型很不尋常，因為它主要是用來進行程式設計存取。</span><span class="sxs-lookup"><span data-stu-id="3e60d-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="3e60d-128">Microsoft 消費者介面自動化用戶端可以監視和操作語義縮放控制項，以控制清單的放大狀態。</span><span class="sxs-lookup"><span data-stu-id="3e60d-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="3e60d-129">未使用輔助技術的使用者通常會透過觸控手勢或鍵盤快速鍵直接操作語義縮放控制項。</span><span class="sxs-lookup"><span data-stu-id="3e60d-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="3e60d-130">下列章節會定義 **SemanticZoom** 控制項類型所需的消費者介面自動化樹狀結構、屬性、控制項模式和事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="3e60d-131">消費者介面自動化需求適用于所有的語義縮放控制項，其中 UI framework/平臺會整合控制項類型和控制項模式的消費者介面自動化支援。</span><span class="sxs-lookup"><span data-stu-id="3e60d-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="3e60d-132">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="3e60d-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e60d-133">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="3e60d-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3e60d-134">相關屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3e60d-135">必要的控制項模式和屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="3e60d-136">必要的事件</span><span class="sxs-lookup"><span data-stu-id="3e60d-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3e60d-137">備註</span><span class="sxs-lookup"><span data-stu-id="3e60d-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="3e60d-138">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e60d-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3e60d-139">一般樹狀結構</span><span class="sxs-lookup"><span data-stu-id="3e60d-139">Typical Tree Structure</span></span>

<span data-ttu-id="3e60d-140">下表描述 **SemanticZoom** 控制項類型之消費者介面自動化樹狀結構的一般控制項和內容視圖，並說明每個視圖中可包含的內容。</span><span class="sxs-lookup"><span data-stu-id="3e60d-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="3e60d-141">如需消費者介面自動化樹狀結構的詳細資訊，請參閱 [消費者介面自動化樹狀結構總覽](uiauto-treeoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="3e60d-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e60d-142">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="3e60d-142">Control View</span></span></th>
<th><span data-ttu-id="3e60d-143">內容檢視</span><span class="sxs-lookup"><span data-stu-id="3e60d-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3e60d-144">List</span><span class="sxs-lookup"><span data-stu-id="3e60d-144">List</span></span>
<ul>
<li><span data-ttu-id="3e60d-145">[SemanticZoom]</span><span class="sxs-lookup"><span data-stu-id="3e60d-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="3e60d-146">ListItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="3e60d-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3e60d-147">List</span><span class="sxs-lookup"><span data-stu-id="3e60d-147">List</span></span>
<ul>
<li><span data-ttu-id="3e60d-148">ListItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="3e60d-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3e60d-149">或：</span><span class="sxs-lookup"><span data-stu-id="3e60d-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e60d-150">控制項檢視</span><span class="sxs-lookup"><span data-stu-id="3e60d-150">Control View</span></span></th>
<th><span data-ttu-id="3e60d-151">內容檢視</span><span class="sxs-lookup"><span data-stu-id="3e60d-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3e60d-152">[SemanticZoom]</span><span class="sxs-lookup"><span data-stu-id="3e60d-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="3e60d-153">List</span><span class="sxs-lookup"><span data-stu-id="3e60d-153">List</span></span>
<ul>
<li><span data-ttu-id="3e60d-154">ListItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="3e60d-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3e60d-155">List</span><span class="sxs-lookup"><span data-stu-id="3e60d-155">List</span></span>
<ul>
<li><span data-ttu-id="3e60d-156">ListItem (0 個以上)</span><span class="sxs-lookup"><span data-stu-id="3e60d-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="3e60d-157">相關屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-157">Relevant Properties</span></span>

<span data-ttu-id="3e60d-158">下表列出消費者介面自動化屬性，其值或定義與執行 **SemanticZoom** 控制項類型的控制項特別相關。</span><span class="sxs-lookup"><span data-stu-id="3e60d-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="3e60d-159">如需消費者介面自動化屬性的詳細資訊，請參閱 [從消費者介面自動化元素取得屬性](uiauto-propertiesforclients.md)。</span><span class="sxs-lookup"><span data-stu-id="3e60d-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e60d-160">使用者介面自動化屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="3e60d-161">值</span><span class="sxs-lookup"><span data-stu-id="3e60d-161">Value</span></span></th>
<th><span data-ttu-id="3e60d-162">注意</span><span class="sxs-lookup"><span data-stu-id="3e60d-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e60d-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-164">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-164">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-165">這個屬性的值在消費者介面自動化樹狀結構的原始視圖中的所有對等元素之間必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="3e60d-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e60d-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-167">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-167">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-168">包含整個控制項的最外層矩形。</span><span class="sxs-lookup"><span data-stu-id="3e60d-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e60d-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-170">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-170">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-171">如果清單控制項具有可點按的點 (可按一下以使清單取得焦點) 的點，則必須透過這個屬性公開該點。</span><span class="sxs-lookup"><span data-stu-id="3e60d-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="3e60d-172">如果 <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> 屬性的值為 <strong>TRUE</strong>，則嘗試取得此屬性會導致 <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> 錯誤。</span><span class="sxs-lookup"><span data-stu-id="3e60d-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e60d-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="3e60d-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3e60d-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-176">true</span><span class="sxs-lookup"><span data-stu-id="3e60d-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3e60d-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-178">true</span><span class="sxs-lookup"><span data-stu-id="3e60d-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="3e60d-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e60d-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="3e60d-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-182">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-182">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-183">如果有靜態文字標籤，這個屬性必須公開該控制項的參考。</span><span class="sxs-lookup"><span data-stu-id="3e60d-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e60d-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-185">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-185">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-186">對應到 <strong>SemanticZoom</strong> 控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="3e60d-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="3e60d-187">預設值為 &quot; &quot; En-us 或英文 (美國) 的語義縮放。</span><span class="sxs-lookup"><span data-stu-id="3e60d-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="3e60d-188">某些架構將此串連為 &quot; semanticzoom &quot; 。</span><span class="sxs-lookup"><span data-stu-id="3e60d-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e60d-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="3e60d-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="3e60d-190">請參閱備註。</span><span class="sxs-lookup"><span data-stu-id="3e60d-190">See notes.</span></span></td>
<td><span data-ttu-id="3e60d-191">空字串是可接受的，或是可以提供更有用的名稱，只要它不包含「語義比例」詞彙，這會讓控制項類型和名稱的組合混淆。</span><span class="sxs-lookup"><span data-stu-id="3e60d-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="3e60d-192">必要的控制項模式和屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="3e60d-193">下表列出所有語義縮放控制項都必須支援的消費者介面自動化控制項模式。</span><span class="sxs-lookup"><span data-stu-id="3e60d-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="3e60d-194">如需控制項模式的詳細資訊，請參閱 [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md)。</span><span class="sxs-lookup"><span data-stu-id="3e60d-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="3e60d-195">控制項模式/模式屬性</span><span class="sxs-lookup"><span data-stu-id="3e60d-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="3e60d-196">支援/值</span><span class="sxs-lookup"><span data-stu-id="3e60d-196">Support/Value</span></span> | <span data-ttu-id="3e60d-197">備註</span><span class="sxs-lookup"><span data-stu-id="3e60d-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e60d-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="3e60d-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="3e60d-199">相依</span><span class="sxs-lookup"><span data-stu-id="3e60d-199">Depends</span></span>       | <span data-ttu-id="3e60d-200">語義縮放控制項支援 [切換](uiauto-implementingtoggle.md) 控制項模式，允許啟用或停用縮放。</span><span class="sxs-lookup"><span data-stu-id="3e60d-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="3e60d-201">[**ToggleState \_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) 對應于 [一般]、[全部啟動] 狀態，而 [ [**ToggleState \_**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) ] 對應至 [高階]、[放大] 視圖。</span><span class="sxs-lookup"><span data-stu-id="3e60d-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="3e60d-202">必要的事件</span><span class="sxs-lookup"><span data-stu-id="3e60d-202">Required Events</span></span>

<span data-ttu-id="3e60d-203">下表列出需要語義縮放控制項才能支援的消費者介面自動化事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="3e60d-204">如需 [UI Automation Events Overview](uiauto-eventsoverview.md)事件的詳細資訊，請參閱</span><span class="sxs-lookup"><span data-stu-id="3e60d-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3e60d-205">消費者介面自動化事件</span><span class="sxs-lookup"><span data-stu-id="3e60d-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="3e60d-206">備註</span><span class="sxs-lookup"><span data-stu-id="3e60d-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e60d-207">[**UIA \_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="3e60d-208">[**UIA \_IsEnabledPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="3e60d-209">如果控制項支援 [**IsEnabled**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="3e60d-210">[**UIA \_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="3e60d-211">如果控制項支援 [**IsOffscreen**](uiauto-automation-element-propids.md) 屬性，就必須支援這個事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="3e60d-212">[**UIA \_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) 屬性變更事件。</span><span class="sxs-lookup"><span data-stu-id="3e60d-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="3e60d-213">備註</span><span class="sxs-lookup"><span data-stu-id="3e60d-213">Remarks</span></span>

<span data-ttu-id="3e60d-214">如果 UI 具有切換語義縮放控制項行為的可見按鈕，此按鈕就不應該有 **SemanticZoom** 控制項類型。</span><span class="sxs-lookup"><span data-stu-id="3e60d-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="3e60d-215">這是可直覺化的，但 **SemanticZoom** 控制項類型是指縮放內容容器的特性，而不是控制縮放的按鈕。</span><span class="sxs-lookup"><span data-stu-id="3e60d-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="3e60d-216">您可以使用[切換](uiauto-implementingtoggle.md)控制項模式，以[按鈕](uiauto-supportbuttoncontroltype.md)控制項類型來表示 (這類按鈕。 ) </span><span class="sxs-lookup"><span data-stu-id="3e60d-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e60d-217">相關主題</span><span class="sxs-lookup"><span data-stu-id="3e60d-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e60d-218">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="3e60d-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3e60d-219">UI 自動化概觀</span><span class="sxs-lookup"><span data-stu-id="3e60d-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

