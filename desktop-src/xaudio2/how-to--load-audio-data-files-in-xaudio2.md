---
description: 本主題說明在 XAudio2 中填入播放音訊資料所需結構的步驟。
ms.assetid: caeb522e-d4f6-91e2-5e85-ea0af0f61300
title: 使用方法：在 XAudio2 中載入音訊資料檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659b4d8e106b6f0b2eb942505f99562f56fdada7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113649"
---
# <a name="how-to-load-audio-data-files-in-xaudio2"></a><span data-ttu-id="8b928-103">使用方法：在 XAudio2 中載入音訊資料檔</span><span class="sxs-lookup"><span data-stu-id="8b928-103">How to: Load Audio Data Files in XAudio2</span></span>

> [!Note]  
> <span data-ttu-id="8b928-104">此內容僅適用于桌面應用程式，且需要在 Windows Store 應用程式中使用修訂功能。</span><span class="sxs-lookup"><span data-stu-id="8b928-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="8b928-105">請參閱 [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2)、 [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)、 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)、 [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)和 [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex)的檔。</span><span class="sxs-lookup"><span data-stu-id="8b928-105">Please refer to the documentation for [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2), [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex).</span></span> <span data-ttu-id="8b928-106">請參閱 [Windows SDK 範例庫](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208))中的 BasicSound Windows 8 範例中的 SoundFileReader .h/.cpp。</span><span class="sxs-lookup"><span data-stu-id="8b928-106">See SoundFileReader.h/.cpp in the BasicSound Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="8b928-107">本主題說明在 XAudio2 中填入播放音訊資料所需結構的步驟。</span><span class="sxs-lookup"><span data-stu-id="8b928-107">This topic describes the steps to populate the structures required to play audio data in XAudio2.</span></span> <span data-ttu-id="8b928-108">下列步驟會載入音訊檔案的 ' bcp.fmt ' 和 ' data ' 區塊，並使用它們來填入 **WAVEFORMATEXTENSIBLE** 結構和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-108">The following steps load the 'fmt ' and 'data' chunks of an audio file, and uses them to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>

