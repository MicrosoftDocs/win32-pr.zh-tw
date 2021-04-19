---
description: DirectShow 的新功能
ms.assetid: 675a34d4-7a33-4125-86af-cd4ed73ad430
title: DirectShow 的新功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74747349848a7b370cd4766113085c84d0c7a1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989069"
---
# <a name="whats-new-in-directshow"></a><span data-ttu-id="85c22-103">DirectShow 的新功能</span><span class="sxs-lookup"><span data-stu-id="85c22-103">What's New in DirectShow</span></span>

## <a name="whats-new-for-directshow-in-windows-7"></a><span data-ttu-id="85c22-104">Windows 7 中的 DirectShow 新功能</span><span class="sxs-lookup"><span data-stu-id="85c22-104">What's New for DirectShow in Windows 7</span></span>

<span data-ttu-id="85c22-105">新介面：</span><span class="sxs-lookup"><span data-stu-id="85c22-105">New interfaces:</span></span>

-   [<span data-ttu-id="85c22-106">**IAMAsyncReaderTimestampScaling**</span><span class="sxs-lookup"><span data-stu-id="85c22-106">**IAMAsyncReaderTimestampScaling**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling)
-   [<span data-ttu-id="85c22-107">**IAMPluginControl**</span><span class="sxs-lookup"><span data-stu-id="85c22-107">**IAMPluginControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol)

<span data-ttu-id="85c22-108">新的或更新的篩選：</span><span class="sxs-lookup"><span data-stu-id="85c22-108">New or updated filters:</span></span>

-   [<span data-ttu-id="85c22-109">**Microsoft MPEG-1/DD/AAC 音訊解碼器**</span><span class="sxs-lookup"><span data-stu-id="85c22-109">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](microsoft-mpeg-1-dd-audio-decoder.md)
-   [<span data-ttu-id="85c22-110">**Microsoft MPEG-2 影片解碼**</span><span class="sxs-lookup"><span data-stu-id="85c22-110">**Microsoft MPEG-2 Video Decoder**</span></span>](microsoft-mpeg-2-video-decoder.md)

<span data-ttu-id="85c22-111">"智慧型 connect" 演算法已經過修改，可支援慣用和封鎖的篩選。</span><span class="sxs-lookup"><span data-stu-id="85c22-111">The "intelligent connect" algorithms have been modified to support preferred and blocked filters.</span></span> <span data-ttu-id="85c22-112">如需詳細資訊，請參閱 [智慧型 Connect](intelligent-connect.md)。</span><span class="sxs-lookup"><span data-stu-id="85c22-112">For details, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="85c22-113">DVD 播放： [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) 方法的新選項。</span><span class="sxs-lookup"><span data-stu-id="85c22-113">DVD playback: New options for the [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) method.</span></span>

## <a name="whats-new-for-directshow-in-windows-vista"></a><span data-ttu-id="85c22-114">Windows Vista 中的 DirectShow 新功能</span><span class="sxs-lookup"><span data-stu-id="85c22-114">What's New for DirectShow in Windows Vista</span></span>

