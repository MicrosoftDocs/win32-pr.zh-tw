---
description: 編碼是指將數位媒體從一種格式轉換成另一種格式的程式。 例如，將 MP3 音訊轉換成 Advanced Systems 格式所定義的 Windows Media 音訊格式 (ASF) 規格。
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 教學課程： 1-傳遞 Windows Media 編碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103696262"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>教學課程： 1-傳遞 Windows Media 編碼

編碼是指將數位媒體從一種格式轉換成另一種格式的程式。 例如，將 MP3 音訊轉換成 Advanced Systems 格式所定義的 Windows Media 音訊格式 (ASF) 規格。

**注意**  ASF 規格會定義輸出檔的容器類型 ( .wma 或 .wmv) 可包含任何格式、壓縮或未壓縮的媒體資料。 例如，一個 ASF 容器（例如 .wma 檔）可以包含 MP3 格式的媒體資料。 編碼程式會轉換檔案中包含的實際資料格式。

本教學課程示範如何將純 (的非 DRM 保護) 輸入來源編碼為 Windows Media 內容，並將資料寫入新的 ASF 檔案 ( \* 使用管線層級 ASF 元件) wm。 這些元件將用來建立部分編碼拓撲，這會由媒體會話的實例控制。

在本教學課程中，您將建立主控台應用程式，該應用程式會採用輸入和輸出檔案名，並使用編碼模式作為引數。 輸入檔案可以是壓縮或未壓縮的媒體格式。 有效的編碼模式為 "CBR" (常數位元速率) 或 "VBR" (變數位元速率) 。 應用程式會建立媒體來源以代表輸入檔案名所指定的來源，以及使用 ASF 檔案接收，將原始程式檔的編碼內容封存到 ASF 檔案中。 為了讓案例更容易執行，輸出檔只會有一個音訊串流和一個影片串流。 應用程式會插入適用于音訊串流格式轉換的 Windows Media 音訊 9.1 Professional 編解碼器，以及適用于影片串流的 Windows Media 視訊9編解碼器。

針對常數的位元速率編碼，編碼會話開始之前，編碼器必須知道它必須達到的目標位元速率。 在本教學課程中，針對「CBR」模式，應用程式會使用在媒體類型協商期間從編碼器抓取的第一個輸出媒體類型所提供的位元速率，以做為目標位元速率。 針對變數位元速率編碼，本教學課程會藉由設定品質等級來示範如何使用變數位元速率進行編碼。 音訊串流的編碼品質為98，而視頻串流的品質等級為95。

下列程式摘要說明在 ASF 容器中使用1傳遞編碼模式來編碼 Windows Media 內容的步驟。

1.  使用來源解析程式建立所指定的媒體來源。
2.  列舉媒體來源中的串流。
3.  根據媒體來源中需要編碼的資料流程，建立 ASF 媒體接收器並新增資料流程接收器。
4.  使用必要的編碼屬性來設定媒體接收器。
5.  在輸出檔中建立資料流程的 Windows Media 編碼器。
6.  使用在媒體接收上設定的屬性來設定編碼器。
7.  建立部分編碼拓撲。
8.  將媒體會話具現化，並在媒體會話上設定拓撲。
9.  藉由控制媒體會話並從媒體會話取得所有相關事件，來啟動編碼會話。
10. 針對 VBR 編碼，從編碼器取得編碼屬性值，並在媒體接收器上進行設定。
11. 關閉並關閉編碼會話。

本教學課程包含下列各節：

