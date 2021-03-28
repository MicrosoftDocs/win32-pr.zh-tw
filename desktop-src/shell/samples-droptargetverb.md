---
description: 示範如何使用 DropTarget 方法來執行 Shell 動詞。
title: DropTarget 動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: BEAD20C9-B01A-48aa-A85A-B7171383FBDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1f737c951c5bd588760dbb716859c04c0dc062fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973340"
---
# <a name="droptarget-verb-sample"></a><span data-ttu-id="b0cc9-103">DropTarget 動詞範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-103">DropTarget Verb Sample</span></span>

<span data-ttu-id="b0cc9-104">示範如何使用 DropTarget 方法來執行 Shell 動詞。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-104">Demonstrates how to implement a Shell verb using the DropTarget method.</span></span>

<span data-ttu-id="b0cc9-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b0cc9-106">說明</span><span class="sxs-lookup"><span data-stu-id="b0cc9-106">Description</span></span>](#description)
-   [<span data-ttu-id="b0cc9-107">需求</span><span class="sxs-lookup"><span data-stu-id="b0cc9-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b0cc9-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="b0cc9-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="b0cc9-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="b0cc9-111">Description</span><span class="sxs-lookup"><span data-stu-id="b0cc9-111">Description</span></span>

<span data-ttu-id="b0cc9-112">這個範例示範如何使用 DropTarget 方法來執行 Shell 動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-112">This sample shows how to implement a Shell verb using the DropTarget method.</span></span> <span data-ttu-id="b0cc9-113">對於必須在 Windows XP 上運作的動詞命令而言，這是慣用的方法。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-113">This method is preferred for verb implementations that must work on Windows XP.</span></span> <span data-ttu-id="b0cc9-114">此範例會將獨立本機伺服器元件物件模型 (COM) 物件中，但必須將動詞執行整合至現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-114">This sample implements a standalone local server Component Object Model (COM) object but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="b0cc9-115">若要這樣做，您的主要應用程式物件會自行註冊 class factory。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-115">To do so, your main application object registers a class factory for itself.</span></span> <span data-ttu-id="b0cc9-116">該物件會針對您的應用程式動詞來實行 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-116">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="b0cc9-117">請注意，如果您的應用程式尚未執行，COM 會啟動應用程式，但如果有的話，則會連接到應用程式的執行中實例。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-117">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0cc9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0cc9-118">Requirements</span></span>



| <span data-ttu-id="b0cc9-119">產品</span><span class="sxs-lookup"><span data-stu-id="b0cc9-119">Product</span></span>                                | <span data-ttu-id="b0cc9-120">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="b0cc9-120">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="b0cc9-121">Windows</span><span class="sxs-lookup"><span data-stu-id="b0cc9-121">Windows</span></span>                                | <span data-ttu-id="b0cc9-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b0cc9-122">Windows Vista</span></span>           |
| <span data-ttu-id="b0cc9-123">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="b0cc9-123">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="b0cc9-124">7.0</span><span class="sxs-lookup"><span data-stu-id="b0cc9-124">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="b0cc9-125">下載範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-125">Downloading the Sample</span></span>

| <span data-ttu-id="b0cc9-126">Location</span><span class="sxs-lookup"><span data-stu-id="b0cc9-126">Location</span></span>      | <span data-ttu-id="b0cc9-127">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="b0cc9-127">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0cc9-128">GitHub</span><span class="sxs-lookup"><span data-stu-id="b0cc9-128">GitHub</span></span>  | [<span data-ttu-id="b0cc9-129">DropTargetVerb 範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-129">DropTargetVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/DropTargetVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="b0cc9-130">建立範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-130">Building the Sample</span></span>

<span data-ttu-id="b0cc9-131">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="b0cc9-131">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="b0cc9-132">開啟 [命令提示字元] 視窗，並流覽至 **DropTargetVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-132">Open the command prompt window and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="b0cc9-133">輸入 `msbuild DropTargetVerb.sln`。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-133">Enter `msbuild DropTargetVerb.sln`.</span></span>

<span data-ttu-id="b0cc9-134">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="b0cc9-134">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="b0cc9-135">開啟 Windows 檔案總管，然後流覽至 **DropTargetVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-135">Open Windows Explorer and navigate to the **DropTargetVerb** project directory.</span></span>
2.  <span data-ttu-id="b0cc9-136">按兩下 DropTargetVerb .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-136">Double-click the icon for the DropTargetVerb.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="b0cc9-137">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-137">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b0cc9-138">執行範例</span><span class="sxs-lookup"><span data-stu-id="b0cc9-138">Running the Sample</span></span>

1.  <span data-ttu-id="b0cc9-139">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-139">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="b0cc9-140">在命令列中，輸入 `DropTargetVerb.exe` 。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-140">At the command line, enter `DropTargetVerb.exe`.</span></span> <span data-ttu-id="b0cc9-141">或者，從 Windows 檔案總管按兩下 DropTargetVerb.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="b0cc9-141">Alternatively, from Windows Explorer double-click the icon for DropTargetVerb.exe.</span></span>
3.  <span data-ttu-id="b0cc9-142">遵循顯示的對話方塊中的指示</span><span class="sxs-lookup"><span data-stu-id="b0cc9-142">Follow the instructions in the displayed dialog</span></span>

 

 
