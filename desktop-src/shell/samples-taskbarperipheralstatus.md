---
description: 示範工作列圖示重迭和進度列。
title: 工作列週邊設備狀態範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991746"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="027ea-103">工作列週邊設備狀態範例</span><span class="sxs-lookup"><span data-stu-id="027ea-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="027ea-104">示範工作列圖示重迭和進度列。</span><span class="sxs-lookup"><span data-stu-id="027ea-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="027ea-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="027ea-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="027ea-106">說明</span><span class="sxs-lookup"><span data-stu-id="027ea-106">Description</span></span>](#description)
-   [<span data-ttu-id="027ea-107">需求</span><span class="sxs-lookup"><span data-stu-id="027ea-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="027ea-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="027ea-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="027ea-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="027ea-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="027ea-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="027ea-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="027ea-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="027ea-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="027ea-112">Description</span><span class="sxs-lookup"><span data-stu-id="027ea-112">Description</span></span>

<span data-ttu-id="027ea-113">這個範例會建立一個範例工作列按鈕，其示範如何使用 [**ITaskbarList3：： SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) ，方法是讓您套用從功能表中選擇的各種重迭。</span><span class="sxs-lookup"><span data-stu-id="027ea-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="027ea-114">此範例也提供在按鈕上模擬進度指標的選項，示範如何使用 [**ITaskbarList3：： SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) 和 [**ITaskbarList3：： SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) ，方法是先顯示不定的進度指標 (TBPF \_ 不定) ，然後使用一般比例指標 (TBPF \_ 正常) 。</span><span class="sxs-lookup"><span data-stu-id="027ea-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="027ea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="027ea-115">Requirements</span></span>



| <span data-ttu-id="027ea-116">產品</span><span class="sxs-lookup"><span data-stu-id="027ea-116">Product</span></span>                                | <span data-ttu-id="027ea-117">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="027ea-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="027ea-118">Windows</span><span class="sxs-lookup"><span data-stu-id="027ea-118">Windows</span></span>                                | <span data-ttu-id="027ea-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="027ea-119">Windows 7</span></span>               |
| <span data-ttu-id="027ea-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="027ea-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="027ea-121">7.0</span><span class="sxs-lookup"><span data-stu-id="027ea-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="027ea-122">下載範例</span><span class="sxs-lookup"><span data-stu-id="027ea-122">Downloading the Sample</span></span>

| <span data-ttu-id="027ea-123">Location</span><span class="sxs-lookup"><span data-stu-id="027ea-123">Location</span></span>      | <span data-ttu-id="027ea-124">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="027ea-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027ea-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="027ea-125">GitHub</span></span>  | [<span data-ttu-id="027ea-126">TaskBarPeripheralStatus 範例</span><span class="sxs-lookup"><span data-stu-id="027ea-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="027ea-127">建立範例</span><span class="sxs-lookup"><span data-stu-id="027ea-127">Building the Sample</span></span>

<span data-ttu-id="027ea-128">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="027ea-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="027ea-129">開啟 [命令提示字元] 視窗，並流覽至 **TaskbarPeripheralStatus** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="027ea-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="027ea-130">輸入 `msbuild PeripheralStatus.sln`。</span><span class="sxs-lookup"><span data-stu-id="027ea-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="027ea-131">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="027ea-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="027ea-132">開啟 Windows 檔案總管，然後流覽至 **TaskbarPeripheralStatus** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="027ea-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="027ea-133">按兩下 PeripheralStatus .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="027ea-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="027ea-134">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="027ea-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="027ea-135">執行範例</span><span class="sxs-lookup"><span data-stu-id="027ea-135">Running the Sample</span></span>

1.  <span data-ttu-id="027ea-136">流覽至包含新可執行檔的目錄， (例如， `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`) ，請使用命令提示字元或 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="027ea-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="027ea-137">如果使用命令列，請輸入 `PeripheralStatus.exe` 。</span><span class="sxs-lookup"><span data-stu-id="027ea-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="027ea-138">如果使用 Windows 檔案總管，請按兩下 PeripheralStatus.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="027ea-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="027ea-139">新視窗隨即開啟，其中會有相關聯的工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="027ea-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="027ea-140">若要示範重迭，請從視窗的 [**週邊狀態**] 功能表選擇 [重迭 **1** ] 或 [重迭 **2** ]</span><span class="sxs-lookup"><span data-stu-id="027ea-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="027ea-141">選擇的重迭會出現在工作列按鈕上。</span><span class="sxs-lookup"><span data-stu-id="027ea-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="027ea-142">若要移除重迭，請選擇 [ **清除** 覆迭]。</span><span class="sxs-lookup"><span data-stu-id="027ea-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="027ea-143">若要示範進度列，請從視窗的 [**週邊狀態**] 功能表選擇 [**模擬進度**]。</span><span class="sxs-lookup"><span data-stu-id="027ea-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="027ea-144">工作列按鈕會顯示不定的進度指示器，然後切換至一般指標。</span><span class="sxs-lookup"><span data-stu-id="027ea-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="027ea-145">從視窗 **的 [** 檔案]**功能表選擇 [** 結束]，以結束程式。</span><span class="sxs-lookup"><span data-stu-id="027ea-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="027ea-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="027ea-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="027ea-147">工作列擴充功能</span><span class="sxs-lookup"><span data-stu-id="027ea-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



