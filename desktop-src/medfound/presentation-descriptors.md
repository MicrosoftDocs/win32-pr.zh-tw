---
description: 簡報描述項
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: 簡報描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988690"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="3b32d-103">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="3b32d-103">Presentation Descriptors</span></span>

<span data-ttu-id="3b32d-104">*簡報* 是一組共用常見展示時間的相關媒體串流。</span><span class="sxs-lookup"><span data-stu-id="3b32d-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="3b32d-105">例如，簡報可能包含電影的音訊和影片串流。</span><span class="sxs-lookup"><span data-stu-id="3b32d-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="3b32d-106">*簡報描述* 項是一個物件，其中包含特定簡報的描述。</span><span class="sxs-lookup"><span data-stu-id="3b32d-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="3b32d-107">簡報描述項可用來設定媒體來源和某些媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="3b32d-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="3b32d-108">每個呈現描述項都包含一或多個 *資料流程描述* 項的清單。</span><span class="sxs-lookup"><span data-stu-id="3b32d-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="3b32d-109">這些會描述簡報中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b32d-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="3b32d-110">您可以選取或取消選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b32d-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="3b32d-111">只有選取的資料流程會產生資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-111">Only the selected streams produce data.</span></span> <span data-ttu-id="3b32d-112">取消選取的資料流程不在使用中，也不會產生任何資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="3b32d-113">每個資料流程描述項都有 *媒體類型處理常式*，可用來變更資料流程的媒體類型，或取得資料流程的目前媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3b32d-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="3b32d-114"> (如需有關媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="3b32d-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="3b32d-115">下表顯示這些物件所公開的主要介面。</span><span class="sxs-lookup"><span data-stu-id="3b32d-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="3b32d-116">Object</span><span class="sxs-lookup"><span data-stu-id="3b32d-116">Object</span></span>                  | <span data-ttu-id="3b32d-117">介面</span><span class="sxs-lookup"><span data-stu-id="3b32d-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3b32d-118">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="3b32d-118">Presentation descriptor</span></span> | [<span data-ttu-id="3b32d-119">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3b32d-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="3b32d-120">資料流程描述項</span><span class="sxs-lookup"><span data-stu-id="3b32d-120">Stream descriptor</span></span>       | [<span data-ttu-id="3b32d-121">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="3b32d-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="3b32d-122">媒體類型處理常式</span><span class="sxs-lookup"><span data-stu-id="3b32d-122">Media type handler</span></span>      | [<span data-ttu-id="3b32d-123">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="3b32d-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="3b32d-124">媒體來源簡報</span><span class="sxs-lookup"><span data-stu-id="3b32d-124">Media Source Presentations</span></span>

<span data-ttu-id="3b32d-125">每個媒體來源都提供描述來源預設設定的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="3b32d-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="3b32d-126">在預設設定中，至少選取一個資料流程，而每個選取的資料流程都有媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3b32d-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="3b32d-127">若要取得簡報描述項，請呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="3b32d-128">方法會傳回 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 指標。</span><span class="sxs-lookup"><span data-stu-id="3b32d-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="3b32d-129">您可以修改來源的展示描述項，以選取一組不同的資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b32d-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="3b32d-130">除非媒體來源已停止，否則請勿修改表示描述項。</span><span class="sxs-lookup"><span data-stu-id="3b32d-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="3b32d-131">當您呼叫 [**IMFMediaSource：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 來啟動來源時，會套用這些變更。</span><span class="sxs-lookup"><span data-stu-id="3b32d-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="3b32d-132">若要取得資料流程的數目，請呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="3b32d-133">若要取得資料流程的資料流程描述元，請呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，並傳入資料流程的索引。</span><span class="sxs-lookup"><span data-stu-id="3b32d-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="3b32d-134">資料流程是從零開始編制索引。</span><span class="sxs-lookup"><span data-stu-id="3b32d-134">Streams are indexed from zero.</span></span> <span data-ttu-id="3b32d-135">**GetStreamDescriptorByIndex** 方法會傳回 [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)指標。</span><span class="sxs-lookup"><span data-stu-id="3b32d-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="3b32d-136">它也會傳回布林值旗標，指出是否已選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b32d-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="3b32d-137">如果選取資料流程，媒體來源會產生該資料流程的資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="3b32d-138">否則，來源不會產生該資料流程的任何資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="3b32d-139">若要選取資料流程，請使用資料流程的索引來呼叫 [**IMFPresentationDescriptor：： SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) 。</span><span class="sxs-lookup"><span data-stu-id="3b32d-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="3b32d-140">若要取消選取資料流程，請呼叫 [**IMFPresentationDescriptor：:D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="3b32d-141">下列程式碼示範如何從媒體來源取得簡報描述項，並列舉資料流程。</span><span class="sxs-lookup"><span data-stu-id="3b32d-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="3b32d-142">媒體類型處理常式</span><span class="sxs-lookup"><span data-stu-id="3b32d-142">Media Type Handlers</span></span>

<span data-ttu-id="3b32d-143">若要變更資料流程的媒體類型或取得資料流程目前的媒體類型，請使用資料流程描述項的媒體類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="3b32d-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="3b32d-144">呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) 以取得媒體類型處理常式。</span><span class="sxs-lookup"><span data-stu-id="3b32d-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="3b32d-145">這個方法會傳回 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 指標。</span><span class="sxs-lookup"><span data-stu-id="3b32d-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="3b32d-146">如果您只想要知道串流中的資料類型（例如音訊或影片），請呼叫 [**IMFMediaTypeHandler：： GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="3b32d-147">這個方法會傳回主要媒體類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3b32d-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="3b32d-148">例如，播放應用程式通常會將音訊串流連接到音訊轉譯器和影片轉譯器。</span><span class="sxs-lookup"><span data-stu-id="3b32d-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="3b32d-149">如果您使用媒體會話或拓撲載入器來建立拓撲，主要類型 GUID 可能是您唯一需要的格式資訊。</span><span class="sxs-lookup"><span data-stu-id="3b32d-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="3b32d-150">如果您的應用程式需要更多有關目前格式的詳細資訊，請呼叫 [**IMFMediaTypeHandler：： GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="3b32d-151">這個方法會傳回媒體類型之 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3b32d-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="3b32d-152">使用此介面可取得格式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="3b32d-153">媒體類型處理常式也包含資料流程支援的媒體類型清單。</span><span class="sxs-lookup"><span data-stu-id="3b32d-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="3b32d-154">若要取得清單的大小，請呼叫 [**IMFMediaTypeHandler：： GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="3b32d-155">若要從清單中取得媒體類型，請使用媒體類型的索引來呼叫 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) 。</span><span class="sxs-lookup"><span data-stu-id="3b32d-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="3b32d-156">媒體類型會依喜好設定的近似順序傳回。</span><span class="sxs-lookup"><span data-stu-id="3b32d-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="3b32d-157">例如，針對音訊格式，較高的取樣率優先于較低的取樣率。</span><span class="sxs-lookup"><span data-stu-id="3b32d-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="3b32d-158">不過，沒有任何可控制順序的明確規則，因此您應該將它視為指導方針。</span><span class="sxs-lookup"><span data-stu-id="3b32d-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="3b32d-159">支援的類型清單可能不包含資料流程所支援的每種可能媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3b32d-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="3b32d-160">若要測試是否支援特定的媒體類型，請呼叫 [**IMFMediaTypeHandler：： IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="3b32d-161">若要設定媒體類型，請呼叫 [**IMFMediaTypeHandler：： SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype)。</span><span class="sxs-lookup"><span data-stu-id="3b32d-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="3b32d-162">如果方法成功，資料流程將會包含符合指定格式的資料。</span><span class="sxs-lookup"><span data-stu-id="3b32d-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="3b32d-163">**SetCurrentMediaType** 方法不會變更慣用類型的清單。</span><span class="sxs-lookup"><span data-stu-id="3b32d-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="3b32d-164">下列程式碼示範如何取得媒體類型處理常式、列舉慣用的媒體類型，以及設定媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3b32d-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="3b32d-165">此範例假設應用程式有一些演算法，而不是此處所示，無法選取媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3b32d-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="3b32d-166">細節會大幅依賴您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3b32d-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="3b32d-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="3b32d-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b32d-168">媒體來源</span><span class="sxs-lookup"><span data-stu-id="3b32d-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="3b32d-169">媒體基礎平臺 Api</span><span class="sxs-lookup"><span data-stu-id="3b32d-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



