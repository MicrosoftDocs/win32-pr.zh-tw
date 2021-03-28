---
description: 示範縮圖工具列、內嵌于視窗縮圖預覽中的作用中工具列控制項，用來提供視窗的按鍵命令存取權，而不需要使用者還原或啟動應用程式的視窗。
title: 工作列縮圖工具列範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973533"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="ca020-103">工作列縮圖工具列範例</span><span class="sxs-lookup"><span data-stu-id="ca020-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="ca020-104">示範縮圖工具列、內嵌于視窗縮圖預覽中的作用中工具列控制項，用來提供視窗的按鍵命令存取權，而不需要使用者還原或啟動應用程式的視窗。</span><span class="sxs-lookup"><span data-stu-id="ca020-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="ca020-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="ca020-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ca020-106">說明</span><span class="sxs-lookup"><span data-stu-id="ca020-106">Description</span></span>](#description)
-   [<span data-ttu-id="ca020-107">需求</span><span class="sxs-lookup"><span data-stu-id="ca020-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ca020-108">下載範例</span><span class="sxs-lookup"><span data-stu-id="ca020-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="ca020-109">建立範例</span><span class="sxs-lookup"><span data-stu-id="ca020-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="ca020-110">執行範例</span><span class="sxs-lookup"><span data-stu-id="ca020-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="ca020-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca020-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="ca020-112">Description</span><span class="sxs-lookup"><span data-stu-id="ca020-112">Description</span></span>

<span data-ttu-id="ca020-113">這個範例示範如何提供簡單的工具列給工作列縮圖預覽。</span><span class="sxs-lookup"><span data-stu-id="ca020-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="ca020-114">工具列包含三個按鈕。</span><span class="sxs-lookup"><span data-stu-id="ca020-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="ca020-115">按一下按鈕會顯示一個視窗，以確認按鈕已啟用。</span><span class="sxs-lookup"><span data-stu-id="ca020-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="ca020-116">以下是示範的 Api：</span><span class="sxs-lookup"><span data-stu-id="ca020-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="ca020-117">**ITaskbarList3::ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="ca020-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="ca020-118">**ITaskbarList3::ThumbBarSetImageList**</span><span class="sxs-lookup"><span data-stu-id="ca020-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="ca020-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) 結構</span><span class="sxs-lookup"><span data-stu-id="ca020-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="ca020-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca020-120">Requirements</span></span>



| <span data-ttu-id="ca020-121">產品</span><span class="sxs-lookup"><span data-stu-id="ca020-121">Product</span></span>                                | <span data-ttu-id="ca020-122">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="ca020-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="ca020-123">Windows</span><span class="sxs-lookup"><span data-stu-id="ca020-123">Windows</span></span>                                | <span data-ttu-id="ca020-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca020-124">Windows 7</span></span>               |
| <span data-ttu-id="ca020-125">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="ca020-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="ca020-126">7.0</span><span class="sxs-lookup"><span data-stu-id="ca020-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="ca020-127">下載範例</span><span class="sxs-lookup"><span data-stu-id="ca020-127">Downloading the Sample</span></span>

| <span data-ttu-id="ca020-128">Location</span><span class="sxs-lookup"><span data-stu-id="ca020-128">Location</span></span>      | <span data-ttu-id="ca020-129">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="ca020-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca020-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="ca020-130">GitHub</span></span>  | [<span data-ttu-id="ca020-131">TaskbarThumbnailToolbar 範例</span><span class="sxs-lookup"><span data-stu-id="ca020-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="ca020-132">建立範例</span><span class="sxs-lookup"><span data-stu-id="ca020-132">Building the Sample</span></span>

<span data-ttu-id="ca020-133">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="ca020-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="ca020-134">開啟 [命令提示字元] 視窗，並流覽至 **TaskbarThumbnailToolbar** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="ca020-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="ca020-135">輸入 `msbuild ThumbnailToolbar.sln`。</span><span class="sxs-lookup"><span data-stu-id="ca020-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="ca020-136">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="ca020-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="ca020-137">開啟 Windows 檔案總管，然後流覽至 **TaskbarThumbnailToolbar** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="ca020-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="ca020-138">按兩下 ThumbnailToolbar .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="ca020-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="ca020-139">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="ca020-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ca020-140">執行範例</span><span class="sxs-lookup"><span data-stu-id="ca020-140">Running the Sample</span></span>

1.  <span data-ttu-id="ca020-141">流覽至包含新可執行檔的目錄， (例如， `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`) ，請使用命令提示字元或 Windows 檔案總管。</span><span class="sxs-lookup"><span data-stu-id="ca020-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="ca020-142">如果使用命令列，請輸入 `ThumbnailToolbar.exe` 。</span><span class="sxs-lookup"><span data-stu-id="ca020-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="ca020-143">如果使用 Windows 檔案總管，請按兩下 ThumbnailToolbar.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="ca020-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="ca020-144">新視窗隨即開啟，其中會有相關聯的工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="ca020-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="ca020-145">將游標停留在 **ThumbnailToolbar** 工作列按鈕上，讓預覽顯示。</span><span class="sxs-lookup"><span data-stu-id="ca020-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="ca020-146">按一下三個按鈕的其中一個 (綠色、黃色、紅色) 顯示在預覽的工具列中。</span><span class="sxs-lookup"><span data-stu-id="ca020-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="ca020-147">從視窗 **的 [** 檔案]**功能表選擇 [** 結束]，以結束程式。</span><span class="sxs-lookup"><span data-stu-id="ca020-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ca020-148">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca020-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca020-149">工作列擴充功能</span><span class="sxs-lookup"><span data-stu-id="ca020-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



