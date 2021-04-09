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
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="3892f-103">教學課程：使用 WMContainer 物件撰寫 WMA 檔案</span><span class="sxs-lookup"><span data-stu-id="3892f-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="3892f-104">本教學課程示範如何將非壓縮)  ( 音訊檔案中的媒體內容解壓縮，以將新的音訊檔 ( .wma) ，然後以 ASF 格式將其壓縮。</span><span class="sxs-lookup"><span data-stu-id="3892f-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="3892f-105">轉換所使用的編碼模式是 (CBR) 的 [固定位速率編碼](constant-bit-rate-encoding.md) 。</span><span class="sxs-lookup"><span data-stu-id="3892f-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="3892f-106">在此模式中，應用程式會在編碼會話之前，指定編碼器必須達到的目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="3892f-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="3892f-107">在本教學課程中，您將建立主控台應用程式，以將輸入和輸出檔案名視為引數。</span><span class="sxs-lookup"><span data-stu-id="3892f-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="3892f-108">應用程式會從 wave 檔案剖析應用程式取得未壓縮的媒體範例，此應用程式會在本教學課程中提供。</span><span class="sxs-lookup"><span data-stu-id="3892f-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="3892f-109">這些範例會傳送至編碼器，以轉換成 Windows Media 音訊9格式。</span><span class="sxs-lookup"><span data-stu-id="3892f-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="3892f-110">編碼器是針對 CBR 編碼進行設定，並使用在媒體類型協商期間可用的第一個位元速率做為目標位元速率。</span><span class="sxs-lookup"><span data-stu-id="3892f-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="3892f-111">編碼的範例會傳送至多工器，以取得 ASF 資料格式的 packetization。</span><span class="sxs-lookup"><span data-stu-id="3892f-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="3892f-112">這些封包將會寫入代表 ASF 資料物件的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="3892f-113">在 [資料] 區段就緒之後，您將建立一個 ASF 音訊檔案，並撰寫新的 ASF 標頭物件來合併所有標頭資訊，然後附加 ASF 資料物件位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="3892f-114">本教學課程包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="3892f-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="3892f-115">先決條件</span><span class="sxs-lookup"><span data-stu-id="3892f-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3892f-116">術語</span><span class="sxs-lookup"><span data-stu-id="3892f-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="3892f-117">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="3892f-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="3892f-118">2. 宣告 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="3892f-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="3892f-119">3. 開啟音訊檔案</span><span class="sxs-lookup"><span data-stu-id="3892f-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="3892f-120">4. 設定編碼器</span><span class="sxs-lookup"><span data-stu-id="3892f-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="3892f-121">5. 建立 ASF ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="3892f-122">6. 建立 ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="3892f-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="3892f-123">7. 產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="3892f-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="3892f-124">8. 寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="3892f-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="3892f-125">9. 定義 Entry-Point 函數</span><span class="sxs-lookup"><span data-stu-id="3892f-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="3892f-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="3892f-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3892f-127">必要條件</span><span class="sxs-lookup"><span data-stu-id="3892f-127">Prerequisites</span></span>

<span data-ttu-id="3892f-128">本教學課程假設您已句備下列條件：</span><span class="sxs-lookup"><span data-stu-id="3892f-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="3892f-129">您已熟悉 ASF 檔案的結構以及媒體基礎提供的元件，以使用 ASF 物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="3892f-130">這些元件包括 ContentInfo、分隔器、多工器和設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="3892f-131">如需詳細資訊，請參閱 [WMCONTAINER ASF 元件](wmcontainer-asf-components.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="3892f-132">您熟悉 Windows Media 編碼器以及各種編碼類型，尤其是 CBR。</span><span class="sxs-lookup"><span data-stu-id="3892f-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="3892f-133">如需詳細資訊，請參閱 [Windows Media 編碼器](windows-media-encoders.md) 。</span><span class="sxs-lookup"><span data-stu-id="3892f-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="3892f-134">您熟悉 [媒體緩衝區](media-buffers.md) 和位元組資料流程：具體而言，使用位元組資料流程的檔案作業，以及將媒體緩衝區的內容寫入位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="3892f-135">詞彙</span><span class="sxs-lookup"><span data-stu-id="3892f-135">Terminology</span></span>