-   <span data-ttu-id="85c22-115">DirectShow 現在是 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="85c22-115">DirectShow is now part of the Windows SDK.</span></span> <span data-ttu-id="85c22-116">您不再將 DirectShow 標頭、程式庫、範例和工具組含在 DirectX SDK 中。</span><span class="sxs-lookup"><span data-stu-id="85c22-116">The DirectShow headers, libraries, samples, and tools are no longer included in the DirectX SDK.</span></span>
-   <span data-ttu-id="85c22-117">DirectX Video 加速 (DXVA) 2.0 包含許多來自 DXVA 1.0 的增強功能。</span><span class="sxs-lookup"><span data-stu-id="85c22-117">DirectX Video Acceleration (DXVA) 2.0 contains many enhancements from DXVA 1.0.</span></span>

    -   <span data-ttu-id="85c22-118">硬體視頻管線已大幅改進。</span><span class="sxs-lookup"><span data-stu-id="85c22-118">The hardware video pipeline has been significantly improved.</span></span>
    -   <span data-ttu-id="85c22-119">例如，您可以直接存取 DXVA 2.0 的元件，而不需要透過影片轉譯器進行通訊。</span><span class="sxs-lookup"><span data-stu-id="85c22-119">Components such as decoders can access DXVA 2.0 directly without communicating through the video renderer.</span></span>
    -   <span data-ttu-id="85c22-120">Direct3D 裝置管理員可讓元件共用相同的 Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="85c22-120">The Direct3D Device Manager enables components to share the same Direct3D device.</span></span>

    <span data-ttu-id="85c22-121">如需 DXVA 2.0 的詳細資訊，請參閱 [DirectX Video 加速 2.0](../medfound/directx-video-acceleration-2-0.md) 檔，這是 [Microsoft 媒體基礎](../medfound/microsoft-media-foundation-sdk.md) 檔的一部分。</span><span class="sxs-lookup"><span data-stu-id="85c22-121">For more information about DXVA 2.0, see the [DirectX Video Acceleration 2.0](../medfound/directx-video-acceleration-2-0.md) documentation, which is part of the [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>

-   <span data-ttu-id="85c22-122">[**增強型影片**](enhanced-video-renderer-filter.md)轉譯器 (EVR) 是一種功能強大的新影片轉譯器，它會與媒體基礎版本的 EVR 共用相同的外掛程式模型。</span><span class="sxs-lookup"><span data-stu-id="85c22-122">The [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) is a powerful new video renderer, which shares the same plug-in model as the Media Foundation version of the EVR.</span></span> <span data-ttu-id="85c22-123">如需 EVR 的詳細資訊，請參閱 [Microsoft 媒體基礎](../medfound/microsoft-media-foundation-sdk.md) 檔。</span><span class="sxs-lookup"><span data-stu-id="85c22-123">For more information about the EVR, see the [Microsoft Media Foundation](../medfound/microsoft-media-foundation-sdk.md) documentation.</span></span>
-   <span data-ttu-id="85c22-124">Windows Vista 顯示驅動程式模型 (WDDM) capture 的支援。</span><span class="sxs-lookup"><span data-stu-id="85c22-124">Support for Windows Vista Display Driver Model (WDDM) capture.</span></span> <span data-ttu-id="85c22-125">這項功能可讓篩選器充分利用視訊卡與整合式影片捕獲，減少影片記憶體和系統記憶體之間的不必要複本。</span><span class="sxs-lookup"><span data-stu-id="85c22-125">This feature enables filters to take full advantage of video cards with integrated video capture, to reduce unnecessary copies between video memory and system memory.</span></span> <span data-ttu-id="85c22-126">如需詳細資訊，請參閱 [在 DirectShow 中使用 WDDM Capture](using-wddm-capture-in-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="85c22-126">For more information, see [Using WDDM Capture in DirectShow](using-wddm-capture-in-directshow.md).</span></span>
-   <span data-ttu-id="85c22-127">MPEG-2 圖層 II 音訊解碼器現在使用浮點算術，以改善解碼品質。</span><span class="sxs-lookup"><span data-stu-id="85c22-127">The MPEG-1 Layer II audio decoder now uses floating-point arithmetic, for improved decoding quality.</span></span>
-   <span data-ttu-id="85c22-128">DVD 播放的增強功能。</span><span class="sxs-lookup"><span data-stu-id="85c22-128">DVD playback enhancements.</span></span> <span data-ttu-id="85c22-129">如需詳細資訊，請參閱 [Windows Vista 中的 DVD 播放增強功能](dvd-playback-enhancements-in-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="85c22-129">For details, see [DVD Playback Enhancements in Windows Vista](dvd-playback-enhancements-in-windows-vista.md).</span></span>
    -   <span data-ttu-id="85c22-130">更好的訣竅模式支援：在速率之間進行平滑轉換;向前與反向播放之間的轉換;支援向前快轉和反向播放音訊。</span><span class="sxs-lookup"><span data-stu-id="85c22-130">Better trick-mode support: Smooth transitions between rates; transitions between forward and reverse playback; support for audio playback during fast-forward and reverse.</span></span>
    -   <span data-ttu-id="85c22-131">增強的快取。</span><span class="sxs-lookup"><span data-stu-id="85c22-131">Enhanced caching.</span></span> <span data-ttu-id="85c22-132">應用程式可以設定 DVD 導覽器預先讀取的資料量。</span><span class="sxs-lookup"><span data-stu-id="85c22-132">Applications can set how much data the DVD Navigator reads in advance.</span></span> <span data-ttu-id="85c22-133">設定較大的快取可以延長電池壽命，並在磁片磁碟機) 關閉之後 (啟用無訊息播放。</span><span class="sxs-lookup"><span data-stu-id="85c22-133">Setting a larger cache can extend battery life and enable silent playback (after the drive spins down).</span></span> <span data-ttu-id="85c22-134">如需詳細資訊，請參閱 [**DVD \_ 選項 \_ 旗**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag)標。</span><span class="sxs-lookup"><span data-stu-id="85c22-134">For more information, see [**DVD\_OPTION\_FLAG**](/windows/win32/api/strmif/ne-strmif-dvd_option_flag).</span></span>
-   <span data-ttu-id="85c22-135">音訊端點裝置：應用程式可以將 DirectSound 轉譯 [器篩選器](directsound-renderer-filter.md) 與特定的音訊端點裝置產生關聯。</span><span class="sxs-lookup"><span data-stu-id="85c22-135">Audio end-point devices: Applications can associate the [DirectSound Renderer Filter](directsound-renderer-filter.md) with a particular audio end-point device.</span></span> <span data-ttu-id="85c22-136">應用程式可以使用多媒體裝置 (MMDevice) API 來列舉和選取端點裝置。</span><span class="sxs-lookup"><span data-stu-id="85c22-136">Applications can use the Multimedia Device (MMDevice) API to enumerate and select the end-point device.</span></span> <span data-ttu-id="85c22-137">如需詳細資訊，請參閱 Windows SDK 中的核心音訊 API 檔。</span><span class="sxs-lookup"><span data-stu-id="85c22-137">For more information, see the Core Audio API documentation in the Windows SDK.</span></span>
-   <span data-ttu-id="85c22-138">以下是從 Windows Vista 移除的篩選：</span><span class="sxs-lookup"><span data-stu-id="85c22-138">The following filters have been removed from Windows Vista:</span></span>
    -   [<span data-ttu-id="85c22-139">BDA IP 接收篩選器</span><span class="sxs-lookup"><span data-stu-id="85c22-139">BDA IP Sink Filter</span></span>](/previous-versions/windows/desktop/mstv/bda-ip-sink-filter)
    -   [<span data-ttu-id="85c22-140">BDA 單 Deframer 篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-140">BDA SLIP Deframer Filter</span></span>](/previous-versions/windows/desktop/mstv/bda-slip-deframer-filter)
    -   [<span data-ttu-id="85c22-141">CC 解碼篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-141">CC Decoder Filter</span></span>](cc-decoder-filter.md)
    -   [<span data-ttu-id="85c22-142">NABTS/FEC VBI 編解碼器篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-142">NABTS/FEC VBI Codec Filter</span></span>](/previous-versions/windows/desktop/mstv/nabts-fec-vbi-codec-filter)
    -   [<span data-ttu-id="85c22-143">QT 解壓縮程式篩選器</span><span class="sxs-lookup"><span data-stu-id="85c22-143">QT Decompressor Filter</span></span>](qt-decompressor-filter.md)
    -   [<span data-ttu-id="85c22-144">QuickTime 影片剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-144">QuickTime Movie Parser Filter</span></span>](quicktime-movie-parser-filter.md)
    -   [<span data-ttu-id="85c22-145">WST 編解碼器篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-145">WST Codec Filter</span></span>](wst-codec-filter.md)
    -   [<span data-ttu-id="85c22-146">WST 解碼篩選</span><span class="sxs-lookup"><span data-stu-id="85c22-146">WST Decoder Filter</span></span>](wst-decoder-filter.md)
-   <span data-ttu-id="85c22-147">許多 DirectShow 介面的 proxy/stub 程式碼已經從 quartz.dll 移至 proppage.dll。</span><span class="sxs-lookup"><span data-stu-id="85c22-147">The proxy/stub code for many of the DirectShow interfaces has been moved from quartz.dll to proppage.dll.</span></span> <span data-ttu-id="85c22-148">這段程式碼已從 quartz.dll 中移除，因為它不適合應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="85c22-148">This code was removed from quartz.dll because it was not intended for use by applications.</span></span> <span data-ttu-id="85c22-149">不過，它很適合用於偵錯工具，因為它可讓測試應用程式從遠端連線到另一個進程中的 DirectShow 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="85c22-149">However, it is useful for debugging, because it enables a test application to connect remotely to a DirectShow filter graph in another process.</span></span> <span data-ttu-id="85c22-150">若要在 Windows Vista 中使用這項功能，您必須先註冊 proppage.dll。</span><span class="sxs-lookup"><span data-stu-id="85c22-150">To use this feature in Windows Vista, you must first register proppage.dll.</span></span> <span data-ttu-id="85c22-151">此 DLL 可在 Windows SDK tools 目錄中取得。</span><span class="sxs-lookup"><span data-stu-id="85c22-151">This DLL is available in the Windows SDK tools directory.</span></span> <span data-ttu-id="85c22-152"> (需詳細資訊，請參閱 [從外部進程載入圖形](loading-a-graph-from-an-external-process.md)) 。</span><span class="sxs-lookup"><span data-stu-id="85c22-152">(For more information, see [Loading a Graph From an External Process](loading-a-graph-from-an-external-process.md).)</span></span>

 

 
