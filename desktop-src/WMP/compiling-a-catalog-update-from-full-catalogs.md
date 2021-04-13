---
title: 從完整目錄編譯目錄更新
description: 從完整目錄編譯目錄更新
ms.assetid: 046c0a01-0ad7-41b6-bad5-dcab953a3980
keywords:
- Windows Media Player 線上商店，編譯目錄
- 線上商店，編譯目錄
- 輸入1個線上商店，編譯目錄
- Windows Media Player 線上商店、類別目錄更新
- 線上商店、類別目錄更新
- 輸入1個線上商店、類別目錄更新
- Windows Media Player 線上商店、完整目錄
- 線上商店、完整目錄
- 輸入1個線上商店、完整目錄
- 編譯目錄
- 目錄更新
- 完整目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaa6d1bc0d3dbc4fefaffe1498be03259716a5e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314214"
---
# <a name="compiling-a-catalog-update-from-full-catalogs"></a><span data-ttu-id="3fa81-115">從完整目錄編譯目錄更新</span><span class="sxs-lookup"><span data-stu-id="3fa81-115">Compiling a Catalog Update from Full Catalogs</span></span>

<span data-ttu-id="3fa81-116">您可以使用下列語法來建立包含已編譯之類別目錄的兩個版本之間變更的目錄更新，其中 *path1* 是包含第一個目錄的目錄， *path2* 是包含第二個目錄的目錄，而且可以選擇性地包含 debug，以在畫面上顯示詳細的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="3fa81-116">A catalog update containing the changes between two versions of a compiled catalog can be created by using the syntax below, where *path1* is the directory containing the first catalog, *path2* is the directory containing the second catalog, and debug can be optionally included to display detailed error information on the screen.</span></span> <span data-ttu-id="3fa81-117">類別目錄檔案必須是未壓縮的格式—已編譯之目錄的檔案名會是 wmdb，而不是 wmdb. lz。</span><span class="sxs-lookup"><span data-stu-id="3fa81-117">The catalog files must be in uncompressed form—the file name of the compiled catalog would be catalog.wmdb, rather than catalog.wmdb.lz.</span></span>


```C++
catcomp diff <path1> <path2> [debug]
```



<span data-ttu-id="3fa81-118">例如，如果 C： \\ Catalog210 \\ 目錄包含完整編譯目錄的210版，而 c： \\ Catalog211 \\ 包含211版，則下列命令會建立一個差異檔案，其中包含兩個版本之間的變更：</span><span class="sxs-lookup"><span data-stu-id="3fa81-118">For example, if the C:\\Catalog210\\ directory contains version 210 of a full compiled catalog and C:\\Catalog211\\ contains version 211, the following command creates a difference file that contains the changes between the two versions:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\
```



<span data-ttu-id="3fa81-119">若要顯示詳細的錯誤資訊，您可以新增選擇性的 debug 參數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3fa81-119">To display detailed error information, you can add the optional debug parameter as follows:</span></span>


```C++
catcomp diff C:\Catalog210\ C:\Catalog211\ debug
```



<span data-ttu-id="3fa81-120">如果編譯成功，catcomp.exe 會建立如下所列的輸出檔案，並將它們儲存在包含第一個目錄的目錄中。</span><span class="sxs-lookup"><span data-stu-id="3fa81-120">If compilation is successful, catcomp.exe creates the output files listed below and saves them in the directory that contains the first catalog.</span></span>



| <span data-ttu-id="3fa81-121">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="3fa81-121">File name</span></span>             | <span data-ttu-id="3fa81-122">描述</span><span class="sxs-lookup"><span data-stu-id="3fa81-122">Description</span></span>                                                                                                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa81-123">目錄。差異</span><span class="sxs-lookup"><span data-stu-id="3fa81-123">catalog.diff</span></span>          | <span data-ttu-id="3fa81-124">未壓縮的已編譯差異檔案。</span><span class="sxs-lookup"><span data-stu-id="3fa81-124">Uncompressed compiled difference file.</span></span>                                                                                                                                                           |
| <span data-ttu-id="3fa81-125">catalog. lz</span><span class="sxs-lookup"><span data-stu-id="3fa81-125">catalog.diff.lz</span></span>       | <span data-ttu-id="3fa81-126">目錄更新檔案的壓縮版本。</span><span class="sxs-lookup"><span data-stu-id="3fa81-126">Compressed version of catalog update file.</span></span> <span data-ttu-id="3fa81-127">您的外掛程式可將此檔案的位置提供給 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)中的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="3fa81-127">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="3fa81-128">catalog. wmdb delta</span><span class="sxs-lookup"><span data-stu-id="3fa81-128">catalog.wmdb.delta</span></span>    | <span data-ttu-id="3fa81-129">中繼輸出檔。</span><span class="sxs-lookup"><span data-stu-id="3fa81-129">Intermediate output file.</span></span> <span data-ttu-id="3fa81-130">Windows Media Player 未使用</span><span class="sxs-lookup"><span data-stu-id="3fa81-130">Not used by Windows Media Player</span></span>                                                                                                                                       |
| <span data-ttu-id="3fa81-131">catalog. wmdb. 修改</span><span class="sxs-lookup"><span data-stu-id="3fa81-131">catalog.wmdb.modified</span></span> | <span data-ttu-id="3fa81-132">中繼輸出檔。</span><span class="sxs-lookup"><span data-stu-id="3fa81-132">Intermediate output file.</span></span> <span data-ttu-id="3fa81-133">Windows Media Player 未使用</span><span class="sxs-lookup"><span data-stu-id="3fa81-133">Not used by Windows Media Player</span></span>                                                                                                                                       |



 

 

 




