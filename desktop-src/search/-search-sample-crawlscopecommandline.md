---
description: CrawlScopeCommandLine 程式碼範例會示範如何定義編目範圍管理員 (CSM) 索引編制作業的命令列選項。
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971364"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="cb33b-103">CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="cb33b-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="cb33b-104">CrawlScopeCommandLine 程式碼範例會示範如何定義編目範圍管理員 (CSM) 索引編制作業的命令列選項。</span><span class="sxs-lookup"><span data-stu-id="cb33b-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="cb33b-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="cb33b-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="cb33b-106">需求</span><span class="sxs-lookup"><span data-stu-id="cb33b-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="cb33b-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="cb33b-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="cb33b-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="cb33b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb33b-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="cb33b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb33b-111">Requirements</span></span>

| <span data-ttu-id="cb33b-112">產品</span><span class="sxs-lookup"><span data-stu-id="cb33b-112">Product</span></span>     | <span data-ttu-id="cb33b-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="cb33b-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="cb33b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="cb33b-114">Windows</span></span>     | <span data-ttu-id="cb33b-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="cb33b-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="cb33b-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="cb33b-116">Windows SDK</span></span> | <span data-ttu-id="cb33b-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="cb33b-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="cb33b-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-118">Downloading the Sample</span></span>

<span data-ttu-id="cb33b-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="cb33b-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="cb33b-120">Location</span><span class="sxs-lookup"><span data-stu-id="cb33b-120">Location</span></span> | <span data-ttu-id="cb33b-121">路徑或 URL</span><span class="sxs-lookup"><span data-stu-id="cb33b-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="cb33b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="cb33b-122">GitHub</span></span>   |    [<span data-ttu-id="cb33b-123">CrawlScopeCommandLine 範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="cb33b-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="cb33b-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="cb33b-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-125">Building the Sample</span></span>

1. <span data-ttu-id="cb33b-126">開啟 Windows 檔案總管，然後流覽至 **CrawlScopeCommandLine** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="cb33b-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="cb33b-127">按兩下 csmcmd .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="cb33b-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="cb33b-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="cb33b-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="cb33b-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="cb33b-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="cb33b-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="cb33b-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="cb33b-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-131">Running the Sample</span></span>

1. <span data-ttu-id="cb33b-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="cb33b-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="cb33b-133">在命令提示字元中，輸入 `csmcmd.exe` ，或從 Windows 檔案總管中，按兩下 csmcmd.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="cb33b-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb33b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb33b-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="cb33b-135">參考</span><span class="sxs-lookup"><span data-stu-id="cb33b-135">Reference</span></span>

[<span data-ttu-id="cb33b-136">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="cb33b-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="cb33b-137">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="cb33b-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="cb33b-138">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="cb33b-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="cb33b-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="cb33b-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="cb33b-140">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="cb33b-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="cb33b-141">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="cb33b-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="cb33b-142">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="cb33b-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="cb33b-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="cb33b-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="cb33b-144">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="cb33b-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="cb33b-145">其他範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-145">Other Samples</span></span>

[<span data-ttu-id="cb33b-146">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="cb33b-146">Search Code Samples</span></span>](-search-samples-ovw.md)
