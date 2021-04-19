---
description: IFilterSample 程式碼範例會示範如何建立用來執行 IFilter 介面的 IFilter 基類。
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991990"
---
# <a name="ifiltersample"></a><span data-ttu-id="0a38b-103">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="0a38b-103">IFilterSample</span></span>

<span data-ttu-id="0a38b-104">IFilterSample 程式碼範例會示範如何建立用來執行 [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) 介面的 ifilter 基類。</span><span class="sxs-lookup"><span data-stu-id="0a38b-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="0a38b-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="0a38b-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="0a38b-106">需求</span><span class="sxs-lookup"><span data-stu-id="0a38b-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="0a38b-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="0a38b-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="0a38b-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="0a38b-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a38b-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="0a38b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a38b-111">Requirements</span></span>

| <span data-ttu-id="0a38b-112">產品</span><span class="sxs-lookup"><span data-stu-id="0a38b-112">Product</span></span>     | <span data-ttu-id="0a38b-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="0a38b-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="0a38b-114">Windows</span><span class="sxs-lookup"><span data-stu-id="0a38b-114">Windows</span></span>     | <span data-ttu-id="0a38b-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="0a38b-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="0a38b-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="0a38b-116">Windows SDK</span></span> | <span data-ttu-id="0a38b-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="0a38b-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="0a38b-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-118">Downloading the Sample</span></span>

<span data-ttu-id="0a38b-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="0a38b-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="0a38b-120">Location</span><span class="sxs-lookup"><span data-stu-id="0a38b-120">Location</span></span>      | <span data-ttu-id="0a38b-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="0a38b-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0a38b-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="0a38b-122">GitHub</span></span>        | [<span data-ttu-id="0a38b-123">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="0a38b-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="0a38b-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="0a38b-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="0a38b-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-125">Building the Sample</span></span>

1. <span data-ttu-id="0a38b-126">開啟 Windows 檔案總管，然後流覽至 **FilterBase** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="0a38b-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="0a38b-127">按兩下 FilterBase .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="0a38b-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="0a38b-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="0a38b-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="0a38b-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="0a38b-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="0a38b-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="0a38b-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="0a38b-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-131">Running the Sample</span></span>

1. <span data-ttu-id="0a38b-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="0a38b-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="0a38b-133">在命令提示字元中，輸入 `FilterBase.exe` ，或從 Windows 檔案總管中，按兩下 FilterBase.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="0a38b-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a38b-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="0a38b-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="0a38b-135">參考</span><span class="sxs-lookup"><span data-stu-id="0a38b-135">Reference</span></span>

[<span data-ttu-id="0a38b-136">**IFilter**</span><span class="sxs-lookup"><span data-stu-id="0a38b-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="0a38b-137">概念</span><span class="sxs-lookup"><span data-stu-id="0a38b-137">Conceptual</span></span>

[<span data-ttu-id="0a38b-138">開發篩選處理常式</span><span class="sxs-lookup"><span data-stu-id="0a38b-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="0a38b-139">其他範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-139">Other Samples</span></span>

[<span data-ttu-id="0a38b-140">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="0a38b-140">Search Code Samples</span></span>](-search-samples-ovw.md)
