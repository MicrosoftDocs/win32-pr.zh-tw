---
description: XAudio2 是低層級的音訊 API。 它會針對類似于前身、DirectSound 和 XAudio 的遊戲，提供信號處理和混合基礎。
ms.assetid: c87be63a-58b5-9cd1-1f03-f32b5a858b2e
title: XAudio2 簡介
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7cde958256d9126746a07764dc0c792e88289c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984256"
---
# <a name="xaudio2-introduction"></a><span data-ttu-id="baa94-104">XAudio2 簡介</span><span class="sxs-lookup"><span data-stu-id="baa94-104">XAudio2 Introduction</span></span>

<span data-ttu-id="baa94-105">XAudio2 是低層級的音訊 API。</span><span class="sxs-lookup"><span data-stu-id="baa94-105">XAudio2 is a low-level audio API.</span></span> <span data-ttu-id="baa94-106">它會針對類似于前身、DirectSound 和 XAudio 的遊戲，提供信號處理和混合基礎。</span><span class="sxs-lookup"><span data-stu-id="baa94-106">It provides a signal processing and mixing foundation for games that is similar to its predecessors, DirectSound and XAudio.</span></span>

<span data-ttu-id="baa94-107">XAudio2 是適用于 DirectSound 的長時間等待取代。</span><span class="sxs-lookup"><span data-stu-id="baa94-107">XAudio2 is the long-awaited replacement for DirectSound.</span></span> <span data-ttu-id="baa94-108">它解決了數個未處理的問題和功能要求。</span><span class="sxs-lookup"><span data-stu-id="baa94-108">It addresses several outstanding issues and feature requests.</span></span>

## <a name="xaudio2-features"></a><span data-ttu-id="baa94-109">XAudio2 功能</span><span class="sxs-lookup"><span data-stu-id="baa94-109">XAudio2 Features</span></span>

<span data-ttu-id="baa94-110">以下是可讓開發人員改善其遊戲效能的 XAudio2 功能和新功能清單。</span><span class="sxs-lookup"><span data-stu-id="baa94-110">The following is a list of XAudio2 features and new functionality that enable developers to improve performance in their games.</span></span>

-   <span data-ttu-id="baa94-111">DSP 效果和每一語音篩選</span><span class="sxs-lookup"><span data-stu-id="baa94-111">DSP Effects and Per Voice Filtering</span></span>

    <span data-ttu-id="baa94-112">數位信號處理 (DSP) 效果是音訊的圖元著色器。</span><span class="sxs-lookup"><span data-stu-id="baa94-112">Digital Signal Processing (DSP) effects are the pixel shaders of audio.</span></span> <span data-ttu-id="baa94-113">它們都能處理轉換音效的一切問題—將 pig squeal 變成低、令人驚訝的怪物音效，以使用回音和遮蔽或障礙物篩選來放置遊戲環境中的聲音。</span><span class="sxs-lookup"><span data-stu-id="baa94-113">They handle everything from transforming a sound—turning a pig squeal into a low, scary monster sound—to placing sounds in the game environment using reverb and occlusion or obstruction filtering.</span></span> <span data-ttu-id="baa94-114">XAudio2 提供有彈性且功能強大的 DSP 架構。</span><span class="sxs-lookup"><span data-stu-id="baa94-114">XAudio2 provides a flexible and powerful DSP framework.</span></span> <span data-ttu-id="baa94-115">它也會針對每個語音提供內建的篩選準則，以提供有效率的低/高/頻外篩選效果。</span><span class="sxs-lookup"><span data-stu-id="baa94-115">It also provides a built-in filter on every voice, for efficient low/high/band-pass filtering effects.</span></span>

    <span data-ttu-id="baa94-116">如需有關 DSP 效果及每個語音篩選的詳細資訊，請參閱 [XAudio2 音訊效果](xaudio2-audio-effects.md) 和 [**IXAudio2Voice：： SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) 。</span><span class="sxs-lookup"><span data-stu-id="baa94-116">See [XAudio2 Audio Effects](xaudio2-audio-effects.md) and [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters) for more information about DSP effects and per voice filtering.</span></span>

