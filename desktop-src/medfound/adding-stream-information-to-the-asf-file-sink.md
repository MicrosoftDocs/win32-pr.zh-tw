---
description: 深入瞭解如何將 stream 資訊新增至 ASF 檔案接收，應用程式可以使用該檔案來將 ASF 媒體資料封存至檔案。
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: 將資料流程資訊新增至 ASF 檔案接收
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404353"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a><span data-ttu-id="d5dc3-103">將資料流程資訊新增至 ASF 檔案接收</span><span class="sxs-lookup"><span data-stu-id="d5dc3-103">Adding Stream Information to the ASF File Sink</span></span>

<span data-ttu-id="d5dc3-104">ASF 檔案接收是媒體基礎所提供的 [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) ，可讓應用程式用來將 ASF 媒體資料封存至檔案。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-104">The ASF file sink is an implementation of [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) provided by Media Foundation that an application can use to archive ASF media data to a file.</span></span> <span data-ttu-id="d5dc3-105">如需 ASF 媒體接收器的物件模型和一般使用方式的相關資訊，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-105">For information about ASF Media Sinks' object model and general usage, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

<span data-ttu-id="d5dc3-106">在具現化檔案接收之後，必須先設定它，才能建立拓撲。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-106">After instantiating the file sink, it must be configured before building the topology.</span></span> <span data-ttu-id="d5dc3-107">檔案接收需要知道輸出檔中的資料流程、編碼模式資訊和中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-107">The file sink needs to know about the streams in the output file, the encoding mode information, and the metadata.</span></span> <span data-ttu-id="d5dc3-108">本主題說明在檔案接收中加入資料流程的程式。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-108">This topic describes the process of adding stream in the file sink.</span></span>

