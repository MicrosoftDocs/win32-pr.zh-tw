---
title: 從 TSV 檔案編譯完整目錄
description: 從 TSV 檔案編譯完整目錄
ms.assetid: fba80b32-dc78-4c4a-a351-e8786f9a7131
keywords:
- Windows Media Player 線上商店，編譯目錄
- 線上商店，編譯目錄
- 輸入1個線上商店，編譯目錄
- Windows Media Player 線上商店，TSV 檔案
- 線上商店，TSV 檔案
- 輸入1個線上商店，TSV 檔案
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- catcomp.exe
- 編譯目錄
- tab 鍵分隔值 (TSV) 檔案
- TSV (定位字元分隔值) 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b68af019a5e2302f52f615d5a1dba2180e27cfe5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106968082"
---
# <a name="compiling-a-full-catalog-from-tsv-files"></a><span data-ttu-id="538b1-116">從 TSV 檔案編譯完整目錄</span><span class="sxs-lookup"><span data-stu-id="538b1-116">Compiling a Full Catalog from TSV Files</span></span>

<span data-ttu-id="538b1-117">新的目錄是從一組定位鍵分隔值 (TSV) 檔案建立。</span><span class="sxs-lookup"><span data-stu-id="538b1-117">New catalogs are created from a set of tab-separated-value (TSV) files.</span></span> <span data-ttu-id="538b1-118">檔案必須採用 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="538b1-118">The files must be in Unicode format.</span></span> <span data-ttu-id="538b1-119">將下列所需的 TSV 檔案放入資料夾中， (catcomp.exe) 的輸入路徑引數，並使用下列語法呼叫 catcomp.exe：</span><span class="sxs-lookup"><span data-stu-id="538b1-119">Place the required TSV files listed below into a folder (the input path argument to catcomp.exe), and call catcomp.exe using the following syntax:</span></span>


```C++
catcomp <input path> [version number] [locale ID] [debug]
```



<span data-ttu-id="538b1-120">如果未提供版本號碼，則版本號碼會設定為0。</span><span class="sxs-lookup"><span data-stu-id="538b1-120">If a version number is not provided, the version number will be set to 0.</span></span> <span data-ttu-id="538b1-121">如果未提供任何地區設定識別碼，則會使用系統地區設定。</span><span class="sxs-lookup"><span data-stu-id="538b1-121">If no locale ID is provided, the system locale is used.</span></span> <span data-ttu-id="538b1-122">如果只提供一個數值選擇性引數，則會假設為版本號碼。</span><span class="sxs-lookup"><span data-stu-id="538b1-122">If only one numeric optional argument is provided, it is assumed to be the version number.</span></span> <span data-ttu-id="538b1-123">如果指定 debug，畫面的輸出將會提供更詳細的診斷資訊。</span><span class="sxs-lookup"><span data-stu-id="538b1-123">If debug is specified, the output to the screen will provide more detailed diagnostic information.</span></span>

<span data-ttu-id="538b1-124">例如，下列程式碼會從 C： CatalogData 210 中的檔案編譯 \\ 目錄 \\ ，並為目錄提供210版的版本號碼：</span><span class="sxs-lookup"><span data-stu-id="538b1-124">For example, the following will compile a catalog from the files in C:\\CatalogData\\210 and give the catalog a version number of 210:</span></span>


```C++
catcomp C:\CatalogData\210 210
```



<span data-ttu-id="538b1-125">若要顯示更詳細的錯誤訊息，可以新增選擇性的 debug 引數，如下所示：</span><span class="sxs-lookup"><span data-stu-id="538b1-125">To display more detailed error messages, the optional debug argument can be added, as follows:</span></span>


```C++
catcomp C:\CatalogData\210 210 debug
```



## <a name="required-tsv-files"></a><span data-ttu-id="538b1-126">必要的 TSV 檔案</span><span class="sxs-lookup"><span data-stu-id="538b1-126">Required TSV Files</span></span>

