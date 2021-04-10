---
description: Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689304"
---
# <a name="dxva-hd"></a><span data-ttu-id="b4072-103">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b4072-103">DXVA-HD</span></span>

<span data-ttu-id="b4072-104">Microsoft DirectX Video 加速 High Definition (DXVA-HD) 是用於硬體加速影片處理的 API。</span><span class="sxs-lookup"><span data-stu-id="b4072-104">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <span data-ttu-id="b4072-105">DXVA-HD 使用 GPU 來執行去交錯、合成和色彩空間轉換等功能。</span><span class="sxs-lookup"><span data-stu-id="b4072-105">DXVA-HD uses the GPU to perform functions such as deinterlacing, compositing, and color-space conversion.</span></span>

<span data-ttu-id="b4072-106">DXVA-HD 類似于 [DXVA 影片處理](dxva-video-processing.md) (DXVA-VP) ，但提供增強的功能和更簡單的處理模型。</span><span class="sxs-lookup"><span data-stu-id="b4072-106">DXVA-HD is similar to [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), but offers enhanced features and a simpler processing model.</span></span> <span data-ttu-id="b4072-107">藉由提供更有彈性的組合模型，DXVA-HD 設計為支援新一代的 HD 光學格式和廣播標準。</span><span class="sxs-lookup"><span data-stu-id="b4072-107">By providing a more flexible composition model, DXVA-HD is designed to support the next generation of HD optical formats and broadcast standards.</span></span>

<span data-ttu-id="b4072-108">DXVA-HD API 需要 WDDM 顯示器驅動程式，以支援 DXVA-HD 設備磁碟機介面 (的 DDI) 或外掛程式軟體處理器。</span><span class="sxs-lookup"><span data-stu-id="b4072-108">The DXVA-HD API requires either a WDDM display driver that supports the DXVA-HD device driver interface (DDI), or a plug-in software processor.</span></span>

