---
title: UI 自動化控制項類型概觀
description: Microsoft 消費者介面自動化控制項類型是可做為已知識別碼的屬性，表示特定 UI 專案所代表的控制項類型，例如下拉式方塊或按鈕。
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- 消費者介面自動化，控制項類型總覽
- 消費者介面自動化，UIA_LocalizedControlTypePropertyId 屬性
- 控制項類型，關於
- 控制項類型，先決條件
- 控制項類型，必要條件
- 控制項類型，預先定義
- 控制項類型，UIA_LocalizedControlTypePropertyId 屬性
- 預先定義的控制項類型
- UIA_LocalizedControlTypePropertyId 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507939"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="5f7db-112">UI 自動化控制項類型概觀</span><span class="sxs-lookup"><span data-stu-id="5f7db-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="5f7db-113">Microsoft 消費者介面自動化控制項類型是可做為已知識別碼的屬性，表示特定 UI 專案所代表的控制項類型，例如下拉式方塊或按鈕。</span><span class="sxs-lookup"><span data-stu-id="5f7db-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="5f7db-114">用戶端應用程式會使用類型來識別控制項的功能，以及判斷如何與其互動。</span><span class="sxs-lookup"><span data-stu-id="5f7db-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="5f7db-115">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="5f7db-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="5f7db-116">UI 自動化控制項類型必要條件</span><span class="sxs-lookup"><span data-stu-id="5f7db-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="5f7db-117">LocalizedControlType 屬性</span><span class="sxs-lookup"><span data-stu-id="5f7db-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="5f7db-118">目前 UI 自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="5f7db-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f7db-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="5f7db-120">UI 自動化控制項類型必要條件</span><span class="sxs-lookup"><span data-stu-id="5f7db-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="5f7db-121">每個消費者介面自動化控制項類型都有一組相關聯的條件。</span><span class="sxs-lookup"><span data-stu-id="5f7db-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="5f7db-122">當提供者將控制項類型指派給控制項時，提供者必須確保控制項符合與該控制項類型相關聯的所有條件。</span><span class="sxs-lookup"><span data-stu-id="5f7db-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="5f7db-123">這些條件包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="5f7db-123">The conditions include the following:</span></span>

-   <span data-ttu-id="5f7db-124">消費者介面自動化控制項模式：每個控制項類型都有一組控制項必須支援的控制項模式、選擇性的集合，以及控制項不能支援的集合。</span><span class="sxs-lookup"><span data-stu-id="5f7db-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="5f7db-125">使用者介面自動化屬性值：每個控制項類型都有一組控制項必須支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="5f7db-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="5f7db-126">使用者介面自動化事件：每個控制項類型都有一組控制項必須支援的事件。</span><span class="sxs-lookup"><span data-stu-id="5f7db-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="5f7db-127">使用者介面自動化樹狀結構：每個控制項類型皆定義控制項在使用者介面自動化樹狀結構中必須如何顯示。</span><span class="sxs-lookup"><span data-stu-id="5f7db-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="5f7db-128">當控制項符合特定控制項類型的條件時， [**IUIAutomationElement：： CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (或 [**IUIAutomationElement：：) CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype) 屬性值會指出該控制項類型。</span><span class="sxs-lookup"><span data-stu-id="5f7db-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="5f7db-129">如果您的控制項不符合特定控制項類型的規格，請使用 [**UIA \_ CustomControlTypeId**](uiauto-controltype-ids.md) 做為控制項類型識別碼，並使用相關的控制項模式和屬性來完全描述控制項。</span><span class="sxs-lookup"><span data-stu-id="5f7db-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="5f7db-130">您也可以將 [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) 屬性設定為最能描述控制項類型的字串。</span><span class="sxs-lookup"><span data-stu-id="5f7db-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="5f7db-131">LocalizedControlType 屬性</span><span class="sxs-lookup"><span data-stu-id="5f7db-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="5f7db-132">如果您使用預先定義的控制項類型來描述您的控制項，請使用 [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) 屬性的預設值，並允許消費者介面自動化提供當地語系化的字串，讓提供者正確公開。</span><span class="sxs-lookup"><span data-stu-id="5f7db-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="5f7db-133">如果您無法使用預先定義的控制項類型來描述您的控制項，請將 **UIA \_ LocalizedControlTypePropertyId** 屬性設定為可精確描述控制項類型的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="5f7db-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="5f7db-134">此字串應該很簡潔，但其精確度足以讓輔助技術（例如螢幕讀取器）可以在 UI 中使用它來通知使用者控制項的型別。</span><span class="sxs-lookup"><span data-stu-id="5f7db-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="5f7db-135">目前 UI 自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="5f7db-136">下列主題描述消費者介面自動化控制項類型。</span><span class="sxs-lookup"><span data-stu-id="5f7db-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="5f7db-137">針對每個控制項類型，描述包含指定類型的控制項必須支援的一組條件：</span><span class="sxs-lookup"><span data-stu-id="5f7db-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="5f7db-138">AppBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="5f7db-139">Button 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="5f7db-140">行事曆控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="5f7db-141">CheckBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="5f7db-142">ComboBox 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="5f7db-143">DataGrid 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="5f7db-144">DataItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="5f7db-145">檔控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="5f7db-146">編輯控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="5f7db-147">群組控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="5f7db-148">標題控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="5f7db-149">HeaderItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="5f7db-150">Hyperlink 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="5f7db-151">影像控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="5f7db-152">清單控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   <span data-ttu-id="5f7db-153">[[類型] 控制項類型](uiauto-supportlistitemcontroltype.md)</span><span class="sxs-lookup"><span data-stu-id="5f7db-153">[ListItem Control Type](uiauto-supportlistitemcontroltype.md)</span></span>
-   [<span data-ttu-id="5f7db-154">Menu 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="5f7db-155">功能表列控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="5f7db-156">MenuItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="5f7db-157">窗格控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="5f7db-158">ProgressBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="5f7db-159">選項按鈕控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="5f7db-160">捲軸控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="5f7db-161">SemanticZoom 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="5f7db-162">分隔符號控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="5f7db-163">滑杆控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="5f7db-164">微調控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="5f7db-165">SplitButton 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="5f7db-166">狀態列控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="5f7db-167">索引標籤控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="5f7db-168">TabItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="5f7db-169">Table 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="5f7db-170">Text 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="5f7db-171">Thumb 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="5f7db-172">標題列控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="5f7db-173">ToolBar 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="5f7db-174">ToolTip 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="5f7db-175">樹狀目錄控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="5f7db-176">TreeItem 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="5f7db-177">Window 控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="5f7db-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f7db-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5f7db-179">**參考**</span><span class="sxs-lookup"><span data-stu-id="5f7db-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5f7db-180">控制項類型識別碼</span><span class="sxs-lookup"><span data-stu-id="5f7db-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="5f7db-181">**概念**</span><span class="sxs-lookup"><span data-stu-id="5f7db-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5f7db-182">支援消費者介面自動化控制項類型</span><span class="sxs-lookup"><span data-stu-id="5f7db-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="5f7db-183">標準控制項的 UI 自動化支援</span><span class="sxs-lookup"><span data-stu-id="5f7db-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="5f7db-184">UI 自動化基礎</span><span class="sxs-lookup"><span data-stu-id="5f7db-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 