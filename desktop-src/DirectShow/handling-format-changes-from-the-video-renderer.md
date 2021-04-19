---
description: 處理影片轉譯器的格式變更
ms.assetid: ac7d7b1c-3c9a-4693-87ea-0a10a8ab915c
title: 處理影片轉譯器的格式變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d731ac4b9d6985cf5ad92f642b6d8262209fa91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106995797"
---
# <a name="handling-format-changes-from-the-video-renderer"></a><span data-ttu-id="3754a-103">處理影片轉譯器的格式變更</span><span class="sxs-lookup"><span data-stu-id="3754a-103">Handling Format Changes from the Video Renderer</span></span>

<span data-ttu-id="3754a-104">本節說明「解碼器篩選準則」或「轉換」篩選器如何處理來自影片轉譯器的格式變更。</span><span class="sxs-lookup"><span data-stu-id="3754a-104">This section describes how a decoder filter or transform filter should handle format changes from the video renderer.</span></span>

<span data-ttu-id="3754a-105">**影片轉譯器篩選**</span><span class="sxs-lookup"><span data-stu-id="3754a-105">**Video Renderer Filter**</span></span>

<span data-ttu-id="3754a-106">當舊的 [影片](video-renderer-filter.md) 轉譯器篩選連接時，需要符合主要監視器顯示格式的 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="3754a-106">When the old [Video Renderer](video-renderer-filter.md) filter connects, it requires an RGB format that matches the display format of the primary monitor.</span></span> <span data-ttu-id="3754a-107">這可讓它在 DirectDraw 無法使用的情況下，使用 GDI 來呈現。</span><span class="sxs-lookup"><span data-stu-id="3754a-107">This enables it to use GDI for rendering if DirectDraw is not available.</span></span> <span data-ttu-id="3754a-108">播放開始時，影片轉譯器可能會切換到 DirectDraw 相容的格式。</span><span class="sxs-lookup"><span data-stu-id="3754a-108">When playback starts, the Video Renderer may switch to a DirectDraw-compatible format.</span></span> <span data-ttu-id="3754a-109">為了 verfify 上游篩選是否可支援新的格式，影片轉譯器會在上游篩選器的輸出釘選上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 。</span><span class="sxs-lookup"><span data-stu-id="3754a-109">To verfify whether the upstream filter can support the new format, the Video Renderer calls [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) on the upstream filter's output pin.</span></span> <span data-ttu-id="3754a-110">如果上游篩選器接受新的格式， **QueryAccept** 方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3754a-110">If the upstream filter accepts the new format, the **QueryAccept** method returns S\_OK.</span></span> <span data-ttu-id="3754a-111">影片轉譯器會切換格式，方法是將具有新格式的媒體類型附加至其配置器所傳回的下一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3754a-111">The Video Renderer switches formats by attaching a media type with the new format to the next media sample returned by its allocator.</span></span> <span data-ttu-id="3754a-112">上游篩選器應該在每個範例上呼叫 [**IMediaSample：： GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) ，以檢查格式變更。</span><span class="sxs-lookup"><span data-stu-id="3754a-112">The upstream filter should check for format changes by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) on each sample.</span></span> <span data-ttu-id="3754a-113">影片轉譯器可能會在串流期間的任何時間，從原始格式和新格式來回切換。</span><span class="sxs-lookup"><span data-stu-id="3754a-113">The Video Renderer may switch back and forth between the original format and new format at any time during streaming.</span></span> <span data-ttu-id="3754a-114">它不會在第一次格式變更之後呼叫 **QueryAccept** 。</span><span class="sxs-lookup"><span data-stu-id="3754a-114">It does not call **QueryAccept** after the first format change.</span></span> <span data-ttu-id="3754a-115">上游篩選器接受新的格式之後，就必須能夠來回切換。</span><span class="sxs-lookup"><span data-stu-id="3754a-115">Once the upstream filter has accepted the new format, it must be able to switch back and forth.</span></span>

<span data-ttu-id="3754a-116">上游篩選器會從 QueryAccept 傳回 FALSE，以拒絕格式變更 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="3754a-116">The upstream filter can reject the format change by returning S\_FALSE from **QueryAccept**.</span></span> <span data-ttu-id="3754a-117">在此情況下，影片轉譯器會繼續使用具有原始格式的 GDI。</span><span class="sxs-lookup"><span data-stu-id="3754a-117">In that case, the Video Renderer continues to use GDI with the original format.</span></span>

