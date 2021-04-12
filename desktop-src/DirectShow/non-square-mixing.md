---
description: 非正方形混合
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: 非正方形混合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510174"
---
# <a name="non-square-mixing"></a><span data-ttu-id="8fe35-103">非正方形混合</span><span class="sxs-lookup"><span data-stu-id="8fe35-103">Non-Square Mixing</span></span>

<span data-ttu-id="8fe35-104">本主題適用于 Windows XP Service Pack 2 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="8fe35-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="8fe35-105">當 VMR-9 混用兩個以上的資料流程時，有兩個點可進行調整：當混音器組合輸入資料流程時，以及配置器呈現者轉譯合成影像時。</span><span class="sxs-lookup"><span data-stu-id="8fe35-105">When the VMR-9 mixes two or more streams, there are two points where scaling can occur: When the mixer composites the input streams, and when the allocator-presenter renders the composited image.</span></span>

![vmr 混合作業](images/vmr-nonsquare-mixing.png)

<span data-ttu-id="8fe35-107">舊版的 VMR-9 一律會使用平方 (1:1) 圖元外觀比例 (PAR) 來組合輸入資料流程，即使只有一個影片串流也一樣。</span><span class="sxs-lookup"><span data-stu-id="8fe35-107">Previous versions of the VMR-9 always composited the input streams using a square (1:1) pixel aspect ratio (PAR), even when there was only a single video stream.</span></span> <span data-ttu-id="8fe35-108">如果輸入資料流程有非正方形圖元，這會導致不必要的調整作業。</span><span class="sxs-lookup"><span data-stu-id="8fe35-108">If the input stream had non-square pixels, this caused an unnecessary scaling operation.</span></span> <span data-ttu-id="8fe35-109">當然應該盡可能避免調整，因為它會降低最終的影像品質。</span><span class="sxs-lookup"><span data-stu-id="8fe35-109">Scaling should be avoided as much as possible, of course, because it degrades the final image quality.</span></span>

<span data-ttu-id="8fe35-110">從 Windows XP Service Pack 2 開始，VMR-9 支援兩種不同的方式來避免雙重調整的問題：</span><span class="sxs-lookup"><span data-stu-id="8fe35-110">Starting in Windows XP Service Pack 2, the VMR-9 supports two different ways to avoid the problem of double scaling:</span></span>

-   <span data-ttu-id="8fe35-111">執行自訂配置器-展示者並支援 [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) 介面。</span><span class="sxs-lookup"><span data-stu-id="8fe35-111">Implement a custom allocator-presenter and support the [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) interface.</span></span>
-   <span data-ttu-id="8fe35-112">使用非方形混合模式。</span><span class="sxs-lookup"><span data-stu-id="8fe35-112">Use non-square mixing mode.</span></span>

<span data-ttu-id="8fe35-113">本節說明非方形混合模式。</span><span class="sxs-lookup"><span data-stu-id="8fe35-113">This section describes non-square mixing mode.</span></span> <span data-ttu-id="8fe35-114">應用程式可以結合這兩種技術。</span><span class="sxs-lookup"><span data-stu-id="8fe35-114">Applications can combine both techniques.</span></span>

<span data-ttu-id="8fe35-115">**非正方形混合的運作方式**</span><span class="sxs-lookup"><span data-stu-id="8fe35-115">**How Non-Square Mixing Works**</span></span>

<span data-ttu-id="8fe35-116">在非方形混合模式中，VMR-9 會選取一個輸入資料流程作為目標大小，也就是相等。</span><span class="sxs-lookup"><span data-stu-id="8fe35-116">In non-square mixing mode, the VMR-9 selects one input stream to be the target size and PAR.</span></span> <span data-ttu-id="8fe35-117">VMR 的混音器不會從該資料流程或任何其他影像大小相同的資料流程調整影片。</span><span class="sxs-lookup"><span data-stu-id="8fe35-117">The VMR's mixer does not scale the video from that stream or from any other streams with the same image size and PAR.</span></span> <span data-ttu-id="8fe35-118">具有不同大小或外觀比例的資料流程會進行調整，以符合目標的等於和 letterboxed，以符合最終輸出影像的大小。</span><span class="sxs-lookup"><span data-stu-id="8fe35-118">Streams with a different size or aspect ratio are scaled to match the target PAR and letterboxed to fit the final output image size.</span></span>

