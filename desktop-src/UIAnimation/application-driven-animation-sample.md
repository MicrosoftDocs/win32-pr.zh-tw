---
title: Application-Driven 的動畫範例
description: 使用 Direct2D 以動畫顯示視窗的背景色彩，並同步處理至重新整理率，以在應用程式驅動的設定中顯示 Windows 動畫。
ms.assetid: deefc473-6749-4e2b-ad34-33ccd206d231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06b24905d09ac6559527146ebf572666a6a84f5
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2020
ms.locfileid: "106995563"
---
# <a name="application-driven-animation-sample"></a><span data-ttu-id="19cee-103">Application-Driven 的動畫範例</span><span class="sxs-lookup"><span data-stu-id="19cee-103">Application-Driven Animation Sample</span></span>

<span data-ttu-id="19cee-104">使用 Direct2D 以動畫顯示視窗的背景色彩，並同步處理至重新整理率，以在應用程式驅動的設定中顯示 Windows 動畫。</span><span class="sxs-lookup"><span data-stu-id="19cee-104">Shows Windows Animation in the application-driven configuration by using Direct2D to animate the background color of a window and syncing to the refresh rate.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="19cee-105">下載範例</span><span class="sxs-lookup"><span data-stu-id="19cee-105">Downloading the Sample</span></span>

<span data-ttu-id="19cee-106">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="19cee-106">This sample is available in the following locations.</span></span>



| <span data-ttu-id="19cee-107">Location</span><span class="sxs-lookup"><span data-stu-id="19cee-107">Location</span></span>                               | <span data-ttu-id="19cee-108">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="19cee-108">Path/URL</span></span>                                                                                          |
|----------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cee-109">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="19cee-109">Windows Software Development Kit (SDK)</span></span> | [<span data-ttu-id="19cee-110">Microsoft Windows 軟體開發套件7。0</span><span class="sxs-lookup"><span data-stu-id="19cee-110">Microsoft Windows Software Development Kit 7.0</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) |
| <span data-ttu-id="19cee-111">Code Gallery (程式碼庫)</span><span class="sxs-lookup"><span data-stu-id="19cee-111">Code Gallery</span></span>                           | [<span data-ttu-id="19cee-112">Windows 動畫管理員範例程式碼</span><span class="sxs-lookup"><span data-stu-id="19cee-112">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)          |



 

<span data-ttu-id="19cee-113">下載並安裝 Windows SDK 之後，您會在安裝目錄中找到範例。</span><span class="sxs-lookup"><span data-stu-id="19cee-113">After you have downloaded and installed the Windows SDK, you will find the samples in the installation directory.</span></span> <span data-ttu-id="19cee-114">例如，如果您使用 Windows 7 的 Windows SDK 預設安裝路徑，則範例會安裝在 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例中。</span><span class="sxs-lookup"><span data-stu-id="19cee-114">For example, if you use the default installation path for the Windows SDK for Windows 7, the samples are installed in C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="19cee-115">建立範例</span><span class="sxs-lookup"><span data-stu-id="19cee-115">Building the Sample</span></span>

<span data-ttu-id="19cee-116">您可以使用下列其中一種方法來建立範例。</span><span class="sxs-lookup"><span data-stu-id="19cee-116">Use one of the following methods to build the sample.</span></span>

<span data-ttu-id="19cee-117">**若要在命令提示字元中建立範例**</span><span class="sxs-lookup"><span data-stu-id="19cee-117">**To build the sample at the Command Prompt**</span></span>

1.  <span data-ttu-id="19cee-118">開啟 [命令提示字元] 視窗，並流覽至 AppDriven 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="19cee-118">Open the Command Prompt window and navigate to the AppDriven project directory.</span></span> <span data-ttu-id="19cee-119">例如，此範例的預設安裝路徑是 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ WindowsAnimation \\ AppDriven。</span><span class="sxs-lookup"><span data-stu-id="19cee-119">For example, the default installation path for this sample is C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WindowsAnimation\\AppDriven.</span></span>

2.  <span data-ttu-id="19cee-120">執行下列命令： **Msbuild AppDriven .sln**</span><span class="sxs-lookup"><span data-stu-id="19cee-120">Run the following command: **msbuild AppDriven.sln**</span></span>

<span data-ttu-id="19cee-121">**若要使用 Microsoft Visual Studio (慣用的來建立範例)**</span><span class="sxs-lookup"><span data-stu-id="19cee-121">**To build the sample using Microsoft Visual Studio (preferred)**</span></span>

1.  <span data-ttu-id="19cee-122">開啟 Windows 檔案總管，然後流覽至 AppDriven 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="19cee-122">Open Windows Explorer and navigate to the AppDriven project directory.</span></span>

2.  <span data-ttu-id="19cee-123">按兩下 AppDriven .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="19cee-123">Double-click the icon for the AppDriven.sln file to open the project in Visual Studio.</span></span>

    > [!Note]  
    > <span data-ttu-id="19cee-124">.Sln 副檔名不會顯示在 [預設資料夾設定] 下。</span><span class="sxs-lookup"><span data-stu-id="19cee-124">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="19cee-125">在這種情況下，它可以透過其唯一圖示或其類型描述「Microsoft Visual Studio 解決方案」來識別。</span><span class="sxs-lookup"><span data-stu-id="19cee-125">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="19cee-126">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="19cee-126">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="19cee-127">執行範例</span><span class="sxs-lookup"><span data-stu-id="19cee-127">Running the Sample</span></span>

<span data-ttu-id="19cee-128">若要執行範例：</span><span class="sxs-lookup"><span data-stu-id="19cee-128">To run the sample:</span></span>

1.  <span data-ttu-id="19cee-129">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="19cee-129">Navigate to the directory that contains the new executable, using either the command prompt or Windows Explorer.</span></span>

2.  <span data-ttu-id="19cee-130">在命令提示字元中執行 **AppDriven.exe** ，或按兩下 Windows 檔案總管中 AppDriven.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="19cee-130">Run **AppDriven.exe** at the command prompt, or double-click the icon for AppDriven.exe in Windows Explorer.</span></span>

3.  <span data-ttu-id="19cee-131">按一下工作區中的任何位置，視窗的背景色彩會變更為隨機色彩。</span><span class="sxs-lookup"><span data-stu-id="19cee-131">Click anywhere in the client area, and the background color of the window will change to a random color.</span></span>

 

 




