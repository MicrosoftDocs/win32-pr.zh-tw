---
description: 本教學課程示範如何使用來源讀取器將音訊從媒體檔案解碼，並將音訊寫入 WAVE 檔案。
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 教學課程：解碼音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eb6d9f48419b62fa1c379c636abaf2bb0a63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558765"
---
# <a name="tutorial-decoding-audio"></a><span data-ttu-id="19cc9-103">教學課程：解碼音訊</span><span class="sxs-lookup"><span data-stu-id="19cc9-103">Tutorial: Decoding Audio</span></span>

<span data-ttu-id="19cc9-104">本教學課程示範如何使用 [來源讀取器](source-reader.md) 將音訊從媒體檔案解碼，並將音訊寫入 WAVE 檔案。</span><span class="sxs-lookup"><span data-stu-id="19cc9-104">This tutorial shows how to use the [Source Reader](source-reader.md) to decode audio from a media file and write the audio to a WAVE file.</span></span> <span data-ttu-id="19cc9-105">本教學課程是以 [音訊剪輯](audio-clip-sample.md) 範例為基礎。</span><span class="sxs-lookup"><span data-stu-id="19cc9-105">The tutorial is based on the [Audio Clip](audio-clip-sample.md) sample.</span></span>

-   [<span data-ttu-id="19cc9-106">概觀</span><span class="sxs-lookup"><span data-stu-id="19cc9-106">Overview</span></span>](#overview)
-   [<span data-ttu-id="19cc9-107">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="19cc9-107">Header and Library Files</span></span>](#header-and-library-files)
-   [<span data-ttu-id="19cc9-108">執行 wmain</span><span class="sxs-lookup"><span data-stu-id="19cc9-108">Implement wmain</span></span>](#implement-wmain)
-   [<span data-ttu-id="19cc9-109">寫入 WAVE 檔案</span><span class="sxs-lookup"><span data-stu-id="19cc9-109">Write the WAVE File</span></span>](#write-the-wave-file)
-   [<span data-ttu-id="19cc9-110">設定來源讀取器</span><span class="sxs-lookup"><span data-stu-id="19cc9-110">Configure the Source Reader</span></span>](#configure-the-source-reader)
-   [<span data-ttu-id="19cc9-111">寫入 WAVE 檔案標頭</span><span class="sxs-lookup"><span data-stu-id="19cc9-111">Write the WAVE File Header</span></span>](#write-the-wave-file-header)
-   [<span data-ttu-id="19cc9-112">計算資料大小上限</span><span class="sxs-lookup"><span data-stu-id="19cc9-112">Calculate the Maximum Data Size</span></span>](#calculate-the-maximum-data-size)
-   [<span data-ttu-id="19cc9-113">解碼音訊</span><span class="sxs-lookup"><span data-stu-id="19cc9-113">Decode the Audio</span></span>](#decode-the-audio)
-   [<span data-ttu-id="19cc9-114">完成檔案標頭</span><span class="sxs-lookup"><span data-stu-id="19cc9-114">Finalize the File Header</span></span>](#finalize-the-file-header)
-   [<span data-ttu-id="19cc9-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="19cc9-115">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="19cc9-116">概觀</span><span class="sxs-lookup"><span data-stu-id="19cc9-116">Overview</span></span>

<span data-ttu-id="19cc9-117">在本教學課程中，您將建立一個主控台應用程式，該應用程式會採用兩個命令列引數：包含音訊串流的輸入檔名稱和輸出檔名稱。</span><span class="sxs-lookup"><span data-stu-id="19cc9-117">In this tutorial, you will create a console application that takes two command-line arguments: The name of an input file that contains an audio stream, and the output file name.</span></span> <span data-ttu-id="19cc9-118">應用程式會從輸入檔讀取五秒的音訊資料，並以 WAVE 資料的形式將音訊寫入輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="19cc9-118">The application reads five seconds of audio data from the input file and writes the audio to the output file as WAVE data.</span></span>

<span data-ttu-id="19cc9-119">若要取得已解碼的音訊資料，應用程式會使用來源讀取器物件。</span><span class="sxs-lookup"><span data-stu-id="19cc9-119">To get the decoded audio data, the application uses the source reader object.</span></span> <span data-ttu-id="19cc9-120">來源讀取器會公開 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 介面。</span><span class="sxs-lookup"><span data-stu-id="19cc9-120">The source reader exposes the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface.</span></span> <span data-ttu-id="19cc9-121">為了將解碼的音訊寫入 WAVE 檔案中，應用程式會使用 Windows i/o 函數。</span><span class="sxs-lookup"><span data-stu-id="19cc9-121">To write the decoded audio to the WAVE file, the applications uses Windows I/O functions.</span></span> <span data-ttu-id="19cc9-122">下圖說明此程式。</span><span class="sxs-lookup"><span data-stu-id="19cc9-122">The following image illustrates this process.</span></span>

![顯示來源讀取器從來源檔案取得音訊資料的圖表。](images/audio-clip-tutorial.gif)

<span data-ttu-id="19cc9-124">以最簡單的形式而言，WAVE 檔案具有下列結構：</span><span class="sxs-lookup"><span data-stu-id="19cc9-124">In its simplest form, a WAVE file has the following structure:</span></span>



| <span data-ttu-id="19cc9-125">資料類型</span><span class="sxs-lookup"><span data-stu-id="19cc9-125">Data Type</span></span>                              | <span data-ttu-id="19cc9-126">大小 (位元組)</span><span class="sxs-lookup"><span data-stu-id="19cc9-126">Size (Bytes)</span></span> | <span data-ttu-id="19cc9-127">值</span><span class="sxs-lookup"><span data-stu-id="19cc9-127">Value</span></span>                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| <span data-ttu-id="19cc9-128">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="19cc9-128">**FOURCC**</span></span>                             | <span data-ttu-id="19cc9-129">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-129">4</span></span>            | <span data-ttu-id="19cc9-130">RIFF</span><span class="sxs-lookup"><span data-stu-id="19cc9-130">'RIFF'</span></span>                                                                |
| <span data-ttu-id="19cc9-131">**Dword**</span><span class="sxs-lookup"><span data-stu-id="19cc9-131">**DWORD**</span></span>                              | <span data-ttu-id="19cc9-132">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-132">4</span></span>            | <span data-ttu-id="19cc9-133">檔案大小總計，不包含前8個位元組</span><span class="sxs-lookup"><span data-stu-id="19cc9-133">Total file size, not including the first 8 bytes</span></span>                      |
| <span data-ttu-id="19cc9-134">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="19cc9-134">**FOURCC**</span></span>                             | <span data-ttu-id="19cc9-135">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-135">4</span></span>            | <span data-ttu-id="19cc9-136">WAVE</span><span class="sxs-lookup"><span data-stu-id="19cc9-136">'WAVE'</span></span>                                                                |
| <span data-ttu-id="19cc9-137">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="19cc9-137">**FOURCC**</span></span>                             | <span data-ttu-id="19cc9-138">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-138">4</span></span>            | <span data-ttu-id="19cc9-139">bcp.fmt</span><span class="sxs-lookup"><span data-stu-id="19cc9-139">'fmt '</span></span>                                                                |
| <span data-ttu-id="19cc9-140">**Dword**</span><span class="sxs-lookup"><span data-stu-id="19cc9-140">**DWORD**</span></span>                              | <span data-ttu-id="19cc9-141">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-141">4</span></span>            | <span data-ttu-id="19cc9-142">接下來的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 資料大小。</span><span class="sxs-lookup"><span data-stu-id="19cc9-142">Size of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) data that follows.</span></span> |
| <span data-ttu-id="19cc9-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19cc9-143">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))</span></span> | <span data-ttu-id="19cc9-144">不定</span><span class="sxs-lookup"><span data-stu-id="19cc9-144">Varies</span></span>       | <span data-ttu-id="19cc9-145">音訊格式標頭。</span><span class="sxs-lookup"><span data-stu-id="19cc9-145">Audio format header.</span></span>                                                  |
| <span data-ttu-id="19cc9-146">**FOURCC**</span><span class="sxs-lookup"><span data-stu-id="19cc9-146">**FOURCC**</span></span>                             | <span data-ttu-id="19cc9-147">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-147">4</span></span>            | <span data-ttu-id="19cc9-148">data</span><span class="sxs-lookup"><span data-stu-id="19cc9-148">'data'</span></span>                                                                |
| <span data-ttu-id="19cc9-149">**Dword**</span><span class="sxs-lookup"><span data-stu-id="19cc9-149">**DWORD**</span></span>                              | <span data-ttu-id="19cc9-150">4</span><span class="sxs-lookup"><span data-stu-id="19cc9-150">4</span></span>            | <span data-ttu-id="19cc9-151">音訊資料的大小。</span><span class="sxs-lookup"><span data-stu-id="19cc9-151">Size of the audio data.</span></span>                                               |
| <span data-ttu-id="19cc9-152">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="19cc9-152">**BYTE**\[\]</span></span>                           | <span data-ttu-id="19cc9-153">不定</span><span class="sxs-lookup"><span data-stu-id="19cc9-153">Varies</span></span>       | <span data-ttu-id="19cc9-154">音訊資料。</span><span class="sxs-lookup"><span data-stu-id="19cc9-154">Audio data.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="19cc9-155">**FOURCC** 是串連四個 ASCII 字元所形成的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="19cc9-155">A **FOURCC** is a **DWORD** formed by concatenating four ASCII characters.</span></span>

 

<span data-ttu-id="19cc9-156">您可以藉由新增檔案中繼資料和其他資訊來擴充這個基本結構，但這已超出本教學課程的範圍。</span><span class="sxs-lookup"><span data-stu-id="19cc9-156">This basic structure can be extended by adding file metadata and other information, which is beyond the scope of this tutorial.</span></span>

## <a name="header-and-library-files"></a><span data-ttu-id="19cc9-157">標頭檔和程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="19cc9-157">Header and Library Files</span></span>

<span data-ttu-id="19cc9-158">在您的專案中包含下列標頭檔：</span><span class="sxs-lookup"><span data-stu-id="19cc9-158">Include the following header files in your project:</span></span>


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



<span data-ttu-id="19cc9-159">連結至下列程式庫：</span><span class="sxs-lookup"><span data-stu-id="19cc9-159">Link to the following libraries:</span></span>

-   <span data-ttu-id="19cc9-160">mfplat .lib</span><span class="sxs-lookup"><span data-stu-id="19cc9-160">mfplat.lib</span></span>
-   <span data-ttu-id="19cc9-161">mfreadwrite .lib</span><span class="sxs-lookup"><span data-stu-id="19cc9-161">mfreadwrite.lib</span></span>
-   <span data-ttu-id="19cc9-162">mfuuid .lib</span><span class="sxs-lookup"><span data-stu-id="19cc9-162">mfuuid.lib</span></span>

## <a name="implement-wmain"></a><span data-ttu-id="19cc9-163">執行 wmain</span><span class="sxs-lookup"><span data-stu-id="19cc9-163">Implement wmain</span></span>

<span data-ttu-id="19cc9-164">下列程式碼顯示應用程式的進入點函數。</span><span class="sxs-lookup"><span data-stu-id="19cc9-164">The following code shows the entry-point function for the application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        printf("arguments: input_file output_file.wav\n");
        return 1;
    }

    const WCHAR *wszSourceFile = argv[1];
    const WCHAR *wszTargetFile = argv[2];

    const LONG MAX_AUDIO_DURATION_MSEC = 5000; // 5 seconds

    HRESULT hr = S_OK;

    IMFSourceReader *pReader = NULL;
    HANDLE hFile = INVALID_HANDLE_VALUE;

    // Initialize the COM library.
    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    // Initialize the Media Foundation platform.
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
    }

    // Create the source reader to read the input file.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSourceReaderFromURL(wszSourceFile, NULL, &pReader);
        if (FAILED(hr))
        {
            printf("Error opening input file: %S\n", wszSourceFile, hr);
        }
    }

    // Open the output file for writing.
    if (SUCCEEDED(hr))
    {
        hFile = CreateFile(wszTargetFile, GENERIC_WRITE, FILE_SHARE_READ, NULL,
            CREATE_ALWAYS, 0, NULL);

        if (hFile == INVALID_HANDLE_VALUE)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            printf("Cannot create output file: %S\n", wszTargetFile, hr);
        }
    }

    // Write the WAVE file.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveFile(pReader, hFile, MAX_AUDIO_DURATION_MSEC);
    }

    if (FAILED(hr))
    {
        printf("Failed, hr = 0x%X\n", hr);
    }

    // Clean up.
    if (hFile != INVALID_HANDLE_VALUE)
    {
        CloseHandle(hFile);
    }

    SafeRelease(&pReader);
    MFShutdown();
    CoUninitialize();

    return SUCCEEDED(hr) ? 0 : 1;
};
```



<span data-ttu-id="19cc9-165">此函式會執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="19cc9-165">This function does the following:</span></span>

1.  <span data-ttu-id="19cc9-166">呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="19cc9-166">Calls [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the COM library.</span></span>
2.  <span data-ttu-id="19cc9-167">呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 以初始化媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="19cc9-167">Calls [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) to initialize the Media Foundation platform.</span></span>
3.  <span data-ttu-id="19cc9-168">呼叫 [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) 來建立來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="19cc9-168">Calls [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) to create the source reader.</span></span> <span data-ttu-id="19cc9-169">此函式會採用輸入檔的名稱，並接收 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="19cc9-169">This function takes the name of the input file and receives an [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) interface pointer.</span></span>
4.  <span data-ttu-id="19cc9-170">藉由呼叫 **CreateFile** 函式來建立輸出檔案，此函數會傳回檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="19cc9-170">Creates the output file by calling the **CreateFile** function, which returns a file handle.</span></span>
5.  <span data-ttu-id="19cc9-171">呼叫應用程式定義的 [WriteWavFile](#write-the-wave-file) 函數。</span><span class="sxs-lookup"><span data-stu-id="19cc9-171">Calls the application-defined [WriteWavFile](#write-the-wave-file) function.</span></span> <span data-ttu-id="19cc9-172">此函式會解碼音訊並寫入 WAVE 檔。</span><span class="sxs-lookup"><span data-stu-id="19cc9-172">This function decodes the audio and writes the WAVE file.</span></span>
6.  <span data-ttu-id="19cc9-173">釋放 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 指標和檔案控制代碼。</span><span class="sxs-lookup"><span data-stu-id="19cc9-173">Releases the [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) pointer and the file handle.</span></span>
7.  <span data-ttu-id="19cc9-174">呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 來關閉媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="19cc9-174">Calls [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Media Foundation platform.</span></span>
8.  <span data-ttu-id="19cc9-175">呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 以釋放 COM 程式庫。</span><span class="sxs-lookup"><span data-stu-id="19cc9-175">Calls [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) to release the COM library.</span></span>

## <a name="write-the-wave-file"></a><span data-ttu-id="19cc9-176">寫入 WAVE 檔案</span><span class="sxs-lookup"><span data-stu-id="19cc9-176">Write the WAVE File</span></span>

<span data-ttu-id="19cc9-177">大部分的工作會在函式中進行，而此函式 `WriteWavFile` 會從呼叫 `wmain` 。</span><span class="sxs-lookup"><span data-stu-id="19cc9-177">Most of the work happens in the `WriteWavFile` function, which is called from `wmain`.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveFile
//
// Writes a WAVE file by getting audio data from the source reader.
//
//-------------------------------------------------------------------

HRESULT WriteWaveFile(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    HANDLE hFile,               // Handle to the output file.
    LONG msecAudioData          // Maximum amount of audio data to write, in msec.
    )
{
    HRESULT hr = S_OK;

    DWORD cbHeader = 0;         // Size of the WAVE file header, in bytes.
    DWORD cbAudioData = 0;      // Total bytes of PCM audio data written to the file.
    DWORD cbMaxAudioData = 0;

    IMFMediaType *pAudioType = NULL;    // Represents the PCM audio format.

    // Configure the source reader to get uncompressed PCM audio from the source file.

    hr = ConfigureAudioStream(pReader, &pAudioType);

    // Write the WAVE file header.
    if (SUCCEEDED(hr))
    {
        hr = WriteWaveHeader(hFile, pAudioType, &cbHeader);
    }

    // Calculate the maximum amount of audio to decode, in bytes.
    if (SUCCEEDED(hr))
    {
        cbMaxAudioData = CalculateMaxAudioDataSize(pAudioType, cbHeader, msecAudioData);

        // Decode audio data to the file.
        hr = WriteWaveData(hFile, pReader, cbMaxAudioData, &cbAudioData);
    }

    // Fix up the RIFF headers with the correct sizes.
    if (SUCCEEDED(hr))
    {
        hr = FixUpChunkSizes(hFile, cbHeader, cbAudioData);
    }

    SafeRelease(&pAudioType);
    return hr;
}
```



<span data-ttu-id="19cc9-178">此函數會呼叫一系列的其他應用程式定義函數：</span><span class="sxs-lookup"><span data-stu-id="19cc9-178">This function calls a series of other application-defined functions:</span></span>

1.  <span data-ttu-id="19cc9-179">[ConfigureAudioStream](#configure-the-source-reader)函式會初始化來源讀取器。</span><span class="sxs-lookup"><span data-stu-id="19cc9-179">The [ConfigureAudioStream](#configure-the-source-reader) function initializes the source reader.</span></span> <span data-ttu-id="19cc9-180">此函式會接收指向 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標，此介面可用來取得已解碼音訊格式的描述，包括取樣率、通道數目，以及每個樣本) 的位深度 (位。</span><span class="sxs-lookup"><span data-stu-id="19cc9-180">This function receives a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which is used to get a description of the decoded audio format, including sample rate, number of channels, and bit depth (bits per sample).</span></span>
2.  <span data-ttu-id="19cc9-181">WriteWaveHeader 函式會寫入 WAVE 檔案的第一個部分，包括標頭和 ' data ' 區塊的開頭。</span><span class="sxs-lookup"><span data-stu-id="19cc9-181">The WriteWaveHeader function writes the first part of the WAVE file, including the header and the start of the 'data' chunk.</span></span>
3.  <span data-ttu-id="19cc9-182">CalculateMaxAudioDataSize 函式會計算要寫入檔案的最大音訊量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="19cc9-182">The CalculateMaxAudioDataSize function calculates the maximum amount of audio to write to the file, in bytes.</span></span>
4.  <span data-ttu-id="19cc9-183">WriteWaveData 函式會將 PCM 音訊資料寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="19cc9-183">The WriteWaveData function writes the PCM audio data to the file.</span></span>
5.  <span data-ttu-id="19cc9-184">FixUpChunkSizes 函式會寫入在 WAVE 檔案中的 ' RIFF ' 和 ' data ' **FOURCC** 值之後出現的檔案大小資訊。</span><span class="sxs-lookup"><span data-stu-id="19cc9-184">The FixUpChunkSizes function writes the file-size information that appears after the 'RIFF' and 'data' **FOURCC** values in the WAVE file.</span></span> <span data-ttu-id="19cc9-185"> (這些值在完成之前都是未知的 `WriteWaveData` 。 ) </span><span class="sxs-lookup"><span data-stu-id="19cc9-185">(These values are not known until `WriteWaveData` completes.)</span></span>

<span data-ttu-id="19cc9-186">本教學課程的其餘各節會顯示這些函式。</span><span class="sxs-lookup"><span data-stu-id="19cc9-186">These functions are shown in the remaining sections of this tutorial.</span></span>

## <a name="configure-the-source-reader"></a><span data-ttu-id="19cc9-187">設定來源讀取器</span><span class="sxs-lookup"><span data-stu-id="19cc9-187">Configure the Source Reader</span></span>

<span data-ttu-id="19cc9-188">此函式會設定 `ConfigureAudioStream` 來源讀取器，以解碼原始程式檔中的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="19cc9-188">The `ConfigureAudioStream` function configures the source reader to decode the audio stream in the source file.</span></span> <span data-ttu-id="19cc9-189">它也會傳回已解碼音訊格式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="19cc9-189">It also returns information about the format of the decoded audio.</span></span>

<span data-ttu-id="19cc9-190">在媒體基礎中，媒體格式會使用 *媒體類型* 物件來描述。</span><span class="sxs-lookup"><span data-stu-id="19cc9-190">In Media Foundation, media formats are described using *media type* objects.</span></span> <span data-ttu-id="19cc9-191">媒體類型物件會公開 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面，此介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="19cc9-191">A media type object exposes the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which inherits the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="19cc9-192">基本上，媒體類型是描述格式的屬性集合。</span><span class="sxs-lookup"><span data-stu-id="19cc9-192">Essentially, a media type is a collection of properties that describe the format.</span></span> <span data-ttu-id="19cc9-193">如需詳細資訊，請參閱 [媒體類型](media-types.md)。</span><span class="sxs-lookup"><span data-stu-id="19cc9-193">For more information, see [Media Types](media-types.md).</span></span>


```C++
//-------------------------------------------------------------------
// ConfigureAudioStream
//
// Selects an audio stream from the source file, and configures the
// stream to deliver decoded PCM audio.
//-------------------------------------------------------------------

HRESULT ConfigureAudioStream(
    IMFSourceReader *pReader,   // Pointer to the source reader.
    IMFMediaType **ppPCMAudio   // Receives the audio format.
    )
{
    IMFMediaType *pUncompressedAudioType = NULL;
    IMFMediaType *pPartialType = NULL;

    // Select the first audio stream, and deselect all other streams.
    HRESULT hr = pReader->SetStreamSelection(
        (DWORD)MF_SOURCE_READER_ALL_STREAMS, FALSE);

    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM, TRUE);
    }

    // Create a partial media type that specifies uncompressed PCM audio.
    hr = MFCreateMediaType(&pPartialType);

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Audio);
    }

    if (SUCCEEDED(hr))
    {
        hr = pPartialType->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_PCM);
    }

    // Set this type on the source reader. The source reader will
    // load the necessary decoder.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            NULL, pPartialType);
    }

    // Get the complete uncompressed format.
    if (SUCCEEDED(hr))
    {
        hr = pReader->GetCurrentMediaType(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            &pUncompressedAudioType);
    }

    // Ensure the stream is selected.
    if (SUCCEEDED(hr))
    {
        hr = pReader->SetStreamSelection(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            TRUE);
    }

    // Return the PCM format to the caller.
    if (SUCCEEDED(hr))
    {
        *ppPCMAudio = pUncompressedAudioType;
        (*ppPCMAudio)->AddRef();
    }

    SafeRelease(&pUncompressedAudioType);
    SafeRelease(&pPartialType);
    return hr;
}
```



<span data-ttu-id="19cc9-194">`ConfigureAudioStream`函數會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="19cc9-194">The `ConfigureAudioStream` function does the following:</span></span>

1.  <span data-ttu-id="19cc9-195">呼叫 [**IMFSourceReader：： SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) 方法來選取音訊串流，然後取消選取所有其他資料流程。</span><span class="sxs-lookup"><span data-stu-id="19cc9-195">Calls the [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) method to select the audio stream and deselect all other streams.</span></span> <span data-ttu-id="19cc9-196">此步驟可改善效能，因為它可防止來源讀取器保有應用程式未使用的影片畫面。</span><span class="sxs-lookup"><span data-stu-id="19cc9-196">This step can improve performance, because it prevents the source reader from holding onto video frames that the application does not use.</span></span>
2.  <span data-ttu-id="19cc9-197">建立指定 PCM 音訊的 *部分* 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="19cc9-197">Creates a *partial* media type that specifies PCM audio.</span></span> <span data-ttu-id="19cc9-198">函數會建立部分類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="19cc9-198">The function creates the partial type as follows:</span></span>
    1.  <span data-ttu-id="19cc9-199">呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 以建立空的媒體類型物件。</span><span class="sxs-lookup"><span data-stu-id="19cc9-199">Calls [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) to create an empty media type object.</span></span>
    2.  <span data-ttu-id="19cc9-200">將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為 [ **MFMediaType \_ 音訊**]。</span><span class="sxs-lookup"><span data-stu-id="19cc9-200">Sets the [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>
    3.  <span data-ttu-id="19cc9-201">將 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性設定為 **MFAudioFormat \_ PCM**。</span><span class="sxs-lookup"><span data-stu-id="19cc9-201">Sets the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute to **MFAudioFormat\_PCM**.</span></span>
3.  <span data-ttu-id="19cc9-202">呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) 來設定來源讀取器上的部分類型。</span><span class="sxs-lookup"><span data-stu-id="19cc9-202">Calls [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) to set the partial type on the source reader.</span></span> <span data-ttu-id="19cc9-203">如果來源檔案包含編碼的音訊，來源讀取器會自動載入必要的音訊解碼器。</span><span class="sxs-lookup"><span data-stu-id="19cc9-203">If the source file contains encoded audio, the source reader automatically loads the necessary audio decoder.</span></span>
4.  <span data-ttu-id="19cc9-204">呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) 來取得實際的 PCM 媒體類型。</span><span class="sxs-lookup"><span data-stu-id="19cc9-204">Calls [**IMFSourceReader::GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) to get the actual PCM media type.</span></span> <span data-ttu-id="19cc9-205">這個方法會傳回已填滿所有格式詳細資料的媒體類型，例如音訊取樣率和通道數目。</span><span class="sxs-lookup"><span data-stu-id="19cc9-205">This method returns a media type with all of the format details filled in, such as the audio sample rate and the number of channels.</span></span>
5.  <span data-ttu-id="19cc9-206">呼叫 [**IMFSourceReader：： SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) 來啟用音訊串流。</span><span class="sxs-lookup"><span data-stu-id="19cc9-206">Calls [**IMFSourceReader::SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) to enable the audio stream.</span></span>

## <a name="write-the-wave-file-header"></a><span data-ttu-id="19cc9-207">寫入 WAVE 檔案標頭</span><span class="sxs-lookup"><span data-stu-id="19cc9-207">Write the WAVE File Header</span></span>

<span data-ttu-id="19cc9-208">`WriteWaveHeader`函數會寫入 WAVE 檔案標頭。</span><span class="sxs-lookup"><span data-stu-id="19cc9-208">The `WriteWaveHeader` function writes the WAVE file header.</span></span>

<span data-ttu-id="19cc9-209">這個函式所呼叫的唯一媒體基礎 API 是 [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)，它會將媒體類型轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。</span><span class="sxs-lookup"><span data-stu-id="19cc9-209">The only Media Foundation API called from this function is [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype), which converts the media type to a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveHeader
//
// Write the WAVE file header.
//
// Note: This function writes placeholder values for the file size
// and data size, as these values will need to be filled in later.
//-------------------------------------------------------------------

HRESULT WriteWaveHeader(
    HANDLE hFile,               // Output file.
    IMFMediaType *pMediaType,   // PCM audio format.
    DWORD *pcbWritten           // Receives the size of the header.
    )
{
    HRESULT hr = S_OK;
    UINT32 cbFormat = 0;

    WAVEFORMATEX *pWav = NULL;

    *pcbWritten = 0;

    // Convert the PCM audio format into a WAVEFORMATEX structure.
    hr = MFCreateWaveFormatExFromMFMediaType(pMediaType, &pWav, &cbFormat);

    // Write the 'RIFF' header and the start of the 'fmt ' chunk.
    if (SUCCEEDED(hr))
    {
        DWORD header[] = {
            // RIFF header
            FCC('RIFF'),
            0,
            FCC('WAVE'),
            // Start of 'fmt ' chunk
            FCC('fmt '),
            cbFormat
        };

        DWORD dataHeader[] = { FCC('data'), 0 };

        hr = WriteToFile(hFile, header, sizeof(header));

        // Write the WAVEFORMATEX structure.
        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, pWav, cbFormat);
        }

        // Write the start of the 'data' chunk

        if (SUCCEEDED(hr))
        {
            hr = WriteToFile(hFile, dataHeader, sizeof(dataHeader));
        }

        if (SUCCEEDED(hr))
        {
            *pcbWritten = sizeof(header) + cbFormat + sizeof(dataHeader);
        }
    }


    CoTaskMemFree(pWav);
    return hr;
}
```



<span data-ttu-id="19cc9-210">函式 `WriteToFile` 是簡單的 helper 函式，它會包裝 Windows **WriteFile** 函式並傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="19cc9-210">The `WriteToFile` function is a simple helper function that wraps the Windows **WriteFile** function and returns an **HRESULT** value.</span></span>


```C++
//-------------------------------------------------------------------
//
// Writes a block of data to a file
//
// hFile: Handle to the file.
// p: Pointer to the buffer to write.
// cb: Size of the buffer, in bytes.
//
//-------------------------------------------------------------------

