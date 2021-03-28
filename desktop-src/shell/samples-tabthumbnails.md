---
description: 示範應用程式如何公開多個切換目標 (作為 taskband 上的索引標籤) ，以及如何提供縮圖。
title: TabThumbnails 範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 3F48EAA2-98A3-4530-9FC6-A395987157B7
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 323604d104be3432a5fc251901c4308bfc989f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973745"
---
# <a name="tabthumbnails-sample"></a><span data-ttu-id="6144d-103">TabThumbnails 範例</span><span class="sxs-lookup"><span data-stu-id="6144d-103">TabThumbnails Sample</span></span>

<span data-ttu-id="6144d-104">示範應用程式如何公開多個切換目標 (作為 taskband 上的索引標籤) ，以及如何提供縮圖。</span><span class="sxs-lookup"><span data-stu-id="6144d-104">Demonstrates how an application can expose multiple switch targets (as for tabs) on a taskband and how to provide their thumbnails.</span></span>

<span data-ttu-id="6144d-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6144d-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6144d-106">需求</span><span class="sxs-lookup"><span data-stu-id="6144d-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6144d-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="6144d-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6144d-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="6144d-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6144d-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="6144d-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6144d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6144d-110">Requirements</span></span>



| <span data-ttu-id="6144d-111">產品</span><span class="sxs-lookup"><span data-stu-id="6144d-111">Product</span></span>                                | <span data-ttu-id="6144d-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="6144d-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6144d-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6144d-113">Windows</span></span>                                | <span data-ttu-id="6144d-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6144d-114">Windows 7</span></span>               |
| <span data-ttu-id="6144d-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6144d-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6144d-116">7.0</span><span class="sxs-lookup"><span data-stu-id="6144d-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6144d-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="6144d-117">Downloading the Sample</span></span>

| <span data-ttu-id="6144d-118">Location</span><span class="sxs-lookup"><span data-stu-id="6144d-118">Location</span></span>      | <span data-ttu-id="6144d-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="6144d-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6144d-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6144d-120">GitHub</span></span>  | [<span data-ttu-id="6144d-121">TabThumbnails 範例</span><span class="sxs-lookup"><span data-stu-id="6144d-121">TabThumbnails sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails) |

## <a name="building-the-sample"></a><span data-ttu-id="6144d-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="6144d-122">Building the Sample</span></span>

<span data-ttu-id="6144d-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="6144d-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="6144d-124">開啟 [命令提示字元] 視窗，並流覽至 **TabThumbnails** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="6144d-124">Open the command prompt window and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="6144d-125">輸入 `msbuild TabThumbnails.sln`。</span><span class="sxs-lookup"><span data-stu-id="6144d-125">Enter `msbuild TabThumbnails.sln`.</span></span>

<span data-ttu-id="6144d-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="6144d-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6144d-127">開啟 Windows 檔案總管，然後流覽至 **TabThumbnails** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="6144d-127">Open Windows Explorer and navigate to the **TabThumbnails** project directory.</span></span>
2.  <span data-ttu-id="6144d-128">按兩下 TabThumbnails .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="6144d-128">Double-click the icon for the TabThumbnails.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="6144d-129">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="6144d-129">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6144d-130">執行範例</span><span class="sxs-lookup"><span data-stu-id="6144d-130">Running the Sample</span></span>

1.  <span data-ttu-id="6144d-131">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="6144d-131">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="6144d-132">在命令列中，輸入 `TabThumbnails.exe` 。</span><span class="sxs-lookup"><span data-stu-id="6144d-132">At the command line, enter `TabThumbnails.exe`.</span></span> <span data-ttu-id="6144d-133">或者，從 Windows 檔案總管按兩下 TabThumbnails.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="6144d-133">Alternatively, from Windows Explorer double-click the icon for TabThumbnails.exe.</span></span>

 

 



