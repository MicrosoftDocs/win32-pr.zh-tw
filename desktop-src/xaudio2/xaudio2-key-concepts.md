---
description: 本總覽介紹一些使用 XAudio2 的重要概念。
ms.assetid: 103e939f-7815-51c5-159a-c607da1e99ba
title: XAudio2 重要概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c2c0e173e2205070c9f94e8c25dcd9ce7e548c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990436"
---
# <a name="xaudio2-key-concepts"></a><span data-ttu-id="ad088-103">XAudio2 重要概念</span><span class="sxs-lookup"><span data-stu-id="ad088-103">XAudio2 Key Concepts</span></span>

<span data-ttu-id="ad088-104">本總覽介紹一些使用 XAudio2 的重要概念。</span><span class="sxs-lookup"><span data-stu-id="ad088-104">This overview introduces some key concepts for using XAudio2.</span></span>

-   [<span data-ttu-id="ad088-105">XAudio2 引擎</span><span class="sxs-lookup"><span data-stu-id="ad088-105">XAudio2 Engine</span></span>](#xaudio2-engine)
-   [<span data-ttu-id="ad088-106">語音</span><span class="sxs-lookup"><span data-stu-id="ad088-106">Voices</span></span>](#voices)
-   [<span data-ttu-id="ad088-107">音訊圖形</span><span class="sxs-lookup"><span data-stu-id="ad088-107">Audio Graph</span></span>](#audio-graph)
-   [<span data-ttu-id="ad088-108">回撥</span><span class="sxs-lookup"><span data-stu-id="ad088-108">Callbacks</span></span>](#callbacks)
-   [<span data-ttu-id="ad088-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad088-109">Related Topics</span></span>](#related-topics)

## <a name="xaudio2-engine"></a><span data-ttu-id="ad088-110">XAudio2 引擎</span><span class="sxs-lookup"><span data-stu-id="ad088-110">XAudio2 Engine</span></span>

<span data-ttu-id="ad088-111">[**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面是 XAudio2 引擎的核心。</span><span class="sxs-lookup"><span data-stu-id="ad088-111">The [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface is the core of the XAudio2 engine.</span></span> <span data-ttu-id="ad088-112">建立 **IXAudio2** 介面的實例，可讓用戶端列舉可用的音訊裝置、設定全域 API 屬性、建立語音，以及監視效能。</span><span class="sxs-lookup"><span data-stu-id="ad088-112">Creating an instance of the **IXAudio2** interface allows the client to enumerate the available audio devices, to configure global API properties, to create voices, and to monitor performance.</span></span> <span data-ttu-id="ad088-113">[**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper 函式會針對 XAudio2 執行具現化和初始作業。</span><span class="sxs-lookup"><span data-stu-id="ad088-113">The [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) helper function performs instantiation and initialization tasks for XAudio2.</span></span>

<span data-ttu-id="ad088-114">您可以在單一進程內多次建立 XAudio2 的實例。</span><span class="sxs-lookup"><span data-stu-id="ad088-114">You can create instances of XAudio2 multiple times within a single process.</span></span> <span data-ttu-id="ad088-115">每個 XAudio2 物件會獨立運作，而且有自己的音訊處理執行緒。</span><span class="sxs-lookup"><span data-stu-id="ad088-115">Each XAudio2 object operates independently, and has its own audio processing thread.</span></span> <span data-ttu-id="ad088-116">只有 debug 設定是共用的。</span><span class="sxs-lookup"><span data-stu-id="ad088-116">Only the debug settings are shared.</span></span> <span data-ttu-id="ad088-117">這在 Windows 上很重要，因為在單一進程中可以載入數個不同的元件。</span><span class="sxs-lookup"><span data-stu-id="ad088-117">This is important on Windows where several different components may be loaded in a single process.</span></span> <span data-ttu-id="ad088-118">例如，Internet Explorer 可能會同時使用多個 XAudio2 元件。</span><span class="sxs-lookup"><span data-stu-id="ad088-118">For example, Internet Explorer might use multiple XAudio2 components simultaneously.</span></span> <span data-ttu-id="ad088-119">雖然可以在單一用戶端應用程式內建立多個 XAudio2 引擎物件，但您不應該在其各自的圖形之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="ad088-119">Although it is possible to create multiple XAudio2 engine objects within a single client application, you should not pass information between their respective graphs.</span></span>

<span data-ttu-id="ad088-120">如需初始化 XAudio2 引擎的範例，請參閱 [如何：初始化 XAudio2](how-to--initialize-xaudio2.md)。</span><span class="sxs-lookup"><span data-stu-id="ad088-120">For an example of initializing the XAudio2 engine, see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>

## <a name="voices"></a><span data-ttu-id="ad088-121">語音</span><span class="sxs-lookup"><span data-stu-id="ad088-121">Voices</span></span>

<span data-ttu-id="ad088-122">語音是 XAudio2 用來處理、操作及播放音訊資料的物件。</span><span class="sxs-lookup"><span data-stu-id="ad088-122">Voices are the objects XAudio2 use to process, to manipulate, and to play audio data.</span></span> <span data-ttu-id="ad088-123">XAudio2 中有三種類型的語音。</span><span class="sxs-lookup"><span data-stu-id="ad088-123">There are three types of voices in XAudio2.</span></span>

-   [<span data-ttu-id="ad088-124">**來源語音**</span><span class="sxs-lookup"><span data-stu-id="ad088-124">**Source Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)

    <span data-ttu-id="ad088-125">來源語音代表音訊資料的資料流程。</span><span class="sxs-lookup"><span data-stu-id="ad088-125">Source voices represent a stream of audio data.</span></span> <span data-ttu-id="ad088-126">來源語音會將其資料傳送至其他類型的語音。</span><span class="sxs-lookup"><span data-stu-id="ad088-126">Source voices send their data to other types of voices.</span></span>

-   [<span data-ttu-id="ad088-127">**Submix 語音**</span><span class="sxs-lookup"><span data-stu-id="ad088-127">**Submix Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)

    <span data-ttu-id="ad088-128">Submix 語音會對其所接收的音訊資料執行某些操作。</span><span class="sxs-lookup"><span data-stu-id="ad088-128">Submix voices perform some manipulation of audio data they receive.</span></span> <span data-ttu-id="ad088-129">音訊資料操作的其中一個範例可能是取樣率轉換。</span><span class="sxs-lookup"><span data-stu-id="ad088-129">One example of audio data manipulation might be sample rate conversion.</span></span> <span data-ttu-id="ad088-130">在 submix 聲音處理資料之後，它會將該資料傳遞給另一個 submix 聲音或主要語音。</span><span class="sxs-lookup"><span data-stu-id="ad088-130">After a submix voice processes data, it passes that data to another submix voice or to a master voice.</span></span>

-   [<span data-ttu-id="ad088-131">**主控語音**</span><span class="sxs-lookup"><span data-stu-id="ad088-131">**Mastering Voices**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)

    <span data-ttu-id="ad088-132">「掌控語音」會從來源語音和 submix 語音接收資料，並將該資料傳送到音訊硬體。</span><span class="sxs-lookup"><span data-stu-id="ad088-132">Mastering voices receive data from source voices and submix voices, and sends that data to the audio hardware.</span></span>

<span data-ttu-id="ad088-133">如需 XAudio2 聲音的總覽，請參閱 [XAudio2 語音](voices.md) 。</span><span class="sxs-lookup"><span data-stu-id="ad088-133">See [XAudio2 Voices](voices.md) for an overview of XAudio2 voices.</span></span>

## <a name="audio-graph"></a><span data-ttu-id="ad088-134">音訊圖形</span><span class="sxs-lookup"><span data-stu-id="ad088-134">Audio Graph</span></span>

<span data-ttu-id="ad088-135">音訊圖形是一組 XAudio2 語音。</span><span class="sxs-lookup"><span data-stu-id="ad088-135">An audio graph is a collection of XAudio2 voices.</span></span> <span data-ttu-id="ad088-136">音訊會以來源語音中音訊圖表的一端開始，選擇性地通過一或多個 submix 語音，並以精通聲音結束。</span><span class="sxs-lookup"><span data-stu-id="ad088-136">Audio starts at one side of an audio graph in source voices, optionally passes through one or more submix voices, and ends at a mastering voice.</span></span> <span data-ttu-id="ad088-137">音訊圖形會包含每個目前播放的音效、零個或更多的 submix 語音，以及一個主控聲音的來源聲音。</span><span class="sxs-lookup"><span data-stu-id="ad088-137">An audio graph will contain a source voice for each sound currently playing, zero or more submix voices, and one mastering voice.</span></span> <span data-ttu-id="ad088-138">最簡單的音訊圖形，以及在 XAudio2 中發出雜訊所需的最小值，都是單一來源語音，直接輸出至主控語音。</span><span class="sxs-lookup"><span data-stu-id="ad088-138">The simplest audio graph, and the minimum needed to make a noise in XAudio2, is a single source voice outputting directly to a mastering voice.</span></span> <span data-ttu-id="ad088-139">請參閱 [如何：使用 XAudio2 播放音效](how-to--play-a-sound-with-xaudio2.md) ，以取得使用 XAudio2 播放音效所需的最少步驟範例。</span><span class="sxs-lookup"><span data-stu-id="ad088-139">See [How to: Play a Sound with XAudio2](how-to--play-a-sound-with-xaudio2.md) for an example of the minimum steps need to play a sound with XAudio2.</span></span>

<span data-ttu-id="ad088-140">如需 XAudio2 音訊圖表的總覽，請參閱 [XAudio2 音訊圖形](audio-graphs.md) 。</span><span class="sxs-lookup"><span data-stu-id="ad088-140">See [XAudio2 Audio Graph](audio-graphs.md) for an overview of XAudio2 audio graphs.</span></span>

## <a name="callbacks"></a><span data-ttu-id="ad088-141">回撥</span><span class="sxs-lookup"><span data-stu-id="ad088-141">Callbacks</span></span>

<span data-ttu-id="ad088-142">回呼是 XAudio2 用來信號用戶端程式代碼的機制，也就是某個事件發生在聲音或引擎物件中。</span><span class="sxs-lookup"><span data-stu-id="ad088-142">Callbacks are the mechanism XAudio2 uses to signal client code that some event has occurred in a voice or in the engine object.</span></span> <span data-ttu-id="ad088-143">由於音訊播放在 XAudio2 引擎中是非同步，因此回呼提供唯一的方法來判斷音效何時完成播放。</span><span class="sxs-lookup"><span data-stu-id="ad088-143">Because audio playback is asynchronous in the XAudio2 engine, callbacks provide the only way to determine when a sound is finished playing.</span></span>

<span data-ttu-id="ad088-144">如需 XAudio2 回呼的總覽，請參閱 [XAudio2 回呼](callbacks.md) 。</span><span class="sxs-lookup"><span data-stu-id="ad088-144">See [XAudio2 Callbacks](callbacks.md) for an overview of XAudio2 callbacks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad088-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad088-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad088-146">快速入門</span><span class="sxs-lookup"><span data-stu-id="ad088-146">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="ad088-147">XAudio2 版本</span><span class="sxs-lookup"><span data-stu-id="ad088-147">XAudio2 Versions</span></span>](xaudio2-versions.md)
</dt> <dt>

[<span data-ttu-id="ad088-148">使用方法：初始化 XAudio2</span><span class="sxs-lookup"><span data-stu-id="ad088-148">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="ad088-149">操作說明：使用 XAudio2 播放音效</span><span class="sxs-lookup"><span data-stu-id="ad088-149">How to: Play a sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 



