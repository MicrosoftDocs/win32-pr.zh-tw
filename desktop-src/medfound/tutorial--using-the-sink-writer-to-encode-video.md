---
description: 本教學課程使用接收寫入器來編碼影片檔案。
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 教學課程：使用接收寫入器編碼影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983562"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a><span data-ttu-id="18926-103">教學課程：使用接收寫入器編碼影片</span><span class="sxs-lookup"><span data-stu-id="18926-103">Tutorial: Using the Sink Writer to Encode Video</span></span>

<span data-ttu-id="18926-104">本教學課程使用 [接收寫入器](sink-writer.md) 來編碼影片檔案。</span><span class="sxs-lookup"><span data-stu-id="18926-104">This tutorial uses the [Sink Writer](sink-writer.md) to encode a video file.</span></span>

## <a name="define-the-video-format"></a><span data-ttu-id="18926-105">定義影片格式</span><span class="sxs-lookup"><span data-stu-id="18926-105">Define the Video Format</span></span>

<span data-ttu-id="18926-106">為了簡單起見，本教學課程使用固定的影片格式，由下列常數所定義：</span><span class="sxs-lookup"><span data-stu-id="18926-106">For simplicity, this tutorial uses a fixed video format, defined by the following constants:</span></span>


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



<span data-ttu-id="18926-107">這些常數會指定下列影片格式的參數：</span><span class="sxs-lookup"><span data-stu-id="18926-107">These constants specify the following parameters of the video format:</span></span>

-   <span data-ttu-id="18926-108">框架大小 (寬度和高度) </span><span class="sxs-lookup"><span data-stu-id="18926-108">Frame size (width and height)</span></span>
-   <span data-ttu-id="18926-109">每秒畫面數。</span><span class="sxs-lookup"><span data-stu-id="18926-109">Frames per second.</span></span>
-   <span data-ttu-id="18926-110">編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="18926-110">Encoded bit rate.</span></span>
-   <span data-ttu-id="18926-111">編碼格式，也就是 Windows Media 視訊 9 (**MFVideoFormat \_ WMV3**) 。</span><span class="sxs-lookup"><span data-stu-id="18926-111">Encoding format, which is Windows Media Video 9 (**MFVideoFormat\_WMV3**).</span></span>
-   <span data-ttu-id="18926-112">輸入格式，也就是32位 RGB。</span><span class="sxs-lookup"><span data-stu-id="18926-112">Input format, which is 32-bit RGB.</span></span>
-   <span data-ttu-id="18926-113">輸出檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="18926-113">Duration of the output file.</span></span>

<span data-ttu-id="18926-114">程式會使用這些常數來建立描述格式的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="18926-114">The program uses these constants to create the media types that describe the format.</span></span> <span data-ttu-id="18926-115">在實際的應用程式中，您通常會支援一系列的編碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="18926-115">In a real application, you would typically support a range of encoding profiles.</span></span>

## <a name="create-an-uncompressed-video-frame"></a><span data-ttu-id="18926-116">建立未壓縮的影片畫面</span><span class="sxs-lookup"><span data-stu-id="18926-116">Create an Uncompressed Video Frame</span></span>

<span data-ttu-id="18926-117">此外，為了簡單起見，本教學課程會使用靜態影片框架做為輸入。</span><span class="sxs-lookup"><span data-stu-id="18926-117">Also for simplicity, this tutorial uses a static video frame as input.</span></span> <span data-ttu-id="18926-118">影片框架包含一個穩固的綠色矩形，並以程式設計方式產生。</span><span class="sxs-lookup"><span data-stu-id="18926-118">The video frame contains a solid green rectangle and is generated programmatically.</span></span> <span data-ttu-id="18926-119">影片畫面會儲存在全域變數中，做為 **DWORD** s 的陣列：</span><span class="sxs-lookup"><span data-stu-id="18926-119">The video frame is stored in a global variable as an array of **DWORD** s:</span></span>


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



<span data-ttu-id="18926-120">下列程式碼會將框架中的每個圖元設定為綠色：</span><span class="sxs-lookup"><span data-stu-id="18926-120">The following code sets every pixel in the frame to green:</span></span>


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a><span data-ttu-id="18926-121">初始化接收寫入器</span><span class="sxs-lookup"><span data-stu-id="18926-121">Initialize the Sink Writer</span></span>

<span data-ttu-id="18926-122">若要初始化接收寫入器，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="18926-122">To initialize the sink writer, perform the following steps.</span></span>

