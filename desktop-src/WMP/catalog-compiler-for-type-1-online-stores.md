---
title: 類型1線上商店的目錄編譯器
description: 類型1線上商店的目錄編譯器
ms.assetid: 49c03d3b-3381-4663-83c8-5bc8fa70f7c3
keywords:
- Windows Media Player 線上商店，目錄編譯器
- 線上商店，目錄編譯器
- 輸入1個線上商店、目錄編譯器
- Windows Media Player 線上商店，catcomp.exe
- 線上商店、catcomp.exe
- 輸入1個線上商店，catcomp.exe
- 目錄編譯器
- catcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c54ffd054c5e72b04ddd32eef12c7fe6b6cc89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965830"
---
# <a name="catalog-compiler-for-type-1-online-stores"></a><span data-ttu-id="b821f-111">類型1線上商店的目錄編譯器</span><span class="sxs-lookup"><span data-stu-id="b821f-111">Catalog Compiler for Type 1 Online Stores</span></span>

<span data-ttu-id="b821f-112">目錄編譯器 (catcomp.exe) 是一種命令列工具，可供型別1線上商店用來將包含線上商店目錄資料的一組 tab 鍵分隔值 (TSV) 檔案，編譯成可透過 Windows Media Player 下載的壓縮類別目錄。</span><span class="sxs-lookup"><span data-stu-id="b821f-112">The catalog compiler (catcomp.exe) is a command-line tool used by Type 1 online stores to compile the set of tab-separated-value (TSV) files containing the online store's catalog data into a compressed catalog that can be downloaded by Windows Media Player.</span></span> <span data-ttu-id="b821f-113">目錄編譯器也會編譯目錄更新檔案，其中只包含上次目錄更新之後變更的目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="b821f-113">The catalog compiler also compiles catalog update files containing only the catalog information that has changed since the last catalog update.</span></span>

<span data-ttu-id="b821f-114">您應在 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)的線上商店外掛程式的執行中，提供已壓縮的類別目錄檔案或目錄更新檔案，以供下載 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="b821f-114">The compressed catalog files or catalog update files should be provided to Windows Media Player for download in the online store plug-in's implementation of [IWMPContentPartner::GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl).</span></span>

<span data-ttu-id="b821f-115">一般工作</span><span class="sxs-lookup"><span data-stu-id="b821f-115">Common Tasks</span></span>

-   [<span data-ttu-id="b821f-116">從 TSV 檔案編譯完整目錄</span><span class="sxs-lookup"><span data-stu-id="b821f-116">Compiling a Full Catalog from TSV Files</span></span>](compiling-a-full-catalog-from-tsv-files.md)
-   [<span data-ttu-id="b821f-117">從完整目錄編譯目錄更新</span><span class="sxs-lookup"><span data-stu-id="b821f-117">Compiling a Catalog Update from Full Catalogs</span></span>](compiling-a-catalog-update-from-full-catalogs.md)

<span data-ttu-id="b821f-118">診斷工作</span><span class="sxs-lookup"><span data-stu-id="b821f-118">Diagnostic Tasks</span></span>

-   [<span data-ttu-id="b821f-119">顯示說明</span><span class="sxs-lookup"><span data-stu-id="b821f-119">Displaying Help</span></span>](displaying-help.md)
-   [<span data-ttu-id="b821f-120">正在抓取目錄資訊</span><span class="sxs-lookup"><span data-stu-id="b821f-120">Retrieving Catalog Information</span></span>](retrieving-catalog-information.md)
-   [<span data-ttu-id="b821f-121">將更新套用至目錄</span><span class="sxs-lookup"><span data-stu-id="b821f-121">Applying an Update To a Catalog</span></span>](applying-an-update-to-a-catalog.md)

 

 




