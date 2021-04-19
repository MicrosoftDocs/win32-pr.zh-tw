---
description: 本教學課程說明如何使用 ASF 分隔器，從 Advanced 系統格式取得資料封包 (ASF) 檔。
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 教學課程：使用 WMContainer 物件讀取 ASF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986852"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a>教學課程：使用 WMContainer 物件讀取 ASF 檔案

本教學課程說明如何使用 [Asf 分隔器](asf-splitter.md)，從 Advanced 系統格式取得資料封包 (asf) 檔。 在本教學課程中，您將建立簡單的主控台應用程式，以讀取 ASF 檔案，並為檔案中的第一個影片串流產生壓縮媒體範例。 應用程式會顯示影片串流中主要畫面格的相關資訊。

本教學課程包含下列步驟：

-   [先決條件](#prerequisites)
-   [1. 設定專案](#1-set-up-the-project)
-   [2. 開啟 ASF 檔案](#2-open-an-asf-file)
-   [3. 讀取 ASF 標頭物件](#3-read-the-asf-header-object)
-   [4. 建立 ASF 分隔器](#4-create-the-asf-splitter)
-   [5. 選取要剖析的資料流程](#5-select-a-stream-for-parsing)
-   [6. 產生壓縮的媒體範例](#6-generate-compressed-media-samples)
-   [7. 撰寫 Entry-Point 函式](#7-write-the-entry-point-function)
-   [程式清單](#program-listing)
-   [相關主題](#related-topics)

本教學課程並未涵蓋如何解碼應用程式從 ASF 分隔器取得的壓縮資料。

## <a name="prerequisites"></a>必要條件

本教學課程假設您已句備下列條件：

-   您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。 這些元件包括 ContentInfo 物件、分隔器、多工器和設定檔。 如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。
-   您已熟悉 [媒體緩衝區](media-buffers.md) 和位元組資料流程：具體而言，使用位元組資料流程的檔案作業、從位元組資料流程讀取至媒體緩衝區，以及將媒體緩衝區的內容寫入位元組資料流程。

## <a name="1-set-up-the-project"></a>1. 設定專案

在原始程式檔中包含下列標頭：


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
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



## <a name="2-open-an-asf-file"></a>2. 開啟 ASF 檔案

接下來，藉由呼叫 [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) 函式來開啟指定的檔案。 方法會傳回位元組資料流程物件的指標，其中包含檔案的內容。 檔案名是由使用者透過應用程式的命令列引數所指定。

下列程式碼範例會採用檔案名，並將指標傳回給可用來讀取檔案的位元組資料流程物件。


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a>3. 讀取 ASF 標頭物件

接著，建立 [ASF ContentInfo 物件](asf-contentinfo-object.md) ，並使用它來剖析指定檔案的 Asf 標頭物件。 ContentInfo 物件會儲存來自 ASF 標頭的資訊，包括通用檔案屬性和每個串流的相關資訊。 您稍後會在本教學課程中使用 ContentInfo 物件來初始化 ASF 分隔器，並取得影片資料流程的串流號碼。

若要建立 ASF ContentInfo 物件：

1.  呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函數，以建立 ContentInfo 物件。 方法會傳回 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面的指標。
2.  將 ASF 檔案中的前30個位元組資料讀入媒體緩衝區。
3.  將媒體緩衝區傳遞給 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) 方法。 這個方法會傳回 ASF 檔案中標頭物件的總大小。
4.  將相同的媒體緩衝區傳遞給 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法。
5.  將標頭物件的其餘部分讀入新的媒體緩衝區。
6.  將第二個緩衝區傳遞給 [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法。 在 **ParseHeader** 的 *cbOffsetWithinHeader* 參數中指定30位元組的位移。 **ParseHeader** 方法會使用從標頭物件中包含的各種 ASF 物件收集而來的資訊，初始化 ContentInfo 物件。


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



此函式會使用函式 `ReadFromByteStream` 從位元組資料流程讀取至媒體緩衝區：


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a>4. 建立 ASF 分隔器

接下來，建立 [ASF 分隔器](asf-splitter.md) 物件。 您將使用 ASF 分隔器來剖析 ASF 資料物件，其中包含適用于 ASF 檔案的 packetized 媒體資料。

若要建立 ASF 檔案的分隔器物件：

1.  呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 函數來建立 ASF 分隔器。 函數會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標。
2.  呼叫 [**IMFASFSplitter：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 以初始化 ASF 分隔器。 這個方法會採用在程式3中建立之 ContentInfo 物件的指標。


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a>5. 選取要剖析的資料流程

接下來，列舉 ASF 檔案中的串流，然後選取第一個影片串流進行剖析。 若要列舉資料流程，您將使用 ASF 設定檔物件，並搜尋具有影片媒體類型的資料流程。

若要選取影片資料流程：

1.  在 ContentInfo 物件上呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) ，以建立 ASF 設定檔。 在其他資訊中，設定檔會描述 ASF 檔案中的資料流程。
2.  呼叫 [**IMFASFProfile：： GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) 來取得 ASF 檔案中的資料流程數目。
3.  在迴圈中呼叫 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) 來列舉資料流程。 方法會傳回 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的指標。 它也會傳回資料流程識別碼。
4.  呼叫 [**IMFASFStreamConfig：： GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) 來取得資料流程的主要類型 GUID。 如果主要型別 GUID 是 MFMediaType \_ video，資料流程就會包含影片。
5.  如果您在步驟4中找到影片資料流程，請呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) 來選取資料流程。 這個方法會接受資料流程識別碼的陣列。 在本教學課程中，陣列大小為1，因為應用程式將剖析單一資料流程。

下列範例程式碼會列舉 ASF 檔案中的資料流程，並選取 ASF 分隔器上的第一個影片資料流程：


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a>6. 產生壓縮的媒體範例

接下來，使用 ASF 分隔器來剖析 ASF 資料物件，並取得所選影片資料流程的資料封包。 應用程式會從固定大社區塊中的 ASF 檔案讀取資料，並將資料傳遞給 ASF 分隔器。 分隔器會剖析資料，並產生包含已壓縮影片資料的 [媒體範例](media-samples.md) 。 應用程式會檢查每個範例是否代表主要畫面格。 如果是，應用程式會顯示範例的一些基本資訊：

-   媒體緩衝區數目
-   資料的大小總計
-   時間戳記

若要產生壓縮的媒體範例：

1.  配置新的媒體緩衝區。
2.  從位元組資料流程將資料讀入媒體緩衝區。
3.  將媒體緩衝區傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法。 方法會剖析緩衝區中的 ASF 資料。
4.  在迴圈中，藉由呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample)從分隔器取得媒體範例。 如果 *ppISample* 參數收到有效的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標，則表示 ASF 分隔器已剖析一或多個資料封包。 如果 *ppISample* 收到 **Null** 值，請中斷迴圈，然後返回步驟1。
5.  顯示範例的相關資訊。
6.  在下列情況下，從迴圈中斷：
    -   *PpISample* 參數會接收 **Null** 值。
    -   *PdwStatusFlags* 參數未收到 **ASF \_ STATUSFLAGS \_ 不完整** 旗標。

重複這些步驟，直到到達檔案結尾為止。 下列程式碼顯示這些步驟：


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



IsKeyFrame 函式會藉由取得 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性的值，測試範例是否為主要畫面格。


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



為了方便說明，本教學課程會藉由呼叫下列函式，顯示每個影片主要畫面格的一些資訊：


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



一般的應用程式會使用資料封包來解碼、remuxing、透過網路傳送，或執行其他工作。

## <a name="7-write-the-entry-point-function"></a>7. 撰寫 Entry-Point 函式

現在您可以將先前的步驟結合成完整的應用程式。 使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。 當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。 如需詳細資訊，請 [媒體基礎初始化](initializing-media-foundation.md)。


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a>程式清單

下列程式碼顯示教學課程的完整清單。


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
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

 

 



