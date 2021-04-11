---
description: WSSQL 程式碼範例會示範如何透過結構化查詢語言 (SQL)  (SQL) ，在 Microsoft OLE DB 和 Windows Search 之間進行通訊。
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847812"
---
# <a name="wssql"></a><span data-ttu-id="34f39-103">WSSQL</span><span class="sxs-lookup"><span data-stu-id="34f39-103">WSSQL</span></span>

<span data-ttu-id="34f39-104">WSSQL 程式碼範例會示範如何透過結構化查詢語言 (SQL)  (SQL) ，在 Microsoft OLE DB 和 Windows Search 之間進行通訊。</span><span class="sxs-lookup"><span data-stu-id="34f39-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="34f39-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="34f39-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="34f39-106">需求</span><span class="sxs-lookup"><span data-stu-id="34f39-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="34f39-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="34f39-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="34f39-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="34f39-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="34f39-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="34f39-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="34f39-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="34f39-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="34f39-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="34f39-111">Requirements</span></span>

| <span data-ttu-id="34f39-112">產品</span><span class="sxs-lookup"><span data-stu-id="34f39-112">Product</span></span>     | <span data-ttu-id="34f39-113">產品版本</span><span class="sxs-lookup"><span data-stu-id="34f39-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="34f39-114">Windows</span><span class="sxs-lookup"><span data-stu-id="34f39-114">Windows</span></span>     | <span data-ttu-id="34f39-115">Windows 7、8.1 或 10</span><span class="sxs-lookup"><span data-stu-id="34f39-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="34f39-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="34f39-116">Windows SDK</span></span> | <span data-ttu-id="34f39-117">7.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="34f39-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="34f39-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="34f39-118">Downloading the Sample</span></span>

<span data-ttu-id="34f39-119">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="34f39-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="34f39-120">Location</span><span class="sxs-lookup"><span data-stu-id="34f39-120">Location</span></span>      | <span data-ttu-id="34f39-121">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="34f39-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="34f39-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="34f39-122">GitHub</span></span>        | [<span data-ttu-id="34f39-123">WSSQL 範例</span><span class="sxs-lookup"><span data-stu-id="34f39-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="34f39-124">針對所有 Windows 版本（包括 Windows 7），建議您直接從 GitHub 下載最新版本的範例。</span><span class="sxs-lookup"><span data-stu-id="34f39-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="34f39-125">建立範例</span><span class="sxs-lookup"><span data-stu-id="34f39-125">Building the Sample</span></span>

1. <span data-ttu-id="34f39-126">開啟 Windows 檔案總管，然後流覽至 **WSSQL** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="34f39-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="34f39-127">按兩下 WSSQL .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="34f39-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="34f39-128">.Sln 檔案是在舊版 Visual Studio 下建立的，因此，如果您執行 Visual Studio 2012 或更新版本，則需要進行升級。</span><span class="sxs-lookup"><span data-stu-id="34f39-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="34f39-129">這不會影響範例的行為。</span><span class="sxs-lookup"><span data-stu-id="34f39-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="34f39-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="34f39-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="34f39-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="34f39-131">Running the Sample</span></span>

1. <span data-ttu-id="34f39-132">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="34f39-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="34f39-133">在命令提示字元中，輸入 `WSSQL.exe` ，或從 Windows 檔案總管中，按兩下 WSSQL.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="34f39-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34f39-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="34f39-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="34f39-135">概念</span><span class="sxs-lookup"><span data-stu-id="34f39-135">Conceptual</span></span>

[<span data-ttu-id="34f39-136">使用 Windows Search SQL 語法</span><span class="sxs-lookup"><span data-stu-id="34f39-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="34f39-137">一般查詢語言資訊</span><span class="sxs-lookup"><span data-stu-id="34f39-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="34f39-138">OLE DB 程式設計總覽</span><span class="sxs-lookup"><span data-stu-id="34f39-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="34f39-139">其他範例</span><span class="sxs-lookup"><span data-stu-id="34f39-139">Other Samples</span></span>

[<span data-ttu-id="34f39-140">搜尋程式碼範例</span><span class="sxs-lookup"><span data-stu-id="34f39-140">Search Code Samples</span></span>](-search-samples-ovw.md)
