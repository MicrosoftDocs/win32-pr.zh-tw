---
description: 解碼器的需求
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: 解碼器的需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461120bec88636e4c015c2e319d855571e8ac1b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467624"
---
# <a name="requirements-for-decoders"></a><span data-ttu-id="589c2-103">解碼器的需求</span><span class="sxs-lookup"><span data-stu-id="589c2-103">Requirements for Decoders</span></span>

<span data-ttu-id="589c2-104">傳遞範例給 VMR 的解碼器必須遵守下列規則：</span><span class="sxs-lookup"><span data-stu-id="589c2-104">Decoders that deliver samples to the VMR must observe the following rules:</span></span>

-   <span data-ttu-id="589c2-105">每個影片畫面應該會有一個子圖片的框架傳遞至 VMR。</span><span class="sxs-lookup"><span data-stu-id="589c2-105">There should be one subpicture frame delivered to the VMR for each video frame.</span></span> <span data-ttu-id="589c2-106">這兩個畫面格的時間戳記應該相同。</span><span class="sxs-lookup"><span data-stu-id="589c2-106">The two frames should have the same time stamps.</span></span>
-   <span data-ttu-id="589c2-107">如果子圖片未變更，請使用 \_ \_ [**IMemAllocator：： GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) 方法中的 AM GBF NOTASYNCPOINT 旗標，強制配置器傳回緩衝區，其中包含傳遞至 VMR 的最後一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="589c2-107">If the subpicture has not changed, use the AM\_GBF\_NOTASYNCPOINT flag in the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method to force the allocator to return a buffer containing the last frame delivered to the VMR.</span></span> <span data-ttu-id="589c2-108">只要將新的時間戳記放在範例上，然後再將它傳遞至 VMR。</span><span class="sxs-lookup"><span data-stu-id="589c2-108">Just put a new time stamp on the sample and deliver it to the VMR again.</span></span> <span data-ttu-id="589c2-109">如果子圖片成名是空白的，您仍然應該提供它。</span><span class="sxs-lookup"><span data-stu-id="589c2-109">If the subpicture fame is blank, you should still deliver it.</span></span> <span data-ttu-id="589c2-110">VMR 將會偵測到空白框架，而不會將它與影片混合。</span><span class="sxs-lookup"><span data-stu-id="589c2-110">The VMR will detect the empty frame and not blend it with the video.</span></span> <span data-ttu-id="589c2-111">這項測試是由 VGA 晶片執行，並不會影響播放效能。</span><span class="sxs-lookup"><span data-stu-id="589c2-111">This test is performed by the VGA chip and does not affect the playback performance.</span></span>
-   <span data-ttu-id="589c2-112">除了即時資料流以外的所有範例都必須附加有效的開始和停止時間戳記。</span><span class="sxs-lookup"><span data-stu-id="589c2-112">All samples, except for live streams, must have valid start and stop time stamps attached.</span></span> <span data-ttu-id="589c2-113"> (DVD 不是即時串流。 ) </span><span class="sxs-lookup"><span data-stu-id="589c2-113">(DVD is not a live stream.)</span></span>
-   <span data-ttu-id="589c2-114">媒體取樣時間戳記必須是連續的</span><span class="sxs-lookup"><span data-stu-id="589c2-114">The media sample time stamps must be contiguous</span></span>
-   <span data-ttu-id="589c2-115">此解碼器必須將本身識別為可供圖形產生器使用的 VMR。</span><span class="sxs-lookup"><span data-stu-id="589c2-115">The decoder must identify itself as VMR-capable for use by graph builders.</span></span>
-   <span data-ttu-id="589c2-116">子圖片資料流程現在應該包含內嵌的每圖元 Alpha 值。</span><span class="sxs-lookup"><span data-stu-id="589c2-116">The subpicture stream should now contain embedded per-pixel alpha values.</span></span> <span data-ttu-id="589c2-117">ARGB4444 介面類別型很適合用於 subpictures。</span><span class="sxs-lookup"><span data-stu-id="589c2-117">The ARGB4444 surface type is ideal for subpictures.</span></span>
-   <span data-ttu-id="589c2-118">請勿假設子圖片的 stride 與表面寬度相同。</span><span class="sxs-lookup"><span data-stu-id="589c2-118">Do not assume that the stride of the subpicture is the same as the surface width.</span></span> <span data-ttu-id="589c2-119">這不一定是 VMR 的情況。</span><span class="sxs-lookup"><span data-stu-id="589c2-119">This is not always the case with the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="589c2-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="589c2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="589c2-121">關於 DirectX Video 加速</span><span class="sxs-lookup"><span data-stu-id="589c2-121">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



