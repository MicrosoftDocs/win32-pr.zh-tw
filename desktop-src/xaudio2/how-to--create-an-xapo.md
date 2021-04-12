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
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="8ce36-103">使用方法：建立 XAPO</span><span class="sxs-lookup"><span data-stu-id="8ce36-103">How to: Create an XAPO</span></span>

<span data-ttu-id="8ce36-104">XAPO API 會提供 [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) 介面和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 類別來建立新的 XAPO 類型。</span><span class="sxs-lookup"><span data-stu-id="8ce36-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="8ce36-105">**IXAPO** 介面包含所有需要實作為建立新 XAPO 的方法。</span><span class="sxs-lookup"><span data-stu-id="8ce36-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="8ce36-106">**CXAPOBase** 類別提供 **IXAPO** 介面的基本實作為。</span><span class="sxs-lookup"><span data-stu-id="8ce36-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="8ce36-107">**CXAPOBase** 會執行所有 **IXAPO** 介面方法，但是 [**IXAPO：:P ROCESS**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法是每個 XAPO 唯一的。</span><span class="sxs-lookup"><span data-stu-id="8ce36-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="8ce36-108">若要建立新的靜態 XAPO</span><span class="sxs-lookup"><span data-stu-id="8ce36-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="8ce36-109">從 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 基類衍生新的 XAPO 類別。</span><span class="sxs-lookup"><span data-stu-id="8ce36-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="8ce36-110">XAPOs 會執行 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="8ce36-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="8ce36-111">[**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo)和 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)介面包括三個 **IUnknown** 方法： **QueryInterface**、 **AddRef** 和 **Release**。</span><span class="sxs-lookup"><span data-stu-id="8ce36-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="8ce36-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) 提供這三種 **IUnknown** 方法的所有方法。</span><span class="sxs-lookup"><span data-stu-id="8ce36-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="8ce36-113">**CXAPOBase** 的新實例會有1的參考計數。</span><span class="sxs-lookup"><span data-stu-id="8ce36-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="8ce36-114">當其參考計數變成0時，就會將它終結。</span><span class="sxs-lookup"><span data-stu-id="8ce36-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="8ce36-115">若要允許 XAudio2 在不再需要時終結 XAPO 的實例，請在 XAPO 新增至 XAudio2 效果鏈之後，于上呼叫 **IUnknown：： Release** 。</span><span class="sxs-lookup"><span data-stu-id="8ce36-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="8ce36-116">如需有關搭配 XAudio2 使用 XAPO 的詳細資訊，請參閱 [如何：在 XAudio2 中使用 XAPO](how-to--use-an-xapo-in-xaudio2.md) 。</span><span class="sxs-lookup"><span data-stu-id="8ce36-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="8ce36-117">覆寫 [**IXAPO：： LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)方法的 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)類別實作為。</span><span class="sxs-lookup"><span data-stu-id="8ce36-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="8ce36-118">覆寫 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 可讓您儲存要儲存之音訊資料格式的相關資訊，以便在 IXAPO 中使用 [**：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)。</span><span class="sxs-lookup"><span data-stu-id="8ce36-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="8ce36-119">執行 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法。</span><span class="sxs-lookup"><span data-stu-id="8ce36-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="8ce36-120">每當 XAPO 需要處理音訊資料時，XAudio2 會呼叫 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法。</span><span class="sxs-lookup"><span data-stu-id="8ce36-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="8ce36-121">**進程** 包含 XAPO 的大量程式碼。</span><span class="sxs-lookup"><span data-stu-id="8ce36-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="8ce36-122">執行 Process 方法</span><span class="sxs-lookup"><span data-stu-id="8ce36-122">Implementing the Process Method</span></span>

<span data-ttu-id="8ce36-123">[**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)方法接受串流緩衝區來輸入和輸出音訊資料。</span><span class="sxs-lookup"><span data-stu-id="8ce36-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="8ce36-124">一般 XAPO 預期會有一個輸入資料流程緩衝區和一個輸出資料流程緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8ce36-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="8ce36-125">您應該根據 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 函式中指定的格式，以及使用輸入資料流程緩衝區傳遞給 **處理** 函式的任何旗標，以輸入資料流程緩衝區的資料做為處理基礎。</span><span class="sxs-lookup"><span data-stu-id="8ce36-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="8ce36-126">將處理過的輸入資料流程緩衝區資料複製到輸出資料流程緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8ce36-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="8ce36-127">將輸出資料流程緩衝區的 BufferFlags 參數設定為 [**XAPO \_ buffer \_ VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) 或 **XAPO \_ buffer \_ 無** 訊息。</span><span class="sxs-lookup"><span data-stu-id="8ce36-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="8ce36-128">下列範例示範只將資料從輸入緩衝區複製到輸出緩衝區的 [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) 和 [**流程**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 執行。</span><span class="sxs-lookup"><span data-stu-id="8ce36-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="8ce36-129">不過，如果輸入緩衝區以 [**\_ \_ 無**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags)訊息的方式標記 XAPO 緩衝區，則不會進行任何處理。</span><span class="sxs-lookup"><span data-stu-id="8ce36-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


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



<span data-ttu-id="8ce36-130">撰寫 [**處理**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法時，請務必注意 XAudio2 音訊資料是交錯的。</span><span class="sxs-lookup"><span data-stu-id="8ce36-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="8ce36-131">這表示，每個通道的資料會與特定範例編號相鄰。</span><span class="sxs-lookup"><span data-stu-id="8ce36-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="8ce36-132">例如，如果有4個通道 wave 進入 XAudio2 來源語音，音訊資料會是 channel 0、channel 1 範例、channel 2 的範例、channel 3 的範例，以及第一個通道0、1、2、3等的範例的範例。</span><span class="sxs-lookup"><span data-stu-id="8ce36-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ce36-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ce36-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ce36-134">音訊效果</span><span class="sxs-lookup"><span data-stu-id="8ce36-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="8ce36-135">XAPO 概觀</span><span class="sxs-lookup"><span data-stu-id="8ce36-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
