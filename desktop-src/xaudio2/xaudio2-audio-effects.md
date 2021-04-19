---
description: 音訊效果是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。 您可以使用效果來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。
ms.assetid: 8c3fa4ca-dcff-bd23-7220-7d0aeb6c6068
title: XAudio2 音訊效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8de87a65ea4321b5e8d73a837f79a3e56e8e3a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974070"
---
# <a name="xaudio2-audio-effects"></a><span data-ttu-id="5ab29-104">XAudio2 音訊效果</span><span class="sxs-lookup"><span data-stu-id="5ab29-104">XAudio2 Audio Effects</span></span>

<span data-ttu-id="5ab29-105">音訊效果是接受傳入音訊資料的物件，並在資料傳遞之前對資料執行某些作業。</span><span class="sxs-lookup"><span data-stu-id="5ab29-105">An audio effect is an object that takes incoming audio data, and performs some operation on the data before passing it on.</span></span> <span data-ttu-id="5ab29-106">您可以使用效果來執行各種不同的工作，包括將回音新增至音訊串流以及監視尖峰音量層級。</span><span class="sxs-lookup"><span data-stu-id="5ab29-106">You can use an effect to perform a variety of tasks, including adding reverb to an audio stream and monitoring peak volume levels.</span></span>

## <a name="effect-chains"></a><span data-ttu-id="5ab29-107">效果鏈</span><span class="sxs-lookup"><span data-stu-id="5ab29-107">Effect Chains</span></span>

