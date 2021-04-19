---
description: 建立 ASF 檔案的其中一種方式是從現有的檔案複製 ASF 資料流程。
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 教學課程：使用 WMContainer 物件複製 ASF 資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978887"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>教學課程：使用 WMContainer 物件複製 ASF 資料流程

建立 ASF 檔案的其中一種方式是從現有的檔案複製 ASF 資料流程。 若要這樣做，您可以從來源檔案取出媒體資料，然後寫入輸出檔。 如果來源檔案是 ASF 檔案，您可以複製 stream 範例，而不需要解壓縮並 recompressing 它們。

本教學課程會示範此案例，方法是將 ASF 音訊影片檔案中的第一個音訊串流解壓縮 ( .wmv) ，並將它複製到新的 ASF 音訊檔案 ( .wma) 。 在本教學課程中，您將建立主控台應用程式，以將輸入和輸出檔案名視為引數。 應用程式會使用 ASF 分隔器來剖析輸入資料流程範例，然後將它們傳送給 ASF 多工器，以寫入音訊串流的 ASF 資料封包。

本教學課程包含下列步驟：

-   [先決條件](#prerequisites)
-   [術語](#terminology)
-   [1. 設定專案](#1-set-up-the-project)
-   [2. 宣告 Helper 函數](#2-declare-helper-functions)
-   [3. 開啟輸入 ASF 檔案](#3-open-the-input-asf-file)
-   [4. 初始化輸入檔的物件](#4-initialize-objects-for-the-input-file)
-   [5. 建立音訊設定檔](#5-create-an-audio-profile)
-   [6. 初始化輸出檔案的物件](#6-initialize-objects-for-the-output-file)
-   [7. 產生新的 ASF 資料封包](#7-generate-new-asf-data-packets)
-   [8. 在新檔案中寫入 ASF 物件](#8-write-the-asf-objects-in-the-new-file)
-   [9撰寫 Entry-Point 函式](#9-write-the-entry-point-function)
-   [相關主題](#related-topics)

## <a name="prerequisites"></a>必要條件

本教學課程假設您已句備下列條件：

-   您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。 這些元件包括 ContentInfo、分隔器、多工器和設定檔物件。 如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。
-   您已熟悉剖析 ASF 標頭物件和現有檔案的 ASF 資料封包，以及使用分隔器產生壓縮資料流程範例的程式。 如需詳細資訊，請參閱 [教學課程：讀取 ASF](tutorial--reading-an-asf-file.md)檔。
-   您熟悉媒體緩衝區和位元組資料流程：具體而言，使用位元組資料流程的檔案作業，以及將媒體緩衝區的內容寫入位元組資料流程中。  (請參閱 [2。宣告 Helper 函數](#2-declare-helper-functions)。 ) 

## <a name="terminology"></a>詞彙

本教學課程使用下列詞彙：

-   來源位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸入檔的內容。
-   來源 ContentInfo 物件： ContentInfo 物件會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸入檔的 ASF 標頭物件。
-   音訊設定檔：設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面，其中只包含輸入檔的音訊資料流程。
-   資料流程範例：媒體範例（公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面）由分隔器產生，代表從輸入檔以壓縮狀態取得的選定資料流程媒體資料。
-   Output ContentInfo object： ContentInfo 物件會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸出檔案的 ASF 標頭物件。
-   資料位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，此介面代表輸出檔案的整個 ASF 資料物件部分。
-   資料封包：媒體範例（公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面）由多工器所產生，代表將寫入資料位元組資料流程的 ASF 資料封包。
-   輸出位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸出檔的內容。

## <a name="1-set-up-the-project"></a>1. 設定專案

在原始程式檔中包含下列標頭：


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



連結至下列程式庫檔案：

-   mfplat .lib
-   mf .lib
-   mfuuid .lib

宣告 [SafeRelease](saferelease.md) 函數：


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



## <a name="2-declare-helper-functions"></a>2. 宣告 Helper 函數

本教學課程會使用下列 helper 函式，從位元組資料流程讀取和寫入。

`AllocReadFromByteStream`函數會從位元組資料流程讀取資料，並配置新的媒體緩衝區來保存資料。 如需詳細資訊，請參閱 [**IMFByteStream：： Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read)。


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



函數會將 `WriteBufferToByteStream` 資料從媒體緩衝區寫入位元組資料流程。 如需詳細資訊，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。


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



函數會將 `AppendToByteStream` 一個位元組資料流程的內容附加至另一個位元組資料流程：


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



## <a name="3-open-the-input-asf-file"></a>3. 開啟輸入 ASF 檔案

藉由呼叫 [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) 函數來開啟輸入檔。 方法會傳回位元組資料流程物件的指標，其中包含檔案的內容。 檔案名是由使用者透過應用程式的命令列引數所指定。

下列程式碼範例會採用檔案名，並將指標傳回給可用來讀取檔案的位元組資料流程物件。


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. 初始化輸入檔的物件

接下來，您將建立並初始化來源 ContentInfo 物件和分隔器，以產生資料流程範例。

在步驟2中建立的這個來源位元組資料流程將用來剖析 ASF 標頭物件，並填入來源 ContentInfo 物件。 此物件將用來初始化分隔器，以協助剖析輸入檔中音訊資料流程的 ASF 資料封包。 您也會取出輸入檔中的 ASF 資料物件長度，以及相對於檔開頭的第一個 ASF 資料封包的位移。 分隔器會使用這些屬性來產生音訊串流範例。

建立並初始化輸入檔的 ASF 元件：

1.  呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立 ContentInfo 物件。 此函數會傳回 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面的指標。
2.  呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 來剖析 ASF 標頭。 如需此步驟的詳細資訊，請參閱 [讀取現有檔案的 ASF 標頭物件](reading-the-asf-header-object-of-an-existing-file.md)。
3.  呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 來建立 ASF 分隔器物件。 此函數會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標。
4.  呼叫 [**IMFASFSplitter：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize)，傳入 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標。 如需此步驟的詳細資訊，請參閱 [建立 ASF 分隔器物件](creating-the-asf-splitter-object.md)。
5.  呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) 來取得 ASF 檔案的表示描述項。
6.  從表示描述項取得 [ [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md) ] 屬性的值。 此值是檔案中 ASF 資料物件的位置，以位元組位移的形式從檔案開頭開始。
7.  從表示描述項取得 [ [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md) ] 屬性的值。 此值為 ASF 資料物件的總大小（以位元組為單位）。 如需詳細資訊，請參閱 [從 ASF 標頭物件取得資訊](getting-information-from-asf-header-objects.md)。

下列範例程式碼顯示合併所有步驟的函式。 此函式會接受來源位元組資料流程的指標，並傳回來源 ContentInfo 物件和分隔器的指標。 此外，它也會接收 ASF 資料物件的長度和位移。


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a>5. 建立音訊設定檔

接下來，您將會從來源 ContentInfo 物件取得輸入檔的設定檔物件。 接著，您將設定設定檔，使其只包含輸入檔的音訊資料流程。 若要這樣做，請列舉資料流程並從設定檔中移除非音訊串流。 本教學課程稍後將使用音訊設定檔物件來初始化輸出 ContentInfo 物件。

建立音訊設定檔

1.  藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)，從來源 ContentInfo 物件取得輸入檔的設定檔物件。 方法會傳回設定檔物件的指標，其中包含輸入檔中的所有資料流程。 如需詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。
2.  從設定檔中移除任何相互排除的物件。 這是必要步驟，因為非音訊串流將會從設定檔中移除，這可能會使相互排除物件失效。
3.  移除設定檔中的所有非音訊串流，如下所示：
    -   呼叫 [**IMFASFProfile：： GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) 來取得資料流程數目。
    -   在迴圈中，呼叫 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) ，以依索引取得每個資料流程。
    -   呼叫 [**IMFASFStreamConfig：： GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) 以取得資料流程類型。
    -   若為非音訊資料流程，請呼叫 [**IMFASFProfile：： RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) 來移除資料流程。
4.  儲存第一個音訊串流的串流編號。 這將會在分隔器上選取，以產生資料流程範例。 如果資料流程號碼為零，則呼叫端可以假設沒有音訊資料流程檔案。

下列程式碼會執行這些步驟：


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



`RemoveMutexes`函數會從設定檔中移除任何互斥物件：


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a>6. 初始化輸出檔案的物件

接下來，您將建立輸出 ContentInfo 物件和多工器，以產生輸出檔的資料封包。

在步驟4中建立的音訊設定檔將用來填入輸出 ContentInfo 物件。 此物件包含通用檔案屬性和資料流程屬性等資訊。 輸出 ContentInfo 物件將用來初始化多工器，這些多工器會產生輸出檔的資料封包。 產生資料封包之後，必須更新 ContentInfo 物件，以反映新的值。

建立和初始化輸出檔案的 ASF 元件

1.  藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立空的 ContentInfo 物件，並在其中填入在步驟3中建立之音訊設定檔的資訊，方法是呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)。 如需詳細資訊，請參閱 [初始化新 ASF 檔案的 ContentInfo 物件](initializing-the-contentinfo-object-of-a-new-asf-file.md)。
2.  使用 output ContentInfo 物件來建立和初始化多工器物件。 如需詳細資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)。

下列範例程式碼顯示可合併步驟的函式。 此函式會接受設定檔物件的指標，並傳回輸出 ContentInfo 物件和多工器的指標。


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a>7. 產生新的 ASF 資料封包

接下來，您將使用分隔器從來源位元組資料流程產生音訊串流範例，並將它們傳送至多工器，以建立 ASF 資料封包。 這些資料封包將構成新檔案的最終 ASF 資料物件。

產生音訊串流範例

1.  藉由呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)，在分隔器上選取第一個音訊串流。
2.  從來源位元組串流將固定大小的媒體資料區塊讀取至媒體緩衝區。
3.  藉由在迴圈中呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) ，在迴圈中呼叫：：，以將資料流程範例收集為媒體範例，只要它收到 \_ \_ *pdwStatusFlags* 參數中的 ASF STATUSFLAGS 不完整旗標即可。 如需詳細資訊，請參閱 [從現有的 Asf 資料物件產生資料流程範例](generating-stream-samples-from-an-existing-asf-data-object.md)中，產生 asf 資料封包的範例。
4.  針對每個媒體範例，呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，將媒體範例傳送至多工器。 多工器會產生 ASF 資料物件的資料封包。
5.  將多工器產生的資料封包寫入資料位元組資料流程。
6.  產生所有的資料封包之後，請呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) ，以在 ASF 資料封包產生期間所收集的資訊來更新輸出 ContentInfo 物件。

下列程式碼範例會從 ASF 分隔器產生串流範例，並將它們傳送至多工器。 多工器會產生 ASF 資料封包，並將其寫入資料流程。


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



為了取得來自 ASF 分隔器的封包，先前的程式碼會呼叫函式 `GetPacketsFromSplitter` ，如下所示：


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



函數會從多工器 `GenerateDataPackets` 取得資料封包。 如需詳細資訊，請參閱 [取得 ASF 資料封包](generating-new-asf-data-packets.md)。


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. 在新檔案中寫入 ASF 物件

接下來，您會呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)，將輸出 ContentInfo 物件的內容寫入媒體緩衝區。 這個方法會將儲存在 ContentInfo 物件中的資料，轉換成 ASF 標頭物件格式的二進位資料。 如需詳細資訊，請參閱 [產生新的 ASF 標頭物件](generating-a-new-asf-header-object.md)。

在產生新的 ASF 標頭物件之後，先將標頭物件寫入至步驟2中建立的輸出位元組資料流程（藉由呼叫 helper 函數 WriteBufferToByteStream），以寫入輸出檔。 使用包含在資料位元組資料流程中的資料物件來追蹤標頭物件。 範例程式碼會示範將資料位元組資料流程的內容傳送至輸出位元組資料流程的函式。


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a>9撰寫 Entry-Point 函式

現在您可以將先前的步驟結合成完整的應用程式。 使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。 當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。 如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。

下列程式碼顯示完整的主控台應用程式。 命令列引數會指定要轉換的檔案名和新音訊檔案的名稱。


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
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

 

 