<span data-ttu-id="3754a-118">**影片混合轉譯器篩選**</span><span class="sxs-lookup"><span data-stu-id="3754a-118">**Video Mixing Renderer Filter**</span></span>

<span data-ttu-id="3754a-119">影片混合轉譯器篩選器 (VMR-7 和 VMR-9) 將會連接到系統上圖形硬體所支援的任何格式。</span><span class="sxs-lookup"><span data-stu-id="3754a-119">The Video Mixing Renderer filter (VMR-7 and VMR-9) will connect with any format that is supported by the graphics hardware on the system.</span></span> <span data-ttu-id="3754a-120">VMR-7 一律會使用 DirectDraw 進行轉譯，並且在上游篩選連接時配置基礎 DirectDraw 表面。</span><span class="sxs-lookup"><span data-stu-id="3754a-120">The VMR-7 always uses DirectDraw for rendering, and allocates the underlying DirectDraw surfaces when the upstream filter connects.</span></span> <span data-ttu-id="3754a-121">VMR-9 一律會使用 Direct3D 進行轉譯，並且在上游篩選連接時配置基礎 Direct3D 表面。</span><span class="sxs-lookup"><span data-stu-id="3754a-121">The VMR-9 always uses Direct3D for rendering, and allocates the underlying Direct3D surfaces when the upstream filter connects.</span></span>

<span data-ttu-id="3754a-122">圖形硬體可能需要比影像寬度更大的 surface stride。</span><span class="sxs-lookup"><span data-stu-id="3754a-122">The graphics hardware may require a larger surface stride than the image width.</span></span> <span data-ttu-id="3754a-123">在此情況下，VMR 會藉由呼叫 **QueryAccept** 來要求新的格式。</span><span class="sxs-lookup"><span data-stu-id="3754a-123">In that case, the VMR requests a new format by calling **QueryAccept**.</span></span> <span data-ttu-id="3754a-124">它會以影片格式報告 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)的 **biWidth** 成員中的表面 stride。</span><span class="sxs-lookup"><span data-stu-id="3754a-124">It reports the surface stride in the **biWidth** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) in the video format.</span></span> <span data-ttu-id="3754a-125">如果上游篩選不會 \_ 從 **QueryAccept** 傳回 S OK，則 VMR 會拒絕格式，並嘗試使用上游篩選器所通告的下一個格式來進行連接。</span><span class="sxs-lookup"><span data-stu-id="3754a-125">If the upstream filter does not return S\_OK from **QueryAccept**, the VMR rejects the format and tries to connect using the next format advertised by the upstream filter.</span></span> <span data-ttu-id="3754a-126">VMR 會將具有新格式的媒體類型附加至第一個媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3754a-126">The VMR attaches the media type with the new format to the first media sample.</span></span> <span data-ttu-id="3754a-127">在第一個範例之後，格式會維持不變;當圖形正在執行時，VMR 不會切換格式。</span><span class="sxs-lookup"><span data-stu-id="3754a-127">After the first sample, the format remains constant; the VMR will not switch formats while the graph is running.</span></span>

<span data-ttu-id="3754a-128">**增強的影片呈現 (EVR)**</span><span class="sxs-lookup"><span data-stu-id="3754a-128">**Enhanced Video Render (EVR)**</span></span>

<span data-ttu-id="3754a-129">EVR 一律使用 Direct3D 來呈現。</span><span class="sxs-lookup"><span data-stu-id="3754a-129">The EVR always uses Direct3D for rendering.</span></span> <span data-ttu-id="3754a-130">如果需要較大的介面 stride，EVR 會使用與 VMR 相同的 **QueryAccept** 機制。</span><span class="sxs-lookup"><span data-stu-id="3754a-130">If a larger surface stride is needed, the EVR uses the same **QueryAccept** mechanism as the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3754a-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="3754a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3754a-132">QueryAccept (上游) </span><span class="sxs-lookup"><span data-stu-id="3754a-132">QueryAccept (Upstream)</span></span>](queryaccept--upstream.md)
</dt> </dl>

 

 



