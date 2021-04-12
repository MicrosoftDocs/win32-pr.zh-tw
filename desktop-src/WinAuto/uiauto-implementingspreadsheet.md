---
title: 試算表控制項模式
description: 描述執行 ISpreadsheetProvider 的方針和慣例，包括方法的相關資訊。
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- 消費者介面自動化，執行試算表控制項模式
- 消費者介面自動化，試算表控制項模式
- 消費者介面自動化、ISpreadsheetProvider
- ISpreadsheetProvider
- 執行消費者介面自動化試算表控制項模式
- 試算表控制項模式
- 控制項模式，ISpreadsheetProvider
- 控制項模式，執行消費者介面自動化試算表
- 控制項模式，試算表
- 介面，ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315775"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="7f375-113">試算表控制項模式</span><span class="sxs-lookup"><span data-stu-id="7f375-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="7f375-114">描述執行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider)的方針和慣例，包括方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="7f375-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="7f375-115">其他參考的連結列於主題的結尾。</span><span class="sxs-lookup"><span data-stu-id="7f375-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="7f375-116">**試算表** 控制項模式是用來公開試算表或其他以方格為基礎之檔的內容。</span><span class="sxs-lookup"><span data-stu-id="7f375-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="7f375-117">**試算表** 控制項模式與 [方格](uiauto-implementinggrid.md)控制項模式緊密相關;執行 **試算表** 控制項模式的控制項也應該執行方格控制項模式。</span><span class="sxs-lookup"><span data-stu-id="7f375-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="7f375-118">控制項也可以執行 [Table](uiauto-implementingtable.md) 控制項模式（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="7f375-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="7f375-119">如需執行這些控制項模式的控制項範例，請參閱 [控制項類型及其支援的控制項模式](uiauto-controlpatternmapping.md)。</span><span class="sxs-lookup"><span data-stu-id="7f375-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="7f375-120">實作方針和慣例</span><span class="sxs-lookup"><span data-stu-id="7f375-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="7f375-121">在執行 **試算表** 控制項模式時，請注意下列方針和慣例：</span><span class="sxs-lookup"><span data-stu-id="7f375-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="7f375-122">如果試算表實行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) 介面，其儲存格必須實 [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) 介面。</span><span class="sxs-lookup"><span data-stu-id="7f375-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="7f375-123">[**ISpreadsheetProvider：： GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname)方法的目的，是要提供應用程式可能會以 **跳至標籤** 功能提供的相同流覽類型。</span><span class="sxs-lookup"><span data-stu-id="7f375-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="7f375-124">許多試算表程式都可讓特定的資料格獲得易記的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="7f375-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="7f375-125">**GetItemByName** 可讓用戶端根據其易記名稱查閱儲存格。</span><span class="sxs-lookup"><span data-stu-id="7f375-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="7f375-126">這個方法不應該抓取任何包含該名稱文字的資料格，因為結果可能會有極明確的混淆。</span><span class="sxs-lookup"><span data-stu-id="7f375-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="7f375-127">如果試算表程式允許相同試算表中的多個資料格具有相同的易記名稱或標籤，則不會定義 Microsoft 消費者介面自動化行為。</span><span class="sxs-lookup"><span data-stu-id="7f375-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="7f375-128">**ISpreadsheetProvider** 的必要成員</span><span class="sxs-lookup"><span data-stu-id="7f375-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="7f375-129">以下是執行 [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) 介面的必要方法。</span><span class="sxs-lookup"><span data-stu-id="7f375-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="7f375-130">必要成員</span><span class="sxs-lookup"><span data-stu-id="7f375-130">Required members</span></span>                                                       | <span data-ttu-id="7f375-131">成員類型</span><span class="sxs-lookup"><span data-stu-id="7f375-131">Member type</span></span> | <span data-ttu-id="7f375-132">備註</span><span class="sxs-lookup"><span data-stu-id="7f375-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="7f375-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="7f375-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="7f375-134">方法</span><span class="sxs-lookup"><span data-stu-id="7f375-134">Method</span></span>      | <span data-ttu-id="7f375-135">無</span><span class="sxs-lookup"><span data-stu-id="7f375-135">None</span></span>  |



 

<span data-ttu-id="7f375-136">此控制項模式沒有任何相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="7f375-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f375-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f375-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f375-138">控制項類型及其支援的控制項模式</span><span class="sxs-lookup"><span data-stu-id="7f375-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="7f375-139">UI 自動化控制項模式概觀</span><span class="sxs-lookup"><span data-stu-id="7f375-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="7f375-140">UI 自動化樹狀目錄概觀</span><span class="sxs-lookup"><span data-stu-id="7f375-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 