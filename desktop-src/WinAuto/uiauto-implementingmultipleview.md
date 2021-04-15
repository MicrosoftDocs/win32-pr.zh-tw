---
title: MultipleView 控制項模式
description: 描述執行 IMultipleViewProvider 的方針和慣例，包括屬性和方法的相關資訊。
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- 消費者介面自動化，執行 MultipleView 控制項模式
- 消費者介面自動化，MultipleView 控制項模式
- 消費者介面自動化、IMultipleViewProvider
- IMultipleViewProvider
- 執行消費者介面自動化 MultipleView 控制項模式
- MultipleView 控制項模式
- 控制項模式，IMultipleViewProvider
- 控制模式，消費者介面自動化執行 MultipleView
- 控制項模式，MultipleView
- 介面，IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372333"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="af6e8-113">MultipleView 控制項模式</span><span class="sxs-lookup"><span data-stu-id="af6e8-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="af6e8-114">描述執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)的方針和慣例，包括屬性和方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="af6e8-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="af6e8-115">其他參考的連結列於主題的結尾。</span><span class="sxs-lookup"><span data-stu-id="af6e8-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="af6e8-116">**MultipleView** 控制項模式用來支援控制項，這些控制項可讓您在相同資訊或同一組子控制項的多個標記法之間切換。</span><span class="sxs-lookup"><span data-stu-id="af6e8-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="af6e8-117">可顯示多個視圖的控制項範例包括清單視圖 (可以將其內容顯示為縮圖。磚、圖示或詳細資料) 、Microsoft Excel 圖表 (圓形圖、線條、橫條圖、具有公式) 的儲存格值、Microsoft Word 檔 (一般、web 版面配置、列印配置、閱讀版面配置、大綱) 、Microsoft Outlook 行事曆 (年、月、周、日) 和 Microsoft Windows Media Player 的外觀。</span><span class="sxs-lookup"><span data-stu-id="af6e8-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="af6e8-118">支援哪些檢視會由控制項的開發人員決定，而且是每個控制項所特有。</span><span class="sxs-lookup"><span data-stu-id="af6e8-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="af6e8-119">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="af6e8-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="af6e8-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="af6e8-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="af6e8-121">**IMultipleViewProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="af6e8-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="af6e8-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="af6e8-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="af6e8-123">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="af6e8-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="af6e8-124">在執行 **MultipleView** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="af6e8-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="af6e8-125">如果容器與提供目前視圖的控制項不同，則也應該在管理目前視圖的容器上執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) 。</span><span class="sxs-lookup"><span data-stu-id="af6e8-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="af6e8-126">例如，Windows 檔案總管包含目前資料夾內容的清單控制項，而控制項的視圖是從 Windows 檔案總管應用程式進行管理。</span><span class="sxs-lookup"><span data-stu-id="af6e8-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="af6e8-127">可以排序內容的控制項不視為支援多種檢視。</span><span class="sxs-lookup"><span data-stu-id="af6e8-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="af6e8-128">檢視集合在執行個體之間必須完全相同。</span><span class="sxs-lookup"><span data-stu-id="af6e8-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="af6e8-129">視圖名稱必須適合用於文字轉換語音、盲文和其他人類可讀取的應用程式。</span><span class="sxs-lookup"><span data-stu-id="af6e8-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="af6e8-130">**IMultipleViewProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="af6e8-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="af6e8-131">執行 [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) 介面需要下列屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="af6e8-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="af6e8-132">必要成員</span><span class="sxs-lookup"><span data-stu-id="af6e8-132">Required members</span></span>                                                            | <span data-ttu-id="af6e8-133">成員類型</span><span class="sxs-lookup"><span data-stu-id="af6e8-133">Member type</span></span> | <span data-ttu-id="af6e8-134">備註</span><span class="sxs-lookup"><span data-stu-id="af6e8-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="af6e8-135">**CurrentView**</span><span class="sxs-lookup"><span data-stu-id="af6e8-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="af6e8-136">屬性</span><span class="sxs-lookup"><span data-stu-id="af6e8-136">Property</span></span>    | <span data-ttu-id="af6e8-137">無</span><span class="sxs-lookup"><span data-stu-id="af6e8-137">None</span></span>  |
| [<span data-ttu-id="af6e8-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="af6e8-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="af6e8-139">方法</span><span class="sxs-lookup"><span data-stu-id="af6e8-139">Method</span></span>      | <span data-ttu-id="af6e8-140">無</span><span class="sxs-lookup"><span data-stu-id="af6e8-140">None</span></span>  |
| [<span data-ttu-id="af6e8-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="af6e8-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="af6e8-142">方法</span><span class="sxs-lookup"><span data-stu-id="af6e8-142">Method</span></span>      | <span data-ttu-id="af6e8-143">無</span><span class="sxs-lookup"><span data-stu-id="af6e8-143">None</span></span>  |
| [<span data-ttu-id="af6e8-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="af6e8-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="af6e8-145">方法</span><span class="sxs-lookup"><span data-stu-id="af6e8-145">Method</span></span>      | <span data-ttu-id="af6e8-146">無</span><span class="sxs-lookup"><span data-stu-id="af6e8-146">None</span></span>  |



 

<span data-ttu-id="af6e8-147">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="af6e8-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af6e8-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="af6e8-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af6e8-149">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="af6e8-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="af6e8-150">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="af6e8-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="af6e8-151">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="af6e8-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="af6e8-152">ExpandCollapse 控制項模式</span><span class="sxs-lookup"><span data-stu-id="af6e8-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




