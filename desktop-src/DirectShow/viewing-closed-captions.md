---
description: 查看隱藏式輔助字幕
ms.assetid: 86c0c553-af35-4ad1-8918-63d9e4577c73
title: 查看隱藏式輔助字幕
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82ff2d6d213259ccce6e9b02272d0c9db3ad7b71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104551023"
---
# <a name="viewing-closed-captions"></a><span data-ttu-id="8844e-103">查看隱藏式輔助字幕</span><span class="sxs-lookup"><span data-stu-id="8844e-103">Viewing Closed Captions</span></span>

<span data-ttu-id="8844e-104">為了支援類比電視中的隱藏式輔助字幕，「捕捉」篩選器會公開提供 VBI 或隱藏式輔助字幕資料的 pin。</span><span class="sxs-lookup"><span data-stu-id="8844e-104">To support closed captions in analog television, the capture filter exposes a pin that delivers either VBI or closed caption data.</span></span> <span data-ttu-id="8844e-105">Pin 會有下列其中一個 pin 類別：</span><span class="sxs-lookup"><span data-stu-id="8844e-105">The pin will have one of the following pin categories:</span></span>

-   <span data-ttu-id="8844e-106">VBI pin (釘選 \_ 類別 \_ VBI) 。</span><span class="sxs-lookup"><span data-stu-id="8844e-106">VBI pin (PIN\_CATEGORY\_VBI).</span></span> <span data-ttu-id="8844e-107">傳遞 VBI 波形範例的資料流程。</span><span class="sxs-lookup"><span data-stu-id="8844e-107">Delivers a stream of VBI waveform samples.</span></span> <span data-ttu-id="8844e-108">這些會傳遞至解碼篩選器，以解壓縮隱藏式輔助字幕資料。</span><span class="sxs-lookup"><span data-stu-id="8844e-108">These are passed to a decoder filter that extracts the closed captioning data.</span></span>
-   <span data-ttu-id="8844e-109">CC pin (釘 \_ 選 \_ cc) 。</span><span class="sxs-lookup"><span data-stu-id="8844e-109">CC pin (PIN\_CATEGORY\_CC).</span></span> <span data-ttu-id="8844e-110">傳遞已關閉的標題位元組組（從第21行資料解壓縮）。</span><span class="sxs-lookup"><span data-stu-id="8844e-110">Delivers closed-caption byte pairs, extracted from the line-21 data.</span></span>
-   <span data-ttu-id="8844e-111">硬體切割 CC pin (PINNAME \_ 影片 \_ 副本 \_) 。</span><span class="sxs-lookup"><span data-stu-id="8844e-111">Hardware slicing CC pin (PINNAME\_VIDEO\_CC\_CAPTURE).</span></span>

