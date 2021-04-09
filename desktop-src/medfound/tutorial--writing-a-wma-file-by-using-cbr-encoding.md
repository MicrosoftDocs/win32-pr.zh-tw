---
description: 本教學課程示範如何將非壓縮)  ( 音訊檔案中的媒體內容解壓縮，以將新的音訊檔 ( .wma) ，然後以 ASF 格式將其壓縮。
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 教學課程：使用 WMContainer 物件撰寫 WMA 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848700"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>教學課程：使用 WMContainer 物件撰寫 WMA 檔案

本教學課程示範如何將非壓縮)  ( 音訊檔案中的媒體內容解壓縮，以將新的音訊檔 ( .wma) ，然後以 ASF 格式將其壓縮。 轉換所使用的編碼模式是 (CBR) 的 [固定位速率編碼](constant-bit-rate-encoding.md) 。 在此模式中，應用程式會在編碼會話之前，指定編碼器必須達到的目標位元速率。

在本教學課程中，您將建立主控台應用程式，以將輸入和輸出檔案名視為引數。 應用程式會從 wave 檔案剖析應用程式取得未壓縮的媒體範例，此應用程式會在本教學課程中提供。 這些範例會傳送至編碼器，以轉換成 Windows Media 音訊9格式。 編碼器是針對 CBR 編碼進行設定，並使用在媒體類型協商期間可用的第一個位元速率做為目標位元速率。 編碼的範例會傳送至多工器，以取得 ASF 資料格式的 packetization。 這些封包將會寫入代表 ASF 資料物件的位元組資料流程。 在 [資料] 區段就緒之後，您將建立一個 ASF 音訊檔案，並撰寫新的 ASF 標頭物件來合併所有標頭資訊，然後附加 ASF 資料物件位元組資料流程。

本教學課程包含下列各節：

-   [先決條件](#prerequisites)
-   [術語](#terminology)
-   [1. 設定專案](#1-set-up-the-project)
-   [2. 宣告 Helper 函數](#2-declare-helper-functions)
-   [3. 開啟音訊檔案](#3-open-an-audio-file)
-   [4. 設定編碼器](#4-configure-the-encoder)
-   [5. 建立 ASF ContentInfo 物件。](#5-create-the-asf-contentinfo-object)
-   [6. 建立 ASF 多工器](#6-create-the-asf-multiplexer)
-   [7. 產生新的 ASF 資料封包](#7-generate-new-asf-data-packets)
-   [8. 寫入 ASF 檔案](#8-write-the-asf-file)
-   [9. 定義 Entry-Point 函數](#9-define-the-entry-point-function)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本教學課程假設您已句備下列條件：

-   您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。 這些元件包括 ContentInfo、分隔器、多工器和設定檔物件。 如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。
-   您熟悉 Windows Media 編碼器以及各種編碼類型，尤其是 CBR。 如需詳細資訊，請參閱 [Windows Media 編碼器](windows-media-encoders.md) 。
-   您熟悉 [媒體緩衝區](media-buffers.md) 和位元組資料流程：具體而言，使用位元組資料流程的檔案作業，以及將媒體緩衝區的內容寫入位元組資料流程。

## <a name="terminology"></a>詞彙

本教學課程使用下列詞彙：

-   來源媒體類型：媒體類型物件會公開 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面，此介面會描述輸入檔的內容。
-   音訊設定檔：設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面，其中只包含輸出檔案的音訊資料流程。
-   資料流程範例：媒體範例會公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面，代表從編碼器以壓縮狀態取得的輸入檔媒體資料。
-   ContentInfo 物件： [ASF ContentInfo 物件](asf-contentinfo-object.md)會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸出檔案的 ASF 標頭物件。
-   資料位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，此介面代表輸出檔案的整個 ASF 資料物件部分。
-   資料封包：媒體範例會公開由 [ASF](asf-multiplexer.md)多工器產生的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)介面;表示將寫入資料位元組資料流程的 ASF 資料封包。
-   輸出位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸出檔的內容。

## <a name="1-set-up-the-project"></a>1. 設定專案

1.  在原始程式檔中包含下列標頭：

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  連結至下列程式庫檔案：

    -   mfplat .lib
    -   mf .lib
    -   mfuuid .lib

3.  宣告 [SafeRelease](saferelease.md) 函數。
4.  在您的專案中包含 CWmaEncoder 類別。 如需此類別的完整原始碼，請參閱 [編碼器範例程式碼](encoder-example-code.md)。

## <a name="2-declare-helper-functions"></a>2. 宣告 Helper 函數

本教學課程會使用下列 helper 函式，從位元組資料流程讀取和寫入。

-   `AppendToByteStream`：將一個位元組資料流程的內容附加至另一個位元組資料流程。
-   WriteBufferToByteStream：將資料從媒體緩衝區寫入位元組資料流程。

如需詳細資訊，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。 下列程式碼顯示這些 helper 函式：


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a>3. 開啟音訊檔案

本教學課程假設您的應用程式將會產生未壓縮的音訊進行編碼。 基於這個目的，本教學課程中會宣告兩個函數：


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



這些函式的實作為讀者。

-   函式 `OpenAudioFile` 應該會開啟 *pszURL* 所指定的媒體檔案，並傳回描述音訊串流之媒體類型的指標。
-   `GetNextAudioSample`函數應該從開啟的檔案讀取未壓縮的 PCM 音訊 `OpenAudioFile` 。 到達檔案結尾時， *pbEOS* 會收到值 **TRUE**。 否則， *ppSample* 會收到包含音訊緩衝區的媒體範例。

## <a name="4-configure-the-encoder"></a>4. 設定編碼器

接著，建立編碼器、設定它以產生 CBR 編碼的資料流程範例，並協商輸入和輸出媒體類型。

在媒體基礎中，編碼器 (公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面) 會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。

在本教學課程中，會在為 MFT 提供包裝函式的類別中實作為編碼器 `CWmaEncoder` 。 如需此類別的完整原始碼，請參閱 [編碼器範例程式碼](encoder-example-code.md)。

> [!Note]  
> 您可以選擇性地將編碼類型指定為 CBR。 根據預設，編碼器會設定為使用 CBR 編碼。 如需詳細資訊，請參閱 [常數位元速率編碼](constant-bit-rate-encoding.md)。 您可以設定其他屬性，視編碼類型而定，如需編碼模式特定屬性的相關資訊，請參閱 [品質型變數位速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)、不受限制的變數位 [速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)，以及 [尖峰限制的變數位元速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md)。

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a>5. 建立 ASF ContentInfo 物件。

[ASF ContentInfo 物件](asf-contentinfo-object.md)包含輸出檔案中各種標頭物件的相關資訊。

首先，建立音訊串流的 ASF 設定檔：

1.  呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 來建立空白的 ASF 設定檔物件。 ASF 設定檔會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。 如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。
2.  從物件取得編碼的音訊格式 `CWmaEncoder` 。
3.  呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) ，以建立適用于 ASF 設定檔的新資料流程。 傳入 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標，代表資料流程格式。
4.  呼叫 [**IMFASFStreamConfig：： SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) 以指派資料流程識別碼。
5.  藉由在資料流程物件上設定 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性，設定 "有漏洞 bucket" 參數。
6.  呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) ，將新的資料流程新增至設定檔。

現在建立 ASF ContentInfo 物件，如下所示：

1.  呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。
2.  呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 來設定 ASF 設定檔。

下列程式碼顯示這些步驟：


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a>6. 建立 ASF 多工器

[Asf](asf-multiplexer.md)多工器會產生 asf 資料封包。

1.  呼叫 [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) 來建立 ASF 多工器。
2.  呼叫 [**IMFASFMultiplexer：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) 以初始化多工器。 傳入在上一節中建立之 ASF 內容資訊物件的指標。
3.  呼叫 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) 來設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標。 使用此設定時，多工器會自動調整 ASF 內容的位元速率，以符合多工處理的資料流程特性。


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. 產生新的 ASF 資料封包

接下來，為新檔案產生 ASF 資料封包。 這些資料封包將構成新檔案的最終 ASF 資料物件。 若要產生新的 ASF 資料封包：

1.  呼叫 [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) 以建立暫存位元組資料流程來保存 ASF 資料封包。
2.  呼叫應用程式定義的 `GetNextAudioSample` 函數，以取得編碼器的未壓縮音訊資料。
3.  將未壓縮的音訊傳遞給編碼器進行壓縮。 如需詳細資訊，請參閱在[編碼器中處理資料](processing-data-in-the-encoder.md)。
4.  呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 將壓縮的音訊範例傳送至適用于 PACKETIZATION 的 ASF 多工器。
5.  從多工器取得 ASF 封包，並將它們寫入暫存位元組資料流程。 如需詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。
6.  當您到達來來源資料流的結尾時，請清空編碼器，並從編碼器提取剩餘的壓縮樣本。 如需有關清空 MFT 的詳細資訊，請參閱 [基本的 Mft 處理模型](basic-mft-processing-model.md)。
7.  所有範例都傳送至多工器之後，請呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) ，然後從多工器提取其餘的 ASF 封包。
8.  呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end)。

下列程式碼會產生 ASF 資料封包。 函數會傳回包含 ASF 資料物件的位元組資料流程指標。


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



函式的 `GenerateASFDataPackets` 程式碼會顯示在 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)的主題中。

## <a name="8-write-the-asf-file"></a>8. 寫入 ASF 檔案

接下來，呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)，將 ASF 標頭寫入媒體緩衝區。 這個方法會將儲存在 ContentInfo 物件中的資料，轉換成 ASF 標頭物件格式的二進位資料。 如需詳細資訊，請參閱 [產生新的 ASF 標頭物件](generating-a-new-asf-header-object.md)。

產生新的 ASF 標頭物件之後，請建立輸出檔案的位元組資料流程。 首先，將標頭物件寫入輸出位元組資料流程。 使用包含在資料位元組資料流程中的資料物件來追蹤標頭物件。


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a>9. 定義 Entry-Point 函數

現在您可以將先前的步驟結合成完整的應用程式。 使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。 當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。 如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。

下列程式碼顯示完整的主控台應用程式。 命令列引數會指定要轉換的檔案名和新音訊檔案的名稱。


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMContainer ASF 元件](wmcontainer-asf-components.md)
</dt> <dt>

[媒體基礎中的 ASF 支援](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