<span data-ttu-id="3892f-136">本教學課程使用下列詞彙：</span><span class="sxs-lookup"><span data-stu-id="3892f-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="3892f-137">來源媒體類型：媒體類型物件會公開 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面，此介面會描述輸入檔的內容。</span><span class="sxs-lookup"><span data-stu-id="3892f-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="3892f-138">音訊設定檔：設定檔物件會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面，其中只包含輸出檔案的音訊資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="3892f-139">資料流程範例：媒體範例會公開 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面，代表從編碼器以壓縮狀態取得的輸入檔媒體資料。</span><span class="sxs-lookup"><span data-stu-id="3892f-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="3892f-140">ContentInfo 物件： [ASF ContentInfo 物件](asf-contentinfo-object.md)會公開 [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) 介面，此介面代表輸出檔案的 ASF 標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="3892f-141">資料位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，此介面代表輸出檔案的整個 ASF 資料物件部分。</span><span class="sxs-lookup"><span data-stu-id="3892f-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="3892f-142">資料封包：媒體範例會公開由 [ASF](asf-multiplexer.md)多工器產生的 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)介面;表示將寫入資料位元組資料流程的 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="3892f-143">輸出位元組資料流程：位元組資料流程物件會公開 [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) 介面，其中包含輸出檔的內容。</span><span class="sxs-lookup"><span data-stu-id="3892f-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="3892f-144">1. 設定專案</span><span class="sxs-lookup"><span data-stu-id="3892f-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="3892f-145">在原始程式檔中包含下列標頭：</span><span class="sxs-lookup"><span data-stu-id="3892f-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="3892f-146">連結至下列程式庫檔案：</span><span class="sxs-lookup"><span data-stu-id="3892f-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="3892f-147">mfplat .lib</span><span class="sxs-lookup"><span data-stu-id="3892f-147">mfplat.lib</span></span>
    -   <span data-ttu-id="3892f-148">mf .lib</span><span class="sxs-lookup"><span data-stu-id="3892f-148">mf.lib</span></span>
    -   <span data-ttu-id="3892f-149">mfuuid .lib</span><span class="sxs-lookup"><span data-stu-id="3892f-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="3892f-150">宣告 [SafeRelease](saferelease.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="3892f-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="3892f-151">在您的專案中包含 CWmaEncoder 類別。</span><span class="sxs-lookup"><span data-stu-id="3892f-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="3892f-152">如需此類別的完整原始碼，請參閱 [編碼器範例程式碼](encoder-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="3892f-153">2. 宣告 Helper 函數</span><span class="sxs-lookup"><span data-stu-id="3892f-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="3892f-154">本教學課程會使用下列 helper 函式，從位元組資料流程讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="3892f-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="3892f-155">`AppendToByteStream`：將一個位元組資料流程的內容附加至另一個位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="3892f-156">WriteBufferToByteStream：將資料從媒體緩衝區寫入位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="3892f-157">如需詳細資訊，請參閱 [**IMFByteStream：： Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)。</span><span class="sxs-lookup"><span data-stu-id="3892f-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="3892f-158">下列程式碼顯示這些 helper 函式：</span><span class="sxs-lookup"><span data-stu-id="3892f-158">The following code shows these helper functions:</span></span>


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



## <a name="3-open-an-audio-file"></a><span data-ttu-id="3892f-159">3. 開啟音訊檔案</span><span class="sxs-lookup"><span data-stu-id="3892f-159">3. Open an Audio File</span></span>

<span data-ttu-id="3892f-160">本教學課程假設您的應用程式將會產生未壓縮的音訊進行編碼。</span><span class="sxs-lookup"><span data-stu-id="3892f-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="3892f-161">基於這個目的，本教學課程中會宣告兩個函數：</span><span class="sxs-lookup"><span data-stu-id="3892f-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="3892f-162">這些函式的實作為讀者。</span><span class="sxs-lookup"><span data-stu-id="3892f-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="3892f-163">函式 `OpenAudioFile` 應該會開啟 *pszURL* 所指定的媒體檔案，並傳回描述音訊串流之媒體類型的指標。</span><span class="sxs-lookup"><span data-stu-id="3892f-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="3892f-164">`GetNextAudioSample`函數應該從開啟的檔案讀取未壓縮的 PCM 音訊 `OpenAudioFile` 。</span><span class="sxs-lookup"><span data-stu-id="3892f-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="3892f-165">到達檔案結尾時， *pbEOS* 會收到值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3892f-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="3892f-166">否則， *ppSample* 會收到包含音訊緩衝區的媒體範例。</span><span class="sxs-lookup"><span data-stu-id="3892f-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="3892f-167">4. 設定編碼器</span><span class="sxs-lookup"><span data-stu-id="3892f-167">4. Configure the Encoder</span></span>