<span data-ttu-id="8844e-112">若要預覽隱藏式輔助字幕，請使用 VBI 釘選類別來呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) ，如果失敗，請使用 CC 類別再次呼叫它。</span><span class="sxs-lookup"><span data-stu-id="8844e-112">To preview closed captions, call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the VBI pin category, and if that fails, call it again with the CC category.</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, 0);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, 0);
}
```



<span data-ttu-id="8844e-113">下圖顯示用來顯示隱藏式輔助字幕的一般篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="8844e-113">The following diagram shows a typical filter graph for displaying closed captions.</span></span>

![隱藏式輔助字幕預覽圖形](images/vidcap08.png)

<span data-ttu-id="8844e-115">此圖表會使用下列篩選器來顯示隱藏式輔助字幕：</span><span class="sxs-lookup"><span data-stu-id="8844e-115">This graph uses the following filters for closed caption display:</span></span>

-   <span data-ttu-id="8844e-116">[T/接收到接收的轉換器](tee-sink-to-sink-converter.md)。</span><span class="sxs-lookup"><span data-stu-id="8844e-116">[Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md).</span></span> <span data-ttu-id="8844e-117">接受 capture 篩選器中的 VBI 資訊，並將其分割為信號上的每個資料服務的個別資料流程。</span><span class="sxs-lookup"><span data-stu-id="8844e-117">Accepts the VBI information from the capture filter and splits it into separate streams for each of the data services present on the signal.</span></span> <span data-ttu-id="8844e-118">Microsoft 針對隱藏式標題、NABTS 和全球標準 Teletext 提供 VBI 編解碼器 (WST) 。</span><span class="sxs-lookup"><span data-stu-id="8844e-118">Microsoft provides VBI codecs for Closed Caption, NABTS, and World Standard Teletext (WST).</span></span>
-   <span data-ttu-id="8844e-119">[CC 解碼器](cc-decoder-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="8844e-119">[CC Decoder](cc-decoder-filter.md).</span></span> <span data-ttu-id="8844e-120">從 capture 篩選器所提供的取樣 VBI 波形中解碼 CC 資料。</span><span class="sxs-lookup"><span data-stu-id="8844e-120">Decodes CC data from the sampled VBI waveforms provided by the capture filter.</span></span>
-   <span data-ttu-id="8844e-121">[第21行的解碼器](line-21-decoder-filter.md)。</span><span class="sxs-lookup"><span data-stu-id="8844e-121">[Line 21 Decoder](line-21-decoder-filter.md).</span></span> <span data-ttu-id="8844e-122">轉譯副本的位元組配對，並將標題文字繪製到點陣圖。</span><span class="sxs-lookup"><span data-stu-id="8844e-122">Translates the CC byte pairs and draws the caption text onto bitmaps.</span></span> <span data-ttu-id="8844e-123">下游篩選 (在此案例中，重迭混音器) 將點陣圖重迭到影片。</span><span class="sxs-lookup"><span data-stu-id="8844e-123">The downstream filter (in this case the Overlay Mixer) overlays the bitmaps onto the video.</span></span>

<span data-ttu-id="8844e-124">[Capture Graph Builder] 的 [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) 方法會自動加入這些篩選。</span><span class="sxs-lookup"><span data-stu-id="8844e-124">The Capture Graph Builder's [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds these filters automatically.</span></span> <span data-ttu-id="8844e-125">如果捕捉篩選具有 CC pin，而不是 VBI pin，則副本 pin 會直接連接到第21行的解碼篩選器。</span><span class="sxs-lookup"><span data-stu-id="8844e-125">If the capture filter has a CC pin instead of a VBI pin, the CC pin is connected directly to the Line 21 Decoder filter.</span></span>

> [!Note]  
> <span data-ttu-id="8844e-126">如果您使用影片混合轉譯器 (VMR) 篩選器進行轉譯，請使用第21行的解碼器篩選器2。</span><span class="sxs-lookup"><span data-stu-id="8844e-126">If you are using the Video Mixing Renderer (VMR) filter for rendering, use the Line 21 Decoder Filter 2.</span></span> <span data-ttu-id="8844e-127">此篩選器的功能與第21行的解碼器相同，但 CLSID 是 CLSID \_ Line21Decoder2。</span><span class="sxs-lookup"><span data-stu-id="8844e-127">This filter has the same functionality as the Line 21 Decoder, but the CLSID is CLSID\_Line21Decoder2.</span></span>

 

> [!Note]  
> <span data-ttu-id="8844e-128">在 Windows Vista 中已移除 CC 解碼器篩選。</span><span class="sxs-lookup"><span data-stu-id="8844e-128">The CC Decoder filter was removed in Windows Vista.</span></span> <span data-ttu-id="8844e-129">新的應用程式應該使用 VBICodec 篩選器，其記載于 Microsoft 電視技術檔中。</span><span class="sxs-lookup"><span data-stu-id="8844e-129">New applications should use the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

 

<span data-ttu-id="8844e-130">如果捕捉裝置使用影片埠，則 capture 篩選器可能會有影片埠 VBI 釘選， (PIN \_ 類別 \_ VIDEOPORT \_ VBI) 。</span><span class="sxs-lookup"><span data-stu-id="8844e-130">If the capture device uses a video port, the capture filter might have a video port VBI pin (PIN\_CATEGORY\_VIDEOPORT\_VBI).</span></span> <span data-ttu-id="8844e-131">此 pin 必須連接到 [VBI Surface](vbi-surface-allocator.md) 配置器篩選器，這會配置用來保存所捕捉 VBI 資料的表面。</span><span class="sxs-lookup"><span data-stu-id="8844e-131">This pin must be connected to the [VBI Surface Allocator](vbi-surface-allocator.md) filter, which allocates surfaces to hold the captured VBI data.</span></span> <span data-ttu-id="8844e-132">[**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)方法會在需要時加入此篩選準則。</span><span class="sxs-lookup"><span data-stu-id="8844e-132">The [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) method adds this filter if it is required.</span></span> <span data-ttu-id="8844e-133">下圖顯示具有 VBI Surface 配置器的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="8844e-133">The following diagram shows a filter graph with the VBI Surface Allocator.</span></span>

![隱藏式輔助字幕預覽圖形與 vbi surface 配置器](images/vidcap09.png)

### <a name="enabling-and-disabling-the-captions"></a><span data-ttu-id="8844e-135">啟用和停用標題</span><span class="sxs-lookup"><span data-stu-id="8844e-135">Enabling and Disabling the Captions</span></span>

<span data-ttu-id="8844e-136">若要控制字幕顯示，請使用第21行的 [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) 介面。</span><span class="sxs-lookup"><span data-stu-id="8844e-136">To control the captioning display, use the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface on the Line 21 Decoder filter.</span></span> <span data-ttu-id="8844e-137">例如，您可以使用 [**IAMLine21Decoder：： SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) 方法關閉字幕顯示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="8844e-137">For example, you can turn off the captioning display using the [**IAMLine21Decoder::SetServiceState**](/previous-versions/windows/desktop/api/il21dec/nf-il21dec-iamline21decoder-setservicestate) method, as follows:</span></span>


```C++
// Use the FindInterface method to find the interface.
IAMLine21Decoder *pLine21 = NULL;
hr = pBuild->FindInterface(
    &LOOK_DOWNSTREAM_ONLY, // Look downstream from pCap 
    NULL,                  // No particular media type
    pCap,                  // Pointer to the capture filter.
    IID_IAMLine21Decoder, (void**)&pLine21);
