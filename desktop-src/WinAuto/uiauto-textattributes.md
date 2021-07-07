---
title: 消費者介面自動化 Text 屬性
description: 本主題說明 Microsoft 消費者介面自動化如何公開格式和樣式屬性 (文字內容) 的 text 屬性，並提供支援的文字屬性清單。
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- 消費者介面自動化，text 屬性
- text 屬性，關於
- 文字屬性、變異類型
- 文字屬性，資料類型
- 消費者介面自動化，屬性清單
- 消費者介面自動化，文字屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353621"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="45bb3-109">消費者介面自動化 Text 屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="45bb3-110">本主題說明 Microsoft 消費者介面自動化如何公開格式和樣式屬性 (文字內容) 的 *text 屬性* ，並提供支援的文字屬性清單。</span><span class="sxs-lookup"><span data-stu-id="45bb3-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="45bb3-111">消費者介面自動化提供者會透過 [TextRange](uiauto-about-text-and-textrange-patterns.md)控制項模式的 [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)和 [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)方法來公開文字屬性。</span><span class="sxs-lookup"><span data-stu-id="45bb3-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="45bb3-112">用戶端應用程式會使用 [**IUIAutomationTextRange：： GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) 方法來抓取文字範圍的特定文字屬性值。</span><span class="sxs-lookup"><span data-stu-id="45bb3-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="45bb3-113">用戶端可以使用 [**IUIAutomationTextRange：： FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) 方法，在文字範圍中搜尋具有特定屬性的文字。</span><span class="sxs-lookup"><span data-stu-id="45bb3-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="45bb3-114">如果找到任何相符的文字，方法會建立包含相符文字的新文字範圍。</span><span class="sxs-lookup"><span data-stu-id="45bb3-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="45bb3-115">**TextRange** 控制項模式支援下列清單中的 text 屬性。</span><span class="sxs-lookup"><span data-stu-id="45bb3-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="45bb3-116">屬性名稱衍生自消費者介面自動化的 text 屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="45bb3-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="45bb3-117">例如， **AnimationStyle** 屬性是由用戶端識別為 [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (定義于) uiautomationclient.dll 中，而提供者則是 AnimationStyle. h) 中定義的 **Text \_ Uiautomationcoreapi \_ attribute \_ GUID** (。</span><span class="sxs-lookup"><span data-stu-id="45bb3-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="45bb3-118">如需每個支援的 text 屬性的詳細資訊，請參閱 [**文字屬性識別碼**](uiauto-textattribute-ids.md)。</span><span class="sxs-lookup"><span data-stu-id="45bb3-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="45bb3-119">從 Windows 8 開始支援列出的部分屬性。</span><span class="sxs-lookup"><span data-stu-id="45bb3-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="45bb3-120">如需有關版本支援的附注，請參閱 [**文字屬性識別碼**](uiauto-textattribute-ids.md) 。</span><span class="sxs-lookup"><span data-stu-id="45bb3-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="45bb3-121">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="45bb3-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="45bb3-122">註釋屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="45bb3-123">字型屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="45bb3-124">語言屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="45bb3-125">連結屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="45bb3-126">頁面邊界屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="45bb3-127">文字對齊屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="45bb3-128">文字色彩屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="45bb3-129">文字裝飾屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="45bb3-130">文字樣式屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="45bb3-131">互動和選取屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="45bb3-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="45bb3-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="45bb3-133">註釋屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-133">Annotation Attributes</span></span>

<span data-ttu-id="45bb3-134">批註物件和批註類型可透過下列屬性取得。</span><span class="sxs-lookup"><span data-stu-id="45bb3-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="45bb3-135">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-135">Attribute</span></span>             | <span data-ttu-id="45bb3-136">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="45bb3-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="45bb3-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="45bb3-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-annotation-type-identifiers.md) |
| <span data-ttu-id="45bb3-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="45bb3-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="45bb3-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="45bb3-141">字型屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-141">Font Attributes</span></span>

<span data-ttu-id="45bb3-142">您可以透過下列屬性取得字型的名稱、大小和權數。</span><span class="sxs-lookup"><span data-stu-id="45bb3-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="45bb3-143">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-143">Attribute</span></span>      | <span data-ttu-id="45bb3-144">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="45bb3-145">**FontName**</span></span>   | [<span data-ttu-id="45bb3-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="45bb3-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="45bb3-147">**FontSize**</span></span>   | [<span data-ttu-id="45bb3-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="45bb3-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="45bb3-149">**FontWeight**</span></span> | [<span data-ttu-id="45bb3-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="45bb3-151">語言屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-151">Language Attributes</span></span>

<span data-ttu-id="45bb3-152">您可以透過下列屬性取得文字語言的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="45bb3-153">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-153">Attribute</span></span>              | <span data-ttu-id="45bb3-154">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-155">**文化特性**</span><span class="sxs-lookup"><span data-stu-id="45bb3-155">**Culture**</span></span>            | [<span data-ttu-id="45bb3-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="45bb3-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="45bb3-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="45bb3-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="45bb3-159">連結屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-159">Link Attribute</span></span>

<span data-ttu-id="45bb3-160">下列屬性提供的文字範圍是檔中連結的目標。</span><span class="sxs-lookup"><span data-stu-id="45bb3-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="45bb3-161">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-161">Attribute</span></span> | <span data-ttu-id="45bb3-162">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-163">**連結**</span><span class="sxs-lookup"><span data-stu-id="45bb3-163">**Link**</span></span>  | [<span data-ttu-id="45bb3-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="45bb3-165">頁面邊界屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-165">Page Margin Attributes</span></span>

<span data-ttu-id="45bb3-166">文字範圍的周框矩形不會公開頁面中文字的座標。</span><span class="sxs-lookup"><span data-stu-id="45bb3-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="45bb3-167">但是，提供者可以使用下列文字屬性來公開頁面邊界資訊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="45bb3-168">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-168">Attribute</span></span>          | <span data-ttu-id="45bb3-169">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="45bb3-170">**MarginBottom**</span></span>   | [<span data-ttu-id="45bb3-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="45bb3-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="45bb3-172">**MarginLeading**</span></span>  | [<span data-ttu-id="45bb3-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="45bb3-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="45bb3-174">**MarginTop**</span></span>      | [<span data-ttu-id="45bb3-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="45bb3-176">**MarginTrailing**</span></span> | [<span data-ttu-id="45bb3-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="45bb3-178">文字對齊屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-178">Text Alignment Attributes</span></span>

<span data-ttu-id="45bb3-179">您可以透過下列屬性取得文字對齊方式的相關資訊，例如縮排、定位鍵設定和水準對齊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="45bb3-180">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-180">Attribute</span></span>                   | <span data-ttu-id="45bb3-181">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="45bb3-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="45bb3-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="45bb3-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="45bb3-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="45bb3-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="45bb3-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="45bb3-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-188">**IndentationTrailing**</span><span class="sxs-lookup"><span data-stu-id="45bb3-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="45bb3-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="45bb3-190">**索引標籤**</span><span class="sxs-lookup"><span data-stu-id="45bb3-190">**Tabs**</span></span>                    | [<span data-ttu-id="45bb3-191">**UIA \_ TabsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="45bb3-192">文字色彩屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-192">Text Color Attributes</span></span>

<span data-ttu-id="45bb3-193">前景和背景文字色彩可透過下列 text 屬性取得。</span><span class="sxs-lookup"><span data-stu-id="45bb3-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="45bb3-194">這兩種色彩都指定為 [**COLORREF**](/windows/desktop/gdi/colorref) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="45bb3-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="45bb3-195">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-195">Attribute</span></span>           | <span data-ttu-id="45bb3-196">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="45bb3-197">**BackgroundColor**</span></span> | [<span data-ttu-id="45bb3-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="45bb3-199">**ForegroundColor**</span></span> | [<span data-ttu-id="45bb3-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="45bb3-201">文字裝飾屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-201">Text Decoration Attributes</span></span>

<span data-ttu-id="45bb3-202">文字裝飾包括專案符號、底線和動畫等區域。</span><span class="sxs-lookup"><span data-stu-id="45bb3-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="45bb3-203">如果文字包含前置的專案符號或數位，則文字資料流程中應包含專案符號或數位所使用的符號或文字（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="45bb3-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="45bb3-204">您可以透過下列屬性取得文字裝飾的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="45bb3-205">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-205">Attribute</span></span>              | <span data-ttu-id="45bb3-206">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-207">**AnimationStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="45bb3-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="45bb3-209">**BulletStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-209">**BulletStyle**</span></span>        | [<span data-ttu-id="45bb3-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="45bb3-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="45bb3-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="45bb3-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="45bb3-213">**OverlineColor**</span></span>      | [<span data-ttu-id="45bb3-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="45bb3-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="45bb3-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="45bb3-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="45bb3-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="45bb3-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="45bb3-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="45bb3-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="45bb3-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="45bb3-225">文字樣式屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-225">Text Style Attributes</span></span>

<span data-ttu-id="45bb3-226">您可以使用下列屬性來取得文字樣式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="45bb3-227">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-227">Attribute</span></span>         | <span data-ttu-id="45bb3-228">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="45bb3-229">**CapStyle**</span></span>      | [<span data-ttu-id="45bb3-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="45bb3-231">**IsHidden**</span></span>      | [<span data-ttu-id="45bb3-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-233">**IsItalic**</span><span class="sxs-lookup"><span data-stu-id="45bb3-233">**IsItalic**</span></span>      | [<span data-ttu-id="45bb3-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="45bb3-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="45bb3-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="45bb3-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="45bb3-237">**IsSuperscript**</span></span> | [<span data-ttu-id="45bb3-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="45bb3-239">**IsSubscript**</span></span>   | [<span data-ttu-id="45bb3-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="45bb3-241">互動和選取屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="45bb3-242">您可以透過下列屬性，取得範圍和焦點狀態中目前文字選取範圍的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="45bb3-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="45bb3-243">屬性</span><span class="sxs-lookup"><span data-stu-id="45bb3-243">Attribute</span></span>              | <span data-ttu-id="45bb3-244">識別碼</span><span class="sxs-lookup"><span data-stu-id="45bb3-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45bb3-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="45bb3-245">**IsActive**</span></span>           | [<span data-ttu-id="45bb3-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="45bb3-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="45bb3-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="45bb3-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="45bb3-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="45bb3-249">**CaretPosition**</span></span>      | [<span data-ttu-id="45bb3-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="45bb3-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="45bb3-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="45bb3-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="45bb3-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="45bb3-253">相關主題</span><span class="sxs-lookup"><span data-stu-id="45bb3-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="45bb3-254">**概念**</span><span class="sxs-lookup"><span data-stu-id="45bb3-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="45bb3-255">關於消費者介面自動化 Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="45bb3-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="45bb3-256">Text 和 TextRange 控制項模式</span><span class="sxs-lookup"><span data-stu-id="45bb3-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="45bb3-257">使用以文字為基礎的控制項</span><span class="sxs-lookup"><span data-stu-id="45bb3-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 