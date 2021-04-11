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
# <a name="how-to-load-audio-data-files-in-xaudio2"></a>使用方法：在 XAudio2 中載入音訊資料檔

> [!Note]  
> 此內容僅適用于桌面應用程式，且需要在 Windows Store 應用程式中使用修訂功能。 請參閱 [**CreateFile2**](/windows/win32/api/fileapi/nf-fileapi-createfile2)、 [**CreateEventEx**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)、 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)、 [**SetFilePointerEx**](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)和 [**GetOverlappedResultEx**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresultex)的檔。 請參閱 [Windows SDK 範例庫](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20file%20playback%20sample%20(Windows%208))中的 BasicSound Windows 8 範例中的 SoundFileReader .h/.cpp。

 

本主題說明在 XAudio2 中填入播放音訊資料所需結構的步驟。 下列步驟會載入音訊檔案的 ' bcp.fmt ' 和 ' data ' 區塊，並使用它們來填入 **WAVEFORMATEXTENSIBLE** 結構和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。

-   [正在準備剖析音訊檔案。](#preparing-to-parse-the-audio-file)
-   [以 RIFF 區塊的內容填入 XAudio2 結構。](#populating-xaudio2-structures-with-the-contents-of-riff-chunks)

## <a name="preparing-to-parse-the-audio-file"></a>準備剖析音訊檔案

XAudio2 支援的音訊檔案會使用資源交換檔案格式 (RIFF) 。 [ (RIFF) 總覽的資源交換檔案格式](resource-interchange-file-format--riff-.md)中會說明 RIFF。 RIFF 檔案中的音訊資料是藉由尋找 RIFF 區塊來載入，然後在區塊之間進行迴圈，以尋找包含在 RIFF 區塊中的個別區塊。 下列函式是用來尋找區塊的程式碼範例，以及包含在區塊中的載入資料。

-   若要在 RIFF 檔中尋找區塊：

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

    

-   在區塊中讀取資料之後的資料。

    一旦找到所需的區塊，就可以藉由將檔案指標調整至區塊資料區段的開頭，來讀取其資料。 在找到區塊之後，從區塊讀取資料的函式可能會如下所示。

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

    

## <a name="populating-xaudio2-structures-with-the-contents-of-riff-chunks"></a>以 RIFF 區塊的內容填入 XAudio2 結構

為了讓 XAudio2 能夠以來源聲音播放音訊，它需要 **WAVEFORMATEX** 結構和 [**XAudio2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。 **WAVEFORMATEX** 結構可能是較大的結構，例如 **WAVEFORMATEXTENSIBLE** ，其中包含 **WAVEFORMATEX** 結構作為其第一個成員。 如需詳細資訊，請參閱 **WAVEFORMATEX** 參考頁面。

在此範例中， **WAVEFORMATEXTENSIBLE** 是用來允許載入兩個以上頻道的 PCM 音訊檔案。

下列步驟說明如何使用上面所述的函式來填入 **WAVEFORMATEXTENSIBLE** 結構和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。 在此情況下，所載入的音訊檔會包含 PCM 資料，而且只會包含 ' RIFF '、' bcp.fmt ' 和 ' data ' 區塊。 其他格式可能包含如 [資源交換檔案格式 ](resource-interchange-file-format--riff-.md)所述的其他區塊類型 (RIFF) 。

1.  宣告 **WAVEFORMATEXTENSIBLE** 和 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。
    ```
    WAVEFORMATEXTENSIBLE wfx = {0};
    XAUDIO2_BUFFER buffer = {0};
    ```

    

2.  使用 CreateFile 開啟音訊檔案。
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

    

3.  找出音訊檔案中的 ' RIFF ' 區塊，然後檢查檔案類型。
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

    

4.  找出 ' bcp.fmt ' 區塊，並將其內容複寫到 **WAVEFORMATEXTENSIBLE** 結構中。
    ```
    FindChunk(hFile,fourccFMT, dwChunkSize, dwChunkPosition );
    ReadChunkData(hFile, &wfx, dwChunkSize, dwChunkPosition );
    ```

    

5.  找出 ' data ' 區塊，並將其內容讀入緩衝區。
    ```
    //fill out the audio data buffer with the contents of the fourccDATA chunk
    FindChunk(hFile,fourccDATA,dwChunkSize, dwChunkPosition );
    BYTE * pDataBuffer = new BYTE[dwChunkSize];
    ReadChunkData(hFile, pDataBuffer, dwChunkSize, dwChunkPosition);
    ```

    

6.  填入 [**XAUDIO2 \_ 緩衝區**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) 結構。
    ```
    buffer.AudioBytes = dwChunkSize;  //size of the audio buffer in bytes
    buffer.pAudioData = pDataBuffer;  //buffer containing audio data
    buffer.Flags = XAUDIO2_END_OF_STREAM; // tell the source voice not to expect any data after this buffer
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[快速入門](getting-started.md)
</dt> <dt>

[使用方法：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md)
</dt> <dt>

[XAudio2 程式設計參考](programming-reference.md)
</dt> </dl>

 

 