-   <span data-ttu-id="baa94-117">Submixing</span><span class="sxs-lookup"><span data-stu-id="baa94-117">Submixing</span></span>

    <span data-ttu-id="baa94-118">Submixing 會將數個音效合併成單一音訊串流，例如，引擎音效由複合元件組成，全都是同時播放。</span><span class="sxs-lookup"><span data-stu-id="baa94-118">Submixing combines several sounds into a single audio stream—for example, an engine sound made up of composite parts, all of which are playing simultaneously.</span></span> <span data-ttu-id="baa94-119">此外，您也可以使用 submixing 來處理和合併遊戲的相似部分。</span><span class="sxs-lookup"><span data-stu-id="baa94-119">Also, you can use submixing to process and combine similar parts of a game.</span></span> <span data-ttu-id="baa94-120">例如，您可以結合所有遊戲音效效果，讓使用者音量設定可以在個別設定控制音樂音量時套用。</span><span class="sxs-lookup"><span data-stu-id="baa94-120">For example, you could combine all game sound effects to allow a user volume setting to be applied while a separate setting controls music volume.</span></span> <span data-ttu-id="baa94-121">Submixing 結合了 DSP，提供現今遊戲所需的資料路由與處理類型。</span><span class="sxs-lookup"><span data-stu-id="baa94-121">Combined with DSP, submixing provides the type of data routing and processing necessary for today's games.</span></span> <span data-ttu-id="baa94-122">XAudio2 允許任意層級的 submixing，讓您能夠建立複雜的音效和遊戲混合。</span><span class="sxs-lookup"><span data-stu-id="baa94-122">XAudio2 allows for arbitrary levels of submixing, enabling the creation of complex sounds and game mixes.</span></span>

    <span data-ttu-id="baa94-123">如需 submixing 的詳細資訊，請參閱 [XAudio2 音訊圖形](xaudio2-audio-graph.md) 和 [XAudio2 聲音](xaudio2-voices.md) 。</span><span class="sxs-lookup"><span data-stu-id="baa94-123">See [XAudio2 Audio Graph](xaudio2-audio-graph.md) and [XAudio2 Voices](xaudio2-voices.md) for more information about submixing.</span></span>

-   <span data-ttu-id="baa94-124">壓縮的音訊支援</span><span class="sxs-lookup"><span data-stu-id="baa94-124">Compressed Audio Support</span></span>

    <span data-ttu-id="baa94-125">DirectSound 的其中一個主要功能要求是針對壓縮的音訊支援。</span><span class="sxs-lookup"><span data-stu-id="baa94-125">One of the major feature requests for DirectSound has been for compressed audio support.</span></span> <span data-ttu-id="baa94-126">XAudio2 支援壓縮格式（ADPCM），以原生方式解壓縮執行時間。</span><span class="sxs-lookup"><span data-stu-id="baa94-126">XAudio2 supports compressed formats—ADPCM—natively with run-time decompression.</span></span>

-   <span data-ttu-id="baa94-127">增強的多重通道和環繞音效支援</span><span class="sxs-lookup"><span data-stu-id="baa94-127">Enhanced Multichannel and Surround Sound Support</span></span>

    <span data-ttu-id="baa94-128">多重通道、3D 和環繞音效支援都已展開。</span><span class="sxs-lookup"><span data-stu-id="baa94-128">Multichannel, 3D, and surround sound support is expanded.</span></span> <span data-ttu-id="baa94-129">3D 和環繞音效現在更有彈性且更透明。</span><span class="sxs-lookup"><span data-stu-id="baa94-129">3D and surround sound are now much more flexible and transparent.</span></span> <span data-ttu-id="baa94-130">XAudio2 會移除多聲道音效的6個通道限制，並支援任何具備多處理器功能的音訊卡上的多頻道音訊。</span><span class="sxs-lookup"><span data-stu-id="baa94-130">XAudio2 removes the 6-channel limit on multichannel sounds, and supports multichannel audio on any multichannel-capable audio card.</span></span> <span data-ttu-id="baa94-131">卡片不需要硬體加速。</span><span class="sxs-lookup"><span data-stu-id="baa94-131">The card does not need to be hardware-accelerated.</span></span>

-   <span data-ttu-id="baa94-132">Multirate 處理</span><span class="sxs-lookup"><span data-stu-id="baa94-132">Multirate Processing</span></span>

    <span data-ttu-id="baa94-133">為了協助將 CPU 使用率降至最低，XAudio2 提供了建立多個低比率音訊處理圖形的技術。</span><span class="sxs-lookup"><span data-stu-id="baa94-133">To help minimize CPU usage, XAudio2 provides the technology to create multiple, low-rate audio processing graphs.</span></span> <span data-ttu-id="baa94-134">如此一來，如果速率小於 48 kHz，可讓遊戲以來源資料的速率處理音訊，以大幅降低 CPU 的使用量。</span><span class="sxs-lookup"><span data-stu-id="baa94-134">This can significantly reduce CPU usage by allowing a game to process audio at the rate of the source material if the rate is less than 48 kHz.</span></span>

