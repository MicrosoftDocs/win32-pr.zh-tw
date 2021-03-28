---
description: 示範如何建立在選取的 Shell 專案或容器上操作的動詞，以建立播放清單。
title: 播放清單建立者範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5c5e4f6570faff459126a32ea4680d41a3b8302e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973833"
---
# <a name="playlist-creator-sample"></a><span data-ttu-id="4d88a-103">播放清單建立者範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-103">Playlist Creator Sample</span></span>

<span data-ttu-id="4d88a-104">示範如何建立在選取的 Shell 專案或容器上操作的動詞，以建立播放清單。</span><span class="sxs-lookup"><span data-stu-id="4d88a-104">Demonstrates how to create a verb that operates on a selected Shell item or container to create a playlist.</span></span>

<span data-ttu-id="4d88a-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="4d88a-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d88a-106">需求</span><span class="sxs-lookup"><span data-stu-id="4d88a-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4d88a-107">下載範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4d88a-108">建立範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4d88a-109">執行範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="4d88a-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d88a-110">Requirements</span></span>



| <span data-ttu-id="4d88a-111">產品</span><span class="sxs-lookup"><span data-stu-id="4d88a-111">Product</span></span>                                | <span data-ttu-id="4d88a-112">最小產品版本</span><span class="sxs-lookup"><span data-stu-id="4d88a-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4d88a-113">Windows</span><span class="sxs-lookup"><span data-stu-id="4d88a-113">Windows</span></span>                                | <span data-ttu-id="4d88a-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d88a-114">Windows Vista</span></span>           |
| <span data-ttu-id="4d88a-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="4d88a-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4d88a-116">7.0</span><span class="sxs-lookup"><span data-stu-id="4d88a-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="4d88a-117">下載範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-117">Downloading the Sample</span></span>

| <span data-ttu-id="4d88a-118">Location</span><span class="sxs-lookup"><span data-stu-id="4d88a-118">Location</span></span>      | <span data-ttu-id="4d88a-119">路徑 URL</span><span class="sxs-lookup"><span data-stu-id="4d88a-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d88a-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="4d88a-120">GitHub</span></span>  | [<span data-ttu-id="4d88a-121">PlaylistCreator 範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-121">PlaylistCreator sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a><span data-ttu-id="4d88a-122">建立範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-122">Building the Sample</span></span>

<span data-ttu-id="4d88a-123">若要從命令提示字元建立範例：</span><span class="sxs-lookup"><span data-stu-id="4d88a-123">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="4d88a-124">開啟 [命令提示字元] 視窗，並流覽至 **PlaylistCreator** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="4d88a-124">Open the command prompt window and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="4d88a-125">輸入 `msbuild PlaylistCreator.sln`。</span><span class="sxs-lookup"><span data-stu-id="4d88a-125">Enter `msbuild PlaylistCreator.sln`.</span></span>

<span data-ttu-id="4d88a-126">若要使用 Microsoft Visual Studio (慣用的) 來建立範例：</span><span class="sxs-lookup"><span data-stu-id="4d88a-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

> [!Note]  
> <span data-ttu-id="4d88a-127">如果無法使用完整的 Visual Studio，此範例也可以搭配 Visual C++ Express 版本使用。</span><span class="sxs-lookup"><span data-stu-id="4d88a-127">This sample can also be used with the Visual C++ Express Edition if the full Visual Studio is not available.</span></span>

 

1.  <span data-ttu-id="4d88a-128">開啟 Windows 檔案總管，然後流覽至 **PlaylistCreator** 專案目錄。</span><span class="sxs-lookup"><span data-stu-id="4d88a-128">Open Windows Explorer and navigate to the **PlaylistCreator** project directory.</span></span>
2.  <span data-ttu-id="4d88a-129">按兩下 PlaylistCreator .sln 檔案的圖示，在 Visual Studio 中開啟專案。</span><span class="sxs-lookup"><span data-stu-id="4d88a-129">Double-click the icon for the PlaylistCreator.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="4d88a-130">從 [ **組建** ] 功能表選取 [ **建立方案**]。</span><span class="sxs-lookup"><span data-stu-id="4d88a-130">From the **Build** menu, select **Build Solution**.</span></span>
    > [!Note]  
    > <span data-ttu-id="4d88a-131">如果您要使用 Visual C++ Express Edition 編譯64位，您必須使用 Windows SDK 提供的 x64 跨編譯器。</span><span class="sxs-lookup"><span data-stu-id="4d88a-131">If you are compiling 64-bit using the Visual C++ Express Edition, you must to use the x64 cross-compiler supplied with the Windows SDK.</span></span>

     

## <a name="running-the-sample"></a><span data-ttu-id="4d88a-132">執行範例</span><span class="sxs-lookup"><span data-stu-id="4d88a-132">Running the Sample</span></span>

1.  <span data-ttu-id="4d88a-133">使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。</span><span class="sxs-lookup"><span data-stu-id="4d88a-133">Navigate to the directory that contains the new executable, using the command prompt or Windows Explorer.</span></span>
2.  <span data-ttu-id="4d88a-134">在命令列中，輸入 `PlaylistCreator.exe` 。</span><span class="sxs-lookup"><span data-stu-id="4d88a-134">At the command line, enter `PlaylistCreator.exe`.</span></span> <span data-ttu-id="4d88a-135">或者，從 Windows 檔案總管按兩下 PlaylistCreator.exe 的圖示。</span><span class="sxs-lookup"><span data-stu-id="4d88a-135">Alternatively, from Windows Explorer double-click the icon for PlaylistCreator.exe.</span></span>
3.  <span data-ttu-id="4d88a-136">在 Windows 檔案總管中，以滑鼠右鍵按一下包含音樂檔案的任何音樂檔或資料夾，以建立播放清單來顯示內容功能表</span><span class="sxs-lookup"><span data-stu-id="4d88a-136">Right-click any music file or folder containing music files in Windows Explorer to create a playlist to bring up the context menu</span></span>
4.  <span data-ttu-id="4d88a-137">您可以建立 m3u 或. .wpl 播放清單。</span><span class="sxs-lookup"><span data-stu-id="4d88a-137">You can create a .m3u or .wpl playlist.</span></span> <span data-ttu-id="4d88a-138">播放清單會在資料夾中建立 `%userprofile%\Music\Playlists` 。</span><span class="sxs-lookup"><span data-stu-id="4d88a-138">Playlists are created in the `%userprofile%\Music\Playlists` folder.</span></span>
    > [!Note]  
    > <span data-ttu-id="4d88a-139">在內容功能表中，您可以在 [ **音樂** ] 資料夾、音樂堆疊、 **音樂媒體** 櫃中的堆疊，以及音樂檔案的集合中找到新的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="4d88a-139">New verbs in the context menu can be found in the **Music** folder, music stacks, stacks in the **Music Library**, and collections of music files.</span></span>

     

 

 



