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
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="1aac1-103">教學課程：使用 WMContainer 物件複製 ASF 資料流程</span><span class="sxs-lookup"><span data-stu-id="1aac1-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="1aac1-104">建立 ASF 檔案的其中一種方式是從現有的檔案複製 ASF 資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="1aac1-105">若要這樣做，您可以從來源檔案取出媒體資料，然後寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="1aac1-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="1aac1-106">如果來源檔案是 ASF 檔案，您可以複製 stream 範例，而不需要解壓縮並 recompressing 它們。</span><span class="sxs-lookup"><span data-stu-id="1aac1-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="1aac1-107">本教學課程會示範此案例，方法是將 ASF 音訊影片檔案中的第一個音訊串流解壓縮 ( .wmv) ，並將它複製到新的 ASF 音訊檔案 ( .wma) 。</span><span class="sxs-lookup"><span data-stu-id="1aac1-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="1aac1-108">在本教學課程中，您將建立主控台應用程式，以將輸入和輸出檔案名視為引數。</span><span class="sxs-lookup"><span data-stu-id="1aac1-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="1aac1-109">應用程式會使用 ASF 分隔器來剖析輸入資料流程範例，然後將它們傳送給 ASF 多工器，以寫入音訊串流的 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="1aac1-110">本教學課程包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1aac1-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="1aac1-111">先決條件</span><span class="sxs-lookup"><span data-stu-id="1aac1-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="1aac1-112">術語</span><span class="sxs-lookup"><span data-stu-id="1aac1-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="1aac1-113">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="1aac1-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="1aac1-114">2. 宣告 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="1aac1-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="1aac1-115">3. 開啟輸入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="1aac1-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="1aac1-116">4. 初始化輸入檔的物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="1aac1-117">5. 建立音訊設定檔</span><span class="sxs-lookup"><span data-stu-id="1aac1-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="1aac1-118">6. 初始化輸出檔案的物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="1aac1-119">7. 產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="1aac1-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="1aac1-120">8. 在新檔案中寫入 ASF 物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="1aac1-121">9撰寫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="1aac1-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="1aac1-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aac1-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="1aac1-123">必要條件</span><span class="sxs-lookup"><span data-stu-id="1aac1-123">Prerequisites</span></span>

<span data-ttu-id="1aac1-124">本教學課程假設您已句備下列條件：</span><span class="sxs-lookup"><span data-stu-id="1aac1-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="1aac1-125">您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="1aac1-126">這些元件包括 ContentInfo、分隔器、多工器和設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="1aac1-127">如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="1aac1-128">您已熟悉剖析 ASF 標頭物件和現有檔案的 ASF 資料封包，以及使用分隔器產生壓縮資料流程範例的程式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="1aac1-129">如需詳細資訊，請參閱 [教學課程：讀取 ASF](tutorial--reading-an-asf-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="1aac1-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="1aac1-130">您熟悉媒體緩衝區和位元組資料流程：具體而言，使用位元組資料流程的檔案作業，以及將媒體緩衝區的內容寫入位元組資料流程中。</span><span class="sxs-lookup"><span data-stu-id="1aac1-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="1aac1-131"> (請參閱 [2。宣告 Helper 函數](#2-declare-helper-functions)。 ) </span><span class="sxs-lookup"><span data-stu-id="1aac1-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="1aac1-132">詞彙</span><span class="sxs-lookup"><span data-stu-id="1aac1-132">Terminology</span></span>

<span data-ttu-id="1aac1-133">本教學課程使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="1aac1-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="1aac1-134">來源位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸入檔的內容。</span><span class="sxs-lookup"><span data-stu-id="1aac1-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="1aac1-135">來源 ContentInfo 物件： ContentInfo 物件會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸入檔的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="1aac1-136">音訊設定檔：設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面，其中只包含輸入檔的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="1aac1-137">資料流程範例：媒體範例（公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面）由分隔器產生，代表從輸入檔以壓縮狀態取得的選定資料流程媒體資料。</span><span class="sxs-lookup"><span data-stu-id="1aac1-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="1aac1-138">Output ContentInfo object： ContentInfo 物件會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸出檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="1aac1-139">資料位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，此介面代表輸出檔案的整個 ASF 資料物件部分。</span><span class="sxs-lookup"><span data-stu-id="1aac1-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="1aac1-140">資料封包：媒體範例（公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面）由多工器所產生，代表將寫入資料位元組資料流程的 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="1aac1-141">輸出位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸出檔的內容。</span><span class="sxs-lookup"><span data-stu-id="1aac1-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="1aac1-142">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="1aac1-142">1. Set up the Project</span></span>