1.  <span data-ttu-id="18926-123">呼叫 [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) 來建立接收寫入器的新實例。</span><span class="sxs-lookup"><span data-stu-id="18926-123">Call [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) to create a new instance of the sink writer.</span></span>
2.  <span data-ttu-id="18926-124">建立描述編碼影片的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="18926-124">Create a media type that describes the encoded video.</span></span>
3.  <span data-ttu-id="18926-125">將此媒體類型傳遞給 [**IMFSinkWriter：： AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) 方法。</span><span class="sxs-lookup"><span data-stu-id="18926-125">Pass this media type to the [**IMFSinkWriter::AddStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream) method.</span></span>
4.  <span data-ttu-id="18926-126">建立第二種媒體類型來描述未壓縮的輸入。</span><span class="sxs-lookup"><span data-stu-id="18926-126">Create a second media type that describes the uncompressed input.</span></span>
5.  <span data-ttu-id="18926-127">將未壓縮的媒體類型傳遞給 [**IMFSinkWriter：： SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) 方法。</span><span class="sxs-lookup"><span data-stu-id="18926-127">Pass the uncompressed media type to the [**IMFSinkWriter::SetInputMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype) method.</span></span>
6.  <span data-ttu-id="18926-128">呼叫 [**IMFSinkWriter：： BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) 方法。</span><span class="sxs-lookup"><span data-stu-id="18926-128">Call the [**IMFSinkWriter::BeginWriting**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting) method.</span></span>
7.  <span data-ttu-id="18926-129">接收寫入器現在已準備好接受輸入範例。</span><span class="sxs-lookup"><span data-stu-id="18926-129">The sink writer is now ready to accept input samples.</span></span>

<span data-ttu-id="18926-130">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="18926-130">The following code shows these steps.</span></span>


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



<span data-ttu-id="18926-131">先前程式碼範例中的大部分步驟是設定這兩種媒體類型的媒體類型屬性。</span><span class="sxs-lookup"><span data-stu-id="18926-131">Most of the steps in previous code example are setting the media type attributes for the two media types.</span></span> <span data-ttu-id="18926-132">媒體類型的詳細資料將視您的來源內容和所需的編碼設定檔而定。</span><span class="sxs-lookup"><span data-stu-id="18926-132">The details of the media types will depend on your source content and the desired encoding profile.</span></span>

## <a name="send-video-frames-to-the-sink-writer"></a><span data-ttu-id="18926-133">將影片框架傳送至接收寫入器</span><span class="sxs-lookup"><span data-stu-id="18926-133">Send Video Frames to the Sink Writer</span></span>

<span data-ttu-id="18926-134">若要將影片框架傳送至接收寫入器，請呼叫 [**IMFSinkWriter：： WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) 方法。</span><span class="sxs-lookup"><span data-stu-id="18926-134">To send a video frame to the sink writer, call the [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method.</span></span> <span data-ttu-id="18926-135">**WriteSample** 方法會使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)介面的指標，該介面表示 *媒體範例* 物件。</span><span class="sxs-lookup"><span data-stu-id="18926-135">The **WriteSample** method takes a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which represents a *media sample* object.</span></span> <span data-ttu-id="18926-136">媒體範例包含 *媒體緩衝區* 物件，該物件接著會包含影片畫面的指標。</span><span class="sxs-lookup"><span data-stu-id="18926-136">The media sample contains a *media buffer* object, which in turn contains a pointer to the video frame.</span></span> <span data-ttu-id="18926-137">如需媒體範例和緩衝區的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="18926-137">For more information about media samples and buffer, see the following topics.</span></span>

-   [<span data-ttu-id="18926-138">媒體範例</span><span class="sxs-lookup"><span data-stu-id="18926-138">Media Samples</span></span>](media-samples.md)
-   [<span data-ttu-id="18926-139">媒體緩衝區</span><span class="sxs-lookup"><span data-stu-id="18926-139">Media Buffers</span></span>](media-buffers.md)

<span data-ttu-id="18926-140">視您的應用程式而定，您可能會從 [來源讀取器](source-reader.md)取得媒體範例。</span><span class="sxs-lookup"><span data-stu-id="18926-140">Depending on your application, you might get the media samples from the [Source Reader](source-reader.md).</span></span> <span data-ttu-id="18926-141">或者，您也可以建立媒體範例，並直接操作緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="18926-141">Alternatively, you can create the media samples and directly manipulate the data in the buffer.</span></span> <span data-ttu-id="18926-142">下列程式碼顯示第二個方法。</span><span class="sxs-lookup"><span data-stu-id="18926-142">The following code shows the second approach.</span></span> <span data-ttu-id="18926-143">它會建立記憶體緩衝區，並將單一影片框架寫入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18926-143">It creates a memory buffer and writes a single video frame to the buffer.</span></span> <span data-ttu-id="18926-144">然後，它會將該緩衝區新增至媒體範例，並將媒體範例傳送至接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="18926-144">Then it adds that buffer to a media sample, and sends the media sample to the sink writer.</span></span>


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="18926-145">此程式碼會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="18926-145">This code performs the following steps.</span></span>

