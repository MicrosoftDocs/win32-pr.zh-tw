---
description: 示範如何判斷家庭操作人員的成員資格狀態、列舉 [家庭工作] Shell 資料夾中的最上層專案，以及啟動 [家庭共用嚮導]。
title: 家用群組範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: FDEFF261-BF86-4fbb-8567-892F79F23D92
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c22ea84431f464ef8fcae6bfad0d90a45ba310d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026912"
---
# <a name="homegroup-sample"></a><span data-ttu-id="d76c1-103">家用群組範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-103">HomeGroup Sample</span></span>

<span data-ttu-id="d76c1-104">示範如何判斷家庭操作人員的成員資格狀態、列舉 [ **家庭** 工作] Shell 資料夾中的最上層專案，以及啟動 [ **家庭共用嚮導]**。</span><span class="sxs-lookup"><span data-stu-id="d76c1-104">Demonstrates how to determine HomeGroup membership status, enumerate top-level items in the **HomeGroup** Shell folder, and launch the **HomeGroup Sharing Wizard**.</span></span>

<span data-ttu-id="d76c1-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="d76c1-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d76c1-106">需求</span><span class="sxs-lookup"><span data-stu-id="d76c1-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="d76c1-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="d76c1-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="d76c1-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="d76c1-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="d76c1-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="d76c1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d76c1-111">Requirements</span></span>



| <span data-ttu-id="d76c1-112">產品</span><span class="sxs-lookup"><span data-stu-id="d76c1-112">Product</span></span>                                | <span data-ttu-id="d76c1-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="d76c1-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="d76c1-114">Windows</span><span class="sxs-lookup"><span data-stu-id="d76c1-114">Windows</span></span>                                | <span data-ttu-id="d76c1-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d76c1-115">Windows 7</span></span>               |
| <span data-ttu-id="d76c1-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="d76c1-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="d76c1-117">7.0</span><span class="sxs-lookup"><span data-stu-id="d76c1-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="d76c1-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-118">Downloading the Sample</span></span>

| <span data-ttu-id="d76c1-119">Location</span><span class="sxs-lookup"><span data-stu-id="d76c1-119">Location</span></span>      | <span data-ttu-id="d76c1-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="d76c1-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76c1-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="d76c1-121">GitHub</span></span>  | [<span data-ttu-id="d76c1-122">家庭群組範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-122">HomeGroup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/HomeGroup) |

## <a name="building-the-sample"></a><span data-ttu-id="d76c1-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-123">Building the Sample</span></span>

<span data-ttu-id="d76c1-124">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="d76c1-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="d76c1-125">開啟 [命令提示字元] 視窗，並流覽至 [ **家庭** ] 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d76c1-125">Open the command prompt window and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="d76c1-126">輸入 `msbuild HomeGroup.sln`。</span><span class="sxs-lookup"><span data-stu-id="d76c1-126">Enter `msbuild HomeGroup.sln`.</span></span>

<span data-ttu-id="d76c1-127">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="d76c1-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="d76c1-128">開啟 Windows 檔案總管，然後流覽至 [ **家庭** ] 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="d76c1-128">Open Windows Explorer and navigate to the **HomeGroup** project directory.</span></span>
2.  <span data-ttu-id="d76c1-129">按兩下 [檔案群組] .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="d76c1-129">Double-click the icon for the HomeGroup.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="d76c1-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="d76c1-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="d76c1-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="d76c1-131">Running the Sample</span></span>

1.  <span data-ttu-id="d76c1-132">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="d76c1-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="d76c1-133">在命令列中，輸入 `HomeGroup.exe` 。</span><span class="sxs-lookup"><span data-stu-id="d76c1-133">At the command line, enter `HomeGroup.exe`.</span></span> <span data-ttu-id="d76c1-134">或者，從 Windows 檔案總管按兩下 HomeGroup.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="d76c1-134">Alternatively, from Windows Explorer double-click the icon for HomeGroup.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d76c1-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="d76c1-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d76c1-136">**IHomeGroup**</span><span class="sxs-lookup"><span data-stu-id="d76c1-136">**IHomeGroup**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup)
</dt> <dt>

[<span data-ttu-id="d76c1-137">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="d76c1-137">**KNOWNFOLDERID**</span></span>](knownfolderid.md)
</dt> </dl>

 

 



