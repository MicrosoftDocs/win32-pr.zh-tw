---
title: SpreadsheetItem 控制項模式
description: 描述執行 ISpreadsheetItemProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- 消費者介面自動化，執行 SpreadsheetItem 控制項模式
- 消費者介面自動化，SpreadsheetItem 控制項模式
- 消費者介面自動化、ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- 執行消費者介面自動化 SpreadsheetItem 控制項模式
- SpreadsheetItem 控制項模式
- 控制項模式，ISpreadsheetItemProvider
- 控制模式，消費者介面自動化執行 SpreadsheetItem
- 控制項模式，SpreadsheetItem
- 介面，ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023964"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="294af-113">SpreadsheetItem 控制項模式</span><span class="sxs-lookup"><span data-stu-id="294af-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="294af-114">描述執行 [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="294af-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="294af-115">**SpreadsheetItem** 控制項模式是用來公開試算表或其他以方格為基礎之檔中的儲存格屬性。</span><span class="sxs-lookup"><span data-stu-id="294af-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="294af-116">**SpreadsheetItem** 控制項模式與 [GridItem](uiauto-implementinggriditem.md)控制項模式緊密相關;實 **SpreadsheetItem** 控制項模式的控制項也應執行 GridItem 控制項模式。</span><span class="sxs-lookup"><span data-stu-id="294af-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="294af-117">控制項也可以執行 [TableItem](uiauto-implementingtableitem.md) 控制項模式（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="294af-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="294af-118">如需執行這些控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="294af-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="294af-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="294af-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="294af-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="294af-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="294af-121">**ISpreadsheetItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="294af-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="294af-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="294af-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="294af-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="294af-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="294af-124">在執行 **SpreadsheetItem** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="294af-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="294af-125">在執行 [**ISpreadsheetItemProvider：： GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) 和 [**ISpreadsheetItemProvider：： GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) 方法時，請參閱 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 檔。</span><span class="sxs-lookup"><span data-stu-id="294af-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="294af-126">這些方法都會傳回陣列，讓提供者支援單一資料格上的多個批註。</span><span class="sxs-lookup"><span data-stu-id="294af-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="294af-127">某些類型的注釋不需要完整執行 [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="294af-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="294af-128">例如，可以藉由讓 [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) 傳回 [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)的文字屬性識別碼，並讓 [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) 傳回 null 值，來表示簡單的拼寫錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="294af-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="294af-129">**ISpreadsheetItemProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="294af-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="294af-130">執行 [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="294af-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="294af-131">必要成員</span><span class="sxs-lookup"><span data-stu-id="294af-131">Required members</span></span>                                                                         | <span data-ttu-id="294af-132">成員類型</span><span class="sxs-lookup"><span data-stu-id="294af-132">Member type</span></span> | <span data-ttu-id="294af-133">備註</span><span class="sxs-lookup"><span data-stu-id="294af-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="294af-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="294af-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="294af-135">屬性</span><span class="sxs-lookup"><span data-stu-id="294af-135">Property</span></span>    | <span data-ttu-id="294af-136">因為資料格的 [Value](value-property.md)屬性通常會傳回資料格的計算值，所以必須執行個別的 [**公式**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)屬性。</span><span class="sxs-lookup"><span data-stu-id="294af-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="294af-137">如果未設定任何公式， **公式** 屬性應為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="294af-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="294af-138">**GetAnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="294af-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="294af-139">方法</span><span class="sxs-lookup"><span data-stu-id="294af-139">Method</span></span>      | <span data-ttu-id="294af-140">傳回專案提供者的陣列，這些提供者會參考連結至此儲存格的批註。</span><span class="sxs-lookup"><span data-stu-id="294af-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="294af-141">如果批註沒有連結的提供者，陣列內的指標可以是 null。</span><span class="sxs-lookup"><span data-stu-id="294af-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="294af-142">**GetAnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="294af-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="294af-143">方法</span><span class="sxs-lookup"><span data-stu-id="294af-143">Method</span></span>      | <span data-ttu-id="294af-144">傳回批註類型識別碼的陣列，描述此資料格上的批註。</span><span class="sxs-lookup"><span data-stu-id="294af-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="294af-145">陣列的大小必須與 [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects)所傳回的陣列相同。</span><span class="sxs-lookup"><span data-stu-id="294af-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="294af-146">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="294af-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="294af-147">相關主題</span><span class="sxs-lookup"><span data-stu-id="294af-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="294af-148">**概念**</span><span class="sxs-lookup"><span data-stu-id="294af-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="294af-149">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="294af-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="294af-150">試算表控制項模式</span><span class="sxs-lookup"><span data-stu-id="294af-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="294af-151">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="294af-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="294af-152">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="294af-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 