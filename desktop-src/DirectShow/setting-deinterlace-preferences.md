---
description: 設定交錯喜好設定
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: 設定交錯喜好設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687380"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="a48f0-103">設定交錯喜好設定</span><span class="sxs-lookup"><span data-stu-id="a48f0-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="a48f0-104"> (VMR) 的影片混合轉譯器支援硬體加速去交錯，可改善交錯式影片的轉譯品質。</span><span class="sxs-lookup"><span data-stu-id="a48f0-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="a48f0-105">可用的確切功能取決於基礎硬體。</span><span class="sxs-lookup"><span data-stu-id="a48f0-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="a48f0-106">應用程式可以查詢硬體去交錯功能，並透過 [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) 介面設定去交錯喜好設定 (VMR-7) 或 [**IVMRDEINTERLACECONTROL9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) 介面 (VMR-9) 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="a48f0-107">去交錯會以每個資料流程為基礎執行。</span><span class="sxs-lookup"><span data-stu-id="a48f0-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="a48f0-108">VMR-7 和 VMR-9 之間的交錯行為有一個重要的差異。</span><span class="sxs-lookup"><span data-stu-id="a48f0-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="a48f0-109">在圖形硬體不支援 advanced 去交錯的系統上，VMR-7 可以切換回硬體重迭，並指示它使用 BOB 樣式的交錯。</span><span class="sxs-lookup"><span data-stu-id="a48f0-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="a48f0-110">在此情況下，雖然 VMR 是報告30fps，但影片實際上是轉譯成每秒60個翻轉。</span><span class="sxs-lookup"><span data-stu-id="a48f0-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="a48f0-111">除了使用硬體重迭的 VMR-7 案例之外，去交錯是由 VMR 的混音器所執行。</span><span class="sxs-lookup"><span data-stu-id="a48f0-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="a48f0-112">混音器會使用 DirectX Video 加速 (DXVA) 去交錯設備磁碟機介面 (DDI) 來執行去交錯。</span><span class="sxs-lookup"><span data-stu-id="a48f0-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="a48f0-113">應用程式無法呼叫此 DDI，應用程式無法取代 VMR 的去交錯功能。</span><span class="sxs-lookup"><span data-stu-id="a48f0-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="a48f0-114">不過，應用程式可以選取所需的去交錯模式，如本節所述。</span><span class="sxs-lookup"><span data-stu-id="a48f0-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="a48f0-115">本節說明 **IVMRDeinterlaceControl9** 方法，但 VMR-7 版本幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="a48f0-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="a48f0-116">若要取得影片串流的去交錯功能，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="a48f0-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="a48f0-117">使用影片資料流程的描述填入 [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) 結構。</span><span class="sxs-lookup"><span data-stu-id="a48f0-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="a48f0-118">稍後會提供如何填寫此結構的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a48f0-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="a48f0-119">將結構傳遞給 [**IVMRDeinterlaceControl9：： GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) 方法。</span><span class="sxs-lookup"><span data-stu-id="a48f0-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="a48f0-120">呼叫方法兩次。</span><span class="sxs-lookup"><span data-stu-id="a48f0-120">Call the method twice.</span></span> <span data-ttu-id="a48f0-121">第一個呼叫會傳回硬體針對指定的格式所支援的交錯模式數目。</span><span class="sxs-lookup"><span data-stu-id="a48f0-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="a48f0-122">配置此大小的 Guid 陣列，然後再次呼叫方法，傳遞陣列的位址。</span><span class="sxs-lookup"><span data-stu-id="a48f0-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="a48f0-123">第二個呼叫會以 Guid 填入陣列。</span><span class="sxs-lookup"><span data-stu-id="a48f0-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="a48f0-124">每個 GUID 會識別一個去交錯模式。</span><span class="sxs-lookup"><span data-stu-id="a48f0-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="a48f0-125">若要取得特定模式的 capabiltiies，請呼叫 [**IVMRDeinterlaceControl9：： GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) 方法。</span><span class="sxs-lookup"><span data-stu-id="a48f0-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="a48f0-126">傳入相同的 **VMR9VideoDesc** 結構，以及陣列中的其中一個 guid。</span><span class="sxs-lookup"><span data-stu-id="a48f0-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="a48f0-127">方法會以模式功能填入 [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) 結構。</span><span class="sxs-lookup"><span data-stu-id="a48f0-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="a48f0-128">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="a48f0-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="a48f0-129">現在應用程式可以使用下列方法來設定資料流程的去交錯模式：</span><span class="sxs-lookup"><span data-stu-id="a48f0-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="a48f0-130">[**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode)方法會設定慣用模式。</span><span class="sxs-lookup"><span data-stu-id="a48f0-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="a48f0-131">使用 GUID \_ Null 來關閉去交錯。</span><span class="sxs-lookup"><span data-stu-id="a48f0-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="a48f0-132">如果無法使用要求的模式， [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) 方法會指定行為。</span><span class="sxs-lookup"><span data-stu-id="a48f0-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="a48f0-133">[**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode)方法會傳回您所設定的慣用模式。</span><span class="sxs-lookup"><span data-stu-id="a48f0-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="a48f0-134">如果未提供慣用模式， [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) 方法會傳回使用中的實際模式，而這可能是回溯模式。</span><span class="sxs-lookup"><span data-stu-id="a48f0-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="a48f0-135">方法參考頁面會提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a48f0-135">The method reference pages give more information.</span></span>

