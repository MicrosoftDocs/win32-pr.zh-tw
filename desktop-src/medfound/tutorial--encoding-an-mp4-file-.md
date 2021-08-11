---
description: 本教學課程會示範如何使用轉碼 API，以視頻串流的 h.264 和音訊串流的 AAC 來編碼數量檔案。
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 教學課程：編碼的檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242777f04015f5444be5e0d8424ca06fc4b95cd84ca88c2b997d7b7466c734af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237621"
---
# <a name="tutorial-encoding-an-mp4-file"></a>教學課程：編碼的檔

本教學課程會示範如何使用 [轉碼 API](transcode-api.md) ，以視頻串流的 h.264 和音訊串流的 AAC 來編碼數量檔案。

-   [標頭檔和程式庫檔案](#headers-and-library-files)
-   [定義編碼設定檔](#define-the-encoding-profiles)
-   [撰寫 wmain 函式](#write-the-wmain-function)
-   [編碼檔案](#encode-the-file)
    -   [建立媒體來源](#create-the-media-source)
    -   [取得來源持續時間](#get-the-source-duration)
    -   [建立轉碼設定檔](#create-the-transcode-profile)
    -   [執行編碼會話](#run-the-encoding-session)
-   [媒體會話協助程式](#media-session-helper)
-   [相關主題](#related-topics)

## <a name="headers-and-library-files"></a>標頭檔和程式庫檔案

請包含下列標頭檔。


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



連結下列程式庫檔案。


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>定義編碼設定檔

其中一種編碼方式是定義事先已知的目標編碼配置檔案清單。 在本教學課程中，我們會採用相當簡單的方法，並儲存 h.264 video 和 AAC 音訊的編碼格式清單。

對於 h.264，最重要的格式屬性是 h.264 設定檔、畫面播放速率、框架大小和編碼的位元速率。 下列陣列包含 h.264 編碼格式的清單。


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



H.264 設定檔是使用 [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) 列舉來指定。 您也可以指定 h.264 層級，但 Microsoft 媒體基礎 h.264 [**影片編碼器**](h-264-video-encoder.md) 可以為指定的影片串流衍生適當的層級，因此建議不要覆寫編碼器的選取層級。 針對交錯式內容，您也可以指定交錯模式 (查看 [影片交錯](video-interlacing.md)) 。

針對 AAC 音訊，最重要的格式屬性是音訊取樣率、通道數目、每個樣本的位數，以及編碼的位元速率。 （選擇性）您可以設定 AAC 音訊設定檔層級指示。 如需詳細資訊，請參閱 [**AAC 編碼器**](aac-encoder.md)。 下列陣列包含 AAC 編碼格式的清單。


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
> `H264ProfileInfo` `AACProfileInfo` 此處定義的和結構不是媒體基礎 API 的一部分。

 

## <a name="write-the-wmain-function"></a>撰寫 wmain 函式

下列程式碼顯示主控台應用程式的進入點。


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



`wmain`函數會執行下列動作：

1.  呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 函數，以初始化 COM 程式庫。
2.  呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 函數來初始化媒體基礎。
3.  呼叫應用程式定義 `EncodeFile` 函數。 此函式會將輸入檔轉碼至輸出檔，並顯示在下一節中。
4.  呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 函數來關閉媒體基礎。
5.  呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式，將 COM 程式庫解除初始化。

## <a name="encode-the-file"></a>編碼檔案

下列程式碼會顯示執行轉碼的函式 `EncodeFile` 。 此函式大部分是由其他應用程式定義函式的呼叫所組成，這些函數稍後會在本主題中顯示。


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



此 `EncodeFile` 函數會執行下列步驟。

1.  使用輸入檔的 URL 或檔案路徑，建立輸入檔案的媒體來源。  (參閱 [建立媒體來源](#create-the-media-source)。 ) 
2.  取得輸入檔的持續時間。  (查看 [取得來源持續時間](#get-the-source-duration)。 ) 
3.  建立轉碼設定檔。  (參閱 [建立轉碼設定檔](#create-the-transcode-profile)。 ) 
4.  呼叫 [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) 來建立部分轉碼拓撲。
5.  建立管理媒體會話的 helper 物件。  (參閱媒體會話協助程式) 。
6.  執行編碼會話，並等候它完成。  (參閱 [執行編碼會話](#run-the-encoding-session)。 ) 
7.  呼叫 [**IMFMediaSource：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) 以關閉媒體來源。
8.  發行介面指標。 此程式碼會使用 [SafeRelease](saferelease.md) 函式來釋放介面指標。 另一個選項是使用 COM 智慧型指標類別，例如 **CComPtr**。

### <a name="create-the-media-source"></a>建立媒體來源

媒體來源是讀取和剖析輸入檔的物件。 若要建立媒體來源，請將輸入檔的 URL 傳遞至 [來源解析程式](source-resolver.md)。 下列程式碼示範如何執行這項操作。


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



如需詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。

### <a name="get-the-source-duration"></a>取得來源持續時間

雖然並非必要，但在輸入檔案期間查詢媒體來源會很有用。 這個值可以用來追蹤編碼進度。 持續時間會儲存在展示描述項的 [ [**MF \_ PD \_ 持續時間**](mf-pd-duration-attribute.md) ] 屬性中。 藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)來取得簡報描述項。


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



### <a name="create-the-transcode-profile"></a>建立轉碼設定檔

轉碼設定檔會描述編碼參數。 如需建立轉碼設定檔的詳細資訊，請參閱 [使用轉碼 API](fast-transcode-objects.md)。 若要建立設定檔，請執行下列步驟。

1.  呼叫 [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) 以建立空的設定檔。
2.  建立 AAC 音訊串流的媒體類型。 藉由呼叫 [**IMFTranscodeProfile：： SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)將其新增至設定檔。
3.  建立 h.264 影片串流的媒體類型。 藉由呼叫 [**IMFTranscodeProfile：： SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)將其新增至設定檔。
4.  呼叫 [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) 來建立容器層級屬性的屬性存放區。
5.  設定 [ [MF \_ 轉碼 \_ CONTAINERTYPE](mf-transcode-containertype.md) ] 屬性。 這是唯一需要的容器層級屬性。 若為設定檔輸出，請將此屬性設定為 **MFTranscodeContainerType \_ MPEG4**。
6.  呼叫 [**IMFTranscodeProfile：： SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) 來設定容器層級的屬性。

下列程式碼顯示這些步驟。


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



若要指定 h.264 影片資料流程的屬性，請建立屬性存放區，並設定下列屬性：



| 屬性                                                       | 描述                      |
|-----------------------------------------------------------------|---------------------------------|
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)              | 設定為 **MFVideoFormat \_ H264**。 |
| [**MF \_ MT \_ MPEG2 \_ 設定檔**](mf-mt-mpeg2-profile-attribute.md) | H.264 設定檔。                  |
| [**MF \_ MT \_ 框架 \_ 大小**](mf-mt-frame-size-attribute.md)       | 框架大小。                     |
| [**MF \_ MT \_ 幀 \_ 速率**](mf-mt-frame-rate-attribute.md)       | 畫面播放速率。                     |
| [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md)     | 編碼的位元速率。               |



 

若要指定 AAC 音訊資料流程的屬性，請建立屬性存放區，並設定下列屬性：



| 屬性                                                                                      | 描述                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)                                             | 設定為 **MFAudioFormat \_ AAC**            |
| [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)        | 音訊取樣率。                       |
| [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)              | 每個音訊範例的位數。                   |
| [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)                     | 音訊聲道數目。                |
| [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 編碼的位元速率。                        |
| [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)               | 設定為 1。                                |
| [MF \_ MT \_ AAC \_ 音訊 \_ 設定檔 \_ 層級 \_ 指示](mf-mt-aac-audio-profile-level-indication.md) | AAC 設定檔層級指示 (選擇性) 。 |



 

下列程式碼會建立影片資料流程屬性。


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



下列程式碼會建立音訊資料流程屬性。


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



請注意，轉碼 API 不需要真正的媒體類型，不過它會使用媒體類型的屬性。 尤其是，因為 [**SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)和 [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)方法意指主要型別，所以不需要 [**MF \_ MT \_ 主要 \_ 型**](mf-mt-major-type-attribute.md)別屬性。 不過，它也是將實際的媒體類型傳遞給這些方法的有效方式。 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)介面 (繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)) 。

### <a name="run-the-encoding-session"></a>執行編碼會話

下列程式碼會執行編碼會話。 它會使用 Media Session helper 類別，如下一節所示。


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



## <a name="media-session-helper"></a>媒體會話協助程式

本檔的[媒體基礎架構](media-foundation-architecture.md)一節中會更完整地說明[媒體會話](media-session.md)。 媒體會話使用非同步事件模型。 在 GUI 應用程式中，您應該在不封鎖 UI 執行緒等候下一個事件的情況下，回應會話事件。 教學課程 [如何播放未受保護的媒體](how-to-play-unprotected-media-files.md) 檔案示範如何在播放應用程式中進行此操作。 針對編碼，原則是相同的，但事件較少：



| 事件                                  | 描述                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | 在編碼完成時引發。                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | [**IMFMediaSession：： Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close)方法完成時引發。 引發此事件之後，就可以安全地關閉媒體會話。 |



 

若為主控台應用程式，則可合理地封鎖和等候事件。 根據來源檔案和編碼設定，可能需要一些時間才能完成編碼。 您可以取得進度更新，如下所示：

1.  呼叫 [**IMFMediaSession：： GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) 以取得簡報時鐘。
2.  查詢 [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) 介面的時鐘。
3.  呼叫 [**IMFPresentationClock：： GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) 以取得目前的位置。
4.  位置會以時間單位來指定。 若要取得已完成的百分比，請使用此值 `(100 * position) / duration` 。

以下是類別的宣告 `CSession` 。


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



下列程式碼顯示類別的完整實作為 `CSession` 。


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AAC 編碼器**](aac-encoder.md)
</dt> <dt>

[**H.264 影片編碼器**](h-264-video-encoder.md)
</dt> <dt>

[媒體會話](media-session.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> <dt>

[轉碼 API](transcode-api.md)
</dt> </dl>

 

 
