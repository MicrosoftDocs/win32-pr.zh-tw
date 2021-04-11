---
description: 步驟3會執行 Frame-Grabbing 函式
ms.assetid: 4ec2e4a4-3ab0-45f1-b29a-313599fe9e7d
title: 步驟3會執行 Frame-Grabbing 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97f585ff365e40ec611a9e11ce365839aa87be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850972"
---
# <a name="step-3-implement-the-frame-grabbing-function"></a><span data-ttu-id="dd65f-103">步驟3：執行 Frame-Grabbing 函式</span><span class="sxs-lookup"><span data-stu-id="dd65f-103">Step 3: Implement the Frame-Grabbing Function</span></span>

<span data-ttu-id="dd65f-104">\[此 API 不受支援，而且可能會在未來變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="dd65f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="dd65f-105">本主題是 [抓取海報框架](grabbing-a-poster-frame.md)的步驟3。</span><span class="sxs-lookup"><span data-stu-id="dd65f-105">This topic is Step 3 of [Grabbing a Poster Frame](grabbing-a-poster-frame.md).</span></span>

<span data-ttu-id="dd65f-106">下一步是執行 GetBitmap 函式，此函式會使用媒體偵測器來抓取海報框架。</span><span class="sxs-lookup"><span data-stu-id="dd65f-106">The next step is to implement the GetBitmap function, which uses the Media Detector to grab a poster frame.</span></span> <span data-ttu-id="dd65f-107">在此函數中，執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="dd65f-107">Inside this function, perform the following steps:</span></span>

1.  <span data-ttu-id="dd65f-108">建立媒體偵測器。</span><span class="sxs-lookup"><span data-stu-id="dd65f-108">Create the Media Detector.</span></span>
2.  <span data-ttu-id="dd65f-109">指定媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="dd65f-109">Specify a media file.</span></span>
3.  <span data-ttu-id="dd65f-110">檢查檔案中的每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="dd65f-110">Examine each stream in the file.</span></span> <span data-ttu-id="dd65f-111">如果是影片串流，請取得影片的原生維度。</span><span class="sxs-lookup"><span data-stu-id="dd65f-111">If it is a video stream, get the native dimensions of the video.</span></span>
4.  <span data-ttu-id="dd65f-112">取得海報框架，並指定搜尋時間和目標維度。</span><span class="sxs-lookup"><span data-stu-id="dd65f-112">Obtain a poster frame, specifying the seek time and the target dimension.</span></span>

<span data-ttu-id="dd65f-113">藉由呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)來建立媒體偵測器物件：</span><span class="sxs-lookup"><span data-stu-id="dd65f-113">Create the Media Detector object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance):</span></span>


```C++
CComPtr<IMediaDet> pDet;
hr = pDet.CoCreateInstance(__uuidof(MediaDet));
```



<span data-ttu-id="dd65f-114">使用 [**IMediaDet：:p 內容 \_ 名稱方法**](imediadet-put-filename.md) 指定檔案名。</span><span class="sxs-lookup"><span data-stu-id="dd65f-114">Specify a file name, using the [**IMediaDet::put\_Filename**](imediadet-put-filename.md) method.</span></span> <span data-ttu-id="dd65f-115">這個方法會採用 **BSTR** 參數。</span><span class="sxs-lookup"><span data-stu-id="dd65f-115">This method takes a **BSTR** parameter.</span></span>


```C++
hr = pDet->put_Filename(bstrFilename);
```



<span data-ttu-id="dd65f-116">取得資料流程的數目，並對每個檢查媒體類型的資料流程執行迴圈。</span><span class="sxs-lookup"><span data-stu-id="dd65f-116">Get the number of streams, and loop through each stream checking the media type.</span></span> <span data-ttu-id="dd65f-117">[**IMediaDet：： get \_ OutputStreams**](imediadet-get-outputstreams.md)方法會抓取資料流程的數目，而 [**IMediaDet：:p 的內容 \_ CurrentStream**](imediadet-put-currentstream.md)方法會指定要檢查的資料流程。</span><span class="sxs-lookup"><span data-stu-id="dd65f-117">The [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) method retrieves the number of streams, and the [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) method specifies which stream to examine.</span></span> <span data-ttu-id="dd65f-118">結束第一個影片串流上的迴圈。</span><span class="sxs-lookup"><span data-stu-id="dd65f-118">Exit the loop on the first video stream.</span></span>