-   [先決條件](#prerequisites)
-   [設定專案](#set-up-the-project)
-   [建立媒體來源](#create-the-media-source)
-   [建立 ASF File 接收器](#create-the-asf-file-sink)
    -   [建立 ASF 設定檔物件](#create-the-asf-profile-object)
    -   [建立壓縮的音訊媒體類型](#create-a-compressed-audio-media-type)
    -   [建立壓縮的影片媒體類型](#create-a-compressed-video-media-type)
    -   [建立 ASF ContentInfo 物件](#create-the-asf-contentinfo-object)
    -   [建立 ASF File 接收器](#create-the-asf-file-sink)
-   [建立部分編碼拓撲](#build-the-partial-encoding-topology)
    -   [建立媒體來源的來源拓撲節點](#create-the-source-topology-node-for-the-media-source)
    -   [具現化所需的編碼器，並建立轉換節點](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [建立檔案接收的輸出拓撲節點](#create-the-output-topology-nodes-for-the-file-sink)
    -   [連接來源、轉換和接收節點](#connect-the-source-transform-and-sink-nodes)
-   [處理編碼會話](#handling-the-encoding-session)
-   [更新 File 接收器中的編碼屬性](#update-encoding-properties-in-the-file-sink)
-   [執行 Main](#implement-main)
-   [測試輸出檔案](#test-the-output-file)
-   [常見的錯誤碼和調試秘訣](#common-error-codes-and-debugging-tips)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本教學課程假設您已句備下列條件：

-   您已熟悉 Asf 檔案 [結構](asf-file-structure.md)，媒體基礎提供的 [管線層 ASF 元件](pipeline-layer-asf-components.md) ，可與 asf 物件搭配使用。 這些元件包括下列物件：
    -   [媒體來源](media-sources.md)

        **注意**  如果您正在執行 transrating (將較高的位元速率檔案轉換成較低的位元速率檔案，而不變更) 的格式，則會使用 [ASF 媒體來源](asf-media-source.md)。

    -   [Windows Media 編碼器](windows-media-encoders.md)
    -   [ASF 媒體接收](asf-media-sinks.md)
    -   [ASF ContentInfo 物件](asf-contentinfo-object.md)
    -   [ASF 設定檔](asf-profile.md)

-   您已熟悉 Windows Media 編碼器，以及各種編碼類型，尤其是 [常數的位元速率編碼](constant-bit-rate-encoding.md) 和 [品質型變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)。
-   您已熟悉編碼器 MFT 作業。 具體而言，就是建立編碼器的實例，並在編碼器上設定輸入和輸出類型。
-   您已熟悉拓撲物件，以及如何建立編碼拓撲。 如需拓撲與拓撲節點的詳細資訊，請參閱 [建立拓撲](creating-topologies.md)。
-   您已熟悉 [媒體會話](media-session.md)的事件模型和流程式控制製作業。 如需詳細資訊，請參閱 [媒體會話事件](media-session-events.md)。

## <a name="set-up-the-project"></a>設定專案

1.  在原始程式檔中包含下列標頭：

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  連結至下列程式庫檔案：

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  宣告 [SafeRelease](saferelease.md) 函數。

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  宣告編碼 \_ 模式列舉來定義 CBR 和 VBR 編碼類型。

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  為影片資料流程定義緩衝區視窗的常數。

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>建立媒體來源

建立輸入來源的媒體來源。 媒體基礎提供各種媒體格式的內建媒體來源： MP3、3GP、AVI/WAVE。 如需媒體基礎所支援之格式的相關資訊，請參閱 [媒體基礎中支援的媒體格式](supported-media-formats-in-media-foundation.md)。

若要建立媒體來源，請使用 [來源解析程式](source-resolver.md)。 這個物件會分析針對原始程式檔所指定的 URL，並建立適當的媒體來源。

進行下列呼叫：

-   [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    如需這些呼叫的詳細資訊，請參閱 [使用來源解析程式](using-the-source-resolver.md)。

    如果您的輸入檔是 ASF 格式，而且您想要將它轉換成不同的位元速率檔案而不變更格式，來源規劃求解會建立 [Asf 媒體來源](asf-media-source.md)的實例。

下列程式碼範例顯示的函式 CreateMediaSource 會建立指定檔案的媒體來源。


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>建立 ASF File 接收器

建立 ASF 檔案接收的實例，將編碼的媒體資料封存至編碼會話結尾的 ASF 檔案。

在本教學課程中，您將建立 ASF 檔案接收的啟用物件。 檔案接收需要下列資訊，才能建立必要的資料流程接收。

-   要在最後一個檔案中編碼和寫入的資料流程。
-   用來編碼媒體內容的編碼屬性，例如編碼類型、編碼次數和相關屬性。
-   通用檔案屬性，指出媒體接收是否應該自動調整有漏洞值區參數 (位速率和緩衝區大小) 。

資料流程資訊是在 ASF 設定檔物件中設定，而且編碼和全域屬性是在 ASF ContentInfo 物件所管理的屬性存放區中設定。

如需 ASF 檔案接收的總覽，請參閱 [Asf 媒體接收器](asf-media-sinks.md)。

### <a name="create-the-asf-profile-object"></a>建立 ASF 設定檔物件

若要讓 ASF 檔案接收將編碼的媒體資料寫入 ASF 檔案，接收端必須知道要建立串流接收器的資料流程數目和資料流程類型。 在本教學課程中，您將從媒體來源解壓縮該資訊，並建立對應的輸出資料流程。 將您的輸出資料流程限制為一個音訊串流和一個影片串流。 針對來源中的每個選取的資料流程，建立目標資料流程並將它新增至設定檔。

若要執行此步驟，您需要下列物件。

-   [ASF 設定檔](asf-profile.md)
-   媒體來源的簡報描述項
-   媒體來源中所選取資料流程的資料流程描述項。
-   所選資料流程的媒體類型。

下列步驟說明建立 ASF 設定檔和目標資料流程的程式。

**建立 ASF 設定檔**

1.  呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 以建立空的設定檔物件。
2.  呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) ，以建立本教學課程的「建立媒體來源」一節所述步驟中所建立之媒體來源的簡報描述項。
3.  呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) 來取得媒體來源中的資料流程數目。
4.  針對媒體來源中的每個資料流程呼叫 [**IMFPresentationDescriptor：： GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) ，取得資料流程的資料流程描述項。
5.  呼叫 [**IMFStreamDescriptor：： GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) ，後面接著 [**IMFMediaTypeHandler：： GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) ，並取得資料流程的第一個媒體類型。

    **注意**   若要避免複雜的呼叫，請假設每個資料流程只有一個媒體類型，並選取資料流程的第一個媒體類型。 針對複雜的資料流程，您需要從媒體類型處理常式列舉每個媒體類型，並選擇您要編碼的媒體類型。

6.  呼叫 I [**IMFMediaType：： GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) 來取得資料流程的主要類型，以判斷資料流程是否包含音訊或影片。
7.  視資料流程的主要類型而定，建立目標媒體類型。 這些媒體類型會保存編碼器將在編碼會話期間使用的格式資訊。 本教學課程的下列各節將說明建立目標媒體類型的程式。
    -   建立壓縮的音訊媒體類型
    -   建立壓縮的影片媒體類型
8.  根據目標媒體類型建立資料流程，根據應用程式的需求設定資料流程，然後將資料流程新增至設定檔。 如需詳細資訊，請參閱 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)。

    1.  呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) ，並傳遞目標媒體類型以建立輸出資料流程。 方法會捕獲資料流程物件的 IMFASFStreamConfig 介面。
    2.  設定資料流程。
        -   呼叫 [**IMFASFStreamConfig：： SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) ，將數位指派給資料流程。 這是必要設定。
        -   藉由呼叫 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 方法和相關的資料流程設定屬性，選擇性地設定每個資料流程的有漏洞值區參數、承載延伸模組、互斥。
    3.  使用 ASF ContentInfo 物件來新增串流層級編碼屬性。 如需此步驟的詳細資訊，請參閱本教學課程中的「建立 ASF ContentInfo 物件」一節。
    4.  呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) ，將資料流程新增至設定檔。

    下列程式碼範例會建立輸出音訊串流。

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    下列程式碼範例會建立輸出影片串流。

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

    

下列程式碼範例會根據來源中的資料流程建立輸出資料流程。


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>建立壓縮的音訊媒體類型

如果您想要在輸出檔中包含音訊串流，請設定所需的屬性，藉由指定編碼類型的特性來建立音訊類型。 為確保音訊類型與 Windows Media 音訊編碼器相容，請具現化編碼器 MFT、設定編碼屬性，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)來取得媒體類型。 藉由逐一查看所有可用的類型、取得每個媒體類型的屬性，以及選取最接近您需求的類型，來取得所需的輸出類型。 在本教學課程中，從編碼器支援的輸出媒體類型清單取得第一個可用類型。

**注意**  針對 Windows 7，媒體基礎提供新的函式 [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) ，以抓取相容音訊類型的清單。 此函數只會取得 CBR 編碼的媒體類型。

完整的音訊類型必須設定下列屬性：

-   [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md)
-   [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)
-   [**MF \_ MT \_ 音訊 \_ 數目 \_ 通道**](mf-mt-audio-num-channels-attribute.md)
-   [**\_每秒的 MF MT \_ 音訊 \_ 範例 \_ \_**](mf-mt-audio-samples-per-second-attribute.md)
-   [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_每秒的 MF MT \_ 音訊 \_ 平均 \_ 位元組數 \_ \_**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_ \_ \_ \_ 每個 \_ 樣本的 MF MT 音訊位數**](mf-mt-audio-bits-per-sample-attribute.md)

下列程式碼範例會從 Windows Media 音訊編碼器取得相容的類型，以建立壓縮的音訊類型。 SetEncodingProperties 的實作為本教學課程的「建立 ASF ContentInfo 物件」一節所示。


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>建立壓縮的影片媒體類型

如果您想要在輸出檔中包含影片串流，請建立完整編碼的影片類型。 完整的媒體類型必須包含所需的位元速率和編解碼器私用資料。

有兩種方式可以建立完整的影片媒體類型。

-   建立空的媒體類型，並從來源影片類型複製媒體類型屬性，然後以 GUID 常數 MFVideoFormat WMV3 覆寫 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性 \_ 。

    完整的影片類型必須設定下列屬性：

    -   MF \_ MT \_ 主要 \_ 類型
    -   MF \_ MT \_ 子類型
    -   MF \_ MT \_ 幀 \_ 速率
    -   MF \_ MT \_ 框架 \_ 大小
    -   MF \_ MT \_ 交錯 \_ 模式
    -   MF \_ MT \_ 圖元 \_ 外觀 \_ 比例
    -   MF \_ MT \_ 平均 \_ 位元速率
    -   MF \_ MT \_ 使用者 \_ 資料

    下列程式碼範例會從來源的影片類型建立壓縮的影片類型。

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   藉由設定編碼屬性，然後呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)，從 Windows media video 編碼器取得相容的媒體類型。 這個方法會傳回部分型別。 藉由新增下列資訊，請務必將部分類型轉換成完整的類型：

    -   設定 [ [**MF \_ MT \_ 平均 \_ 位元速率**](mf-mt-avg-bitrate-attribute.md) ] 屬性中的 [影片位率]。
    -   藉由設定 [**MF \_ MT \_ 使用者 \_ 資料**](mf-mt-user-data-attribute.md) 屬性來新增編解碼器私用資料。 如需詳細指示，請參閱設定 [WMV 編碼器](configuring-a-wmv-encoder.md)中的「私用編解碼器資料」。

    因為 [**IWMCodecPrivateData：： GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) 會在傳回編解碼器私用資料之前檢查位元速率，所以請確定您在取得編解碼器私用資料之前，先設定位元速率。

    下列程式碼範例會從 Windows Media 視訊編碼器取得相容的類型，以建立壓縮的影片類型。 它也會建立未壓縮的影片類型，並將它設定為編碼器的輸入。 這會在 helper 函式 CreateUncompressedVideoType 中執行。 GetOutputTypeFromWMVEncoder 藉由新增編解碼器私用資料，將傳回的部分型別轉換成完整型別。 SetEncodingProperties 的實作為本教學課程的「建立 ASF ContentInfo 物件」一節所示。

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    下列程式碼範例會建立未壓縮的影片類型。

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    下列程式碼範例會將編解碼器私用資料新增至指定的影片媒體類型。

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>建立 ASF ContentInfo 物件

ASF ContentInfo 物件是 WMContainer 層級元件，主要是設計用來儲存 ASF 標頭物件資訊。 ASF 檔案接收會執行 ContentInfo 物件，以便將資訊儲存 (在屬性存放區中，) ，此屬性存放區會用來寫入編碼檔案的 ASF 標頭物件。 若要這樣做，您必須在啟動編碼會話之前，先在 ContentInfo 物件上建立並設定下列資訊集。

1.  呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。

    下列程式碼範例會建立空的 ContentInfo 物件。

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) ，以取得 file 接收器的資料流程層級屬性存放區。 在此呼叫中，您必須在建立 ASF 設定檔時，傳遞您為串流指派的串流號碼。
3.  在 file 接收器的資料流程屬性存放區中設定資料流程層級 [編碼屬性](configuring-the-encoder.md) 。 如需詳細資訊，請參閱在檔案接收中 [設定屬性](setting-properties-in-the-file-sink.md)的「資料流程編碼屬性」。

    下列程式碼範例會在 file 接收器的屬性存放區中設定資料流程層級屬性。

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    下列程式碼範例顯示 SetEncodingProperties 的執行。 此函式會設定 CBR 和 VBR 的資料流程層級編碼屬性。

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  呼叫 [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) 來取得 file 接收器的全域屬性存放區。 在此呼叫中，您必須在第一個參數中傳遞0。 如需詳細資訊，請參閱在檔案 [接收中設定屬性](setting-properties-in-the-file-sink.md)的「通用檔案接收屬性」。
5.  將 [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ 位元速率**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) 設定為 VARIANT \_ TRUE，以確保正確地調整 ASF 多工器的有漏洞 bucket 值。 如需此屬性的相關資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)中的「多工器初始化和有漏洞 Bucket 設定」。

    下列程式碼範例會在 file 接收器的屬性存放區中設定資料流程層級屬性。

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > 您可以在全域層級設定檔案接收的其他屬性。 如需詳細資訊，請參閱在 [ContentInfo 物件中設定屬性](setting-properties-in-the-contentinfo-object.md)（property）中的「使用編碼器設定設定 ContentInfo 物件」。

     

您將使用設定的 ASF ContentInfo 來建立 ASF 檔案接收的啟用物件 (下一節) 所述。

如果您要建立跨進程的檔案接收 ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)) ，也就是使用啟始物件，您可以使用已設定的 ContentInfo 物件，將 ASF 媒體接收器具現化， (下一節) 所述。 如果您要建立同進程檔案接收 ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)) ，而不是依照步驟1中所述建立空的 ContentInfo 物件，請在檔案接收上呼叫 **IMFMediaSink：： QueryInterface** ，以取得 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)介面的參考。 接著，您必須設定 ContentInfo 物件，如本節所述。

### <a name="create-the-asf-file-sink"></a>建立 ASF File 接收器

在本教學課程的這個步驟中，您將使用您在上一個步驟中建立的已設定 ASF ContentInfo，透過呼叫 [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) 函式來建立 asf 檔案接收的啟用物件。 如需詳細資訊，請參閱 [建立 ASF File 接收器](creating-the-asf-file-sink.md)。

下列程式碼範例會建立檔案接收的啟用物件。


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>建立部分編碼拓撲

接下來，您將建立部分編碼拓撲，方法是建立媒體來源的拓撲節點、必要的 Windows Media 編碼器，以及 ASF 檔案接收。 新增拓撲節點之後，您將連接來源、轉換和接收節點。 在新增拓撲節點之前，您必須藉由呼叫 [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)來建立空白拓撲物件。

### <a name="create-the-source-topology-node-for-the-media-source"></a>建立媒體來源的來源拓撲節點

在此步驟中，您將建立媒體來源的來源拓撲節點。

若要建立此節點，您需要下列參考：

-   您在本教學課程的「建立媒體來源」一節所述的步驟中所建立之媒體來源的指標。
-   媒體來源的簡報描述元指標。 您可以藉由呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)，取得媒體來源之 IMFPresentationDescriptor 介面的參考。
-   在此教學課程的「建立 ASF 設定檔物件」一節所述的步驟中，您已建立目標資料流程之媒體來源中每個資料流程的資料流程描述元指標。

如需有關建立來源節點和程式碼範例的詳細資訊，請參閱 [建立來源節點](creating-source-nodes.md)。

下列程式碼範例會藉由新增來源節點和必要的轉換節點來建立部分拓撲。 此程式碼會呼叫 helper 函式 AddSourceNode 和 AddTransformOutputNodes。 本教學課程稍後會包含這些函數。


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



下列程式碼範例會建立來源拓撲節點，並將其加入至編碼拓撲中。 它會採用先前拓撲物件的指標、用來列舉來來源資料流的媒體來源、媒體來源的展示描述項，以及媒體來源的資料流程描述項。 呼叫端會收到來源拓撲節點的指標。


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>具現化所需的編碼器，並建立轉換節點

媒體基礎管線不會自動插入必須編碼的資料流程所需的 Windows Media 編碼器。 應用程式必須手動新增編碼器。 若要這樣做，請在本教學課程的「建立 ASF 設定檔物件」一節所述的步驟中，列舉在您建立的 ASF 設定檔中的串流。 針對來源中的每個資料流程和設定檔中的對應資料流程，將所需的編碼器具現化。 針對此步驟，您需要在本教學課程的「建立 ASF 檔案接收」一節所述的步驟中所建立之檔案接收的啟用物件指標。

如需透過啟用物件建立編碼器的總覽，請參閱 [使用編碼器的啟用物件](using-an-encoder-s-activation-objects.md)。

下列程式說明具現化必要編碼器所需的步驟。

1.  藉由呼叫 **QueryInterface** 來取得接收之 ContentInfo 物件的參考，方法是在檔案接收啟動時呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ，然後從檔案接收查詢 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 。
2.  藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)，取得與 ContentInfo 物件相關聯的 ASF 設定檔。
3.  列舉設定檔中的資料流程。 針對這一點，您將需要串流計數和每個資料流程 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的參考。

    呼叫下列方法：

    -   [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  針對每個資料流程，從 ContentInfo 物件取得主要類型和資料流程的編碼屬性。

    呼叫下列方法：

    -   [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        針對此呼叫，您需要 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) 呼叫所取出的串流號碼。

5.  根據串流、音訊或影片的類型，藉由呼叫 [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 或 [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)，將編碼器的啟用物件具現化。

    若要呼叫這些函式，您需要下列參考：

    -   上一個步驟中由 [**IMFASFStreamConfig：： GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) 所抓取資料流程的媒體類型指標。
    -   [**IMFASFContentInfo：： GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)所抓取資料流程的編碼屬性存放區指標。 藉由將指標傳遞至屬性存放區，就會將檔案接收中設定的資料流程屬性複製到編碼器 MFT 上。

6.  更新音訊串流的有漏洞 bucket 參數。

    [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) 會針對 Windows Media 音訊編解碼器，設定基礎編碼器 MFT 的輸出類型。 設定輸出媒體類型之後，編碼器會從輸出媒體類型取得平均位元速率、計算緩衝區視窗開始風行位速率，以及設定要在編碼會話期間使用的有漏洞值區值。 您可以藉由查詢編碼器或設定自訂值，更新檔案接收中的這些值。 若要更新值，您需要下列一組資訊：

    -   平均位元速率：從在媒體類型協商期間選取的輸出媒體類型上，取得 [**MF \_ MT \_ 音訊 \_ \_ \_ 每 \_ 秒平均位元組數**](mf-mt-audio-avg-bytes-per-second-attribute.md) 屬性的平均位元速率。
    -   緩衝區視窗：您可以藉由呼叫 [**IWMCodecLeakyBucket：： GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)來取得它。
    -   初始緩衝區大小：設定為0。

    建立 Dword 陣列，並在音訊串流接收器的 [**MFPKEY \_ ASFSTREAMSINK \_ 更正 \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) 屬性中設定值。 如果您未提供更新的值，媒體會話就會適當地設定這些值。

    如需詳細資訊，請參閱 [有漏洞 Bucket 緩衝區模型](the-leaky-bucket-buffer-model.md)。

在步驟5中建立的啟用物件必須新增至拓撲，作為轉換拓撲節點。 如需詳細資訊和程式碼範例，請參閱 [建立轉換節點](creating-transform-nodes.md)中的「從啟用物件建立轉換節點」。

下列程式碼範例會建立並新增所需的編碼器啟用。 它會使用先前建立之拓撲物件的指標、檔案接收的啟用物件和來來源資料流的媒體類型。 它也會呼叫 AddOutputNode (請參閱下一個程式碼範例) ，此範例會建立接收節點並將其加入至編碼拓撲中。 呼叫端會收到來源拓撲節點的指標。


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>建立檔案接收的輸出拓撲節點

在此步驟中，您將建立 ASF 檔案接收的輸出拓撲節點。

若要建立此節點，您需要下列參考：

-   您在本教學課程的「建立 ASF 檔案接收」一節所述的步驟中所建立之啟用物件的指標。
-   用來識別已新增至檔案接收之資料流程接收器的資料流程號碼。 串流號碼符合資料流程建立時所設定的資料流程識別碼。

如需有關建立輸出節點和程式碼範例的詳細資訊，請參閱 [建立輸出節點](creating-output-nodes.md)中的「從啟用物件建立輸出節點」。

如果您不是使用檔案接收的啟用物件，您必須列舉 ASF 檔案接收中的串流接收器，並將每個資料流程接收設定為拓撲中的輸出節點。 如需資料流程接收列舉的詳細資訊，請參閱 [將資料流程資訊新增至 ASF 檔案接收](adding-stream-information-to-the-asf-file-sink.md)中的「列舉資料流程接收器」。

下列程式碼範例會建立接收節點，並將其加入至編碼拓撲。 它會使用先前建立之拓撲物件的指標、檔案接收的啟用物件和資料流程的識別碼。 呼叫端會收到來源拓撲節點的指標。


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



下列程式碼範例會列舉指定媒體接收器的資料流程接收。


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>連接來源、轉換和接收節點

在此步驟中，您會將來源節點連接到參考該編碼的轉換節點，並啟用您在本教學課程的 < 具現化必要的編碼器和建立轉換節點的步驟中所述的步驟中所建立的轉換節點。 [轉換] 節點將連接至輸出節點，其中包含 file 接收的啟用物件。

## <a name="handling-the-encoding-session"></a>處理編碼會話

在步驟中，您將執行下列步驟：

1.  呼叫 [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) 來建立編碼會話。
2.  呼叫 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 來設定會話的編碼拓撲。 如果呼叫完成，媒體會話就會評估拓撲節點，並插入其他轉換物件，例如將指定的壓縮來源轉換成未壓縮樣本的解碼器，以作為編碼器的輸入。
3.  呼叫 [**IMFMediaSession：： GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) ，以要求媒體會話所引發的事件。

    在事件迴圈中，您將會根據媒體會話所引發的事件，啟動並關閉編碼會話。 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)呼叫會產生媒體會話，並使用已設定的 MF [](mesessiontopologystatus.md) \_ TOPOSTATUS 就緒旗標來引發 MESessionTopologyStatus 事件 \_ 。 所有事件都是以非同步方式產生，而應用程式可以同步或非同步方式抓取這些事件。 因為本教學課程中的應用程式是主控台應用程式，而且封鎖使用者介面執行緒並不是問題，所以我們會以同步方式從媒體會話取得事件。

    若要以非同步方式取得事件，您的應用程式必須執行 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。 如需此介面的詳細資訊和範例執行，請參閱 [如何使用媒體基礎播放媒體](how-to-play-unprotected-media-files.md)檔案中的「處理會話事件」。

在取得媒體會話事件的事件迴圈中，等候 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)完成且拓撲已解決時所引發的 [MESessionTopologyStatus](mesessiontopologystatus.md)事件。 取得 MESessionTopologyStatus 事件時，請呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)來啟動編碼會話。 當所有編碼作業都完成時，媒體會話就會產生 [MEEndOfPresentation](meendofpresentation.md) 事件。 此事件必須針對 VBR 編碼進行處理，並在本教學課程的下一節「針對 VBR 編碼的檔案接收更新編碼屬性」中加以討論。

媒體會話會產生 ASF 標頭物件，並在編碼會話完成時完成檔案，然後引發 [MESessionClosed](mesessionclosed.md) 事件。 此事件必須透過在媒體會話執行適當的關機操作來處理。 若要開始關機作業，請呼叫 [**IMFMediaSession：： shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)。 在編碼會話關閉之後，您就無法在相同的媒體會話實例上設定另一個要進行編碼的拓朴。 若要編碼另一個檔案，必須關閉並釋放目前的媒體會話，且必須在新建立的媒體會話上設定新的拓撲。 下列程式碼範例會建立媒體會話、設定編碼拓撲，以及處理媒體會話事件。

下列程式碼範例會建立媒體會話、設定編碼拓撲，以及藉由處理來自媒體會話的事件來控制編碼會話。


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
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

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>更新 File 接收器中的編碼屬性

某些編碼屬性（例如編碼位元速率和精確的有漏洞值區值）在編碼完成之前都是未知的，特別是針對 VBR 編碼。 若要取得正確的值，應用程式必須等待 [MEEndOfPresentation](meendofpresentation.md) 事件，指出編碼會話已完成。 有漏洞值區值必須在接收中更新，如此 ASF 標頭物件才能反映正確的值。

下列程式說明在編碼拓撲中執行節點以取得 file sink 節點，並設定必要的有漏洞 bucket 屬性所需的步驟。

**更新 ASF 檔案接收的 post 編碼屬性值**

1.  呼叫 [**IMFTopology：： GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) ，以從編碼拓撲取得輸出節點集合。
2.  針對每個節點，藉由呼叫 [**IMFTopologyNode：： GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject)來取得節點中資料流程接收的指標。 在 **IMFTopologyNode：： GetObject** 傳回的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標上查詢 [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)介面。
3.  針對每個串流接收，藉由呼叫 [**IMFTopologyNode：： >getinput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput)取得下游節點 (編碼器) 。
4.  查詢節點，以從編碼器節點取得 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 指標。
5.  查詢 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標的編碼器，以從編碼器取得編碼屬性存放區。
6.  查詢 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 指標的串流接收器，以取得資料流程接收的屬性存放區。
7.  呼叫 [**IPropertyStore：： GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 以從編碼器的屬性存放區取得必要的屬性值，並藉由呼叫 **IPropertyStore：： SetValue**，將它們複製到資料流程接收器的屬性存放區。

下表顯示必須在影片資料流程的串流接收上設定的 post 編碼屬性值。



| 編碼類型                                                                                  | 屬性名稱 (GetValue)                                                                         | 屬性名稱 (SetValue)                                                                                                 |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [常數位元速率編碼](constant-bit-rate-encoding.md)                                   | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/>                                                 | MFPKEY \_ STAT \_ BAVG<br/> MFPKEY \_ STAT \_ RAVG<br/>                                                             |
| [以品質為基礎的變數位元速率編碼](quality-based-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ BAVG<br/> MFPKEY \_ RAVG<br/> MFPKEY \_ BMAX<br/> MFPKEY \_ RMAX<br/> | MFPKEY \_ STAT \_ BAVG<br/> MFPKEY \_ STAT \_ RAVG<br/> MFPKEY \_ STAT \_ BMAX<br/> MFPKEY \_ STAT \_ RMAX<br/> |



 

下列程式碼範例會設定編碼後屬性值。


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>執行 Main

下列程式碼範例顯示主控台應用程式的主要功能。


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>測試輸出檔案

下列清單描述測試編碼檔案的檢查清單。 您可以在 [檔案屬性] 對話方塊中選取這些值，方法是以滑鼠右鍵按一下編碼的檔案，然後從內容功能表中選取 [ **屬性** ]。

-   編碼檔案的路徑是正確的。
-   檔案大小超過零 KB，且播放持續時間符合原始程式檔的持續時間。
-   若為影片串流，請檢查框架寬度和高度（畫面播放速率）。 這些值應該符合您在「建立 ASF 設定檔物件」一節所述的步驟中所建立的 ASF 設定檔中所指定的值。
-   若為音訊串流，位元速率必須接近您在目標媒體類型上所指定的值。
-   在 Windows Media Player 中開啟檔案，並檢查編碼的品質。
-   在 ASFViewer 中開啟 ASF 檔案，以查看 ASF 檔案的結構。 您可以從這個 [Microsoft 網站](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)下載此工具。

## <a name="common-error-codes-and-debugging-tips"></a>常見的錯誤碼和調試秘訣

下列清單描述您可能會收到的一般錯誤碼和偵錯工具提示。

-   呼叫 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 會停止應用程式。

    藉由呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)，確定您已初始化媒體基礎平臺。 此函式會設定非同步平臺，以供所有在內部啟動非同步作業的方法（例如 [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)）使用。

-   [**IMFSourceResolver：： CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) 會傳回 HRESULT 0X80070002」，系統找不到指定的檔案。

    請確定使用者在第一個引數中所指定的輸入檔名稱是否存在。

-   HRESULT 0x80070020 「進程無法存取檔案，因為另一個進程正在使用該檔案。 "

    請確定系統中的其他資源目前並未使用輸入和輸出檔案。

-   呼叫 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 方法會傳回 MF \_ E \_ INVALIDMEDIATYPE。

    請確定下列條件成立：

    -   輸入類型或您指定的輸出類型與編碼器支援的媒體類型相容。
    -   您指定的媒體類型已完成。 若要完成媒體類型，請參閱本教學課程的「建立壓縮的音訊媒體類型」和「建立壓縮的影片媒體類型」一節中的必要屬性。
    -   請確定您已在要新增編解碼器私用資料的部分媒體類型上設定目標位速率。

-   媒體會話會 \_ \_ 在事件狀態中傳回 MF E 不支援 \_ \_ 的 D3D 類型。

    當來源的媒體類型指出 Windows Media 視訊編碼器不支援的混合交錯模式時，會傳回此錯誤。 如果您的壓縮影片媒體類型設定為使用漸進模式，則管線必須使用取消交錯轉換。 因為管線找不到符合 (此錯誤碼) 指出的相符，所以您必須手動在解碼器和編碼器節點之間插入 interlacer (轉碼 video 處理器) 。

-   媒體會話會傳回 \_ 事件狀態中的 E INVALIDARG。

    當來源的媒體類型屬性與 Windows Media 編碼器上設定之輸出媒體類型的屬性不相容時，就會傳回此錯誤。

-   [**IWMCodecPrivateData：： GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) 會傳回 HRESULT 0x80040203 「嘗試評估查詢字串時發生語法錯誤」

    請確定已在編碼器 MFT 上設定輸入類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管線層 ASF 元件](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
