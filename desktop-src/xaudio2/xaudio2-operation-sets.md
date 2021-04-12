---
description: 本總覽導入了數個 XAudio2 方法，您可以呼叫這些方法作為作業集的一部分。
ms.assetid: 5bfd747d-af65-f619-e549-be8130748261
title: XAudio2 操作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90955fc0557f3f84840436c121f768caff4af81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195297"
---
# <a name="xaudio2-operation-sets"></a><span data-ttu-id="cc19d-103">XAudio2 操作集</span><span class="sxs-lookup"><span data-stu-id="cc19d-103">XAudio2 Operation Sets</span></span>

<span data-ttu-id="cc19d-104">本總覽導入了數個 XAudio2 方法，您可以呼叫這些方法作為作業集的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc19d-104">This overview introduces several XAudio2 methods that you can call as part of an operation set.</span></span>

<span data-ttu-id="cc19d-105">有數個 XAudio2 方法會採用 *OperationSet* 引數，這可讓它們作為延遲群組的一部分來呼叫。</span><span class="sxs-lookup"><span data-stu-id="cc19d-105">Several XAudio2 methods take the *OperationSet* argument, which allows them to be called as part of a deferred group.</span></span> <span data-ttu-id="cc19d-106">在特定時間，您可以藉由呼叫函式 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) 與該群組的 *OperationSet* 識別碼，同時套用整個變更集。</span><span class="sxs-lookup"><span data-stu-id="cc19d-106">At a specific time, you can apply an entire set of changes simultaneously by calling the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the *OperationSet* identifier for that group.</span></span> <span data-ttu-id="cc19d-107">識別碼為任意數目。</span><span class="sxs-lookup"><span data-stu-id="cc19d-107">The identifier is an arbitrary number.</span></span> <span data-ttu-id="cc19d-108">因此，它可讓用戶端程式代碼的個別部分在沒有任何衝突的情況下，將個別的不可部分完成變更套用到圖形。</span><span class="sxs-lookup"><span data-stu-id="cc19d-108">Thus, it allows separate parts of the client code to apply separate atomic changes to the graph without any conflict.</span></span> <span data-ttu-id="cc19d-109">建議的作法是讓用戶端在需要產生唯一的新 *OperationSet* 識別碼時，遞增全域計數器。</span><span class="sxs-lookup"><span data-stu-id="cc19d-109">The recommended practice is for the client to increment a global counter whenever it needs to generate a unique, new *OperationSet* identifier.</span></span> <span data-ttu-id="cc19d-110">對圖形進行的一組變更（以不可部分完成的方式套用）保證會是正確的範例。</span><span class="sxs-lookup"><span data-stu-id="cc19d-110">A set of changes to the graph, applied atomically, is guaranteed to be sample-accurate.</span></span> <span data-ttu-id="cc19d-111">例如，語音將會開始同步。</span><span class="sxs-lookup"><span data-stu-id="cc19d-111">For example, voices will start in sync.</span></span>

