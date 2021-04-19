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
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="b325e-103">教學課程：使用 WMContainer 物件讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b325e-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="b325e-104">本教學課程說明如何使用 [Asf 分隔器](asf-splitter.md)，從 Advanced 系統格式取得資料封包 (asf) 檔。</span><span class="sxs-lookup"><span data-stu-id="b325e-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="b325e-105">在本教學課程中，您將建立簡單的主控台應用程式，以讀取 ASF 檔案，並為檔案中的第一個影片串流產生壓縮媒體範例。</span><span class="sxs-lookup"><span data-stu-id="b325e-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="b325e-106">應用程式會顯示影片串流中主要畫面格的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b325e-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="b325e-107">本教學課程包含下列步驟：</span><span class="sxs-lookup"><span data-stu-id="b325e-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="b325e-108">先決條件</span><span class="sxs-lookup"><span data-stu-id="b325e-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="b325e-109">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="b325e-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="b325e-110">2. 開啟 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b325e-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="b325e-111">3. 讀取 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="b325e-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="b325e-112">4. 建立 ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="b325e-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="b325e-113">5. 選取要剖析的資料流程</span><span class="sxs-lookup"><span data-stu-id="b325e-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="b325e-114">6. 產生壓縮的媒體範例</span><span class="sxs-lookup"><span data-stu-id="b325e-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="b325e-115">7. 撰寫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="b325e-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="b325e-116">程式清單</span><span class="sxs-lookup"><span data-stu-id="b325e-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="b325e-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="b325e-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="b325e-118">本教學課程並未涵蓋如何解碼應用程式從 ASF 分隔器取得的壓縮資料。</span><span class="sxs-lookup"><span data-stu-id="b325e-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b325e-119">必要條件</span><span class="sxs-lookup"><span data-stu-id="b325e-119">Prerequisites</span></span>

<span data-ttu-id="b325e-120">本教學課程假設您已句備下列條件：</span><span class="sxs-lookup"><span data-stu-id="b325e-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="b325e-121">您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="b325e-122">這些元件包括 ContentInfo 物件、分隔器、多工器和設定檔。</span><span class="sxs-lookup"><span data-stu-id="b325e-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="b325e-123">如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。</span><span class="sxs-lookup"><span data-stu-id="b325e-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="b325e-124">您已熟悉 [媒體緩衝區](media-buffers.md) 和位元組資料流程：具體而言，使用位元組資料流程的檔案作業、從位元組資料流程讀取至媒體緩衝區，以及將媒體緩衝區的內容寫入位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="b325e-125">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="b325e-125">1. Set up the Project</span></span>

<span data-ttu-id="b325e-126">在原始程式檔中包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="b325e-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="b325e-127">連結至下列程式庫檔案：</span><span class="sxs-lookup"><span data-stu-id="b325e-127">Link to the following library files:</span></span>

-   <span data-ttu-id="b325e-128">mfplat .lib</span><span class="sxs-lookup"><span data-stu-id="b325e-128">mfplat.lib</span></span>
-   <span data-ttu-id="b325e-129">mf .lib</span><span class="sxs-lookup"><span data-stu-id="b325e-129">mf.lib</span></span>
-   <span data-ttu-id="b325e-130">mfuuid .lib</span><span class="sxs-lookup"><span data-stu-id="b325e-130">mfuuid.lib</span></span>

<span data-ttu-id="b325e-131">宣告 [SafeRelease](saferelease.md) 函數：</span><span class="sxs-lookup"><span data-stu-id="b325e-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="b325e-132">2. 開啟 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="b325e-132">2. Open an ASF File</span></span>