-   [<span data-ttu-id="d5dc3-109">在 ASF 檔案接收中新增資料流程</span><span class="sxs-lookup"><span data-stu-id="d5dc3-109">Adding Streams in the ASF File Sink</span></span>](#adding-streams-in-the-asf-file-sink)
-   [<span data-ttu-id="d5dc3-110">列舉資料流程接收</span><span class="sxs-lookup"><span data-stu-id="d5dc3-110">Enumerating Stream Sinks</span></span>](#enumerating-stream-sinks)
-   [<span data-ttu-id="d5dc3-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5dc3-111">Related topics</span></span>](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a><span data-ttu-id="d5dc3-112">在 ASF 檔案接收中新增資料流程</span><span class="sxs-lookup"><span data-stu-id="d5dc3-112">Adding Streams in the ASF File Sink</span></span>

<span data-ttu-id="d5dc3-113">檔案接收必須知道輸出資料流程及其屬性，才能據以產生輸出範例，並將其新增至輸出 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-113">The file sink must know of the output streams and their properties so that it can generate output samples accordingly and add them to the output ASF file.</span></span> <span data-ttu-id="d5dc3-114">這些設定會寫入到最後一個 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-114">These settings are written to the final ASF Header Object.</span></span>

<span data-ttu-id="d5dc3-115">若要設定資料流程資訊，您必須有 file 接收器的 ASF ContentInfo 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-115">To set stream information, you must have a reference to the file sink's ASF ContentInfo object.</span></span> <span data-ttu-id="d5dc3-116">如需詳細資訊，請參閱 [建立 ASF 檔案接收](creating-the-asf-file-sink.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-116">For information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="d5dc3-117">下列程式摘要說明使用 ASF 設定檔物件來設定資料流程的一般步驟。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-117">The following procedure summarizes the general steps for configuring stream by using the ASF profile object.</span></span>

<span data-ttu-id="d5dc3-118">**在 ASF 檔案接收中設定串流資訊**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-118">**To configure stream information in the ASF file sink**</span></span>

1.  <span data-ttu-id="d5dc3-119">藉由呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)來建立 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-119">Create an ASF profile object by calling [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).</span></span>
2.  <span data-ttu-id="d5dc3-120">針對輸出檔中的每個資料流程，建立要在檔案接收中加入之目標資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-120">For each stream in the output file, create a media type for the target stream to be added in the file sink.</span></span> <span data-ttu-id="d5dc3-121">媒體類型必須與 Windows Media 編碼器支援的輸出類型相容。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-121">The media type must be compatible with the output types supported by the Windows Media encoders.</span></span>

    <span data-ttu-id="d5dc3-122">如需將音訊串流新增至設定檔的相關資訊，請參閱建立適用于 ASF 編碼的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-122">For information about adding audio streams to the profile, see Creating Audio Streams for ASF Encoding.</span></span>

    <span data-ttu-id="d5dc3-123">如需將視頻串流新增至設定檔的相關資訊，請參閱建立適用于 ASF 編碼的影片串流。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-123">For information about adding video streams to the profile, see Creating Video Streams for ASF Encoding.</span></span>

3.  <span data-ttu-id="d5dc3-124">藉由呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream)，根據步驟2中建立的媒體類型建立資料流程。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-124">Create streams based on the media types created in step 2 by calling [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).</span></span>
4.  <span data-ttu-id="d5dc3-125">藉由呼叫步驟3中所收到的 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面指標，指派新建立資料流程的資料流程號碼。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-125">Assign a stream number for the newly created stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface pointer received in step 3.</span></span>
5.  <span data-ttu-id="d5dc3-126">選擇性地使用下列資訊設定資料流程：</span><span class="sxs-lookup"><span data-stu-id="d5dc3-126">Optionally configure the stream with the following information:</span></span>
    -   <span data-ttu-id="d5dc3-127">藉由設定屬性來有漏洞 bucket 參數： [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 或 [**mf \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="d5dc3-127">Leaky bucket parameters by setting the attributes: [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)</span></span>
    -   <span data-ttu-id="d5dc3-128">裝載延伸，藉由呼叫 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 方法相互排除。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-128">Payload extension, mutual exclusion by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods.</span></span>
6.  <span data-ttu-id="d5dc3-129">藉由設定 [**mf \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) 和 [**mf \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) 屬性，選擇性地設定設定檔的資料封包大小。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-129">Optionally set data packet size for the profile by setting [**MF\_ASFPROFILE\_MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) and [**MF\_ASFPROFILE\_MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) attributes.</span></span> <span data-ttu-id="d5dc3-130">ASF 設定檔會公開 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面，應用程式可以藉由呼叫 **IMFASFProfile：： QueryInterface** 來取得其參考。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-130">The ASF profile exposes the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface, which an application can get reference to by calling **IMFASFProfile::QueryInterface**.</span></span>
7.  <span data-ttu-id="d5dc3-131">在檔案接收中設定資料流程的編碼資訊。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-131">Set encoding information for the stream in the file sink.</span></span> <span data-ttu-id="d5dc3-132">在 [檔接收器中設定屬性的](setting-properties-in-the-file-sink.md)討論。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-132">Discussed in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
8.  <span data-ttu-id="d5dc3-133">藉由呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)，將資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-133">Add the stream to the profile by calling [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).</span></span>
9.  <span data-ttu-id="d5dc3-134">藉由呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)，將設定檔與 ContentInfo 物件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-134">Associate the profile with the ContentInfo object by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span>

<span data-ttu-id="d5dc3-135">若要修改現有的資料流程，應用程式可以取得資料流程 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的參考，並根據需求加以重新設定。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-135">To modify an existing stream, the application can get a reference to the stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface and reconfigure it according to the requirements.</span></span> <span data-ttu-id="d5dc3-136">若要加入或移除資料流程，應用程式必須呼叫 [**IMFASFProfile：： RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-136">To add or remove streams, the application must call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).</span></span> <span data-ttu-id="d5dc3-137">若要套用這些變更、串流修改或移除，您必須在 ContentInfo 物件中再次設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-137">To apply these changes, stream modifications or removal, you must set the profile again in the ContentInfo object.</span></span> <span data-ttu-id="d5dc3-138">這會覆寫已與 ContentInfo 物件相關聯的現有設定檔。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-138">This overwrites the existing profile that is already associated with the ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a><span data-ttu-id="d5dc3-139">列舉資料流程接收</span><span class="sxs-lookup"><span data-stu-id="d5dc3-139">Enumerating Stream Sinks</span></span>

