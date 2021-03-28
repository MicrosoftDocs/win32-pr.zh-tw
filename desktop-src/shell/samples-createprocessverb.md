---
description: 示範如何使用 CreateProcess 方法來執行 Shell 動詞命令。
title: CreateProcess 動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8e52f251e12f0ca06bcb729407a7c8303836f9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973537"
---
# <a name="createprocess-verb-sample"></a><span data-ttu-id="94aa3-103">CreateProcess 動詞範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-103">CreateProcess Verb Sample</span></span>

<span data-ttu-id="94aa3-104">示範如何使用 CreateProcess 方法來執行 Shell 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="94aa3-104">Demonstrates how to implement a Shell verb using the CreateProcess method.</span></span>

<span data-ttu-id="94aa3-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="94aa3-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="94aa3-106">說明</span><span class="sxs-lookup"><span data-stu-id="94aa3-106">Description</span></span>](#description)
-   [<span data-ttu-id="94aa3-107">需求</span><span class="sxs-lookup"><span data-stu-id="94aa3-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="94aa3-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="94aa3-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="94aa3-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="94aa3-111">Description</span><span class="sxs-lookup"><span data-stu-id="94aa3-111">Description</span></span>

<span data-ttu-id="94aa3-112">CreateProcess 型動詞相依于執行可執行檔，並將命令列引數傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="94aa3-112">CreateProcess-based verbs depend on running a executable and passing it a command-line argument.</span></span> <span data-ttu-id="94aa3-113">這種方法的功能不如 DropTarget 和 ExecuteCommand 方法，但它確實可以達成所需的跨進程行為。</span><span class="sxs-lookup"><span data-stu-id="94aa3-113">This method is not as powerful as the DropTarget and ExecuteCommand methods but it does achieve the desirable out-of-process behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="94aa3-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="94aa3-114">Requirements</span></span>



| <span data-ttu-id="94aa3-115">產品</span><span class="sxs-lookup"><span data-stu-id="94aa3-115">Product</span></span>                                | <span data-ttu-id="94aa3-116">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="94aa3-116">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="94aa3-117">Windows</span><span class="sxs-lookup"><span data-stu-id="94aa3-117">Windows</span></span>                                | <span data-ttu-id="94aa3-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94aa3-118">Windows Vista</span></span>           |
| <span data-ttu-id="94aa3-119">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="94aa3-119">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="94aa3-120">7.0</span><span class="sxs-lookup"><span data-stu-id="94aa3-120">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="94aa3-121">下載範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-121">Downloading the Sample</span></span>

| <span data-ttu-id="94aa3-122">Location</span><span class="sxs-lookup"><span data-stu-id="94aa3-122">Location</span></span>      | <span data-ttu-id="94aa3-123">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="94aa3-123">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94aa3-124">GitHub</span><span class="sxs-lookup"><span data-stu-id="94aa3-124">GitHub</span></span>  | [<span data-ttu-id="94aa3-125">CreateProcessVerb 範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-125">CreateProcessVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="94aa3-126">建立範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-126">Building the Sample</span></span>

<span data-ttu-id="94aa3-127">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="94aa3-127">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="94aa3-128">開啟 [命令提示字元] 視窗，並流覽至 **CreateProcessVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="94aa3-128">Open the command prompt window and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="94aa3-129">輸入 `msbuild CreateProcessVerb.sln`。</span><span class="sxs-lookup"><span data-stu-id="94aa3-129">Enter `msbuild CreateProcessVerb.sln`.</span></span>

<span data-ttu-id="94aa3-130">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="94aa3-130">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="94aa3-131">開啟 Windows 檔案總管，然後流覽至 **CreateProcessVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="94aa3-131">Open Windows Explorer and navigate to the **CreateProcessVerb** project directory.</span></span>
2.  <span data-ttu-id="94aa3-132">按兩下 CreateProcessVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="94aa3-132">Double-click the icon for the CreateProcessVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="94aa3-133">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="94aa3-133">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="94aa3-134">執行範例</span><span class="sxs-lookup"><span data-stu-id="94aa3-134">Running the Sample</span></span>

1.  <span data-ttu-id="94aa3-135">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="94aa3-135">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="94aa3-136">在命令列中，輸入 `CreateProcessVerb.exe` 。</span><span class="sxs-lookup"><span data-stu-id="94aa3-136">At the command line, enter `CreateProcessVerb.exe`.</span></span> <span data-ttu-id="94aa3-137">或者，從 Windows 檔案總管按兩下 CreateProcessVerb.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="94aa3-137">Alternatively, from Windows Explorer double-click the icon for CreateProcessVerb.exe.</span></span>
3.  <span data-ttu-id="94aa3-138">遵循顯示的對話方塊中的指示</span><span class="sxs-lookup"><span data-stu-id="94aa3-138">Follow the instructions in the displayed dialog</span></span>

 

 



