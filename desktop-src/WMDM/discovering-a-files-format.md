---
title: 探索檔案的格式
description: 探索檔案的格式
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Media 裝置管理員，檔案格式
- 裝置管理員，檔案格式
- 程式設計指南，檔案格式
- 桌面應用程式，檔案格式
- 建立 Windows Media 裝置管理員應用程式，檔案格式
- 將檔案寫入裝置、檔案格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672668"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="6500f-109">探索檔案的格式</span><span class="sxs-lookup"><span data-stu-id="6500f-109">Discovering a File's Format</span></span>

<span data-ttu-id="6500f-110">將檔案傳送至裝置之前，應用程式應判斷裝置是否支援該檔案格式。</span><span class="sxs-lookup"><span data-stu-id="6500f-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="6500f-111">探索檔案的格式可能很複雜。</span><span class="sxs-lookup"><span data-stu-id="6500f-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="6500f-112">最簡單的方式是建立對應至特定 WMDM \_ FORMATCODE 列舉值的副檔名清單。</span><span class="sxs-lookup"><span data-stu-id="6500f-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="6500f-113">不過，這個系統有幾個問題：一個是單一格式可以有多個副檔名 (例如 .jpg、jpe 和 jpeg 影像) 。</span><span class="sxs-lookup"><span data-stu-id="6500f-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="6500f-114">此外，不同的程式可以使用相同的副檔名來進行不同的格式。</span><span class="sxs-lookup"><span data-stu-id="6500f-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="6500f-115">若要克服嚴格對應的限制，應用程式最好驗證格式是否符合延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6500f-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="6500f-116">DirectShow SDK 提供的工具可讓應用程式探索大部分媒體檔案類型的一組有限詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6500f-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="6500f-117">Windows Media Format SDK 會公開大量的詳細資料，但只會顯示最多 ASF 檔。</span><span class="sxs-lookup"><span data-stu-id="6500f-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="6500f-118">由於所有檔案類型的格式程式碼都應該盡可能驗證，因此最好使用 DirectShow 來探索或驗證基本的格式程式碼，然後使用 Windows Media Format SDK 來探索任何其他有關 ASF 檔案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6500f-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="6500f-119">DirectShow 也可以用來探索非 ASF 檔案的基本中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6500f-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="6500f-120">以下是使用延伸模組對應和 DirectShow 探索檔案格式的一種方式。</span><span class="sxs-lookup"><span data-stu-id="6500f-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="6500f-121">首先，將副檔名與已知的副檔名清單進行比較。</span><span class="sxs-lookup"><span data-stu-id="6500f-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="6500f-122">務必讓您的比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6500f-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="6500f-123">如果延伸模組未對應，請將格式設定為 WMDM \_ FORMATCODE \_ UNDEFINED。</span><span class="sxs-lookup"><span data-stu-id="6500f-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="6500f-124">如果找不到格式代碼 (或您想要確認檔案是) 的媒體檔案，您可以執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="6500f-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="6500f-125">使用 **CoCreateInstance** (CLSID MediaDet) 建立 DirectShow 媒體偵測器物件 \_ ，並取出 **IMediaDet** 介面。</span><span class="sxs-lookup"><span data-stu-id="6500f-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="6500f-126">藉由呼叫 **IMediaDet：:p 的檔案 \_ 名稱** 來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="6500f-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="6500f-127">如果檔案受到保護，此呼叫將會失敗。</span><span class="sxs-lookup"><span data-stu-id="6500f-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="6500f-128">藉由呼叫 **IMediaDet：： get \_ StreamMediaType**（傳回 **AM \_ 媒體 \_ 類型**）來取得預設資料流程的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="6500f-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="6500f-129">藉由呼叫 **IMediaDet：： get \_ OutputStreams** 取得資料流程的數目。</span><span class="sxs-lookup"><span data-stu-id="6500f-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="6500f-130">如果只有一個資料流程而且是音訊，則檔案類型會是 WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO</span><span class="sxs-lookup"><span data-stu-id="6500f-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="6500f-131">如果只有一個資料流程而且是影片，則檔案類型會是 WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO</span><span class="sxs-lookup"><span data-stu-id="6500f-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="6500f-132">如果只有一個資料流程而且是影片，而且位元速率為零，則檔案類型會是 WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT。</span><span class="sxs-lookup"><span data-stu-id="6500f-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="6500f-133">您也可以嘗試比對取自 **get \_ StreamMediaType** 的 **VIDEOINFOHEADER** 或 **WAVEFORMATEX** 成員的音訊或影片編解碼器。</span><span class="sxs-lookup"><span data-stu-id="6500f-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="6500f-134">下列 c + + 函式會示範副檔名比對，並使用 DirectShow 來嘗試分析未知的檔案。</span><span class="sxs-lookup"><span data-stu-id="6500f-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a><span data-ttu-id="6500f-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="6500f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6500f-136">**將檔案寫入至裝置**</span><span class="sxs-lookup"><span data-stu-id="6500f-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




