---
description: DVD 篩選圖形設定
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: DVD 篩選圖形設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510262"
---
# <a name="dvd-filter-graph-configuration"></a><span data-ttu-id="a0e71-103">DVD 篩選圖形設定</span><span class="sxs-lookup"><span data-stu-id="a0e71-103">DVD Filter Graph Configuration</span></span>

<span data-ttu-id="a0e71-104">本節說明在 DirectShow 中播放 DVD 的各種篩選圖形設定。</span><span class="sxs-lookup"><span data-stu-id="a0e71-104">This section describes the various filter graph configurations for DVD playback in DirectShow.</span></span> <span data-ttu-id="a0e71-105">這些圖表主要是供參考之用。</span><span class="sxs-lookup"><span data-stu-id="a0e71-105">These diagrams are provided mainly for reference.</span></span> <span data-ttu-id="a0e71-106">DVD 導覽器會建立圖形，因此通常不需要瞭解如何設定圖形的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a0e71-106">The DVD Navigator builds the graph, so in general it is not necessary to understand the details of how the graph is configured.</span></span> <span data-ttu-id="a0e71-107">如需詳細資訊，請參閱 [建立 DVD 篩選圖形](building-the-dvd-filter-graph.md)。</span><span class="sxs-lookup"><span data-stu-id="a0e71-107">For more information, see [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).</span></span>

<span data-ttu-id="a0e71-108">下圖顯示具有軟體解碼器的 DVD 篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a0e71-108">The following illustration shows a DVD filter graph with a software decoder.</span></span>

![適用于 windows xp 的 dvd 篩選圖形](images/dvd-graph-xp.png)

