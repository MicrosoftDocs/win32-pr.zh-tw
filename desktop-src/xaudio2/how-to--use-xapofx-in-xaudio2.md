---
description: 本主題說明如何使用 XAudio2 效果鏈中 XAPOFX 所包含的其中一個效果。
ms.assetid: dc325584-13f7-231a-e0c7-17f38d54ae11
title: 使用方法：在 XAudio2 中使用 XAPOFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b0bb4cbeabb38f408d9102a2534634e8eed7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977020"
---
# <a name="how-to-use-xapofx-in-xaudio2"></a><span data-ttu-id="209b4-103">使用方法：在 XAudio2 中使用 XAPOFX</span><span class="sxs-lookup"><span data-stu-id="209b4-103">How to: Use XAPOFX in XAudio2</span></span>

<span data-ttu-id="209b4-104">本主題說明如何使用 XAudio2 效果鏈中 XAPOFX 所包含的其中一個效果。</span><span class="sxs-lookup"><span data-stu-id="209b4-104">This topic shows you how to use one of the effects included in XAPOFX in an XAudio2 effect chain.</span></span>

## <a name="to-use-an-effect-from-xapofx-in-an-xaudio2-effect-chain"></a><span data-ttu-id="209b4-105">在 XAudio2 效果鏈中使用 XAPOFX 的效果</span><span class="sxs-lookup"><span data-stu-id="209b4-105">To use an effect from XAPOFX in an XAudio2 effect chain</span></span>

1.  <span data-ttu-id="209b4-106">將 XAPOFX 效果的 CLSID 傳遞給 [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 函數，以建立效果。</span><span class="sxs-lookup"><span data-stu-id="209b4-106">Create the effect by passing the CLSID of an XAPOFX effect to the [**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) function.</span></span>

    <span data-ttu-id="209b4-107">在此情況下，會建立簡化的「FXReverb」效果。</span><span class="sxs-lookup"><span data-stu-id="209b4-107">In this case, the simplified reverb effect FXReverb is being created.</span></span>

    ```
    IUnknown * pXAPO;
    CreateFX(__uuidof(FXReverb),&pXAPO);
    ```

    

2.  <span data-ttu-id="209b4-108">以資料填入 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構。</span><span class="sxs-lookup"><span data-stu-id="209b4-108">Populate an [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_DESCRIPTOR descriptor;
    descriptor.InitialState = true;
    descriptor.OutputChannels = 1;
    descriptor.pEffect = pXAPO;
    ```

    

3.  <span data-ttu-id="209b4-109">以資料填入 [**XAUDIO2 \_ 效果 \_ 鏈**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) 結構。</span><span class="sxs-lookup"><span data-stu-id="209b4-109">Populate an [**XAUDIO2\_EFFECT\_CHAIN**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain) structure with data.</span></span>

    ```
    XAUDIO2_EFFECT_CHAIN chain;
    chain.EffectCount = 1;
    chain.pEffectDescriptors = &descriptor;
    ```

    

4.  <span data-ttu-id="209b4-110">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) 功能將效果鏈套用至 XAudio2 聲音。</span><span class="sxs-lookup"><span data-stu-id="209b4-110">Apply the effect chain to an XAudio2 voice with the [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain) function.</span></span>

    ```
    pVoice->SetEffectChain(&chain);
    ```

    

    > [!Note]  
    > <span data-ttu-id="209b4-111">當您以參數的形式傳遞 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)、 [**IXAudio2：： CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice)或 [**IXAudio2：： CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice)時，您也可以在建立語音時將效果鏈套用至語音。</span><span class="sxs-lookup"><span data-stu-id="209b4-111">You can also apply an effect chain to a voice when you create the voice by passing the chain as a parameter to [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice), [**IXAudio2::CreateSubmixVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsubmixvoice), or [**IXAudio2::CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice).</span></span>

     

5.  <span data-ttu-id="209b4-112">使用 IUnknown：： Release 來釋放效果。</span><span class="sxs-lookup"><span data-stu-id="209b4-112">Release the effect with IUnknown::Release.</span></span> <span data-ttu-id="209b4-113">當您建立 XAPO 時，它的參考計數會是1。</span><span class="sxs-lookup"><span data-stu-id="209b4-113">When you create an XAPO, it will have a reference count of 1.</span></span> <span data-ttu-id="209b4-114">使用 [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)將 XAPO 傳遞至 XAudio2 時，XAudio2 會遞增 XAPO 上的參考計數。</span><span class="sxs-lookup"><span data-stu-id="209b4-114">When the XAPO is passed to XAudio2 with [**SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), XAudio2 increments the reference count on the XAPO.</span></span> <span data-ttu-id="209b4-115">釋放用戶端對 XAPO 的參考，可讓 XAudio2 取得 XAPO 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="209b4-115">Releasing the client's reference to the XAPO allows XAudio2 to take ownership of the XAPO.</span></span> <span data-ttu-id="209b4-116">如果 XAudio2 只有 XAPO 的參考，當 XAudio2 不再使用此參考時，就會處置此參考。</span><span class="sxs-lookup"><span data-stu-id="209b4-116">If XAudio2 has the only reference to the XAPO, this reference is disposed of when it is no longer being used by XAudio2.</span></span> <span data-ttu-id="209b4-117">如果用戶端程式代碼需要維護 XAPO 的參考（例如，稍後重複使用），您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="209b4-117">If the client code needs to maintain a reference to the XAPO—for example, for reuse later—you can skip this step.</span></span>

    ```
    pXAPO->Release();
    ```

    

6.  <span data-ttu-id="209b4-118">填入與效果相關聯的參數結構（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="209b4-118">Populate the parameter structure, if any, associated with the effect.</span></span>

    <span data-ttu-id="209b4-119">在此情況下， [**FXREVERB \_ 參數**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) 結構是用來設定應該使用的擴散和空間大小。</span><span class="sxs-lookup"><span data-stu-id="209b4-119">In this case, the [**FXREVERB\_PARAMETERS**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters) structure is used to set the diffusion and room size that the reverb effect should use.</span></span>

    ```
    FXREVERB_PARAMETERS XAPOParameters;
    XAPOParameters.Diffusion = FXREVERB_DEFAULT_DIFFUSION;
    XAPOParameters.RoomSize = FXREVERB_DEFAULT_ROOMSIZE;
    ```

    

7.  <span data-ttu-id="209b4-120">在附加效果的聲音上呼叫 [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) 函式，以將效果參數結構傳遞給效果。</span><span class="sxs-lookup"><span data-stu-id="209b4-120">Pass the effect parameter structure to the effect by calling the [**SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters) function on the voice to which the effect is attached.</span></span>

    ```
    hr = pVoice->SetEffectParameters( 0, &XAPOParameters, sizeof( FXREVERB_PARAMETERS ) );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="209b4-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="209b4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="209b4-122">音訊效果</span><span class="sxs-lookup"><span data-stu-id="209b4-122">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="209b4-123">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="209b4-123">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
