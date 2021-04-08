---
description: 此範例會使用核心音訊 Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Osd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025948"
---
# <a name="osd"></a><span data-ttu-id="56a45-103">Osd</span><span class="sxs-lookup"><span data-stu-id="56a45-103">OSD</span></span>

<span data-ttu-id="56a45-104">此範例會使用核心音訊 Api 來執行螢幕顯示，以顯示透過預設音訊轉譯端點裝置播放之輸出資料流程的音量變更。</span><span class="sxs-lookup"><span data-stu-id="56a45-104">This sample uses the Core Audio APIs to implement an on-screen display that shows volume changes to the output stream that plays through the default audio-rendering endpoint device.</span></span> <span data-ttu-id="56a45-105">當使用者調整 Windows 音量控制程式中的音量層級時，會顯示幕幕畫面顯示，Sndvol.exe，且在短時間內，磁片區層級保持不變之後就會消失。</span><span class="sxs-lookup"><span data-stu-id="56a45-105">The on-screen display appears when the user adjusts the volume level in the Windows volume-control program, Sndvol.exe, and it disappears after the volume level remains unchanged for a short period.</span></span>

<span data-ttu-id="56a45-106">本主題將包含以下各節。</span><span class="sxs-lookup"><span data-stu-id="56a45-106">This topic containes the following sections.</span></span>

