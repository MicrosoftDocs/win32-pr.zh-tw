---
title: 使用未壓縮的音訊和影片串流
description: 使用未壓縮的音訊和影片串流
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- 串流，設定未壓縮的音訊和影片串流
- 編解碼器，設定未壓縮的音訊和影片串流
- 影片串流，未壓縮
- 音訊串流，未壓縮
- 未壓縮的音訊和影片串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966842"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="b0b6d-108">使用未壓縮的音訊和影片串流</span><span class="sxs-lookup"><span data-stu-id="b0b6d-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="b0b6d-109">在大部分的情況下，未壓縮的媒體具有極大的儲存和傳遞需求，但在某些本機播放案例中，品質層級必須足以保證不使用壓縮。</span><span class="sxs-lookup"><span data-stu-id="b0b6d-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="b0b6d-110">未壓縮媒體資料流程的設定應該會反映來源媒體的設定。</span><span class="sxs-lookup"><span data-stu-id="b0b6d-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="b0b6d-111">設定未壓縮的資料流程時，您必須計算媒體的位元速率，然後藉由呼叫 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)來適當地設定資料流程。</span><span class="sxs-lookup"><span data-stu-id="b0b6d-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="b0b6d-112">因為未壓縮的資料流程無法用於串流處理，所以您應該一律呼叫 [**IWMStreamConfig：： SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow)，將未壓縮媒體資料流程的緩衝區視窗設定為零。</span><span class="sxs-lookup"><span data-stu-id="b0b6d-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="b0b6d-113">未壓縮的影片資料流程支援下列像素格式：</span><span class="sxs-lookup"><span data-stu-id="b0b6d-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="b0b6d-114">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="b0b6d-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="b0b6d-115">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="b0b6d-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="b0b6d-116">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="b0b6d-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="b0b6d-117">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="b0b6d-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="b0b6d-118">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="b0b6d-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="b0b6d-119">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="b0b6d-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="b0b6d-120">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="b0b6d-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="b0b6d-121">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="b0b6d-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="b0b6d-122">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="b0b6d-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0b6d-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="b0b6d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0b6d-124">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="b0b6d-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="b0b6d-125">**設定音訊串流**</span><span class="sxs-lookup"><span data-stu-id="b0b6d-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="b0b6d-126">**設定資料流程**</span><span class="sxs-lookup"><span data-stu-id="b0b6d-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="b0b6d-127">**設定影片串流**</span><span class="sxs-lookup"><span data-stu-id="b0b6d-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




