---
description: ICE19 會驗證公告的元件是否參考元件資料表的 KeyPath 資料行中的檔案，以及公告的快捷方式是否參考此資料行中的目錄。
ms.assetid: 438153c1-bc4b-4ecf-ab85-d66ad69c987c
title: ICE19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a53aa3268a1c77f674d4a130c9de02c44b56243
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193489"
---
# <a name="ice19"></a><span data-ttu-id="7dc0b-103">ICE19</span><span class="sxs-lookup"><span data-stu-id="7dc0b-103">ICE19</span></span>

<span data-ttu-id="7dc0b-104">ICE19 會驗證公告的元件是否參考 [元件資料表](component-table.md) 的 KeyPath 資料行中的檔案，以及公告的快捷方式是否參考此資料行中的目錄。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-104">ICE19 validates that advertised components reference a file in the KeyPath column of the [Component table](component-table.md) and that an advertised shortcut references a directory in this column.</span></span>

<span data-ttu-id="7dc0b-105">ICE19 會驗證公告的元件或快捷方式是否有元件。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-105">ICE19 validates that advertised components or shortcuts have a ComponentId.</span></span> <span data-ttu-id="7dc0b-106">[PublishComponent 資料表](publishcomponent-table.md)中不是在另一個資料表中公告的元件，只會檢查其是否有一個元件。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-106">Components in the [PublishComponent table](publishcomponent-table.md), which are not advertised in another table, are only checked to see whether they have a ComponentId.</span></span>

## <a name="result"></a><span data-ttu-id="7dc0b-107">結果</span><span class="sxs-lookup"><span data-stu-id="7dc0b-107">Result</span></span>

<span data-ttu-id="7dc0b-108">如果在已公告的快捷方式中，如果元件資料表的 KeyPath 資料行未參考檔案或目錄，ICE19 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-108">ICE19 posts an error message if the KeyPath column of the Component table does not reference a file in the case of an advertised component or a directory in the case of an advertised shortcut.</span></span> <span data-ttu-id="7dc0b-109">如果任何公告的元件或快捷方式沒有元件，ICE19 會張貼錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-109">ICE19 posts an error message if any advertised components or shortcuts do not have a ComponentId.</span></span>

## <a name="example"></a><span data-ttu-id="7dc0b-110">範例</span><span class="sxs-lookup"><span data-stu-id="7dc0b-110">Example</span></span>

<span data-ttu-id="7dc0b-111">ICE19 會針對所顯示的範例張貼下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="7dc0b-111">ICE19 posts the following error messages for the example shown:</span></span>

-   <span data-ttu-id="7dc0b-112">擴充功能 flp 會參考元件 [資料表](component-table.md)中沒有指定元件的元件 Comp1。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-112">Extension flp references the component Comp1 which does not have a ComponentId specified in the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="7dc0b-113">擴充 exe 參考參考目錄作為其 KeyPath 的元件 Comp4。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-113">Extension exe references the component Comp4 which references a directory as its KeyPath.</span></span> <span data-ttu-id="7dc0b-114">元件資料表中的 KeyPath 為 Null。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-114">The KeyPath is Null in the Component table.</span></span>
-   <span data-ttu-id="7dc0b-115">快速鍵 Shortcut2 會參考參考登錄專案做為金鑰路徑的元件 Comp3。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-115">Shortcut Shortcut2 references the component Comp3 which references a Registry entry as the key path.</span></span> <span data-ttu-id="7dc0b-116">元件資料表中的 [屬性] 資料行值為4。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-116">The value of the Attributes column in the Component table is 4.</span></span>

<span data-ttu-id="7dc0b-117">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="7dc0b-117">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="7dc0b-118">元件</span><span class="sxs-lookup"><span data-stu-id="7dc0b-118">Component</span></span> | <span data-ttu-id="7dc0b-119">ComponentId</span><span class="sxs-lookup"><span data-stu-id="7dc0b-119">ComponentId</span></span>                            | <span data-ttu-id="7dc0b-120">屬性</span><span class="sxs-lookup"><span data-stu-id="7dc0b-120">Attributes</span></span> | <span data-ttu-id="7dc0b-121">KeyPath</span><span class="sxs-lookup"><span data-stu-id="7dc0b-121">KeyPath</span></span> |
|-----------|----------------------------------------|------------|---------|
| <span data-ttu-id="7dc0b-122">Comp1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-122">Comp1</span></span>     | <span data-ttu-id="7dc0b-123">Null</span><span class="sxs-lookup"><span data-stu-id="7dc0b-123">Null</span></span>                                   | <span data-ttu-id="7dc0b-124">0</span><span class="sxs-lookup"><span data-stu-id="7dc0b-124">0</span></span>          | <span data-ttu-id="7dc0b-125">File1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-125">File1</span></span>   |
| <span data-ttu-id="7dc0b-126">Comp2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-126">Comp2</span></span>     | {00000002-0003-0000-0000-624474736554} | <span data-ttu-id="7dc0b-127">0</span><span class="sxs-lookup"><span data-stu-id="7dc0b-127">0</span></span>          | <span data-ttu-id="7dc0b-128">File2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-128">File2</span></span>   |
| <span data-ttu-id="7dc0b-129">Comp3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-129">Comp3</span></span>     | {00000003-0003-0000-0000-624474736554} | <span data-ttu-id="7dc0b-130">4</span><span class="sxs-lookup"><span data-stu-id="7dc0b-130">4</span></span>          | <span data-ttu-id="7dc0b-131">Reg3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-131">Reg3</span></span>    |
| <span data-ttu-id="7dc0b-132">Comp4</span><span class="sxs-lookup"><span data-stu-id="7dc0b-132">Comp4</span></span>     | {00000004-0003-0000-0000-624474736554} | <span data-ttu-id="7dc0b-133">0</span><span class="sxs-lookup"><span data-stu-id="7dc0b-133">0</span></span>          | <span data-ttu-id="7dc0b-134">Null</span><span class="sxs-lookup"><span data-stu-id="7dc0b-134">Null</span></span>    |



 

