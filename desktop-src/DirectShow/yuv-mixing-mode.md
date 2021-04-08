---
description: YUV 混合模式
ms.assetid: 296b1d96-1824-4000-8bec-158925555177
title: YUV 混合模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf4ca6b1ba5317145c410d6e5b899c7cf264f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851368"
---
# <a name="yuv-mixing-mode"></a><span data-ttu-id="c3206-103">YUV 混合模式</span><span class="sxs-lookup"><span data-stu-id="c3206-103">YUV Mixing Mode</span></span>

<span data-ttu-id="c3206-104">本主題適用于 Windows XP Service Pack 2 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c3206-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="c3206-105">從 Windows XP Service Pack 2 開始，VMR 支援稱為 YUV 混合模式的混合模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-105">Starting in Windows XP Service Pack 2, the VMR supports a mixing mode called YUV mixing mode.</span></span> <span data-ttu-id="c3206-106">這種模式最適用于先進的電視或 DVD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3206-106">This mode is most useful for advanced TV or DVD applications.</span></span> <span data-ttu-id="c3206-107">它會在使用統一記憶體架構設計的低終端圖形硬體上，以更佳的效能來為 VMR 混音器提供更佳的效能。</span><span class="sxs-lookup"><span data-stu-id="c3206-107">It trades some of the power of the VMR mixer for better performance on low end graphics hardware that uses a unified memory architecture design.</span></span> <span data-ttu-id="c3206-108">VMR-7 和 VMR-9 都支援 YUV 混合模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-108">YUV mixing mode is supported on both the VMR-7 and VMR-9.</span></span>

<span data-ttu-id="c3206-109">**優點**</span><span class="sxs-lookup"><span data-stu-id="c3206-109">**Advantages**</span></span>

<span data-ttu-id="c3206-110">YUV 混合模式有幾個優點，與 VMR 所支援的原始 RGB 混合模式轉譯效能有關：</span><span class="sxs-lookup"><span data-stu-id="c3206-110">YUV mixing mode has several advantages relating to rendering performance over the original RGB mixing mode supported by the VMR:</span></span>

-   <span data-ttu-id="c3206-111">當 VMR 處於 YUV 混合模式時，所有的取消交錯和影片串流組合作業都會以 YUV 色彩空間來執行。</span><span class="sxs-lookup"><span data-stu-id="c3206-111">When the VMR is in YUV mixing mode, all de-interlacing and video stream composition operations are performed in YUV color space.</span></span> <span data-ttu-id="c3206-112">YUV 表面通常需要50% 到60% 的記憶體頻寬，比對等的 RGB 介面還要低。</span><span class="sxs-lookup"><span data-stu-id="c3206-112">YUV surfaces typically require from 50% to 60% less memory bandwidth than equivalent RGB surfaces.</span></span>
-   <span data-ttu-id="c3206-113">去交錯和資料流程組合是由單一呼叫圖形驅動程式來執行。</span><span class="sxs-lookup"><span data-stu-id="c3206-113">The deinterlacing and stream composition are performed by a single call to the graphics driver.</span></span> <span data-ttu-id="c3206-114">此驅動程式可以使用圖形硬體的多重紋理功能，因而節省額外的記憶體頻寬。</span><span class="sxs-lookup"><span data-stu-id="c3206-114">The driver can use the graphics hardware's multi-texturing capabilities, resulting in additional memory bandwidth savings.</span></span>

<span data-ttu-id="c3206-115">雖然任何影片應用程式都可以使用 YUV 混合模式，但主要是用於兩種類型的影片播放應用程式：</span><span class="sxs-lookup"><span data-stu-id="c3206-115">Although any video application can use YUV mixing mode, it is primarily intended for two types of video playback application:</span></span>

1.  <span data-ttu-id="c3206-116">顯示隱藏式字幕或 teletext 的電視應用程式。</span><span class="sxs-lookup"><span data-stu-id="c3206-116">TV applications that display closed captions or teletext.</span></span>
2.  <span data-ttu-id="c3206-117">DVD 應用程式會顯示 DVD 子圖片資料或隱藏式輔助字幕。</span><span class="sxs-lookup"><span data-stu-id="c3206-117">DVD applications display DVD subpicture data or closed captions.</span></span>

<span data-ttu-id="c3206-118">**限制**</span><span class="sxs-lookup"><span data-stu-id="c3206-118">**Restrictions**</span></span>

<span data-ttu-id="c3206-119">當 VMR 進入 YUV 混合模式時，會強制執行一些限制：</span><span class="sxs-lookup"><span data-stu-id="c3206-119">A number of restrictions are enforced by the VMR when it is put into YUV mixing mode:</span></span>

