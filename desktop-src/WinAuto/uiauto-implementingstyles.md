---
title: 樣式控制項模式
description: 描述執行 IStylesProvider 的方針和慣例，包括屬性和方法的相關資訊。 樣式控制項模式是用來描述具有特定樣式、填滿色彩、填滿模式或圖形的 UI 元素。
ms.assetid: 65125E07-70D4-48E5-B18D-E9D66ABC6FC0
keywords:
- 消費者介面自動化，執行樣式控制項模式
- 消費者介面自動化，樣式控制項模式
- 消費者介面自動化、IStylesProvider
- IStylesProvider
- 執行消費者介面自動化樣式控制項模式
- 樣式控制項模式
- 控制項模式，IStylesProvider
- 控制項模式，執行消費者介面自動化樣式
- 控制項模式、樣式
- 介面，IStylesProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 611e2f1979aaa4744ce3ff39965053f63399b2b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682933"
---
# <a name="styles-control-pattern"></a><span data-ttu-id="14a63-114">樣式控制項模式</span><span class="sxs-lookup"><span data-stu-id="14a63-114">Styles Control Pattern</span></span>

<span data-ttu-id="14a63-115">描述執行 [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="14a63-115">Describes guidelines and conventions for implementing [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider), including information about properties and methods.</span></span> <span data-ttu-id="14a63-116">**樣式** 控制項模式是用來描述具有特定樣式、填滿色彩、填滿模式或圖形的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="14a63-116">The **Styles** control pattern is used to describe a UI element that has a specific style, fill color, fill pattern, or shape.</span></span>

<span data-ttu-id="14a63-117">**樣式** 控制項模式特別適用于描述檔中的專案，這通常會有這類樣式。</span><span class="sxs-lookup"><span data-stu-id="14a63-117">The **Styles** control pattern is especially useful for describing elements in a document, which frequently have such styles.</span></span> <span data-ttu-id="14a63-118">樣式通常會攜帶適用于殘障客戶的資訊;例如，樣式可以將特定字串描述為檔的標題，或是將特定流程圖物件描述為鑽石或圓形。</span><span class="sxs-lookup"><span data-stu-id="14a63-118">Styles typically carry information that is useful for customers with disabilities; for example, a style can describe a certain string as the title of a document, or a certain flowchart object as a diamond or a circle.</span></span> <span data-ttu-id="14a63-119">如需執行此控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="14a63-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="14a63-120">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="14a63-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="14a63-121">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="14a63-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="14a63-122">**IStylesProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="14a63-122">Required Members for **IStylesProvider**</span></span>](#required-members-for-istylesprovider)
-   [<span data-ttu-id="14a63-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="14a63-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="14a63-124">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="14a63-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="14a63-125">在執行 **樣式** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="14a63-125">When implementing the **Styles** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="14a63-126">Uiautomationclient.dll 標頭檔會定義一組命名的常數值，用來識別數個常見的樣式。</span><span class="sxs-lookup"><span data-stu-id="14a63-126">The UIAutomationClient.h header file defines a set of named constant values used to identify several common styles.</span></span> <span data-ttu-id="14a63-127">如需詳細資訊，請參閱 [**樣式識別碼**](uiauto-style-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="14a63-127">For more information, see [**Style Identifiers**](uiauto-style-identifiers.md).</span></span>
-   <span data-ttu-id="14a63-128">如果您使用 [**StyleId \_ 自訂**](uiauto-style-identifiers.md)，則必須執行 [**IStylesProvider：： StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) 屬性，讓用戶端能夠探索樣式的名稱。</span><span class="sxs-lookup"><span data-stu-id="14a63-128">If you use [**StyleId\_Custom**](uiauto-style-identifiers.md), you must implement the [**IStylesProvider::StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) property to enable clients to discover the name of the style.</span></span> <span data-ttu-id="14a63-129">您不需要執行標準樣式的 **StyleName** 屬性，因為 Microsoft 消費者介面自動化會提供預設名稱，但如果您需要覆寫預設名稱，則可以加以執行。</span><span class="sxs-lookup"><span data-stu-id="14a63-129">You do not need to implement the **StyleName** property for a standard style because Microsoft UI Automation provides a default name, but you can implement it if you need to override the default name.</span></span>
-   <span data-ttu-id="14a63-130">**樣式** 模式中的其他屬性是選擇性的;提供者可以針對不支援的屬性傳回 [**UIA \_ E \_ NOTSUPPORTED**](uiauto-error-codes.md) 。</span><span class="sxs-lookup"><span data-stu-id="14a63-130">The other properties in the **Styles** pattern are optional; the provider can return [**UIA\_E\_NOTSUPPORTED**](uiauto-error-codes.md) for a property that is not supported.</span></span>
-   <span data-ttu-id="14a63-131">文字範圍中的樣式可透過下列文字屬性來表示：</span><span class="sxs-lookup"><span data-stu-id="14a63-131">Styles in a text range can be represented through the following text attributes:</span></span>
    -   <span data-ttu-id="14a63-132">回應 [**StyleId**](uiauto-textattribute-ids.md) text 屬性的要求時，文字範圍應傳回 [**樣式識別碼**](uiauto-style-identifiers.md)中所述的其中一個樣式識別碼。</span><span class="sxs-lookup"><span data-stu-id="14a63-132">When responding to a request for the [**StyleId**](uiauto-textattribute-ids.md) text attribute, the text range should return one of the style identifiers described in [**Style Identifiers**](uiauto-style-identifiers.md).</span></span>
    -   <span data-ttu-id="14a63-133">如果使用 [**StyleId \_ Custom**](uiauto-style-identifiers.md) ，則文字範圍應傳回 [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) text 屬性的字串值，讓用戶端能夠探索樣式名稱。</span><span class="sxs-lookup"><span data-stu-id="14a63-133">If [**StyleId\_Custom**](uiauto-style-identifiers.md) is used, the text range should return a string value for the [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) text attribute to enable clients to discover the style name.</span></span>
    -   <span data-ttu-id="14a63-134">具有多個樣式的文字範圍（例如標題和一般文字）應該會傳回 [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)和 [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)屬性的特殊消費者介面自動化 [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)屬性。</span><span class="sxs-lookup"><span data-stu-id="14a63-134">A text range that has multiple styles, such as both heading and normal text, should return the special UI Automation [**ReservedMixedAttributeValue**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue) property for both the [**StyleId**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid) and [**StyleName**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename) properties.</span></span> <span data-ttu-id="14a63-135">接收此回應的用戶端可以細分文字範圍，以找出樣式的開頭和結尾。</span><span class="sxs-lookup"><span data-stu-id="14a63-135">A client receiving this response can subdivide the text range to find where the styles begin and end.</span></span>
-   <span data-ttu-id="14a63-136">應用程式可以使用各式各樣的樣式來描述物件，但是消費者介面自動化只代表最常見的物件。</span><span class="sxs-lookup"><span data-stu-id="14a63-136">Applications can use a wide variety of styles to describe objects, but UI Automation represents only the most common ones.</span></span> <span data-ttu-id="14a63-137">若要表示其他樣式屬性，例如框線色彩，提供者可以傳回 [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) 屬性中的其他屬性清單。</span><span class="sxs-lookup"><span data-stu-id="14a63-137">To represent additional style attributes, such as border color, a provider can return a list of additional attributes in the [**ExtendedProperties**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) property.</span></span> <span data-ttu-id="14a63-138">這基本上是具有一組擴充屬性的屬性包，例如 "邊框： = 0xFF0000;BorderStyle = 點線」。</span><span class="sxs-lookup"><span data-stu-id="14a63-138">This is basically a property bag with a set of extended properties, such as "BorderColor=0xFF0000;BorderStyle=dotted".</span></span> <span data-ttu-id="14a63-139">擴充屬性的值可以是應用程式特定的值。</span><span class="sxs-lookup"><span data-stu-id="14a63-139">The values of extended properties can be application-specific.</span></span>

## <a name="required-members-for-istylesprovider"></a><span data-ttu-id="14a63-140">**IStylesProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="14a63-140">Required Members for **IStylesProvider**</span></span>

<span data-ttu-id="14a63-141">執行 [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) 介面需要下列屬性。</span><span class="sxs-lookup"><span data-stu-id="14a63-141">The following properties are required for implementing the [**IStylesProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-istylesprovider) interface.</span></span>



| <span data-ttu-id="14a63-142">必要成員</span><span class="sxs-lookup"><span data-stu-id="14a63-142">Required members</span></span>                                                            | <span data-ttu-id="14a63-143">成員類型</span><span class="sxs-lookup"><span data-stu-id="14a63-143">Member type</span></span> | <span data-ttu-id="14a63-144">備註</span><span class="sxs-lookup"><span data-stu-id="14a63-144">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="14a63-145">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="14a63-145">**ExtendedProperties**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-istylesprovider-get_extendedproperties) | <span data-ttu-id="14a63-146">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-146">Property</span></span>    | <span data-ttu-id="14a63-147">無</span><span class="sxs-lookup"><span data-stu-id="14a63-147">None</span></span>  |
| [<span data-ttu-id="14a63-148">**FillColor**</span><span class="sxs-lookup"><span data-stu-id="14a63-148">**FillColor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillcolor)                       | <span data-ttu-id="14a63-149">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-149">Property</span></span>    | <span data-ttu-id="14a63-150">無</span><span class="sxs-lookup"><span data-stu-id="14a63-150">None</span></span>  |
| [<span data-ttu-id="14a63-151">**FillPatternColor**</span><span class="sxs-lookup"><span data-stu-id="14a63-151">**FillPatternColor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatterncolor)         | <span data-ttu-id="14a63-152">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-152">Property</span></span>    | <span data-ttu-id="14a63-153">無</span><span class="sxs-lookup"><span data-stu-id="14a63-153">None</span></span>  |
| [<span data-ttu-id="14a63-154">**FillPatternStyle**</span><span class="sxs-lookup"><span data-stu-id="14a63-154">**FillPatternStyle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_fillpatternstyle)         | <span data-ttu-id="14a63-155">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-155">Property</span></span>    | <span data-ttu-id="14a63-156">無</span><span class="sxs-lookup"><span data-stu-id="14a63-156">None</span></span>  |
| [<span data-ttu-id="14a63-157">**形狀**</span><span class="sxs-lookup"><span data-stu-id="14a63-157">**Shape**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_shape)                               | <span data-ttu-id="14a63-158">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-158">Property</span></span>    | <span data-ttu-id="14a63-159">無</span><span class="sxs-lookup"><span data-stu-id="14a63-159">None</span></span>  |
| [<span data-ttu-id="14a63-160">**StyleId**</span><span class="sxs-lookup"><span data-stu-id="14a63-160">**StyleId**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_styleid)                           | <span data-ttu-id="14a63-161">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-161">Property</span></span>    | <span data-ttu-id="14a63-162">無</span><span class="sxs-lookup"><span data-stu-id="14a63-162">None</span></span>  |
| [<span data-ttu-id="14a63-163">**StyleName**</span><span class="sxs-lookup"><span data-stu-id="14a63-163">**StyleName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-istylesprovider-get_stylename)                       | <span data-ttu-id="14a63-164">屬性</span><span class="sxs-lookup"><span data-stu-id="14a63-164">Property</span></span>    | <span data-ttu-id="14a63-165">無</span><span class="sxs-lookup"><span data-stu-id="14a63-165">None</span></span>  |



 

<span data-ttu-id="14a63-166">此控制項模式沒有任何相關聯的方法或事件。</span><span class="sxs-lookup"><span data-stu-id="14a63-166">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14a63-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="14a63-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14a63-168">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="14a63-168">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="14a63-169">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="14a63-169">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="14a63-170">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="14a63-170">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 