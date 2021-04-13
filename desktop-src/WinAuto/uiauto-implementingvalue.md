---
title: 值控制項模式
description: 描述執行 IValueProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- 消費者介面自動化，實值控制項模式
- 消費者介面自動化，值控制項模式
- 消費者介面自動化、IValueProvider
- IValueProvider
- 實消費者介面自動化值控制項模式
- 值控制項模式
- 控制項模式，IValueProvider
- 控制項模式，實施消費者介面自動化值
- 控制項模式、值
- 介面，IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375993"
---
# <a name="value-control-pattern"></a><span data-ttu-id="9595b-113">值控制項模式</span><span class="sxs-lookup"><span data-stu-id="9595b-113">Value Control Pattern</span></span>

<span data-ttu-id="9595b-114">描述執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9595b-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="9595b-115">**值** 控制項模式用來支援具有未跨越範圍且可以表示為字串之內建值的控制項。</span><span class="sxs-lookup"><span data-stu-id="9595b-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="9595b-116">您可以根據控制項及其設定，來編輯值字串。</span><span class="sxs-lookup"><span data-stu-id="9595b-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="9595b-117">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="9595b-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9595b-118">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="9595b-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9595b-119">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="9595b-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9595b-120">**IValueProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="9595b-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="9595b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="9595b-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9595b-122">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="9595b-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9595b-123">在實 **值** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="9595b-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9595b-124">如果任何專案的值都是可編輯的，則控制項（例如清單專案或樹狀結構專案）必須支援 **值** 控制項模式，不論控制項目前的編輯模式為何。</span><span class="sxs-lookup"><span data-stu-id="9595b-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="9595b-125">如果子專案是可編輯的，父控制項也必須支援 **值** 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="9595b-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="9595b-126">下圖顯示可編輯清單專案的範例。</span><span class="sxs-lookup"><span data-stu-id="9595b-126">The following image shows an example of an editable list item.</span></span>

    ![顯示可編輯清單專案的圖例](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="9595b-128">單一和多行編輯控制項必須執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 來公開其唯讀內容。</span><span class="sxs-lookup"><span data-stu-id="9595b-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="9595b-129">如果可以變更多行編輯控制項的內容，則必須執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 。</span><span class="sxs-lookup"><span data-stu-id="9595b-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="9595b-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 不支援抓取格式化資訊或子字串值。</span><span class="sxs-lookup"><span data-stu-id="9595b-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="9595b-131">在這些案例中執行 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 。</span><span class="sxs-lookup"><span data-stu-id="9595b-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="9595b-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 必須由 Microsoft Word 中的色彩選擇器選取控制項等控制項來執行， (請參閱下圖) ，其支援色彩值之間的字串對應 (例如，"黃色" ) 和相等的內部 [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) 值。</span><span class="sxs-lookup"><span data-stu-id="9595b-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![顯示色樣字串對應的圖例](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="9595b-134">控制項應將其 **IsEnabled** 屬性設定為 **TRUE** ，並在允許呼叫 [**ITextProvider：： SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)之前，將其 [**ITextProvider：： IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)屬性設定為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="9595b-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="9595b-135">**IValueProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="9595b-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="9595b-136">執行 [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="9595b-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="9595b-137">必要成員</span><span class="sxs-lookup"><span data-stu-id="9595b-137">Required members</span></span>                                       | <span data-ttu-id="9595b-138">成員類型</span><span class="sxs-lookup"><span data-stu-id="9595b-138">Member type</span></span> | <span data-ttu-id="9595b-139">備註</span><span class="sxs-lookup"><span data-stu-id="9595b-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="9595b-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="9595b-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="9595b-141">屬性</span><span class="sxs-lookup"><span data-stu-id="9595b-141">Property</span></span>    | <span data-ttu-id="9595b-142">無</span><span class="sxs-lookup"><span data-stu-id="9595b-142">None</span></span>  |
| [<span data-ttu-id="9595b-143">**值**</span><span class="sxs-lookup"><span data-stu-id="9595b-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="9595b-144">屬性</span><span class="sxs-lookup"><span data-stu-id="9595b-144">Property</span></span>    | <span data-ttu-id="9595b-145">無</span><span class="sxs-lookup"><span data-stu-id="9595b-145">None</span></span>  |
| [<span data-ttu-id="9595b-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="9595b-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="9595b-147">方法</span><span class="sxs-lookup"><span data-stu-id="9595b-147">Method</span></span>      | <span data-ttu-id="9595b-148">無</span><span class="sxs-lookup"><span data-stu-id="9595b-148">None</span></span>  |



 

<span data-ttu-id="9595b-149">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="9595b-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9595b-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="9595b-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9595b-151">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="9595b-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9595b-152">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="9595b-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9595b-153">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="9595b-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="9595b-154">Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="9595b-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 