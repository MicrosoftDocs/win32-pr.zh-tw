---
description: '[OpenSearch 程式碼] 範例示範如何使用 [OpenSearch] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。'
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386124"
---
# <a name="opensearch"></a><span data-ttu-id="42b65-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="42b65-103">OpenSearch</span></span>

<span data-ttu-id="42b65-104">[OpenSearch 程式碼] 範例示範如何使用 [ [opensearch](https://github.com/dewitt/opensearch) ] 通訊協定建立同盟搜尋服務，以及 ( 的 [ (搜尋) 連接器]) 檔案的 [.osdx]。</span><span class="sxs-lookup"><span data-stu-id="42b65-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="42b65-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="42b65-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="42b65-106">需求</span><span class="sxs-lookup"><span data-stu-id="42b65-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="42b65-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="42b65-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="42b65-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="42b65-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="42b65-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="42b65-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="42b65-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="42b65-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="42b65-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="42b65-111">Requirements</span></span>



| <span data-ttu-id="42b65-112">產品</span><span class="sxs-lookup"><span data-stu-id="42b65-112">Product</span></span>     | <span data-ttu-id="42b65-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="42b65-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="42b65-114">Windows</span><span class="sxs-lookup"><span data-stu-id="42b65-114">Windows</span></span>     | <span data-ttu-id="42b65-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="42b65-115">Windows 7</span></span>               |
| <span data-ttu-id="42b65-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="42b65-116">Windows SDK</span></span> | <span data-ttu-id="42b65-117">7.0</span><span class="sxs-lookup"><span data-stu-id="42b65-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="42b65-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="42b65-118">Downloading the Sample</span></span>

<span data-ttu-id="42b65-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="42b65-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="42b65-120">Location</span><span class="sxs-lookup"><span data-stu-id="42b65-120">Location</span></span>      | <span data-ttu-id="42b65-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="42b65-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="42b65-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="42b65-122">GitHub</span></span>  | [<span data-ttu-id="42b65-123">OpenSearch 範例</span><span class="sxs-lookup"><span data-stu-id="42b65-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="42b65-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="42b65-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="42b65-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="42b65-125">Building the Sample</span></span>

<span data-ttu-id="42b65-126">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="42b65-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="42b65-127">開啟 [命令提示字元] 視窗，並流覽至 **AdventureSearch** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="42b65-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="42b65-128">輸入 `msbuild AdventureSearch.sln`。</span><span class="sxs-lookup"><span data-stu-id="42b65-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="42b65-129">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="42b65-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="42b65-130">開啟 Windows 檔案總管，然後流覽至 **AdventureSearch** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="42b65-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="42b65-131">按兩下 AdventureSearch .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="42b65-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="42b65-132">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="42b65-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="42b65-133">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="42b65-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="42b65-134">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="42b65-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="42b65-135">執行範例</span><span class="sxs-lookup"><span data-stu-id="42b65-135">Running the Sample</span></span>

1.  <span data-ttu-id="42b65-136">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="42b65-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="42b65-137">在命令提示字元中，輸入 `AdventureSearch.exe` ，或從 Windows 檔案總管中，按兩下 AdventureSearch.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="42b65-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="42b65-138">在命令提示字元中，輸入 `GetOSDX.exe` ，或從 Windows 檔案總管中，按兩下 GetOSDX.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="42b65-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42b65-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="42b65-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="42b65-140">**參考**</span><span class="sxs-lookup"><span data-stu-id="42b65-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="42b65-141">搜尋連接器描述架構的總覽</span><span class="sxs-lookup"><span data-stu-id="42b65-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="42b65-142">**概念**</span><span class="sxs-lookup"><span data-stu-id="42b65-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="42b65-143">Windows 中的同盟搜尋</span><span class="sxs-lookup"><span data-stu-id="42b65-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="42b65-144">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="42b65-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="42b65-145">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="42b65-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="42b65-146">程式庫描述架構</span><span class="sxs-lookup"><span data-stu-id="42b65-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 
