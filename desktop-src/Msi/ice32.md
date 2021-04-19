---
description: ICE32 會驗證 .msi 檔案中的索引鍵和外鍵的大小和資料行定義類型是否相同。
ms.assetid: cc488ec5-e17a-4829-9763-38ba3c33bfde
title: ICE32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d6ff9e4de592ac073050b357aff0c63d984f0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980365"
---
# <a name="ice32"></a><span data-ttu-id="593f9-103">ICE32</span><span class="sxs-lookup"><span data-stu-id="593f9-103">ICE32</span></span>

<span data-ttu-id="593f9-104">ICE32 會驗證 .msi 檔案中的索引鍵和外鍵的大小和資料行定義類型是否相同。</span><span class="sxs-lookup"><span data-stu-id="593f9-104">ICE32 validates that keys and foreign keys in the .msi file are of the same size and column definition types.</span></span> <span data-ttu-id="593f9-105">這個 ICE 自訂動作會使用 [ \_ 驗證資料表](-validation-table.md)來進行比較，並使用 [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo)所傳回的定義類型。</span><span class="sxs-lookup"><span data-stu-id="593f9-105">This ICE custom action makes the comparison using the [\_Validation table](-validation-table.md) and using the definition types that are returned by [**MsiViewGetColumnInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgetcolumninfo).</span></span> <span data-ttu-id="593f9-106">如需詳細資訊，請參閱資料 [行定義格式](column-definition-format.md)。</span><span class="sxs-lookup"><span data-stu-id="593f9-106">For more information, see [Column Definition Format](column-definition-format.md).</span></span>

## <a name="result"></a><span data-ttu-id="593f9-107">結果</span><span class="sxs-lookup"><span data-stu-id="593f9-107">Result</span></span>

<span data-ttu-id="593f9-108">如果 .msi 檔案包含不同資料行長度或資料行資料類型之索引鍵的任何外鍵，則 ICE32 文章錯誤。</span><span class="sxs-lookup"><span data-stu-id="593f9-108">ICE32 posts errors if the .msi file contains any foreign keys to keys of a different column length or column data type.</span></span>

## <a name="example"></a><span data-ttu-id="593f9-109">範例</span><span class="sxs-lookup"><span data-stu-id="593f9-109">Example</span></span>

<span data-ttu-id="593f9-110">ICE32 會針對所顯示的範例張貼兩個錯誤：</span><span class="sxs-lookup"><span data-stu-id="593f9-110">ICE32 posts two errors for the example shown:</span></span>

-   <span data-ttu-id="593f9-111">有一個定義的外鍵和索引鍵大小不同。</span><span class="sxs-lookup"><span data-stu-id="593f9-111">There is a foreign key and key defined that differ in size.</span></span>
-   <span data-ttu-id="593f9-112">定義的外鍵和索引鍵在其定義類型中有所差異。</span><span class="sxs-lookup"><span data-stu-id="593f9-112">There is a foreign key and key defined that differ in their definition type.</span></span>

