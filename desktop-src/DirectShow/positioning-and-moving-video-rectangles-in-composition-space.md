---
title: 在組合空間中定位和移動影片矩形
description: 在組合空間中定位和移動影片矩形
ms.assetid: 97e7bb24-79f6-4638-a9c4-ac09dbd29be9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef766d1ae739e46a2c56bfab81b4243c9dcf6f10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972110"
---
# <a name="position-and-move-video-rectangles-in-composition-space"></a><span data-ttu-id="9b708-103">在組合空間中定位和移動影片矩形</span><span class="sxs-lookup"><span data-stu-id="9b708-103">Position and move video rectangles in composition space</span></span>

<span data-ttu-id="9b708-104">當 VMR 混合多個輸入資料流程時，會將每個串流放置於一個正規化的矩形內，稱為「組合空間」。</span><span class="sxs-lookup"><span data-stu-id="9b708-104">When the VMR mixes multiple input streams, it positions each stream within a normalized rectangle, called "composition space."</span></span> <span data-ttu-id="9b708-105">在組合空間內，座標 (0.0，0.0) 至 (1.0，1.0) 形成可見的影片矩形。</span><span class="sxs-lookup"><span data-stu-id="9b708-105">Within composition space, the coordinates (0.0, 0.0) to (1.0, 1.0) form the visible video rectangle.</span></span> <span data-ttu-id="9b708-106">落在這個矩形之外的任何座標都會裁剪。</span><span class="sxs-lookup"><span data-stu-id="9b708-106">Any coordinates that fall outside of this rectangle are clipped.</span></span>

<span data-ttu-id="9b708-107">應用程式可以藉由變更資料流程的組合空間中的目的地矩形，來執行從輸入串流移動、延展和壓縮影片的特殊效果。</span><span class="sxs-lookup"><span data-stu-id="9b708-107">An application can perform special effects with moving, stretching, and shrinking the video from an input stream, by changing the destination rectangle in composition space for that stream.</span></span> <span data-ttu-id="9b708-108">如果指定的矩形與原生影片矩形的大小不同，則原生影片將會縮小或伸展以容納。</span><span class="sxs-lookup"><span data-stu-id="9b708-108">If the specified rectangle is a different size than the native video rectangle, the native video will be shrunk or stretched to fit.</span></span> <span data-ttu-id="9b708-109">藉由呼叫 [**IVMRMixerControl：： SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) 方法來指定目的地矩形。</span><span class="sxs-lookup"><span data-stu-id="9b708-109">The destination rectangle is specified by calling the [**IVMRMixerControl::SetOutputRect**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setmixingprefs) method.</span></span>

<span data-ttu-id="9b708-110">例如，假設「資料流程0」 (對應至「pin 0」) 包含主要的影片資料流程，而「串流1」 (對應至 pin 1) 包含次要影片。</span><span class="sxs-lookup"><span data-stu-id="9b708-110">For example, assume that stream 0 (which corresponds to pin 0) contains the main video stream, and stream 1 (which corresponds to pin 1) contains a secondary video.</span></span> <span data-ttu-id="9b708-111">您可以藉由指定 {-1.0 f、0.0 f、0.0 f、1.0 f} 的正規化矩形，將 Stream 1 完全放置於外。</span><span class="sxs-lookup"><span data-stu-id="9b708-111">Stream 1 can be positioned completely offscreen by specifying a normalized rectangle of { -1.0f, 0.0f, 0.0f, 1.0f }.</span></span> <span data-ttu-id="9b708-112">然後，您可以在連續呼叫 **SetOutputRect** 時，藉由修改矩形的左右側邊，將 Stream 1 移至可見區域：</span><span class="sxs-lookup"><span data-stu-id="9b708-112">Stream 1 can then be moved into the visible area by modifying the left and right sides of the rectangle on successive calls to **SetOutputRect**:</span></span>



|        |                             |
|--------|-----------------------------|
| <span data-ttu-id="9b708-113">Time</span><span class="sxs-lookup"><span data-stu-id="9b708-113">Time</span></span>   | <span data-ttu-id="9b708-114">矩形</span><span class="sxs-lookup"><span data-stu-id="9b708-114">Rectangle</span></span>                   |
| <span data-ttu-id="9b708-115">t + 0</span><span class="sxs-lookup"><span data-stu-id="9b708-115">t + 0</span></span>  | <span data-ttu-id="9b708-116">{-1.0 f、0.0 f、0.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="9b708-116">{ -1.0f, 0.0f, 0.0f, 1.0f }</span></span> |
| <span data-ttu-id="9b708-117">t + 1</span><span class="sxs-lookup"><span data-stu-id="9b708-117">t + 1</span></span>  | <span data-ttu-id="9b708-118">{-0.9 f、0.0 f、0.1 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="9b708-118">{ -0.9f, 0.0f, 0.1f, 1.0f }</span></span> |
| <span data-ttu-id="9b708-119">t + 2</span><span class="sxs-lookup"><span data-stu-id="9b708-119">t + 2</span></span>  | <span data-ttu-id="9b708-120">{-0.8 f、0.0 f、0.2 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="9b708-120">{ -0.8f, 0.0f, 0.2f, 1.0f }</span></span> |
| <span data-ttu-id="9b708-121">...</span><span class="sxs-lookup"><span data-stu-id="9b708-121">...</span></span>    | <span data-ttu-id="9b708-122">...</span><span class="sxs-lookup"><span data-stu-id="9b708-122">...</span></span>                         |
| <span data-ttu-id="9b708-123">t + 10</span><span class="sxs-lookup"><span data-stu-id="9b708-123">t + 10</span></span> | <span data-ttu-id="9b708-124">{0.0 f、0.0 f、1.0 f、1.0 f}</span><span class="sxs-lookup"><span data-stu-id="9b708-124">{ 0.0f, 0.0f, 1.0f, 1.0f }</span></span>  |



 

![在組合空間中移動影片資料流程](images/composition-space.png)

<span data-ttu-id="9b708-126">在時間 t + 10，資料流程1的影片完全可見。</span><span class="sxs-lookup"><span data-stu-id="9b708-126">At time t+10, the video from stream 1 is completely visible.</span></span> <span data-ttu-id="9b708-127">在此範例中，資料流程1的原生大小是在移動時進行維護。</span><span class="sxs-lookup"><span data-stu-id="9b708-127">In this example, the native size of stream 1 was maintained while it was moving.</span></span> <span data-ttu-id="9b708-128">您也可以延展或縮小矩形，以產生有趣的效果。</span><span class="sxs-lookup"><span data-stu-id="9b708-128">You could also stretch or shrink the rectangle to produce interesting effects.</span></span> <span data-ttu-id="9b708-129">您也可以垂直翻轉影片、指定頂端的較大值，或是水準鏡像影片，方法是指定右邊左邊的較大值。</span><span class="sxs-lookup"><span data-stu-id="9b708-129">You can also flip the video vertically, by specifying a greater value for the top than the bottom, or mirror the video horizontally, by specifying a greater value for the left than the right.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b708-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="9b708-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b708-131">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="9b708-131">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