<span data-ttu-id="1aac1-143">在原始程式檔中包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="1aac1-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="1aac1-144">連結至下列程式庫檔案：</span><span class="sxs-lookup"><span data-stu-id="1aac1-144">Link to the following library files:</span></span>

-   <span data-ttu-id="1aac1-145">mfplat .lib</span><span class="sxs-lookup"><span data-stu-id="1aac1-145">mfplat.lib</span></span>
-   <span data-ttu-id="1aac1-146">mf .lib</span><span class="sxs-lookup"><span data-stu-id="1aac1-146">mf.lib</span></span>
-   <span data-ttu-id="1aac1-147">mfuuid .lib</span><span class="sxs-lookup"><span data-stu-id="1aac1-147">mfuuid.lib</span></span>

<span data-ttu-id="1aac1-148">宣告 [SafeRelease](saferelease.md) 函數：</span><span class="sxs-lookup"><span data-stu-id="1aac1-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-declare-helper-functions"></a><span data-ttu-id="1aac1-149">2. 宣告 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="1aac1-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="1aac1-150">本教學課程會使用下列 helper 函式，從位元組資料流程讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="1aac1-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="1aac1-151">`AllocReadFromByteStream`函數會從位元組資料流程讀取資料，並配置新的媒體緩衝區來保存資料。</span><span class="sxs-lookup"><span data-stu-id="1aac1-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="1aac1-152">如需詳細資訊，請參閱 [**IMFByteStream：： Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


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