-   [<span data-ttu-id="8b928-109">正在準備剖析音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="8b928-109">Preparing to parse the audio file.</span></span>](#preparing-to-parse-the-audio-file)
-   [<span data-ttu-id="8b928-110">以 RIFF 區塊的內容填入 XAudio2 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-110">Populating XAudio2 structures with the contents of RIFF chunks.</span></span>](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a><span data-ttu-id="8b928-111">準備剖析音訊檔案</span><span class="sxs-lookup"><span data-stu-id="8b928-111">Preparing to parse the audio file</span></span>

<span data-ttu-id="8b928-112">XAudio2 支援的音訊檔案會使用資源交換檔案格式 (RIFF) 。</span><span class="sxs-lookup"><span data-stu-id="8b928-112">Audio files supported by XAudio2 use the Resource Interchange File Format (RIFF).</span></span> <span data-ttu-id="8b928-113">[ (RIFF) 總覽的資源交換檔案格式](resource-interchange-file-format--riff-.md)中會說明 RIFF。</span><span class="sxs-lookup"><span data-stu-id="8b928-113">RIFF is described in the [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md) overview.</span></span> <span data-ttu-id="8b928-114">RIFF 檔案中的音訊資料是藉由尋找 RIFF 區塊來載入，然後在區塊之間進行迴圈，以尋找包含在 RIFF 區塊中的個別區塊。</span><span class="sxs-lookup"><span data-stu-id="8b928-114">Audio data in a RIFF file is loaded by finding the RIFF chunk and then looping through the chunk to find individual chunks contained in the RIFF chunk.</span></span> <span data-ttu-id="8b928-115">下列函式是用來尋找區塊的程式碼範例，以及包含在區塊中的載入資料。</span><span class="sxs-lookup"><span data-stu-id="8b928-115">The following functions are examples of code to find chunks and load data contained in the chunks.</span></span>

-   <span data-ttu-id="8b928-116">若要在 RIFF 檔中尋找區塊：</span><span class="sxs-lookup"><span data-stu-id="8b928-116">To find a chunk in a RIFF file:</span></span>

    ```
    #ifdef _XBOX //Big-Endian
    #define fourccRIFF 'RIFF'
    #define fourccDATA 'data'
    #define fourccFMT 'fmt '
    #define fourccWAVE 'WAVE'
    #define fourccXWMA 'XWMA'
    #define fourccDPDS 'dpds'
    #endif

    #ifndef _XBOX //Little-Endian
    #define fourccRIFF 'FFIR'
    #define fourccDATA 'atad'
    #define fourccFMT ' tmf'
    #define fourccWAVE 'EVAW'
    #define fourccXWMA 'AMWX'
    #define fourccDPDS 'sdpd'
    #endif
    HRESULT FindChunk(HANDLE hFile, DWORD fourcc, DWORD & dwChunkSize, DWORD & dwChunkDataPosition)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );

        DWORD dwChunkType;
        DWORD dwChunkDataSize;
        DWORD dwRIFFDataSize = 0;
        DWORD dwFileType;
        DWORD bytesRead = 0;
        DWORD dwOffset = 0;

        while (hr == S_OK)
        {
            DWORD dwRead;
            if( 0 == ReadFile( hFile, &dwChunkType, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            if( 0 == ReadFile( hFile, &dwChunkDataSize, sizeof(DWORD), &dwRead, NULL ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );

            switch (dwChunkType)
            {
            case fourccRIFF:
                dwRIFFDataSize = dwChunkDataSize;
                dwChunkDataSize = 4;
                if( 0 == ReadFile( hFile, &dwFileType, sizeof(DWORD), &dwRead, NULL ) )
                    hr = HRESULT_FROM_WIN32( GetLastError() );
                break;

            default:
                if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, dwChunkDataSize, NULL, FILE_CURRENT ) )
                return HRESULT_FROM_WIN32( GetLastError() );            
            }

            dwOffset += sizeof(DWORD) * 2;
            
            if (dwChunkType == fourcc)
            {
                dwChunkSize = dwChunkDataSize;
                dwChunkDataPosition = dwOffset;
                return S_OK;
            }

            dwOffset += dwChunkDataSize;
            
            if (bytesRead >= dwRIFFDataSize) return S_FALSE;

        }

        return S_OK;
        
    }
    ```

    

-   <span data-ttu-id="8b928-117">在區塊中讀取資料之後的資料。</span><span class="sxs-lookup"><span data-stu-id="8b928-117">To read data in a chunk after it has been located.</span></span>

    <span data-ttu-id="8b928-118">一旦找到所需的區塊，就可以藉由將檔案指標調整至區塊資料區段的開頭，來讀取其資料。</span><span class="sxs-lookup"><span data-stu-id="8b928-118">Once a desired chunk is found, its data can be read by adjusting the file pointer to the beginning of the data section of the chunk.</span></span> <span data-ttu-id="8b928-119">在找到區塊之後，從區塊讀取資料的函式可能會如下所示。</span><span class="sxs-lookup"><span data-stu-id="8b928-119">A function to read the data from a chunk once it is found might look like this.</span></span>

    ```
    HRESULT ReadChunkData(HANDLE hFile, void * buffer, DWORD buffersize, DWORD bufferoffset)
    {
        HRESULT hr = S_OK;
        if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, bufferoffset, NULL, FILE_BEGIN ) )
            return HRESULT_FROM_WIN32( GetLastError() );
        DWORD dwRead;
        if( 0 == ReadFile( hFile, buffer, buffersize, &dwRead, NULL ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
        return hr;
    }
    ```

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a><span data-ttu-id="8b928-120">以 RIFF 區塊的內容填入 XAudio2 結構</span><span class="sxs-lookup"><span data-stu-id="8b928-120">Populating XAudio2 structures with the contents of RIFF chunks</span></span>

<span data-ttu-id="8b928-121">為了讓 XAudio2 能夠以來源聲音播放音訊，它需要 **WAVEFORMATEX** 結構和 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-121">In order for XAudio2 to play audio with a source voice, it needs a **WAVEFORMATEX** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="8b928-122">**WAVEFORMATEX** 結構可能是較大的結構，例如 **WAVEFORMATEXTENSIBLE** ，其中包含 **WAVEFORMATEX** 結構作為其第一個成員。</span><span class="sxs-lookup"><span data-stu-id="8b928-122">The **WAVEFORMATEX** structure may be a larger structure such as **WAVEFORMATEXTENSIBLE** that contains a **WAVEFORMATEX** structure as its first member.</span></span> <span data-ttu-id="8b928-123">如需詳細資訊，請參閱 **WAVEFORMATEX** 參考頁面。</span><span class="sxs-lookup"><span data-stu-id="8b928-123">See the **WAVEFORMATEX** reference page for more information.</span></span>

<span data-ttu-id="8b928-124">在此範例中， **WAVEFORMATEXTENSIBLE** 是用來允許載入兩個以上頻道的 PCM 音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="8b928-124">In this example a **WAVEFORMATEXTENSIBLE** is being used to allow loading of PCM audio files with more than two channels.</span></span>

<span data-ttu-id="8b928-125">下列步驟說明如何使用上面所述的函式來填入 **WAVEFORMATEXTENSIBLE** 結構和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-125">The following steps illustrate using the functions described above to populate a **WAVEFORMATEXTENSIBLE** structure and an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span> <span data-ttu-id="8b928-126">在此情況下，所載入的音訊檔會包含 PCM 資料，而且只會包含 ' RIFF '、' bcp.fmt ' 和 ' data ' 區塊。</span><span class="sxs-lookup"><span data-stu-id="8b928-126">In this case, the audio file being loaded contains PCM data, and will only contain a 'RIFF', 'fmt ', and 'data' chunk.</span></span> <span data-ttu-id="8b928-127">其他格式可能包含如 [資源交換檔案格式 ](resource-interchange-file-format--riff-.md)所述的其他區塊類型 (RIFF) 。</span><span class="sxs-lookup"><span data-stu-id="8b928-127">Other formats may contain additional chunk types as described in [Resource Interchange File Format (RIFF)](resource-interchange-file-format--riff-.md).</span></span>

1.  <span data-ttu-id="8b928-128">宣告 **WAVEFORMATEXTENSIBLE** 和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-128">Declare **WAVEFORMATEXTENSIBLE** and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structures.</span></span>
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  <span data-ttu-id="8b928-129">使用 CreateFile 開啟音訊檔案。</span><span class="sxs-lookup"><span data-stu-id="8b928-129">Open the audio file with CreateFile.</span></span>
    ```
    #ifdef _XBOX
    char * strFileName = "game:\\media\\MusicMono.wav";
    #else
    TCHAR * strFileName = _TEXT("media\\MusicMono.wav");
    #endif
    // Open the file
    HANDLE hFile = CreateFile(
        strFileName,
        GENERIC_READ,
        FILE_SHARE_READ,
        NULL,
        OPEN_EXISTING,
        0,
        NULL );

    if( INVALID_HANDLE_VALUE == hFile )
        return HRESULT_FROM_WIN32( GetLastError() );

    if( INVALID_SET_FILE_POINTER == SetFilePointer( hFile, 0, NULL, FILE_BEGIN ) )
        return HRESULT_FROM_WIN32( GetLastError() );
    ```

    

3.  <span data-ttu-id="8b928-130">找出音訊檔案中的 ' RIFF ' 區塊，然後檢查檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8b928-130">Locate the 'RIFF' chunk in the audio file, and check the file type.</span></span>
    ```
    DWORD dwChunkSize;
    DWORD dwChunkPosition;
    //check the file type, should be fourccWAVE or 'XWMA'
    FindChunk(hFile,fourccRIFF,dwChunkSize, dwChunkPosition );
    DWORD filetype;
    ReadChunkData(hFile,&filetype,sizeof(DWORD),dwChunkPosition);
    if (filetype != fourccWAVE)
        return S_FALSE;
    ```

    

4.  <span data-ttu-id="8b928-131">找出 ' bcp.fmt ' 區塊，並將其內容複寫到 **WAVEFORMATEXTENSIBLE** 結構中。</span><span class="sxs-lookup"><span data-stu-id="8b928-131">Locate the 'fmt ' chunk, and copy its contents into a **WAVEFORMATEXTENSIBLE** structure.</span></span>
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  <span data-ttu-id="8b928-132">找出 ' data ' 區塊，並將其內容讀入緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8b928-132">Locate the 'data' chunk, and read its contents into a buffer.</span></span>
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  <span data-ttu-id="8b928-133">填入 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。</span><span class="sxs-lookup"><span data-stu-id="8b928-133">Populate an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure.</span></span>
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a><span data-ttu-id="8b928-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="8b928-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b928-135">快速入門</span><span class="sxs-lookup"><span data-stu-id="8b928-135">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="8b928-136">使用方法：使用 XAudio2 播放音效</span><span class="sxs-lookup"><span data-stu-id="8b928-136">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="8b928-137">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="8b928-137">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
