---
title: 自訂插即用範例
description: 示範如何搭配使用 Windows 動畫與您自己的自訂插即用來呈現 Direct2D。
ms.assetid: 90c4a53a-5c5e-4dcc-8946-bc8f23a07ea2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833a1a2ef09d603eaefac90b2ae25b3f533ba307
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "104092608"
---
# <a name="custom-interpolator-sample"></a><span data-ttu-id="743bf-103">自訂插即用範例</span><span class="sxs-lookup"><span data-stu-id="743bf-103">Custom Interpolator Sample</span></span>

<span data-ttu-id="743bf-104">示範如何搭配使用 Windows 動畫與您自己的自訂插即用來呈現 Direct2D。</span><span class="sxs-lookup"><span data-stu-id="743bf-104">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <span data-ttu-id="743bf-105">從圖片庫載入範例影像。</span><span class="sxs-lookup"><span data-stu-id="743bf-105">Sample images are loaded from the Picture Library.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="743bf-106">下載範例</span><span class="sxs-lookup"><span data-stu-id="743bf-106">Downloading the Sample</span></span>

<span data-ttu-id="743bf-107">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="743bf-107">This sample is available in the following locations.</span></span>



| <span data-ttu-id="743bf-108">Location</span><span class="sxs-lookup"><span data-stu-id="743bf-108">Location</span></span>                               | <span data-ttu-id="743bf-109">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="743bf-109">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="743bf-110">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="743bf-110">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="743bf-111">Microsoft Windows 軟體開發套件7。0</span><span class="sxs-lookup"><span data-stu-id="743bf-111">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="743bf-112">Code Gallery (程式碼庫)</span><span class="sxs-lookup"><span data-stu-id="743bf-112">Code Gallery</span></span>                           | [<span data-ttu-id="743bf-113">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="743bf-113">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="743bf-114">下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。</span><span class="sxs-lookup"><span data-stu-id="743bf-114">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="743bf-115">例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。</span><span class="sxs-lookup"><span data-stu-id="743bf-115">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="743bf-116">建立範例</span><span class="sxs-lookup"><span data-stu-id="743bf-116">Building the Sample</span></span>

<span data-ttu-id="743bf-117">您可以使用下列其中一種方法來建立範例。</span><span class="sxs-lookup"><span data-stu-id="743bf-117">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="743bf-118">**若要在命令提示字元中建立範例**</span><span class="sxs-lookup"><span data-stu-id="743bf-118">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="743bf-119">開啟 [命令提示字元] 視窗，並流覽至 CustomInterpolator 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="743bf-119">Open the Command Prompt window and navigate to the CustomInterpolator project directory.</span></span> <span data-ttu-id="743bf-120">例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ CustomInterpolator</span><span class="sxs-lookup"><span data-stu-id="743bf-120">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\CustomInterpolator</span></span>

2.  <span data-ttu-id="743bf-121">執行下列命令： **Msbuild CustomInterpolator .sln**</span><span class="sxs-lookup"><span data-stu-id="743bf-121">Run the following command: **msbuild CustomInterpolator.sln**</span></span>

<span data-ttu-id="743bf-122">**若要使用 Microsoft Visual Studio (慣用的來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="743bf-122">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="743bf-123">開啟 Windows 檔案總管，然後流覽至 CustomInterpolator 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="743bf-123">Open Windows Explorer and navigate to the CustomInterpolator project directory.</span></span>

    > [!Note]  
    > <span data-ttu-id="743bf-124">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="743bf-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="743bf-125">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="743bf-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

2.  <span data-ttu-id="743bf-126">按兩下 CustomInterpolator .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="743bf-126">Double-click the icon for the CustomInterpolator.sln file to open the project in Visual Studio.</span></span>

3.  <span data-ttu-id="743bf-127">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="743bf-127">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="743bf-128">執行範例</span><span class="sxs-lookup"><span data-stu-id="743bf-128">Running the Sample</span></span>

<span data-ttu-id="743bf-129">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="743bf-129">To run the sample:</span></span>

1.  <span data-ttu-id="743bf-130">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="743bf-130">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="743bf-131">在命令提示字元中執行 **CustomInterpolator.exe** ，或按兩下 Windows 檔案總管中 CustomInterpolator.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="743bf-131">Run **CustomInterpolator.exe** at the command prompt, or double-click the icon for CustomInterpolator.exe in Windows Explorer.</span></span>
3.  <span data-ttu-id="743bf-132">調整視窗大小或按空格鍵，影像會在工作區的中間隨機排列。</span><span class="sxs-lookup"><span data-stu-id="743bf-132">Resize the window or press the spacebar, and the images will arrange themselves randomly in the middle of the client area.</span></span>

4.  <span data-ttu-id="743bf-133">按向上或向下箭號，影像將會加速至工作區的頂端或底部。</span><span class="sxs-lookup"><span data-stu-id="743bf-133">Press the up or down arrow and the images will accelerate toward the top or bottom of the client area.</span></span>

 

 