<span data-ttu-id="1aac1-153">函數會將 `WriteBufferToByteStream` 資料從媒體緩衝區寫入位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="1aac1-154">如需詳細資訊，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="1aac1-155">函數會將 `AppendToByteStream` 一個位元組資料流程的內容附加至另一個位元組資料流程：</span><span class="sxs-lookup"><span data-stu-id="1aac1-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="1aac1-156">3. 開啟輸入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="1aac1-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="1aac1-157">藉由呼叫 [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) 函數來開啟輸入檔。</span><span class="sxs-lookup"><span data-stu-id="1aac1-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="1aac1-158">方法會傳回位元組資料流程物件的指標，其中包含檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="1aac1-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="1aac1-159">檔案名是由使用者透過應用程式的命令列引數所指定。</span><span class="sxs-lookup"><span data-stu-id="1aac1-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="1aac1-160">下列程式碼範例會採用檔案名，並將指標傳回給可用來讀取檔案的位元組資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="1aac1-161">4. 初始化輸入檔的物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="1aac1-162">接下來，您將建立並初始化來源 ContentInfo 物件和分隔器，以產生資料流程範例。</span><span class="sxs-lookup"><span data-stu-id="1aac1-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="1aac1-163">在步驟2中建立的這個來源位元組資料流程將用來剖析 ASF 標頭物件，並填入來源 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="1aac1-164">此物件將用來初始化分隔器，以協助剖析輸入檔中音訊資料流程的 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="1aac1-165">您也會取出輸入檔中的 ASF 資料物件長度，以及相對於檔開頭的第一個 ASF 資料封包的位移。</span><span class="sxs-lookup"><span data-stu-id="1aac1-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="1aac1-166">分隔器會使用這些屬性來產生音訊串流範例。</span><span class="sxs-lookup"><span data-stu-id="1aac1-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="1aac1-167">建立並初始化輸入檔的 ASF 元件：</span><span class="sxs-lookup"><span data-stu-id="1aac1-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="1aac1-168">呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="1aac1-169">此函數會傳回 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1aac1-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="1aac1-170">呼叫 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 來剖析 ASF 標頭。</span><span class="sxs-lookup"><span data-stu-id="1aac1-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="1aac1-171">如需此步驟的詳細資訊，請參閱 [讀取現有檔案的 ASF 標頭物件](reading-the-asf-header-object-of-an-existing-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="1aac1-172">呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 來建立 ASF 分隔器物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="1aac1-173">此函數會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1aac1-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="1aac1-174">呼叫 [**IMFASFSplitter：： Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize)，傳入 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)指標。</span><span class="sxs-lookup"><span data-stu-id="1aac1-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="1aac1-175">如需此步驟的詳細資訊，請參閱 [建立 ASF 分隔器物件](creating-the-asf-splitter-object.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="1aac1-176">呼叫 [**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) 來取得 ASF 檔案的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="1aac1-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="1aac1-177">從表示描述項取得 [ [**MF \_ PD \_ ASF \_ 資料 \_ 起始 \_ 位移**](mf-pd-asf-data-start-offset-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1aac1-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="1aac1-178">此值是檔案中 ASF 資料物件的位置，以位元組位移的形式從檔案開頭開始。</span><span class="sxs-lookup"><span data-stu-id="1aac1-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="1aac1-179">從表示描述項取得 [ [**MF \_ PD \_ ASF \_ 資料 \_ 長度**](mf-pd-asf-data-length-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1aac1-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="1aac1-180">此值為 ASF 資料物件的總大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="1aac1-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="1aac1-181">如需詳細資訊，請參閱 [從 ASF 標頭物件取得資訊](getting-information-from-asf-header-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="1aac1-182">下列範例程式碼顯示合併所有步驟的函式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="1aac1-183">此函式會接受來源位元組資料流程的指標，並傳回來源 ContentInfo 物件和分隔器的指標。</span><span class="sxs-lookup"><span data-stu-id="1aac1-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="1aac1-184">此外，它也會接收 ASF 資料物件的長度和位移。</span><span class="sxs-lookup"><span data-stu-id="1aac1-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


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



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="1aac1-185">5. 建立音訊設定檔</span><span class="sxs-lookup"><span data-stu-id="1aac1-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="1aac1-186">接下來，您將會從來源 ContentInfo 物件取得輸入檔的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="1aac1-187">接著，您將設定設定檔，使其只包含輸入檔的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="1aac1-188">若要這樣做，請列舉資料流程並從設定檔中移除非音訊串流。</span><span class="sxs-lookup"><span data-stu-id="1aac1-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="1aac1-189">本教學課程稍後將使用音訊設定檔物件來初始化輸出 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="1aac1-190">建立音訊設定檔</span><span class="sxs-lookup"><span data-stu-id="1aac1-190">To create an audio profile</span></span>

1.  <span data-ttu-id="1aac1-191">藉由呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)，從來源 ContentInfo 物件取得輸入檔的設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="1aac1-192">方法會傳回設定檔物件的指標，其中包含輸入檔中的所有資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="1aac1-193">如需詳細資訊，請參閱 [建立 ASF 設定檔](creating-an-asf-profile.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="1aac1-194">從設定檔中移除任何相互排除的物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="1aac1-195">這是必要步驟，因為非音訊串流將會從設定檔中移除，這可能會使相互排除物件失效。</span><span class="sxs-lookup"><span data-stu-id="1aac1-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="1aac1-196">移除設定檔中的所有非音訊串流，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1aac1-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="1aac1-197">呼叫 [**IMFASFProfile：： GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) 來取得資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="1aac1-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="1aac1-198">在迴圈中，呼叫 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) ，以依索引取得每個資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="1aac1-199">呼叫 [**IMFASFStreamConfig：： GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) 以取得資料流程類型。</span><span class="sxs-lookup"><span data-stu-id="1aac1-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="1aac1-200">若為非音訊資料流程，請呼叫 [**IMFASFProfile：： RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) 來移除資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="1aac1-201">儲存第一個音訊串流的串流編號。</span><span class="sxs-lookup"><span data-stu-id="1aac1-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="1aac1-202">這將會在分隔器上選取，以產生資料流程範例。</span><span class="sxs-lookup"><span data-stu-id="1aac1-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="1aac1-203">如果資料流程號碼為零，則呼叫端可以假設沒有音訊資料流程檔案。</span><span class="sxs-lookup"><span data-stu-id="1aac1-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="1aac1-204">下列程式碼會執行這些步驟：</span><span class="sxs-lookup"><span data-stu-id="1aac1-204">The following code these steps:</span></span>


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



<span data-ttu-id="1aac1-205">`RemoveMutexes`函數會從設定檔中移除任何互斥物件：</span><span class="sxs-lookup"><span data-stu-id="1aac1-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


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



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="1aac1-206">6. 初始化輸出檔案的物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="1aac1-207">接下來，您將建立輸出 ContentInfo 物件和多工器，以產生輸出檔的資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="1aac1-208">在步驟4中建立的音訊設定檔將用來填入輸出 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="1aac1-209">此物件包含通用檔案屬性和資料流程屬性等資訊。</span><span class="sxs-lookup"><span data-stu-id="1aac1-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="1aac1-210">輸出 ContentInfo 物件將用來初始化多工器，這些多工器會產生輸出檔的資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="1aac1-211">產生資料封包之後，必須更新 ContentInfo 物件，以反映新的值。</span><span class="sxs-lookup"><span data-stu-id="1aac1-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="1aac1-212">建立和初始化輸出檔案的 ASF 元件</span><span class="sxs-lookup"><span data-stu-id="1aac1-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="1aac1-213">藉由呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 來建立空的 ContentInfo 物件，並在其中填入在步驟3中建立之音訊設定檔的資訊，方法是呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="1aac1-214">如需詳細資訊，請參閱 [初始化新 ASF 檔案的 ContentInfo 物件](initializing-the-contentinfo-object-of-a-new-asf-file.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="1aac1-215">使用 output ContentInfo 物件來建立和初始化多工器物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="1aac1-216">如需詳細資訊，請參閱建立多工器 [物件](creating-the-multiplexer-object.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="1aac1-217">下列範例程式碼顯示可合併步驟的函式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="1aac1-218">此函式會接受設定檔物件的指標，並傳回輸出 ContentInfo 物件和多工器的指標。</span><span class="sxs-lookup"><span data-stu-id="1aac1-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="1aac1-219">7. 產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="1aac1-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="1aac1-220">接下來，您將使用分隔器從來源位元組資料流程產生音訊串流範例，並將它們傳送至多工器，以建立 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="1aac1-221">這些資料封包將構成新檔案的最終 ASF 資料物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="1aac1-222">產生音訊串流範例</span><span class="sxs-lookup"><span data-stu-id="1aac1-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="1aac1-223">藉由呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams)，在分隔器上選取第一個音訊串流。</span><span class="sxs-lookup"><span data-stu-id="1aac1-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="1aac1-224">從來源位元組串流將固定大小的媒體資料區塊讀取至媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1aac1-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="1aac1-225">藉由在迴圈中呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) ，在迴圈中呼叫：：，以將資料流程範例收集為媒體範例，只要它收到 \_ \_ *pdwStatusFlags* 參數中的 ASF STATUSFLAGS 不完整旗標即可。</span><span class="sxs-lookup"><span data-stu-id="1aac1-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="1aac1-226">如需詳細資訊，請參閱 [從現有的 Asf 資料物件產生資料流程範例](generating-stream-samples-from-an-existing-asf-data-object.md)中，產生 asf 資料封包的範例。</span><span class="sxs-lookup"><span data-stu-id="1aac1-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="1aac1-227">針對每個媒體範例，呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) ，將媒體範例傳送至多工器。</span><span class="sxs-lookup"><span data-stu-id="1aac1-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="1aac1-228">多工器會產生 ASF 資料物件的資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="1aac1-229">將多工器產生的資料封包寫入資料位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="1aac1-230">產生所有的資料封包之後，請呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) ，以在 ASF 資料封包產生期間所收集的資訊來更新輸出 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="1aac1-231">下列程式碼範例會從 ASF 分隔器產生串流範例，並將它們傳送至多工器。</span><span class="sxs-lookup"><span data-stu-id="1aac1-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="1aac1-232">多工器會產生 ASF 資料封包，並將其寫入資料流程。</span><span class="sxs-lookup"><span data-stu-id="1aac1-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


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



