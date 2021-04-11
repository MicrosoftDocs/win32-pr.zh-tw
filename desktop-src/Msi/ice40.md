---
description: ICE40 會進行其他驗證。
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115756"
---
# <a name="ice40"></a><span data-ttu-id="1a27f-103">ICE40</span><span class="sxs-lookup"><span data-stu-id="1a27f-103">ICE40</span></span>

<span data-ttu-id="1a27f-104">ICE40 會進行其他驗證。</span><span class="sxs-lookup"><span data-stu-id="1a27f-104">ICE40 does miscellaneous validation.</span></span>

## <a name="result"></a><span data-ttu-id="1a27f-105">結果</span><span class="sxs-lookup"><span data-stu-id="1a27f-105">Result</span></span>

<span data-ttu-id="1a27f-106">ICE40 文章的警告如下：</span><span class="sxs-lookup"><span data-stu-id="1a27f-106">ICE40 posts warnings on the following:</span></span>

-   <span data-ttu-id="1a27f-107">已覆寫 [**REINSTALLMODE**](reinstallmode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1a27f-107">The [**REINSTALLMODE**](reinstallmode.md) property has been overridden.</span></span>
-   <span data-ttu-id="1a27f-108">[RemoveIniFile 資料表](removeinifile-table.md)有一個不含值的刪除標記專案。</span><span class="sxs-lookup"><span data-stu-id="1a27f-108">The [RemoveIniFile table](removeinifile-table.md) has a Delete Tag entry with no value.</span></span>
-   <span data-ttu-id="1a27f-109">.Msi 檔案遺漏 [錯誤資料表](error-table.md) ，且 [**頁面計數摘要**](page-count-summary.md) 屬性小於或等於100。</span><span class="sxs-lookup"><span data-stu-id="1a27f-109">The .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <span data-ttu-id="1a27f-110">這項 ICE 警告已淘汰，因為 Windows Installer 不需要套件具有錯誤資料表。</span><span class="sxs-lookup"><span data-stu-id="1a27f-110">This ICE warning is obsolete because Windows Installer does not require the package to have an Error table.</span></span> <span data-ttu-id="1a27f-111">您可以使用 Msimsg.dll 來取出錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1a27f-111">Error messages can be retrieved using Msimsg.dll.</span></span>

## <a name="example"></a><span data-ttu-id="1a27f-112">範例</span><span class="sxs-lookup"><span data-stu-id="1a27f-112">Example</span></span>

[<span data-ttu-id="1a27f-113">屬性工作表</span><span class="sxs-lookup"><span data-stu-id="1a27f-113">Property Table</span></span>](property-table.md)



| <span data-ttu-id="1a27f-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1a27f-114">Property</span></span>                               | <span data-ttu-id="1a27f-115">值</span><span class="sxs-lookup"><span data-stu-id="1a27f-115">Value</span></span> |
|----------------------------------------|-------|
| [<span data-ttu-id="1a27f-116">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="1a27f-116">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="1a27f-117">A</span><span class="sxs-lookup"><span data-stu-id="1a27f-117">A</span></span>     |



 

[<span data-ttu-id="1a27f-118">RemoveIniFile 資料表</span><span class="sxs-lookup"><span data-stu-id="1a27f-118">RemoveIniFile Table</span></span>](removeinifile-table.md)



| <span data-ttu-id="1a27f-119">RemoveIniFile</span><span class="sxs-lookup"><span data-stu-id="1a27f-119">RemoveIniFile</span></span>                          | <span data-ttu-id="1a27f-120">動作</span><span class="sxs-lookup"><span data-stu-id="1a27f-120">Action</span></span> | <span data-ttu-id="1a27f-121">值</span><span class="sxs-lookup"><span data-stu-id="1a27f-121">Value</span></span> |
|----------------------------------------|--------|-------|
| [<span data-ttu-id="1a27f-122">**REINSTALLMODE**</span><span class="sxs-lookup"><span data-stu-id="1a27f-122">**REINSTALLMODE**</span></span>](reinstallmode.md) | <span data-ttu-id="1a27f-123">4</span><span class="sxs-lookup"><span data-stu-id="1a27f-123">4</span></span>      |       |



 

## <a name="results"></a><span data-ttu-id="1a27f-124">結果</span><span class="sxs-lookup"><span data-stu-id="1a27f-124">Results</span></span>

<span data-ttu-id="1a27f-125">ICE40 會報告下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="1a27f-125">ICE40 would report the following errors.</span></span>



| <span data-ttu-id="1a27f-126">ICE40 錯誤</span><span class="sxs-lookup"><span data-stu-id="1a27f-126">ICE40 error</span></span>                                                                                           | <span data-ttu-id="1a27f-127">Description</span><span class="sxs-lookup"><span data-stu-id="1a27f-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a27f-128">[**REINSTALLMODE**](reinstallmode.md) 定義于屬性工作表中。</span><span class="sxs-lookup"><span data-stu-id="1a27f-128">[**REINSTALLMODE**](reinstallmode.md) is defined in the Property table.</span></span> <span data-ttu-id="1a27f-129">這可能會造成問題。</span><span class="sxs-lookup"><span data-stu-id="1a27f-129">This may cause difficulties.</span></span> | <span data-ttu-id="1a27f-130">在 .msi 檔案中定義 [**REINSTALLMODE**](reinstallmode.md) 屬性可能會導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="1a27f-130">Defining the [**REINSTALLMODE**](reinstallmode.md) property in .msi file can lead to unexpected behavior.</span></span> <span data-ttu-id="1a27f-131">若要修正這個錯誤，請不要定義這個屬性。</span><span class="sxs-lookup"><span data-stu-id="1a27f-131">To fix this error, do not define this property.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="1a27f-132">RemoveIniFile 專案 Remove1 必須有值，因為動作是「刪除標記」 (4) 。</span><span class="sxs-lookup"><span data-stu-id="1a27f-132">RemoveIniFile entry Remove1 must have a value, because the Action is "Delete Tag" (4).</span></span>                | <span data-ttu-id="1a27f-133">[RemoveIniFile 資料表](removeinifile-table.md)的 RemoveIniFile 資料行中有一個刪除標記動作，但沒有在 [值] 資料行中指定要刪除的標記。</span><span class="sxs-lookup"><span data-stu-id="1a27f-133">There is a Delete Tag action in the in the RemoveIniFile column of the [RemoveIniFile table](removeinifile-table.md) without specifying a tag to delete in the Value column.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="1a27f-134">遺漏錯誤資料表。</span><span class="sxs-lookup"><span data-stu-id="1a27f-134">Error Table is missing.</span></span> <span data-ttu-id="1a27f-135">只會產生數值錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1a27f-135">Only numerical error messages will be generated.</span></span>                              | <span data-ttu-id="1a27f-136">這項 ICE 警告已淘汰，因為 Windows Installer 不需要套件具有 [錯誤資料表](error-table.md)。</span><span class="sxs-lookup"><span data-stu-id="1a27f-136">This ICE warning is obsolete because Windows Installer does not require the package to have an [Error table](error-table.md).</span></span> <span data-ttu-id="1a27f-137">您可以使用 Msimsg.dll 來取出錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1a27f-137">Error messages can be retrieved using Msimsg.dll.</span></span><br/> <span data-ttu-id="1a27f-138">此警告表示 .msi 檔案遺漏 [錯誤資料表](error-table.md) ，且 [ [**頁面計數摘要**](page-count-summary.md) ] 屬性小於或等於100。</span><span class="sxs-lookup"><span data-stu-id="1a27f-138">This warning means that the .msi file is missing the [Error table](error-table.md) and the [**Page Count Summary**](page-count-summary.md) Property is less than or equal to 100.</span></span> <br/> <span data-ttu-id="1a27f-139">若要修正這個錯誤，請使用目前版本的 Windows Installer，或將錯誤資料表加入至安裝套件，並在 [訊息] 資料行中撰寫格式化範本以取得錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1a27f-139">To fix this error, use a current version of the Windows Installer, or add an Error table to the installation package and author formatting templates in the Message column for error messages.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1a27f-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="1a27f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a27f-141">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="1a27f-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




