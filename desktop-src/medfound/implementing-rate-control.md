---
description: 本主題說明自訂管線物件如何支援可變的播放率，包括反向播放。 如需從應用程式使用速率控制的詳細資訊，請參閱速率控制。
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: 執行速率控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027134"
---
# <a name="implementing-rate-control"></a><span data-ttu-id="832c9-104">執行速率控制</span><span class="sxs-lookup"><span data-stu-id="832c9-104">Implementing Rate Control</span></span>

<span data-ttu-id="832c9-105">本主題說明自訂管線物件如何支援可變的播放率，包括反向播放。</span><span class="sxs-lookup"><span data-stu-id="832c9-105">This topic describes how custom pipeline objects can support variable playback rates, including reverse playback.</span></span> <span data-ttu-id="832c9-106">如需從應用程式使用速率控制的詳細資訊，請參閱 [速率控制](rate-control.md)。</span><span class="sxs-lookup"><span data-stu-id="832c9-106">For information about using rate control from an application, see [Rate Control](rate-control.md).</span></span>

<span data-ttu-id="832c9-107">本主題包含下列幾節：</span><span class="sxs-lookup"><span data-stu-id="832c9-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="832c9-108">媒體來源</span><span class="sxs-lookup"><span data-stu-id="832c9-108">Media Sources</span></span>](#media-sources)
-   [<span data-ttu-id="832c9-109">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="832c9-109">Media Foundation Transforms</span></span>](#media-foundation-transforms)
    -   [<span data-ttu-id="832c9-110">反向播放</span><span class="sxs-lookup"><span data-stu-id="832c9-110">Reverse Playback</span></span>](#reverse-playback)
-   [<span data-ttu-id="832c9-111">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="832c9-111">Media Sinks</span></span>](#media-sinks)
-   [<span data-ttu-id="832c9-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="832c9-112">Related topics</span></span>](#related-topics)

<span data-ttu-id="832c9-113">如果您要 (媒體來源、轉換或媒體接收) 來撰寫 Microsoft 媒體基礎管線物件，您可能需要支援變數播放速率。</span><span class="sxs-lookup"><span data-stu-id="832c9-113">If you are writing a Microsoft Media Foundation pipeline object (a media source, transform, or media sink), you might need to support variable playback rates.</span></span> <span data-ttu-id="832c9-114">若要這樣做，請執行下列介面：</span><span class="sxs-lookup"><span data-stu-id="832c9-114">To do so, implement the following interfaces:</span></span>

1.  <span data-ttu-id="832c9-115">執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面。</span><span class="sxs-lookup"><span data-stu-id="832c9-115">Implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>
2.  <span data-ttu-id="832c9-116">支援 **MF \_ 速率 \_ 控制 \_ 服務** 服務。</span><span class="sxs-lookup"><span data-stu-id="832c9-116">Support the **MF\_RATE\_CONTROL\_SERVICE** service.</span></span> <span data-ttu-id="832c9-117"> (查看 [服務介面](service-interfaces.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="832c9-117">(See [Service Interfaces](service-interfaces.md).)</span></span>
3.  <span data-ttu-id="832c9-118">執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，以取得物件所支援的播放速率。</span><span class="sxs-lookup"><span data-stu-id="832c9-118">Implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface, which gets the playback rates supported by the object.</span></span>
4.  <span data-ttu-id="832c9-119">執行可取得或設定播放速率的 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="832c9-119">Implement the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface, which gets or sets the playback rate.</span></span>

## <a name="media-sources"></a><span data-ttu-id="832c9-120">媒體來源</span><span class="sxs-lookup"><span data-stu-id="832c9-120">Media Sources</span></span>

<span data-ttu-id="832c9-121">如果媒體來源支援速率控制，則應該同時執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。</span><span class="sxs-lookup"><span data-stu-id="832c9-121">If a media source supports rate control, it should implement both [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="832c9-122">否則，媒體會話會報告最小和最大播放速率為1.0，不論管線中有哪些其他元件。</span><span class="sxs-lookup"><span data-stu-id="832c9-122">Otherwise, the Media Session reports that the minimum and maximum playback rate is 1.0, regardless of what other components are in the pipeline.</span></span>

<span data-ttu-id="832c9-123">播放速率不會影響樣本的呈現時間，因此媒體來源不應調整其時間戳記。</span><span class="sxs-lookup"><span data-stu-id="832c9-123">The playback rate does not affect the presentation times of the samples, so the media source should not adjust its time stamps.</span></span> <span data-ttu-id="832c9-124">相反地，標記法會以較快或較慢的速度執行。</span><span class="sxs-lookup"><span data-stu-id="832c9-124">Instead, the presentation clock runs at a faster or slower speed.</span></span> <span data-ttu-id="832c9-125">若為反向播放，來源會以相反的順序傳遞範例，並減少時間戳記。</span><span class="sxs-lookup"><span data-stu-id="832c9-125">For reverse playback, the source delivers samples in reverse order, with decreasing time stamps.</span></span>

<span data-ttu-id="832c9-126">[**IMFRateControl：： SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)方法的 *fThin* 參數會指出媒體來源是否應將內容 *精簡*。</span><span class="sxs-lookup"><span data-stu-id="832c9-126">The *fThin* parameter of the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method indicates whether media source should *thin* the content.</span></span> <span data-ttu-id="832c9-127">Thinning 主要適用于影片串流。</span><span class="sxs-lookup"><span data-stu-id="832c9-127">Thinning applies primarily to video streams.</span></span> <span data-ttu-id="832c9-128">在 thinned 模式中，來源會卸載差異畫面格，並只提供主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="832c9-128">In thinned mode, the source drops delta frames and deliver only key frames.</span></span> <span data-ttu-id="832c9-129">在非常高的播放速率中，來源可能會略過一些主要畫面格 (例如，將每個其他主要畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="832c9-129">At very high playback rates, the source might skip some key frames (for example, deliver every other key frame).</span></span>

<span data-ttu-id="832c9-130">來源不需要以 thinned 模式卸載音訊樣本。</span><span class="sxs-lookup"><span data-stu-id="832c9-130">The source does not have to drop audio samples in thinned mode.</span></span> <span data-ttu-id="832c9-131">不過，以非常高的播放速度，來源可能無法讀取資料快速 nough 以填滿管線的範例要求。</span><span class="sxs-lookup"><span data-stu-id="832c9-131">At very high playback rates, however, the source might not be able to read data fast nough to fill the pipeline's sample requests.</span></span> <span data-ttu-id="832c9-132">在這種情況下，來源可能需要卸載某些音訊資料。</span><span class="sxs-lookup"><span data-stu-id="832c9-132">In that case, the source might need to drop some audio data.</span></span> <span data-ttu-id="832c9-133">如果是，則應該嘗試將接近時間的音訊範例傳遞給影片範例， (假設來源同時有兩種類型的資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="832c9-133">If so, it should attempt to deliver audio samples that are close in time to the video samples (assuming that the source has both types of stream).</span></span>

<span data-ttu-id="832c9-134">當資料流程在 thinned 和非 thinned 模式之間轉換時，它會傳送 [MEStreamThinMode](mestreamthinmode.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="832c9-134">When a stream transitions between thinned and non-thinned mode, it sends an [MEStreamThinMode](mestreamthinmode.md) event.</span></span>

<span data-ttu-id="832c9-135">當媒體來源完成呼叫 [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)時，它會傳送 [MESourceRateChanged](mesourceratechanged.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="832c9-135">When the media source completes a call to [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate), it sends the [MESourceRateChanged](mesourceratechanged.md) event.</span></span>

<span data-ttu-id="832c9-136">在反向播放期間：</span><span class="sxs-lookup"><span data-stu-id="832c9-136">During reverse playback:</span></span>

-   <span data-ttu-id="832c9-137">媒體來源會以反向順序傳遞範例，而不會調整時間戳記。</span><span class="sxs-lookup"><span data-stu-id="832c9-137">The media source delivers samples in reverse order, without adjusting the time stamps.</span></span>
-   <span data-ttu-id="832c9-138">資料流程中的時間戳記應該單純地減少。</span><span class="sxs-lookup"><span data-stu-id="832c9-138">Time stamps within a stream should monotonically decrease.</span></span>
-   <span data-ttu-id="832c9-139">內容的開頭會視為資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="832c9-139">The beginning of the content is considered the end of the stream.</span></span> <span data-ttu-id="832c9-140">在每個媒體資料流程提供資料流程中的第一個範例之後 (也就是說，presentation time = 0) ，它會傳送 [MEEndOfStream](meendofstream.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="832c9-140">After each media stream delivers the first sample in the stream (that is, presentation time = 0), it sends the [MEEndOfStream](meendofstream.md) event.</span></span>

## <a name="media-foundation-transforms"></a><span data-ttu-id="832c9-141">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="832c9-141">Media Foundation Transforms</span></span>

<span data-ttu-id="832c9-142">一般來說，媒體基礎轉換 (MFT) 不需要明確支援速率控制，除非該 MFT 會執行非 thinned 的反向播放。</span><span class="sxs-lookup"><span data-stu-id="832c9-142">In general, a Media Foundation transform (MFT) does not need explicit support for rate control, unless the MFT implements non-thinned reverse playback.</span></span>

<span data-ttu-id="832c9-143">如果 MFT 未執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，媒體會話會假設下列各項：</span><span class="sxs-lookup"><span data-stu-id="832c9-143">If an MFT does not implement the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface, the Media Session assumes the following:</span></span>

-   <span data-ttu-id="832c9-144">此 MFT 支援用於向前播放的任意播放速率，也就是 thinned 和非 thinned。</span><span class="sxs-lookup"><span data-stu-id="832c9-144">The MFT supports arbitary playback rates for forward playback, both thinned and non-thinned.</span></span>
-   <span data-ttu-id="832c9-145">此 MFT 支援 thinned 反向播放，但不支援非 thinned 反向播放。</span><span class="sxs-lookup"><span data-stu-id="832c9-145">The MFT supports thinned reverse playback, but does not support non-thinned reverse playback.</span></span>

<span data-ttu-id="832c9-146">如果上述任一條件不成立，則 MFT 應執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。</span><span class="sxs-lookup"><span data-stu-id="832c9-146">If either of these conditions is not true, the MFT should implement [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span>

### <a name="reverse-playback"></a><span data-ttu-id="832c9-147">反向播放</span><span class="sxs-lookup"><span data-stu-id="832c9-147">Reverse Playback</span></span>

<span data-ttu-id="832c9-148">即使管線中的一或多個轉換未明確支援反向播放，媒體會話仍可反向播放。</span><span class="sxs-lookup"><span data-stu-id="832c9-148">The Media Session can play in reverse even if one or more transforms in the pipeline do not explicitly support reverse playback.</span></span>

<span data-ttu-id="832c9-149">如果 MFT 未公開 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 介面，媒體會話就會使用 *thinning* 來進行反向播放，如下所示：</span><span class="sxs-lookup"><span data-stu-id="832c9-149">If an MFT does not expose the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface, the Media Session uses *thinning* for reverse playback, as follows:</span></span>

-   <span data-ttu-id="832c9-150">媒體會話藉由呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)，以平常的方式將主要畫面格傳送到 MFT。</span><span class="sxs-lookup"><span data-stu-id="832c9-150">The Media Session sends key frames to the MFT in the usual way, by calling [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

-   <span data-ttu-id="832c9-151">媒體會話會卸載 delta 框架，並將其取代為 [MEStreamTick](mestreamtick.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="832c9-151">The Media Session drops delta frames and replaces them with [MEStreamTick](mestreamtick.md) events.</span></span>

-   <span data-ttu-id="832c9-152">在每個範例之間，媒體會話都會排清 MFT，以避免因為時間戳記減少而造成的任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="832c9-152">Between each sample, the Media Session flushes the MFT, to avoid any errors caused by the fact that the time stamps are decreasing.</span></span>

<span data-ttu-id="832c9-153">如果範例的 [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) 屬性設定為 **TRUE**，則會將其視為主要畫面格，如果這個屬性為 **FALSE** 或未設定，則會被視為差異框架。</span><span class="sxs-lookup"><span data-stu-id="832c9-153">A sample is considered a key frame if it has the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute set to **TRUE**, and is considered a delta frame if this attribute is **FALSE** or not set.</span></span>

<span data-ttu-id="832c9-154">如果 MFT 執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)，媒體會話就會使用此介面來探索 MFT 是否支援非 thinned 反向播放。</span><span class="sxs-lookup"><span data-stu-id="832c9-154">If the MFT implements [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport), the Media Session uses this interface to discover whether the MFT supports non-thinned reverse playback.</span></span> <span data-ttu-id="832c9-155">如果 MFT 支援非 thinned 反向播放，媒體會話會以反向順序傳遞所有範例，而不會卸載樣本或清除 MFT。</span><span class="sxs-lookup"><span data-stu-id="832c9-155">If the MFT supports non-thinned reverse playback, the Media Session delivers all of the samples, in reverse order, without dropping samples or flushing the MFT.</span></span>

<span data-ttu-id="832c9-156">如果某個 MFT 支援非 thinned 反向播放，它應該會執行 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="832c9-156">If an MFT supports non-thinned reverse playback, it should implement the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span> <span data-ttu-id="832c9-157">當進行反向播放時，媒體會話將會使用此介面來通知 MFT。</span><span class="sxs-lookup"><span data-stu-id="832c9-157">The Media Session will use this interface to notify the MFT when reverse playback occurs.</span></span> <span data-ttu-id="832c9-158">屆時，必須針對時間戳記進行縮減，以使差異框架以相反的順序抵達。</span><span class="sxs-lookup"><span data-stu-id="832c9-158">At that point, the MFT must be prepared for the time stamps to decrease and for delta frames to arrive in reverse order.</span></span> <span data-ttu-id="832c9-159">解碼器通常需要緩衝範例，直到它收到整個圖形群組 (GOP) ，然後將整個 GOP 解碼，然後以正確的 (反向) 順序輸出已解碼的框架。</span><span class="sxs-lookup"><span data-stu-id="832c9-159">A decoder will typically need to buffer samples until it has received an entire group of pictures (GOP), then decode the entire GOP and output the decoded frames in the correct (reverse) order.</span></span>

## <a name="media-sinks"></a><span data-ttu-id="832c9-160">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="832c9-160">Media Sinks</span></span>

<span data-ttu-id="832c9-161">如果媒體接收器 *rateless*，媒體會話會假設媒體接收器可以處理任何播放速率。</span><span class="sxs-lookup"><span data-stu-id="832c9-161">If a media sink is *rateless*, the Media Session assumes that media sink can handle any playback rate.</span></span> <span data-ttu-id="832c9-162">媒體接收器不需要執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)。</span><span class="sxs-lookup"><span data-stu-id="832c9-162">The media sink does not need to implement [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport).</span></span> <span data-ttu-id="832c9-163"> (rateless 媒體接收會 \_ 從 [**IMFMediaSink：： GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) 方法傳回 MEDIASINK rateless 旗標 ) 。</span><span class="sxs-lookup"><span data-stu-id="832c9-163">(A rateless media sink returns the MEDIASINK\_RATELESS flag from the [**IMFMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) method.)</span></span>

<span data-ttu-id="832c9-164">否則，如果媒體接收器可以處理1.0 以外的播放率，則應該執行 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 。</span><span class="sxs-lookup"><span data-stu-id="832c9-164">Otherwise, a media sink should implement [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) if it can handle playback rates other than 1.0.</span></span>

<span data-ttu-id="832c9-165">媒體接收器不應執行 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)。</span><span class="sxs-lookup"><span data-stu-id="832c9-165">Media sinks should not implement [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol).</span></span> <span data-ttu-id="832c9-166">當播放速率變更時，呈現時鐘會呼叫媒體接收器的 [**IMFClockStateSink：： OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) 方法。</span><span class="sxs-lookup"><span data-stu-id="832c9-166">When the playback rate changes, the presentation clock calls the media sink's [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="832c9-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="832c9-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="832c9-168">速率控制</span><span class="sxs-lookup"><span data-stu-id="832c9-168">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="832c9-169">搜尋、向前快轉及反向播放</span><span class="sxs-lookup"><span data-stu-id="832c9-169">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



