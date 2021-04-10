---
description: 當您建立來源語音時，可以將結構傳遞給它，以定義特定音訊事件的回呼。 您可以使用這些回呼來執行動作或指示其他程式碼。
ms.assetid: 0bace0c5-9171-efd8-9a38-2c2b3452f73f
title: 使用方法：使用來源聲音回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c10005ed838a22ea0dfce59312d6f293c213c39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690888"
---
# <a name="how-to-use-source-voice-callbacks"></a><span data-ttu-id="5d314-104">使用方法：使用來源聲音回呼</span><span class="sxs-lookup"><span data-stu-id="5d314-104">How to: Use Source Voice Callbacks</span></span>

<span data-ttu-id="5d314-105">當您建立來源語音時，可以將結構傳遞給它，以定義特定音訊事件的回呼。</span><span class="sxs-lookup"><span data-stu-id="5d314-105">When you create a source voice, you can pass a structure to it that defines callbacks for certain audio events.</span></span> <span data-ttu-id="5d314-106">您可以使用這些回呼來執行動作或指示其他程式碼。</span><span class="sxs-lookup"><span data-stu-id="5d314-106">You can use these callbacks to perform actions or to signal other code.</span></span>

1.  <span data-ttu-id="5d314-107">建立繼承自 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別。</span><span class="sxs-lookup"><span data-stu-id="5d314-107">Create a class that inherits from the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface.</span></span> <span data-ttu-id="5d314-108">**IXAudio2VoiceCallback** 的所有成員函式都是純虛擬的，而且必須定義。</span><span class="sxs-lookup"><span data-stu-id="5d314-108">All member functions of **IXAudio2VoiceCallback** are purely virtual, and must be defined.</span></span> <span data-ttu-id="5d314-109">此範例中的唯一相關函數是 [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend)。</span><span class="sxs-lookup"><span data-stu-id="5d314-109">The only function of interest in this example is [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend).</span></span> <span data-ttu-id="5d314-110">因此，其餘的函式都是存根。</span><span class="sxs-lookup"><span data-stu-id="5d314-110">Therefore, the rest of the functions are stubs.</span></span> <span data-ttu-id="5d314-111">**OnStreamEnd** 函式會觸發指出音效已完成播放的事件。</span><span class="sxs-lookup"><span data-stu-id="5d314-111">The **OnStreamEnd** function triggers an event that indicates the sound is done playing.</span></span>

    ```
    class VoiceCallback : public IXAudio2VoiceCallback
    {
    public:
        HANDLE hBufferEndEvent;
        VoiceCallback(): hBufferEndEvent( CreateEvent( NULL, FALSE, FALSE, NULL ) ){}
        ~VoiceCallback(){ CloseHandle( hBufferEndEvent ); }

        //Called when the voice has just finished playing a contiguous audio stream.
        void OnStreamEnd() { SetEvent( hBufferEndEvent ); }

        //Unused methods are stubs
        void OnVoiceProcessingPassEnd() { }
        void OnVoiceProcessingPassStart(UINT32 SamplesRequired) {    }
        void OnBufferEnd(void * pBufferContext)    { }
        void OnBufferStart(void * pBufferContext) {    }
        void OnLoopEnd(void * pBufferContext) {    }
        void OnVoiceError(void * pBufferContext, HRESULT Error) { }
    };
    ```

    

2.  <span data-ttu-id="5d314-112">使用先前建立為 pCallback 參數的回呼類別實例，以 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)建立 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)。</span><span class="sxs-lookup"><span data-stu-id="5d314-112">Create a [**source voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice) with [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) using an instance of the callback class created previously as the pCallback parameter.</span></span>

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  <span data-ttu-id="5d314-113">開始語音之後，請使用 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) 方法來等候觸發事件。</span><span class="sxs-lookup"><span data-stu-id="5d314-113">After starting the voice, use the [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) method to wait for the event to be triggered.</span></span>

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="5d314-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="5d314-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d314-115">回撥</span><span class="sxs-lookup"><span data-stu-id="5d314-115">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="5d314-116">XAudio2 回呼</span><span class="sxs-lookup"><span data-stu-id="5d314-116">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="5d314-117">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5d314-117">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5d314-118">使用方法：建立基本音訊處理圖形</span><span class="sxs-lookup"><span data-stu-id="5d314-118">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="5d314-119">使用方法：從磁碟串流處理音效</span><span class="sxs-lookup"><span data-stu-id="5d314-119">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
