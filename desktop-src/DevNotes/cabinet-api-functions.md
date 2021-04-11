---
description: 深入瞭解：封包 API 函式
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: 封包 API 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847187"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="7d56a-103">封包 API 函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-103">Cabinet API Functions</span></span>

<span data-ttu-id="7d56a-104">本節說明下列封包 API 函式：</span><span class="sxs-lookup"><span data-stu-id="7d56a-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="7d56a-105">FCI 函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-105">FCI Functions</span></span>

<span data-ttu-id="7d56a-106">FCI (檔案壓縮介面) 程式庫提供建立封包 (也稱為「CAB 檔案」 ) 的功能。</span><span class="sxs-lookup"><span data-stu-id="7d56a-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="7d56a-107">此外，程式庫還提供壓縮來減少儲存在封包中的檔案資料大小。</span><span class="sxs-lookup"><span data-stu-id="7d56a-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="7d56a-108">函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-108">Function</span></span>                                   | <span data-ttu-id="7d56a-109">描述</span><span class="sxs-lookup"><span data-stu-id="7d56a-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d56a-110">**FCIAddFile**</span><span class="sxs-lookup"><span data-stu-id="7d56a-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="7d56a-111">將檔案新增至目前正在效果的封包。</span><span class="sxs-lookup"><span data-stu-id="7d56a-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="7d56a-112">**FCICreate**</span><span class="sxs-lookup"><span data-stu-id="7d56a-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="7d56a-113">建立 FCI 內容。</span><span class="sxs-lookup"><span data-stu-id="7d56a-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="7d56a-114">**FCIDestroy**</span><span class="sxs-lookup"><span data-stu-id="7d56a-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="7d56a-115">刪除開啟的 FCI 內容，釋放與內容相關聯的任何記憶體和暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="7d56a-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="7d56a-116">**FCIFlushCabinet**</span><span class="sxs-lookup"><span data-stu-id="7d56a-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="7d56a-117">完成目前的封包。</span><span class="sxs-lookup"><span data-stu-id="7d56a-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="7d56a-118">**FCIFlushFolder**</span><span class="sxs-lookup"><span data-stu-id="7d56a-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="7d56a-119">強制立即完成結構下目前的資料夾。</span><span class="sxs-lookup"><span data-stu-id="7d56a-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="7d56a-120">FDI 函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-120">FDI Functions</span></span>

<span data-ttu-id="7d56a-121">FDI (檔案解壓縮介面) 程式庫提供從封包解壓縮檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="7d56a-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="7d56a-122">函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-122">Function</span></span>                                         | <span data-ttu-id="7d56a-123">描述</span><span class="sxs-lookup"><span data-stu-id="7d56a-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7d56a-124">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="7d56a-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="7d56a-125">從封包解壓縮檔案。</span><span class="sxs-lookup"><span data-stu-id="7d56a-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="7d56a-126">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="7d56a-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="7d56a-127">建立 FDI 內容。</span><span class="sxs-lookup"><span data-stu-id="7d56a-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="7d56a-128">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="7d56a-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="7d56a-129">刪除開啟的 FDI 內容。</span><span class="sxs-lookup"><span data-stu-id="7d56a-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="7d56a-130">**FDIIsCabinet**</span><span class="sxs-lookup"><span data-stu-id="7d56a-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="7d56a-131">判斷檔案是否為封包，如果是，則會傳回描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="7d56a-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="7d56a-132">**FDITruncateCabinet**</span><span class="sxs-lookup"><span data-stu-id="7d56a-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="7d56a-133">從指定的資料夾編號開始截斷封包檔。</span><span class="sxs-lookup"><span data-stu-id="7d56a-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="7d56a-134">已淘汰函式</span><span class="sxs-lookup"><span data-stu-id="7d56a-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="7d56a-135">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="7d56a-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="7d56a-136">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="7d56a-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="7d56a-137">**提取**</span><span class="sxs-lookup"><span data-stu-id="7d56a-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="7d56a-138">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="7d56a-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="7d56a-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d56a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d56a-140">封包 API 參考</span><span class="sxs-lookup"><span data-stu-id="7d56a-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="7d56a-141">使用封包 API</span><span class="sxs-lookup"><span data-stu-id="7d56a-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




