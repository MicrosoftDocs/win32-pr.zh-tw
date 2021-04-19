---
description: DSearch 程式碼範例示範如何建立靜態主控台應用程式的類別，以使用 ISearchQueryHelper 的來查詢 Windows Search。
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972181"
---
# <a name="dsearch"></a><span data-ttu-id="854b5-103">DSearch</span><span class="sxs-lookup"><span data-stu-id="854b5-103">DSearch</span></span>

<span data-ttu-id="854b5-104">DSearch 程式碼範例示範如何建立靜態主控台應用程式的類別，以使用 [**ISearchQueryHelper 的**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)來查詢 Windows Search。</span><span class="sxs-lookup"><span data-stu-id="854b5-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="854b5-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="854b5-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="854b5-106">需求</span><span class="sxs-lookup"><span data-stu-id="854b5-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="854b5-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="854b5-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="854b5-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="854b5-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="854b5-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="854b5-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="854b5-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="854b5-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="854b5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="854b5-111">Requirements</span></span>

| <span data-ttu-id="854b5-112">產品</span><span class="sxs-lookup"><span data-stu-id="854b5-112">Product</span></span>     | <span data-ttu-id="854b5-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="854b5-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="854b5-114">Windows</span><span class="sxs-lookup"><span data-stu-id="854b5-114">Windows</span></span>     | <span data-ttu-id="854b5-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="854b5-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="854b5-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="854b5-116">Windows SDK</span></span> | <span data-ttu-id="854b5-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="854b5-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="854b5-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="854b5-118">Downloading the Sample</span></span>

<span data-ttu-id="854b5-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="854b5-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="854b5-120">Location</span><span class="sxs-lookup"><span data-stu-id="854b5-120">Location</span></span>      | <span data-ttu-id="854b5-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="854b5-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="854b5-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="854b5-122">GitHub</span></span>        | [<span data-ttu-id="854b5-123">DSearch 範例</span><span class="sxs-lookup"><span data-stu-id="854b5-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="854b5-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="854b5-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="854b5-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="854b5-125">Building the Sample</span></span>

1. <span data-ttu-id="854b5-126">開啟 Windows 檔案總管，然後流覽至 **DSearch** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="854b5-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="854b5-127">按兩下 DSearch .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="854b5-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="854b5-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="854b5-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="854b5-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="854b5-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="854b5-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="854b5-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="854b5-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="854b5-131">Running the Sample</span></span>

1. <span data-ttu-id="854b5-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="854b5-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="854b5-133">在命令提示字元中，輸入 `DSearch.exe` ，或從 Windows 檔案總管中，按兩下 DSearch.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="854b5-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="854b5-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="854b5-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="854b5-135">參考</span><span class="sxs-lookup"><span data-stu-id="854b5-135">Reference</span></span>

[<span data-ttu-id="854b5-136">**ISearchQueryHelper**</span><span class="sxs-lookup"><span data-stu-id="854b5-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="854b5-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="854b5-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="854b5-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="854b5-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="854b5-139">其他範例</span><span class="sxs-lookup"><span data-stu-id="854b5-139">Other Samples</span></span>

[<span data-ttu-id="854b5-140">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="854b5-140">Search Code Samples</span></span>](-search-samples-ovw.md)
