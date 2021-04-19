---
description: StructuredQuerySample 程式碼範例示範如何從主控台讀取行、使用系統架構加以剖析，以及顯示產生的條件樹狀結構。
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991696"
---
# <a name="structuredquerysample"></a><span data-ttu-id="8fe8d-103">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="8fe8d-103">StructuredQuerySample</span></span>

<span data-ttu-id="8fe8d-104">StructuredQuerySample 程式碼範例示範如何從主控台讀取行、使用系統架構加以剖析，以及顯示產生的條件樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="8fe8d-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="8fe8d-106">需求</span><span class="sxs-lookup"><span data-stu-id="8fe8d-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="8fe8d-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="8fe8d-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="8fe8d-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="8fe8d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fe8d-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="8fe8d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe8d-111">Requirements</span></span>

| <span data-ttu-id="8fe8d-112">產品</span><span class="sxs-lookup"><span data-stu-id="8fe8d-112">Product</span></span>     | <span data-ttu-id="8fe8d-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="8fe8d-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="8fe8d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="8fe8d-114">Windows</span></span>     | <span data-ttu-id="8fe8d-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="8fe8d-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="8fe8d-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="8fe8d-116">Windows SDK</span></span> | <span data-ttu-id="8fe8d-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="8fe8d-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="8fe8d-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-118">Downloading the Sample</span></span>

<span data-ttu-id="8fe8d-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="8fe8d-120">Location</span><span class="sxs-lookup"><span data-stu-id="8fe8d-120">Location</span></span>      | <span data-ttu-id="8fe8d-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="8fe8d-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="8fe8d-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="8fe8d-122">GitHub</span></span>        | [<span data-ttu-id="8fe8d-123">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="8fe8d-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="8fe8d-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="8fe8d-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-125">Building the Sample</span></span>

1. <span data-ttu-id="8fe8d-126">開啟 Windows 檔案總管，然後流覽至 **StructuredQuerySample** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="8fe8d-127">按兩下 StructuredQuerySample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="8fe8d-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="8fe8d-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="8fe8d-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="8fe8d-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-131">Running the Sample</span></span>

1. <span data-ttu-id="8fe8d-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="8fe8d-133">在命令提示字元中，輸入 `StructuredQuerySample.exe` ，或從 Windows 檔案總管中，按兩下 StructuredQuerySample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="8fe8d-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fe8d-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fe8d-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="8fe8d-135">參考</span><span class="sxs-lookup"><span data-stu-id="8fe8d-135">Reference</span></span>

[<span data-ttu-id="8fe8d-136">**ICondition**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="8fe8d-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="8fe8d-138">**IConditionFactory**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="8fe8d-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="8fe8d-140">**IConditionGenerator**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="8fe8d-141">**IQueryParser**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="8fe8d-142">**IQueryParserManager**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="8fe8d-143">**IQuerySolution**</span><span class="sxs-lookup"><span data-stu-id="8fe8d-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="8fe8d-144">其他範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-144">Other Samples</span></span>

[<span data-ttu-id="8fe8d-145">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="8fe8d-145">Search Code Samples</span></span>](-search-samples-ovw.md)