<span data-ttu-id="8fe35-119">資料流程的選擇取決於目前的混合模式：</span><span class="sxs-lookup"><span data-stu-id="8fe35-119">The choice of streams depends on the current mixing mode:</span></span>

-   <span data-ttu-id="8fe35-120">在 pin 0 上，會將 YUV 混合模式限制為一個影片串流。</span><span class="sxs-lookup"><span data-stu-id="8fe35-120">YUV mixing mode is restricted to one video stream on pin 0.</span></span> <span data-ttu-id="8fe35-121"> (其他 pin 可能具有子圖片或隱藏式字幕資料流程。 ) 因此，VMR-9 一律會為目標映射大小和等於選取 pin 0。</span><span class="sxs-lookup"><span data-stu-id="8fe35-121">(The other pins may have subpicture or closed caption streams.) Therefore, the VMR-9 always selects pin 0 for the target image size and PAR.</span></span>
-   <span data-ttu-id="8fe35-122">在 RGB 混合模式中，VMR 會選取影像大小最大的資料流程。</span><span class="sxs-lookup"><span data-stu-id="8fe35-122">In RGB mixing mode, the VMR selects the stream with the largest image size.</span></span> <span data-ttu-id="8fe35-123">如果有一個以上的，則會選取具有最高 z 順序的一個：如果仍然有系結，則會選取具有最低 pin 碼的串流。</span><span class="sxs-lookup"><span data-stu-id="8fe35-123">If there is more than one, it selects the one with the highest z-order; and if there is still a tie, it selects the stream with the lowest pin number.</span></span>

<span data-ttu-id="8fe35-124">**操作範例**</span><span class="sxs-lookup"><span data-stu-id="8fe35-124">**Examples of Operation**</span></span>

<span data-ttu-id="8fe35-125">**範例1。**</span><span class="sxs-lookup"><span data-stu-id="8fe35-125">**Example 1.**</span></span> <span data-ttu-id="8fe35-126">Stream 0 是 720 x 480 圖元，圖片的外觀比例為16:9。</span><span class="sxs-lookup"><span data-stu-id="8fe35-126">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="8fe35-127">Stream 1 是 640 x 480 圖元，圖片的外觀比例為4:3。</span><span class="sxs-lookup"><span data-stu-id="8fe35-127">Stream 1 is a 640 x 480 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="8fe35-128">在此範例中，stream 0 具有最大的影像大小，因此無論是 RGB 混合模式或 YUB 混合模式，VMR 都會選擇此資料流程。</span><span class="sxs-lookup"><span data-stu-id="8fe35-128">In this example, stream 0 has the largest image size, so the VMR chooses this stream, regardless of RGB mixing mode or YUB mixing mode.</span></span> <span data-ttu-id="8fe35-129">等於 32:27 (16:9/720:480) ，這表示影像必須以這個比例水準延展，以產生正確的16:9 圖片外觀比例。</span><span class="sxs-lookup"><span data-stu-id="8fe35-129">The PAR is 32:27 (16:9 / 720:480), meaning the image must be stretched horizontally by this ratio to produce the correct 16:9 picture aspect ratio.</span></span>

<span data-ttu-id="8fe35-130">為了符合目標，VMR 混音器會依據反向比率調整資料流程 1 (27:32) ，導致 540 x 480 影像。</span><span class="sxs-lookup"><span data-stu-id="8fe35-130">To match the target PAR, the VMR mixer scales stream 1 by the inverse ratio (27:32), resulting in a 540 x 480 image.</span></span> <span data-ttu-id="8fe35-131">這兩個數據流接著會合成至一個介面上。</span><span class="sxs-lookup"><span data-stu-id="8fe35-131">The two streams are then composited onto one surface.</span></span> <span data-ttu-id="8fe35-132">若要正確顯示產生的影像，配置器展示者必須水準延展影像，以符合16:9 圖片的外觀比例。</span><span class="sxs-lookup"><span data-stu-id="8fe35-132">To display the resulting image correctly, the allocator presenter must stretch the image horizontally to fit the 16:9 picture aspect ratio.</span></span>

