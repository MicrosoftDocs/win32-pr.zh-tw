---
description: XAudio2 可呼叫用戶端所提供的函式，以非同步方式在音訊處理執行緒中發生特定事件時通知它。
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: XAudio2 回呼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320900"
---
# <a name="xaudio2-callbacks"></a><span data-ttu-id="eece1-103">XAudio2 回呼</span><span class="sxs-lookup"><span data-stu-id="eece1-103">XAudio2 Callbacks</span></span>

<span data-ttu-id="eece1-104">XAudio2 可呼叫用戶端所提供的函式，以非同步方式在音訊處理執行緒中發生特定事件時通知它。</span><span class="sxs-lookup"><span data-stu-id="eece1-104">XAudio2 can call functions provided by the client to notify it asynchronously of certain events taking place in the audio processing thread.</span></span> <span data-ttu-id="eece1-105">這些回呼可以是全域或特定的指定來源語音。</span><span class="sxs-lookup"><span data-stu-id="eece1-105">These callbacks can be global or specific to a given source voice.</span></span> <span data-ttu-id="eece1-106">若要接收全域引擎回呼，用戶端必須提供在初始化 XAudio2 時執行 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) 介面的類別實例。</span><span class="sxs-lookup"><span data-stu-id="eece1-106">To receive global engine callbacks, the client must provide an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface when initializing XAudio2.</span></span> <span data-ttu-id="eece1-107">若要接收來源語音回呼，用戶端必須提供在建立來源語音時實 [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) 介面的類別實例。</span><span class="sxs-lookup"><span data-stu-id="eece1-107">To receive source voice callbacks, the client must provide an instance of a class implementing the [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) interface when creating source voices.</span></span> <span data-ttu-id="eece1-108">如需詳細資訊，請參閱 **IXAudio2EngineCallback** 和 **IXAudio2VoiceCallback**。</span><span class="sxs-lookup"><span data-stu-id="eece1-108">For more details, see **IXAudio2EngineCallback** and **IXAudio2VoiceCallback**.</span></span>

<span data-ttu-id="eece1-109">您必須小心執行回呼，以避免在音訊中導致中斷。</span><span class="sxs-lookup"><span data-stu-id="eece1-109">You must implement callbacks carefully to avoid causing breaks in the audio.</span></span> <span data-ttu-id="eece1-110">每當回呼執行時，XAudio2 就無法產生任何音訊。</span><span class="sxs-lookup"><span data-stu-id="eece1-110">Whenever a callback is running, XAudio2 cannot generate any audio.</span></span> <span data-ttu-id="eece1-111">延遲超過幾毫秒可能會導致音訊問題。</span><span class="sxs-lookup"><span data-stu-id="eece1-111">Delays of more than a few milliseconds can cause an audio problem.</span></span> <span data-ttu-id="eece1-112">這種本質的延遲也會產生偵錯工具輸出。</span><span class="sxs-lookup"><span data-stu-id="eece1-112">Delays of this nature also generate debugger output.</span></span> <span data-ttu-id="eece1-113">這表示可能發生效能問題。</span><span class="sxs-lookup"><span data-stu-id="eece1-113">This indicates potential performance issues.</span></span> <span data-ttu-id="eece1-114">回呼函式至少不得執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="eece1-114">At a minimum, callback functions must not do the following:</span></span>

-   <span data-ttu-id="eece1-115">存取硬碟或其他永久儲存體</span><span class="sxs-lookup"><span data-stu-id="eece1-115">Access the hard disk or other permanent storage</span></span>
-   <span data-ttu-id="eece1-116">進行昂貴或封鎖的 API 呼叫</span><span class="sxs-lookup"><span data-stu-id="eece1-116">Make expensive or blocking API calls</span></span>
-   <span data-ttu-id="eece1-117">與用戶端程式代碼的其他部分同步處理</span><span class="sxs-lookup"><span data-stu-id="eece1-117">Synchronize with other parts of client code</span></span>
-   <span data-ttu-id="eece1-118">需要大量的 CPU 使用率</span><span class="sxs-lookup"><span data-stu-id="eece1-118">Require significant CPU usage</span></span>

