---
description: 您可以向 XAudio2 引擎註冊執行 IXAudio2EngineCallback 介面之類別的實例，以通知 XAudio2 用戶端程式代碼引擎事件。
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 使用方法：使用引擎回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386267"
---
# <a name="how-to-use-engine-callbacks"></a>使用方法：使用引擎回呼

您可以向 XAudio2 引擎註冊執行 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面之類別的實例，以通知 XAudio2 用戶端程式代碼引擎事件。 如此一來，XAudio2 用戶端程式代碼就能追蹤音訊處理發生的時間，以及在發生嚴重錯誤時，重新開機引擎的時機。

## <a name="to-use-an-engine-callback"></a>使用引擎回呼

下列步驟會註冊物件來處理引擎事件。

1.  建立繼承自 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面的類別。

    [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)的所有方法都是純虛擬的，而且必須定義。 在此範例中，您需要的方法是 [**IXAudio2EngineCallback：： OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror)，它會設定旗標來表示重大錯誤發生時的主要遊戲迴圈。 其餘的方法 [**IXAudio2EngineCallback：： OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) 和 [**IXAudio2EngineCallback：： OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend)是此範例中的存根。

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 來建立 XAudio2 引擎的實例。

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  使用 [**IXAudio2：： RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) 來註冊引擎回呼。

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  如果您不需要引擎回呼，請呼叫 [**IXAudio2：： UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks)。

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
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

 

 