<span data-ttu-id="1aac1-233">為了取得來自 ASF 分隔器的封包，先前的程式碼會呼叫函式 `GetPacketsFromSplitter` ，如下所示：</span><span class="sxs-lookup"><span data-stu-id="1aac1-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


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



<span data-ttu-id="1aac1-234">函數會從多工器 `GenerateDataPackets` 取得資料封包。</span><span class="sxs-lookup"><span data-stu-id="1aac1-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="1aac1-235">如需詳細資訊，請參閱 [取得 ASF 資料封包](generating-new-asf-data-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="1aac1-236">8. 在新檔案中寫入 ASF 物件</span><span class="sxs-lookup"><span data-stu-id="1aac1-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="1aac1-237">接下來，您會呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)，將輸出 ContentInfo 物件的內容寫入媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="1aac1-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="1aac1-238">這個方法會將儲存在 ContentInfo 物件中的資料，轉換成 ASF 標頭物件格式的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="1aac1-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="1aac1-239">如需詳細資訊，請參閱 [產生新的 ASF 標頭物件](generating-a-new-asf-header-object.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="1aac1-240">在產生新的 ASF 標頭物件之後，先將標頭物件寫入至步驟2中建立的輸出位元組資料流程（藉由呼叫 helper 函數 WriteBufferToByteStream），以寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="1aac1-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="1aac1-241">使用包含在資料位元組資料流程中的資料物件來追蹤標頭物件。</span><span class="sxs-lookup"><span data-stu-id="1aac1-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="1aac1-242">範例程式碼會示範將資料位元組資料流程的內容傳送至輸出位元組資料流程的函式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


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



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="1aac1-243">9撰寫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="1aac1-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="1aac1-244">現在您可以將先前的步驟結合成完整的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="1aac1-245">使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="1aac1-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="1aac1-246">當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="1aac1-247">如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="1aac1-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="1aac1-248">下列程式碼顯示完整的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="1aac1-248">The following code shows the complete console application.</span></span> <span data-ttu-id="1aac1-249">命令列引數會指定要轉換的檔案名和新音訊檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="1aac1-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="1aac1-250">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aac1-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aac1-251">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="1aac1-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="1aac1-252">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="1aac1-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