-   <span data-ttu-id="c3206-120">Stream 0 (連接至輸入 Pin 0) 的資料流程可以是漸進式或交錯式;所有其他資料流程都必須是漸進式的。</span><span class="sxs-lookup"><span data-stu-id="c3206-120">Stream 0 (the stream connected to Input Pin 0) can be progressive or interlaced; all other streams must be progressive.</span></span>
-   <span data-ttu-id="c3206-121">\_不允許串流0使用 GUID Null (編織模式) 。</span><span class="sxs-lookup"><span data-stu-id="c3206-121">GUID\_NULL (weave mode) is not allowed for stream 0.</span></span>
-   <span data-ttu-id="c3206-122">\_因為這可能會使非交錯裝置無法建立，所以無法使用 DeinterlacePref 的編織作為回溯模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-122">DeinterlacePref\_Weave cannot be used as a fallback mode because this could prevent a de-interlace device from being created.</span></span> <span data-ttu-id="c3206-123">因為連入的影片不是交錯式的，所以 YUV 混合模式需要經過隔行掃描裝置。</span><span class="sxs-lookup"><span data-stu-id="c3206-123">YUV mixing mode requires a deinterlace device even if the incoming video is not interlaced.</span></span>
-   <span data-ttu-id="c3206-124">與每個 VMR 輸入資料流程相關聯的平面 Alpha 值都不會進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="c3206-124">No changes can be made to the planar alpha value associated with each VMR input stream.</span></span>
-   <span data-ttu-id="c3206-125">使用者無法改變連接的影片資料流程的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="c3206-125">The user cannot alter the Z-order of the connected video streams.</span></span> <span data-ttu-id="c3206-126">預設的 Z 順序是取自釘選順序。</span><span class="sxs-lookup"><span data-stu-id="c3206-126">The default Z-order is taken from the pin order.</span></span>
-   <span data-ttu-id="c3206-127">不支援色彩加密。</span><span class="sxs-lookup"><span data-stu-id="c3206-127">Color keying is not supported.</span></span>
-   <span data-ttu-id="c3206-128">輸入 pin 0 必須接收影片串流。</span><span class="sxs-lookup"><span data-stu-id="c3206-128">Input pin 0 must receive the video stream.</span></span>
-   <span data-ttu-id="c3206-129">其他輸入的 pin 只能接收影片子資料流程資料，例如 DVD 子圖片、隱藏式輔助字幕或 teletext。</span><span class="sxs-lookup"><span data-stu-id="c3206-129">The other inputs pins can only receive video sub-stream data such as DVD sub-picture, closed captions or teletext.</span></span>
-   <span data-ttu-id="c3206-130">其他輸入釘選只能接受每圖元的 Alpha YUV 格式，例如 AYUV、AI44 和 IA44。</span><span class="sxs-lookup"><span data-stu-id="c3206-130">The other inputs pins can only accept per-pixel alpha YUV formats, such as AYUV, AI44 and IA44.</span></span>
-   <span data-ttu-id="c3206-131">VMR 的輸入圖釘都不能接受任何 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="c3206-131">None of the VMR's input pins can accept any RGB formats.</span></span>
-   <span data-ttu-id="c3206-132">應用程式提供的點陣圖影像在呈現至顯示器之前，無法再與影片合併。</span><span class="sxs-lookup"><span data-stu-id="c3206-132">Application supplied bitmap images can no longer be combined with the video prior to presentation to the display.</span></span>
-   <span data-ttu-id="c3206-133">您無法使用 VMR 的混音器「輸出矩形」函式，以水準或垂直方式反轉個別的子資料流程。</span><span class="sxs-lookup"><span data-stu-id="c3206-133">Individual sub-streams cannot be inverted horizontally or vertically using the VMR's mixer "output rectangle" functions.</span></span> <span data-ttu-id="c3206-134">支援「正常」的資料流程重新置放和調整大小。</span><span class="sxs-lookup"><span data-stu-id="c3206-134">"Normal" stream re-positioning and re-sizing is supported.</span></span>
-   <span data-ttu-id="c3206-135">[**IVMRMixerControl：： SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) 指定的混合背景色彩 (仍是在 rgb 色彩空間中指定，就像在 rgb 混合模式中一樣。</span><span class="sxs-lookup"><span data-stu-id="c3206-135">The mixing background color (specified by [**IVMRMixerControl::SetBackgroundClr**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setbackgroundclr)) is still specified in the RGB color space, just as in RGB mixing mode.</span></span>

<span data-ttu-id="c3206-136">**Configuration**</span><span class="sxs-lookup"><span data-stu-id="c3206-136">**Configuration**</span></span>

<span data-ttu-id="c3206-137">應用程式必須明確設定 VMR，以利用 YUV 混合模式;原始 RGB 混合模式會維持預設的混合模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-137">Applications must explicitly configure the VMR to take advantage of YUV mixing mode; the original RGB mixing mode remains the default mixing mode.</span></span> <span data-ttu-id="c3206-138">若要啟用 VMR-7 中的 YUV 混合模式，請使用 MixerPref RenderTargetYUV 旗標來呼叫 [**IVMRMixerControl：： SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3206-138">To enable YUV mixing mode in the VMR-7, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect) with the MixerPref\_RenderTargetYUV flag.</span></span> <span data-ttu-id="c3206-139">您必須在連接任何 VMR 的輸入圖釘之前進行此呼叫。</span><span class="sxs-lookup"><span data-stu-id="c3206-139">This call must be made before any of the VMR's input pins are connected.</span></span> <span data-ttu-id="c3206-140">若要啟用 VMR-9 中的 YUV 混合模式，請使用 MixerPref9 RenderTargetYUV 旗標來呼叫 [**IVMRMixerControl9：： SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3206-140">To enable YUV mixing mode in the VMR-9, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) with the MixerPref9\_RenderTargetYUV flag.</span></span>