<span data-ttu-id="7dc0b-135">[延伸模組資料表](extension-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="7dc0b-135">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="7dc0b-136">分機</span><span class="sxs-lookup"><span data-stu-id="7dc0b-136">Extension</span></span> | <span data-ttu-id="7dc0b-137">元件\_</span><span class="sxs-lookup"><span data-stu-id="7dc0b-137">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="7dc0b-138">flp</span><span class="sxs-lookup"><span data-stu-id="7dc0b-138">flp</span></span>       | <span data-ttu-id="7dc0b-139">Comp1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-139">Comp1</span></span>       |
| <span data-ttu-id="7dc0b-140">Tst</span><span class="sxs-lookup"><span data-stu-id="7dc0b-140">tst</span></span>       | <span data-ttu-id="7dc0b-141">Comp2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-141">Comp2</span></span>       |
| <span data-ttu-id="7dc0b-142">exe</span><span class="sxs-lookup"><span data-stu-id="7dc0b-142">exe</span></span>       | <span data-ttu-id="7dc0b-143">Comp4</span><span class="sxs-lookup"><span data-stu-id="7dc0b-143">Comp4</span></span>       |



 

<span data-ttu-id="7dc0b-144"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="7dc0b-144">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="7dc0b-145">快速鍵</span><span class="sxs-lookup"><span data-stu-id="7dc0b-145">Shortcut</span></span>  | <span data-ttu-id="7dc0b-146">元件\_</span><span class="sxs-lookup"><span data-stu-id="7dc0b-146">Component\_</span></span> | <span data-ttu-id="7dc0b-147">功能\_</span><span class="sxs-lookup"><span data-stu-id="7dc0b-147">Feature\_</span></span>      |
|-----------|-------------|----------------|
| <span data-ttu-id="7dc0b-148">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="7dc0b-148">Shortcut1</span></span> | <span data-ttu-id="7dc0b-149">Comp4</span><span class="sxs-lookup"><span data-stu-id="7dc0b-149">Comp4</span></span>       | <span data-ttu-id="7dc0b-150">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="7dc0b-150">ProductFeature</span></span> |
| <span data-ttu-id="7dc0b-151">Shortcut2</span><span class="sxs-lookup"><span data-stu-id="7dc0b-151">Shortcut2</span></span> | <span data-ttu-id="7dc0b-152">Comp3</span><span class="sxs-lookup"><span data-stu-id="7dc0b-152">Comp3</span></span>       | <span data-ttu-id="7dc0b-153">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="7dc0b-153">ProductFeature</span></span> |



 

<span data-ttu-id="7dc0b-154">[功能表](feature-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="7dc0b-154">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="7dc0b-155">功能</span><span class="sxs-lookup"><span data-stu-id="7dc0b-155">Feature</span></span>        |
|----------------|
| <span data-ttu-id="7dc0b-156">ProductFeature</span><span class="sxs-lookup"><span data-stu-id="7dc0b-156">ProductFeature</span></span> |



 

> [!Note]  
> <span data-ttu-id="7dc0b-157">如果延伸模組 flp 和 exe 都參考相同的元件，則開啟它們的 EXE 或 COM 伺服器必須相同。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-157">If the extension flp and exe both reference the same component, the EXE or COM server that opens them must be the same.</span></span> <span data-ttu-id="7dc0b-158">這個 EXE 通常是元件的 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-158">This EXE is normally the KeyPath for the Component.</span></span> <span data-ttu-id="7dc0b-159">針對 OFFICE，延伸模組檔和 xls 無法參考相同的元件，因為相同的 EXE 不會同時開啟這兩個延伸模組。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-159">For OFFICE, the extensions doc and xls cannot reference the same component because the same EXE does not open both extensions.</span></span> <span data-ttu-id="7dc0b-160">您需要 winword.exe 開啟檔副檔名，而且需要 excel.exe 來開啟 xls 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7dc0b-160">You need winword.exe to open doc extensions and you need excel.exe to open xls extensions.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7dc0b-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="7dc0b-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7dc0b-162">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="7dc0b-162">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



