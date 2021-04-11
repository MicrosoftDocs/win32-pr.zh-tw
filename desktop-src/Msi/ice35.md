---
description: ICE35 會驗證封裝含儲存在封包檔中壓縮檔案的元件，不會設定為從來源執行。 在 Windows Installer 2.0 或更新版本中，已移除此限制。
ms.assetid: b4df27e2-9790-4b18-a173-25fa8b0ecd4d
title: ICE35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea6a98079d3c57e0c796332cf0cd5f11045a07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944534"
---
# <a name="ice35"></a><span data-ttu-id="78053-104">ICE35</span><span class="sxs-lookup"><span data-stu-id="78053-104">ICE35</span></span>

<span data-ttu-id="78053-105">ICE35 會驗證封裝含儲存在封 [包](cabinet-files.md) 檔中壓縮檔案的元件，不會設定為從來源執行。</span><span class="sxs-lookup"><span data-stu-id="78053-105">ICE35 validates that components containing compressed files stored in a [cabinet file](cabinet-files.md) are not set to run from source.</span></span> <span data-ttu-id="78053-106">在 Windows Installer 2.0 或更新版本中，已移除此限制。</span><span class="sxs-lookup"><span data-stu-id="78053-106">With Windows Installer 2.0 or later, this restriction has been removed.</span></span>

<span data-ttu-id="78053-107">ICE35 會查詢 [媒體資料表](media-table.md) 的 [封包] 資料行，以判斷壓縮並儲存在封包檔中的檔案。</span><span class="sxs-lookup"><span data-stu-id="78053-107">ICE35 queries the Cabinet column of the [Media table](media-table.md) to determine which files are compressed and stored in a cabinet file.</span></span> <span data-ttu-id="78053-108">它會查詢檔案 [資料表](file-table.md) ，以判斷哪些元件包含這些檔案。</span><span class="sxs-lookup"><span data-stu-id="78053-108">It queries the [File table](file-table.md) to determine which components contain these files.</span></span> <span data-ttu-id="78053-109">最後，它會檢查 [元件資料表](component-table.md) ，以判斷是否已在 [屬性] 資料行中設定從來源執行的位。</span><span class="sxs-lookup"><span data-stu-id="78053-109">Finally, it checks the [Component table](component-table.md) to determine whether the run-from-source bits are set in the Attributes column.</span></span>

## <a name="result"></a><span data-ttu-id="78053-110">結果</span><span class="sxs-lookup"><span data-stu-id="78053-110">Result</span></span>

<span data-ttu-id="78053-111">如果有壓縮檔案儲存在屬於元件 [資料表](component-table.md)之 [屬性] 資料行中的 msidbComponentAttributesSourceOnly 位元件的元件，ICE35 會張貼一則錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="78053-111">ICE35 posts an error message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesSourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="78053-112">在 Windows Installer 2.0 或更新版本中，這會從錯誤變更為警告訊息。</span><span class="sxs-lookup"><span data-stu-id="78053-112">With Windows Installer 2.0 or later, this is changed from an error to a warning message.</span></span> <span data-ttu-id="78053-113">僅支援 Windows Installer 2.0 和更新版本的封裝，會將 \_ 摘要資訊資料流程的 PID PAGECOUNT 屬性設定為至少200的值。</span><span class="sxs-lookup"><span data-stu-id="78053-113">A package that supports only Windows Installer 2.0 and later has the PID\_PAGECOUNT property of the Summary Information Stream set to a value of at least 200.</span></span>

<span data-ttu-id="78053-114">如果有壓縮檔案儲存在屬於元件 [資料表](component-table.md)之 [屬性] 資料行中的 msidbComponentAttributesOptional 位元件的元件，ICE35 會張貼警告訊息。</span><span class="sxs-lookup"><span data-stu-id="78053-114">ICE35 posts warning message if there is a compressed file stored in a cabinet file belonging to a component with the msidbComponentAttributesOptional bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="78053-115">Windows Installer 2.0 和更新版本已移除此警告訊息。</span><span class="sxs-lookup"><span data-stu-id="78053-115">This warning message has been removed with Windows Installer 2.0 and later.</span></span>

<span data-ttu-id="78053-116">如果元件中的多個檔案位於封包檔中，ICE35 會針對每個已設定從來源位執行的檔案報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="78053-116">If multiple files in a component are in a cabinet file, ICE35 reports errors for each file that has the run from source bit set.</span></span>

## <a name="example"></a><span data-ttu-id="78053-117">範例</span><span class="sxs-lookup"><span data-stu-id="78053-117">Example</span></span>