<span data-ttu-id="a48f0-136">**使用 VMR9VideoDesc 結構**</span><span class="sxs-lookup"><span data-stu-id="a48f0-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="a48f0-137">在先前所述的程式中，第一個步驟是使用影片資料流程的描述填入 **VMR9VideoDesc** 結構。</span><span class="sxs-lookup"><span data-stu-id="a48f0-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="a48f0-138">從取得影片串流的媒體類型開始。</span><span class="sxs-lookup"><span data-stu-id="a48f0-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="a48f0-139">您可以在 VMR 篩選器的輸入 pin 上呼叫 [**IPin：： ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) 來執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="a48f0-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="a48f0-140">然後確認影片資料流程是否為交錯式。</span><span class="sxs-lookup"><span data-stu-id="a48f0-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="a48f0-141">只有 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 格式可以交錯。</span><span class="sxs-lookup"><span data-stu-id="a48f0-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="a48f0-142">如果格式類型為 VideoInfo 格式 \_ ，則必須是漸進式框架。</span><span class="sxs-lookup"><span data-stu-id="a48f0-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="a48f0-143">如果格式類型為 VideoInfo2 格式 \_ ，請檢查 AMINTERLACE IsInterlaced 旗標的 **dwInterlaceFlags** 欄位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="a48f0-144">此旗標的存在表示影片是交錯式的。</span><span class="sxs-lookup"><span data-stu-id="a48f0-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="a48f0-145">假設變數 **pBMI** 是格式區塊中 [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a48f0-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="a48f0-146">在 **VMR9VideoDesc** 結構中設定下列值：</span><span class="sxs-lookup"><span data-stu-id="a48f0-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="a48f0-147">**dwSize**：將此欄位設定為 `sizeof(VMR9VideoDesc)` 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="a48f0-148">**dwSampleWidth**：將此欄位設定為 `pBMI->biWidth` 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="a48f0-149">**dwSampleHeight**：將此欄位設定為 `abs(pBMI->biHeight)` 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="a48f0-150">**SampleFormat**：此欄位描述媒體類型的交錯特性。</span><span class="sxs-lookup"><span data-stu-id="a48f0-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="a48f0-151">檢查 **VIDEOINFOHEADER2** 結構中的 **dwInterlaceFlags** 欄位，並將 **SampleFormat** 設定為等於相等的 [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)旗標。</span><span class="sxs-lookup"><span data-stu-id="a48f0-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="a48f0-152">下面提供 helper 函式來進行這項作業。</span><span class="sxs-lookup"><span data-stu-id="a48f0-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="a48f0-153">**InputSampleFreq**：此欄位提供輸入頻率，可從 **VIDEOINFOHEADER2** 結構中的 **AvgTimePerFrame** 欄位計算。</span><span class="sxs-lookup"><span data-stu-id="a48f0-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="a48f0-154">在一般情況下，請將 **dwNumerator** 設定為10000000，並將 **DwDenominator** 設定為 **AvgTimePerFrame**。</span><span class="sxs-lookup"><span data-stu-id="a48f0-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="a48f0-155">不過，您也可以檢查一些已知的畫面播放速率：</span><span class="sxs-lookup"><span data-stu-id="a48f0-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="a48f0-156">每個畫面格的平均時間</span><span class="sxs-lookup"><span data-stu-id="a48f0-156">Average time per frame</span></span> | <span data-ttu-id="a48f0-157">畫面播放速率 (fps) </span><span class="sxs-lookup"><span data-stu-id="a48f0-157">Frame rate (fps)</span></span> | <span data-ttu-id="a48f0-158">分子</span><span class="sxs-lookup"><span data-stu-id="a48f0-158">Numerator</span></span> | <span data-ttu-id="a48f0-159">分母</span><span class="sxs-lookup"><span data-stu-id="a48f0-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="a48f0-160">166833</span><span class="sxs-lookup"><span data-stu-id="a48f0-160">166833</span></span>                 | <span data-ttu-id="a48f0-161">59.94 (NTSC) </span><span class="sxs-lookup"><span data-stu-id="a48f0-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="a48f0-162">60000</span><span class="sxs-lookup"><span data-stu-id="a48f0-162">60000</span></span>     | <span data-ttu-id="a48f0-163">1001</span><span class="sxs-lookup"><span data-stu-id="a48f0-163">1001</span></span>        |
    | <span data-ttu-id="a48f0-164">333667</span><span class="sxs-lookup"><span data-stu-id="a48f0-164">333667</span></span>                 | <span data-ttu-id="a48f0-165">29.97 (NTSC) </span><span class="sxs-lookup"><span data-stu-id="a48f0-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="a48f0-166">30000</span><span class="sxs-lookup"><span data-stu-id="a48f0-166">30000</span></span>     | <span data-ttu-id="a48f0-167">1001</span><span class="sxs-lookup"><span data-stu-id="a48f0-167">1001</span></span>        |
    | <span data-ttu-id="a48f0-168">417188</span><span class="sxs-lookup"><span data-stu-id="a48f0-168">417188</span></span>                 | <span data-ttu-id="a48f0-169">23.97 (NTSC) </span><span class="sxs-lookup"><span data-stu-id="a48f0-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="a48f0-170">24000</span><span class="sxs-lookup"><span data-stu-id="a48f0-170">24000</span></span>     | <span data-ttu-id="a48f0-171">1001</span><span class="sxs-lookup"><span data-stu-id="a48f0-171">1001</span></span>        |
    | <span data-ttu-id="a48f0-172">200000</span><span class="sxs-lookup"><span data-stu-id="a48f0-172">200000</span></span>                 | <span data-ttu-id="a48f0-173">50.00 (PAL) </span><span class="sxs-lookup"><span data-stu-id="a48f0-173">50.00 (PAL)</span></span>      | <span data-ttu-id="a48f0-174">50</span><span class="sxs-lookup"><span data-stu-id="a48f0-174">50</span></span>        | <span data-ttu-id="a48f0-175">1</span><span class="sxs-lookup"><span data-stu-id="a48f0-175">1</span></span>           |
    | <span data-ttu-id="a48f0-176">400000</span><span class="sxs-lookup"><span data-stu-id="a48f0-176">400000</span></span>                 | <span data-ttu-id="a48f0-177">25.00 (PAL) </span><span class="sxs-lookup"><span data-stu-id="a48f0-177">25.00 (PAL)</span></span>      | <span data-ttu-id="a48f0-178">25</span><span class="sxs-lookup"><span data-stu-id="a48f0-178">25</span></span>        | <span data-ttu-id="a48f0-179">1</span><span class="sxs-lookup"><span data-stu-id="a48f0-179">1</span></span>           |
    | <span data-ttu-id="a48f0-180">416667</span><span class="sxs-lookup"><span data-stu-id="a48f0-180">416667</span></span>                 | <span data-ttu-id="a48f0-181">24.00 (膠捲) </span><span class="sxs-lookup"><span data-stu-id="a48f0-181">24.00 (Film)</span></span>     | <span data-ttu-id="a48f0-182">24</span><span class="sxs-lookup"><span data-stu-id="a48f0-182">24</span></span>        | <span data-ttu-id="a48f0-183">1</span><span class="sxs-lookup"><span data-stu-id="a48f0-183">1</span></span>           |

    

     

-   <span data-ttu-id="a48f0-184">**OutputFrameFreq**：此欄位提供輸出頻率，可從 **InputSampleFreq** 值和輸入資料流程的交錯特性計算：</span><span class="sxs-lookup"><span data-stu-id="a48f0-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="a48f0-185">Set **OutputFrameFreq. dwDenominator** 等於 **InputSampleFreq. dwDenominator**。</span><span class="sxs-lookup"><span data-stu-id="a48f0-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="a48f0-186">如果輸入影片是交錯的，請將 **OutputFrameFreq. dwNumerator** 設定為 2 x **InputSampleFreq. dwNumerator**。</span><span class="sxs-lookup"><span data-stu-id="a48f0-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="a48f0-187">去交錯之後 (，畫面播放速率會加倍。 ) 否則，請將值設定為 **InputSampleFreq. dwNumerator**。</span><span class="sxs-lookup"><span data-stu-id="a48f0-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="a48f0-188">**dwFourCC**：將此欄位設定為 `pBMI->biCompression` 。</span><span class="sxs-lookup"><span data-stu-id="a48f0-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="a48f0-189">下列 helper 函數會將 AMINTERLACE \_ *X* 旗標轉換成 [**VMR9 \_ SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)值：</span><span class="sxs-lookup"><span data-stu-id="a48f0-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