<span data-ttu-id="b325e-133">接下來，藉由呼叫 [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) 函式來開啟指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="b325e-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="b325e-134">方法會傳回位元組資料流程物件的指標，其中包含檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="b325e-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="b325e-135">檔案名是由使用者透過應用程式的命令列引數所指定。</span><span class="sxs-lookup"><span data-stu-id="b325e-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="b325e-136">下列程式碼範例會採用檔案名，並將指標傳回給可用來讀取檔案的位元組資料流程物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="b325e-137">3. 讀取 ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="b325e-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="b325e-138">接著，建立 [ASF ContentInfo 物件](asf-contentinfo-object.md) ，並使用它來剖析指定檔案的 Asf 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="b325e-139">ContentInfo 物件會儲存來自 ASF 標頭的資訊，包括通用檔案屬性和每個串流的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b325e-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="b325e-140">您稍後會在本教學課程中使用 ContentInfo 物件來初始化 ASF 分隔器，並取得影片資料流程的串流號碼。</span><span class="sxs-lookup"><span data-stu-id="b325e-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="b325e-141">若要建立 ASF ContentInfo 物件：</span><span class="sxs-lookup"><span data-stu-id="b325e-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="b325e-142">呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 函數，以建立 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="b325e-143">方法會傳回 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b325e-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="b325e-144">將 ASF 檔案中的前30個位元組資料讀入媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b325e-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="b325e-145">將媒體緩衝區傳遞給 [**IMFASFContentInfo：： GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) 方法。</span><span class="sxs-lookup"><span data-stu-id="b325e-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="b325e-146">這個方法會傳回 ASF 檔案中標頭物件的總大小。</span><span class="sxs-lookup"><span data-stu-id="b325e-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="b325e-147">將相同的媒體緩衝區傳遞給 [**IMFASFContentInfo：:P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法。</span><span class="sxs-lookup"><span data-stu-id="b325e-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="b325e-148">將標頭物件的其餘部分讀入新的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b325e-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="b325e-149">將第二個緩衝區傳遞給 [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) 方法。</span><span class="sxs-lookup"><span data-stu-id="b325e-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="b325e-150">在 **ParseHeader** 的 *cbOffsetWithinHeader* 參數中指定30位元組的位移。</span><span class="sxs-lookup"><span data-stu-id="b325e-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="b325e-151">**ParseHeader** 方法會使用從標頭物件中包含的各種 ASF 物件收集而來的資訊，初始化 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


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



<span data-ttu-id="b325e-152">此函式會使用函式 `ReadFromByteStream` 從位元組資料流程讀取至媒體緩衝區：</span><span class="sxs-lookup"><span data-stu-id="b325e-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


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



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="b325e-153">4. 建立 ASF 分隔器</span><span class="sxs-lookup"><span data-stu-id="b325e-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="b325e-154">接下來，建立 [ASF 分隔器](asf-splitter.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b325e-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="b325e-155">您將使用 ASF 分隔器來剖析 ASF 資料物件，其中包含適用于 ASF 檔案的 packetized 媒體資料。</span><span class="sxs-lookup"><span data-stu-id="b325e-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="b325e-156">若要建立 ASF 檔案的分隔器物件：</span><span class="sxs-lookup"><span data-stu-id="b325e-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="b325e-157">呼叫 [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) 函數來建立 ASF 分隔器。</span><span class="sxs-lookup"><span data-stu-id="b325e-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="b325e-158">函數會傳回 [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b325e-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="b325e-159">呼叫 [**IMFASFSplitter：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) 以初始化 ASF 分隔器。</span><span class="sxs-lookup"><span data-stu-id="b325e-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="b325e-160">這個方法會採用在程式3中建立之 ContentInfo 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="b325e-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


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



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="b325e-161">5. 選取要剖析的資料流程</span><span class="sxs-lookup"><span data-stu-id="b325e-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="b325e-162">接下來，列舉 ASF 檔案中的串流，然後選取第一個影片串流進行剖析。</span><span class="sxs-lookup"><span data-stu-id="b325e-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="b325e-163">若要列舉資料流程，您將使用 ASF 設定檔物件，並搜尋具有影片媒體類型的資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="b325e-164">若要選取影片資料流程：</span><span class="sxs-lookup"><span data-stu-id="b325e-164">To select the video stream:</span></span>

1.  <span data-ttu-id="b325e-165">在 ContentInfo 物件上呼叫 [**IMFASFContentInfo：： GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) ，以建立 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b325e-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="b325e-166">在其他資訊中，設定檔會描述 ASF 檔案中的資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="b325e-167">呼叫 [**IMFASFProfile：： GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) 來取得 ASF 檔案中的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="b325e-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="b325e-168">在迴圈中呼叫 [**IMFASFProfile：： GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) 來列舉資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="b325e-169">方法會傳回 [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b325e-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="b325e-170">它也會傳回資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="b325e-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="b325e-171">呼叫 [**IMFASFStreamConfig：： GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) 來取得資料流程的主要類型 GUID。</span><span class="sxs-lookup"><span data-stu-id="b325e-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="b325e-172">如果主要型別 GUID 是 MFMediaType \_ video，資料流程就會包含影片。</span><span class="sxs-lookup"><span data-stu-id="b325e-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="b325e-173">如果您在步驟4中找到影片資料流程，請呼叫 [**IMFASFSplitter：： SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) 來選取資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="b325e-174">這個方法會接受資料流程識別碼的陣列。</span><span class="sxs-lookup"><span data-stu-id="b325e-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="b325e-175">在本教學課程中，陣列大小為1，因為應用程式將剖析單一資料流程。</span><span class="sxs-lookup"><span data-stu-id="b325e-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="b325e-176">下列範例程式碼會列舉 ASF 檔案中的資料流程，並選取 ASF 分隔器上的第一個影片資料流程：</span><span class="sxs-lookup"><span data-stu-id="b325e-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


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



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="b325e-177">6. 產生壓縮的媒體範例</span><span class="sxs-lookup"><span data-stu-id="b325e-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="b325e-178">接下來，使用 ASF 分隔器來剖析 ASF 資料物件，並取得所選影片資料流程的資料封包。</span><span class="sxs-lookup"><span data-stu-id="b325e-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="b325e-179">應用程式會從固定大社區塊中的 ASF 檔案讀取資料，並將資料傳遞給 ASF 分隔器。</span><span class="sxs-lookup"><span data-stu-id="b325e-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="b325e-180">分隔器會剖析資料，並產生包含已壓縮影片資料的 [媒體範例](media-samples.md) 。</span><span class="sxs-lookup"><span data-stu-id="b325e-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="b325e-181">應用程式會檢查每個範例是否代表主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="b325e-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="b325e-182">如果是，應用程式會顯示範例的一些基本資訊：</span><span class="sxs-lookup"><span data-stu-id="b325e-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="b325e-183">媒體緩衝區數目</span><span class="sxs-lookup"><span data-stu-id="b325e-183">Number of media buffers</span></span>
-   <span data-ttu-id="b325e-184">資料的大小總計</span><span class="sxs-lookup"><span data-stu-id="b325e-184">Total size of the data</span></span>
-   <span data-ttu-id="b325e-185">時間戳記</span><span class="sxs-lookup"><span data-stu-id="b325e-185">Time stamp</span></span>

<span data-ttu-id="b325e-186">若要產生壓縮的媒體範例：</span><span class="sxs-lookup"><span data-stu-id="b325e-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="b325e-187">配置新的媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b325e-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="b325e-188">從位元組資料流程將資料讀入媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b325e-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="b325e-189">將媒體緩衝區傳遞給 [**IMFASFSplitter：:P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) 方法。</span><span class="sxs-lookup"><span data-stu-id="b325e-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="b325e-190">方法會剖析緩衝區中的 ASF 資料。</span><span class="sxs-lookup"><span data-stu-id="b325e-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="b325e-191">在迴圈中，藉由呼叫 [**IMFASFSplitter：： GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample)從分隔器取得媒體範例。</span><span class="sxs-lookup"><span data-stu-id="b325e-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="b325e-192">如果 *ppISample* 參數收到有效的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 指標，則表示 ASF 分隔器已剖析一或多個資料封包。</span><span class="sxs-lookup"><span data-stu-id="b325e-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="b325e-193">如果 *ppISample* 收到 **Null** 值，請中斷迴圈，然後返回步驟1。</span><span class="sxs-lookup"><span data-stu-id="b325e-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="b325e-194">顯示範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b325e-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="b325e-195">在下列情況下，從迴圈中斷：</span><span class="sxs-lookup"><span data-stu-id="b325e-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="b325e-196">*PpISample* 參數會接收 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="b325e-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="b325e-197">*PdwStatusFlags* 參數未收到 **ASF \_ STATUSFLAGS \_ 不完整** 旗標。</span><span class="sxs-lookup"><span data-stu-id="b325e-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="b325e-198">重複這些步驟，直到到達檔案結尾為止。</span><span class="sxs-lookup"><span data-stu-id="b325e-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="b325e-199">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="b325e-199">The following code shows these steps:</span></span>


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



<span data-ttu-id="b325e-200">IsKeyFrame 函式會藉由取得 [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) 屬性的值，測試範例是否為主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="b325e-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="b325e-201">為了方便說明，本教學課程會藉由呼叫下列函式，顯示每個影片主要畫面格的一些資訊：</span><span class="sxs-lookup"><span data-stu-id="b325e-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


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



<span data-ttu-id="b325e-202">一般的應用程式會使用資料封包來解碼、remuxing、透過網路傳送，或執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="b325e-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="b325e-203">7. 撰寫 Entry-Point 函式</span><span class="sxs-lookup"><span data-stu-id="b325e-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="b325e-204">現在您可以將先前的步驟結合成完整的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b325e-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="b325e-205">使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="b325e-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="b325e-206">當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。</span><span class="sxs-lookup"><span data-stu-id="b325e-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="b325e-207">如需詳細資訊，請 [媒體基礎初始化](initializing-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="b325e-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


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



## <a name="program-listing"></a><span data-ttu-id="b325e-208">程式清單</span><span class="sxs-lookup"><span data-stu-id="b325e-208">Program Listing</span></span>

<span data-ttu-id="b325e-209">下列程式碼顯示教學課程的完整清單。</span><span class="sxs-lookup"><span data-stu-id="b325e-209">The following code shows the complete listing for the tutorial.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b325e-210">相關主題</span><span class="sxs-lookup"><span data-stu-id="b325e-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b325e-211">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="b325e-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="b325e-212">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="b325e-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