```C++
long lStreams;
bool bFound = false;
hr = pDet->get_OutputStreams(&lStreams);
for (long i = 0; i < lStreams; i++)
{
    GUID major_type;
    hr = pDet->put_CurrentStream(i);
    hr = pDet->get_StreamType(&major_type);
    if (major_type == MEDIATYPE_Video)  // Found a video stream.
    {
        bFound = true;
        break;
    }
}
if (!bFound) return VFW_E_INVALIDMEDIATYPE;
```



<span data-ttu-id="dd65f-119">如果找不到任何影片資料流程，則函式會結束。</span><span class="sxs-lookup"><span data-stu-id="dd65f-119">If no video stream was found, the function exits.</span></span>

<span data-ttu-id="dd65f-120">在先前的程式碼中， [**IMediaDet：： get \_ StreamType**](imediadet-get-streamtype.md) 方法只會傳回主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="dd65f-120">In the previous code, the [**IMediaDet::get\_StreamType**](imediadet-get-streamtype.md) method returns just the major type GUID.</span></span> <span data-ttu-id="dd65f-121">如果您不需要檢查完整的媒體類型，這會很方便。</span><span class="sxs-lookup"><span data-stu-id="dd65f-121">This is convenient if you do not need to examine the complete media type.</span></span> <span data-ttu-id="dd65f-122">不過，若要取得影片尺寸，必須檢查格式區塊，因此需要完整的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="dd65f-122">To get the video dimensions, however, it is necessary to examine the format block, so the full media type is needed.</span></span> <span data-ttu-id="dd65f-123">您可以藉由呼叫 [**IMediaDet：： get \_ StreamMediaType**](imediadet-get-streammediatype.md) 方法來取得，此方法會填入 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。</span><span class="sxs-lookup"><span data-stu-id="dd65f-123">You can retrieve that by calling the [**IMediaDet::get\_StreamMediaType**](imediadet-get-streammediatype.md) method, which fills in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="dd65f-124">媒體偵測器會使用 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 格式區塊，將所有影片串流轉換成未壓縮的格式。</span><span class="sxs-lookup"><span data-stu-id="dd65f-124">The Media Detector converts all video streams into uncompressed format, with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format block.</span></span>


```C++
long width = 0, height = 0; 
AM_MEDIA_TYPE mt;
hr = pDet->get_StreamMediaType(&mt);
if (mt.formattype == FORMAT_VideoInfo) 
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
    width = pVih->bmiHeader.biWidth;
    height = pVih->bmiHeader.biHeight;
    
    // We want the absolute height, and don't care about up-down orientation.
    if (height < 0) height *= -1;
}
else {
    return VFW_E_INVALIDMEDIATYPE; // This should not happen, in theory.
}
FreeMediaType(mt);
```



<span data-ttu-id="dd65f-125">[**Get \_ StreamMediaType**](imediadet-get-streammediatype.md)方法會配置呼叫端必須釋放的格式區塊。</span><span class="sxs-lookup"><span data-stu-id="dd65f-125">The [**get\_StreamMediaType**](imediadet-get-streammediatype.md) method allocates the format block, which the caller must free.</span></span> <span data-ttu-id="dd65f-126">這個範例會使用基類庫中的 [**FreeMediaType**](freemediatype.md) 函式。</span><span class="sxs-lookup"><span data-stu-id="dd65f-126">This example uses the [**FreeMediaType**](freemediatype.md) function from the base class library.</span></span>

<span data-ttu-id="dd65f-127">現在您已準備好取得海報框架。</span><span class="sxs-lookup"><span data-stu-id="dd65f-127">Now you are ready to get the poster frame.</span></span> <span data-ttu-id="dd65f-128">先呼叫 [**IMediaDet：： GetBitmapBits**](imediadet-getbitmapbits.md) 方法以及緩衝區的 **Null** 指標：</span><span class="sxs-lookup"><span data-stu-id="dd65f-128">First call the [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) method with a **NULL** pointer for the buffer:</span></span>


```C++
long lSize;
hr = pDet->GetBitmapBits(0, &lSize, NULL, width, height);
```



<span data-ttu-id="dd65f-129">此呼叫會在 *lSize* 參數中傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="dd65f-129">This call returns the required buffer size in the *lSize* parameter.</span></span> <span data-ttu-id="dd65f-130">第一個參數指定要搜尋的資料流程時間;這個範例會使用時間零。</span><span class="sxs-lookup"><span data-stu-id="dd65f-130">The first parameter specifies the stream time to seek to; this example uses time zero.</span></span> <span data-ttu-id="dd65f-131">針對寬度和高度，此範例會使用稍早取得的原生影片維度。</span><span class="sxs-lookup"><span data-stu-id="dd65f-131">For the width and height, this example uses the native video dimensions obtained earlier.</span></span> <span data-ttu-id="dd65f-132">如果您指定其他值，媒體偵測器會延展點陣圖使其相符。</span><span class="sxs-lookup"><span data-stu-id="dd65f-132">If you specify other values, the Media Detector will stretch the bitmap to match.</span></span>

