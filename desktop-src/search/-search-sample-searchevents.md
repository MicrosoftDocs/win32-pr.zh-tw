---
description: SearchEvents 程式碼範例會示範如何設定索引事件的優先順序。
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974016"
---
# <a name="searchevents"></a><span data-ttu-id="c1c16-103">SearchEvents</span><span class="sxs-lookup"><span data-stu-id="c1c16-103">SearchEvents</span></span>

<span data-ttu-id="c1c16-104">SearchEvents 程式碼範例會示範如何設定索引事件的優先順序。</span><span class="sxs-lookup"><span data-stu-id="c1c16-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="c1c16-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="c1c16-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="c1c16-106">需求</span><span class="sxs-lookup"><span data-stu-id="c1c16-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="c1c16-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="c1c16-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="c1c16-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="c1c16-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1c16-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="c1c16-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c1c16-111">Requirements</span></span>

| <span data-ttu-id="c1c16-112">產品</span><span class="sxs-lookup"><span data-stu-id="c1c16-112">Product</span></span>     | <span data-ttu-id="c1c16-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="c1c16-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="c1c16-114">Windows</span><span class="sxs-lookup"><span data-stu-id="c1c16-114">Windows</span></span>     | <span data-ttu-id="c1c16-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="c1c16-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="c1c16-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="c1c16-116">Windows SDK</span></span> | <span data-ttu-id="c1c16-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="c1c16-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="c1c16-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-118">Downloading the Sample</span></span>

<span data-ttu-id="c1c16-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="c1c16-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="c1c16-120">Location</span><span class="sxs-lookup"><span data-stu-id="c1c16-120">Location</span></span>      | <span data-ttu-id="c1c16-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="c1c16-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c1c16-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="c1c16-122">GitHub</span></span>        | [<span data-ttu-id="c1c16-123">SearchEvents 範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="c1c16-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="c1c16-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c1c16-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-125">Building the Sample</span></span>

1. <span data-ttu-id="c1c16-126">開啟 Windows 檔案總管，然後流覽至 **SearchEvents** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="c1c16-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="c1c16-127">按兩下事件 .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="c1c16-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="c1c16-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="c1c16-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="c1c16-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="c1c16-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="c1c16-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="c1c16-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c1c16-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-131">Running the Sample</span></span>

1. <span data-ttu-id="c1c16-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="c1c16-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="c1c16-133">在命令提示字元中，輸入 `Eventing.exe` ，或從 Windows 檔案總管中，按兩下 Eventing.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="c1c16-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1c16-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="c1c16-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="c1c16-135">參考</span><span class="sxs-lookup"><span data-stu-id="c1c16-135">Reference</span></span>

[<span data-ttu-id="c1c16-136">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="c1c16-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="c1c16-137">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="c1c16-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="c1c16-138">**優先權 \_ 層級**</span><span class="sxs-lookup"><span data-stu-id="c1c16-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="c1c16-139">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="c1c16-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="c1c16-140">**ROWSETEVENT \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c1c16-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="c1c16-141">其他範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-141">Other Samples</span></span>

[<span data-ttu-id="c1c16-142">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="c1c16-142">Search Code Samples</span></span>](-search-samples-ovw.md)