<span data-ttu-id="78053-118">ICE35 會針對使用早于 Windows Installer 2.0 版的版本，報告下列範例的錯誤和警告。</span><span class="sxs-lookup"><span data-stu-id="78053-118">ICE35 reports the following errors and warnings for the example shown using a version earlier than Windows Installer version 2.0.</span></span>



| <span data-ttu-id="78053-119">ICE35 錯誤</span><span class="sxs-lookup"><span data-stu-id="78053-119">ICE35 Error</span></span>                                                                                                | <span data-ttu-id="78053-120">Description</span><span class="sxs-lookup"><span data-stu-id="78053-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78053-121">錯誤：無法從來源執行元件 Component3，因為它的成員檔案 ' File3 ' 已壓縮。</span><span class="sxs-lookup"><span data-stu-id="78053-121">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="78053-122">壓縮檔案儲存在封包檔中，且此檔案屬於 [元件資料表](component-table.md)的 [屬性] 資料行中設定 SourceOnly 位的元件。</span><span class="sxs-lookup"><span data-stu-id="78053-122">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="78053-123">若要修正這個錯誤，請將 Component2's 屬性值的較低2位變更為 "00" （表示僅限本機），或從 CAB 檔案中移除 File4。</span><span class="sxs-lookup"><span data-stu-id="78053-123">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="78053-124">錯誤：無法從來源執行元件 Component3，因為它的成員檔案 ' File3 ' 已壓縮。</span><span class="sxs-lookup"><span data-stu-id="78053-124">ERROR: Component Component3 cannot be Run From Source only, because its member file 'File3' is compressed.</span></span> | <span data-ttu-id="78053-125">壓縮檔案儲存在封包檔中，且此檔案屬於 [元件資料表](component-table.md)的 [屬性] 資料行中設定 SourceOnly 位的元件。</span><span class="sxs-lookup"><span data-stu-id="78053-125">There is a compressed file stored in a cabinet file and this file belongs to a component with the SourceOnly bit set in the Attributes column of the [Component table](component-table.md).</span></span> <span data-ttu-id="78053-126">由於元件中的檔案並不是來自相同的媒體，因此 ICE35 會針對封包中的元件中的每個檔案報告錯誤。</span><span class="sxs-lookup"><span data-stu-id="78053-126">Because the files in a component do not all have to originate from the same media, ICE35 reports errors for each file in the component that is in a cabinet.</span></span><br/> <span data-ttu-id="78053-127">若要修正這個錯誤，請將 Component2's 屬性值的較低2位變更為 "00" （表示僅限本機），或從 CAB 檔案中移除 File4。</span><span class="sxs-lookup"><span data-stu-id="78053-127">To fix this error change the lower 2 bits of Component2's Attributes value to "00", meaning Local only, or remove File4 from the CAB file.</span></span><br/> |



 