<span data-ttu-id="538b1-127">下列每個檔案都必須存在，但是如果沒有檔案的資料，就可以使用空的檔案。</span><span class="sxs-lookup"><span data-stu-id="538b1-127">Each of the following files must be present, but an empty file can be used if there is no data for a file.</span></span> <span data-ttu-id="538b1-128">比方說，如果您的目錄不包含任何電臺通道，radio.csv 可以是空的。</span><span class="sxs-lookup"><span data-stu-id="538b1-128">For instance, if your catalog contains no radio channels, radio.csv can be empty.</span></span> <span data-ttu-id="538b1-129">檔案的命名必須與列出的完全相同。</span><span class="sxs-lookup"><span data-stu-id="538b1-129">The files must be named exactly as listed.</span></span>

[<span data-ttu-id="538b1-130">track.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-130">track.csv</span></span>](track-csv.md)

[<span data-ttu-id="538b1-131">album.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-131">album.csv</span></span>](album-csv.md)

[<span data-ttu-id="538b1-132">artist.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-132">artist.csv</span></span>](artist-csv.md)

[<span data-ttu-id="538b1-133">genre.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-133">genre.csv</span></span>](genre-csv.md)

[<span data-ttu-id="538b1-134">subgenre.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-134">subgenre.csv</span></span>](subgenre-csv.md)

[<span data-ttu-id="538b1-135">list.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-135">list.csv</span></span>](list-csv.md)

[<span data-ttu-id="538b1-136">listitem.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-136">listitem.csv</span></span>](listitem-csv.md)

[<span data-ttu-id="538b1-137">radio.csv</span><span class="sxs-lookup"><span data-stu-id="538b1-137">radio.csv</span></span>](radio-csv.md)

> [!Note]  
> <span data-ttu-id="538b1-138">雖然檔案名必須有 .csv 副檔名，但檔案不是以逗號分隔值 (CSV) 格式。</span><span class="sxs-lookup"><span data-stu-id="538b1-138">Although the file names must have .csv extensions, the files are not in Comma Separated Values (CSV) format.</span></span> <span data-ttu-id="538b1-139">檔案必須位於 Tab 分隔值 (TSV) 格式。</span><span class="sxs-lookup"><span data-stu-id="538b1-139">The files must be in Tab Separated Values (TSV) format.</span></span>

 

<span data-ttu-id="538b1-140">如果編譯成功，catcomp.exe 會建立三個輸出檔。</span><span class="sxs-lookup"><span data-stu-id="538b1-140">If compilation is successful, catcomp.exe creates three output files.</span></span>



| <span data-ttu-id="538b1-141">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="538b1-141">File name</span></span>                   | <span data-ttu-id="538b1-142">描述</span><span class="sxs-lookup"><span data-stu-id="538b1-142">Description</span></span>                                                                                                                                                                         |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="538b1-143">catalog. wmdb</span><span class="sxs-lookup"><span data-stu-id="538b1-143">catalog.wmdb</span></span>                | <span data-ttu-id="538b1-144">未壓縮的已編譯目錄。</span><span class="sxs-lookup"><span data-stu-id="538b1-144">Uncompressed compiled catalog.</span></span>                                                                                                                                                      |
| <span data-ttu-id="538b1-145">catalog. wmdb. lz</span><span class="sxs-lookup"><span data-stu-id="538b1-145">catalog.wmdb.lz</span></span>             | <span data-ttu-id="538b1-146">壓縮格式的目錄。</span><span class="sxs-lookup"><span data-stu-id="538b1-146">Catalog in compressed format.</span></span> <span data-ttu-id="538b1-147">您的外掛程式可將此檔案的位置提供給 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)中的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="538b1-147">Your plug-in can give the location of this file to Windows Media Player in [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span> |
| <span data-ttu-id="538b1-148">編譯的 \_ 唯一 \_words.txt</span><span class="sxs-lookup"><span data-stu-id="538b1-148">compiled\_unique\_words.txt</span></span> | <span data-ttu-id="538b1-149">中繼輸出檔。</span><span class="sxs-lookup"><span data-stu-id="538b1-149">An intermediate output file.</span></span> <span data-ttu-id="538b1-150">Windows Media Player 未使用。</span><span class="sxs-lookup"><span data-stu-id="538b1-150">Not used by Windows Media Player.</span></span>                                                                                                                      |



 

 

 




