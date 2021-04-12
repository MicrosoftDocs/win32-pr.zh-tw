---
description: 本主題說明如何使用來源讀取器來處理媒體資料。
ms.assetid: 583f5736-f767-47c5-8fdc-b3645aed59f6
title: 使用來源讀取器來處理媒體資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b19bce4d83298693825037aef92a220d78ed7c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321448"
---
# <a name="using-the-source-reader-to-process-media-data"></a><span data-ttu-id="f70b0-103">使用來源讀取器來處理媒體資料</span><span class="sxs-lookup"><span data-stu-id="f70b0-103">Using the Source Reader to Process Media Data</span></span>

<span data-ttu-id="f70b0-104">本主題說明如何使用 [來源讀取器](source-reader.md) 來處理媒體資料。</span><span class="sxs-lookup"><span data-stu-id="f70b0-104">This topic describes how to use the [Source Reader](source-reader.md) to process media data.</span></span>

<span data-ttu-id="f70b0-105">若要使用來源讀取器，請遵循下列基本步驟：</span><span class="sxs-lookup"><span data-stu-id="f70b0-105">To use the Source Reader, follow these basic steps:</span></span>

1.  <span data-ttu-id="f70b0-106">建立來源讀取器的實例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-106">Create an instance of the Source Reader.</span></span>
2.  <span data-ttu-id="f70b0-107">列舉可能的輸出格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-107">Enumerate the possible output formats.</span></span>
3.  <span data-ttu-id="f70b0-108">設定每個資料流程的實際輸出格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-108">Set the actual output format for each stream.</span></span>
4.  <span data-ttu-id="f70b0-109">處理來自來源的資料。</span><span class="sxs-lookup"><span data-stu-id="f70b0-109">Process data from the source.</span></span>

<span data-ttu-id="f70b0-110">本主題的其餘部分將詳細說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="f70b0-110">The remainder of this topic describes these steps in detail.</span></span>