<span data-ttu-id="3892f-168">接著，建立編碼器、設定它以產生 CBR 編碼的資料流程範例，並協商輸入和輸出媒體類型。</span><span class="sxs-lookup"><span data-stu-id="3892f-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="3892f-169">在媒體基礎中，編碼器 (公開 [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) 介面) 會實作為 [媒體基礎轉換](media-foundation-transforms.md) (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="3892f-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="3892f-170">在本教學課程中，會在為 MFT 提供包裝函式的類別中實作為編碼器 `CWmaEncoder` 。</span><span class="sxs-lookup"><span data-stu-id="3892f-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="3892f-171">如需此類別的完整原始碼，請參閱 [編碼器範例程式碼](encoder-example-code.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="3892f-172">您可以選擇性地將編碼類型指定為 CBR。</span><span class="sxs-lookup"><span data-stu-id="3892f-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="3892f-173">根據預設，編碼器會設定為使用 CBR 編碼。</span><span class="sxs-lookup"><span data-stu-id="3892f-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="3892f-174">如需詳細資訊，請參閱 [常數位元速率編碼](constant-bit-rate-encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="3892f-175">您可以設定其他屬性，視編碼類型而定，如需編碼模式特定屬性的相關資訊，請參閱 [品質型變數位速率編碼](quality-based-variable-bit-rate--vbr--encoding.md)、不受限制的變數位 [速率編碼](unconstrained-variable-bit-rate--vbr--encoding.md)，以及 [尖峰限制的變數位元速率編碼](peak-constrained-variable-bit-rate--vbr--encoding.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


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



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="3892f-176">5. 建立 ASF ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="3892f-177">[ASF ContentInfo 物件](asf-contentinfo-object.md)包含輸出檔案中各種標頭物件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3892f-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="3892f-178">首先，建立音訊串流的 ASF 設定檔：</span><span class="sxs-lookup"><span data-stu-id="3892f-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="3892f-179">呼叫 [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) 來建立空白的 ASF 設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="3892f-180">ASF 設定檔會公開 [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) 介面。</span><span class="sxs-lookup"><span data-stu-id="3892f-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="3892f-181">如需詳細資訊，請參閱 [建立及設定 ASF 資料流程](creating-and-configuring-asf-streams.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="3892f-182">從物件取得編碼的音訊格式 `CWmaEncoder` 。</span><span class="sxs-lookup"><span data-stu-id="3892f-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="3892f-183">呼叫 [**IMFASFProfile：： CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) ，以建立適用于 ASF 設定檔的新資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="3892f-184">傳入 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標，代表資料流程格式。</span><span class="sxs-lookup"><span data-stu-id="3892f-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="3892f-185">呼叫 [**IMFASFStreamConfig：： SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) 以指派資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="3892f-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="3892f-186">藉由在資料流程物件上設定 [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) 屬性，設定 "有漏洞 bucket" 參數。</span><span class="sxs-lookup"><span data-stu-id="3892f-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="3892f-187">呼叫 [**IMFASFProfile：： SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) ，將新的資料流程新增至設定檔。</span><span class="sxs-lookup"><span data-stu-id="3892f-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="3892f-188">現在建立 ASF ContentInfo 物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3892f-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="3892f-189">呼叫 [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) 以建立空的 ContentInfo 物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="3892f-190">呼叫 [**IMFASFContentInfo：： SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) 來設定 ASF 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3892f-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="3892f-191">下列程式碼顯示這些步驟：</span><span class="sxs-lookup"><span data-stu-id="3892f-191">The following code shows these steps:</span></span>


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



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="3892f-192">6. 建立 ASF 多工器</span><span class="sxs-lookup"><span data-stu-id="3892f-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="3892f-193">[Asf](asf-multiplexer.md)多工器會產生 asf 資料封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="3892f-194">呼叫 [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) 來建立 ASF 多工器。</span><span class="sxs-lookup"><span data-stu-id="3892f-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="3892f-195">呼叫 [**IMFASFMultiplexer：： initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) 以初始化多工器。</span><span class="sxs-lookup"><span data-stu-id="3892f-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="3892f-196">傳入在上一節中建立之 ASF 內容資訊物件的指標。</span><span class="sxs-lookup"><span data-stu-id="3892f-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="3892f-197">呼叫 [**IMFASFMultiplexer：： SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) 來設定 MFASF 多工器 **\_ \_ AUTOADJUST \_ 位元速率** 旗標。</span><span class="sxs-lookup"><span data-stu-id="3892f-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="3892f-198">使用此設定時，多工器會自動調整 ASF 內容的位元速率，以符合多工處理的資料流程特性。</span><span class="sxs-lookup"><span data-stu-id="3892f-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


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



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="3892f-199">7. 產生新的 ASF 資料封包</span><span class="sxs-lookup"><span data-stu-id="3892f-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="3892f-200">接下來，為新檔案產生 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="3892f-201">這些資料封包將構成新檔案的最終 ASF 資料物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="3892f-202">若要產生新的 ASF 資料封包：</span><span class="sxs-lookup"><span data-stu-id="3892f-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="3892f-203">呼叫 [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) 以建立暫存位元組資料流程來保存 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="3892f-204">呼叫應用程式定義的 `GetNextAudioSample` 函數，以取得編碼器的未壓縮音訊資料。</span><span class="sxs-lookup"><span data-stu-id="3892f-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="3892f-205">將未壓縮的音訊傳遞給編碼器進行壓縮。</span><span class="sxs-lookup"><span data-stu-id="3892f-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="3892f-206">如需詳細資訊，請參閱在[編碼器中處理資料](processing-data-in-the-encoder.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="3892f-207">呼叫 [**IMFASFMultiplexer：:P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) 將壓縮的音訊範例傳送至適用于 PACKETIZATION 的 ASF 多工器。</span><span class="sxs-lookup"><span data-stu-id="3892f-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="3892f-208">從多工器取得 ASF 封包，並將它們寫入暫存位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="3892f-209">如需詳細資訊，請參閱 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="3892f-210">當您到達來來源資料流的結尾時，請清空編碼器，並從編碼器提取剩餘的壓縮樣本。</span><span class="sxs-lookup"><span data-stu-id="3892f-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="3892f-211">如需有關清空 MFT 的詳細資訊，請參閱 [基本的 Mft 處理模型](basic-mft-processing-model.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="3892f-212">所有範例都傳送至多工器之後，請呼叫 [**IMFASFMultiplexer：： Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) ，然後從多工器提取其餘的 ASF 封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="3892f-213">呼叫 [**IMFASFMultiplexer：： End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end)。</span><span class="sxs-lookup"><span data-stu-id="3892f-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="3892f-214">下列程式碼會產生 ASF 資料封包。</span><span class="sxs-lookup"><span data-stu-id="3892f-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="3892f-215">函數會傳回包含 ASF 資料物件的位元組資料流程指標。</span><span class="sxs-lookup"><span data-stu-id="3892f-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


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



<span data-ttu-id="3892f-216">函式的 `GenerateASFDataPackets` 程式碼會顯示在 [產生新的 ASF 資料封包](generating-new-asf-data-packets.md)的主題中。</span><span class="sxs-lookup"><span data-stu-id="3892f-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="3892f-217">8. 寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="3892f-217">8. Write the ASF File</span></span>

<span data-ttu-id="3892f-218">接下來，呼叫 [**IMFASFContentInfo：： GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader)，將 ASF 標頭寫入媒體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="3892f-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="3892f-219">這個方法會將儲存在 ContentInfo 物件中的資料，轉換成 ASF 標頭物件格式的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="3892f-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="3892f-220">如需詳細資訊，請參閱 [產生新的 ASF 標頭物件](generating-a-new-asf-header-object.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="3892f-221">產生新的 ASF 標頭物件之後，請建立輸出檔案的位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="3892f-222">首先，將標頭物件寫入輸出位元組資料流程。</span><span class="sxs-lookup"><span data-stu-id="3892f-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="3892f-223">使用包含在資料位元組資料流程中的資料物件來追蹤標頭物件。</span><span class="sxs-lookup"><span data-stu-id="3892f-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


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



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="3892f-224">9. 定義 Entry-Point 函數</span><span class="sxs-lookup"><span data-stu-id="3892f-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="3892f-225">現在您可以將先前的步驟結合成完整的應用程式。</span><span class="sxs-lookup"><span data-stu-id="3892f-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="3892f-226">使用任何媒體基礎物件之前，請呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)來初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="3892f-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="3892f-227">當您完成時，請呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)。</span><span class="sxs-lookup"><span data-stu-id="3892f-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="3892f-228">如需詳細資訊，請參閱 [初始化媒體基礎](initializing-media-foundation.md)。</span><span class="sxs-lookup"><span data-stu-id="3892f-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="3892f-229">下列程式碼顯示完整的主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="3892f-229">The following code shows the complete console application.</span></span> <span data-ttu-id="3892f-230">命令列引數會指定要轉換的檔案名和新音訊檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3892f-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3892f-231">相關主題</span><span class="sxs-lookup"><span data-stu-id="3892f-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3892f-232">WMContainer ASF 元件</span><span class="sxs-lookup"><span data-stu-id="3892f-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="3892f-233">媒體基礎中的 ASF 支援</span><span class="sxs-lookup"><span data-stu-id="3892f-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



