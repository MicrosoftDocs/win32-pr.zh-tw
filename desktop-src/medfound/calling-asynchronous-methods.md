---
description: 呼叫非同步方法
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: 呼叫非同步方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510822"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="e52ae-103">呼叫非同步方法</span><span class="sxs-lookup"><span data-stu-id="e52ae-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="e52ae-104">在媒體基礎中，會以非同步方式執行許多作業。</span><span class="sxs-lookup"><span data-stu-id="e52ae-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="e52ae-105">非同步作業可改善效能，因為它們不會封鎖呼叫執行緒。</span><span class="sxs-lookup"><span data-stu-id="e52ae-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="e52ae-106">媒體基礎中的非同步作業是由一組具有命名慣例 **Begin ...** 和 **End**... 的方法所定義。</span><span class="sxs-lookup"><span data-stu-id="e52ae-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="e52ae-107">這兩個方法一起定義了串流上的非同步讀取作業。</span><span class="sxs-lookup"><span data-stu-id="e52ae-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="e52ae-108">若要啟動非同步作業，請呼叫 **Begin** 方法。</span><span class="sxs-lookup"><span data-stu-id="e52ae-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="e52ae-109">**Begin** 方法一律包含至少兩個參數：</span><span class="sxs-lookup"><span data-stu-id="e52ae-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="e52ae-110">[**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e52ae-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="e52ae-111">應用程式必須執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="e52ae-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="e52ae-112">選擇性狀態物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e52ae-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="e52ae-113">當作業完成時， [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) 介面會通知應用程式。</span><span class="sxs-lookup"><span data-stu-id="e52ae-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="e52ae-114">如需如何執行此介面的範例，請參閱 [執行非同步回呼](implementing-the-asynchronous-callback.md)。</span><span class="sxs-lookup"><span data-stu-id="e52ae-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="e52ae-115">狀態物件是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="e52ae-115">The state object is optional.</span></span> <span data-ttu-id="e52ae-116">如果有指定，則必須執行 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="e52ae-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="e52ae-117">您可以使用 state 物件來儲存回呼所需的任何狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="e52ae-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="e52ae-118">如果您不需要狀態資訊，可以將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e52ae-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="e52ae-119">**Begin** 方法可能包含該方法特定的其他參數。</span><span class="sxs-lookup"><span data-stu-id="e52ae-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="e52ae-120">如果 **Begin** 方法傳回失敗碼，表示作業立即失敗，而且不會叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="e52ae-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="e52ae-121">如果 **Begin** 方法成功，則表示作業已暫止，並且會在作業完成時叫用回呼。</span><span class="sxs-lookup"><span data-stu-id="e52ae-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="e52ae-122">例如， [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) 方法會在位元組資料流程上啟動非同步讀取作業：</span><span class="sxs-lookup"><span data-stu-id="e52ae-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="e52ae-123">回呼方法是 [**IMFAsyncCallback：： Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)。</span><span class="sxs-lookup"><span data-stu-id="e52ae-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="e52ae-124">它有單一參數 *pAsyncResult*，也就是 [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e52ae-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="e52ae-125">若要完成非同步作業，請呼叫符合非同步 **Begin** 方法的 **End** 方法。</span><span class="sxs-lookup"><span data-stu-id="e52ae-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="e52ae-126">**End** 方法一律採用 **IMFAsyncResult** 指標。</span><span class="sxs-lookup"><span data-stu-id="e52ae-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="e52ae-127">一律傳入您在 **Invoke** 方法中收到的相同指標。</span><span class="sxs-lookup"><span data-stu-id="e52ae-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="e52ae-128">除非您呼叫 **End** 方法，否則非同步作業不會完成。</span><span class="sxs-lookup"><span data-stu-id="e52ae-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="e52ae-129">您可以從叫 **用方法內** 呼叫 End 方法，也可以從另一個執行緒呼叫 **End** 方法。</span><span class="sxs-lookup"><span data-stu-id="e52ae-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="e52ae-130">例如，若要在位元組資料流程上完成 [**IMFByteStream：： BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) ，請呼叫 [**IMFByteStream：： EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread)：</span><span class="sxs-lookup"><span data-stu-id="e52ae-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="e52ae-131">**End** 方法的傳回值表示非同步作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="e52ae-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="e52ae-132">在大部分情況下，您的應用程式會在非同步作業完成後執行某些工作，不論是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="e52ae-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="e52ae-133">您有幾種選項：</span><span class="sxs-lookup"><span data-stu-id="e52ae-133">You have several options:</span></span>

-   <span data-ttu-id="e52ae-134">在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法內執行工作。</span><span class="sxs-lookup"><span data-stu-id="e52ae-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="e52ae-135">只要您的應用程式永遠不會封鎖呼叫執行緒或等候叫 **用方法內** 的任何內容，就可以接受這個方法。</span><span class="sxs-lookup"><span data-stu-id="e52ae-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="e52ae-136">如果您封鎖呼叫的執行緒，您可能會封鎖串流管線。</span><span class="sxs-lookup"><span data-stu-id="e52ae-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="e52ae-137">例如，您可能會更新某些狀態變數，但不會執行同步讀取作業或等候 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="e52ae-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="e52ae-138">在 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 方法中，設定事件並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e52ae-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="e52ae-139">應用程式的呼叫執行緒會等待事件，並在發出事件時執行工作。</span><span class="sxs-lookup"><span data-stu-id="e52ae-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="e52ae-140">[**在叫用方法中**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)，將私用視窗訊息張貼至應用程式視窗，並立即傳回。</span><span class="sxs-lookup"><span data-stu-id="e52ae-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="e52ae-141">應用程式會在其訊息迴圈上執行工作。</span><span class="sxs-lookup"><span data-stu-id="e52ae-141">The application does the work on its message loop.</span></span> <span data-ttu-id="e52ae-142"> (請務必透過呼叫 **PostMessage**（而非 **SendMessage**）來張貼訊息，因為 **SendMessage** 可以封鎖回呼執行緒。 ) </span><span class="sxs-lookup"><span data-stu-id="e52ae-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="e52ae-143">請務必記住， [**調用**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 是從另一個執行緒呼叫。</span><span class="sxs-lookup"><span data-stu-id="e52ae-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="e52ae-144">您的應用程式會負責確保在 **Invoke** 內執行的任何工作都是安全線程。</span><span class="sxs-lookup"><span data-stu-id="e52ae-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="e52ae-145">依預設，呼叫 [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) 的執行緒不會假設您的回呼物件行為。</span><span class="sxs-lookup"><span data-stu-id="e52ae-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="e52ae-146">（選擇性）您可以執行 [**IMFAsyncCallback：： GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) 方法，以傳回回呼執行的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e52ae-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="e52ae-147">否則，此方法可能會傳回 **E \_ >notimpl**：</span><span class="sxs-lookup"><span data-stu-id="e52ae-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="e52ae-148">如果您在 **Begin** 方法中指定了狀態物件，則可以藉由呼叫 [**IMFAsyncResult：： >getstate**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)，從回呼方法內取出它。</span><span class="sxs-lookup"><span data-stu-id="e52ae-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e52ae-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="e52ae-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e52ae-150">非同步回呼方法</span><span class="sxs-lookup"><span data-stu-id="e52ae-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



