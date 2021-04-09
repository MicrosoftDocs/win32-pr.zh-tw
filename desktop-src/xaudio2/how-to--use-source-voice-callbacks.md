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
# <a name="how-to-use-source-voice-callbacks"></a>使用方法：使用來源聲音回呼

當您建立來源語音時，可以將結構傳遞給它，以定義特定音訊事件的回呼。 您可以使用這些回呼來執行動作或指示其他程式碼。

1.  建立繼承自 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別。 **IXAudio2VoiceCallback** 的所有成員函式都是純虛擬的，而且必須定義。 此範例中的唯一相關函數是 [**OnStreamEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voicecallback-onstreamend)。 因此，其餘的函式都是存根。 **OnStreamEnd** 函式會觸發指出音效已完成播放的事件。

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

    

2.  使用先前建立為 pCallback 參數的回呼類別實例，以 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)建立 [**來源語音**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)。

    ```
    VoiceCallback voiceCallback;
    if( FAILED(hr = pXaudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx,
                                 0, XAUDIO2_DEFAULT_FREQ_RATIO, &voiceCallback, NULL, NULL ) ) ) return;
    ```

    

3.  開始語音之後，請使用 [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) 方法來等候觸發事件。

    ```
    WaitForSingleObjectEx( voiceCallback.hBufferEndEvent, INFINITE, TRUE );
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回撥](callbacks.md)
</dt> <dt>

[XAudio2 回呼](xaudio2-callbacks.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：建立基本音訊處理圖形](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[使用方法：從磁碟串流處理音效](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
