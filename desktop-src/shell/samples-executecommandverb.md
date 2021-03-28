---
description: 示範如何使用 ExecuteCommand 方法來執行 Shell 動詞。
title: 執行命令動詞範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0418318A-3E62-4690-AFB3-9B4A391C537E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 2deeb63fc6648d07b3d870888d6d2eabc6fb0490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195453"
---
# <a name="execute-command-verb-sample"></a><span data-ttu-id="28187-103">執行命令動詞範例</span><span class="sxs-lookup"><span data-stu-id="28187-103">Execute Command Verb Sample</span></span>

<span data-ttu-id="28187-104">示範如何使用 ExecuteCommand 方法來執行 Shell 動詞。</span><span class="sxs-lookup"><span data-stu-id="28187-104">Demonstrates how to implement a Shell verb using the ExecuteCommand method.</span></span>

<span data-ttu-id="28187-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="28187-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28187-106">說明</span><span class="sxs-lookup"><span data-stu-id="28187-106">Description</span></span>](#description)
-   [<span data-ttu-id="28187-107">需求</span><span class="sxs-lookup"><span data-stu-id="28187-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="28187-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="28187-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="28187-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="28187-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="28187-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="28187-110">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="28187-111">Description</span><span class="sxs-lookup"><span data-stu-id="28187-111">Description</span></span>

<span data-ttu-id="28187-112">這是動詞命令的慣用方法，因為它提供最大的彈性、很簡單，而且支援跨進程啟用。</span><span class="sxs-lookup"><span data-stu-id="28187-112">This method is preferred for verb implementations because it provides the most flexibility, is simple, and supports out-of-process activation.</span></span> <span data-ttu-id="28187-113">這個範例會將獨立的本機伺服器元件物件模型 (COM) 物件中，但必須將動詞執行整合到現有的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="28187-113">This sample implements a standalone, local server Component Object Model (COM) object, but it is expected that the verb implementation will be integrated into existing applications.</span></span> <span data-ttu-id="28187-114">若要這樣做，您的主要應用程式物件必須自行註冊 class factory。</span><span class="sxs-lookup"><span data-stu-id="28187-114">To do so, your main application object must register a class factory for itself.</span></span> <span data-ttu-id="28187-115">該物件會針對您的應用程式動詞來實行 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="28187-115">That object implements [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) for your application's verbs.</span></span> <span data-ttu-id="28187-116">請注意，如果您的應用程式尚未執行，COM 會啟動應用程式，但如果有的話，則會連接到應用程式的執行中實例。</span><span class="sxs-lookup"><span data-stu-id="28187-116">Note that COM launches your application if it is not already running but connects to a running instance of your application if one is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="28187-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="28187-117">Requirements</span></span>



| <span data-ttu-id="28187-118">產品</span><span class="sxs-lookup"><span data-stu-id="28187-118">Product</span></span>                                | <span data-ttu-id="28187-119">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="28187-119">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="28187-120">Windows</span><span class="sxs-lookup"><span data-stu-id="28187-120">Windows</span></span>                                | <span data-ttu-id="28187-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="28187-121">Windows 7</span></span>               |
| <span data-ttu-id="28187-122">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="28187-122">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="28187-123">7.0</span><span class="sxs-lookup"><span data-stu-id="28187-123">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="28187-124">下載範例</span><span class="sxs-lookup"><span data-stu-id="28187-124">Downloading the Sample</span></span>

| <span data-ttu-id="28187-125">Location</span><span class="sxs-lookup"><span data-stu-id="28187-125">Location</span></span>      | <span data-ttu-id="28187-126">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="28187-126">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28187-127">GitHub</span><span class="sxs-lookup"><span data-stu-id="28187-127">GitHub</span></span>  | [<span data-ttu-id="28187-128">ExecuteCommandVerb 範例</span><span class="sxs-lookup"><span data-stu-id="28187-128">ExecuteCommandVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/ExecuteCommandVerb) |

## <a name="building-the-sample"></a><span data-ttu-id="28187-129">建立範例</span><span class="sxs-lookup"><span data-stu-id="28187-129">Building the Sample</span></span>

<span data-ttu-id="28187-130">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="28187-130">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="28187-131">開啟 [命令提示字元] 視窗，並流覽至 **ExecuteCommandVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="28187-131">Open the command prompt window and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="28187-132">輸入 `msbuild ExecuteCommand.sln`。</span><span class="sxs-lookup"><span data-stu-id="28187-132">Enter `msbuild ExecuteCommand.sln`.</span></span>

<span data-ttu-id="28187-133">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="28187-133">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="28187-134">開啟 Windows 檔案總管，然後流覽至 **ExecuteCommandVerb** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="28187-134">Open Windows Explorer and navigate to the **ExecuteCommandVerb** project directory.</span></span>
2.  <span data-ttu-id="28187-135">按兩下 ExecuteCommand .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="28187-135">Double-click the icon for the ExecuteCommand.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="28187-136">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="28187-136">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="28187-137">執行範例</span><span class="sxs-lookup"><span data-stu-id="28187-137">Running the Sample</span></span>

1.  <span data-ttu-id="28187-138">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="28187-138">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="28187-139">在命令列中，輸入 `ExecuteCommand.exe` 。</span><span class="sxs-lookup"><span data-stu-id="28187-139">At the command line, enter `ExecuteCommand.exe`.</span></span> <span data-ttu-id="28187-140">或者，從 Windows 檔案總管按兩下 ExecuteCommand.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="28187-140">Alternatively, from Windows Explorer double-click the icon for ExecuteCommand.exe.</span></span>
3.  <span data-ttu-id="28187-141">遵循顯示的對話方塊中的指示</span><span class="sxs-lookup"><span data-stu-id="28187-141">Follow the instructions in the displayed dialog</span></span>

 

 