-   <span data-ttu-id="baa94-135">非封鎖 API 模型</span><span class="sxs-lookup"><span data-stu-id="baa94-135">Nonblocking API Model</span></span>

    <span data-ttu-id="baa94-136">有幾個例外狀況，XAudio2 方法呼叫不會封鎖音訊處理引擎。</span><span class="sxs-lookup"><span data-stu-id="baa94-136">With few exceptions, an XAudio2 method call will not block the audio processing engine.</span></span> <span data-ttu-id="baa94-137">這表示用戶端可以在任何時間安全地進行一組方法呼叫，而不會封鎖長時間執行的呼叫而導致延遲。</span><span class="sxs-lookup"><span data-stu-id="baa94-137">This means that a client can safely make a set of method calls at any time without blocking on long-running calls causing delays.</span></span> <span data-ttu-id="baa94-138">例外狀況是 [**IXAudio2Voice：:D estroyvoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) 方法 (這種方法可能會封鎖引擎，直到終結的聲音已完成處理) 以及終止音訊執行緒的方法： [**IXAudio2：： StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) 和 [**IXAudio2：： Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release)。</span><span class="sxs-lookup"><span data-stu-id="baa94-138">The exceptions are the [**IXAudio2Voice::DestroyVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-destroyvoice) method (which may block the engine until the voice being destroyed is finished processing) and the methods that terminate the audio thread: [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) and [**IXAudio2::Release**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-release).</span></span> <span data-ttu-id="baa94-139">請注意，雖然 XAudio2 方法呼叫不會封鎖音訊處理引擎，但 XAudio2 方法包含重要區段，而且在某些情況下可能會遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="baa94-139">Note that while XAudio2 method calls will not block the audio processing engine, the XAudio2 methods contain critical sections and may themselves become blocked in some circumstances.</span></span>

## <a name="when-to-use-xaudio2"></a><span data-ttu-id="baa94-140">使用 XAudio2 的時機</span><span class="sxs-lookup"><span data-stu-id="baa94-140">When to use XAudio2</span></span>

<span data-ttu-id="baa94-141">XAudio2 主要是用來開發適用于遊戲的高效能音訊引擎。</span><span class="sxs-lookup"><span data-stu-id="baa94-141">XAudio2 is primarily intended for developing high performance audio engines for games.</span></span> <span data-ttu-id="baa94-142">對於想在新型遊戲中增加音效和背景音樂的遊戲開發人員而言，XAudio2 可提供低延遲的音訊圖形和混合引擎，並且支援動態緩衝區、同步取樣精確播放，以及隱含的來源速率轉換。</span><span class="sxs-lookup"><span data-stu-id="baa94-142">For game developers who want to add sound effects and background music to their modern games, XAudio2 offers an audio graph and mixing engine with low-latency and support for dynamic buffers, synchronous sample-accurate playback, and implicit source rate conversion.</span></span> <span data-ttu-id="baa94-143">相較于 WASAPI，XAudio2 只需要最少量的程式碼，即使是複雜的音訊解決方案也一樣。</span><span class="sxs-lookup"><span data-stu-id="baa94-143">Compared to WASAPI, XAudio2 requires only a minimum amount of code even for complex audio solutions.</span></span> <span data-ttu-id="baa94-144">相較于媒體基礎引擎，XAudio2 是一種低層級的低延遲 c + + API，專為在遊戲中使用而設計。</span><span class="sxs-lookup"><span data-stu-id="baa94-144">Compared to the Media Foundation engine, XAudio2 is a low-level, low-latency C++ API that is designed for use in games.</span></span>

<span data-ttu-id="baa94-145">針對只需要定期播放音樂的應用程式，媒體基礎引擎可能與應用程式的需求更相符。</span><span class="sxs-lookup"><span data-stu-id="baa94-145">For applications that simply need regular music playback, the Media Foundation engine may be a better match to the application's requirements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baa94-146">相關主題</span><span class="sxs-lookup"><span data-stu-id="baa94-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa94-147">程式設計指南</span><span class="sxs-lookup"><span data-stu-id="baa94-147">Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="baa94-148">快速入門</span><span class="sxs-lookup"><span data-stu-id="baa94-148">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="baa94-149">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="baa94-149">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