HRESULT WriteToFile(HANDLE hFile, void* p, DWORD cb)
{
    DWORD cbWritten = 0;
    HRESULT hr = S_OK;

    BOOL bResult = WriteFile(hFile, p, cb, &cbWritten, NULL);
    if (!bResult)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



## <a name="calculate-the-maximum-data-size"></a><span data-ttu-id="19cc9-211">計算資料大小上限</span><span class="sxs-lookup"><span data-stu-id="19cc9-211">Calculate the Maximum Data Size</span></span>

<span data-ttu-id="19cc9-212">因為檔案大小會在檔案標頭中儲存為4位元組值，所以 WAVE 檔案的大小上限為0xFFFFFFFF 個位元組，大約 4 GB。</span><span class="sxs-lookup"><span data-stu-id="19cc9-212">Because the file size is stored as a 4-byte value in the file header, a WAVE file is limited to a maximum size of 0xFFFFFFFF bytes—approximately 4 GB.</span></span> <span data-ttu-id="19cc9-213">此值包含檔案標頭的大小。</span><span class="sxs-lookup"><span data-stu-id="19cc9-213">This value includes the size of the file header.</span></span> <span data-ttu-id="19cc9-214">PCM 音訊具有固定的位元速率，因此您可以從音訊格式計算資料大小上限，如下所示：</span><span class="sxs-lookup"><span data-stu-id="19cc9-214">PCM audio has a constant bit rate, so you can calculate the maximum data size from the audio format, as follows:</span></span>


```C++
//-------------------------------------------------------------------
// CalculateMaxAudioDataSize
//
// Calculates how much audio to write to the WAVE file, given the
// audio format and the maximum duration of the WAVE file.
//-------------------------------------------------------------------

DWORD CalculateMaxAudioDataSize(
    IMFMediaType *pAudioType,    // The PCM audio format.
    DWORD cbHeader,              // The size of the WAVE file header.
    DWORD msecAudioData          // Maximum duration, in milliseconds.
    )
{
    UINT32 cbBlockSize = 0;         // Audio frame size, in bytes.
    UINT32 cbBytesPerSecond = 0;    // Bytes per second.

    // Get the audio block size and number of bytes/second from the audio format.

    cbBlockSize = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_BLOCK_ALIGNMENT, 0);
    cbBytesPerSecond = MFGetAttributeUINT32(pAudioType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);

    // Calculate the maximum amount of audio data to write.
    // This value equals (duration in seconds x bytes/second), but cannot
    // exceed the maximum size of the data chunk in the WAVE file.

        // Size of the desired audio clip in bytes:
    DWORD cbAudioClipSize = (DWORD)MulDiv(cbBytesPerSecond, msecAudioData, 1000);

    // Largest possible size of the data chunk:
    DWORD cbMaxSize = MAXDWORD - cbHeader;

    // Maximum size altogether.
    cbAudioClipSize = min(cbAudioClipSize, cbMaxSize);

    // Round to the audio block size, so that we do not write a partial audio frame.
    cbAudioClipSize = (cbAudioClipSize / cbBlockSize) * cbBlockSize;

    return cbAudioClipSize;
}
```



<span data-ttu-id="19cc9-215">為了避免部分的音訊畫面格，大小會四捨五入至區塊對齊，並儲存在 [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="19cc9-215">To avoid partial audio frames, the size is rounded to the block alignment, which is stored in the [**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md) attribute.</span></span>

## <a name="decode-the-audio"></a><span data-ttu-id="19cc9-216">解碼音訊</span><span class="sxs-lookup"><span data-stu-id="19cc9-216">Decode the Audio</span></span>

<span data-ttu-id="19cc9-217">函式會 `WriteWaveData` 從來源檔案讀取解碼的音訊，並寫入 WAVE 檔案。</span><span class="sxs-lookup"><span data-stu-id="19cc9-217">The `WriteWaveData` function reads decoded audio from the source file and writes to the WAVE file.</span></span>


```C++
//-------------------------------------------------------------------
// WriteWaveData
//
// Decodes PCM audio data from the source file and writes it to
// the WAVE file.
//-------------------------------------------------------------------

HRESULT WriteWaveData(
    HANDLE hFile,               // Output file.
    IMFSourceReader *pReader,   // Source reader.
    DWORD cbMaxAudioData,       // Maximum amount of audio data (bytes).
    DWORD *pcbDataWritten       // Receives the amount of data written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbAudioData = 0;
    DWORD cbBuffer = 0;
    BYTE *pAudioData = NULL;

    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Get audio samples from the source reader.
    while (true)
    {
        DWORD dwFlags = 0;

        // Read the next sample.
        hr = pReader->ReadSample(
            (DWORD)MF_SOURCE_READER_FIRST_AUDIO_STREAM,
            0, NULL, &dwFlags, NULL, &pSample );

        if (FAILED(hr)) { break; }

        if (dwFlags & MF_SOURCE_READERF_CURRENTMEDIATYPECHANGED)
        {
            printf("Type change - not supported by WAVE file format.\n");
            break;
        }
        if (dwFlags & MF_SOURCE_READERF_ENDOFSTREAM)
        {
            printf("End of input file.\n");
            break;
        }

        if (pSample == NULL)
        {
            printf("No sample\n");
            continue;
        }

        // Get a pointer to the audio data in the sample.

        hr = pSample->ConvertToContiguousBuffer(&pBuffer);

        if (FAILED(hr)) { break; }


        hr = pBuffer->Lock(&pAudioData, NULL, &cbBuffer);

        if (FAILED(hr)) { break; }


        // Make sure not to exceed the specified maximum size.
        if (cbMaxAudioData - cbAudioData < cbBuffer)
        {
            cbBuffer = cbMaxAudioData - cbAudioData;
        }

        // Write this data to the output file.
        hr = WriteToFile(hFile, pAudioData, cbBuffer);

        if (FAILED(hr)) { break; }

        // Unlock the buffer.
        hr = pBuffer->Unlock();
        pAudioData = NULL;

        if (FAILED(hr)) { break; }

        // Update running total of audio data.
        cbAudioData += cbBuffer;

        if (cbAudioData >= cbMaxAudioData)
        {
            break;
        }

        SafeRelease(&pSample);
        SafeRelease(&pBuffer);
    }

    if (SUCCEEDED(hr))
    {
        printf("Wrote %d bytes of audio data.\n", cbAudioData);

        *pcbDataWritten = cbAudioData;
    }

    if (pAudioData)
    {
        pBuffer->Unlock();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pSample);
    return hr;
}
```



<span data-ttu-id="19cc9-218">`WriteWaveData`函數會在迴圈中執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="19cc9-218">The `WriteWaveData` function does the following in a loop:</span></span>

1.  <span data-ttu-id="19cc9-219">呼叫 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，以從來源檔案讀取音訊。</span><span class="sxs-lookup"><span data-stu-id="19cc9-219">Calls [**IMFSourceReader::ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) to read audio from the source file.</span></span> <span data-ttu-id="19cc9-220">*DwFlags* 參數會從 [**MF \_ 來源 \_ 讀取器 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag)標列舉，接收位 **or** 的旗標。</span><span class="sxs-lookup"><span data-stu-id="19cc9-220">The *dwFlags* parameter receives a bitwise **OR** of flags from the [**MF\_SOURCE\_READER\_FLAG**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag) enumeration.</span></span> <span data-ttu-id="19cc9-221">*PSample* 參數會接收 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)介面的指標，該介面可用來存取音訊資料。</span><span class="sxs-lookup"><span data-stu-id="19cc9-221">The *pSample* parameter receives a pointer to the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, which is used to access the audio data.</span></span> <span data-ttu-id="19cc9-222">在某些情況下，呼叫 **ReadSample** 不會產生資料，在此情況下， **IMFSample** 指標為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="19cc9-222">In some cases a call to **ReadSample** does not generate data, in which case the **IMFSample** pointer is **NULL**.</span></span>
2.  <span data-ttu-id="19cc9-223">檢查 *dwFlags* 是否有下列旗標：</span><span class="sxs-lookup"><span data-stu-id="19cc9-223">Checks *dwFlags* for the following flags:</span></span>
    -   <span data-ttu-id="19cc9-224">**MF \_來源 \_ READERF \_ CURRENTMEDIATYPECHANGED**。</span><span class="sxs-lookup"><span data-stu-id="19cc9-224">**MF\_SOURCE\_READERF\_CURRENTMEDIATYPECHANGED**.</span></span> <span data-ttu-id="19cc9-225">此旗標表示原始檔中的格式變更。</span><span class="sxs-lookup"><span data-stu-id="19cc9-225">This flag indicates a format change in the source file.</span></span> <span data-ttu-id="19cc9-226">WAVE 檔案不支援格式變更。</span><span class="sxs-lookup"><span data-stu-id="19cc9-226">WAVE files do not support format changes.</span></span>
    -   <span data-ttu-id="19cc9-227">**MF \_來源 \_ READERF \_ ENDOFSTREAM**。</span><span class="sxs-lookup"><span data-stu-id="19cc9-227">**MF\_SOURCE\_READERF\_ENDOFSTREAM**.</span></span> <span data-ttu-id="19cc9-228">此旗標表示資料流程的結尾。</span><span class="sxs-lookup"><span data-stu-id="19cc9-228">This flag indicates the end of the stream.</span></span>
3.  <span data-ttu-id="19cc9-229">呼叫 [**IMFSample：： ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) 來取得緩衝區物件的指標。</span><span class="sxs-lookup"><span data-stu-id="19cc9-229">Calls [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) to get a pointer to a buffer object.</span></span>
4.  <span data-ttu-id="19cc9-230">呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得緩衝區記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="19cc9-230">Calls [**IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) to get a pointer to the buffer memory.</span></span>
5.  <span data-ttu-id="19cc9-231">將音訊資料寫入輸出檔。</span><span class="sxs-lookup"><span data-stu-id="19cc9-231">Writes the audio data to the output file.</span></span>
6.  <span data-ttu-id="19cc9-232">呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區物件。</span><span class="sxs-lookup"><span data-stu-id="19cc9-232">Calls [**IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) to unlock the buffer object.</span></span>

<span data-ttu-id="19cc9-233">當發生下列任何情況時，函式會中斷迴圈：</span><span class="sxs-lookup"><span data-stu-id="19cc9-233">The function breaks out of the loop when any of the following occur:</span></span>

-   <span data-ttu-id="19cc9-234">資料流程格式會變更。</span><span class="sxs-lookup"><span data-stu-id="19cc9-234">The stream format changes.</span></span>
-   <span data-ttu-id="19cc9-235">已到達資料流的末端。</span><span class="sxs-lookup"><span data-stu-id="19cc9-235">The end of the stream is reached.</span></span>
-   <span data-ttu-id="19cc9-236">音訊資料的最大數量會寫入輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="19cc9-236">The maximum amount of audio data is written to the output file.</span></span>
-   <span data-ttu-id="19cc9-237">發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="19cc9-237">An error occurs.</span></span>

## <a name="finalize-the-file-header"></a><span data-ttu-id="19cc9-238">完成檔案標頭</span><span class="sxs-lookup"><span data-stu-id="19cc9-238">Finalize the File Header</span></span>

<span data-ttu-id="19cc9-239">在前一個函式完成之前，不知道儲存在 WAVE 標頭中的大小值。</span><span class="sxs-lookup"><span data-stu-id="19cc9-239">The size values that are stored in the WAVE header are not known until the previous function completes.</span></span> <span data-ttu-id="19cc9-240">會 `FixUpChunkSizes` 填入下列值：</span><span class="sxs-lookup"><span data-stu-id="19cc9-240">The `FixUpChunkSizes` fills in these values:</span></span>


```C++
//-------------------------------------------------------------------
// FixUpChunkSizes
//
// Writes the file-size information into the WAVE file header.
//
// WAVE files use the RIFF file format. Each RIFF chunk has a data
// size, and the RIFF header has a total file size.
//-------------------------------------------------------------------

HRESULT FixUpChunkSizes(
    HANDLE hFile,           // Output file.
    DWORD cbHeader,         // Size of the 'fmt ' chuck.
    DWORD cbAudioData       // Size of the 'data' chunk.
    )
{
    HRESULT hr = S_OK;

    LARGE_INTEGER ll;
    ll.QuadPart = cbHeader - sizeof(DWORD);

    if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    // Write the data size.

    if (SUCCEEDED(hr))
    {
        hr = WriteToFile(hFile, &cbAudioData, sizeof(cbAudioData));
    }

    if (SUCCEEDED(hr))
    {
        // Write the file size.
        ll.QuadPart = sizeof(FOURCC);

        if (0 == SetFilePointerEx(hFile, ll, NULL, FILE_BEGIN))
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        DWORD cbRiffFileSize = cbHeader + cbAudioData - 8;

        // NOTE: The "size" field in the RIFF header does not include
        // the first 8 bytes of the file. (That is, the size of the
        // data that appears after the size field.)

        hr = WriteToFile(hFile, &cbRiffFileSize, sizeof(cbRiffFileSize));
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="19cc9-241">相關主題</span><span class="sxs-lookup"><span data-stu-id="19cc9-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19cc9-242">音訊媒體類型</span><span class="sxs-lookup"><span data-stu-id="19cc9-242">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="19cc9-243">來源讀取程式</span><span class="sxs-lookup"><span data-stu-id="19cc9-243">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="19cc9-244">**IMFSourceReader**</span><span class="sxs-lookup"><span data-stu-id="19cc9-244">**IMFSourceReader**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
