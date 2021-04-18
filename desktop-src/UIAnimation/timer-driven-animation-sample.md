---
title: Timer-Driven 的動畫範例
description: 顯示如何使用 Windows 動畫搭配動畫計時器，同時使用 GDI + 以動畫顯示視窗的背景色彩。
ms.assetid: c50a4bfb-855b-4837-a117-84f412943b14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec145b087a112c7482de3a749c690a1824195ea3
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "104314584"
---
# <a name="timer-driven-animation-sample"></a><span data-ttu-id="c0334-103">Timer-Driven 的動畫範例</span><span class="sxs-lookup"><span data-stu-id="c0334-103">Timer-Driven Animation Sample</span></span>

<span data-ttu-id="c0334-104">顯示如何使用 Windows 動畫搭配動畫計時器，同時使用 GDI + 以動畫顯示視窗的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="c0334-104">Shows how to use Windows Animation with the Animation Timer, while using GDI+ to animate the background color of a window.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="c0334-105">下載範例</span><span class="sxs-lookup"><span data-stu-id="c0334-105">Downloading the Sample</span></span>

<span data-ttu-id="c0334-106">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="c0334-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="c0334-107">Location</span><span class="sxs-lookup"><span data-stu-id="c0334-107">Location</span></span>                               | <span data-ttu-id="c0334-108">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="c0334-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0334-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="c0334-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="c0334-110">Microsoft Windows 軟體開發套件7。0</span><span class="sxs-lookup"><span data-stu-id="c0334-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="c0334-111">Code Gallery (程式碼庫)</span><span class="sxs-lookup"><span data-stu-id="c0334-111">Code Gallery</span></span>                           | [<span data-ttu-id="c0334-112">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="c0334-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)         |



 

<span data-ttu-id="c0334-113">下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。</span><span class="sxs-lookup"><span data-stu-id="c0334-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="c0334-114">例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。</span><span class="sxs-lookup"><span data-stu-id="c0334-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="c0334-115">建立範例</span><span class="sxs-lookup"><span data-stu-id="c0334-115">Building the Sample</span></span>

<span data-ttu-id="c0334-116">您可以使用下列其中一種方法來建立範例。</span><span class="sxs-lookup"><span data-stu-id="c0334-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="c0334-117">**若要在命令提示字元中建立範例**</span><span class="sxs-lookup"><span data-stu-id="c0334-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="c0334-118">開啟 [命令提示字元] 視窗，並流覽至 TimerDriven 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="c0334-118">Open the Command Prompt window and navigate to the TimerDriven project directory.</span></span> <span data-ttu-id="c0334-119">例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ TimerDriven。</span><span class="sxs-lookup"><span data-stu-id="c0334-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\TimerDriven.</span></span>

2.  <span data-ttu-id="c0334-120">執行下列命令： **Msbuild TimerDriven .sln**</span><span class="sxs-lookup"><span data-stu-id="c0334-120">Run the following command: **msbuild TimerDriven.sln**</span></span>

<span data-ttu-id="c0334-121">**若要使用 Microsoft Visual Studio (慣用的來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="c0334-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="c0334-122">開啟 Windows 檔案總管，然後流覽至 TimerDriven 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="c0334-122">Open Windows Explorer and navigate to the TimerDriven project directory.</span></span>

2.  <span data-ttu-id="c0334-123">按兩下 TimerDriven .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="c0334-123">Double-click the icon for the TimerDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="c0334-124">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="c0334-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="c0334-125">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="c0334-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="c0334-126">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="c0334-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="c0334-127">執行範例</span><span class="sxs-lookup"><span data-stu-id="c0334-127">Running the Sample</span></span>

<span data-ttu-id="c0334-128">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="c0334-128">To run the sample:</span></span>

1.  <span data-ttu-id="c0334-129">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="c0334-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="c0334-130">在命令提示字元中執行 **TimerDriven.exe** ，或按兩下 Windows 檔案總管中 TimerDriven.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="c0334-130">Run **TimerDriven.exe** at the command prompt, or double-click the icon for TimerDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="c0334-131">按一下工作區中的任何位置，視窗的背景色彩會變更為隨機色彩。</span><span class="sxs-lookup"><span data-stu-id="c0334-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