<span data-ttu-id="cc19d-112">如果您現在將 *OperationSet* 設定為 XAUDIO2 \_ COMMIT \_ ，則變更會立即套用。</span><span class="sxs-lookup"><span data-stu-id="cc19d-112">If you set *OperationSet* to XAUDIO2\_COMMIT\_NOW, the change applies immediately.</span></span> <span data-ttu-id="cc19d-113">它會在方法呼叫之後的第一個音訊處理階段中生效。</span><span class="sxs-lookup"><span data-stu-id="cc19d-113">It takes effect in the first audio processing pass after the method call.</span></span> <span data-ttu-id="cc19d-114">如果您呼叫 [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2 \_ COMMIT \_ ALL，則會執行所有擱置中作業集的變更，不論其 *OperationSet* 識別碼為何。</span><span class="sxs-lookup"><span data-stu-id="cc19d-114">If you call [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with XAUDIO2\_COMMIT\_ALL, changes to all pending operations sets are performed, regardless of their *OperationSet* identifier.</span></span>

<span data-ttu-id="cc19d-115">某些方法會在從 XAudio2 回呼以立即 *OperationSet* 的 XAudio2 認可呼叫時立即生效 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="cc19d-115">Certain methods take effect immediately when they are called from an XAudio2 callback with an *OperationSet* of XAUDIO2\_COMMIT\_NOW.</span></span> <span data-ttu-id="cc19d-116">所有其他採用 *OperationSet* 引數的方法，只會在呼叫方法之後，才會影響下一次處理階段 (如果立即呼叫 with XAUDIO2 \_ COMMIT \_) ，或在使用相同 *OperationSet* 來呼叫 [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges)之後。</span><span class="sxs-lookup"><span data-stu-id="cc19d-116">All other methods that take an *OperationSet* argument only take effect on the next processing pass after the method is called (if called with XAUDIO2\_COMMIT\_NOW), or after [**CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) is called with the same *OperationSet*.</span></span> <span data-ttu-id="cc19d-117">因此，某些方法呼叫不一定會依照呼叫的順序來進行。</span><span class="sxs-lookup"><span data-stu-id="cc19d-117">Because of this, certain method calls may not always happen in the same order in which they were called.</span></span>

<span data-ttu-id="cc19d-118">呼叫 [**IXAudio2：： StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) 時，會以不可部分完成的方式認可所有暫止的作業。</span><span class="sxs-lookup"><span data-stu-id="cc19d-118">All pending operations are committed atomically when [**IXAudio2::StopEngine**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-stopengine) is called.</span></span> <span data-ttu-id="cc19d-119">無論提供的 *OperationSet* 值為何，在引擎停止時呼叫的任何方法都會立即生效。</span><span class="sxs-lookup"><span data-stu-id="cc19d-119">Any methods that are called while the engine is stopped take effect immediately, regardless of the *OperationSet* value provided.</span></span> <span data-ttu-id="cc19d-120">當您重新開機引擎時，XAudio2 會回到非同步模式。</span><span class="sxs-lookup"><span data-stu-id="cc19d-120">When you restart the engine, XAudio2 returns to asynchronous mode.</span></span>

<span data-ttu-id="cc19d-121">作業集很有用的簡單案例包括下列範例。</span><span class="sxs-lookup"><span data-stu-id="cc19d-121">Simple scenarios in which operation sets are useful include the following examples.</span></span>

-   <span data-ttu-id="cc19d-122">同時啟動多個語音。</span><span class="sxs-lookup"><span data-stu-id="cc19d-122">Starting multiple voices simultaneously.</span></span>
-   <span data-ttu-id="cc19d-123">同時提交緩衝區至語音、設定語音參數，以及開始語音。</span><span class="sxs-lookup"><span data-stu-id="cc19d-123">Simultaneously submitting a buffer to a voice, setting the voice parameters, and starting the voice.</span></span>
-   <span data-ttu-id="cc19d-124">對圖形進行大規模變更，例如將所有來源語音連接到新的 submix 語音。</span><span class="sxs-lookup"><span data-stu-id="cc19d-124">Making a large-scale change to the graph, such as connecting all source voices to a new submix voice.</span></span>

<span data-ttu-id="cc19d-125">如需使用作業集的範例，請參閱 [如何：將音訊方法分組為作業集](how-to--group-audio-methods-as-an-operation-set.md) 。</span><span class="sxs-lookup"><span data-stu-id="cc19d-125">See [How to: Group Audio Methods as an Operation Set](how-to--group-audio-methods-as-an-operation-set.md) for an example of using an operation set.</span></span>

## <a name="operation-set-methods"></a><span data-ttu-id="cc19d-126">Operation Set 方法</span><span class="sxs-lookup"><span data-stu-id="cc19d-126">Operation Set Methods</span></span>

<span data-ttu-id="cc19d-127">您可以呼叫下列方法作為作業集的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc19d-127">You can call the following methods as part of an operation set.</span></span>

-   [<span data-ttu-id="cc19d-128">**IXAudio2SourceVoice::ExitLoop**</span><span class="sxs-lookup"><span data-stu-id="cc19d-128">**IXAudio2SourceVoice::ExitLoop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-exitloop)
-   [<span data-ttu-id="cc19d-129">**IXAudio2Voice::SetFilterParameters**</span><span class="sxs-lookup"><span data-stu-id="cc19d-129">**IXAudio2Voice::SetFilterParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters)
-   [<span data-ttu-id="cc19d-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span><span class="sxs-lookup"><span data-stu-id="cc19d-130">**IXAudio2SourceVoice::SetFrequencyRatio**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-setfrequencyratio)
-   [<span data-ttu-id="cc19d-131">**IXAudio2Voice：:D isableEffect**</span><span class="sxs-lookup"><span data-stu-id="cc19d-131">**IXAudio2Voice::DisableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-disableeffect)
-   [<span data-ttu-id="cc19d-132">**IXAudio2Voice::EnableEffect**</span><span class="sxs-lookup"><span data-stu-id="cc19d-132">**IXAudio2Voice::EnableEffect**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-enableeffect)
-   [<span data-ttu-id="cc19d-133">**IXAudio2Voice::SetChannelVolumes**</span><span class="sxs-lookup"><span data-stu-id="cc19d-133">**IXAudio2Voice::SetChannelVolumes**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes)
-   [<span data-ttu-id="cc19d-134">**IXAudio2Voice::SetEffectParameters**</span><span class="sxs-lookup"><span data-stu-id="cc19d-134">**IXAudio2Voice::SetEffectParameters**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-seteffectparameters)
-   [<span data-ttu-id="cc19d-135">**IXAudio2Voice::SetOutputMatrix**</span><span class="sxs-lookup"><span data-stu-id="cc19d-135">**IXAudio2Voice::SetOutputMatrix**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix)
-   [<span data-ttu-id="cc19d-136">**IXAudio2Voice::SetVolume**</span><span class="sxs-lookup"><span data-stu-id="cc19d-136">**IXAudio2Voice::SetVolume**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume)
-   [<span data-ttu-id="cc19d-137">**IXAudio2SourceVoice：： Start**</span><span class="sxs-lookup"><span data-stu-id="cc19d-137">**IXAudio2SourceVoice::Start**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start)
-   [<span data-ttu-id="cc19d-138">**IXAudio2SourceVoice：： Stop**</span><span class="sxs-lookup"><span data-stu-id="cc19d-138">**IXAudio2SourceVoice::Stop**</span></span>](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-stop)

<span data-ttu-id="cc19d-139">如先前所述，用戶端程式代碼最後必須呼叫函式 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) 來執行延遲的變更。</span><span class="sxs-lookup"><span data-stu-id="cc19d-139">As described previously, client code must ultimately call the function [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) to execute the deferred changes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc19d-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc19d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc19d-141">操作集</span><span class="sxs-lookup"><span data-stu-id="cc19d-141">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="cc19d-142">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="cc19d-142">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="cc19d-143">使用方法：將音訊方法群組為操作集</span><span class="sxs-lookup"><span data-stu-id="cc19d-143">How to: Group Audio Methods as an Operation Set</span></span>](how-to--group-audio-methods-as-an-operation-set.md)
</dt> </dl>

 

 