<span data-ttu-id="78053-128">[媒體資料表](media-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="78053-128">[Media Table](media-table.md) (partial)</span></span>



| <span data-ttu-id="78053-129">DiskID</span><span class="sxs-lookup"><span data-stu-id="78053-129">DiskID</span></span> | <span data-ttu-id="78053-130">LastSequence</span><span class="sxs-lookup"><span data-stu-id="78053-130">LastSequence</span></span> | <span data-ttu-id="78053-131">內閣</span><span class="sxs-lookup"><span data-stu-id="78053-131">Cabinet</span></span>   |
|--------|--------------|-----------|
| <span data-ttu-id="78053-132">1</span><span class="sxs-lookup"><span data-stu-id="78053-132">1</span></span>      | <span data-ttu-id="78053-133">2</span><span class="sxs-lookup"><span data-stu-id="78053-133">2</span></span>            |           |
| <span data-ttu-id="78053-134">2</span><span class="sxs-lookup"><span data-stu-id="78053-134">2</span></span>      | <span data-ttu-id="78053-135">4</span><span class="sxs-lookup"><span data-stu-id="78053-135">4</span></span>            | <span data-ttu-id="78053-136">One.cab</span><span class="sxs-lookup"><span data-stu-id="78053-136">One.cab</span></span>   |
| <span data-ttu-id="78053-137">3</span><span class="sxs-lookup"><span data-stu-id="78053-137">3</span></span>      | <span data-ttu-id="78053-138">5</span><span class="sxs-lookup"><span data-stu-id="78053-138">5</span></span>            | <span data-ttu-id="78053-139">\#Two.cab</span><span class="sxs-lookup"><span data-stu-id="78053-139">\#Two.cab</span></span> |



 

<span data-ttu-id="78053-140">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="78053-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="78053-141">檔案</span><span class="sxs-lookup"><span data-stu-id="78053-141">File</span></span>  | <span data-ttu-id="78053-142">元件\_</span><span class="sxs-lookup"><span data-stu-id="78053-142">Component\_</span></span> | <span data-ttu-id="78053-143">順序</span><span class="sxs-lookup"><span data-stu-id="78053-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="78053-144">File1</span><span class="sxs-lookup"><span data-stu-id="78053-144">File1</span></span> | <span data-ttu-id="78053-145">Component1</span><span class="sxs-lookup"><span data-stu-id="78053-145">Component1</span></span>  | <span data-ttu-id="78053-146">1</span><span class="sxs-lookup"><span data-stu-id="78053-146">1</span></span>        |
| <span data-ttu-id="78053-147">File2</span><span class="sxs-lookup"><span data-stu-id="78053-147">File2</span></span> | <span data-ttu-id="78053-148">Component2</span><span class="sxs-lookup"><span data-stu-id="78053-148">Component2</span></span>  | <span data-ttu-id="78053-149">2</span><span class="sxs-lookup"><span data-stu-id="78053-149">2</span></span>        |
| <span data-ttu-id="78053-150">File3</span><span class="sxs-lookup"><span data-stu-id="78053-150">File3</span></span> | <span data-ttu-id="78053-151">Component2</span><span class="sxs-lookup"><span data-stu-id="78053-151">Component2</span></span>  | <span data-ttu-id="78053-152">3</span><span class="sxs-lookup"><span data-stu-id="78053-152">3</span></span>        |
| <span data-ttu-id="78053-153">File4</span><span class="sxs-lookup"><span data-stu-id="78053-153">File4</span></span> | <span data-ttu-id="78053-154">Component3</span><span class="sxs-lookup"><span data-stu-id="78053-154">Component3</span></span>  | <span data-ttu-id="78053-155">4</span><span class="sxs-lookup"><span data-stu-id="78053-155">4</span></span>        |
| <span data-ttu-id="78053-156">File5</span><span class="sxs-lookup"><span data-stu-id="78053-156">File5</span></span> | <span data-ttu-id="78053-157">Component3</span><span class="sxs-lookup"><span data-stu-id="78053-157">Component3</span></span>  | <span data-ttu-id="78053-158">5</span><span class="sxs-lookup"><span data-stu-id="78053-158">5</span></span>        |



 

<span data-ttu-id="78053-159">[元件資料表](component-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="78053-159">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="78053-160">元件</span><span class="sxs-lookup"><span data-stu-id="78053-160">Component</span></span>  | <span data-ttu-id="78053-161">屬性</span><span class="sxs-lookup"><span data-stu-id="78053-161">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="78053-162">Component1</span><span class="sxs-lookup"><span data-stu-id="78053-162">Component1</span></span> | <span data-ttu-id="78053-163">0</span><span class="sxs-lookup"><span data-stu-id="78053-163">0</span></span>          |
| <span data-ttu-id="78053-164">Component2</span><span class="sxs-lookup"><span data-stu-id="78053-164">Component2</span></span> | <span data-ttu-id="78053-165">2</span><span class="sxs-lookup"><span data-stu-id="78053-165">2</span></span>          |
| <span data-ttu-id="78053-166">Component3</span><span class="sxs-lookup"><span data-stu-id="78053-166">Component3</span></span> | <span data-ttu-id="78053-167">1</span><span class="sxs-lookup"><span data-stu-id="78053-167">1</span></span>          |



 

<span data-ttu-id="78053-168"> (部分) 的[快捷方式資料表](shortcut-table.md)</span><span class="sxs-lookup"><span data-stu-id="78053-168">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="78053-169">快速鍵</span><span class="sxs-lookup"><span data-stu-id="78053-169">Shortcut</span></span>  | <span data-ttu-id="78053-170">圖示\_</span><span class="sxs-lookup"><span data-stu-id="78053-170">Icon\_</span></span> |
|-----------|--------|
| <span data-ttu-id="78053-171">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="78053-171">Shortcut1</span></span> | <span data-ttu-id="78053-172">Icon2</span><span class="sxs-lookup"><span data-stu-id="78053-172">Icon2</span></span>  |



 

<span data-ttu-id="78053-173">請注意，您也可以使用 [摘要資訊資料流程](summary-information-stream.md)的 [[**字數統計摘要**](word-count-summary.md)] 屬性，將檔案標示為已壓縮。</span><span class="sxs-lookup"><span data-stu-id="78053-173">Note that files can also be marked as compressed using the [**Word Count Summary**](word-count-summary.md) Property of the [Summary Information stream](summary-information-stream.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="78053-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="78053-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78053-175">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="78053-175">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




