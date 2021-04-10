---
description: 使用影片捕獲中的重迭混音器
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: 使用影片捕獲中的重迭混音器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027047"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="8ef2f-103">使用影片捕獲中的重迭混音器</span><span class="sxs-lookup"><span data-stu-id="8ef2f-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="8ef2f-104">[影片](video-renderer-filter.md)轉譯器篩選器本身無法顯示特定類型的影片。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="8ef2f-105">在這些情況下，影片轉譯器必須搭配覆迭 [混音](overlay-mixer-filter.md) 器篩選器來使用。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="8ef2f-106">重迭混音器會管理轉譯，而影片轉譯器則會管理影片視窗。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="8ef2f-107">在下列情況下，需要重迭混音器：</span><span class="sxs-lookup"><span data-stu-id="8ef2f-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="8ef2f-108">影片埠 (VP) 圖釘。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-108">Video port (VP) pins.</span></span> <span data-ttu-id="8ef2f-109">如果捕捉裝置使用影片埠，重迭混音器會管理硬體重迭。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="8ef2f-110">交錯式影片。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-110">Interlaced video.</span></span> <span data-ttu-id="8ef2f-111">針對交錯式影片，此解碼器需要影片轉譯器不支援的 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="8ef2f-112">隱藏式輔助字幕。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-112">Closed captions.</span></span> <span data-ttu-id="8ef2f-113">標題文字會轉譯為每圖元8位的點陣圖，而重迭混音器會在影片上重迭。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="8ef2f-114">「捕獲圖形產生器」的 **RenderStream** 方法會在每次需要時插入重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="8ef2f-115">但是，如果您要在不使用 [Capture Graph Builder] 的情況下建立圖形，則必須檢查每一種情況，並自行插入重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="8ef2f-116">\[!重要\]</span><span class="sxs-lookup"><span data-stu-id="8ef2f-116">\[!Important\]</span></span>  
    > <span data-ttu-id="8ef2f-117">如果裝置有 VP 釘選，即使您的應用程式中不需要預覽功能，您還是必須連接重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="8ef2f-118">使用影片埠時，capture 裝置一律會將影片資料傳送至硬體重迭，因此一律需要重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="8ef2f-119">影片混合轉譯器篩選器 (VMR-7 和 VMR-9) 兩者都支援交錯式影片，而且能夠將隱藏式輔助字幕點陣圖混合到主要影片上。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="8ef2f-120">如果您在這些案例中使用 VMR，則不需要使用重迭混音器。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="8ef2f-121">VMR-9 不支援副總 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="8ef2f-122">VMR-7 透過「影片埠管理員」篩選器支援副總 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="8ef2f-123">不過，您可能會發現某些驅動程式無法與影片埠管理員正常搭配運作。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="8ef2f-124">基於這個理由，仍建議將重迭混音器用於 VP 圖釘。</span><span class="sxs-lookup"><span data-stu-id="8ef2f-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ef2f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ef2f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ef2f-126">Advanced Capture 主題</span><span class="sxs-lookup"><span data-stu-id="8ef2f-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="8ef2f-127">影片埠釘選</span><span class="sxs-lookup"><span data-stu-id="8ef2f-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="8ef2f-128">VideoInfo2 格式類型</span><span class="sxs-lookup"><span data-stu-id="8ef2f-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



