---
description: CMsgThread 類別是一個背景工作執行緒類別，會將要求排入佇列執行緒以進行非同步完成。
ms.assetid: 57e50abf-c90d-4c8f-afd8-25f29b6a0376
title: CMsgThread 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread
api_type:
- COM
api_location: ''
ms.openlocfilehash: 307b24e1563fe0545ee6f9405f9fb53e1b6d61b7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688452"
---
# <a name="cmsgthread-class"></a><span data-ttu-id="f51a2-103">CMsgThread 類別</span><span class="sxs-lookup"><span data-stu-id="f51a2-103">CMsgThread class</span></span>

<span data-ttu-id="f51a2-104">`CMsgThread`類別是一種背景工作執行緒類別，會將要求排入佇列執行緒以進行非同步完成。</span><span class="sxs-lookup"><span data-stu-id="f51a2-104">The `CMsgThread` class is a worker-thread class that queues requests to the queuing thread for completion asynchronously.</span></span> <span data-ttu-id="f51a2-105">若要使用此類別，請從它衍生您的類別，並覆寫 [**CMsgThread：： ThreadMessageProc**](cmsgthread-threadmessageproc.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="f51a2-105">To use this class, derive your class from it and override the [**CMsgThread::ThreadMessageProc**](cmsgthread-threadmessageproc.md) member function.</span></span> <span data-ttu-id="f51a2-106">**ThreadMessageProc** 成員函式會執行每個要求。</span><span class="sxs-lookup"><span data-stu-id="f51a2-106">The **ThreadMessageProc** member function carries out each request.</span></span> <span data-ttu-id="f51a2-107">您的用戶端函數和 **ThreadMessageProc** 成員函式必須共用 [**CMsg**](cmsg.md) 物件中參數的一般定義。</span><span class="sxs-lookup"><span data-stu-id="f51a2-107">Your client functions and the **ThreadMessageProc** member function must share a common definition of the parameters in the [**CMsg**](cmsg.md) object.</span></span>

<span data-ttu-id="f51a2-108">協商的機制會告知工作者執行緒結束。</span><span class="sxs-lookup"><span data-stu-id="f51a2-108">A negotiated mechanism tells the worker thread to exit.</span></span> <span data-ttu-id="f51a2-109">一般來說，這會是 [**CMsg**](cmsg.md) 類別的 **uMsg** 訊息代碼的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f51a2-109">Typically, this will be one value of the [**CMsg**](cmsg.md) class's **uMsg** message code.</span></span>

<span data-ttu-id="f51a2-110">最好從衍生類別的函式傳送此訊息，並在完成衍生類別的終結之前呼叫 [**CMsgThread：： WaitForThreadExit**](cmsgthread-waitforthreadexit.md) 成員函式。</span><span class="sxs-lookup"><span data-stu-id="f51a2-110">It is a good idea to send this message from the destructor of your derived class, and call the [**CMsgThread::WaitForThreadExit**](cmsgthread-waitforthreadexit.md) member function before completing the destruction of the derived class.</span></span>



| <span data-ttu-id="f51a2-111">受保護的資料成員</span><span class="sxs-lookup"><span data-stu-id="f51a2-111">Protected Data Members</span></span>                                    | <span data-ttu-id="f51a2-112">Description</span><span class="sxs-lookup"><span data-stu-id="f51a2-112">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f51a2-113">m \_ hSem</span><span class="sxs-lookup"><span data-stu-id="f51a2-113">m\_hSem</span></span>                                                   | <span data-ttu-id="f51a2-114">指出用於信號的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f51a2-114">Indicates a handle used for signaling.</span></span>                                                                                                |
| <span data-ttu-id="f51a2-115">m \_ 鎖定</span><span class="sxs-lookup"><span data-stu-id="f51a2-115">m\_Lock</span></span>                                                   | <span data-ttu-id="f51a2-116">保護對清單的存取。</span><span class="sxs-lookup"><span data-stu-id="f51a2-116">Protects access to lists.</span></span>                                                                                                             |
| <span data-ttu-id="f51a2-117">m \_ lWaiting</span><span class="sxs-lookup"><span data-stu-id="f51a2-117">m\_lWaiting</span></span>                                               | <span data-ttu-id="f51a2-118">指出等候可用的執行緒。</span><span class="sxs-lookup"><span data-stu-id="f51a2-118">Indicates waiting for a free thread.</span></span>                                                                                                  |
| <span data-ttu-id="f51a2-119">m \_ ThreadQueue</span><span class="sxs-lookup"><span data-stu-id="f51a2-119">m\_ThreadQueue</span></span>                                            | <span data-ttu-id="f51a2-120">覆寫 [**CMsgThread：： GetThreadMsg**](cmsgthread-getthreadmsg.md) 成員函式和封鎖非此佇列的專案。</span><span class="sxs-lookup"><span data-stu-id="f51a2-120">Overrides the [**CMsgThread::GetThreadMsg**](cmsgthread-getthreadmsg.md) member function and blocks on things other than this queue.</span></span> |
| <span data-ttu-id="f51a2-121">成員函數</span><span class="sxs-lookup"><span data-stu-id="f51a2-121">Member Functions</span></span>                                          | <span data-ttu-id="f51a2-122">Description</span><span class="sxs-lookup"><span data-stu-id="f51a2-122">Description</span></span>                                                                                                                           |
| [<span data-ttu-id="f51a2-123">**CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="f51a2-123">**CMsgThread**</span></span>](cmsgthread-cmsgthread.md)               | <span data-ttu-id="f51a2-124">結構 **CMsgThread** 物件。</span><span class="sxs-lookup"><span data-stu-id="f51a2-124">Constructs a **CMsgThread** object.</span></span>                                                                                                   |
| [<span data-ttu-id="f51a2-125">**CreateThread**</span><span class="sxs-lookup"><span data-stu-id="f51a2-125">**CreateThread**</span></span>](cmsgthread-createthread.md)           | <span data-ttu-id="f51a2-126">建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="f51a2-126">Creates a thread.</span></span>                                                                                                                     |
| [<span data-ttu-id="f51a2-127">**GetThreadHandle**</span><span class="sxs-lookup"><span data-stu-id="f51a2-127">**GetThreadHandle**</span></span>](cmsgthread-getthreadhandle.md)     | <span data-ttu-id="f51a2-128">抓取執行緒控制碼。</span><span class="sxs-lookup"><span data-stu-id="f51a2-128">Retrieves the thread handle.</span></span>                                                                                                          |
| [<span data-ttu-id="f51a2-129">**GetThreadID**</span><span class="sxs-lookup"><span data-stu-id="f51a2-129">**GetThreadID**</span></span>](cmsgthread-getthreadid.md)             | <span data-ttu-id="f51a2-130">抓取執行緒的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f51a2-130">Retrieves the identifier of the thread.</span></span>                                                                                               |
| [<span data-ttu-id="f51a2-131">**GetThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="f51a2-131">**GetThreadPriority**</span></span>](cmsgthread-getthreadpriority.md) | <span data-ttu-id="f51a2-132">抓取目前的執行緒優先權。</span><span class="sxs-lookup"><span data-stu-id="f51a2-132">Retrieves the current thread priority.</span></span>                                                                                                |
| [<span data-ttu-id="f51a2-133">**PutThreadMsg**</span><span class="sxs-lookup"><span data-stu-id="f51a2-133">**PutThreadMsg**</span></span>](cmsgthread-putthreadmsg.md)           | <span data-ttu-id="f51a2-134">將背景工作執行緒執行的要求排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="f51a2-134">Queues a request for execution by the worker thread.</span></span>                                                                                  |
| [<span data-ttu-id="f51a2-135">**ResumeThread**</span><span class="sxs-lookup"><span data-stu-id="f51a2-135">**ResumeThread**</span></span>](cmsgthread-resumethread.md)           | <span data-ttu-id="f51a2-136">繼續進行工作者執行緒的操作。</span><span class="sxs-lookup"><span data-stu-id="f51a2-136">Continues the operation of the worker thread.</span></span>                                                                                         |
| [<span data-ttu-id="f51a2-137">**SetThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="f51a2-137">**SetThreadPriority**</span></span>](cmsgthread-setthreadpriority.md) | <span data-ttu-id="f51a2-138">將執行緒的優先權設定為新的值。</span><span class="sxs-lookup"><span data-stu-id="f51a2-138">Sets the priority of the thread to a new value.</span></span>                                                                                       |
| [<span data-ttu-id="f51a2-139">**SuspendThread**</span><span class="sxs-lookup"><span data-stu-id="f51a2-139">**SuspendThread**</span></span>](cmsgthread-suspendthread.md)         | <span data-ttu-id="f51a2-140">暫停執行中線程的操作。</span><span class="sxs-lookup"><span data-stu-id="f51a2-140">Suspends the operation of a running thread.</span></span>                                                                                           |
| [<span data-ttu-id="f51a2-141">**WaitForThreadExit**</span><span class="sxs-lookup"><span data-stu-id="f51a2-141">**WaitForThreadExit**</span></span>](cmsgthread-waitforthreadexit.md) | <span data-ttu-id="f51a2-142">封鎖直到執行緒在呼叫 [**CMsgThread：： SuspendThread**](cmsgthread-suspendthread.md) 成員函式之後結束為止。</span><span class="sxs-lookup"><span data-stu-id="f51a2-142">Blocks until the thread has exited after a call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span> |
| <span data-ttu-id="f51a2-143">可覆寫的成員函式</span><span class="sxs-lookup"><span data-stu-id="f51a2-143">Overridable Member Functions</span></span>                              | <span data-ttu-id="f51a2-144">Description</span><span class="sxs-lookup"><span data-stu-id="f51a2-144">Description</span></span>                                                                                                                           |
| [<span data-ttu-id="f51a2-145">**GetThreadMsg**</span><span class="sxs-lookup"><span data-stu-id="f51a2-145">**GetThreadMsg**</span></span>](cmsgthread-getthreadmsg.md)           | <span data-ttu-id="f51a2-146">抓取包含要求的佇列 [**CMsg**](cmsg.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f51a2-146">Retrieves a queued [**CMsg**](cmsg.md) object containing a request.</span></span>                                                                  |
| [<span data-ttu-id="f51a2-147">**OnThreadInit**</span><span class="sxs-lookup"><span data-stu-id="f51a2-147">**OnThreadInit**</span></span>](cmsgthread-onthreadinit.md)           | <span data-ttu-id="f51a2-148">提供執行緒的初始化。</span><span class="sxs-lookup"><span data-stu-id="f51a2-148">Provides initialization on a thread.</span></span>                                                                                                  |
| [<span data-ttu-id="f51a2-149">**ThreadMessageProc**</span><span class="sxs-lookup"><span data-stu-id="f51a2-149">**ThreadMessageProc**</span></span>](cmsgthread-threadmessageproc.md) | <span data-ttu-id="f51a2-150">處理要求。</span><span class="sxs-lookup"><span data-stu-id="f51a2-150">Processes requests.</span></span> <span data-ttu-id="f51a2-151">這是單純的虛擬成員函式。</span><span class="sxs-lookup"><span data-stu-id="f51a2-151">This is a pure virtual member function.</span></span>                                                                           |



 

 

 