<span data-ttu-id="d5dc3-140">針對 ContentInfo 物件感知的設定檔中的每個資料流程，ASF 檔案接收會建立並加入包含已編碼資料流程之所有屬性的資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-140">For each stream in the profile that the ContentInfo object is aware of, the ASF file sink creates and adds a stream sink that contains all the properties of the encoded stream.</span></span> <span data-ttu-id="d5dc3-141">ASF file 接收器的設計目的是要包含固定的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-141">The ASF file sink is designed to contain fixed streams.</span></span> <span data-ttu-id="d5dc3-142">這表示您無法藉由呼叫 [**IMFMediaSink：： AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) 或 [**IMFMediaSink：： RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)來新增或移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-142">This means that you cannot add or remove streams by calling [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) or [**IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink).</span></span> <span data-ttu-id="d5dc3-143">這些對檔案接收的呼叫會失敗，並出現 MF \_ E \_ STREAMSINKS \_ 固定錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-143">These calls on the file sink fail with the MF\_E\_STREAMSINKS\_FIXED error code.</span></span> <span data-ttu-id="d5dc3-144">在設定檔中新增或移除資料流程時，不會自動新增或移除檔案接收中的串流接收器。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-144">Adding or removing streams in the profile does not automatically add or remove the stream sinks in the file sink.</span></span> <span data-ttu-id="d5dc3-145">如果設定檔中的資料流程已變更，您必須捨棄檔案的現有實例，並以新的資料流程資訊重新建立它。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-145">You must discard the existing instance of the file and recreate it with new stream information if your streams in the profile have changed.</span></span>

<span data-ttu-id="d5dc3-146">下列程式摘要說明在 ASF 檔案接收中列舉串流接收器的一般步驟。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-146">The following procedure summarizes the general steps for enumerating stream sinks in the ASF file sink.</span></span>

<span data-ttu-id="d5dc3-147">**列舉資料流程接收**</span><span class="sxs-lookup"><span data-stu-id="d5dc3-147">**To enumerate stream sinks**</span></span>

1.  <span data-ttu-id="d5dc3-148">呼叫 [**IMFMediaSink：： GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) ，以取得 ASF 檔案接收中的串流接收器總數。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-148">Call [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) to get the total number of stream sinks in the ASF file sink.</span></span>
2.  <span data-ttu-id="d5dc3-149">流經串流接收器的迴圈會取得資料流程接收器 [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-149">Loop through the stream sinks ang get a reference to the stream sink's [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) interface.</span></span>

    <span data-ttu-id="d5dc3-150">-或-</span><span class="sxs-lookup"><span data-stu-id="d5dc3-150">-or-</span></span>

    <span data-ttu-id="d5dc3-151">呼叫 [**IMFMediaSink：： GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) ，藉由指定資料流程號碼來取得資料流程接收。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-151">Call [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) to get the stream sink by specifying the stream number.</span></span> <span data-ttu-id="d5dc3-152">每個資料流程接收都會以您在設定檔中建立資料流程時所設定的資料流程號碼來識別。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-152">Each stream sink is identified with the stream number you set while creating the stream in the profile.</span></span>

<span data-ttu-id="d5dc3-153">如果您要建立部分拓撲來編碼媒體檔案，您必須將檔案接收以輸出拓撲節點的形式加入拓撲中。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-153">If you are building a partial topology for encoding a media file, you must add the file sink to the topology as an output topology node.</span></span> <span data-ttu-id="d5dc3-154">您可以藉由指定檔案接收中的每個流出接收，或是藉由設定「檔案接收」啟始物件和「串流接收器」識別碼，來進行這項操作。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-154">You can do so either by specifying each steam sink in the file sink or by setting the file sink activation object and the stream sink identifiers.</span></span> <span data-ttu-id="d5dc3-155">如需詳細資訊和程式碼範例，請參閱 [建立輸出節點](creating-output-nodes.md)。</span><span class="sxs-lookup"><span data-stu-id="d5dc3-155">For more information and code example, see [Creating Output Nodes](creating-output-nodes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5dc3-156">相關主題</span><span class="sxs-lookup"><span data-stu-id="d5dc3-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5dc3-157">ASF 媒體接收</span><span class="sxs-lookup"><span data-stu-id="d5dc3-157">ASF Media Sinks</span></span>](asf-media-sinks.md)
</dt> <dt>

[<span data-ttu-id="d5dc3-158">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="d5dc3-158">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



