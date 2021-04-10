---
description: Wait Chain (WCT) 可讓偵錯工具診斷應用程式停止回應和鎖死。
ms.assetid: d266a663-b101-4936-9574-f6ce223419ae
title: 等候鏈遍歷
ms.topic: article
ms.date: 08/10/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 842beb7d5470bc2b3e6e9c7c1150ff2aa1a4cf76
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/04/2021
ms.locfileid: "103845663"
---
# <a name="wait-chain-traversal"></a><span data-ttu-id="4ac24-103">等候鏈遍歷</span><span class="sxs-lookup"><span data-stu-id="4ac24-103">Wait Chain Traversal</span></span>

<span data-ttu-id="4ac24-104">Wait Chain (WCT) 可讓偵錯工具診斷應用程式停止回應和鎖死。</span><span class="sxs-lookup"><span data-stu-id="4ac24-104">Wait Chain Traversal (WCT) enables debuggers to diagnose application hangs and deadlocks.</span></span>

<span data-ttu-id="4ac24-105">*等候鏈* 是執行緒和同步處理物件的交替順序，其中每個執行緒都會等候後面的物件。</span><span class="sxs-lookup"><span data-stu-id="4ac24-105">A *wait chain* is an alternating sequence of threads and synchronization objects where each thread waits for the object that follows.</span></span> <span data-ttu-id="4ac24-106">接下來的每個物件都是由鏈中的後續執行緒所擁有。</span><span class="sxs-lookup"><span data-stu-id="4ac24-106">Each object that follows is, in turn, owned by the subsequent thread in the chain.</span></span>

<span data-ttu-id="4ac24-107">執行緒等候同步處理物件的時間來自執行緒要求物件的時間，直到執行緒取得該物件為止。</span><span class="sxs-lookup"><span data-stu-id="4ac24-107">A thread waits for a synchronization object from the time the thread requests the object until the thread has acquired it.</span></span> <span data-ttu-id="4ac24-108">此「鎖定」是由執行緒取得執行緒時所擁有，直到執行緒釋放它為止。</span><span class="sxs-lookup"><span data-stu-id="4ac24-108">This "lock" is owned by a thread from the time the thread acquires it, until the thread releases it.</span></span> <span data-ttu-id="4ac24-109">換句話說，當執行緒1正在等候執行緒2所擁有的鎖定時，執行緒1的執行緒2就會「等待」。</span><span class="sxs-lookup"><span data-stu-id="4ac24-109">In other words, when thread 1 is waiting for a lock that is owned by thread 2, thread 1 is "waiting" for thread 2.</span></span>

<span data-ttu-id="4ac24-110">WCT 支援下列同步處理原始物件：</span><span class="sxs-lookup"><span data-stu-id="4ac24-110">WCT supports the following synchronization primitives:</span></span>