![範例1。](images/vmr-nonsquare-mixing2.png)

<span data-ttu-id="8fe35-134">**範例2。**</span><span class="sxs-lookup"><span data-stu-id="8fe35-134">**Example 2.**</span></span> <span data-ttu-id="8fe35-135">Stream 0 是 720 x 480 圖元，圖片的外觀比例為16:9。</span><span class="sxs-lookup"><span data-stu-id="8fe35-135">Stream 0 is 720 x 480 pixels with a picture aspect ratio of 16:9.</span></span> <span data-ttu-id="8fe35-136">Stream 1 是 1024 x 768 圖元，圖片的外觀比例為4:3。</span><span class="sxs-lookup"><span data-stu-id="8fe35-136">Stream 1 is a 1024 x 768 pixels with a picture aspect ratio of 4:3.</span></span>

<span data-ttu-id="8fe35-137">如果 VMR-9 使用 YUV 混合模式，它一律會選取資料流程0。</span><span class="sxs-lookup"><span data-stu-id="8fe35-137">If the VMR-9 is using YUV mixing mode, it always selects stream 0.</span></span> <span data-ttu-id="8fe35-138">因此，它會將串流1延伸至 540 x 480 圖元，以符合資料流程0的 PAR。</span><span class="sxs-lookup"><span data-stu-id="8fe35-138">Therefore, it stretches stream 1 to 540 x 480 pixels, to match the PAR of stream 0.</span></span>

<span data-ttu-id="8fe35-139">如果 VMR-9 使用 RGB 混合模式，它會選取資料流程1做為目標，因為該資料流程具有最大的影像大小。</span><span class="sxs-lookup"><span data-stu-id="8fe35-139">If the VMR-9 is using RGB mixing mode, it selects stream 1 as the target, because that stream has the largest image size.</span></span> <span data-ttu-id="8fe35-140">它會將資料流程0伸展為 1024 x 576 圖元的影像大小。</span><span class="sxs-lookup"><span data-stu-id="8fe35-140">It stretches stream 0 to an image size of 1024 x 576 pixels.</span></span> <span data-ttu-id="8fe35-141">請注意，在此情況下，複合影像的大小為1:1，因此配置器呈現者不需要針對非正方形圖元進行修正。</span><span class="sxs-lookup"><span data-stu-id="8fe35-141">Note that in this case, the composited image has a PAR of 1:1, so the allocator-presenter does not have to correct for non-square pixels.</span></span> <span data-ttu-id="8fe35-142"> (可能還是需要將影片延伸至目的地矩形的帳戶。 ) </span><span class="sxs-lookup"><span data-stu-id="8fe35-142">(It might still need to stretch the video to account for the destination rectangle.)</span></span>

<span data-ttu-id="8fe35-143">**使用非正方形混合模式**</span><span class="sxs-lookup"><span data-stu-id="8fe35-143">**Using Non-Square Mixing Mode**</span></span>

<span data-ttu-id="8fe35-144">如果下列任一條件成立，則建議使用非方形混合模式：</span><span class="sxs-lookup"><span data-stu-id="8fe35-144">Non-square mixing mode is recommended if either of the following conditions are true:</span></span>

-   <span data-ttu-id="8fe35-145">您的應用程式永遠不會將一個以上的影片串流傳送至 VMR-9。</span><span class="sxs-lookup"><span data-stu-id="8fe35-145">Your application never sends more than one video stream to the VMR-9.</span></span>
-   <span data-ttu-id="8fe35-146">您的應用程式會轉譯 DVD、電視或 ms dvr 檔案。</span><span class="sxs-lookup"><span data-stu-id="8fe35-146">Your application renders DVD, television, or ms-dvr files.</span></span> <span data-ttu-id="8fe35-147">在此情況下，如果圖形硬體支援，您也應該使用 YUV 混合模式。</span><span class="sxs-lookup"><span data-stu-id="8fe35-147">You should also use YUV mixing mode in this case, if the graphics hardware supports it.</span></span>

