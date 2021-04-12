---
description: XAPO API 會提供 IXAPO 介面和 CXAPOBase 類別來建立新的 XAPO 類型。
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 使用方法：建立 XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195304"
---
# <a name="how-to-create-an-xapo"></a>使用方法：建立 XAPO

XAPO API 會提供 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 類別來建立新的 XAPO 類型。 **IXAPO** 介面包含所有需要實作為建立新 XAPO 的方法。 **CXAPOBase** 類別提供 **IXAPO** 介面的基本實作為。 **CXAPOBase** 會執行所有 **IXAPO** 介面方法，但是 [**IXAPO：:P ROCESS**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法是每個 XAPO 唯一的。

## <a name="to-create-a-new-static-xapo"></a>若要建立新的靜態 XAPO

1.  從 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 基類衍生新的 XAPO 類別。

    > [!Note]  
    > XAPOs 會執行 **IUnknown** 介面。 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)和 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)介面包括三個 **IUnknown** 方法： **QueryInterface**、 **AddRef** 和 **Release**。 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 提供這三種 **IUnknown** 方法的所有方法。 **CXAPOBase** 的新實例會有1的參考計數。 當其參考計數變成0時，就會將它終結。 若要允許 XAudio2 在不再需要時終結 XAPO 的實例，請在 XAPO 新增至 XAudio2 效果鏈之後，于上呼叫 **IUnknown：： Release** 。 如需有關搭配 XAudio2 使用 XAPO 的詳細資訊，請參閱 [如何：在 XAudio2 中使用 XAPO](how-to--use-an-xapo-in-xaudio2.md) 。

     

2.  覆寫 [**IXAPO：： LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)方法的 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)類別實作為。

    覆寫 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 可讓您儲存要儲存之音訊資料格式的相關資訊，以便在 IXAPO 中使用 [**：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)。

3.  執行 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法。

    每當 XAPO 需要處理音訊資料時，XAudio2 會呼叫 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法。 **進程** 包含 XAPO 的大量程式碼。

## <a name="implementing-the-process-method"></a>執行 Process 方法

[**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)方法接受串流緩衝區來輸入和輸出音訊資料。 一般 XAPO 預期會有一個輸入資料流程緩衝區和一個輸出資料流程緩衝區。 您應該根據 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 函式中指定的格式，以及使用輸入資料流程緩衝區傳遞給 **處理** 函式的任何旗標，以輸入資料流程緩衝區的資料做為處理基礎。 將處理過的輸入資料流程緩衝區資料複製到輸出資料流程緩衝區。 將輸出資料流程緩衝區的 BufferFlags 參數設定為 [**XAPO \_ buffer \_ VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) 或 **XAPO \_ buffer \_ 無** 訊息。

下列範例示範只將資料從輸入緩衝區複製到輸出緩衝區的 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 和 [**流程**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 執行。 不過，如果輸入緩衝區以 [**\_ \_ 無**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags)訊息的方式標記 XAPO 緩衝區，則不會進行任何處理。


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



撰寫 [**處理**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法時，請務必注意 XAudio2 音訊資料是交錯的。 這表示，每個通道的資料會與特定範例編號相鄰。 例如，如果有4個通道 wave 進入 XAudio2 來源語音，音訊資料會是 channel 0、channel 1 範例、channel 2 的範例、channel 3 的範例，以及第一個通道0、1、2、3等的範例的範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊效果](audio-effects.md)
</dt> <dt>

[XAPO 概觀](xapo-overview.md)
</dt> </dl>

 

 
