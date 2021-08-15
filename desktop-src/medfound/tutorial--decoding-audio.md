---
description: 本教學課程示範如何使用來源讀取器將音訊從媒體檔案解碼，並將音訊寫入 WAVE 檔案。
ms.assetid: ed40e201-c6ed-444f-bdaa-a5f33d1cc068
title: 教學課程：解碼音訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ad5dbac47680c4d8faa73affa711b987edf220e05324d88cd0ffbda3bb93e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237660"
---
# <a name="tutorial-decoding-audio"></a>教學課程：解碼音訊

本教學課程示範如何使用 [來源讀取器](source-reader.md) 將音訊從媒體檔案解碼，並將音訊寫入 WAVE 檔案。 本教學課程是以 [音訊剪輯](audio-clip-sample.md) 範例為基礎。

-   [概觀](#overview)
-   [標頭檔和程式庫檔案](#header-and-library-files)
-   [執行 wmain](#implement-wmain)
-   [寫入 WAVE 檔案](#write-the-wave-file)
-   [設定來源讀取器](#configure-the-source-reader)
-   [寫入 WAVE 檔案標頭](#write-the-wave-file-header)
-   [計算資料大小上限](#calculate-the-maximum-data-size)
-   [解碼音訊](#decode-the-audio)
-   [完成檔案標頭](#finalize-the-file-header)
-   [相關主題](#related-topics)

## <a name="overview"></a>概觀

在本教學課程中，您將建立一個主控台應用程式，該應用程式會採用兩個命令列引數：包含音訊串流的輸入檔名稱和輸出檔名稱。 應用程式會從輸入檔讀取五秒的音訊資料，並以 WAVE 資料的形式將音訊寫入輸出檔案。

若要取得已解碼的音訊資料，應用程式會使用來源讀取器物件。 來源讀取器會公開 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 介面。 為了將解碼的音訊寫入 WAVE 檔案中，應用程式會使用 Windows i/o 函數。 下圖說明此程式。

![顯示來源讀取器從來源檔案取得音訊資料的圖表。](images/audio-clip-tutorial.gif)

以最簡單的形式而言，WAVE 檔案具有下列結構：



| 資料類型                              | 大小 (位元組) | 值                                                                 |
|----------------------------------------|--------------|-----------------------------------------------------------------------|
| **FOURCC**                             | 4            | RIFF                                                                |
| **Dword**                              | 4            | 檔案大小總計，不包含前8個位元組                      |
| **FOURCC**                             | 4            | WAVE                                                                |
| **FOURCC**                             | 4            | bcp.fmt                                                                |
| **Dword**                              | 4            | 接下來的 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 資料大小。 |
| [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) | 不定       | 音訊格式標頭。                                                  |
| **FOURCC**                             | 4            | data                                                                |
| **Dword**                              | 4            | 音訊資料的大小。                                               |
| **位元組**\[\]                           | 不定       | 音訊資料。                                                           |



 

> [!Note]  
> **FOURCC** 是串連四個 ASCII 字元所形成的 **DWORD** 。

 

您可以藉由新增檔案中繼資料和其他資訊來擴充這個基本結構，但這已超出本教學課程的範圍。

## <a name="header-and-library-files"></a>標頭檔和程式庫檔案

在您的專案中包含下列標頭檔：


```C++
#define WINVER _WIN32_WINNT_WIN7

#include <windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <mfreadwrite.h>
#include <stdio.h>
#include <mferror.h>
```



連結至下列程式庫：

-   mfplat .lib
-   mfreadwrite .lib
-   mfuuid .lib

## <a name="implement-wmain"></a>執行 wmain

下列程式碼顯示應用程式的進入點函數。


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



此函式會執行下列工作：

1.  呼叫 [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) 以初始化 COM 程式庫。
2.  呼叫 [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) 以初始化媒體基礎平臺。
3.  呼叫 [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl) 來建立來源讀取器。 此函式會採用輸入檔的名稱，並接收 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 介面指標。
4.  藉由呼叫 **CreateFile** 函式來建立輸出檔案，此函數會傳回檔案控制代碼。
5.  呼叫應用程式定義的 [WriteWavFile](#write-the-wave-file) 函數。 此函式會解碼音訊並寫入 WAVE 檔。
6.  釋放 [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader) 指標和檔案控制代碼。
7.  呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) 來關閉媒體基礎平臺。
8.  呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 以釋放 COM 程式庫。

## <a name="write-the-wave-file"></a>寫入 WAVE 檔案

大部分的工作會在函式中進行，而此函式 `WriteWavFile` 會從呼叫 `wmain` 。


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



此函數會呼叫一系列的其他應用程式定義函數：

1.  [ConfigureAudioStream](#configure-the-source-reader)函式會初始化來源讀取器。 此函式會接收指向 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面的指標，此介面可用來取得已解碼音訊格式的描述，包括取樣率、通道數目，以及每個樣本) 的位深度 (位。
2.  WriteWaveHeader 函式會寫入 WAVE 檔案的第一個部分，包括標頭和 ' data ' 區塊的開頭。
3.  CalculateMaxAudioDataSize 函式會計算要寫入檔案的最大音訊量（以位元組為單位）。
4.  WriteWaveData 函式會將 PCM 音訊資料寫入檔案。
5.  FixUpChunkSizes 函式會寫入在 WAVE 檔案中的 ' RIFF ' 和 ' data ' **FOURCC** 值之後出現的檔案大小資訊。  (這些值在完成之前都是未知的 `WriteWaveData` 。 ) 

本教學課程的其餘各節會顯示這些函式。

## <a name="configure-the-source-reader"></a>設定來源讀取器

此函式會設定 `ConfigureAudioStream` 來源讀取器，以解碼原始程式檔中的音訊串流。 它也會傳回已解碼音訊格式的相關資訊。

在媒體基礎中，媒體格式會使用 *媒體類型* 物件來描述。 媒體類型物件會公開 [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) 介面，此介面會繼承 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。 基本上，媒體類型是描述格式的屬性集合。 如需詳細資訊，請參閱 [媒體類型](media-types.md)。


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



`ConfigureAudioStream`函數會執行下列動作：

1.  呼叫 [**IMFSourceReader：： SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) 方法來選取音訊串流，然後取消選取所有其他資料流程。 此步驟可改善效能，因為它可防止來源讀取器保有應用程式未使用的影片畫面。
2.  建立指定 PCM 音訊的 *部分* 媒體類型。 函數會建立部分類型，如下所示：
    1.  呼叫 [**MFCreateMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype) 以建立空的媒體類型物件。
    2.  將 [ [**MF \_ MT \_ 主要 \_ 類型**](mf-mt-major-type-attribute.md) ] 屬性設定為 [ **MFMediaType \_ 音訊**]。
    3.  將 [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md) 屬性設定為 **MFAudioFormat \_ PCM**。
3.  呼叫 [**IMFSourceReader：： SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype) 來設定來源讀取器上的部分類型。 如果來源檔案包含編碼的音訊，來源讀取器會自動載入必要的音訊解碼器。
4.  呼叫 [**IMFSourceReader：： GetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getcurrentmediatype) 來取得實際的 PCM 媒體類型。 這個方法會傳回已填滿所有格式詳細資料的媒體類型，例如音訊取樣率和通道數目。
5.  呼叫 [**IMFSourceReader：： SetStreamSelection**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setstreamselection) 來啟用音訊串流。

## <a name="write-the-wave-file-header"></a>寫入 WAVE 檔案標頭

`WriteWaveHeader`函數會寫入 WAVE 檔案標頭。

這個函式所呼叫的唯一媒體基礎 API 是 [**MFCreateWaveFormatExFromMFMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)，它會將媒體類型轉換成 [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) 結構。


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



函式 `WriteToFile` 是簡單的 helper 函式，可包裝 Windows 的 **WriteFile** 函式，並傳回 **HRESULT** 值。


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



## <a name="calculate-the-maximum-data-size"></a>計算資料大小上限

因為檔案大小會在檔案標頭中儲存為4位元組值，所以 WAVE 檔案的大小上限為0xFFFFFFFF 個位元組，大約 4 GB。 此值包含檔案標頭的大小。 PCM 音訊具有固定的位元速率，因此您可以從音訊格式計算資料大小上限，如下所示：


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



為了避免部分的音訊畫面格，大小會四捨五入至區塊對齊，並儲存在 [**MF \_ MT \_ 音訊 \_ 區塊 \_ 對齊**](mf-mt-audio-block-alignment-attribute.md) 屬性中。

## <a name="decode-the-audio"></a>解碼音訊

函式會 `WriteWaveData` 從來源檔案讀取解碼的音訊，並寫入 WAVE 檔案。


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



`WriteWaveData`函數會在迴圈中執行下列動作：

1.  呼叫 [**IMFSourceReader：： ReadSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-readsample) ，以從來源檔案讀取音訊。 *DwFlags* 參數會從 [**MF \_ 來源 \_ 讀取器 \_ 旗**](/windows/desktop/api/mfreadwrite/ne-mfreadwrite-mf_source_reader_flag)標列舉，接收位 **or** 的旗標。 *PSample* 參數會接收 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)介面的指標，該介面可用來存取音訊資料。 在某些情況下，呼叫 **ReadSample** 不會產生資料，在此情況下， **IMFSample** 指標為 **Null**。
2.  檢查 *dwFlags* 是否有下列旗標：
    -   **MF \_來源 \_ READERF \_ CURRENTMEDIATYPECHANGED**。 此旗標表示原始檔中的格式變更。 WAVE 檔案不支援格式變更。
    -   **MF \_來源 \_ READERF \_ ENDOFSTREAM**。 此旗標表示資料流程的結尾。
3.  呼叫 [**IMFSample：： ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer) 來取得緩衝區物件的指標。
4.  呼叫 [**IMFMediaBuffer：： Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) 以取得緩衝區記憶體的指標。
5.  將音訊資料寫入輸出檔。
6.  呼叫 [**IMFMediaBuffer：： unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) 以解除鎖定緩衝區物件。

當發生下列任何情況時，函式會中斷迴圈：

-   資料流程格式會變更。
-   已到達資料流的末端。
-   音訊資料的最大數量會寫入輸出檔案。
-   發生錯誤。

## <a name="finalize-the-file-header"></a>完成檔案標頭

在前一個函式完成之前，不知道儲存在 WAVE 標頭中的大小值。 會 `FixUpChunkSizes` 填入下列值：


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



## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊媒體類型](audio-media-types.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 
