---
title: 方格版面配置範例
description: 示範如何使用 Direct2D 以動畫顯示影像的方格，以使用 Windows 動畫。
ms.assetid: f2f24058-c532-45ad-bde8-d05cfffcd505
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4d691ffa6396e294fd2dfbd07eaf9329f19519
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "103681622"
---
# <a name="grid-layout-sample"></a><span data-ttu-id="95a0c-103">方格版面配置範例</span><span class="sxs-lookup"><span data-stu-id="95a0c-103">Grid Layout Sample</span></span>

<span data-ttu-id="95a0c-104">示範如何使用 Direct2D 以動畫顯示影像的方格，以使用 Windows 動畫。</span><span class="sxs-lookup"><span data-stu-id="95a0c-104">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="95a0c-105">下載範例</span><span class="sxs-lookup"><span data-stu-id="95a0c-105">Downloading the Sample</span></span>

<span data-ttu-id="95a0c-106">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="95a0c-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="95a0c-107">Location</span><span class="sxs-lookup"><span data-stu-id="95a0c-107">Location</span></span>                               | <span data-ttu-id="95a0c-108">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="95a0c-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95a0c-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="95a0c-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="95a0c-110">Microsoft Windows 軟體開發套件7。0</span><span class="sxs-lookup"><span data-stu-id="95a0c-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="95a0c-111">Code Gallery (程式碼庫)</span><span class="sxs-lookup"><span data-stu-id="95a0c-111">Code Gallery</span></span>                           | [<span data-ttu-id="95a0c-112">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="95a0c-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="95a0c-113">下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。</span><span class="sxs-lookup"><span data-stu-id="95a0c-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="95a0c-114">例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。</span><span class="sxs-lookup"><span data-stu-id="95a0c-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="95a0c-115">建立範例</span><span class="sxs-lookup"><span data-stu-id="95a0c-115">Building the Sample</span></span>

<span data-ttu-id="95a0c-116">您可以使用下列其中一種方法來建立範例。</span><span class="sxs-lookup"><span data-stu-id="95a0c-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="95a0c-117">**若要在命令提示字元中建立範例**</span><span class="sxs-lookup"><span data-stu-id="95a0c-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="95a0c-118">開啟 [命令提示字元] 視窗，並流覽至 GridLayout 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="95a0c-118">Open the Command Prompt window and navigate to the GridLayout project directory.</span></span> <span data-ttu-id="95a0c-119">例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ GridLayout</span><span class="sxs-lookup"><span data-stu-id="95a0c-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\GridLayout</span></span>

2.  <span data-ttu-id="95a0c-120">執行下列命令： **Msbuild GridLayout .sln**</span><span class="sxs-lookup"><span data-stu-id="95a0c-120">Run the following command: **msbuild GridLayout.sln**</span></span>

<span data-ttu-id="95a0c-121">**若要使用 Microsoft Visual Studio (慣用的來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="95a0c-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="95a0c-122">開啟 Windows 檔案總管，然後流覽至 GridLayout 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="95a0c-122">Open Windows Explorer and navigate to the GridLayout project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="95a0c-123">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="95a0c-123">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="95a0c-124">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="95a0c-124">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="95a0c-125">按兩下 GridLayout .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="95a0c-125">Double-click the icon for the GridLayout.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="95a0c-126">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="95a0c-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="95a0c-127">執行範例</span><span class="sxs-lookup"><span data-stu-id="95a0c-127">Running the Sample</span></span>

<span data-ttu-id="95a0c-128">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="95a0c-128">To run the sample:</span></span>

1.  <span data-ttu-id="95a0c-129">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="95a0c-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="95a0c-130">在命令提示字元中執行 **GridLayout.exe** ，或按兩下 Windows 檔案總管中 GridLayout.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="95a0c-130">Run **GridLayout.exe** at the command prompt, or double-click the icon for GridLayout.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="95a0c-131">從圖片庫載入範例影像。</span><span class="sxs-lookup"><span data-stu-id="95a0c-131">Sample images are loaded from the Picture Library.</span></span> <span data-ttu-id="95a0c-132">調整視窗的大小，影像會在方格中排列。</span><span class="sxs-lookup"><span data-stu-id="95a0c-132">Resize the window and the images will arrange themselves into a grid.</span></span>

 

 




