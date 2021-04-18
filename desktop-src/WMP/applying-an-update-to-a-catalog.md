---
title: 將更新套用至目錄
description: 將更新套用至目錄
ms.assetid: 4aedb0d6-36c7-425c-b6d3-e16161cf6828
keywords:
- Windows Media Player 線上商店，將更新套用至目錄
- 線上商店，將更新套用至目錄
- 輸入1個線上商店，將更新套用至目錄
- Windows Media Player 線上商店，更新目錄
- 線上商店，更新目錄
- 輸入1個線上商店，更新目錄
- Windows Media Player 線上商店、類別目錄更新
- 線上商店、類別目錄更新
- 輸入1個線上商店、類別目錄更新
- 目錄更新
- 更新目錄
- 將更新套用至目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d468edb7d09b8804fa924f7c31fc1be45d27c8fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968670"
---
# <a name="applying-an-update-to-a-catalog"></a><span data-ttu-id="fd27f-115">將更新套用至目錄</span><span class="sxs-lookup"><span data-stu-id="fd27f-115">Applying an Update To a Catalog</span></span>

> [!Note]  
> <span data-ttu-id="fd27f-116">這通常不是因為診斷用途而完成，例如有助於確認差異檔案是否有效。</span><span class="sxs-lookup"><span data-stu-id="fd27f-116">This is not normally done except for diagnostic purposes—for instance, to help verify that a difference file is valid.</span></span> <span data-ttu-id="fd27f-117">以這種方式產生的目錄不是壓縮格式，且不應該傳遞至 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="fd27f-117">The catalog generated in this way is not in compressed form and should not be passed to Windows Media Player.</span></span>

 

<span data-ttu-id="fd27f-118">您可以使用下列語法來建立新的類別目錄檔案，其中 *inputcatalog* 是原始目錄的位置，而 *inputdiff* 是要套用之差異檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="fd27f-118">A new catalog file can be created by using the syntax below, where *inputcatalog* is the location of the original catalog, and *inputdiff* is the location of the difference file to apply.</span></span> <span data-ttu-id="fd27f-119">類別目錄檔案必須是未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="fd27f-119">The catalog files must be in uncompressed form.</span></span>


```C++
catcomp applydiff <inputcatalog> <inputdiff>
```



<span data-ttu-id="fd27f-120">例如，下列程式會從 C： \\ Catalog210 \\ catalog. Wmdb 和 c： \\ Catalog210 catalog 建立新的目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="fd27f-120">For example, the following creates a new catalog from C:\\Catalog210\\catalog.wmdb and C:\\Catalog210\\catalog.diff.</span></span>


```C++
catcomp applydiff C:\Catalog210\catalog.wmdb C:\Catalog210\catalog.diff
```



<span data-ttu-id="fd27f-121">如果編譯成功，catcomp.exe 會建立下列輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="fd27f-121">If compilation is successful, catcomp.exe creates the follow output files.</span></span>



| <span data-ttu-id="fd27f-122">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="fd27f-122">File name</span></span>        | <span data-ttu-id="fd27f-123">描述</span><span class="sxs-lookup"><span data-stu-id="fd27f-123">Description</span></span>       |
|------------------|-------------------|
| <span data-ttu-id="fd27f-124">catalog. wmdb. new</span><span class="sxs-lookup"><span data-stu-id="fd27f-124">catalog.wmdb.new</span></span> | <span data-ttu-id="fd27f-125">新的類別目錄檔案。</span><span class="sxs-lookup"><span data-stu-id="fd27f-125">New catalog file.</span></span> |



 

 

 