<span data-ttu-id="8fe35-148">如果您的應用程式混合多個可能具有不同影像大小或圖元外觀比例的影片串流，建議使用預設的正方形混合模式。</span><span class="sxs-lookup"><span data-stu-id="8fe35-148">If your application mixes multiple video streams that may have varying image sizes or pixel aspect ratios, the default square mixing mode is recommended.</span></span>

<span data-ttu-id="8fe35-149">若要設定非正方形混合模式，必須停止篩選圖形，並在 VMR-9 中斷所有輸入圖釘的連線。</span><span class="sxs-lookup"><span data-stu-id="8fe35-149">To configure non-square mixing mode, the filter graph must be stopped and all input pins disconnected on the VMR-9.</span></span> <span data-ttu-id="8fe35-150">然後使用 MixerPref9 NonSquareMixing 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ ：</span><span class="sxs-lookup"><span data-stu-id="8fe35-150">Then call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_NonSquareMixing flag:</span></span>


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> <span data-ttu-id="8fe35-151">如果您將 MixerPref9 \_ NonSquareMixing 旗標與 MixerPref9 \_ ARAdjustXorY 旗標結合，VMR-9 會忽略 MixerPref9 \_ ARAdjustXorY 旗標。</span><span class="sxs-lookup"><span data-stu-id="8fe35-151">If you combine the MixerPref9\_NonSquareMixing flag with the MixerPref9\_ARAdjustXorY flag, the VMR-9 ignores the MixerPref9\_ARAdjustXorY flag.</span></span>

 

<span data-ttu-id="8fe35-152">如果您的應用程式使用具有非方形混合模式的自訂配置器提供者，請注意複合影像可能具有非平方的。</span><span class="sxs-lookup"><span data-stu-id="8fe35-152">If your application uses a custom allocator-presenter with non-square mixing mode, be aware that the composited image may have a non-square PAR.</span></span> <span data-ttu-id="8fe35-153">配置器-展示者必須將影像調整為平方 (1:1) 等同。</span><span class="sxs-lookup"><span data-stu-id="8fe35-153">The allocator-presenter must scale the image to a square (1:1) PAR.</span></span>

<span data-ttu-id="8fe35-154">**靜態點陣圖**</span><span class="sxs-lookup"><span data-stu-id="8fe35-154">**Static Bitmaps**</span></span>

<span data-ttu-id="8fe35-155">如果您使用 [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) 介面將靜態點陣圖 blend 至影片，您應該將點陣圖視為第二個影片串流，以供 VMR 混合模式使用。</span><span class="sxs-lookup"><span data-stu-id="8fe35-155">If you use the [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) interface to blend a static bitmap onto the video, you should consider the bitmap to be a second video stream for purposes of the VMR mixing mode.</span></span>

<span data-ttu-id="8fe35-156">VMR 會將點陣圖視為等同于目標。</span><span class="sxs-lookup"><span data-stu-id="8fe35-156">The VMR treats the bitmap as having the same PAR as the target.</span></span> <span data-ttu-id="8fe35-157">它不會縮放點陣圖以調整目標的圖元外觀比例。</span><span class="sxs-lookup"><span data-stu-id="8fe35-157">It does not scale the bitmap to adjust for the target's pixel aspect ratio.</span></span> <span data-ttu-id="8fe35-158">在 VMR 的預設設定中，目標的1:1 等同于大部分的點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8fe35-158">In the VMR's default configuration, the target has a 1:1 PAR, which matches most bitmaps.</span></span> <span data-ttu-id="8fe35-159">在非方形混合模式中，目標可能具有非平方圖元。</span><span class="sxs-lookup"><span data-stu-id="8fe35-159">In non-square mixing mode, the target might have non-square pixels.</span></span> <span data-ttu-id="8fe35-160">為了確保點陣圖顯示正確，應用程式應該提供符合目標的影像。</span><span class="sxs-lookup"><span data-stu-id="8fe35-160">To ensure that the bitmap is displayed correctly, the application should supply an image whose PAR matches the target PAR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fe35-161">相關主題</span><span class="sxs-lookup"><span data-stu-id="8fe35-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fe35-162">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="8fe35-162">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