-   [<span data-ttu-id="b4072-109">超越 DXVA 的改進-VP</span><span class="sxs-lookup"><span data-stu-id="b4072-109">Improvements over DXVA-VP</span></span>](#improvements-over-dxva-vp)
-   [<span data-ttu-id="b4072-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4072-110">Related topics</span></span>](#related-topics)

## <a name="improvements-over-dxva-vp"></a><span data-ttu-id="b4072-111">超越 DXVA 的改進-VP</span><span class="sxs-lookup"><span data-stu-id="b4072-111">Improvements over DXVA-VP</span></span>

<span data-ttu-id="b4072-112">DXVA-HD 擴展 DXVA （VP）所提供的一組功能。</span><span class="sxs-lookup"><span data-stu-id="b4072-112">DXVA-HD expands the set of features provided by DXVA-VP.</span></span> <span data-ttu-id="b4072-113">增強功能包括：</span><span class="sxs-lookup"><span data-stu-id="b4072-113">Enhancements include:</span></span>

-   <span data-ttu-id="b4072-114">RGB 和 YUV 混合。</span><span class="sxs-lookup"><span data-stu-id="b4072-114">RGB and YUV mixing.</span></span> <span data-ttu-id="b4072-115">任何資料流程可以是 RGB 或 YUV。</span><span class="sxs-lookup"><span data-stu-id="b4072-115">Any stream can be either RGB or YUV.</span></span> <span data-ttu-id="b4072-116">主要資料流程與子串流之間已不再有所差異。</span><span class="sxs-lookup"><span data-stu-id="b4072-116">There is no longer a distinction between the primary stream and the substreams.</span></span>
-   <span data-ttu-id="b4072-117">多個資料流程的去交錯。</span><span class="sxs-lookup"><span data-stu-id="b4072-117">Deinterlacing of multiple streams.</span></span> <span data-ttu-id="b4072-118">任何資料流程可以是漸進式或交錯式。</span><span class="sxs-lookup"><span data-stu-id="b4072-118">Any stream can be either progressive or interlaced.</span></span> <span data-ttu-id="b4072-119">此外，步調和畫面播放速率可能會因某個輸入資料流程而異。</span><span class="sxs-lookup"><span data-stu-id="b4072-119">Moreover, the cadence and frame rate can can vary from one input stream to the next.</span></span>
-   <span data-ttu-id="b4072-120">RGB 背景色彩。</span><span class="sxs-lookup"><span data-stu-id="b4072-120">RGB background colors.</span></span> <span data-ttu-id="b4072-121">先前只支援 YUV 的背景色彩。</span><span class="sxs-lookup"><span data-stu-id="b4072-121">Previously, only YUV background colors were supported.</span></span>
-   <span data-ttu-id="b4072-122">Luma 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b4072-122">Luma keying.</span></span> <span data-ttu-id="b4072-123">啟用 luma 金鑰時，落在指定範圍內的 luma 值會變成透明。</span><span class="sxs-lookup"><span data-stu-id="b4072-123">When luma keying is enabled, luma values that fall within a designated range become transparent.</span></span>
-   <span data-ttu-id="b4072-124">在交錯模式之間動態切換。</span><span class="sxs-lookup"><span data-stu-id="b4072-124">Dynamic switching between deinterlace modes.</span></span>

<span data-ttu-id="b4072-125">DXVA-HD 也會定義一些驅動程式可支援的先進功能。</span><span class="sxs-lookup"><span data-stu-id="b4072-125">DXVA-HD also defines some advanced features that drivers can support.</span></span> <span data-ttu-id="b4072-126">不過，應用程式不應該假設所有驅動程式都支援這些功能。</span><span class="sxs-lookup"><span data-stu-id="b4072-126">However, applications should not assume that all drivers will support these features.</span></span> <span data-ttu-id="b4072-127">先進的功能包括：</span><span class="sxs-lookup"><span data-stu-id="b4072-127">The advanced features include:</span></span>

-   <span data-ttu-id="b4072-128">反向電視電視 (例如，60i 至 24p) 。</span><span class="sxs-lookup"><span data-stu-id="b4072-128">Inverse telecine (for example, 60i to 24p).</span></span>
-   <span data-ttu-id="b4072-129">畫面播放速率轉換 (例如，24p 至 120p) 。</span><span class="sxs-lookup"><span data-stu-id="b4072-129">Frame-rate conversion (for example, 24p to 120p).</span></span>
-   <span data-ttu-id="b4072-130">Alpha 填滿模式。</span><span class="sxs-lookup"><span data-stu-id="b4072-130">Alpha-fill modes.</span></span>
-   <span data-ttu-id="b4072-131">減少雜訊和邊緣增強篩選。</span><span class="sxs-lookup"><span data-stu-id="b4072-131">Noise reduction and edge enhancement filtering.</span></span>
-   <span data-ttu-id="b4072-132">Anamorphic 非線性調整。</span><span class="sxs-lookup"><span data-stu-id="b4072-132">Anamorphic non-linear scaling.</span></span>
-   <span data-ttu-id="b4072-133">外延 YCbCr (xvYCC) 。</span><span class="sxs-lookup"><span data-stu-id="b4072-133">Extended YCbCr (xvYCC).</span></span>

<span data-ttu-id="b4072-134">此章節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="b4072-134">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b4072-135">建立 DXVA-HD 視頻處理器</span><span class="sxs-lookup"><span data-stu-id="b4072-135">Creating a DXVA-HD Video Processor</span></span>](creating-a-dxva-hd-video-processor.md)
-   [<span data-ttu-id="b4072-136">檢查支援的 DXVA-HD 格式</span><span class="sxs-lookup"><span data-stu-id="b4072-136">Checking Supported DXVA-HD Formats</span></span>](checking-supported-dxva-hd-formats.md)
-   [<span data-ttu-id="b4072-137">建立 DXVA-HD 影片表面</span><span class="sxs-lookup"><span data-stu-id="b4072-137">Creating DXVA-HD Video Surfaces</span></span>](creating-dxva-hd-video-surfaces.md)
-   [<span data-ttu-id="b4072-138">設定 DXVA-HD 狀態</span><span class="sxs-lookup"><span data-stu-id="b4072-138">Setting DXVA-HD States</span></span>](setting-dxva-hd-states.md)
-   [<span data-ttu-id="b4072-139">執行 DXVA-HD Array.blit</span><span class="sxs-lookup"><span data-stu-id="b4072-139">Performing the DXVA-HD Blit</span></span>](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a><span data-ttu-id="b4072-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="b4072-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4072-141">DirectX Video 加速2。0</span><span class="sxs-lookup"><span data-stu-id="b4072-141">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="b4072-142">DXVA-HD 範例</span><span class="sxs-lookup"><span data-stu-id="b4072-142">DXVA-HD Sample</span></span>](dxva-hd-sample.md)
</dt> </dl>

 

 



