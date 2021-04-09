---
title: TextChild 控制項模式
description: 介紹執行 ITextChildProvider 的指導方針和慣例，包括屬性和方法的相關資訊。 TextChild 控制項模式可用來存取專案的最接近支援文字控制項模式的上階。
ms.assetid: B33BCBEF-9AD2-4A5A-871E-E97E69BE8195
keywords:
- 消費者介面自動化，執行 TextChild 控制項模式
- 消費者介面自動化，TextChild 控制項模式
- 消費者介面自動化、ITextChildProvider
- ITextChildProvider
- 執行消費者介面自動化 TextChild 控制項模式
- TextChild 控制項模式
- 控制項模式，ITextChildProvider
- 控制模式，消費者介面自動化執行 TextChild
- 控制項模式，TextChild
- 介面，ITextChildProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d21102abfef7cee0553850ac01c4f759f81988e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683021"
---
# <a name="textchild-control-pattern"></a><span data-ttu-id="cbd2d-114">TextChild 控制項模式</span><span class="sxs-lookup"><span data-stu-id="cbd2d-114">TextChild Control Pattern</span></span>

<span data-ttu-id="cbd2d-115">介紹執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider)的指導方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-115">Introduces guidelines and conventions for implementing [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider), including information about properties and methods.</span></span> <span data-ttu-id="cbd2d-116">**TextChild** 控制項模式可用來存取專案的最接近支援 [文字](uiauto-implementingtextandtextrange.md)控制項模式的上階。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-116">The **TextChild** control pattern is used to access an element’s nearest ancestor that supports the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>

<span data-ttu-id="cbd2d-117">例如，假設檔中的文字包含內嵌影像以及如下圖所示的超連結。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-117">For example, suppose text in a document contains an embedded image and a hyperlink as shown in the following image.</span></span>

![顯示包含內嵌影像和超連結之文字的螢幕擷取畫面](images/textchild-pattern.png)

<span data-ttu-id="cbd2d-119">如果您使用 Microsoft 消費者介面自動化工具來檢查這份檔內容的消費者介面自動化樹狀結構，它可能會顯示一個檔元素，其中包含代表影像的一個子項目，另一個代表超連結的子專案。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-119">If you use Microsoft UI Automation tools to examine the UI Automation tree for this document content, it might show a document element with one child element that represents the image, and another child element that represents the hyperlink.</span></span> <span data-ttu-id="cbd2d-120">例如：</span><span class="sxs-lookup"><span data-stu-id="cbd2d-120">For example:</span></span>

![顯示檢查報表範例 ui 自動化元素樹狀結構的螢幕擷取畫面](images/textchild-pattern-tree.png)

<span data-ttu-id="cbd2d-122">一般來說，上述範例中的 document 元素支援 [文字](uiauto-implementingtextandtextrange.md) 控制項模式，但 document 專案的兩個子系則不支援。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-122">Typically, the document element in the preceding example supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, but the two children of the document element do not.</span></span> <span data-ttu-id="cbd2d-123">如果消費者介面自動化用戶端應用程式有影像元素或超連結元素的參考，則用戶端可以使用 **TextChild** 控制項模式，以方便存取包含檔專案所公開的 Textcontrol 模式。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-123">If a UI Automation client application has a reference to the image element or hyperlink element, the client can use the **TextChild** control pattern as a convenient way to access the Textcontrol pattern exposed by the containing document element.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="cbd2d-124">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="cbd2d-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="cbd2d-125">在執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="cbd2d-125">When implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="cbd2d-126">[**ITextChildProvider：： TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer)屬性應指定最接近的上階元素，以支援 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)介面，不論上階鏈中較高的元素是否也支援 **ITextProvider**。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-126">The [**ITextChildProvider::TextContainer**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) property should specify the nearest ancestor element that supports [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) interface, regardless of whether elements higher in the ancestor chain also support **ITextProvider**.</span></span>
-   <span data-ttu-id="cbd2d-127">元素不應同時支援 [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) 和 [ITextChildProvider \* \*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-127">An element should not support both the [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) and the [ITextChildProvider\*\*](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>
- <span data-ttu-id="cbd2d-128">實 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 的專案必須是可執行 [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider)之專案的子系（或子項目）。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-128">An element that implements [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) must be a child, or descendent, of an element that implements [**ITextProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider).</span></span> <span data-ttu-id="cbd2d-129">此元素不需要同時執行 [文字控制項模式](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange)。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-129">It is not required that this element also implement the [Text control pattern](/windows/desktop/WinAuto/uiauto-implementingtextandtextrange).</span></span>
-   <span data-ttu-id="cbd2d-130">[**ITextChildProvider：： TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)屬性所指定的文字範圍必須與包含文字提供者專案所傳回的文字範圍相同，因為它的 [**ITextProvider：： RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild)函式是以文字子項目做為括住的子專案來呼叫時。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-130">The [**ITextChildProvider::TextRange**](/windows/win32/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange) property should specify the same text range as the one that the containing text provider element returns when its [**ITextProvider::RangeFromChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextprovider-rangefromchild) function is called with the text child element as the enclosed child element.</span></span>

## <a name="required-members-for-itextchildprovider"></a><span data-ttu-id="cbd2d-131">**ITextChildProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="cbd2d-131">Required Members for **ITextChildProvider**</span></span>

<span data-ttu-id="cbd2d-132">執行 [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) 介面時需要這些屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-132">These properties and methods are required for implementing the [**ITextChildProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextchildprovider) interface.</span></span>



| <span data-ttu-id="cbd2d-133">必要成員</span><span class="sxs-lookup"><span data-stu-id="cbd2d-133">Required members</span></span>                                                     | <span data-ttu-id="cbd2d-134">成員類型</span><span class="sxs-lookup"><span data-stu-id="cbd2d-134">Member type</span></span> | <span data-ttu-id="cbd2d-135">備註</span><span class="sxs-lookup"><span data-stu-id="cbd2d-135">Notes</span></span> |
|----------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="cbd2d-136">**TextContainer**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-136">**TextContainer**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textcontainer) | <span data-ttu-id="cbd2d-137">屬性</span><span class="sxs-lookup"><span data-stu-id="cbd2d-137">Property</span></span>    | <span data-ttu-id="cbd2d-138">無</span><span class="sxs-lookup"><span data-stu-id="cbd2d-138">None</span></span>  |
| [<span data-ttu-id="cbd2d-139">**TextRange**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-139">**TextRange**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextchildprovider-get_textrange)         | <span data-ttu-id="cbd2d-140">屬性</span><span class="sxs-lookup"><span data-stu-id="cbd2d-140">Property</span></span>    | <span data-ttu-id="cbd2d-141">無</span><span class="sxs-lookup"><span data-stu-id="cbd2d-141">None</span></span>  |



 

<span data-ttu-id="cbd2d-142">此控制項模式沒有任何相關聯的方法或事件。</span><span class="sxs-lookup"><span data-stu-id="cbd2d-142">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbd2d-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="cbd2d-143">Related topics</span></span>

<span data-ttu-id="cbd2d-144">**概念**</span><span class="sxs-lookup"><span data-stu-id="cbd2d-144">**Conceptual**</span></span>

- [<span data-ttu-id="cbd2d-145">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="cbd2d-145">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
- [<span data-ttu-id="cbd2d-146">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="cbd2d-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
- [<span data-ttu-id="cbd2d-147">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="cbd2d-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)