---
description: 本主題說明如何使用 Microsoft 媒體基礎中的工作佇列。
ms.assetid: 6be05df7-e8ff-4110-8f73-a62eb31fd414
title: 使用工作佇列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7bb41b830742ca871d44cadac9bd26a9967aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191747"
---
# <a name="using-work-queues"></a><span data-ttu-id="36c17-103">使用工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-103">Using Work Queues</span></span>

<span data-ttu-id="36c17-104">本主題說明如何使用 Microsoft 媒體基礎中的工作佇列。</span><span class="sxs-lookup"><span data-stu-id="36c17-104">This topic describes how to use work queues in Microsoft Media Foundation.</span></span>

-   [<span data-ttu-id="36c17-105">使用工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-105">Using Work Queues</span></span>](#using-work-queues)
-   [<span data-ttu-id="36c17-106">關閉工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-106">Shutting Down Work Queues</span></span>](#shutting-down-work-queues)
-   [<span data-ttu-id="36c17-107">使用已排程的工作專案</span><span class="sxs-lookup"><span data-stu-id="36c17-107">Using Scheduled Work Items</span></span>](#using-scheduled-work-items)
-   [<span data-ttu-id="36c17-108">使用定期回呼</span><span class="sxs-lookup"><span data-stu-id="36c17-108">Using Periodic Callbacks</span></span>](#using-periodic-callbacks)
-   [<span data-ttu-id="36c17-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="36c17-109">Related topics</span></span>](#related-topics)

## <a name="using-work-queues"></a><span data-ttu-id="36c17-110">使用工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-110">Using Work Queues</span></span>

<span data-ttu-id="36c17-111">工作佇列是在另一個執行緒上執行非同步作業的有效方式。</span><span class="sxs-lookup"><span data-stu-id="36c17-111">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span> <span data-ttu-id="36c17-112">在概念上，您會將工作專案放入佇列中，而佇列會有一個執行緒從佇列提取每個專案，然後將其分派。</span><span class="sxs-lookup"><span data-stu-id="36c17-112">Conceptually, you put work items in the queue, and the queue has a thread that pulls each item from the queue and dispatches it.</span></span> <span data-ttu-id="36c17-113">使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面，將工作專案實作為回呼。</span><span class="sxs-lookup"><span data-stu-id="36c17-113">Work items are implemented as callbacks by using the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="36c17-114">媒體基礎會建立數個標準工作佇列，稱為「 *平臺工作佇列*」。</span><span class="sxs-lookup"><span data-stu-id="36c17-114">Media Foundation creates several standard work queues, called *platform work queues*.</span></span> <span data-ttu-id="36c17-115">應用程式也可以建立自己的工作佇列，稱為 *私用工作佇列*。</span><span class="sxs-lookup"><span data-stu-id="36c17-115">Applications can also create their own work queues, called *private work queues*.</span></span> <span data-ttu-id="36c17-116">如需平臺工作佇列的清單，請參閱 [工作佇列識別碼](work-queue-identifiers.md)。</span><span class="sxs-lookup"><span data-stu-id="36c17-116">For a list of the platform work queues, see [Work Queue Identifiers](work-queue-identifiers.md).</span></span> <span data-ttu-id="36c17-117">若要建立私用工作佇列，請呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)。</span><span class="sxs-lookup"><span data-stu-id="36c17-117">To create a private work queue, call [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).</span></span> <span data-ttu-id="36c17-118">此函數會傳回新工作佇列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36c17-118">This function returns an identifier for the new work queue.</span></span> <span data-ttu-id="36c17-119">若要將專案放在佇列中，請呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 或 [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex)。</span><span class="sxs-lookup"><span data-stu-id="36c17-119">To put an item in the queue, call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) or [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex).</span></span> <span data-ttu-id="36c17-120">在這兩種情況下，您都必須指定回呼介面。</span><span class="sxs-lookup"><span data-stu-id="36c17-120">In both cases, you must specify a callback interface.</span></span>

-   <span data-ttu-id="36c17-121">[**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 會使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面的指標，加上可實執行 **IUnknown** 的選擇性狀態物件。</span><span class="sxs-lookup"><span data-stu-id="36c17-121">[**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) takes a pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface, plus an optional state object that implements **IUnknown**.</span></span> <span data-ttu-id="36c17-122">這些是在非同步方法中使用的相同參數，如 [非同步回呼方法](asynchronous-callback-methods.md)主題中所述。</span><span class="sxs-lookup"><span data-stu-id="36c17-122">These are the same parameters used in asynchronous methods, as described in the topic [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span> <span data-ttu-id="36c17-123">就內部而言，此函式會建立非同步結果物件，並將它傳遞給回呼的 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。</span><span class="sxs-lookup"><span data-stu-id="36c17-123">Internally, this function creates an asynchronous result object, which is passed to the callback's [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span>
-   <span data-ttu-id="36c17-124">[**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) 會使用 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="36c17-124">[**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex) takes a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="36c17-125">此介面代表非同步結果物件。</span><span class="sxs-lookup"><span data-stu-id="36c17-125">This interface represents an asynchronous result object.</span></span> <span data-ttu-id="36c17-126">藉由呼叫 [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) ，並指定您的回呼介面和（選擇性）狀態物件來建立這個物件。</span><span class="sxs-lookup"><span data-stu-id="36c17-126">Create this object by calling [**MFCreateAsyncResult**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateasyncresult) and specifying your callback interface and, optionally, a state object.</span></span>

<span data-ttu-id="36c17-127">在這兩種情況下，工作佇列執行緒都會呼叫您的 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法。</span><span class="sxs-lookup"><span data-stu-id="36c17-127">In both cases, the work queue thread calls your [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="36c17-128">使用 **Invoke** 方法來執行工作專案。</span><span class="sxs-lookup"><span data-stu-id="36c17-128">Use the **Invoke** method to perform the work item.</span></span>

<span data-ttu-id="36c17-129">如果有多個執行緒或元件共用相同的工作佇列，您可以呼叫 [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) 來鎖定工作佇列，以防止平臺釋放它。</span><span class="sxs-lookup"><span data-stu-id="36c17-129">If more than one thread or component shares the same work queue, you can call [**MFLockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflockworkqueue) to lock the work queue, which prevents the platform from releasing it.</span></span> <span data-ttu-id="36c17-130">每次呼叫 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) 或 **MFLockWorkQueue** 時，您都必須呼叫 [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) 一次，才能釋放工作佇列。</span><span class="sxs-lookup"><span data-stu-id="36c17-130">For each call to [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) or **MFLockWorkQueue**, you must call [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue) once to release the work queue.</span></span> <span data-ttu-id="36c17-131">例如，如果您建立新的工作佇列，然後將它鎖定一次，則必須呼叫 **MFUnlockWorkQueue** 兩次，一次呼叫 **MFAllocateWorkQueue** ，一次用於 **MFLockWorkQueue** 的呼叫。</span><span class="sxs-lookup"><span data-stu-id="36c17-131">For example, if you create a new work queue and then lock it once, you must call **MFUnlockWorkQueue** twice, once for the call to **MFAllocateWorkQueue** and once for the call to **MFLockWorkQueue**.</span></span>

<span data-ttu-id="36c17-132">下列程式碼示範如何建立新的工作佇列、將工作專案放入佇列中，以及釋放工作佇列。</span><span class="sxs-lookup"><span data-stu-id="36c17-132">The following code shows how to create a new work queue, put a work item in the queue, and release the work queue.</span></span>

<span data-ttu-id="36c17-133">如需 Windows 8 中工作佇列的詳細資訊，請參閱 [工作佇列和執行緒改善](media-foundation-work-queue-and-threading-improvements.md) 。</span><span class="sxs-lookup"><span data-stu-id="36c17-133">See [Work Queue and Threading Improvements](media-foundation-work-queue-and-threading-improvements.md) for additional information on work queues in Windows 8.</span></span>


```C++
DWORD idWorkQueue = 0;
HRESULT hr = S_OK;

// Create a new work queue.
hr = MFAllocateWorkQueue(&idWorkQueue);

// Put an item on the queue.
if (SUCCEEDED(hr))
{
    hr = MFPutWorkItem(idWorkQueue, pCallback, NULL);
}

// Wait for the callback to be invoked.
if (SUCCEEDED(hr))
{
    WaitForSingleObject(hEvent, INFINITE);
}

// Release the work queue.
if (SUCCEEDED(hr))
{
    hr = MFUnlockWorkQueue(idWorkQueue);
}
```



<span data-ttu-id="36c17-134">此範例假設 *pCallback* 為應用程式的 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="36c17-134">This example assumes that *pCallback* is a pointer to the application's [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="36c17-135">它也會假設回呼會設定 *hEvent* 事件控制碼。</span><span class="sxs-lookup"><span data-stu-id="36c17-135">It also assumes that the callback sets the *hEvent* event handle.</span></span> <span data-ttu-id="36c17-136">程式碼會在呼叫 [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue)之前等候設定此事件。</span><span class="sxs-lookup"><span data-stu-id="36c17-136">The code waits for this event to be set before calling [**MFUnlockWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockworkqueue).</span></span>

<span data-ttu-id="36c17-137">工作佇列執行緒一律會在呼叫端的進程中建立。</span><span class="sxs-lookup"><span data-stu-id="36c17-137">Work queue threads are always created in the caller's process.</span></span> <span data-ttu-id="36c17-138">在每個工作佇列中，會序列化回呼。</span><span class="sxs-lookup"><span data-stu-id="36c17-138">Within each work queue, the callbacks are serialized.</span></span> <span data-ttu-id="36c17-139">如果您使用相同的工作佇列呼叫 [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) 兩次，則不會叫用第二個回呼，直到第一個回呼傳回為止。</span><span class="sxs-lookup"><span data-stu-id="36c17-139">If you call [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) twice with the same work queue, the second callback is not invoked until the first callback has returned.</span></span>

## <a name="shutting-down-work-queues"></a><span data-ttu-id="36c17-140">關閉工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-140">Shutting Down Work Queues</span></span>

<span data-ttu-id="36c17-141">在呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之前，請釋放工作佇列執行緒所使用的任何資源。</span><span class="sxs-lookup"><span data-stu-id="36c17-141">Before calling [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), release any resources that are being used by work queue threads.</span></span> <span data-ttu-id="36c17-142">若要同步處理這個進程，您可以鎖定媒體基礎的平臺，這可防止 **MFShutdown** 函式關閉任何工作佇列執行緒。</span><span class="sxs-lookup"><span data-stu-id="36c17-142">To synchronize this process, you can lock the Media Foundation platform, which prevents the **MFShutdown** function from closing any work queue threads.</span></span> <span data-ttu-id="36c17-143">如果在平臺鎖定時呼叫 **MFShutdown** ， **MFShutdown** 會等候數百毫秒讓平臺解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="36c17-143">If **MFShutdown** is called while the platform is locked, **MFShutdown** waits a few hundred milliseconds for the platform to be unlocked.</span></span> <span data-ttu-id="36c17-144">如果在該時間內未解除鎖定， **MFShutdown** 會關閉工作佇列執行緒。</span><span class="sxs-lookup"><span data-stu-id="36c17-144">If it is not unlocked within that time, **MFShutdown** closes the work queue threads.</span></span>

<span data-ttu-id="36c17-145">[**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)的預設執行會在建立結果物件時，自動鎖定媒體基礎平臺。</span><span class="sxs-lookup"><span data-stu-id="36c17-145">The default implementation of [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) automatically locks the Media Foundation platform when the result object is created.</span></span> <span data-ttu-id="36c17-146">釋放介面會將平臺解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="36c17-146">Releasing the interface unlocks the platform.</span></span> <span data-ttu-id="36c17-147">因此，您幾乎都不需要直接鎖定平臺。</span><span class="sxs-lookup"><span data-stu-id="36c17-147">Therefore, you will almost never need to lock the platform directly.</span></span> <span data-ttu-id="36c17-148">但是，如果您撰寫自己的 **IMFAsyncResult** 自訂執行，就應該手動鎖定和解除鎖定平臺。</span><span class="sxs-lookup"><span data-stu-id="36c17-148">But if you write your own custom implementation of **IMFAsyncResult**, then you should manually lock and unlock the platform.</span></span> <span data-ttu-id="36c17-149">若要鎖定平臺，請呼叫 [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform)。</span><span class="sxs-lookup"><span data-stu-id="36c17-149">To lock the platform, call [**MFLockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mflockplatform).</span></span> <span data-ttu-id="36c17-150">若要將平臺解除鎖定，請呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform)。</span><span class="sxs-lookup"><span data-stu-id="36c17-150">To unlock the platform, call [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform).</span></span> <span data-ttu-id="36c17-151">如需範例，請參閱 [自訂非同步結果物件](custom-asynchronous-result-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="36c17-151">For an example, see [Custom Asynchronous Result Objects](custom-asynchronous-result-objects.md).</span></span>

<span data-ttu-id="36c17-152">在您呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之後，您必須確保平臺會在5秒的超時期間內解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="36c17-152">After you call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), you need to ensure that the platform is unlocked within the 5-second time-out period.</span></span> <span data-ttu-id="36c17-153">若要這樣做，請釋放所有 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 的指標，並呼叫 [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) （如果您以手動方式鎖定平臺）。</span><span class="sxs-lookup"><span data-stu-id="36c17-153">Do this by releasing all [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) pointers, and by calling [**MFUnlockPlatform**](/windows/desktop/api/mfapi/nf-mfapi-mfunlockplatform) if you locked the platform manually.</span></span> <span data-ttu-id="36c17-154">請務必釋放工作佇列執行緒所使用的任何資源，否則您的應用程式可能會流失記憶體。</span><span class="sxs-lookup"><span data-stu-id="36c17-154">Make sure to release any resources that are being used by work queue threads, or your application might leak memory.</span></span>

<span data-ttu-id="36c17-155">一般來說，如果您的應用程式在呼叫 [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown)之前關閉並釋出每個媒體基礎物件，就不必擔心鎖定。</span><span class="sxs-lookup"><span data-stu-id="36c17-155">Typically, if your application shuts down and releases every Media Foundation object before calling [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown), you do not have to worry about locking.</span></span> <span data-ttu-id="36c17-156">鎖定機制只是在您呼叫 **MFShutdown** 之後，讓工作佇列執行緒正常結束。</span><span class="sxs-lookup"><span data-stu-id="36c17-156">The locking mechanism simply allows work queue threads to exit gracefully after you call **MFShutdown**.</span></span>

## <a name="using-scheduled-work-items"></a><span data-ttu-id="36c17-157">使用已排程的工作專案</span><span class="sxs-lookup"><span data-stu-id="36c17-157">Using Scheduled Work Items</span></span>

<span data-ttu-id="36c17-158">您可以藉由呼叫 [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) 或 [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex)，將回呼排程在一段時間後發生。</span><span class="sxs-lookup"><span data-stu-id="36c17-158">You can schedule a callback to occur after a set period of time by calling [**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) or [**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex).</span></span>

-   <span data-ttu-id="36c17-159">[**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) 會接受回呼的指標、選擇性的狀態物件，以及逾時間隔。</span><span class="sxs-lookup"><span data-stu-id="36c17-159">[**MFScheduleWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem) takes a pointer to your callback, an optional state object, and a time-out interval.</span></span>
-   <span data-ttu-id="36c17-160">[**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) 會採用非同步結果物件的指標和超時值。</span><span class="sxs-lookup"><span data-stu-id="36c17-160">[**MFScheduleWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex) takes a pointer to an asynchronous result object and a time-out value.</span></span>

<span data-ttu-id="36c17-161">以毫秒為單位，將超時指定為負數值。</span><span class="sxs-lookup"><span data-stu-id="36c17-161">Specify the time-out as a negative value in milliseconds.</span></span> <span data-ttu-id="36c17-162">例如，若要排定在5秒鐘內叫用回呼，請使用值−5000。</span><span class="sxs-lookup"><span data-stu-id="36c17-162">For example, to schedule a callback to be invoked in 5 seconds, use the value −5000.</span></span> <span data-ttu-id="36c17-163">這兩個函式都會傳回 **MFWORKITEM 索引 \_ 鍵值** ，您可以用來取消回呼，方法是將它傳遞至 [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) 函數。</span><span class="sxs-lookup"><span data-stu-id="36c17-163">Both functions return an **MFWORKITEM\_KEY** value, which you can use to cancel the callback by passing it to the [**MFCancelWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfcancelworkitem) function.</span></span>

<span data-ttu-id="36c17-164">排程的工作專案一律使用 MFASYNC \_ 回呼 \_ 佇列 \_ 計時器平臺工作佇列。</span><span class="sxs-lookup"><span data-stu-id="36c17-164">Scheduled work items always use the MFASYNC\_CALLBACK\_QUEUE\_TIMER platform work queue.</span></span>

## <a name="using-periodic-callbacks"></a><span data-ttu-id="36c17-165">使用定期回呼</span><span class="sxs-lookup"><span data-stu-id="36c17-165">Using Periodic Callbacks</span></span>

<span data-ttu-id="36c17-166">[**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback)函式會排定要定期叫用的回呼，直到您取消為止。</span><span class="sxs-lookup"><span data-stu-id="36c17-166">The [**MFAddPeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback) function schedules a callback to be invoked periodically until you cancel it.</span></span> <span data-ttu-id="36c17-167">回呼間隔是固定的;應用程式無法變更它。</span><span class="sxs-lookup"><span data-stu-id="36c17-167">The callback interval is fixed; applications cannot change it.</span></span> <span data-ttu-id="36c17-168">若要找出確切的間隔，請呼叫 [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity)。</span><span class="sxs-lookup"><span data-stu-id="36c17-168">To find out the exact interval, call [**MFGetTimerPeriodicity**](/windows/desktop/api/mfapi/nf-mfapi-mfgettimerperiodicity).</span></span> <span data-ttu-id="36c17-169">間隔是以10毫秒為單位，因此，此函式適用于您需要經常進行「滴答」的情況，例如執行簡報時鐘。</span><span class="sxs-lookup"><span data-stu-id="36c17-169">The interval is on the order of 10 milliseconds, so this function is meant for situations where you need a frequent "tick," such as implementing a presentation clock.</span></span> <span data-ttu-id="36c17-170">如果您想要將作業排程為較不頻繁地進行，請使用先前所述的排程工作專案。</span><span class="sxs-lookup"><span data-stu-id="36c17-170">If you want to schedule an operation to occur less frequently, use a scheduled work item, as described previously.</span></span>

<span data-ttu-id="36c17-171">不同于本主題中所述的其他回呼，定期回呼不會使用 [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面。</span><span class="sxs-lookup"><span data-stu-id="36c17-171">Unlike the other callbacks described in this topic, the periodic callback does not use the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="36c17-172">相反地，它會使用函式指標。</span><span class="sxs-lookup"><span data-stu-id="36c17-172">Instead, it uses a function pointer.</span></span> <span data-ttu-id="36c17-173">如需詳細資訊，請參閱 [**MFPERIODICCALLBACK 回呼**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback)。</span><span class="sxs-lookup"><span data-stu-id="36c17-173">For more information, see [**MFPERIODICCALLBACK Callback**](/windows/win32/api/mfapi/nc-mfapi-mfperiodiccallback).</span></span>

<span data-ttu-id="36c17-174">若要取消定期回呼，請呼叫 [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback)。</span><span class="sxs-lookup"><span data-stu-id="36c17-174">To cancel the periodic callback, call [**MFRemovePeriodicCallback**](/windows/desktop/api/mfapi/nf-mfapi-mfremoveperiodiccallback).</span></span>

<span data-ttu-id="36c17-175">定期回呼會使用 MFASYNC \_ 回呼 \_ 佇列 \_ 計時器平臺工作佇列。</span><span class="sxs-lookup"><span data-stu-id="36c17-175">Periodic callbacks use the MFASYNC\_CALLBACK\_QUEUE\_TIMER platform work queue.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36c17-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="36c17-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36c17-177">工作佇列</span><span class="sxs-lookup"><span data-stu-id="36c17-177">Work Queues</span></span>](work-queues.md)
</dt> <dt>

[<span data-ttu-id="36c17-178">**MFASYNCRESULT**</span><span class="sxs-lookup"><span data-stu-id="36c17-178">**MFASYNCRESULT**</span></span>](/windows/win32/api/mfapi/ns-mfapi-mfasyncresult)
</dt> <dt>

[<span data-ttu-id="36c17-179">工作佇列和執行緒改進</span><span class="sxs-lookup"><span data-stu-id="36c17-179">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 
