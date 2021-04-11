---
title: 優先順序比較範例
description: 示範如何使用 Direct2D 轉譯來搭配使用 Windows 動畫與您自己的優先順序比較。
ms.assetid: aa09f8a7-1919-4a44-832f-be8b848d6a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfcb20785d6a4c3c3384b85327a0e27d93c58d7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "104092607"
---
# <a name="priority-comparison-sample"></a><span data-ttu-id="db12d-103">優先順序比較範例</span><span class="sxs-lookup"><span data-stu-id="db12d-103">Priority Comparison Sample</span></span>

<span data-ttu-id="db12d-104">示範如何使用 Direct2D 轉譯來搭配使用 Windows 動畫與您自己的優先順序比較。</span><span class="sxs-lookup"><span data-stu-id="db12d-104">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="db12d-105">下載範例</span><span class="sxs-lookup"><span data-stu-id="db12d-105">Downloading the Sample</span></span>

<span data-ttu-id="db12d-106">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="db12d-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="db12d-107">Location</span><span class="sxs-lookup"><span data-stu-id="db12d-107">Location</span></span>                               | <span data-ttu-id="db12d-108">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="db12d-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db12d-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="db12d-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="db12d-110">Microsoft Windows 軟體開發套件7。0</span><span class="sxs-lookup"><span data-stu-id="db12d-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="db12d-111">Code Gallery (程式碼庫)</span><span class="sxs-lookup"><span data-stu-id="db12d-111">Code Gallery</span></span>                           | [<span data-ttu-id="db12d-112">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="db12d-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="db12d-113">下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。</span><span class="sxs-lookup"><span data-stu-id="db12d-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="db12d-114">例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。</span><span class="sxs-lookup"><span data-stu-id="db12d-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="db12d-115">建立範例</span><span class="sxs-lookup"><span data-stu-id="db12d-115">Building the Sample</span></span>

<span data-ttu-id="db12d-116">您可以使用下列其中一種方法來建立範例。</span><span class="sxs-lookup"><span data-stu-id="db12d-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="db12d-117">**若要在命令提示字元中建立範例**</span><span class="sxs-lookup"><span data-stu-id="db12d-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="db12d-118">開啟 [命令提示字元] 視窗，並流覽至 PriorityComparison 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="db12d-118">Open the Command Prompt window and navigate to the PriorityComparison project directory.</span></span> <span data-ttu-id="db12d-119">例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ PriorityComparison。</span><span class="sxs-lookup"><span data-stu-id="db12d-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\PriorityComparison.</span></span>

2.  <span data-ttu-id="db12d-120">執行下列命令： **Msbuild PriorityComparison .sln**</span><span class="sxs-lookup"><span data-stu-id="db12d-120">Run the following command: **msbuild PriorityComparison.sln**</span></span>

<span data-ttu-id="db12d-121">**若要使用 Microsoft Visual Studio (慣用的來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="db12d-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="db12d-122">開啟 Windows 檔案總管，然後流覽至 PriorityComparison 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="db12d-122">Open Windows Explorer and navigate to the PriorityComparison project directory.</span></span>

2.  <span data-ttu-id="db12d-123">按兩下 PriorityComparison .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="db12d-123">Double-click the icon for the PriorityComparison.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="db12d-124">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="db12d-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="db12d-125">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="db12d-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="db12d-126">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="db12d-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="db12d-127">執行範例</span><span class="sxs-lookup"><span data-stu-id="db12d-127">Running the Sample</span></span>

<span data-ttu-id="db12d-128">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="db12d-128">To run the sample:</span></span>

1.  <span data-ttu-id="db12d-129">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="db12d-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="db12d-130">在命令提示字元中執行 **PriorityComparison.exe** ，或按兩下 Windows 檔案總管中 PriorityComparison.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="db12d-130">Run **PriorityComparison.exe** at the command prompt, or double-click the icon for PriorityComparison.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="db12d-131">從圖片庫載入範例影像。</span><span class="sxs-lookup"><span data-stu-id="db12d-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="db12d-132">調整視窗大小或按空格鍵，影像將移至中央。</span><span class="sxs-lookup"><span data-stu-id="db12d-132">Resize the window or press the spacebar and the images will move to the center.</span></span>

4.  <span data-ttu-id="db12d-133">您可以使用向左鍵和向右鍵來選取不同的影像， (選取的速度越快越好，) 選取的速度就愈快。</span><span class="sxs-lookup"><span data-stu-id="db12d-133">Use the left and right arrow keys to select different images (the faster the key is pressed the faster the selection will change).</span></span>

5.  <span data-ttu-id="db12d-134">使用向上鍵和向下鍵，透過影像建立 wave (按下按鍵的速度越快，wave) 的速度就愈快。</span><span class="sxs-lookup"><span data-stu-id="db12d-134">Use the up and down arrow keys to create a wave through the images (the faster the key is pressed, the faster the wave).</span></span>

 

 




