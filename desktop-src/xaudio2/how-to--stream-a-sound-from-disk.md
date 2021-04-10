---
description: 您可以在 XAudio2 中串流處理音訊資料，方法是建立個別的執行緒，並在串流執行緒中執行音訊資料的緩衝區讀取，然後使用回呼來控制該執行緒。
ms.assetid: 48b80a66-91c1-973f-069b-6f63422d7154
title: 使用方法：從磁碟串流處理音效
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c5598e8913514d6b0bf81b55bab5b481dbc43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693767"
---
# <a name="how-to-stream-a-sound-from-disk"></a>使用方法：從磁碟串流處理音效

> [!Note]  
> 此內容僅適用于桌面應用程式，且需要在 Windows Store 應用程式中使用修訂功能。 請參閱 **CreateFile2**、 [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa)、 [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)、 [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)和 **GetOverlappedResultEx** 的檔。 請參閱 [Windows SDK 範例庫](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208))中的 StreamEffect Windows 8 範例。

 

您可以在 XAudio2 中串流處理音訊資料，方法是建立個別的執行緒，並在串流執行緒中執行音訊資料的緩衝區讀取，然後使用回呼來控制該執行緒。

-   [在串流執行緒中執行緩衝區讀取](#performing-buffer-reads-in-the-streaming-thread)
-   [建立回呼類別](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a>在串流執行緒中執行緩衝區讀取

若要在串流執行緒中執行緩衝區讀取，請遵循下列步驟：

1.  建立讀取緩衝區的陣列。

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  初始化重迭的結構。

    結構是用來檢查非同步磁片讀取完成的時間。

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  在要播放串流音訊的 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)上呼叫 [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)函數。

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  當目前的讀取位置未超過音訊檔案的結尾時，迴圈。

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    在迴圈中，執行下列動作：

    1.  從磁片讀取資料區塊至目前的讀取緩衝區。

        ```
        DWORD dwRead;
        if( SUCCEEDED(hr) && 0 == ReadFile( hFile, pData, dwDataSize, &dwRead, pOverlapped ) )
            hr = HRESULT_FROM_WIN32( GetLastError() );
            DWORD cbValid = min( STREAMING_BUFFER_SIZE, cbWaveSize - CurrentPosition );
            DWORD dwRead;
            if( 0 == ReadFile( hFile, buffers[CurrentDiskReadBuffer], STREAMING_BUFFER_SIZE, &dwRead, &Overlapped ) )
                hr = HRESULT_FROM_WIN32( GetLastError() );
            Overlapped.Offset += cbValid;

            //update the file position to where it will be once the read finishes
            CurrentPosition += cbValid;
        ```

        

    2.  使用 **GetOverlappedResult** 函式來等候表示讀取已完成的事件。

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  等候 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) 上佇列的緩衝區數目小於讀取緩衝區的數目。

        [**來源聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)的狀態會使用 [**>getstate**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate)函式來檢查。

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  使用 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)函式，將目前的讀取緩衝區提交至 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)。

        ```
        XAUDIO2_BUFFER buf = {0};
        buf.AudioBytes = cbValid;
        buf.pAudioData = buffers[CurrentDiskReadBuffer];
        if( CurrentPosition >= cbWaveSize )
        {
            buf.Flags = XAUDIO2_END_OF_STREAM;
        }
        pSourceVoice->SubmitSourceBuffer( &buf );
        ```

        

    5.  將目前的讀取緩衝區索引設定為下一個緩衝區。

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  在迴圈完成後，等候剩餘的已排入佇列的緩衝區完成播放。

    當剩餘的緩衝區完成播放時，音效會停止，而且執行緒可以結束或重複使用，以串流另一個音效。

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a>建立回呼類別

若要建立回呼類別，請建立繼承自 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別。

類別應該在其 [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) 方法中設定事件。 這可讓串流執行緒進入睡眠狀態，直到事件通知 XAudio2 已完成從音訊緩衝區讀取為止。 如需搭配使用回呼與 XAudio2 的詳細資訊，請參閱 [如何：使用來源語音回呼](how-to--use-source-voice-callbacks.md)。


```
struct StreamingVoiceContext : public IXAudio2VoiceCallback
{
    HANDLE hBufferEndEvent;
    StreamingVoiceContext(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
    ~StreamingVoiceContext(){ CloseHandle( hBufferEndEvent ); }
    void OnBufferEnd( void* ){ SetEvent( hBufferEndEvent ); }
    ...
};
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[串流音訊資料](streaming-audio-data.md)
</dt> <dt>

[XAudio2 回呼](callbacks.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[使用方法：使用來源聲音回呼](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
