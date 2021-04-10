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
# <a name="how-to-stream-a-sound-from-disk"></a><span data-ttu-id="8876d-103">使用方法：從磁碟串流處理音效</span><span class="sxs-lookup"><span data-stu-id="8876d-103">How to: Stream a Sound from Disk</span></span>

> [!Note]  
> <span data-ttu-id="8876d-104">此內容僅適用于桌面應用程式，且需要在 Windows Store 應用程式中使用修訂功能。</span><span class="sxs-lookup"><span data-stu-id="8876d-104">This content applies only to desktop apps and will require revision to function in a Windows Store app.</span></span> <span data-ttu-id="8876d-105">請參閱 **CreateFile2**、 [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa)、 [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex)、 [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex)和 **GetOverlappedResultEx** 的檔。</span><span class="sxs-lookup"><span data-stu-id="8876d-105">Please refer to the documentation for **CreateFile2**, [CreateEventEx](/windows/win32/api/synchapi/nf-synchapi-createeventexa), [WaitForSingleObjectEx](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex), [SetFilePointerEx](/windows/win32/api/fileapi/nf-fileapi-setfilepointerex), and **GetOverlappedResultEx**.</span></span> <span data-ttu-id="8876d-106">請參閱 [Windows SDK 範例庫](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208))中的 StreamEffect Windows 8 範例。</span><span class="sxs-lookup"><span data-stu-id="8876d-106">See the StreamEffect Windows 8 sample from the [Windows SDK Samples Gallery](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/XAudio2%20audio%20stream%20effect%20sample%20(Windows%208)).</span></span>

 

<span data-ttu-id="8876d-107">您可以在 XAudio2 中串流處理音訊資料，方法是建立個別的執行緒，並在串流執行緒中執行音訊資料的緩衝區讀取，然後使用回呼來控制該執行緒。</span><span class="sxs-lookup"><span data-stu-id="8876d-107">You can stream audio data in XAudio2 by creating a separate thread and perform buffer reads of the audio data in the streaming thread, and then use callbacks to control that thread.</span></span>

-   [<span data-ttu-id="8876d-108">在串流執行緒中執行緩衝區讀取</span><span class="sxs-lookup"><span data-stu-id="8876d-108">Performing buffer reads in the streaming thread</span></span>](#performing-buffer-reads-in-the-streaming-thread)
-   [<span data-ttu-id="8876d-109">建立回呼類別</span><span class="sxs-lookup"><span data-stu-id="8876d-109">Creating the callback class</span></span>](#creating-the-callback-class)

## <a name="performing-buffer-reads-in-the-streaming-thread"></a><span data-ttu-id="8876d-110">在串流執行緒中執行緩衝區讀取</span><span class="sxs-lookup"><span data-stu-id="8876d-110">Performing buffer reads in the streaming thread</span></span>

<span data-ttu-id="8876d-111">若要在串流執行緒中執行緩衝區讀取，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8876d-111">To perform buffer reads in the streaming thread follow these steps:</span></span>

1.  <span data-ttu-id="8876d-112">建立讀取緩衝區的陣列。</span><span class="sxs-lookup"><span data-stu-id="8876d-112">Create an array of read buffers.</span></span>

    ```
    #define STREAMING_BUFFER_SIZE 65536
    #define MAX_BUFFER_COUNT 3
    BYTE buffers[MAX_BUFFER_COUNT][STREAMING_BUFFER_SIZE];
    ```

    

2.  <span data-ttu-id="8876d-113">初始化重迭的結構。</span><span class="sxs-lookup"><span data-stu-id="8876d-113">Initialize an OVERLAPPED structure.</span></span>

    <span data-ttu-id="8876d-114">結構是用來檢查非同步磁片讀取完成的時間。</span><span class="sxs-lookup"><span data-stu-id="8876d-114">The structure is used to check when an asynchronous disk read has finished.</span></span>

    ```
    OVERLAPPED Overlapped = {0};
    Overlapped.hEvent = CreateEvent( NULL, TRUE, FALSE, NULL );
    ```

    

3.  <span data-ttu-id="8876d-115">在要播放串流音訊的 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)上呼叫 [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)函數。</span><span class="sxs-lookup"><span data-stu-id="8876d-115">Call the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) that will be playing the streaming audio.</span></span>

    ```
    hr = pSourceVoice->Start( 0, 0 );
    ```

    