1.  <span data-ttu-id="18926-146">呼叫 [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) 來建立媒體緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="18926-146">Call [**MFCreateMemoryBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) to create a media buffer object.</span></span> <span data-ttu-id="18926-147">此函數會配置緩衝區的記憶體。</span><span class="sxs-lookup"><span data-stu-id="18926-147">This function allocates the memory for the buffer.</span></span>
2.  <span data-ttu-id="18926-148">呼叫 [**IMFMediaBuffer：： lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 來鎖定緩衝區，並取得記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="18926-148">Call [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to lock the buffer and get a pointer to the memory.</span></span>
3.  <span data-ttu-id="18926-149">呼叫 [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) 將影片框架複製到緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18926-149">Call [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) to copy the video frame into the buffer.</span></span>
    > [!Note]  
    > <span data-ttu-id="18926-150">在此特定範例中，使用 **memcpy** 也會正常運作。</span><span class="sxs-lookup"><span data-stu-id="18926-150">In this particular example, using **memcpy** would work just as well.</span></span> <span data-ttu-id="18926-151">不過， [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) 函式會正確處理來源影像的 stride 與目標緩衝區不符的情況。</span><span class="sxs-lookup"><span data-stu-id="18926-151">However, the [**MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) function correctly handles the case where the stride of the source image does not match the target buffer.</span></span> <span data-ttu-id="18926-152">如需詳細資訊，請參閱 [影像 Stride](image-stride.md)。</span><span class="sxs-lookup"><span data-stu-id="18926-152">For more information, see [Image Stride](image-stride.md).</span></span>

     

4.  <span data-ttu-id="18926-153">呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區。</span><span class="sxs-lookup"><span data-stu-id="18926-153">Call [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer.</span></span>
5.  <span data-ttu-id="18926-154">呼叫 [**IMFMediaBuffer：： SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) ，以更新緩衝區中有效資料的長度。</span><span class="sxs-lookup"><span data-stu-id="18926-154">Call [**IMFMediaBuffer::SetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) to update the length of the valid data in the buffer.</span></span> <span data-ttu-id="18926-155"> (否則，此值會預設為零。 ) </span><span class="sxs-lookup"><span data-stu-id="18926-155">(Otherwise, this value defaults to zero.)</span></span>
6.  <span data-ttu-id="18926-156">呼叫 [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) 來建立媒體範例物件。</span><span class="sxs-lookup"><span data-stu-id="18926-156">Call [**MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) to create a media sample object.</span></span>
7.  <span data-ttu-id="18926-157">呼叫 [**IMFSample：： AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) ，將媒體緩衝區新增至媒體範例。</span><span class="sxs-lookup"><span data-stu-id="18926-157">Call [**IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) to add the media buffer to the media sample.</span></span>
8.  <span data-ttu-id="18926-158">呼叫 [**IMFSample：： SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) 來設定影片框架的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="18926-158">Call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) to set the time stamp for the video frame.</span></span>
9.  <span data-ttu-id="18926-159">呼叫 [**IMFSample：： SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) 來設定影片框架的持續時間。</span><span class="sxs-lookup"><span data-stu-id="18926-159">Call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) to set the duration of the video frame.</span></span>
10. <span data-ttu-id="18926-160">呼叫 [**IMFSinkWriter：： WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) ，將媒體範例傳送至接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="18926-160">Call [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) to send the media sample to the sink writer.</span></span>

## <a name="write-the-main-function"></a><span data-ttu-id="18926-161">撰寫 main 函數</span><span class="sxs-lookup"><span data-stu-id="18926-161">Write the main Function</span></span>

<span data-ttu-id="18926-162">在 `main` 函數中，執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="18926-162">Inside the `main` function, perform the following steps.</span></span>

1.  <span data-ttu-id="18926-163">呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="18926-163">Call [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="18926-164">呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 以初始化 Microsoft 媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="18926-164">Call [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize Microsoft Media Foundation.</span></span>
3.  <span data-ttu-id="18926-165">建立接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="18926-165">Create the sink writer.</span></span>
4.  <span data-ttu-id="18926-166">將影片框架傳送至接收寫入器。</span><span class="sxs-lookup"><span data-stu-id="18926-166">Send video frames to the sink writer.</span></span>
5.  <span data-ttu-id="18926-167">呼叫 [**IMFSinkWriter：： finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) 完成輸出檔。</span><span class="sxs-lookup"><span data-stu-id="18926-167">Call [**IMFSinkWriter::Finalize**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) to finalize the output file.</span></span>
6.  <span data-ttu-id="18926-168">釋放接收寫入器的指標。</span><span class="sxs-lookup"><span data-stu-id="18926-168">Release the pointer to the sink writer.</span></span>
7.  <span data-ttu-id="18926-169">呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。</span><span class="sxs-lookup"><span data-stu-id="18926-169">Call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>
8.  <span data-ttu-id="18926-170">呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)。</span><span class="sxs-lookup"><span data-stu-id="18926-170">Call [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a><span data-ttu-id="18926-171">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="18926-171">Example Code</span></span>

<span data-ttu-id="18926-172">下列程式碼顯示完整的程式。</span><span class="sxs-lookup"><span data-stu-id="18926-172">The following code shows the complete program.</span></span>


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="18926-173">相關主題</span><span class="sxs-lookup"><span data-stu-id="18926-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18926-174">接收寫入器</span><span class="sxs-lookup"><span data-stu-id="18926-174">Sink Writer</span></span>](sink-writer.md)
</dt> </dl>

 

 
