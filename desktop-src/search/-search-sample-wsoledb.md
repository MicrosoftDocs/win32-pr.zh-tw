---
description: WSOleDB 程式碼範例會示範 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取，並示範兩種從 Windows Search 抓取結果的額外方法。
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847813"
---
# <a name="wsoledb"></a><span data-ttu-id="54643-103">WSOleDB</span><span class="sxs-lookup"><span data-stu-id="54643-103">WSOleDB</span></span>

<span data-ttu-id="54643-104">WSOleDB 程式碼範例會示範 Active Template Library (ATL) OLE DB Windows Search 應用程式的存取，並示範兩種從 Windows Search 抓取結果的額外方法。</span><span class="sxs-lookup"><span data-stu-id="54643-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="54643-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="54643-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="54643-106">需求</span><span class="sxs-lookup"><span data-stu-id="54643-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="54643-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="54643-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="54643-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="54643-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="54643-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="54643-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="54643-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="54643-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="54643-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="54643-111">Requirements</span></span>

| <span data-ttu-id="54643-112">產品</span><span class="sxs-lookup"><span data-stu-id="54643-112">Product</span></span>     | <span data-ttu-id="54643-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="54643-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="54643-114">Windows</span><span class="sxs-lookup"><span data-stu-id="54643-114">Windows</span></span>     | <span data-ttu-id="54643-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="54643-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="54643-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="54643-116">Windows SDK</span></span> | <span data-ttu-id="54643-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="54643-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="54643-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="54643-118">Downloading the Sample</span></span>

<span data-ttu-id="54643-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="54643-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="54643-120">Location</span><span class="sxs-lookup"><span data-stu-id="54643-120">Location</span></span>      | <span data-ttu-id="54643-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="54643-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="54643-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="54643-122">GitHub</span></span>        | [<span data-ttu-id="54643-123">WSOleDB 範例</span><span class="sxs-lookup"><span data-stu-id="54643-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="54643-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="54643-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="54643-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="54643-125">Building the Sample</span></span>

1. <span data-ttu-id="54643-126">開啟 Windows 檔案總管，然後流覽至 **WSOleDB** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="54643-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="54643-127">按兩下 WSOleDB .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="54643-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="54643-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="54643-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="54643-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="54643-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="54643-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="54643-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="54643-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="54643-131">Running the Sample</span></span>

1. <span data-ttu-id="54643-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="54643-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="54643-133">在命令提示字元中，輸入 `WSOleDB.exe` ，或從 Windows 檔案總管中，按兩下 WSOleDB.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="54643-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54643-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="54643-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="54643-135">參考</span><span class="sxs-lookup"><span data-stu-id="54643-135">Reference</span></span>

[<span data-ttu-id="54643-136">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="54643-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="54643-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="54643-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="54643-138">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="54643-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="54643-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="54643-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="54643-140">概念</span><span class="sxs-lookup"><span data-stu-id="54643-140">Conceptual</span></span>

[<span data-ttu-id="54643-141">OLE DB 程式設計總覽</span><span class="sxs-lookup"><span data-stu-id="54643-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="54643-142">其他範例</span><span class="sxs-lookup"><span data-stu-id="54643-142">Other Samples</span></span>

[<span data-ttu-id="54643-143">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="54643-143">Search Code Samples</span></span>](-search-samples-ovw.md)