<span data-ttu-id="c3206-141">判斷 VMR-7 是否支援新的 YUV 混合模式的唯一方式，就是嘗試將 VMR 設為該模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-141">The only way to determine if the VMR-7 supports the new YUV mixing mode is to try setting the VMR into that mode.</span></span> <span data-ttu-id="c3206-142">如果呼叫成功，您仍然可以視需要將 VMR 放回 RGB 混合模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-142">If the call succeeds, you can still put the VMR back into RGB mixing mode if necessary.</span></span> <span data-ttu-id="c3206-143">在設定為 YUV 混合模式之後，VMR 只能在所有輸入接點都中斷連線之後，變更回 RGB 混合模式。</span><span class="sxs-lookup"><span data-stu-id="c3206-143">After it is set into YUV mixing mode, the VMR can only be changed back to RGB mixing mode after all input pins have been disconnected.</span></span>

<span data-ttu-id="c3206-144">在 YUV 混合模式中，您可以在 **SetMixingPrefs** 方法中套用下列旗標，以降低圖形處理器 (GPU) 的負載：</span><span class="sxs-lookup"><span data-stu-id="c3206-144">In YUV mixing mode, you can reduce the load on the graphics processing unit (GPU) by applying the following flags in the **SetMixingPrefs** method:</span></span>



| <span data-ttu-id="c3206-145">旗標</span><span class="sxs-lookup"><span data-stu-id="c3206-145">Flag</span></span>                                                                                 | <span data-ttu-id="c3206-146">描述</span><span class="sxs-lookup"><span data-stu-id="c3206-146">Description</span></span>                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c3206-147">VMR-7： MixerPref \_ DynamicSwitchToBOBVMR-9： MixerPref9 \_ DynamicSwitchToBOB</span><span class="sxs-lookup"><span data-stu-id="c3206-147">VMR-7: MixerPref\_DynamicSwitchToBOBVMR-9: MixerPref9\_DynamicSwitchToBOB</span></span><br/> | <span data-ttu-id="c3206-148">切換至 bob 去交錯。</span><span class="sxs-lookup"><span data-stu-id="c3206-148">Switch to bob deinterlacing.</span></span>                                     |
| <span data-ttu-id="c3206-149">VMR-7： MixerPref \_ DynamicDecimateBy2VMR-9： MixerPref \_ DynamicDecimateBy2</span><span class="sxs-lookup"><span data-stu-id="c3206-149">VMR-7: MixerPref\_DynamicDecimateBy2VMR-9: MixerPref\_DynamicDecimateBy2</span></span><br/>  | <span data-ttu-id="c3206-150">以水準和垂直比例刪減影像。</span><span class="sxs-lookup"><span data-stu-id="c3206-150">Decimate the image by a factor of 2 horizontally and vertically.</span></span> |



 

<span data-ttu-id="c3206-151">當篩選圖形正在執行時，您可以新增或移除這些旗標;當 VMR 混音器撰寫下一個影片畫面格時，就會套用變更。</span><span class="sxs-lookup"><span data-stu-id="c3206-151">You can add or remove these flags while the filter graph is running; the change is applied when the VMR mixer composes the next video frame.</span></span> <span data-ttu-id="c3206-152">旗標不是互斥的。</span><span class="sxs-lookup"><span data-stu-id="c3206-152">The flags are not mutually exclusive.</span></span> <span data-ttu-id="c3206-153">這些設定會降低影像的品質，因此通常只有當影片品質較不重要（例如，如果影片是在使用者介面的一小部分中播放）時才適用。</span><span class="sxs-lookup"><span data-stu-id="c3206-153">These settings reduce the quality of the image, so typically you would apply them only when video quality is less important — for example, if video is playing in a small portion of the user interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3206-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="c3206-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3206-155">使用 VMR 混合模式</span><span class="sxs-lookup"><span data-stu-id="c3206-155">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 