-   [<span data-ttu-id="f70b0-111">建立來源讀取器</span><span class="sxs-lookup"><span data-stu-id="f70b0-111">Creating the Source Reader</span></span>](#creating-the-source-reader)
-   [<span data-ttu-id="f70b0-112">列舉輸出格式</span><span class="sxs-lookup"><span data-stu-id="f70b0-112">Enumerating Output Formats</span></span>](#enumerating-output-formats)
-   [<span data-ttu-id="f70b0-113">設定輸出格式</span><span class="sxs-lookup"><span data-stu-id="f70b0-113">Setting Output Formats</span></span>](#setting-output-formats)
-   [<span data-ttu-id="f70b0-114">處理媒體資料</span><span class="sxs-lookup"><span data-stu-id="f70b0-114">Processing Media Data</span></span>](#using-the-source-reader-to-process-media-data)
-   [<span data-ttu-id="f70b0-115">清空資料管線</span><span class="sxs-lookup"><span data-stu-id="f70b0-115">Draining the Data Pipeline</span></span>](#draining-the-data-pipeline)
-   [<span data-ttu-id="f70b0-116">取得檔案持續時間</span><span class="sxs-lookup"><span data-stu-id="f70b0-116">Getting the File Duration</span></span>](#getting-the-file-duration)
-   [<span data-ttu-id="f70b0-117">尋求</span><span class="sxs-lookup"><span data-stu-id="f70b0-117">Seeking</span></span>](#seeking)
-   [<span data-ttu-id="f70b0-118">播放速率</span><span class="sxs-lookup"><span data-stu-id="f70b0-118">Playback Rate</span></span>](#playback-rate)
-   [<span data-ttu-id="f70b0-119">硬體加速</span><span class="sxs-lookup"><span data-stu-id="f70b0-119">Hardware Acceleration</span></span>](#hardware-acceleration)
-   [<span data-ttu-id="f70b0-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="f70b0-120">Related topics</span></span>](#related-topics)

## <a name="creating-the-source-reader"></a><span data-ttu-id="f70b0-121">建立來源讀取器</span><span class="sxs-lookup"><span data-stu-id="f70b0-121">Creating the Source Reader</span></span>

<span data-ttu-id="f70b0-122">若要建立來源讀取器的實例，請呼叫下列其中一項功能：</span><span class="sxs-lookup"><span data-stu-id="f70b0-122">To create an instance of the Source Reader, call one of the following functions:</span></span>



| <span data-ttu-id="f70b0-123">函式</span><span class="sxs-lookup"><span data-stu-id="f70b0-123">Function</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="f70b0-124">描述</span><span class="sxs-lookup"><span data-stu-id="f70b0-124">Description</span></span>                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70b0-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span><span class="sxs-lookup"><span data-stu-id="f70b0-125"><span id="MFCreateSourceReaderFromURL"></span><span id="mfcreatesourcereaderfromurl"></span><span id="MFCREATESOURCEREADERFROMURL"></span>[**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)</span></span><br/>                                         | <span data-ttu-id="f70b0-126">使用 URL 做為輸入。</span><span class="sxs-lookup"><span data-stu-id="f70b0-126">Takes a URL as input.</span></span> <span data-ttu-id="f70b0-127">此函數會使用 [來源解析程式](source-resolver.md) ，從 URL 建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="f70b0-127">This function uses the [Source Resolver](source-resolver.md) to create a media source from the URL.</span></span><br/>                                                                       |
| <span data-ttu-id="f70b0-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span><span class="sxs-lookup"><span data-stu-id="f70b0-128"><span id="MFCreateSourceReaderFromByteStream"></span><span id="mfcreatesourcereaderfrombytestream"></span><span id="MFCREATESOURCEREADERFROMBYTESTREAM"></span>[**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)</span></span><br/>      | <span data-ttu-id="f70b0-129">取得位元組資料流程的指標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-129">Takes a pointer to a byte stream.</span></span> <span data-ttu-id="f70b0-130">此函數也會使用來源解析程式來建立媒體來源。</span><span class="sxs-lookup"><span data-stu-id="f70b0-130">This function also uses the Source Resolver to create the media source.</span></span><br/>                                                                                        |
| <span data-ttu-id="f70b0-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span><span class="sxs-lookup"><span data-stu-id="f70b0-131"><span id="MFCreateSourceReaderFromMediaSource"></span><span id="mfcreatesourcereaderfrommediasource"></span><span id="MFCREATESOURCEREADERFROMMEDIASOURCE"></span>[**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)</span></span><br/> | <span data-ttu-id="f70b0-132">使用已建立之媒體來源的指標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-132">Takes a pointer to a media source that has already been created.</span></span> <span data-ttu-id="f70b0-133">這項功能適用于來源解析程式無法建立的媒體來源，例如捕獲裝置或自訂媒體來源。</span><span class="sxs-lookup"><span data-stu-id="f70b0-133">This function is useful for media sources that the Source Resolver cannot create, such capture devices or custom media sources.</span></span><br/> |



 

<span data-ttu-id="f70b0-134">通常，針對媒體檔案，請使用 [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-134">Typically, for media files, use [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl).</span></span> <span data-ttu-id="f70b0-135">針對裝置（例如網路攝影機），請使用 [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-135">For devices, such as webcams, use [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource).</span></span> <span data-ttu-id="f70b0-136"> (需 Microsoft 媒體基礎中捕捉裝置的詳細資訊，請參閱 [音訊/影片捕獲](audio-video-capture.md)) 。</span><span class="sxs-lookup"><span data-stu-id="f70b0-136">(For more information about capture devices in Microsoft Media Foundation, see [Audio/Video Capture](audio-video-capture.md).)</span></span>

<span data-ttu-id="f70b0-137">這些函式中的每一個都採用選擇性的 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 指標，此指標可用來在來源讀取器上設定各種選項，如這些函式的參考主題所述。</span><span class="sxs-lookup"><span data-stu-id="f70b0-137">Each of these functions takes an optional [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer, which is used to set various options on the Source Reader, as described in the reference topics for these functions.</span></span> <span data-ttu-id="f70b0-138">若要取得預設行為，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-138">To get the default behavior, set this parameter to **NULL**.</span></span> <span data-ttu-id="f70b0-139">每個函式都會傳回 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 指標作為輸出參數。</span><span class="sxs-lookup"><span data-stu-id="f70b0-139">Each function returns an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer as an output parameter.</span></span> <span data-ttu-id="f70b0-140">在呼叫任何這些函式之前，您必須先呼叫 **CoInitialize (例如)** 和 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-140">You must call **CoInitialize(Ex)** and [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function before calling any of these functions.</span></span>

<span data-ttu-id="f70b0-141">下列程式碼會從 URL 建立來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="f70b0-141">The following code creates the Source Reader from a URL.</span></span>


```C++
int __cdecl wmain(int argc, __in_ecount(argc) PCWSTR* argv)
{
    if (argc < 2)
    {
        return 1;
    }

    const WCHAR *pszURL = argv[1];

    // Initialize the COM runtime.
    HRESULT hr = CoInitializeEx(0, COINIT_MULTITHREADED);
    if (SUCCEEDED(hr))
    {
        // Initialize the Media Foundation platform.
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            // Create the source reader.
            IMFSourceReader *pReader;
            hr = MFCreateSourceReaderFromURL(pszURL, NULL, &pReader);
            if (SUCCEEDED(hr))
            {
                ReadMediaFile(pReader);
                pReader->Release();
            }
            // Shut down Media Foundation.
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="enumerating-output-formats"></a><span data-ttu-id="f70b0-142">列舉輸出格式</span><span class="sxs-lookup"><span data-stu-id="f70b0-142">Enumerating Output Formats</span></span>

<span data-ttu-id="f70b0-143">每個媒體來源都至少有一個資料流程。</span><span class="sxs-lookup"><span data-stu-id="f70b0-143">Every media source has at least one stream.</span></span> <span data-ttu-id="f70b0-144">例如，影片檔案可能包含影片串流和音訊串流。</span><span class="sxs-lookup"><span data-stu-id="f70b0-144">For example, a video file might contain a video stream and an audio stream.</span></span> <span data-ttu-id="f70b0-145">每個資料流程的格式都會使用 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面所代表的媒體類型來描述。</span><span class="sxs-lookup"><span data-stu-id="f70b0-145">The format of each stream is described using a media type, represented by the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface.</span></span> <span data-ttu-id="f70b0-146">如需媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-146">For more information about media types, see [Media Types](media-types.md).</span></span> <span data-ttu-id="f70b0-147">您必須檢查媒體類型，以瞭解您從來源讀取器取得的資料格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-147">You must examine the media type to understand the format of the data that you get from the Source Reader.</span></span>

<span data-ttu-id="f70b0-148">一開始，每個資料流程都有預設格式，您可以藉由呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) 方法來找到此格式：</span><span class="sxs-lookup"><span data-stu-id="f70b0-148">Initially, every stream has a default format, which you can find by calling the [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) method:</span></span>

<span data-ttu-id="f70b0-149">針對每個資料流程，媒體來源會提供該資料流程可能的媒體類型清單。</span><span class="sxs-lookup"><span data-stu-id="f70b0-149">For each stream, the media source offers a list of possible media types for that stream.</span></span> <span data-ttu-id="f70b0-150">類型數目取決於來源。</span><span class="sxs-lookup"><span data-stu-id="f70b0-150">The number of types depends on the source.</span></span> <span data-ttu-id="f70b0-151">如果來源代表媒體檔案，則每個資料流程通常只有一種類型。</span><span class="sxs-lookup"><span data-stu-id="f70b0-151">If the source represents a media file, there is typically only one type per stream.</span></span> <span data-ttu-id="f70b0-152">另一方面，網路攝影機可能能夠以數種不同的格式串流影片。</span><span class="sxs-lookup"><span data-stu-id="f70b0-152">A webcam, on the other hand, might be able to stream video in several different formats.</span></span> <span data-ttu-id="f70b0-153">在此情況下，應用程式可以從媒體類型清單中選取要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-153">In that case, the application can select which format to use from the list of media types.</span></span>

<span data-ttu-id="f70b0-154">若要取得資料流程的其中一種媒體類型，請呼叫 [**IMFSourceReader：： GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="f70b0-154">To get one of the media types for a stream, call the [**IMFSourceReader::GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) method.</span></span> <span data-ttu-id="f70b0-155">這個方法會採用兩個索引參數：資料流程的索引，以及資料流程的媒體類型清單中的索引。</span><span class="sxs-lookup"><span data-stu-id="f70b0-155">This method takes two index parameters: The index of the stream, and an index into the list of media types for the stream.</span></span> <span data-ttu-id="f70b0-156">若要列舉資料流程的所有型別，請在保留資料流程索引常數時遞增清單索引。</span><span class="sxs-lookup"><span data-stu-id="f70b0-156">To enumerate all the types for a stream, increment the list index while keeping the stream index constant.</span></span> <span data-ttu-id="f70b0-157">當清單索引超出範圍時， **GetNativeMediaType** 會傳回 **MF \_ E \_ NO \_ 其他 \_ 類型**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-157">When the list index goes out of bounds, **GetNativeMediaType** returns **MF\_E\_NO\_MORE\_TYPES**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



<span data-ttu-id="f70b0-158">若要列舉每個資料流程的媒體類型，請遞增資料流程索引。</span><span class="sxs-lookup"><span data-stu-id="f70b0-158">To enumerate the media types for every stream, increment the stream index.</span></span> <span data-ttu-id="f70b0-159">當資料流程索引超出範圍時， [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) 會傳回 **MF \_ E \_ INVALIDSTREAMNUMBER**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-159">When the stream index goes out of bounds, [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype) returns **MF\_E\_INVALIDSTREAMNUMBER**.</span></span>


```C++
HRESULT EnumerateTypesForStream(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    HRESULT hr = S_OK;
    DWORD dwMediaTypeIndex = 0;

    while (SUCCEEDED(hr))
    {
        IMFMediaType *pType = NULL;
        hr = pReader->GetNativeMediaType(dwStreamIndex, dwMediaTypeIndex, &pType);
        if (hr == MF_E_NO_MORE_TYPES)
        {
            hr = S_OK;
            break;
        }
        else if (SUCCEEDED(hr))
        {
            // Examine the media type. (Not shown.)

            pType->Release();
        }
        ++dwMediaTypeIndex;
    }
    return hr;
}
```



## <a name="setting-output-formats"></a><span data-ttu-id="f70b0-160">設定輸出格式</span><span class="sxs-lookup"><span data-stu-id="f70b0-160">Setting Output Formats</span></span>

<span data-ttu-id="f70b0-161">若要變更輸出格式，請呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="f70b0-161">To change the output format, call the [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) method.</span></span> <span data-ttu-id="f70b0-162">這個方法會採用資料流程索引和媒體類型：</span><span class="sxs-lookup"><span data-stu-id="f70b0-162">This method takes the stream index and a media type:</span></span>

``` syntax
hr = pReader->SetCurrentMediaType(dwStreamIndex, pMediaType);
```

<span data-ttu-id="f70b0-163">針對媒體類型，它取決於您是否要插入解碼器。</span><span class="sxs-lookup"><span data-stu-id="f70b0-163">For the media type, it depends on whether you want to insert a decoder.</span></span>

-   <span data-ttu-id="f70b0-164">若要直接從來源取得資料，而不將其解碼，請使用 [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype)所傳回的其中一個類型。</span><span class="sxs-lookup"><span data-stu-id="f70b0-164">To get data directly from the source without decoding it, use one of the types returned by [**GetNativeMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getnativemediatype).</span></span>
-   <span data-ttu-id="f70b0-165">若要解碼資料流程，請建立新的媒體類型，以描述所需的未壓縮格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-165">To decode the stream, create a new media type that describes the desired uncompressed format.</span></span>

<span data-ttu-id="f70b0-166">在解碼器的案例中，建立媒體類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f70b0-166">In the case of the decoder, create the media type as follows:</span></span>

1.  <span data-ttu-id="f70b0-167">呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 來建立新的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="f70b0-167">Call [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create a new media type.</span></span>
2.  <span data-ttu-id="f70b0-168">將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為指定音訊或影片。</span><span class="sxs-lookup"><span data-stu-id="f70b0-168">Set the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to specify audio or video.</span></span>
3.  <span data-ttu-id="f70b0-169">設定 [ [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) ] 屬性，以指定解碼格式的子類型。</span><span class="sxs-lookup"><span data-stu-id="f70b0-169">Set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to specify the subtype of the decoding format.</span></span> <span data-ttu-id="f70b0-170"> (查看 [音訊子類型 guid](audio-subtype-guids.md) 和 [影片子類型 guid](video-subtype-guids.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="f70b0-170">(See [Audio Subtype GUIDs](audio-subtype-guids.md) and [Video Subtype GUIDs](video-subtype-guids.md).)</span></span>
4.  <span data-ttu-id="f70b0-171">呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-171">Call [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span>

<span data-ttu-id="f70b0-172">來源讀取器將會自動載入該解碼器。</span><span class="sxs-lookup"><span data-stu-id="f70b0-172">The Source Reader will automatically load the decoder.</span></span> <span data-ttu-id="f70b0-173">若要取得已解碼格式的完整詳細資料，請在呼叫 [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)之後呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype)</span><span class="sxs-lookup"><span data-stu-id="f70b0-173">To get the complete details of the decoded format, call [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) after the call to [**SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype)</span></span>

<span data-ttu-id="f70b0-174">下列程式碼會設定 RGB-32 的影片串流，以及 PCM 音訊的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="f70b0-174">The following code configures the video stream for RGB-32 and the audio stream for PCM audio.</span></span>


```C++
HRESULT ConfigureDecoder(IMFSourceReader *pReader, DWORD dwStreamIndex)
{
    IMFMediaType *pNativeType = NULL;
    IMFMediaType *pType = NULL;

    // Find the native format of the stream.
    HRESULT hr = pReader->GetNativeMediaType(dwStreamIndex, 0, &pNativeType);
    if (FAILED(hr))
    {
        return hr;
    }

    GUID majorType, subtype;

    // Find the major type.
    hr = pNativeType->GetGUID(MF_MT_MAJOR_TYPE, &majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Define the output type.
    hr = MFCreateMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pType->SetGUID(MF_MT_MAJOR_TYPE, majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Select a subtype.
    if (majorType == MFMediaType_Video)
    {
        subtype= MFVideoFormat_RGB32;
    }
    else if (majorType == MFMediaType_Audio)
    {
        subtype = MFAudioFormat_PCM;
    }
    else
    {
        // Unrecognized type. Skip.
        goto done;
    }

    hr = pType->SetGUID(MF_MT_SUBTYPE, subtype);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the uncompressed format.
    hr = pReader->SetCurrentMediaType(dwStreamIndex, NULL, pType);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pNativeType);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="processing-media-data"></a><span data-ttu-id="f70b0-175">處理媒體資料</span><span class="sxs-lookup"><span data-stu-id="f70b0-175">Processing Media Data</span></span>

<span data-ttu-id="f70b0-176">若要從來源取得媒體資料，請呼叫 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 方法，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="f70b0-176">To get media data from the source, call the [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method, as shown in the following code.</span></span>


```C++
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );
```



<span data-ttu-id="f70b0-177">第一個參數是您想要取得資料之資料流程的索引。</span><span class="sxs-lookup"><span data-stu-id="f70b0-177">The first parameter is the index of the stream for which you want to get data.</span></span> <span data-ttu-id="f70b0-178">您也可以指定 **MF \_ 來源 \_ 讀取器 \_ 任何 \_ 串流** ，以從任何串流取得下一個可用的資料。</span><span class="sxs-lookup"><span data-stu-id="f70b0-178">You can also specify **MF\_SOURCE\_READER\_ANY\_STREAM** to get the next available data from any stream.</span></span> <span data-ttu-id="f70b0-179">第二個參數包含選擇性旗標;如需這些的清單，請參閱 [**MF \_ 來源 \_ 讀取器 \_ 控制 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) 標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-179">The second parameter contains optional flags; see [**MF\_SOURCE\_READER\_CONTROL\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_control_flag) for a list of these.</span></span> <span data-ttu-id="f70b0-180">第三個參數會接收實際產生資料之資料流程的索引。</span><span class="sxs-lookup"><span data-stu-id="f70b0-180">The third parameter receives the index of the stream that actually produces the data.</span></span> <span data-ttu-id="f70b0-181">如果您將第一個參數設定為 **MF \_ 來源 \_ 讀取器 \_ 任何 \_ 資料流程**，您將需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="f70b0-181">You will need this information if you set the first parameter to **MF\_SOURCE\_READER\_ANY\_STREAM**.</span></span> <span data-ttu-id="f70b0-182">第四個參數會接收狀態旗標，指出讀取資料時可能發生的各種事件，例如資料流程中的格式變更。</span><span class="sxs-lookup"><span data-stu-id="f70b0-182">The fourth parameter receives status flags, indicating various events that can occur while reading the data, such as format changes in the stream.</span></span> <span data-ttu-id="f70b0-183">如需狀態旗標的清單，請參閱 [**MF \_ 來源 \_ 讀取器 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag)標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-183">For a list of status flags, see [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag).</span></span>

<span data-ttu-id="f70b0-184">如果媒體來源可以產生所要求資料流程的資料，則 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) 的最後一個參數會接收媒體範例物件的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-184">If the media source is able to produce data for the requested stream, the last parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface of a media sample object.</span></span> <span data-ttu-id="f70b0-185">使用媒體範例：</span><span class="sxs-lookup"><span data-stu-id="f70b0-185">Use the media sample to:</span></span>

-   <span data-ttu-id="f70b0-186">取得媒體資料的指標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-186">Get a pointer to the media data.</span></span>
-   <span data-ttu-id="f70b0-187">取得簡報時間和取樣持續時間。</span><span class="sxs-lookup"><span data-stu-id="f70b0-187">Get the presentation time and sample duration.</span></span>
-   <span data-ttu-id="f70b0-188">取得描述交錯、欄位支配和其他範例層面的屬性。</span><span class="sxs-lookup"><span data-stu-id="f70b0-188">Get attributes that describe interlacing, field dominance, and other aspects of the sample.</span></span>

<span data-ttu-id="f70b0-189">媒體資料的內容取決於資料流程的格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-189">The contents of the media data depend on the format of the stream.</span></span> <span data-ttu-id="f70b0-190">針對未壓縮的影片資料流程，每個媒體範例都包含單一的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="f70b0-190">For an uncompressed video stream, each media sample contains a single video frame.</span></span> <span data-ttu-id="f70b0-191">針對未壓縮的音訊串流，每個媒體範例都包含一連串的音訊畫面格。</span><span class="sxs-lookup"><span data-stu-id="f70b0-191">For an uncompressed audio stream, each media sample contains a sequence of audio frames.</span></span>

<span data-ttu-id="f70b0-192">[**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)方法可以傳回「 **\_ 確定**」，但不會傳回 *pSample* 參數中的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-192">The [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) method can return **S\_OK** and yet not return a media sample in the *pSample* parameter.</span></span> <span data-ttu-id="f70b0-193">例如，當您到達檔案結尾時， **ReadSample** 會在 *DwFlags* 中設定 **MF \_ 來源 \_ READERF \_ ENDOFSTREAM** 旗標，並將 *pSample* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-193">For example, when you reach the end of the file, **ReadSample** sets the **MF\_SOURCE\_READERF\_ENDOFSTREAM** flag in *dwFlags* and sets *pSample* to **NULL**.</span></span> <span data-ttu-id="f70b0-194">在此情況下， **ReadSample** 方法會傳回 S，因為未發生任何錯誤，即使 *pSample* 參數設定為 **Null** 也是一樣。 **\_**</span><span class="sxs-lookup"><span data-stu-id="f70b0-194">In this case, the **ReadSample** method returns **S\_OK** because no error has occurred, even though the *pSample* parameter is set to **NULL**.</span></span> <span data-ttu-id="f70b0-195">因此，請一律先檢查 *pSample* 的值，再進行取值。</span><span class="sxs-lookup"><span data-stu-id="f70b0-195">Therefore, always check the value of *pSample* before you dereference it.</span></span>

<span data-ttu-id="f70b0-196">下列程式碼示範如何在迴圈中呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，並檢查方法傳回的資訊，直到到達媒體檔案的結尾為止。</span><span class="sxs-lookup"><span data-stu-id="f70b0-196">The following code shows how to call [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) in a loop and check the information returned by the method, until the end of the media file is reached.</span></span>


```C++
HRESULT ProcessSamples(IMFSourceReader *pReader)
{
    HRESULT hr = S_OK;
    IMFSample *pSample = NULL;
    size_t  cSamples = 0;

    bool quit = false;
    while (!quit)
    {
        DWORD streamIndex, flags;
        LONGLONG llTimeStamp;

        hr = pReader->ReadSample(
            MF_SOURCE_READER_ANY_STREAM,    // Stream index.
            0,                              // Flags.
            &streamIndex,                   // Receives the actual stream index. 
            &flags,                         // Receives status flags.
            &llTimeStamp,                   // Receives the time stamp.
            &pSample                        // Receives the sample or NULL.
            );

        if (FAILED(hr))
        {
            break;
        }

        wprintf(L"Stream %d (%I64d)\n", streamIndex, llTimeStamp);
        if (flags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            wprintf(L"\tEnd of stream\n");
            quit = true;
        }
        if (flags & MF_SOURCE_READERF_NEWSTREAM)
        {
            wprintf(L"\tNew stream\n");
        }
        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            wprintf(L"\tNative type changed\n");
        }
        if (flags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            wprintf(L"\tCurrent type changed\n");
        }
        if (flags & MF_SOURCE_READERF_STREAMTICK)
        {
            wprintf(L"\tStream tick\n");
        }

        if (flags & MF_SOURCE_READERF_NATIVEMEDIATYPECHANGED)
        {
            // The format changed. Reconfigure the decoder.
            hr = ConfigureDecoder(pReader, streamIndex);
            if (FAILED(hr))
            {
                break;
            }
        }

        if (pSample)
        {
            ++cSamples;
        }

        SafeRelease(&pSample);
    }

    if (FAILED(hr))
    {
        wprintf(L"ProcessSamples FAILED, hr = 0x%x\n", hr);
    }
    else
    {
        wprintf(L"Processed %d samples\n", cSamples);
    }
    SafeRelease(&pSample);
    return hr;
}
```



## <a name="draining-the-data-pipeline"></a><span data-ttu-id="f70b0-197">清空資料管線</span><span class="sxs-lookup"><span data-stu-id="f70b0-197">Draining the Data Pipeline</span></span>

<span data-ttu-id="f70b0-198">在資料處理期間，解碼器或其他轉換可能會緩衝輸入範例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-198">During data processing, a decoder or other transform might buffer input samples.</span></span> <span data-ttu-id="f70b0-199">在下圖中，應用程式會呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，並接收表示時間等於 *t1* 的範例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-199">In the following diagram, the application calls [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) and receives a sample with a presentation time equal to *t1*.</span></span> <span data-ttu-id="f70b0-200">此解碼器持有 *t2* 和 *t3* 的範例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-200">The decoder is holding samples for *t2* and *t3*.</span></span>

![顯示在解碼器中緩衝的圖例。](images/sourcereader02.png)

<span data-ttu-id="f70b0-202">在下一次呼叫 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)時，來源讀取器可能會將 *t4* 提供給該解碼，並將 *t2* 傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-202">On the next call to [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample), the Source Reader might give *t4* to the decoder and return *t2* to the application.</span></span>

<span data-ttu-id="f70b0-203">如果您想要將目前在解碼器中緩衝處理的所有樣本解碼，而不將任何新的範例傳遞給該解碼器，請在 [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample)的 *dwControlFlags* 參數中設定 **MF \_ 來源 \_ 讀取器 \_ CONTROLF \_ 清空** 旗標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-203">If you want to decode all of the samples that are currently buffered in the decoder, without passing any new samples to the decoder, set the **MF\_SOURCE\_READER\_CONTROLF\_DRAIN** flag in the *dwControlFlags* parameter of [**ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample).</span></span> <span data-ttu-id="f70b0-204">繼續在迴圈中執行此動作，直到 **ReadSample** 傳回 **Null** 範例指標為止。</span><span class="sxs-lookup"><span data-stu-id="f70b0-204">Continue to do this in a loop until **ReadSample** returns a **NULL** sample pointer.</span></span> <span data-ttu-id="f70b0-205">視解碼器緩衝範例的方式而定，這可能會在 **ReadSample** 的數個呼叫之後立即發生。</span><span class="sxs-lookup"><span data-stu-id="f70b0-205">Depending on how the decoder buffers samples, that might happen immediately or after several calls to **ReadSample**.</span></span>

## <a name="getting-the-file-duration"></a><span data-ttu-id="f70b0-206">取得檔案持續時間</span><span class="sxs-lookup"><span data-stu-id="f70b0-206">Getting the File Duration</span></span>

<span data-ttu-id="f70b0-207">若要取得媒體檔案的持續時間，請呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) 方法，並要求 [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) 屬性，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="f70b0-207">To get the duration of a media file, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method and request the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute, as shown in the following code.</span></span>


```C++
HRESULT GetDuration(IMFSourceReader *pReader, LONGLONG *phnsDuration)
{
    PROPVARIANT var;
    HRESULT hr = pReader->GetPresentationAttribute(MF_SOURCE_READER_MEDIASOURCE, 
        MF_PD_DURATION, &var);
    if (SUCCEEDED(hr))
    {
        hr = PropVariantToInt64(var, phnsDuration);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="f70b0-208">此處顯示的函式會取得 100-毫微秒單位的持續時間。</span><span class="sxs-lookup"><span data-stu-id="f70b0-208">The function shown here gets the duration in 100-nanosecond units.</span></span> <span data-ttu-id="f70b0-209">除以10000000以取得持續時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f70b0-209">Divide by 10,000,000 to get the duration in seconds.</span></span>

## <a name="seeking"></a><span data-ttu-id="f70b0-210">尋求</span><span class="sxs-lookup"><span data-stu-id="f70b0-210">Seeking</span></span>

<span data-ttu-id="f70b0-211">從本機檔案取得資料的媒體來源通常可以搜尋檔案中的任意位置。</span><span class="sxs-lookup"><span data-stu-id="f70b0-211">A media source that gets data from a local file can usually seek to arbitrary positions in the file.</span></span> <span data-ttu-id="f70b0-212">捕捉設備（例如網路攝影機）通常無法搜尋，因為資料是即時的。</span><span class="sxs-lookup"><span data-stu-id="f70b0-212">Capture devices such as webcams generally cannot seek, because the data is live.</span></span> <span data-ttu-id="f70b0-213">根據網路串流通訊協定，在網路上串流資料的來源可能可以搜尋。</span><span class="sxs-lookup"><span data-stu-id="f70b0-213">A source that streams data over a network might be able to seek, depending on the network streaming protocol.</span></span>

<span data-ttu-id="f70b0-214">若要找出媒體來源是否可以搜尋，請呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) ，並要求 [ [MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ 特性](mf-source-reader-mediasource-characteristics.md) ] 屬性，如下列程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="f70b0-214">To find out whether a media source can seek, call [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) and request the [MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS](mf-source-reader-mediasource-characteristics.md) attribute, as shown in the following code:</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



<span data-ttu-id="f70b0-215">此函數會從來源取得一組功能旗標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-215">This function gets a set of capabilities flags from the source.</span></span> <span data-ttu-id="f70b0-216">這些旗標定義于 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) 列舉中。</span><span class="sxs-lookup"><span data-stu-id="f70b0-216">These flags are defined in the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span> <span data-ttu-id="f70b0-217">與搜尋相關的兩個旗標：</span><span class="sxs-lookup"><span data-stu-id="f70b0-217">Two flags relate to seeking:</span></span>



| <span data-ttu-id="f70b0-218">旗標</span><span class="sxs-lookup"><span data-stu-id="f70b0-218">Flag</span></span>                                                                                                                                      | <span data-ttu-id="f70b0-219">描述</span><span class="sxs-lookup"><span data-stu-id="f70b0-219">Description</span></span>                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70b0-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE \_ 可以 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="f70b0-220"><span id="MFMEDIASOURCE_CAN_SEEK"></span><span id="mfmediasource_can_seek"></span>**MFMEDIASOURCE\_CAN\_SEEK**</span></span><br/>                 | <span data-ttu-id="f70b0-221">來源可以搜尋。</span><span class="sxs-lookup"><span data-stu-id="f70b0-221">The source can seek.</span></span><br/>                                                                                                                                                                            |
| <span data-ttu-id="f70b0-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE \_ 有 \_ 緩慢的 \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="f70b0-222"><span id="MFMEDIASOURCE_HAS_SLOW_SEEK"></span><span id="mfmediasource_has_slow_seek"></span>**MFMEDIASOURCE\_HAS\_SLOW\_SEEK**</span></span><br/> | <span data-ttu-id="f70b0-223">搜尋可能需要很長的時間才能完成。</span><span class="sxs-lookup"><span data-stu-id="f70b0-223">Seeking might take a long time to complete.</span></span> <span data-ttu-id="f70b0-224">例如，來源可能需要先下載整個檔案，才能進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="f70b0-224">For example, the source might need to download the entire file before it can seek.</span></span> <span data-ttu-id="f70b0-225"> (沒有任何嚴格準則可讓來源傳回此旗標。 ) </span><span class="sxs-lookup"><span data-stu-id="f70b0-225">(There are no strict criteria for a source to return this flag.)</span></span><br/> |



 

<span data-ttu-id="f70b0-226">下列程式碼 **會測試 MFMEDIASOURCE \_ 可以 \_ 搜尋** 旗標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-226">The following code tests for the **MFMEDIASOURCE\_CAN\_SEEK** flag.</span></span>


```C++
BOOL SourceCanSeek(IMFSourceReader *pReader)
{
    BOOL bCanSeek = FALSE;
    ULONG flags;
    if (SUCCEEDED(GetSourceFlags(pReader, &flags)))
    {
        bCanSeek = ((flags & MFMEDIASOURCE_CAN_SEEK) == MFMEDIASOURCE_CAN_SEEK);
    }
    return bCanSeek;
}
```



<span data-ttu-id="f70b0-227">若要搜尋，請呼叫 [**IMFSourceReader：： SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) 方法，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="f70b0-227">To seek, call the [**IMFSourceReader::SetCurrentPosition**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentposition) method, as shown in the following code.</span></span>


```C++
HRESULT SetPosition(IMFSourceReader *pReader, const LONGLONG& hnsPosition)
{
    PROPVARIANT var;
    HRESULT hr = InitPropVariantFromInt64(hnsPosition, &var);
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentPosition(GUID_NULL, var);
        PropVariantClear(&var);
    }
    return hr;
}
```



<span data-ttu-id="f70b0-228">第一個參數會提供您用來指定搜尋位置的時間格式。</span><span class="sxs-lookup"><span data-stu-id="f70b0-228">The first parameter gives the time format that you are using to specify the seek position.</span></span> <span data-ttu-id="f70b0-229">媒體基礎中的所有媒體來源都必須支援 100-納秒的單位，由值 **GUID \_ Null** 表示。</span><span class="sxs-lookup"><span data-stu-id="f70b0-229">All media sources in Media Foundation are required to support 100-nanosecond units, indicated by the value **GUID\_NULL**.</span></span> <span data-ttu-id="f70b0-230">第二個參數是包含搜尋位置的 **PROPVARIANT** 。</span><span class="sxs-lookup"><span data-stu-id="f70b0-230">The second parameter is a **PROPVARIANT** that contains the seek position.</span></span> <span data-ttu-id="f70b0-231">若為 100-納秒的時間單位，資料類型為 **LONGLONG**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-231">For 100-nanosecond time units, the data type is **LONGLONG**.</span></span>

<span data-ttu-id="f70b0-232">請注意，並非每個媒體來源都提供框架精確的搜尋。</span><span class="sxs-lookup"><span data-stu-id="f70b0-232">Be aware that not every media source provides frame-accurate seeking.</span></span> <span data-ttu-id="f70b0-233">搜尋的精確度取決於數個因素，例如主要畫面格間隔、媒體檔案是否包含索引，以及資料是否具有固定或變數位元速率。</span><span class="sxs-lookup"><span data-stu-id="f70b0-233">The accuracy of seeking depends on several factors, such as the key frame interval, whether the media file contains an index, and whether the data has a constant or variable bit rate.</span></span> <span data-ttu-id="f70b0-234">因此，在您搜尋檔案中的位置之後，就無法保證下一個範例中的時間戳記會完全符合要求的位置。</span><span class="sxs-lookup"><span data-stu-id="f70b0-234">Therefore, after you seek to a position in a file, there is no guarantee that the time stamp on the next sample will exactly match the requested position.</span></span> <span data-ttu-id="f70b0-235">一般來說，實際的位置不會晚于要求的位置，因此您可以捨棄樣本，直到到達資料流程中的所需點為止。</span><span class="sxs-lookup"><span data-stu-id="f70b0-235">Generally, the actual position will not be later than the requested position, so you can discard samples until you reach the desired point in the stream.</span></span>

## <a name="playback-rate"></a><span data-ttu-id="f70b0-236">播放速率</span><span class="sxs-lookup"><span data-stu-id="f70b0-236">Playback Rate</span></span>

<span data-ttu-id="f70b0-237">雖然您可以使用來源讀取器來設定播放速率，但這通常不太實用，原因如下：</span><span class="sxs-lookup"><span data-stu-id="f70b0-237">Although you can set the playback rate using the Source Reader, doing is typically not very useful, for the following reasons:</span></span>

-   <span data-ttu-id="f70b0-238">來源讀取器不支援反向播放，即使媒體來源確實如此。</span><span class="sxs-lookup"><span data-stu-id="f70b0-238">The Source Reader does not support reverse playback, even if the media source does.</span></span>
-   <span data-ttu-id="f70b0-239">應用程式會控制呈現時間，讓應用程式可以在不設定來源的速率的情況下，執行快速或緩慢的播放。</span><span class="sxs-lookup"><span data-stu-id="f70b0-239">The application controls the presentation times, so the application can implement fast or slow play without setting the rate on the source.</span></span>
-   <span data-ttu-id="f70b0-240">有些媒體來源支援 *thinning* 模式，其中來源提供較少的樣本，通常只是主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="f70b0-240">Some media sources support *thinning* mode, where the source delivers fewer samples—typically just the key frames.</span></span> <span data-ttu-id="f70b0-241">但是，如果您想要卸載非主要畫面格，您可以檢查每個範例中的 [MFSampleExtension \_ CleanPoint](mfsampleextension-cleanpoint-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f70b0-241">However, if you want to drop non-key frames, you can check each sample for the [MFSampleExtension\_CleanPoint](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>

<span data-ttu-id="f70b0-242">若要使用來源讀取器設定播放速率，請呼叫 [**IMFSourceReader：： GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) 方法，以從媒體來源取得 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) 和 [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 介面。</span><span class="sxs-lookup"><span data-stu-id="f70b0-242">To set the playback rate using the Source Reader, call the [**IMFSourceReader::GetServiceForStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getserviceforstream) method to get the [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) and [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interfaces from the media source.</span></span>

## <a name="hardware-acceleration"></a><span data-ttu-id="f70b0-243">硬體加速</span><span class="sxs-lookup"><span data-stu-id="f70b0-243">Hardware Acceleration</span></span>

<span data-ttu-id="f70b0-244">來源讀取器相容于 Microsoft DirectX Video 加速 (DXVA) 2.0 進行硬體加速影片解碼。</span><span class="sxs-lookup"><span data-stu-id="f70b0-244">The Source Reader is compatible with Microsoft DirectX Video Acceleration (DXVA) 2.0 for hardware accelerated video decoding.</span></span> <span data-ttu-id="f70b0-245">若要搭配使用 DXVA 與來源讀取器，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="f70b0-245">To use DXVA with the Source Reader, perform the following steps.</span></span>

1.  <span data-ttu-id="f70b0-246">建立 Microsoft Direct3D 裝置。</span><span class="sxs-lookup"><span data-stu-id="f70b0-246">Create a Microsoft Direct3D device.</span></span>
2.  <span data-ttu-id="f70b0-247">呼叫 [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) 函式來建立 Direct3D 裝置管理員。</span><span class="sxs-lookup"><span data-stu-id="f70b0-247">Call the [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9) function to create the Direct3D device manager.</span></span> <span data-ttu-id="f70b0-248">此函式會取得 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="f70b0-248">This function gets a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span>
3.  <span data-ttu-id="f70b0-249">使用 Direct3D 裝置的指標來呼叫 [**IDirect3DDeviceManager9：： ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) 方法。</span><span class="sxs-lookup"><span data-stu-id="f70b0-249">Call the [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method with a pointer to the Direct3D device.</span></span>
4.  <span data-ttu-id="f70b0-250">藉由呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 函數來建立屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="f70b0-250">Create an attribute store by calling the [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) function.</span></span>
5.  <span data-ttu-id="f70b0-251">建立來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="f70b0-251">Create the Source Reader.</span></span> <span data-ttu-id="f70b0-252">在建立函數的 *pAttributes* 參數中傳遞屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="f70b0-252">Pass the attribute store in the *pAttributes* parameter of the creation function.</span></span>

<span data-ttu-id="f70b0-253">當您提供 Direct3D 裝置時，來源讀取器會配置與 DXVA video 處理器 API 相容的影片範例。</span><span class="sxs-lookup"><span data-stu-id="f70b0-253">When you provide a Direct3D device, the Source Reader allocates video samples that are compatible with the DXVA video processor API.</span></span> <span data-ttu-id="f70b0-254">您可以使用 DXVA 影片處理來執行硬體去交錯或視頻混合。</span><span class="sxs-lookup"><span data-stu-id="f70b0-254">You can use DXVA video processing to perform hardware deinterlacing or video mixing.</span></span> <span data-ttu-id="f70b0-255">如需詳細資訊，請參閱 [DXVA 影片處理](dxva-video-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-255">For more information, see [DXVA Video Processing](dxva-video-processing.md).</span></span> <span data-ttu-id="f70b0-256">此外，如果此解碼器支援 DXVA 2.0，則會使用 Direct3D 裝置來執行硬體加速解碼。</span><span class="sxs-lookup"><span data-stu-id="f70b0-256">Also, if the decoder supports DXVA 2.0, it will use the Direct3D device to perform hardware-accelerated decoding.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f70b0-257">從 Windows 8 開始，可以使用 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) ，而不是 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-257">Beginning in Windows 8, [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) can be used instead of the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9).</span></span> <span data-ttu-id="f70b0-258">針對 Windows Store 應用程式，您必須使用 **IMFDXGIDeviceManager**。</span><span class="sxs-lookup"><span data-stu-id="f70b0-258">For Windows Store apps, you must use **IMFDXGIDeviceManager**.</span></span> <span data-ttu-id="f70b0-259">如需詳細資訊，請參閱 [Direct3D 11 影片 api](direct3d-11-video-apis.md)。</span><span class="sxs-lookup"><span data-stu-id="f70b0-259">For more info, see the [Direct3D 11 Video APIs](direct3d-11-video-apis.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f70b0-260">相關主題</span><span class="sxs-lookup"><span data-stu-id="f70b0-260">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f70b0-261">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="f70b0-261">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