<span data-ttu-id="eece1-119">如果用戶端設計需要回呼來觸發動作（如先前所列的動作），回呼應該會通知不同的用戶端執行緒來執行工作。</span><span class="sxs-lookup"><span data-stu-id="eece1-119">If the client design requires a callback to trigger actions such as those listed previously, the callback should signal a different client thread to do the work.</span></span> <span data-ttu-id="eece1-120">您可以使用簡單的 **SetEvent** 機制或更複雜的機制（例如另一個執行緒所耗用的非封鎖命令佇列）來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="eece1-120">You can do this with a simple **SetEvent** mechanism or more sophisticated mechanisms like a nonblocking command queue that is consumed by another thread.</span></span>

## <a name="ixaudio2enginecallback"></a><span data-ttu-id="eece1-121">IXAudio2EngineCallback</span><span class="sxs-lookup"><span data-stu-id="eece1-121">IXAudio2EngineCallback</span></span>

<span data-ttu-id="eece1-122">[**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)類別包含在 XAudio2 引擎中發生特定事件時通知用戶端的方法。</span><span class="sxs-lookup"><span data-stu-id="eece1-122">The [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) class contains methods that notify the client when certain events happen in the XAudio2 engine.</span></span> <span data-ttu-id="eece1-123">這些方法應該由 XAudio2 用戶端所執行。</span><span class="sxs-lookup"><span data-stu-id="eece1-123">These methods should be implemented by the XAudio2 client.</span></span> <span data-ttu-id="eece1-124">XAudio2 會使用 [**IXAudio2：： RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) 方法，透過用戶端所提供的介面指標來呼叫這些方法。</span><span class="sxs-lookup"><span data-stu-id="eece1-124">XAudio2 calls these methods by means of an interface pointer provided by the client using the [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) method.</span></span> <span data-ttu-id="eece1-125">所有這些方法都會傳回 **void**，而不是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="eece1-125">All these methods return **void**, rather than an **HRESULT**.</span></span>

## <a name="ixaudio2voicecallback"></a><span data-ttu-id="eece1-126">IXAudio2VoiceCallback</span><span class="sxs-lookup"><span data-stu-id="eece1-126">IXAudio2VoiceCallback</span></span>

<span data-ttu-id="eece1-127">[**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)類別包含的方法，會在特定的 XAudio2 來源語音中發生特定事件時通知用戶端。</span><span class="sxs-lookup"><span data-stu-id="eece1-127">The [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) class contains methods that notify the client when certain events happen in a specific XAudio2 source voice.</span></span> <span data-ttu-id="eece1-128">XAudio2 會透過 [**IXAudio2：： CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)中用戶端所提供的介面指標來呼叫這些方法。</span><span class="sxs-lookup"><span data-stu-id="eece1-128">XAudio2 calls these methods by means of an interface pointer provided by the client in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice).</span></span> <span data-ttu-id="eece1-129">如同 [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)，這些方法應該由 XAudio2 用戶端執行，並傳回 **Void** 而非 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="eece1-129">As with [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback), these methods should be implemented by the XAudio2 client, and return **void** rather than an **HRESULT**.</span></span>

<span data-ttu-id="eece1-130">如先前所述，用戶端提供的這些回呼的實，在毫秒內最好儘快恢復。</span><span class="sxs-lookup"><span data-stu-id="eece1-130">As mentioned previously, it is crucial that the client-provided implementations of these callbacks return as quickly as possible, preferably within a millisecond.</span></span> <span data-ttu-id="eece1-131">回呼是在音訊處理執行緒中執行，所有處理都會中斷，直到回呼傳回為止。</span><span class="sxs-lookup"><span data-stu-id="eece1-131">The callbacks are executed in the audio processing thread, and all processing is interrupted until the callback returns.</span></span> <span data-ttu-id="eece1-132">回呼中的延遲可能很容易造成音訊問題。</span><span class="sxs-lookup"><span data-stu-id="eece1-132">A delay in a callback can easily cause an audio problem.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eece1-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="eece1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eece1-134">回撥</span><span class="sxs-lookup"><span data-stu-id="eece1-134">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="eece1-135">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="eece1-135">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="eece1-136">使用方法：使用來源聲音回呼</span><span class="sxs-lookup"><span data-stu-id="eece1-136">How to: Use Source Voice Callbacks</span></span>](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[<span data-ttu-id="eece1-137">使用方法：使用引擎回呼</span><span class="sxs-lookup"><span data-stu-id="eece1-137">How to: Use Engine Callbacks</span></span>](how-to--use-engine-callbacks.md)
</dt> <dt>

[<span data-ttu-id="eece1-138">使用方法：從磁碟串流處理音效</span><span class="sxs-lookup"><span data-stu-id="eece1-138">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