if (SUCCEEDED(hr))
{
    pLine21->SetServiceState(AM_L21_CCSTATE_Off);
    // (Use AM_L21_CCSTATE_On to enable.)
    pLine21->Release();
}
```



<span data-ttu-id="8844e-138">這個範例會使用 [**ICaptureGraphBuilder2：： FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) 方法來尋找 [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) 介面。</span><span class="sxs-lookup"><span data-stu-id="8844e-138">This example uses the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to locate the [**IAMLine21Decoder**](/previous-versions/windows/desktop/api/il21dec/nn-il21dec-iamline21decoder) interface.</span></span> <span data-ttu-id="8844e-139">要 **FindInterface** 的第一個參數是 **&\_ \_ 僅供下游參考**，這會指定從 capture 篩選器 (*pCap*) 搜尋下游。</span><span class="sxs-lookup"><span data-stu-id="8844e-139">The first parameter to **FindInterface** is **&LOOK\_DOWNSTREAM\_ONLY**, which specifies to search downstream from the capture filter (*pCap*).</span></span>

### <a name="capturing-closed-caption-bitmaps"></a><span data-ttu-id="8844e-140">捕獲隱藏式輔助字幕點陣圖</span><span class="sxs-lookup"><span data-stu-id="8844e-140">Capturing Closed Caption Bitmaps</span></span>

<span data-ttu-id="8844e-141">您可以將標題點陣圖捕捉到檔案中。</span><span class="sxs-lookup"><span data-stu-id="8844e-141">You can capture the caption bitmaps into a file.</span></span> <span data-ttu-id="8844e-142">若要這樣做，請新增篩選圖形的檔案寫入區段，如將 [影片捕獲到](capturing-video-to-a-file.md)檔案中所述。</span><span class="sxs-lookup"><span data-stu-id="8844e-142">To do so, add the file-writing section of the filter graph, as described in [Capturing Video to a File](capturing-video-to-a-file.md).</span></span> <span data-ttu-id="8844e-143">然後，將 CC 或 VBI 釘轉譯至 mux 篩選器：</span><span class="sxs-lookup"><span data-stu-id="8844e-143">Then render the CC or VBI pin to the mux filter:</span></span>


```C++
hr = pBuild->RenderStream(&PIN_CATEGORY_VBI, 0, pCap, 0, pMux);
if (FAILED(hr))
{
    hr = pBuild->RenderStream(&PIN_CATEGORY_CC, 0, pCap, 0, pMux);
}
```



<span data-ttu-id="8844e-144">如果您也要捕獲影片，這將會建立具有兩個不同影片串流的檔案。</span><span class="sxs-lookup"><span data-stu-id="8844e-144">If you are also capturing the video, this will create a file with two separate video streams.</span></span> <span data-ttu-id="8844e-145">它不會使用在圖片上方重迭的標題來捕獲影片。</span><span class="sxs-lookup"><span data-stu-id="8844e-145">It will not capture video with captions overlaid on top of the picture.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8844e-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="8844e-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8844e-147">隱藏式輔助字幕和 Teletext</span><span class="sxs-lookup"><span data-stu-id="8844e-147">Closed Captions and Teletext</span></span>](closed-captions-and-teletext.md)
</dt> </dl>

 

 



