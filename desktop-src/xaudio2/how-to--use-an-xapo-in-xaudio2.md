---
description: 本主題說明如何在 XAudio2 效果鏈中使用以 XAPO API 建立的效果。
ms.assetid: d4d24177-25eb-13ca-0e38-0c876a273e0d
title: 使用方法：在 XAudio2 中使用 XAPO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780e0ba59b5032ddc01b2709f1f3e9c5a0fcce1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981427"
---
# <a name="how-to-use-an-xapo-in-xaudio2"></a><span data-ttu-id="912e3-103">使用方法：在 XAudio2 中使用 XAPO</span><span class="sxs-lookup"><span data-stu-id="912e3-103">How to: Use an XAPO in XAudio2</span></span>

<span data-ttu-id="912e3-104">本主題說明如何在 XAudio2 效果鏈中使用以 XAPO API 建立的效果。</span><span class="sxs-lookup"><span data-stu-id="912e3-104">This topic shows you how to use an effect created with the XAPO API in an XAudio2 effect chain.</span></span>

1.  <span data-ttu-id="912e3-105">建立 XAPO，如 [如何：建立 XAPO](how-to--create-an-xapo.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="912e3-105">Create the XAPO as described in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

    <span data-ttu-id="912e3-106">您也可以依照 [如何：將執行時間參數支援加入至 XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md)中所述，來執行執行時間參數功能。</span><span class="sxs-lookup"><span data-stu-id="912e3-106">You can also implement run-time parameter functionality as described in [How to: Add Run-time Parameter Support to an XAPO](how-to--add-run-time-parameter-support-to-an-xapo.md).</span></span>

2.  <span data-ttu-id="912e3-107">建立 XAPO 的實例。</span><span class="sxs-lookup"><span data-stu-id="912e3-107">Create an instance of the XAPO.</span></span>

    ```
    IUnknown * pXAPO;
    pXAPO = new SimpleXAPO();
    ```

    

3.  <span data-ttu-id="912e3-108">以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。</span><span class="sxs-lookup"><span data-stu-id="912e3-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

4.  <span data-ttu-id="912e3-109">以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。</span><span class="sxs-lookup"><span data-stu-id="912e3-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

5.  <span data-ttu-id="912e3-110">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 功能將效果鏈套用至 XAudio2 聲音。</span><span class="sxs-lookup"><span data-stu-id="912e3-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="912e3-111">藉由將鏈作為參數傳遞給 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)、 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)或 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)，也可以在建立語音時，將效果鏈套用至語音。</span><span class="sxs-lookup"><span data-stu-id="912e3-111">An effect chain can also be applied to a voice when the voice is created by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

6.  <span data-ttu-id="912e3-112">使用 IUnknown：： Release 來釋放效果。</span><span class="sxs-lookup"><span data-stu-id="912e3-112">Release the effect with IUnknown::Release.</span></span>

    <span data-ttu-id="912e3-113">當您建立 XAPO 時，它的參考計數會是1。</span><span class="sxs-lookup"><span data-stu-id="912e3-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="912e3-114">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="912e3-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="912e3-115">釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="912e3-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="912e3-116">如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用它時，它就會被處置。</span><span class="sxs-lookup"><span data-stu-id="912e3-116">If XAudio2 has the only reference to the XAPO, it will be disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="912e3-117">例如，如果用戶端程式代碼需要維護 XAPO 的參考，以供稍後重複使用，則您應該略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="912e3-117">If the client code needs to maintain a reference to the XAPO for later reuse, for example, you should skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

7.  <span data-ttu-id="912e3-118">填入與效果相關聯的參數結構（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="912e3-118">Populate the parameter structure, if any, associated with the effect.</span></span> <span data-ttu-id="912e3-119">在此情況下，應套用效果的完整強度百分比。</span><span class="sxs-lookup"><span data-stu-id="912e3-119">In this case, the percentage of full strength at which the effect should be applied.</span></span>

    ```
    XAPO_PARAMETERS XAPOParameters;
    XAPOParameters.Level = 0.75;
    ```

    

8.  <span data-ttu-id="912e3-120">在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。</span><span class="sxs-lookup"><span data-stu-id="912e3-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( XAPO_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="912e3-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="912e3-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="912e3-122">音訊效果</span><span class="sxs-lookup"><span data-stu-id="912e3-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="912e3-123">XAPO 概觀</span><span class="sxs-lookup"><span data-stu-id="912e3-123">XAPO Overview</span></span>](xapo-overview.md)
</dt> <dt>

[<span data-ttu-id="912e3-124">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="912e3-124">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
