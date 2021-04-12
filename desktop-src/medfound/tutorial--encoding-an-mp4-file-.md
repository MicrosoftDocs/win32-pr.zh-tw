---
description: 本教學課程會示範如何使用轉碼 API，以視頻串流的 h.264 和音訊串流的 AAC 來編碼數量檔案。
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 教學課程：編碼的檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192153"
---
# <a name="tutorial-encoding-an-mp4-file"></a><span data-ttu-id="55b09-103">教學課程：編碼的檔</span><span class="sxs-lookup"><span data-stu-id="55b09-103">Tutorial: Encoding an MP4 File</span></span>

<span data-ttu-id="55b09-104">本教學課程會示範如何使用 [轉碼 API](transcode-api.md) ，以視頻串流的 h.264 和音訊串流的 AAC 來編碼數量檔案。</span><span class="sxs-lookup"><span data-stu-id="55b09-104">This tutorial shows how to use the [Transcode API](transcode-api.md) to encode an MP4 file, using H.264 for the video stream and AAC for the audio stream.</span></span>

-   [<span data-ttu-id="55b09-105">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="55b09-105">Headers and Library Files</span></span>](#headers-and-library-files)
-   [<span data-ttu-id="55b09-106">定義編碼設定檔</span><span class="sxs-lookup"><span data-stu-id="55b09-106">Define the Encoding Profiles</span></span>](#define-the-encoding-profiles)
-   [<span data-ttu-id="55b09-107">撰寫 wmain 函式</span><span class="sxs-lookup"><span data-stu-id="55b09-107">Write the wmain Function</span></span>](#write-the-wmain-function)
-   [<span data-ttu-id="55b09-108">編碼檔案</span><span class="sxs-lookup"><span data-stu-id="55b09-108">Encode the File</span></span>](#encode-the-file)
    -   [<span data-ttu-id="55b09-109">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="55b09-109">Create the Media Source</span></span>](#create-the-media-source)
    -   [<span data-ttu-id="55b09-110">取得來源持續時間</span><span class="sxs-lookup"><span data-stu-id="55b09-110">Get the Source Duration</span></span>](#get-the-source-duration)
    -   [<span data-ttu-id="55b09-111">建立轉碼設定檔</span><span class="sxs-lookup"><span data-stu-id="55b09-111">Create the Transcode Profile</span></span>](#create-the-transcode-profile)
    -   [<span data-ttu-id="55b09-112">執行編碼會話</span><span class="sxs-lookup"><span data-stu-id="55b09-112">Run the Encoding Session</span></span>](#run-the-encoding-session)
-   [<span data-ttu-id="55b09-113">媒體會話協助程式</span><span class="sxs-lookup"><span data-stu-id="55b09-113">Media Session Helper</span></span>](#media-session-helper)
-   [<span data-ttu-id="55b09-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="55b09-114">Related topics</span></span>](#related-topics)

## <a name="headers-and-library-files"></a><span data-ttu-id="55b09-115">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="55b09-115">Headers and Library Files</span></span>

<span data-ttu-id="55b09-116">請包含下列標頭檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-116">Include the following header files.</span></span>


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



<span data-ttu-id="55b09-117">連結下列程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="55b09-117">Link the following library files.</span></span>


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a><span data-ttu-id="55b09-118">定義編碼設定檔</span><span class="sxs-lookup"><span data-stu-id="55b09-118">Define the Encoding Profiles</span></span>

<span data-ttu-id="55b09-119">其中一種編碼方式是定義事先已知的目標編碼配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="55b09-119">One approach to encoding is to define a list of target encoding profiles that are known in advance.</span></span> <span data-ttu-id="55b09-120">在本教學課程中，我們會採用相當簡單的方法，並儲存 h.264 video 和 AAC 音訊的編碼格式清單。</span><span class="sxs-lookup"><span data-stu-id="55b09-120">For this tutorial, we take a relatively simple approach, and store a list of encoding formats for H.264 video and AAC audio.</span></span>

<span data-ttu-id="55b09-121">對於 h.264，最重要的格式屬性是 h.264 設定檔、畫面播放速率、框架大小和編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="55b09-121">For H.264, the most important format attributes are the H.264 profile, the frame rate, the frame size, and the encoded bit rate.</span></span> <span data-ttu-id="55b09-122">下列陣列包含 h.264 編碼格式的清單。</span><span class="sxs-lookup"><span data-stu-id="55b09-122">The following array contains a list of H.264 encoding formats.</span></span>


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



<span data-ttu-id="55b09-123">H.264 設定檔是使用 [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 列舉來指定。</span><span class="sxs-lookup"><span data-stu-id="55b09-123">H.264 profiles are specified using the [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) enumeration.</span></span> <span data-ttu-id="55b09-124">您也可以指定 h.264 層級，但 Microsoft 媒體基礎 h.264 [**影片編碼器**](h-264-video-encoder.md) 可以為指定的影片串流衍生適當的層級，因此建議不要覆寫編碼器的選取層級。</span><span class="sxs-lookup"><span data-stu-id="55b09-124">You could also specify the H.264 level, but the Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) can derive the proper level for a given video stream, so it is recommended not to override the encoder's selected level.</span></span> <span data-ttu-id="55b09-125">針對交錯式內容，您也可以指定交錯模式 (查看 [影片交錯](video-interlacing.md)) 。</span><span class="sxs-lookup"><span data-stu-id="55b09-125">For interlaced content, you would also specify the interlace mode (see [Video Interlacing](video-interlacing.md)).</span></span>

<span data-ttu-id="55b09-126">針對 AAC 音訊，最重要的格式屬性是音訊取樣率、通道數目、每個樣本的位數，以及編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="55b09-126">For AAC audio, the most important format attributes are the audio sample rate, the number of channels, the number of bits per sample, and the encoded bit rate.</span></span> <span data-ttu-id="55b09-127">（選擇性）您可以設定 AAC 音訊設定檔層級指示。</span><span class="sxs-lookup"><span data-stu-id="55b09-127">Optionally, you can set the AAC audio profile level indication.</span></span> <span data-ttu-id="55b09-128">如需詳細資訊，請參閱 [**AAC 編碼器**](aac-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="55b09-128">For more information, see [**AAC Encoder**](aac-encoder.md).</span></span> <span data-ttu-id="55b09-129">下列陣列包含 AAC 編碼格式的清單。</span><span class="sxs-lookup"><span data-stu-id="55b09-129">The following array contains a list of AAC encoding formats.</span></span>


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> <span data-ttu-id="55b09-130">`H264ProfileInfo` `AACProfileInfo` 此處定義的和結構不是媒體基礎 API 的一部分。</span><span class="sxs-lookup"><span data-stu-id="55b09-130">The `H264ProfileInfo` and `AACProfileInfo` structures defined here are not part of the Media Foundation API.</span></span>

 

## <a name="write-the-wmain-function"></a><span data-ttu-id="55b09-131">撰寫 wmain 函式</span><span class="sxs-lookup"><span data-stu-id="55b09-131">Write the wmain Function</span></span>

<span data-ttu-id="55b09-132">下列程式碼顯示主控台應用程式的進入點。</span><span class="sxs-lookup"><span data-stu-id="55b09-132">The following code shows the entry point for the console application.</span></span>


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



<span data-ttu-id="55b09-133">`wmain`函數會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="55b09-133">The `wmain` function does the following:</span></span>

1.  <span data-ttu-id="55b09-134">呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函數，以初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="55b09-134">Calls the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) function to initialize the COM library.</span></span>
2.  <span data-ttu-id="55b09-135">呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函數來初始化媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="55b09-135">Calls the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function to initialize Media Foundation.</span></span>
3.  <span data-ttu-id="55b09-136">呼叫應用程式定義 `EncodeFile` 函數。</span><span class="sxs-lookup"><span data-stu-id="55b09-136">Calls the application-defined `EncodeFile` function.</span></span> <span data-ttu-id="55b09-137">此函式會將輸入檔轉碼至輸出檔，並顯示在下一節中。</span><span class="sxs-lookup"><span data-stu-id="55b09-137">This function transcodes the input file to the output file, and is shown in the next section.</span></span>
4.  <span data-ttu-id="55b09-138">呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 函數來關閉媒體基礎。</span><span class="sxs-lookup"><span data-stu-id="55b09-138">Calls the [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) function to shut down Media Foundation.</span></span>
5.  <span data-ttu-id="55b09-139">呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式，將 COM 程式庫解除初始化。</span><span class="sxs-lookup"><span data-stu-id="55b09-139">Call the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function to uninitialize the COM library.</span></span>

## <a name="encode-the-file"></a><span data-ttu-id="55b09-140">編碼檔案</span><span class="sxs-lookup"><span data-stu-id="55b09-140">Encode the File</span></span>

<span data-ttu-id="55b09-141">下列程式碼會顯示執行轉碼的函式 `EncodeFile` 。</span><span class="sxs-lookup"><span data-stu-id="55b09-141">The following code shows `EncodeFile` function, which performs the transcoding.</span></span> <span data-ttu-id="55b09-142">此函式大部分是由其他應用程式定義函式的呼叫所組成，這些函數稍後會在本主題中顯示。</span><span class="sxs-lookup"><span data-stu-id="55b09-142">This function consists mostly of calls to other application-defined functions, which are shown later in this topic.</span></span>


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



<span data-ttu-id="55b09-143">此 `EncodeFile` 函數會執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="55b09-143">The `EncodeFile` function performs the following steps.</span></span>

1.  <span data-ttu-id="55b09-144">使用輸入檔的 URL 或檔案路徑，建立輸入檔案的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="55b09-144">Creates a media source for the input file, using the URL or file path of the input file.</span></span> <span data-ttu-id="55b09-145"> (參閱 [建立媒體來源](#create-the-media-source)。 ) </span><span class="sxs-lookup"><span data-stu-id="55b09-145">(See [Create the Media Source](#create-the-media-source).)</span></span>
2.  <span data-ttu-id="55b09-146">取得輸入檔的持續時間。</span><span class="sxs-lookup"><span data-stu-id="55b09-146">Gets the duration of the input file.</span></span> <span data-ttu-id="55b09-147"> (查看 [取得來源持續時間](#get-the-source-duration)。 ) </span><span class="sxs-lookup"><span data-stu-id="55b09-147">(See [Get the Source Duration](#get-the-source-duration).)</span></span>
3.  <span data-ttu-id="55b09-148">建立轉碼設定檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-148">Create the transcode profile.</span></span> <span data-ttu-id="55b09-149"> (參閱 [建立轉碼設定檔](#create-the-transcode-profile)。 ) </span><span class="sxs-lookup"><span data-stu-id="55b09-149">(See [Create the Transcode Profile](#create-the-transcode-profile).)</span></span>
4.  <span data-ttu-id="55b09-150">呼叫 [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 來建立部分轉碼拓撲。</span><span class="sxs-lookup"><span data-stu-id="55b09-150">Call [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) to create the partial transcode topology.</span></span>
5.  <span data-ttu-id="55b09-151">建立管理媒體會話的 helper 物件。</span><span class="sxs-lookup"><span data-stu-id="55b09-151">Create a helper object that manages the Media Session.</span></span> <span data-ttu-id="55b09-152"> (參閱媒體會話協助程式) 。</span><span class="sxs-lookup"><span data-stu-id="55b09-152">(See Media Session Helper).</span></span>
6.  <span data-ttu-id="55b09-153">執行編碼會話，並等候它完成。</span><span class="sxs-lookup"><span data-stu-id="55b09-153">Run the encoding session and wait for it to complete.</span></span> <span data-ttu-id="55b09-154"> (參閱 [執行編碼會話](#run-the-encoding-session)。 ) </span><span class="sxs-lookup"><span data-stu-id="55b09-154">(See [Run the Encoding Session](#run-the-encoding-session).)</span></span>
7.  <span data-ttu-id="55b09-155">呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉媒體來源。</span><span class="sxs-lookup"><span data-stu-id="55b09-155">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) to shut down the media source.</span></span>
8.  <span data-ttu-id="55b09-156">發行介面指標。</span><span class="sxs-lookup"><span data-stu-id="55b09-156">Release interface pointers.</span></span> <span data-ttu-id="55b09-157">此程式碼會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。</span><span class="sxs-lookup"><span data-stu-id="55b09-157">This code uses the [SafeRelease](saferelease.md) function to release interface pointers.</span></span> <span data-ttu-id="55b09-158">另一個選項是使用 COM 智慧型指標類別，例如 **CComPtr**。</span><span class="sxs-lookup"><span data-stu-id="55b09-158">Another option is to use a COM smart pointer class, such as **CComPtr**.</span></span>

### <a name="create-the-media-source"></a><span data-ttu-id="55b09-159">建立媒體來源</span><span class="sxs-lookup"><span data-stu-id="55b09-159">Create the Media Source</span></span>

<span data-ttu-id="55b09-160">媒體來源是讀取和剖析輸入檔的物件。</span><span class="sxs-lookup"><span data-stu-id="55b09-160">The media source is the object that reads and parses the input file.</span></span> <span data-ttu-id="55b09-161">若要建立媒體來源，請將輸入檔的 URL 傳遞至 [來源解析程式](source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="55b09-161">To create the media source, pass the URL of the input file to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="55b09-162">下列程式碼示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="55b09-162">The following code shows how to do this.</span></span>


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="55b09-163">如需詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。</span><span class="sxs-lookup"><span data-stu-id="55b09-163">For more information, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

### <a name="get-the-source-duration"></a><span data-ttu-id="55b09-164">取得來源持續時間</span><span class="sxs-lookup"><span data-stu-id="55b09-164">Get the Source Duration</span></span>

<span data-ttu-id="55b09-165">雖然並非必要，但在輸入檔案期間查詢媒體來源會很有用。</span><span class="sxs-lookup"><span data-stu-id="55b09-165">Although not required, it is useful to query the media source for the duration of the input file.</span></span> <span data-ttu-id="55b09-166">這個值可以用來追蹤編碼進度。</span><span class="sxs-lookup"><span data-stu-id="55b09-166">This value can be used to track the encoding progress.</span></span> <span data-ttu-id="55b09-167">持續時間會儲存在展示描述項的 [ [**MF \_ PD \_ 持續時間**](mf-pd-duration-attribute.md) ] 屬性中。</span><span class="sxs-lookup"><span data-stu-id="55b09-167">The duration is stored in the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute of the presentation descriptor.</span></span> <span data-ttu-id="55b09-168">藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="55b09-168">Get the presentation descriptor by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a><span data-ttu-id="55b09-169">建立轉碼設定檔</span><span class="sxs-lookup"><span data-stu-id="55b09-169">Create the Transcode Profile</span></span>

<span data-ttu-id="55b09-170">轉碼設定檔會描述編碼參數。</span><span class="sxs-lookup"><span data-stu-id="55b09-170">The transcode profile describes the encoding parameters.</span></span> <span data-ttu-id="55b09-171">如需建立轉碼設定檔的詳細資訊，請參閱 [使用轉碼 API](fast-transcode-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="55b09-171">For more information about creating a transcode profile, see [Using the Transcode API](fast-transcode-objects.md).</span></span> <span data-ttu-id="55b09-172">若要建立設定檔，請執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="55b09-172">To create the profile, perform the following steps.</span></span>

1.  <span data-ttu-id="55b09-173">呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 以建立空的設定檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-173">Call [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) to create the empty profile.</span></span>
2.  <span data-ttu-id="55b09-174">建立 AAC 音訊串流的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="55b09-174">Create a media type for the AAC audio stream.</span></span> <span data-ttu-id="55b09-175">藉由呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)將其新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-175">Add it to the profile by calling [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span>
3.  <span data-ttu-id="55b09-176">建立 h.264 影片串流的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="55b09-176">Create a media type for the H.264 video stream.</span></span> <span data-ttu-id="55b09-177">藉由呼叫 [**IMFTranscodeProfile：： SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)將其新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-177">Add it to the profile by calling [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span>
4.  <span data-ttu-id="55b09-178">呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立容器層級屬性的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="55b09-178">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store for the container-level attributes.</span></span>
5.  <span data-ttu-id="55b09-179">設定 [ [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-179">Set the [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute.</span></span> <span data-ttu-id="55b09-180">這是唯一需要的容器層級屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-180">This is the only required container-level attribute.</span></span> <span data-ttu-id="55b09-181">若為設定檔輸出，請將此屬性設定為 **MFTranscodeContainerType \_ MPEG4**。</span><span class="sxs-lookup"><span data-stu-id="55b09-181">For MP4 file output, set this attribute to **MFTranscodeContainerType\_MPEG4**.</span></span>
6.  <span data-ttu-id="55b09-182">呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) 來設定容器層級的屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-182">Call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) to set the container-level attributes.</span></span>

<span data-ttu-id="55b09-183">下列程式碼顯示這些步驟。</span><span class="sxs-lookup"><span data-stu-id="55b09-183">The following code shows these steps.</span></span>


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



<span data-ttu-id="55b09-184">若要指定 h.264 影片資料流程的屬性，請建立屬性存放區，並設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="55b09-184">To specify the attributes for the H.264 video stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="55b09-185">屬性</span><span class="sxs-lookup"><span data-stu-id="55b09-185">Attribute</span></span>                                                       | <span data-ttu-id="55b09-186">描述</span><span class="sxs-lookup"><span data-stu-id="55b09-186">Desription</span></span>                      |
|-----------------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="55b09-187">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="55b09-187">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)              | <span data-ttu-id="55b09-188">設定為 **MFVideoFormat \_ H264**。</span><span class="sxs-lookup"><span data-stu-id="55b09-188">Set to **MFVideoFormat\_H264**.</span></span> |
| [<span data-ttu-id="55b09-189">**MF \_ MT \_ MPEG2 \_ 設定檔**</span><span class="sxs-lookup"><span data-stu-id="55b09-189">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md) | <span data-ttu-id="55b09-190">H.264 設定檔。</span><span class="sxs-lookup"><span data-stu-id="55b09-190">H.264 profile.</span></span>                  |
| [<span data-ttu-id="55b09-191">**MF \_ MT \_ 框架 \_ 大小**</span><span class="sxs-lookup"><span data-stu-id="55b09-191">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)       | <span data-ttu-id="55b09-192">框架大小。</span><span class="sxs-lookup"><span data-stu-id="55b09-192">Frame size.</span></span>                     |
| [<span data-ttu-id="55b09-193">**MF \_ MT \_ 幀 \_ 速率**</span><span class="sxs-lookup"><span data-stu-id="55b09-193">**MF\_MT\_FRAME\_RATE**</span></span>](mf-mt-frame-rate-attribute.md)       | <span data-ttu-id="55b09-194">畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="55b09-194">Frame rate.</span></span>                     |
| [<span data-ttu-id="55b09-195">**MF \_ MT \_ 平均 \_ 位元速率**</span><span class="sxs-lookup"><span data-stu-id="55b09-195">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)     | <span data-ttu-id="55b09-196">編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="55b09-196">Encoded bit rate.</span></span>               |



 

<span data-ttu-id="55b09-197">若要指定 AAC 音訊資料流程的屬性，請建立屬性存放區，並設定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="55b09-197">To specify the attributes for the AAC audio stream, create an attribute store and set the following attributes:</span></span>



| <span data-ttu-id="55b09-198">屬性</span><span class="sxs-lookup"><span data-stu-id="55b09-198">Attribute</span></span>                                                                                      | <span data-ttu-id="55b09-199">描述</span><span class="sxs-lookup"><span data-stu-id="55b09-199">Desription</span></span>                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [<span data-ttu-id="55b09-200">**MF \_ MT \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="55b09-200">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="55b09-201">設定為 **MFAudioFormat \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="55b09-201">Set to **MFAudioFormat\_AAC**</span></span>            |
| [<span data-ttu-id="55b09-202">**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55b09-202">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="55b09-203">音訊取樣率。</span><span class="sxs-lookup"><span data-stu-id="55b09-203">Audio sample rate.</span></span>                       |
| [<span data-ttu-id="55b09-204">**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**</span><span class="sxs-lookup"><span data-stu-id="55b09-204">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="55b09-205">每個音訊範例的位數。</span><span class="sxs-lookup"><span data-stu-id="55b09-205">Bits per audio sample.</span></span>                   |
| [<span data-ttu-id="55b09-206">**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**</span><span class="sxs-lookup"><span data-stu-id="55b09-206">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="55b09-207">音訊聲道數目。</span><span class="sxs-lookup"><span data-stu-id="55b09-207">Number of audio channels.</span></span>                |
| [<span data-ttu-id="55b09-208">**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="55b09-208">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="55b09-209">編碼的位元速率。</span><span class="sxs-lookup"><span data-stu-id="55b09-209">Encoded bit rate.</span></span>                        |
| [<span data-ttu-id="55b09-210">**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**</span><span class="sxs-lookup"><span data-stu-id="55b09-210">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="55b09-211">設定為 1。</span><span class="sxs-lookup"><span data-stu-id="55b09-211">Set to 1.</span></span>                                |
| [<span data-ttu-id="55b09-212">MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示</span><span class="sxs-lookup"><span data-stu-id="55b09-212">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="55b09-213">AAC 設定檔層級指示 (選擇性) 。</span><span class="sxs-lookup"><span data-stu-id="55b09-213">AAC profile level indication (optional).</span></span> |



 

<span data-ttu-id="55b09-214">下列程式碼會建立影片資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-214">The following code creates the video stream attributes.</span></span>


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="55b09-215">下列程式碼會建立音訊資料流程屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-215">The following code creates the audio stream attributes.</span></span>


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



<span data-ttu-id="55b09-216">請注意，轉碼 API 不需要真正的媒體類型，不過它會使用媒體類型的屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-216">Note that the transcode API does not require a true media type, although it uses media-type attributes.</span></span> <span data-ttu-id="55b09-217">尤其是，因為 [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)和 [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)方法意指主要型別，所以不需要 [**MF \_ MT \_ 主要 \_ 型**](mf-mt-major-type-attribute.md)別屬性。</span><span class="sxs-lookup"><span data-stu-id="55b09-217">In particular, the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute it not required, because the [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) and [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) methods imply the major type.</span></span> <span data-ttu-id="55b09-218">不過，它也是將實際的媒體類型傳遞給這些方法的有效方式。</span><span class="sxs-lookup"><span data-stu-id="55b09-218">However, it also valid to pass an actual media type to these methods.</span></span> <span data-ttu-id="55b09-219">[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)介面 (繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)) 。</span><span class="sxs-lookup"><span data-stu-id="55b09-219">(The [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface inherits [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)</span></span>

### <a name="run-the-encoding-session"></a><span data-ttu-id="55b09-220">執行編碼會話</span><span class="sxs-lookup"><span data-stu-id="55b09-220">Run the Encoding Session</span></span>

<span data-ttu-id="55b09-221">下列程式碼會執行編碼會話。</span><span class="sxs-lookup"><span data-stu-id="55b09-221">The following code runs the encoding session.</span></span> <span data-ttu-id="55b09-222">它會使用 Media Session helper 類別，如下一節所示。</span><span class="sxs-lookup"><span data-stu-id="55b09-222">It uses the Media Session helper class, which is shown in the next section.</span></span>


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a><span data-ttu-id="55b09-223">媒體會話協助程式</span><span class="sxs-lookup"><span data-stu-id="55b09-223">Media Session Helper</span></span>

<span data-ttu-id="55b09-224">本檔的[媒體基礎架構](media-foundation-architecture.md)一節中會更完整地說明[媒體會話](media-session.md)。</span><span class="sxs-lookup"><span data-stu-id="55b09-224">The [Media Session](media-session.md) is described more fully in the [Media Foundation Architecture](media-foundation-architecture.md) section of this documentation.</span></span> <span data-ttu-id="55b09-225">媒體會話使用非同步事件模型。</span><span class="sxs-lookup"><span data-stu-id="55b09-225">The Media Session uses an asynchronous event model.</span></span> <span data-ttu-id="55b09-226">在 GUI 應用程式中，您應該在不封鎖 UI 執行緒等候下一個事件的情況下，回應會話事件。</span><span class="sxs-lookup"><span data-stu-id="55b09-226">In a GUI application, you should respond to session events without blocking the UI thread to wait for the next event.</span></span> <span data-ttu-id="55b09-227">教學課程 [如何播放未受保護的媒體](how-to-play-unprotected-media-files.md) 檔案示範如何在播放應用程式中進行此操作。</span><span class="sxs-lookup"><span data-stu-id="55b09-227">The tutorial [How to Play Unprotected Media Files](how-to-play-unprotected-media-files.md) shows how to do this in a playback application.</span></span> <span data-ttu-id="55b09-228">針對編碼，原則是相同的，但事件較少：</span><span class="sxs-lookup"><span data-stu-id="55b09-228">For encoding, the principle is the same, but fewer events are relevant:</span></span>



| <span data-ttu-id="55b09-229">事件</span><span class="sxs-lookup"><span data-stu-id="55b09-229">Event</span></span>                                  | <span data-ttu-id="55b09-230">描述</span><span class="sxs-lookup"><span data-stu-id="55b09-230">Desription</span></span>                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55b09-231">MESessionEnded</span><span class="sxs-lookup"><span data-stu-id="55b09-231">MESessionEnded</span></span>](mesessionended.md)   | <span data-ttu-id="55b09-232">在編碼完成時引發。</span><span class="sxs-lookup"><span data-stu-id="55b09-232">Raised when the encoding is complete.</span></span>                                                                                                                            |
| [<span data-ttu-id="55b09-233">MESessionClosed</span><span class="sxs-lookup"><span data-stu-id="55b09-233">MESessionClosed</span></span>](mesessionclosed.md) | <span data-ttu-id="55b09-234">[**IMFMediaSession：： Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close)方法完成時引發。</span><span class="sxs-lookup"><span data-stu-id="55b09-234">Raised when the [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) method completes.</span></span> <span data-ttu-id="55b09-235">引發此事件之後，就可以安全地關閉媒體會話。</span><span class="sxs-lookup"><span data-stu-id="55b09-235">After this event is raised, it is safe to shut down the Media Session.</span></span> |



 

<span data-ttu-id="55b09-236">若為主控台應用程式，則可合理地封鎖和等候事件。</span><span class="sxs-lookup"><span data-stu-id="55b09-236">For a console application, it is reasonable to block and wait for events.</span></span> <span data-ttu-id="55b09-237">根據來源檔案和編碼設定，可能需要一些時間才能完成編碼。</span><span class="sxs-lookup"><span data-stu-id="55b09-237">Depending on the source file and the encoding settings, it might take awhile to complete the encoding.</span></span> <span data-ttu-id="55b09-238">您可以取得進度更新，如下所示：</span><span class="sxs-lookup"><span data-stu-id="55b09-238">You can get progress updates as follows:</span></span>

1.  <span data-ttu-id="55b09-239">呼叫 [**IMFMediaSession：： GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) 以取得簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="55b09-239">Call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) to get the presentation clock.</span></span>
2.  <span data-ttu-id="55b09-240">查詢 [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) 介面的時鐘。</span><span class="sxs-lookup"><span data-stu-id="55b09-240">Query the clock for the [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) interface.</span></span>
3.  <span data-ttu-id="55b09-241">呼叫 [**IMFPresentationClock：： GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) 以取得目前的位置。</span><span class="sxs-lookup"><span data-stu-id="55b09-241">Call [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) to get the current position.</span></span>
4.  <span data-ttu-id="55b09-242">位置會以時間單位來指定。</span><span class="sxs-lookup"><span data-stu-id="55b09-242">The position is given in units of time.</span></span> <span data-ttu-id="55b09-243">若要取得已完成的百分比，請使用此值 `(100 * position) / duration` 。</span><span class="sxs-lookup"><span data-stu-id="55b09-243">To get the percentage completed, use the value `(100 * position) / duration`.</span></span>

<span data-ttu-id="55b09-244">以下是類別的宣告 `CSession` 。</span><span class="sxs-lookup"><span data-stu-id="55b09-244">Here is the declaration of the `CSession` class.</span></span>


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



<span data-ttu-id="55b09-245">下列程式碼顯示類別的完整實作為 `CSession` 。</span><span class="sxs-lookup"><span data-stu-id="55b09-245">The following code shows the complete implementation of the `CSession` class.</span></span>


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEvent->GetStatus(&hrStatus);
    if (FAILED(hr))
    {
        goto done;
    }

    if (FAILED(hrStatus))
    {
        hr = hrStatus;
        goto done;
    }

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="55b09-246">相關主題</span><span class="sxs-lookup"><span data-stu-id="55b09-246">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55b09-247">**AAC 編碼器**</span><span class="sxs-lookup"><span data-stu-id="55b09-247">**AAC Encoder**</span></span>](aac-encoder.md)
</dt> <dt>

[<span data-ttu-id="55b09-248">**H.264 影片編碼器**</span><span class="sxs-lookup"><span data-stu-id="55b09-248">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="55b09-249">媒體會話</span><span class="sxs-lookup"><span data-stu-id="55b09-249">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="55b09-250">媒體類型</span><span class="sxs-lookup"><span data-stu-id="55b09-250">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="55b09-251">轉碼 API</span><span class="sxs-lookup"><span data-stu-id="55b09-251">Transcode API</span></span>](transcode-api.md)
</dt> </dl>

 

 
