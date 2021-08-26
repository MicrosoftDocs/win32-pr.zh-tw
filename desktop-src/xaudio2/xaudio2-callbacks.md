---
description: XAudio2 可呼叫用戶端所提供的函式，以非同步方式在音訊處理執行緒中發生特定事件時通知它。
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: XAudio2 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3377bd029cc2e21971748eaca7309dd44390a5bd3420d772c45264dfdbd075c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054288"
---
# <a name="xaudio2-callbacks"></a>XAudio2 回呼

XAudio2 可呼叫用戶端所提供的函式，以非同步方式在音訊處理執行緒中發生特定事件時通知它。 這些回呼可以是全域或特定的指定來源語音。 若要接收全域引擎回呼，用戶端必須提供在初始化 XAudio2 時執行 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面的類別實例。 若要接收來源語音回呼，用戶端必須提供在建立來源語音時實 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別實例。 如需詳細資訊，請參閱 **IXAudio2EngineCallback** 和 **IXAudio2VoiceCallback**。

您必須小心執行回呼，以避免在音訊中導致中斷。 每當回呼執行時，XAudio2 就無法產生任何音訊。 延遲超過幾毫秒可能會導致音訊問題。 這種本質的延遲也會產生偵錯工具輸出。 這表示可能發生效能問題。 回呼函式至少不得執行下列作業：

-   存取硬碟或其他永久儲存體
-   進行昂貴或封鎖的 API 呼叫
-   與用戶端程式代碼的其他部分同步處理
-   需要大量的 CPU 使用率

如果用戶端設計需要回呼來觸發動作（如先前所列的動作），回呼應該會通知不同的用戶端執行緒來執行工作。 您可以使用簡單的 **SetEvent** 機制或更複雜的機制（例如另一個執行緒所耗用的非封鎖命令佇列）來達成此目的。

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

[**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)類別包含在 XAudio2 引擎中發生特定事件時通知用戶端的方法。 這些方法應該由 XAudio2 用戶端所執行。 XAudio2 會使用 [**IXAudio2：： RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) 方法，透過用戶端所提供的介面指標來呼叫這些方法。 所有這些方法都會傳回 **void**，而不是 **HRESULT**。

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

[**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)類別包含的方法，會在特定的 XAudio2 來源語音中發生特定事件時通知用戶端。 XAudio2 會透過 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)中用戶端所提供的介面指標來呼叫這些方法。 如同 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)，這些方法應該由 XAudio2 用戶端執行，並傳回 **Void** 而非 **HRESULT**。

如先前所述，用戶端提供的這些回呼的實，在毫秒內最好儘快恢復。 回呼是在音訊處理執行緒中執行，所有處理都會中斷，直到回呼傳回為止。 回呼中的延遲可能很容易造成音訊問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[回撥](callbacks.md)
</dt> <dt>

[XAudio2 程式設計指南](programming-guide.md)
</dt> <dt>

[使用方法：使用來源聲音回呼](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[使用方法：使用引擎回呼](how-to--use-engine-callbacks.md)
</dt> <dt>

[使用方法：從磁碟串流處理音效](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