<span data-ttu-id="5ab29-108">任何 XAudio2 聲音都可以裝載一連串的音訊效果。</span><span class="sxs-lookup"><span data-stu-id="5ab29-108">Any XAudio2 voice can host a chain of audio effects.</span></span> <span data-ttu-id="5ab29-109">您可以使用 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) 項結構的陣列來指定效果鏈。</span><span class="sxs-lookup"><span data-stu-id="5ab29-109">You can use an array of [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor) structures to specify effect chains.</span></span> <span data-ttu-id="5ab29-110">每個描述項都包含用戶端所提供之效果物件的指標。</span><span class="sxs-lookup"><span data-stu-id="5ab29-110">Each descriptor contains a pointer to an effect object provided by the client.</span></span> <span data-ttu-id="5ab29-111">這些物件必須 (APO) 介面來執行音訊處理物件。</span><span class="sxs-lookup"><span data-stu-id="5ab29-111">These objects must implement the Audio Processing Object (APO) interfaces.</span></span> <span data-ttu-id="5ab29-112">如需 APO 模型的詳細資訊，請參閱 [XAPO 總覽](xapo-overview.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ab29-112">See the [XAPO Overview](xapo-overview.md) for more information about the APO model.</span></span>

<span data-ttu-id="5ab29-113">當 XAudio2 引擎執行時，用戶端可以動態地修改效果鏈 () 、可以個別啟用或停用效果，而效果參數也可以變更，而不會干擾音訊。</span><span class="sxs-lookup"><span data-stu-id="5ab29-113">Effect chains can be modified by the client dynamically (while the XAudio2 engine is running), effects can be enabled or disabled individually, and effect parameters can be changed—all without any interruption of the audio.</span></span> <span data-ttu-id="5ab29-114">每當效果圖形的任何方面變更時，XAudio2 會再次優化圖形，以避免不必要的處理。</span><span class="sxs-lookup"><span data-stu-id="5ab29-114">Whenever any aspect of the effect graph changes, XAudio2 optimizes the graph again to avoid unnecessary processing.</span></span> <span data-ttu-id="5ab29-115">請參閱 [**IXAudio2Voice：： SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain)、 [**IXAudio2Voice：： EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)和 [**IXAudio2Voice：： SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-115">See [**IXAudio2Voice::SetEffectChain**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectchain), [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect), and [**IXAudio2Voice::SetEffectParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters).</span></span>

<span data-ttu-id="5ab29-116">將效果附加至 XAudio2 聲音之後，XAudio2 會控制效果，而且用戶端不應該對其進行任何進一步的呼叫。</span><span class="sxs-lookup"><span data-stu-id="5ab29-116">After an effect is attached to an XAudio2 voice, XAudio2 takes control of the effect, and the client should not make any further calls to it.</span></span> <span data-ttu-id="5ab29-117">確保這一點最簡單的方式，就是釋放效果的所有指標。</span><span class="sxs-lookup"><span data-stu-id="5ab29-117">The simplest way to ensure this is to release all pointers to the effect.</span></span>

<span data-ttu-id="5ab29-118">給定 XAudio2 聲音效果鏈中的效果，必須以該語音的處理範例費率取用並產生浮點音訊。</span><span class="sxs-lookup"><span data-stu-id="5ab29-118">The effects in a given XAudio2 voice's effect chain must consume and produce floating-point audio at that voice's processing sample rate.</span></span> <span data-ttu-id="5ab29-119">其可變更之音訊格式的唯一層面是通道計數 (例如，將 mono 效果轉換成 5.1) 。</span><span class="sxs-lookup"><span data-stu-id="5ab29-119">The only aspect of the audio format they can change is the channel count (for example, a reverb effect can convert mono data to 5.1).</span></span> <span data-ttu-id="5ab29-120">用戶端可以使用 [**XAUDIO2 \_ 效果 \_ 描述**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)元。**OutputChannels** 欄位，指定每個效果應產生的通道數目。</span><span class="sxs-lookup"><span data-stu-id="5ab29-120">The client can use the [**XAUDIO2\_EFFECT\_DESCRIPTOR**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor).**OutputChannels** field to specify the number of channels that each effect should produce.</span></span> <span data-ttu-id="5ab29-121">如果有任何效果無法滿足這些需求，或如果效果產生了下一個效果無法處理的通道數目，效果鏈就會失敗。</span><span class="sxs-lookup"><span data-stu-id="5ab29-121">The effect chain fails if any of the effects cannot fulfill these requirements, or if an effect produces a number of channels that the next effect cannot handle.</span></span> <span data-ttu-id="5ab29-122">任何 [**IXAudio2Voice：： EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) 或 [**IXAudio2Voice：:D**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) 會導致效果鏈停止滿足這些需求的 isableeffect 呼叫都將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5ab29-122">Any [**IXAudio2Voice::EnableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect) or [**IXAudio2Voice::DisableEffect**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect) calls that cause the effect chain to stop fulfilling these requirements will fail.</span></span>

<span data-ttu-id="5ab29-123">XAudio2 中使用的 APO 介面必須是 *破壞性* 的。</span><span class="sxs-lookup"><span data-stu-id="5ab29-123">APO interfaces used in XAudio2 must be *destructive*.</span></span> <span data-ttu-id="5ab29-124">這表示它們一律會覆寫他們在輸出緩衝區中找到的任何資料。</span><span class="sxs-lookup"><span data-stu-id="5ab29-124">This means they always overwrite any data they find in their output buffers.</span></span> <span data-ttu-id="5ab29-125">否則，產生的音訊可能會不正確，因為 XAudio2 無法保證這些緩衝區先前已使用無聲初始化。</span><span class="sxs-lookup"><span data-stu-id="5ab29-125">Otherwise, the resulting audio might be incorrect because XAudio2 makes no guarantee that these buffers have been initialized previously with silence.</span></span>

## <a name="xaudio2-built-in-effects"></a><span data-ttu-id="5ab29-126">XAudio2 內建效果</span><span class="sxs-lookup"><span data-stu-id="5ab29-126">XAudio2 Built-in Effects</span></span>

<span data-ttu-id="5ab29-127">下表列出 XAudio2 所提供的內建音訊效果及其建立方法。</span><span class="sxs-lookup"><span data-stu-id="5ab29-127">The following table lists the set of built-in audio effects provided by XAudio2 and their creation methods.</span></span> 

| <span data-ttu-id="5ab29-128">效果</span><span class="sxs-lookup"><span data-stu-id="5ab29-128">Effect</span></span>       | <span data-ttu-id="5ab29-129">建立方法</span><span class="sxs-lookup"><span data-stu-id="5ab29-129">Creation Method</span></span>                                              |
|--------------|--------------------------------------------------------------|
| <span data-ttu-id="5ab29-130">混響</span><span class="sxs-lookup"><span data-stu-id="5ab29-130">Reverb</span></span>       | [<span data-ttu-id="5ab29-131">**XAudio2CreateReverb**</span><span class="sxs-lookup"><span data-stu-id="5ab29-131">**XAudio2CreateReverb**</span></span>](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createreverb)           |
| <span data-ttu-id="5ab29-132">磁片區計量</span><span class="sxs-lookup"><span data-stu-id="5ab29-132">Volume Meter</span></span> | [<span data-ttu-id="5ab29-133">**XAudio2CreateVolumeMeter**</span><span class="sxs-lookup"><span data-stu-id="5ab29-133">**XAudio2CreateVolumeMeter**</span></span>](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-xaudio2createvolumemeter) |



 

<span data-ttu-id="5ab29-134">如需建立和使用音訊效果實例的範例，請參閱 [如何：建立效果鏈](how-to--create-an-effect-chain.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-134">For an example of creating and using an instance of an audio effect, see [How to: Create an Effect Chain](how-to--create-an-effect-chain.md).</span></span>

## <a name="custom-effects-in-xaudio2"></a><span data-ttu-id="5ab29-135">XAudio2 中的自訂效果</span><span class="sxs-lookup"><span data-stu-id="5ab29-135">Custom Effects in XAudio2</span></span>

<span data-ttu-id="5ab29-136">[XAPO](xapo-overview.md) API 提供的架構可讓您建立可在 XAudio2 中使用的自訂音訊效果。</span><span class="sxs-lookup"><span data-stu-id="5ab29-136">The [XAPO](xapo-overview.md) API provides a framework for creating custom audio effects that you can use in XAudio2.</span></span> <span data-ttu-id="5ab29-137">如需使用 XAPO 建立自訂效果的範例，請參閱 [如何：建立 XAPO](how-to--create-an-xapo.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-137">For an example of creating a custom effect with XAPO, see [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>

## <a name="xapo-effect-library-xapofx"></a><span data-ttu-id="5ab29-138">XAPO 效果程式庫 (XAPOFX) </span><span class="sxs-lookup"><span data-stu-id="5ab29-138">XAPO Effect Library (XAPOFX)</span></span>

<span data-ttu-id="5ab29-139">[XAPOFX](xapofx-overview.md) 提供額外的 XAPOs 程式庫，以及建立它們的常用機制。</span><span class="sxs-lookup"><span data-stu-id="5ab29-139">[XAPOFX](xapofx-overview.md) provides an additional library of XAPOs and common mechanism for creating them.</span></span> <span data-ttu-id="5ab29-140">如需搭配使用 XAPOFX 與 XAudio2 的範例，請參閱 [如何：使用 XAudio2 中的 XAPOFX](how-to--use-xapofx-in-xaudio2.md)。</span><span class="sxs-lookup"><span data-stu-id="5ab29-140">For an example of using XAPOFX with XAudio2, see [How to: Use XAPOFX in XAudio2](how-to--use-xapofx-in-xaudio2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ab29-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="5ab29-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab29-142">音訊效果</span><span class="sxs-lookup"><span data-stu-id="5ab29-142">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="5ab29-143">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="5ab29-143">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> </dl>

 

 
