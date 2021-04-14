---
description: ReindexMatchingUrls 程式碼範例會示範如何提供三種方式來指定要重新建立索引的檔案：符合檔案類型、mime 類型或指定 WHERE 子句的 Url。
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468796"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="76c6a-103">ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="76c6a-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="76c6a-104">ReindexMatchingUrls 程式碼範例會示範如何提供三種方式來指定要重新建立索引的檔案：符合檔案類型、mime 類型或指定 WHERE 子句的 Url。</span><span class="sxs-lookup"><span data-stu-id="76c6a-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="76c6a-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="76c6a-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="76c6a-106">需求</span><span class="sxs-lookup"><span data-stu-id="76c6a-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="76c6a-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="76c6a-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="76c6a-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="76c6a-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="76c6a-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="76c6a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="76c6a-111">Requirements</span></span>

| <span data-ttu-id="76c6a-112">產品</span><span class="sxs-lookup"><span data-stu-id="76c6a-112">Product</span></span>     | <span data-ttu-id="76c6a-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="76c6a-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="76c6a-114">Windows</span><span class="sxs-lookup"><span data-stu-id="76c6a-114">Windows</span></span>     | <span data-ttu-id="76c6a-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="76c6a-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="76c6a-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="76c6a-116">Windows SDK</span></span> | <span data-ttu-id="76c6a-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="76c6a-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="76c6a-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-118">Downloading the Sample</span></span>

<span data-ttu-id="76c6a-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="76c6a-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="76c6a-120">Location</span><span class="sxs-lookup"><span data-stu-id="76c6a-120">Location</span></span>      | <span data-ttu-id="76c6a-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="76c6a-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="76c6a-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="76c6a-122">GitHub</span></span>  | [<span data-ttu-id="76c6a-123">ReindexMatchingUrls 範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="76c6a-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="76c6a-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="76c6a-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-125">Building the Sample</span></span>

1. <span data-ttu-id="76c6a-126">開啟 Windows 檔案總管，然後流覽至 **ReindexMatchingUrls** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="76c6a-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="76c6a-127">例如，完整的預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` 。</span><span class="sxs-lookup"><span data-stu-id="76c6a-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="76c6a-128">按兩下 [索引] .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="76c6a-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="76c6a-129">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="76c6a-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="76c6a-130">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="76c6a-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="76c6a-131">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="76c6a-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="76c6a-132">執行範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-132">Running the Sample</span></span>

1. <span data-ttu-id="76c6a-133">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="76c6a-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="76c6a-134">在命令提示字元中，輸入 `Reindex.exe` ，或從 Windows 檔案總管中，按兩下 Reindex.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="76c6a-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76c6a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="76c6a-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="76c6a-136">參考</span><span class="sxs-lookup"><span data-stu-id="76c6a-136">Reference</span></span>

[<span data-ttu-id="76c6a-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="76c6a-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="76c6a-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="76c6a-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="76c6a-139">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="76c6a-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="76c6a-140">**ISearchPersistentItemsChangedSink**</span><span class="sxs-lookup"><span data-stu-id="76c6a-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="76c6a-141">**ISearchViewChangedSink**</span><span class="sxs-lookup"><span data-stu-id="76c6a-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="76c6a-142">**設定 \_ 旗標的優先順序**</span><span class="sxs-lookup"><span data-stu-id="76c6a-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="76c6a-143">其他範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-143">Other Samples</span></span>

[<span data-ttu-id="76c6a-144">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="76c6a-144">Search Code Samples</span></span>](-search-samples-ovw.md)