<span data-ttu-id="593f9-113">[ \_ 驗證資料表](-validation-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="593f9-113">[\_Validation Table](-validation-table.md) (partial)</span></span>



| <span data-ttu-id="593f9-114">資料表</span><span class="sxs-lookup"><span data-stu-id="593f9-114">Table</span></span> | <span data-ttu-id="593f9-115">資料行</span><span class="sxs-lookup"><span data-stu-id="593f9-115">Column</span></span>  | <span data-ttu-id="593f9-116">KeyTable</span><span class="sxs-lookup"><span data-stu-id="593f9-116">KeyTable</span></span> | <span data-ttu-id="593f9-117">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="593f9-117">KeyColumn</span></span> |
|-------|---------|----------|-----------|
| <span data-ttu-id="593f9-118">檔案</span><span class="sxs-lookup"><span data-stu-id="593f9-118">File</span></span>  | <span data-ttu-id="593f9-119">版本</span><span class="sxs-lookup"><span data-stu-id="593f9-119">Version</span></span> | <span data-ttu-id="593f9-120">檔案</span><span class="sxs-lookup"><span data-stu-id="593f9-120">File</span></span>     | <span data-ttu-id="593f9-121">1</span><span class="sxs-lookup"><span data-stu-id="593f9-121">1</span></span>         |
| <span data-ttu-id="593f9-122">皮 瓣</span><span class="sxs-lookup"><span data-stu-id="593f9-122">Flap</span></span>  | <span data-ttu-id="593f9-123">Column8</span><span class="sxs-lookup"><span data-stu-id="593f9-123">Column8</span></span> | <span data-ttu-id="593f9-124">皮 瓣</span><span class="sxs-lookup"><span data-stu-id="593f9-124">Flap</span></span>     | <span data-ttu-id="593f9-125">1</span><span class="sxs-lookup"><span data-stu-id="593f9-125">1</span></span>         |



 

<span data-ttu-id="593f9-126"> (部分) 的資料行定義</span><span class="sxs-lookup"><span data-stu-id="593f9-126">Column Definitions (partial)</span></span>



| <span data-ttu-id="593f9-127">資料表</span><span class="sxs-lookup"><span data-stu-id="593f9-127">Table</span></span> | <span data-ttu-id="593f9-128">資料行</span><span class="sxs-lookup"><span data-stu-id="593f9-128">Column</span></span>  | <span data-ttu-id="593f9-129">類型</span><span class="sxs-lookup"><span data-stu-id="593f9-129">Type</span></span> | <span data-ttu-id="593f9-130">大小</span><span class="sxs-lookup"><span data-stu-id="593f9-130">Size</span></span> |
|-------|---------|------|------|
| <span data-ttu-id="593f9-131">檔案</span><span class="sxs-lookup"><span data-stu-id="593f9-131">File</span></span>  | <span data-ttu-id="593f9-132">檔案</span><span class="sxs-lookup"><span data-stu-id="593f9-132">File</span></span>    | <span data-ttu-id="593f9-133">s</span><span class="sxs-lookup"><span data-stu-id="593f9-133">s</span></span>    | <span data-ttu-id="593f9-134">72</span><span class="sxs-lookup"><span data-stu-id="593f9-134">72</span></span>   |
| <span data-ttu-id="593f9-135">檔案</span><span class="sxs-lookup"><span data-stu-id="593f9-135">File</span></span>  | <span data-ttu-id="593f9-136">版本</span><span class="sxs-lookup"><span data-stu-id="593f9-136">Version</span></span> | <span data-ttu-id="593f9-137">S</span><span class="sxs-lookup"><span data-stu-id="593f9-137">S</span></span>    | <span data-ttu-id="593f9-138">32</span><span class="sxs-lookup"><span data-stu-id="593f9-138">32</span></span>   |
| <span data-ttu-id="593f9-139">皮 瓣</span><span class="sxs-lookup"><span data-stu-id="593f9-139">Flap</span></span>  | <span data-ttu-id="593f9-140">資料行1</span><span class="sxs-lookup"><span data-stu-id="593f9-140">Column1</span></span> | <span data-ttu-id="593f9-141">i</span><span class="sxs-lookup"><span data-stu-id="593f9-141">i</span></span>    | <span data-ttu-id="593f9-142">2</span><span class="sxs-lookup"><span data-stu-id="593f9-142">2</span></span>    |
| <span data-ttu-id="593f9-143">皮 瓣</span><span class="sxs-lookup"><span data-stu-id="593f9-143">Flap</span></span>  | <span data-ttu-id="593f9-144">Column8</span><span class="sxs-lookup"><span data-stu-id="593f9-144">Column8</span></span> | <span data-ttu-id="593f9-145">S</span><span class="sxs-lookup"><span data-stu-id="593f9-145">S</span></span>    | <span data-ttu-id="593f9-146">32</span><span class="sxs-lookup"><span data-stu-id="593f9-146">32</span></span>   |



 

<span data-ttu-id="593f9-147">File 資料表的 [版本] 資料行可以是檔案資料表中另一個檔案的外鍵。</span><span class="sxs-lookup"><span data-stu-id="593f9-147">The Version column of the File table can be a foreign key to another file in the File table.</span></span> <span data-ttu-id="593f9-148">這會發生在隨附的檔案中。</span><span class="sxs-lookup"><span data-stu-id="593f9-148">This occurs with companion files.</span></span> <span data-ttu-id="593f9-149">但是，Version 資料行只允許字串長度為32，而 File 資料行允許字串長度為72。</span><span class="sxs-lookup"><span data-stu-id="593f9-149">However, the Version column only allows a string length 32, whereas the File column allows a string length 72.</span></span> <span data-ttu-id="593f9-150">若要修正這個錯誤，請將字串長度變更為相符。</span><span class="sxs-lookup"><span data-stu-id="593f9-150">To fix this error change the string lengths to match.</span></span>

<span data-ttu-id="593f9-151">定義的外鍵和索引鍵在其定義類型中有所差異。</span><span class="sxs-lookup"><span data-stu-id="593f9-151">There is a foreign key and key defined that differ in their definition types.</span></span> <span data-ttu-id="593f9-152">傳動表的 Column8 會列為 Column1 的外鍵。</span><span class="sxs-lookup"><span data-stu-id="593f9-152">Column8 of the Flap Table is listed as a foreign key to Column1.</span></span> <span data-ttu-id="593f9-153">Column8 是一個字串資料行，而 Column1 是一個整數資料行。</span><span class="sxs-lookup"><span data-stu-id="593f9-153">Column8 is a string column and Column1 is an integer column.</span></span> <span data-ttu-id="593f9-154">必須定義外鍵和索引鍵組，使其資料類型相符。</span><span class="sxs-lookup"><span data-stu-id="593f9-154">The foreign key and key pairs must be defined so that their data types match.</span></span>

## <a name="related-topics"></a><span data-ttu-id="593f9-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="593f9-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="593f9-156">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="593f9-156">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