-   [<span data-ttu-id="56a45-107">說明</span><span class="sxs-lookup"><span data-stu-id="56a45-107">Description</span></span>](#description)
-   [<span data-ttu-id="56a45-108">需求</span><span class="sxs-lookup"><span data-stu-id="56a45-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="56a45-109">下載範例</span><span class="sxs-lookup"><span data-stu-id="56a45-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="56a45-110">建立範例</span><span class="sxs-lookup"><span data-stu-id="56a45-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="56a45-111">執行範例</span><span class="sxs-lookup"><span data-stu-id="56a45-111">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="56a45-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="56a45-112">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="56a45-113">Description</span><span class="sxs-lookup"><span data-stu-id="56a45-113">Description</span></span>

<span data-ttu-id="56a45-114">這個範例會示範下列功能。</span><span class="sxs-lookup"><span data-stu-id="56a45-114">This sample demonstrates the following features.</span></span>

-   <span data-ttu-id="56a45-115">適用于多媒體裝置列舉和選取的[MMDEVICE API](mmdevice-api.md) 。</span><span class="sxs-lookup"><span data-stu-id="56a45-115">[MMDevice API](mmdevice-api.md) for multimedia device enumeration and selection.</span></span>
-   <span data-ttu-id="56a45-116">音訊 [ENDPOINTVOLUME API](endpointvolume-api.md)</span><span class="sxs-lookup"><span data-stu-id="56a45-116">Audio [EndpointVolume API](endpointvolume-api.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="56a45-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="56a45-117">Requirements</span></span>



| <span data-ttu-id="56a45-118">產品</span><span class="sxs-lookup"><span data-stu-id="56a45-118">Product</span></span>                                                        | <span data-ttu-id="56a45-119">版本</span><span class="sxs-lookup"><span data-stu-id="56a45-119">Version</span></span>                |
|----------------------------------------------------------------|------------------------|
| [<span data-ttu-id="56a45-120">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="56a45-120">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="56a45-121">Windows Vista 或更新版本</span><span class="sxs-lookup"><span data-stu-id="56a45-121">Windows Vista or later</span></span> |
| <span data-ttu-id="56a45-122">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56a45-122">Visual Studio</span></span>                                                  | <span data-ttu-id="56a45-123">2005或更新版本</span><span class="sxs-lookup"><span data-stu-id="56a45-123">2005 or later</span></span>          |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="56a45-124">下載範例</span><span class="sxs-lookup"><span data-stu-id="56a45-124">Downloading the Sample</span></span>

<span data-ttu-id="56a45-125">下列位置提供此範例。</span><span class="sxs-lookup"><span data-stu-id="56a45-125">This sample is available in the following locations.</span></span>



| <span data-ttu-id="56a45-126">Location</span><span class="sxs-lookup"><span data-stu-id="56a45-126">Location</span></span>    | <span data-ttu-id="56a45-127">路徑/URL</span><span class="sxs-lookup"><span data-stu-id="56a45-127">Path/URL</span></span>                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="56a45-128">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="56a45-128">Windows SDK</span></span> | <span data-ttu-id="56a45-129">\\Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ 多媒體 \\ 音訊 \\ OSD \\ .。。</span><span class="sxs-lookup"><span data-stu-id="56a45-129">\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\Audio\\OSD\\...</span></span> |



 

## <a name="building-the-sample"></a><span data-ttu-id="56a45-130">建立範例</span><span class="sxs-lookup"><span data-stu-id="56a45-130">Building the Sample</span></span>

1.  <span data-ttu-id="56a45-131">開啟 Windows SDK 的 CMD shell，並變更為 OSD 範例目錄。</span><span class="sxs-lookup"><span data-stu-id="56a45-131">Open the CMD shell for the Windows SDK and change to the OSD sample directory.</span></span>
2.  <span data-ttu-id="56a45-132">在 OSD 目錄中執行 "start .OSD" 命令，以在 Visual Studio 視窗中開啟 OSD 專案。</span><span class="sxs-lookup"><span data-stu-id="56a45-132">Run the command "start OSD.sln" in the OSD directory to open the OSD project in the Visual Studio window.</span></span>
3.  <span data-ttu-id="56a45-133">從視窗內選取 [ **Debug** ] 或 [ **發行** ] 方案設定，從功能表列選取 [ **組建** ] 功能表，然後選取 [ **建立** ] 選項。</span><span class="sxs-lookup"><span data-stu-id="56a45-133">From within the window, select the **Debug** or **Release** solution configuration, select the **Build** menu from the menu bar, and select the **Build** option.</span></span> <span data-ttu-id="56a45-134">如果您未從 SDK 的 CMD shell 開啟 Visual Studio，Visual Studio 將無法存取 SDK 組建環境。</span><span class="sxs-lookup"><span data-stu-id="56a45-134">If you do not open Visual Studio from the CMD shell for the SDK, Visual Studio will not have access to the SDK build environment.</span></span> <span data-ttu-id="56a45-135">在此情況下，除非您明確設定用於專案檔 vcproj 的環境變數 MSSdk，否則此範例不會建立。</span><span class="sxs-lookup"><span data-stu-id="56a45-135">In that case, the sample will not build unless you explicitly set environment variable MSSdk, which is used in the project file, OSD.vcproj.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="56a45-136">執行範例</span><span class="sxs-lookup"><span data-stu-id="56a45-136">Running the Sample</span></span>

1.  <span data-ttu-id="56a45-137">在 Windows Vista 或更新版本中執行 OSD 可執行檔 OSD.exe。</span><span class="sxs-lookup"><span data-stu-id="56a45-137">Run the OSD executable file, OSD.exe, in Windows Vista or later.</span></span> <span data-ttu-id="56a45-138">請注意，您不會看到應用程式的系統匣圖示或視窗，但您可以使用 TaskMgr.exe 查看正在執行的進程。</span><span class="sxs-lookup"><span data-stu-id="56a45-138">Note that you will not see a system tray icon or a window for the application, but you can see the process running using TaskMgr.exe.</span></span>
2.  <span data-ttu-id="56a45-139">執行 sndvol.exe 來變更音量或靜音，或使用鍵盤控制項或隱藏控制項來變更音量。</span><span class="sxs-lookup"><span data-stu-id="56a45-139">Run sndvol.exe to change the volume or mute, or change the volume using keyboard controls or an HID control.</span></span> <span data-ttu-id="56a45-140">OSD 使用者介面隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="56a45-140">The OSD user interface is displayed.</span></span>
3.  <span data-ttu-id="56a45-141">若要結束應用程式，請執行 TaskMgr.exe、反白顯示 OSD.exe 進程，然後按一下 [ **結束處理** 程式]。</span><span class="sxs-lookup"><span data-stu-id="56a45-141">To exit the application, run TaskMgr.exe, highlight the OSD.exe process and click **End Process**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56a45-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="56a45-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56a45-143">使用核心音訊 Api 的 SDK 範例</span><span class="sxs-lookup"><span data-stu-id="56a45-143">SDK Samples That Use the Core Audio APIs</span></span>](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



