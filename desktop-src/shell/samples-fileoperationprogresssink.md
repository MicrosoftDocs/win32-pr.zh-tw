---
description: 示範如何使用 IFileOperationProgressSink 介面方法來監視 IFileOperation 介面動作的詳細資料。
title: 檔案作業進度接收
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026913"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="6717f-103">檔案作業進度接收</span><span class="sxs-lookup"><span data-stu-id="6717f-103">File Operation Progress Sink</span></span>

<span data-ttu-id="6717f-104">示範如何使用 [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) 介面方法來監視 [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) 介面動作的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6717f-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="6717f-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="6717f-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6717f-106">需求</span><span class="sxs-lookup"><span data-stu-id="6717f-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6717f-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="6717f-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="6717f-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="6717f-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="6717f-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="6717f-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="6717f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6717f-110">Requirements</span></span>



| <span data-ttu-id="6717f-111">產品</span><span class="sxs-lookup"><span data-stu-id="6717f-111">Product</span></span>                                | <span data-ttu-id="6717f-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="6717f-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="6717f-113">Windows</span><span class="sxs-lookup"><span data-stu-id="6717f-113">Windows</span></span>                                | <span data-ttu-id="6717f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6717f-114">Windows Vista</span></span>           |
| <span data-ttu-id="6717f-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="6717f-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="6717f-116">6.1</span><span class="sxs-lookup"><span data-stu-id="6717f-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="6717f-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="6717f-117">Downloading the Sample</span></span>

| <span data-ttu-id="6717f-118">Location</span><span class="sxs-lookup"><span data-stu-id="6717f-118">Location</span></span>      | <span data-ttu-id="6717f-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="6717f-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6717f-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="6717f-120">GitHub</span></span>  | [<span data-ttu-id="6717f-121">FileOperationProgressSink 範例</span><span class="sxs-lookup"><span data-stu-id="6717f-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="6717f-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="6717f-122">Building the Sample</span></span>

<span data-ttu-id="6717f-123">若要從命令提示字元視窗建立範例：</span><span class="sxs-lookup"><span data-stu-id="6717f-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="6717f-124">開啟 [命令提示字元] 視窗，並流覽至 **FileOperationProgressSink** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="6717f-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="6717f-125">輸入 `msbuild FileOperationProgressSinkSample.sln`。</span><span class="sxs-lookup"><span data-stu-id="6717f-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="6717f-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="6717f-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="6717f-127">開啟 Windows 檔案總管，然後流覽至 **FilesInUse** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="6717f-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="6717f-128">例如，完整的預設安裝路徑為 `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` 。</span><span class="sxs-lookup"><span data-stu-id="6717f-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="6717f-129">按兩下 FileOperationProgressSinkSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="6717f-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="6717f-130">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="6717f-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="6717f-131">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="6717f-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="6717f-132">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="6717f-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="6717f-133">執行範例</span><span class="sxs-lookup"><span data-stu-id="6717f-133">Running the Sample</span></span>

1.  <span data-ttu-id="6717f-134">使用命令提示字元視窗或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="6717f-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="6717f-135">在命令提示字元中，輸入 `FileOperationProgressSinkSample.exe` ，或從 Windows 檔案總管中，按兩下 FileOperationProgressSinkSample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="6717f-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



