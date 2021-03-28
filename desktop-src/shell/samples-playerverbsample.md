---
description: 示範如何建立可在 Shell 專案和容器上操作的動詞，以播放專案或將專案加入至佇列。
title: 播放程式動詞命令範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: ABD905DD-F216-495e-A052-E43D93DD3D6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b8346d54bfb99c5f1870812775b31097d850025f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193164"
---
# <a name="player-verb-sample"></a><span data-ttu-id="f63cf-103">播放程式動詞命令範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-103">Player Verb Sample</span></span>

<span data-ttu-id="f63cf-104">示範如何建立可在 Shell 專案和容器上操作的動詞，以播放專案或將專案加入至佇列。</span><span class="sxs-lookup"><span data-stu-id="f63cf-104">Demonstrates how to create a verb that operates on Shell items and containers which plays items or adds items to a queue.</span></span> <span data-ttu-id="f63cf-105">此範例對於媒體應用程式特別有用。</span><span class="sxs-lookup"><span data-stu-id="f63cf-105">This sample is particularly useful for media applications.</span></span>

<span data-ttu-id="f63cf-106">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="f63cf-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f63cf-107">需求</span><span class="sxs-lookup"><span data-stu-id="f63cf-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="f63cf-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="f63cf-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="f63cf-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="f63cf-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f63cf-111">Requirements</span></span>



| <span data-ttu-id="f63cf-112">產品</span><span class="sxs-lookup"><span data-stu-id="f63cf-112">Product</span></span>                                | <span data-ttu-id="f63cf-113">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="f63cf-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="f63cf-114">Windows</span><span class="sxs-lookup"><span data-stu-id="f63cf-114">Windows</span></span>                                | <span data-ttu-id="f63cf-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f63cf-115">Windows Vista</span></span>           |
| <span data-ttu-id="f63cf-116">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="f63cf-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="f63cf-117">7.0</span><span class="sxs-lookup"><span data-stu-id="f63cf-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="f63cf-118">下載範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-118">Downloading the Sample</span></span>

| <span data-ttu-id="f63cf-119">Location</span><span class="sxs-lookup"><span data-stu-id="f63cf-119">Location</span></span>      | <span data-ttu-id="f63cf-120">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="f63cf-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f63cf-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="f63cf-121">GitHub</span></span>  | [<span data-ttu-id="f63cf-122">PlayerVerb 範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-122">PlayerVerb sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlayerVerbSample) |

## <a name="building-the-sample"></a><span data-ttu-id="f63cf-123">建立範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-123">Building the Sample</span></span>

<span data-ttu-id="f63cf-124">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="f63cf-124">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="f63cf-125">開啟 [命令提示字元] 視窗，並流覽至 **PlayerVerbSample** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f63cf-125">Open the command prompt window and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="f63cf-126">輸入 `msbuild PlayerVerbSample.sln`。</span><span class="sxs-lookup"><span data-stu-id="f63cf-126">Enter `msbuild PlayerVerbSample.sln`.</span></span>

<span data-ttu-id="f63cf-127">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="f63cf-127">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="f63cf-128">開啟 Windows 檔案總管，然後流覽至 **PlayerVerbSample** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="f63cf-128">Open Windows Explorer and navigate to the **PlayerVerbSample** project directory.</span></span>
2.  <span data-ttu-id="f63cf-129">按兩下 PlayerVerbSample .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="f63cf-129">Double-click the icon for the PlayerVerbSample.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="f63cf-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="f63cf-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="f63cf-131">執行範例</span><span class="sxs-lookup"><span data-stu-id="f63cf-131">Running the Sample</span></span>

1.  <span data-ttu-id="f63cf-132">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="f63cf-132">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="f63cf-133">在命令列中，輸入 `PlayerVerbSample.exe` 。</span><span class="sxs-lookup"><span data-stu-id="f63cf-133">At the command line, enter `PlayerVerbSample.exe`.</span></span> <span data-ttu-id="f63cf-134">或者，從 Windows 檔案總管按兩下 PlayerVerbSample.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="f63cf-134">Alternatively, from Windows Explorer double-click the icon for PlayerVerbSample.exe.</span></span>
3.  <span data-ttu-id="f63cf-135">`Register Verbs`在 [**播放玩家動詞範例**] 對話方塊中選取。</span><span class="sxs-lookup"><span data-stu-id="f63cf-135">Select `Register Verbs` in the **Player Verb Sample** dialog.</span></span>
4.  <span data-ttu-id="f63cf-136">在 Windows 檔案總管中，以滑鼠右鍵按一下 [圖片專案] (的 [檔案]、[資料夾] 或 [堆疊]) ，將它們新增至佇列，或在範例應用程式中播放。</span><span class="sxs-lookup"><span data-stu-id="f63cf-136">Right-click picture items (file, folder, or stack) in Windows Explorer to add them to a queue or play them in the sample application.</span></span> <span data-ttu-id="f63cf-137">當您將範例變更為使用音樂時，請使用音樂專案。</span><span class="sxs-lookup"><span data-stu-id="f63cf-137">Use music items when you change the sample to work with music.</span></span>

 

 