<span data-ttu-id="dd65f-133">如果方法成功，請配置緩衝區，並再次呼叫 [**GetBitmapBits**](imediadet-getbitmapbits.md) ：</span><span class="sxs-lookup"><span data-stu-id="dd65f-133">If the method succeeds, allocate the buffer and call [**GetBitmapBits**](imediadet-getbitmapbits.md) again:</span></span>


```C++
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[lSize];
    if (!pBuffer) return E_OUTOFMEMORY;
    hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
    if (FAILED(hr))
        delete [] pBuffer;
}
```



<span data-ttu-id="dd65f-134">以下是完整的函式，有更好的錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="dd65f-134">Here is the complete function, with somewhat better error handling.</span></span>


```C++
HRESULT GetBitmap(LPTSTR pszFileName, BITMAPINFOHEADER** ppbmih)
{
    HRESULT hr;
    CComPtr<IMediaDet> pDet;
    hr = pDet.CoCreateInstance(__uuidof(MediaDet));
    if (FAILED(hr)) return hr;

    // Convert the file name to a BSTR.
    CComBSTR bstrFilename(pszFileName);
    hr = pDet->put_Filename(bstrFilename);
    if (FAILED(hr)) return hr;

    long lStreams;
    bool bFound = false;
    hr = pDet->get_OutputStreams(&lStreams);
    if (FAILED(hr)) return hr;

    for (long i = 0; i < lStreams; i++)
    {
        GUID major_type;
        hr = pDet->put_CurrentStream(i);
        if (SUCCEEDED(hr))
        {
            hr = pDet->get_StreamType(&major_type);
        }
        if (FAILED(hr)) break;

        if (major_type == MEDIATYPE_Video)
        {
            bFound = true;
            break;
        }
    }
    if (!bFound) return VFW_E_INVALIDMEDIATYPE;

    long width = 0, height = 0; 
    AM_MEDIA_TYPE mt;
    hr = pDet->get_StreamMediaType(&mt);
    if (SUCCEEDED(hr)) 
    {
        if ((mt.formattype == FORMAT_VideoInfo) && 
            (mt.cbFormat >= sizeof(VIDEOINFOHEADER)))
        {
            VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)(mt.pbFormat);
            width = pVih->bmiHeader.biWidth;
            height = pVih->bmiHeader.biHeight;
        
            // We want the absolute height, don't care about orientation.
            if (height < 0) height *= -1;
        }
        else
        {
            hr = VFW_E_INVALIDMEDIATYPE; // Should not happen, in theory.
        }
        FreeMediaType(mt);
    }
    if (FAILED(hr)) return hr;
    
    // Find the required buffer size.
    long size;
    hr = pDet->GetBitmapBits(0, &size, NULL, width, height);
    if (SUCCEEDED(hr)) 
    {
        char *pBuffer = new char[size];
        if (!pBuffer) return E_OUTOFMEMORY;
        try {
            hr = pDet->GetBitmapBits(0, NULL, pBuffer, width, height);
            if (SUCCEEDED(hr))
            {
                // Delete the old image, if any.
                if (*ppbmih) delete[] (*ppbmih);
                (*ppbmih) = (BITMAPINFOHEADER*)pBuffer;
            }
            else
            {
                delete [] pBuffer;
            }
        }
        catch (...) {
            delete [] pBuffer;
            return E_OUTOFMEMORY;
        }
    }
    return hr;
}
```



<span data-ttu-id="dd65f-135">下一 [步：步驟4：在工作區上繪製點陣圖](step-4--draw-the-bitmap-on-the-client-area.md)</span><span class="sxs-lookup"><span data-stu-id="dd65f-135">Next: [Step 4: Draw the Bitmap on the Client Area](step-4--draw-the-bitmap-on-the-client-area.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd65f-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="dd65f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd65f-137">抓取海報框架</span><span class="sxs-lookup"><span data-stu-id="dd65f-137">Grabbing a Poster Frame</span></span>](grabbing-a-poster-frame.md)
</dt> </dl>

 

 