<span data-ttu-id="a0e71-110">當硬體解碼存在時，通常會透過影片埠直接連接到視訊卡。</span><span class="sxs-lookup"><span data-stu-id="a0e71-110">When a hardware decoder is present, it is typically connected directly to the video card by a video port.</span></span> <span data-ttu-id="a0e71-111">這可讓已解碼的影片位直接傳送到圖形配接器上的框架緩衝區，而不會傳入主機記憶體。</span><span class="sxs-lookup"><span data-stu-id="a0e71-111">This enables the decoded video bits to be sent directly to the frame buffer on the graphics card without passing into host memory.</span></span> <span data-ttu-id="a0e71-112">若要在舊版 Windows 上管理此直接連線，DirectShow 透過覆迭 [混音器篩選器](overlay-mixer-filter.md)上的介面，支援 DirectDraw)  (VPE 的視訊連接埠擴充。</span><span class="sxs-lookup"><span data-stu-id="a0e71-112">To manage this direct connection on earlier versions of Windows, DirectShow supports DirectDraw Video Port Extensions (VPE) through an interface on the [Overlay Mixer Filter](overlay-mixer-filter.md).</span></span>

> [!Note]  
> <span data-ttu-id="a0e71-113">覆迭混音器現在已被取代。</span><span class="sxs-lookup"><span data-stu-id="a0e71-113">The Overlay Mixer is now deprecated.</span></span>

 

<span data-ttu-id="a0e71-114">在 Windows XP 和更新版本中，硬體解碼器可以連接到 [視訊連接埠管理員](video-port-manager.md) 篩選器。</span><span class="sxs-lookup"><span data-stu-id="a0e71-114">In Windows XP and later, a hardware decoder can connect to the [Video Port Manager](video-port-manager.md) filter.</span></span>

![具有硬體解碼的 windows xp dvd graph](images/dvd-hwgraph-xp.png)

<span data-ttu-id="a0e71-116">在所有這些圖形中，DVD 導覽器是來源篩選;它會執行幾項工作：</span><span class="sxs-lookup"><span data-stu-id="a0e71-116">In all these graphs, the DVD Navigator is the source filter; it performs several tasks:</span></span>

-   <span data-ttu-id="a0e71-117">從光碟讀取導覽和影片資料。</span><span class="sxs-lookup"><span data-stu-id="a0e71-117">Reads the navigation and video data from the disc.</span></span>
-   <span data-ttu-id="a0e71-118">將影片、音訊和子圖片資料 Demultiplexes 至不同的串流。</span><span class="sxs-lookup"><span data-stu-id="a0e71-118">Demultiplexes the video, audio, and subpicture data into separate streams.</span></span>
-   <span data-ttu-id="a0e71-119">將資料流程提取到圖形中，以進行進一步的處理和最終呈現。</span><span class="sxs-lookup"><span data-stu-id="a0e71-119">Pumps the streams into the graph for further processing and eventual rendering.</span></span>
-   <span data-ttu-id="a0e71-120">通知您應用程式 DVD 相關事件。</span><span class="sxs-lookup"><span data-stu-id="a0e71-120">Informs your application of DVD-related events.</span></span>

<span data-ttu-id="a0e71-121">在音訊串流中，DVD 導覽器會連線到音訊解碼器，以連接到 DirectSound 轉譯 [器篩選器](directsound-renderer-filter.md)，也就是預設的音訊轉譯器。</span><span class="sxs-lookup"><span data-stu-id="a0e71-121">On the audio stream, the DVD Navigator connects downstream to an audio decoder, which connects to the [DirectSound Renderer Filter](directsound-renderer-filter.md), the default audio renderer.</span></span> <span data-ttu-id="a0e71-122">在影片和子圖片串流上，下游篩選器為協力廠商的影片解碼，而影片混合轉譯器 (或重迭 [混音](overlay-mixer-filter.md)器，以及繼承應用程式上的 [影片](video-renderer-filter.md) 轉譯器) 。</span><span class="sxs-lookup"><span data-stu-id="a0e71-122">On the video and subpicture streams, the downstream filters are the third-party video decoder, and the Video Mixing Renderer (or the [Overlay Mixer](overlay-mixer-filter.md), and the [Video Renderer](video-renderer-filter.md) on downlevel applications).</span></span> <span data-ttu-id="a0e71-123">如果您的應用程式將處理第21行的已關閉標題資料，您必須將 DirectShow 線21的第21行篩選器新增至圖形。</span><span class="sxs-lookup"><span data-stu-id="a0e71-123">If your application will handle line 21 closed-captioned data, you must add the DirectShow Line 21 Decoder 2 filter to the graph.</span></span> <span data-ttu-id="a0e71-124">這牽涉到單一方法呼叫;篩選器會自動連接。</span><span class="sxs-lookup"><span data-stu-id="a0e71-124">This involves a single method call; the filter will be connected automatically.</span></span>

<span data-ttu-id="a0e71-125">您的應用程式會透過 DVD 導覽器所公開的自訂介面，與 DVD 導覽器進行通訊及控制： [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)-"set" 方法（以及 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)） "get" 方法。</span><span class="sxs-lookup"><span data-stu-id="a0e71-125">Your application communicates with and controls the DVD Navigator through the custom interfaces that the DVD Navigator exposes: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)—the "set" methods—and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)—the "get" methods.</span></span> <span data-ttu-id="a0e71-126">它也必須透過 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) 與篩選 graph 管理員 (進行通訊，以停止、啟動及控制圖形。</span><span class="sxs-lookup"><span data-stu-id="a0e71-126">It also must communicate with the filter graph manager (through [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) to stop, start, and otherwise control the graph.</span></span> <span data-ttu-id="a0e71-127">您可能也需要控制其他個別篩選器，例如在視窗化與全螢幕顯示之間切換的重迭混音器篩選器。</span><span class="sxs-lookup"><span data-stu-id="a0e71-127">You might also need to control other individual filters, such as the Overlay Mixer filter for switching between windowed and full-screen display.</span></span> <span data-ttu-id="a0e71-128">如需詳細資訊，請參閱 [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2)。</span><span class="sxs-lookup"><span data-stu-id="a0e71-128">For more information, see [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2).</span></span> <span data-ttu-id="a0e71-129">圖形的確切設定取決於您已安裝的 MPEG-2 解碼器類型、是否需要處理第21行的已隱藏標題資料，以及其他因素。</span><span class="sxs-lookup"><span data-stu-id="a0e71-129">The exact configuration of the graph will vary depending on what type of MPEG-2 decoder you have installed, whether you need to handle line 21 closed-captioned data, and other factors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0e71-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0e71-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0e71-131">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="a0e71-131">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