- [<span data-ttu-id="4ac24-111"> (ALPC) 的 Advanced Local Procedure 呼叫 </span><span class="sxs-lookup"><span data-stu-id="4ac24-111">Advanced Local Procedure Call (ALPC)</span></span>](../etw/alpc.md)
- [<span data-ttu-id="4ac24-112">元件物件模型 (COM)</span><span class="sxs-lookup"><span data-stu-id="4ac24-112">Component Object Model (COM)</span></span>](../com/the-component-object-model.md)
- [<span data-ttu-id="4ac24-113">重要區段</span><span class="sxs-lookup"><span data-stu-id="4ac24-113">Critical sections</span></span>](../sync/critical-section-objects.md)
- [<span data-ttu-id="4ac24-114">Mutex</span><span class="sxs-lookup"><span data-stu-id="4ac24-114">Mutexes</span></span>](../sync/mutex-objects.md)
- [<span data-ttu-id="4ac24-115">SendMessage</span><span class="sxs-lookup"><span data-stu-id="4ac24-115">SendMessage</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
- <span data-ttu-id="4ac24-116">[進程和執行緒](../procthread/processes-and-threads.md)的[等候](../sync/wait-functions.md)作業</span><span class="sxs-lookup"><span data-stu-id="4ac24-116">[Wait](../sync/wait-functions.md) operations on [processes and threads](../procthread/processes-and-threads.md)</span></span>

<span data-ttu-id="4ac24-117">若要取得一或多個執行緒的等候鏈，請使用 [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) 和 [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) 函式來建立 WCT 會話。</span><span class="sxs-lookup"><span data-stu-id="4ac24-117">To retrieve the wait chain for one or more threads, create a WCT session using the [OpenThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-openthreadwaitchainsession) and [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) functions.</span></span> <span data-ttu-id="4ac24-118">WCT 會話會以 **HWCT** 類型的控制碼表示。</span><span class="sxs-lookup"><span data-stu-id="4ac24-118">WCT sessions are represented by a handle of type **HWCT**.</span></span>

## <a name="sessions-can-be-synchronous-or-asynchronous"></a><span data-ttu-id="4ac24-119">會話可以是同步或非同步</span><span class="sxs-lookup"><span data-stu-id="4ac24-119">Sessions can be synchronous or asynchronous</span></span>

<span data-ttu-id="4ac24-120">除非已抓取等候鏈，否則無法取消同步會話，並封鎖呼叫執行緒。</span><span class="sxs-lookup"><span data-stu-id="4ac24-120">Synchronous sessions cannot be canceled, and block the calling thread, until a wait chain has been retrieved.</span></span>

<span data-ttu-id="4ac24-121">非同步會話不會封鎖呼叫的執行緒，而且可以使用 [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) 函式來取消應用程式。</span><span class="sxs-lookup"><span data-stu-id="4ac24-121">Asynchronous sessions do not block the calling thread, and can be canceled by the application using the [CloseThreadWaitChainSession](/windows/desktop/api/Wct/nf-wct-closethreadwaitchainsession) function.</span></span> <span data-ttu-id="4ac24-122">非同步作業的結果是透過應用程式所提供的 [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) 回呼函式提供。</span><span class="sxs-lookup"><span data-stu-id="4ac24-122">Results from asynchronous operations are made available through a [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function provided by the application.</span></span>

<span data-ttu-id="4ac24-123">針對非同步會話，呼叫端可以透過 [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) 指定內容資料結構的指標 (這個相同的指標會傳遞至 [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) 回呼函數) 。</span><span class="sxs-lookup"><span data-stu-id="4ac24-123">For asynchronous sessions, the caller can specify a pointer to a context data structure through [GetThreadWaitChain](/windows/desktop/api/Wct/nf-wct-getthreadwaitchain) (this same pointer is passed to the [WaitChainCallback](/windows/win32/api/wct/nc-wct-pwaitchaincallback) callback function).</span></span>

<span data-ttu-id="4ac24-124">內容資料結構是使用者定義的，而不是 WCT 的不透明。</span><span class="sxs-lookup"><span data-stu-id="4ac24-124">The context data structure is user-defined and opaque to WCT.</span></span> <span data-ttu-id="4ac24-125">應用程式可以使用它來在 WCT 查詢和回呼函數之間通訊內容。</span><span class="sxs-lookup"><span data-stu-id="4ac24-125">It can be used by the application to communicate context between a WCT query and a callback function.</span></span> <span data-ttu-id="4ac24-126">一般來說，您會透過此結構傳遞事件控制碼，並在執行回呼時，發出此事件的信號，並通知監視執行緒已完成查詢。</span><span class="sxs-lookup"><span data-stu-id="4ac24-126">Typically, you pass an event handle through this structure and, when the callback is executed, this event is signalled and a monitoring thread is informed that the query has been completed.</span></span>

<span data-ttu-id="4ac24-127">請參閱 [使用 WCT](using-wct.md) 以取得等候鏈進行的範例。</span><span class="sxs-lookup"><span data-stu-id="4ac24-127">See [Using WCT](using-wct.md) for an example of wait chain traversal.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ac24-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="4ac24-128">Related topics</span></span>

<span data-ttu-id="4ac24-129">[使用 WCT](using-wct.md)、 [WCT 參考](wct-reference.md)、 [MSDN 雜誌 2007 7 月-Bugslayer.web：等候鏈的遍歷](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span><span class="sxs-lookup"><span data-stu-id="4ac24-129">[Using WCT](using-wct.md), [WCT Reference](wct-reference.md), [MSDN Magazine 2007 July - Bugslayer: Wait Chain Traversal](/archive/msdn-magazine/2007/july/bugslayer-wait-chain-traversal)</span></span>