4.  <span data-ttu-id="8876d-116">當目前的讀取位置未超過音訊檔案的結尾時，迴圈。</span><span class="sxs-lookup"><span data-stu-id="8876d-116">Loop while the current read position is not passed the end of the audio file.</span></span>

    ```
    CurrentDiskReadBuffer = 0;
    CurrentPosition = 0;
    while ( CurrentPosition < cbWaveSize )
    {
        ...
    }
    ```

    

    <span data-ttu-id="8876d-117">在迴圈中，執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="8876d-117">In the loop, do the following:</span></span>

    1.  <span data-ttu-id="8876d-118">從磁片讀取資料區塊至目前的讀取緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8876d-118">Read a chunk of data from the disk into the current read buffer.</span></span>

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

        

    2.  <span data-ttu-id="8876d-119">使用 **GetOverlappedResult** 函式來等候表示讀取已完成的事件。</span><span class="sxs-lookup"><span data-stu-id="8876d-119">Use the **GetOverlappedResult** function to wait for the event that signals the read has finished.</span></span>

        ```
        DWORD NumberBytesTransferred;
        ::GetOverlappedResult(hFile,&Overlapped,&NumberBytesTransferred, TRUE);
        ```

        

    3.  <span data-ttu-id="8876d-120">等候 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) 上佇列的緩衝區數目小於讀取緩衝區的數目。</span><span class="sxs-lookup"><span data-stu-id="8876d-120">Wait for the number of buffers queued on the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) to be less than the number of read buffers.</span></span>

        <span data-ttu-id="8876d-121">[**來源聲音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)的狀態會使用 [**>getstate**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate)函式來檢查。</span><span class="sxs-lookup"><span data-stu-id="8876d-121">The state of the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) is checked with the [**GetState**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-getstate) function.</span></span>

        ```
        XAUDIO2_VOICE_STATE state;
        while( pSourceVoice->GetState( &state ), state.BuffersQueued >= MAX_BUFFER_COUNT - 1)
        {
            WaitForSingleObject( Context.hBufferEndEvent, INFINITE );
        }
        ```

        

    4.  <span data-ttu-id="8876d-122">使用 [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer)函式，將目前的讀取緩衝區提交至 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)。</span><span class="sxs-lookup"><span data-stu-id="8876d-122">Submit the current read buffer to the [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) using the [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer) function.</span></span>

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

        

    5.  <span data-ttu-id="8876d-123">將目前的讀取緩衝區索引設定為下一個緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8876d-123">Set the current read buffer index to the next buffer.</span></span>

        ```
        CurrentDiskReadBuffer++;
        CurrentDiskReadBuffer %= MAX_BUFFER_COUNT;
        ```

        

5.  <span data-ttu-id="8876d-124">在迴圈完成後，等候剩餘的已排入佇列的緩衝區完成播放。</span><span class="sxs-lookup"><span data-stu-id="8876d-124">After the loop has finished, wait for the remaining queued buffers to finish playing.</span></span>

    <span data-ttu-id="8876d-125">當剩餘的緩衝區完成播放時，音效會停止，而且執行緒可以結束或重複使用，以串流另一個音效。</span><span class="sxs-lookup"><span data-stu-id="8876d-125">When the remaining buffers have finished playing, the sound stops, and the thread can exit or be reused to stream another sound.</span></span>

    ```
    XAUDIO2_VOICE_STATE state;
    while( pSourceVoice->GetState( &state ), state.BuffersQueued > 0 )
    {
        WaitForSingleObjectEx( Context.hBufferEndEvent, INFINITE, TRUE );
    }
    ```

    

## <a name="creating-the-callback-class"></a><span data-ttu-id="8876d-126">建立回呼類別</span><span class="sxs-lookup"><span data-stu-id="8876d-126">Creating the callback class</span></span>

<span data-ttu-id="8876d-127">若要建立回呼類別，請建立繼承自 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="8876d-127">To create the callback class, create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span>

<span data-ttu-id="8876d-128">類別應該在其 [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) 方法中設定事件。</span><span class="sxs-lookup"><span data-stu-id="8876d-128">The class should set an event in its [**OnBufferEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onbufferend) method.</span></span> <span data-ttu-id="8876d-129">這可讓串流執行緒進入睡眠狀態，直到事件通知 XAudio2 已完成從音訊緩衝區讀取為止。</span><span class="sxs-lookup"><span data-stu-id="8876d-129">This allows the streaming thread to put itself to sleep until the event signals it that XAudio2 has finished reading from an audio buffer.</span></span> <span data-ttu-id="8876d-130">如需搭配使用回呼與 XAudio2 的詳細資訊，請參閱 [如何：使用來源語音回呼](how-to--use-source-voice-callbacks.md)。</span><span class="sxs-lookup"><span data-stu-id="8876d-130">For more information about using callbacks with XAudio2, see [How to: Use Source Voice Callbacks](how-to--use-source-voice-callbacks.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8876d-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="8876d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8876d-132">串流音訊資料</span><span class="sxs-lookup"><span data-stu-id="8876d-132">Streaming Audio Data</span></span>](streaming-audio-data.md)
</dt> <dt>

[<span data-ttu-id="8876d-133">XAudio2 回呼</span><span class="sxs-lookup"><span data-stu-id="8876d-133">XAudio2 Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="8876d-134">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="8876d-134">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="8876d-135">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="8876d-135">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="8876d-136">使用方法：使用來源聲音回呼</span><span class="sxs-lookup"><span data-stu-id="8876d-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> </dl>

 

 
