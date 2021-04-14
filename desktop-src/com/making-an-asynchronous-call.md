---
title: 進行非同步呼叫
description: 進行同步呼叫的程式很簡單，用戶端會在伺服器物件上取得介面指標，並透過該指標呼叫方法。 非同步呼叫涉及 call 物件，因此它包含幾個步驟。
ms.assetid: ab65d38d-836a-48d4-87c1-8812cbc8ff92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22dcd7a6509cd07e12357a96222baa04f9e4c942
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382997"
---
# <a name="making-an-asynchronous-call"></a><span data-ttu-id="15dc6-104">進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="15dc6-104">Making an Asynchronous Call</span></span>

<span data-ttu-id="15dc6-105">進行同步呼叫的程式很簡單：用戶端會取得伺服器物件上的介面指標，並透過該指標呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-105">The procedure for making a synchronous call is straightforward: The client obtains an interface pointer on the server object and calls methods through that pointer.</span></span> <span data-ttu-id="15dc6-106">非同步呼叫涉及 call 物件，因此它包含幾個步驟。</span><span class="sxs-lookup"><span data-stu-id="15dc6-106">Asynchronous calling involves a call object, so it involves a few more steps.</span></span>

<span data-ttu-id="15dc6-107">針對同步介面上的每個方法，對應的非同步介面會執行兩個方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-107">For each method on a synchronous interface, the corresponding asynchronous interface implements two methods.</span></span> <span data-ttu-id="15dc6-108">這些方法會將開頭和結尾的前置詞附加 \_ \_ 至同步方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="15dc6-108">These methods attach the prefixes Begin\_ and Finish\_ to the name of the synchronous method.</span></span> <span data-ttu-id="15dc6-109">例如，如果名為 ISimpleStream 的介面有 Read 方法，AsyncISimpleStream 介面將會有開始 \_ 讀取和完成 \_ 讀取方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-109">For example, if an interface named ISimpleStream has a Read method, the AsyncISimpleStream interface will have a Begin\_Read and a Finish\_Read method.</span></span> <span data-ttu-id="15dc6-110">若要開始非同步呼叫，用戶端會呼叫 Begin \_ 方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-110">To begin an asynchronous call, the client calls the Begin\_ method.</span></span>

<span data-ttu-id="15dc6-111">**開始非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="15dc6-111">**To begin an asynchronous call**</span></span>

1.  <span data-ttu-id="15dc6-112">查詢 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) 介面的伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="15dc6-112">Query the server object for the [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory) interface.</span></span> <span data-ttu-id="15dc6-113">如果 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 傳回 E \_ NOINTERFACE，則伺服器物件不支援非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc6-113">If [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) returns E\_NOINTERFACE, the server object does not support asynchronous calling.</span></span>

2.  <span data-ttu-id="15dc6-114">呼叫 [**ICallFactory：： CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) 來建立對應至所需介面的呼叫物件，然後將指標釋放至 [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory)。</span><span class="sxs-lookup"><span data-stu-id="15dc6-114">Call [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) to create a call object corresponding to the interface you want, and then release the pointer to [**ICallFactory**](/windows/win32/api/objidlbase/nn-objidlbase-icallfactory).</span></span>

3.  <span data-ttu-id="15dc6-115">如果您未要求呼叫 [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall)的非同步介面指標，請查詢非同步介面的呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="15dc6-115">If you did not request a pointer to the asynchronous interface from the call to [**CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall), query the call object for the asynchronous interface.</span></span>

4.  <span data-ttu-id="15dc6-116">呼叫適當的 Begin \_ 方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-116">Call the appropriate Begin\_ method.</span></span>

<span data-ttu-id="15dc6-117">伺服器物件現在正在處理非同步呼叫，用戶端可以自由地執行其他工作，直到需要呼叫的結果為止。</span><span class="sxs-lookup"><span data-stu-id="15dc6-117">The server object is now processing the asynchronous call, and the client is free to do other work until it needs the results of the call.</span></span>

<span data-ttu-id="15dc6-118">呼叫物件一次只能處理一個非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc6-118">A call object can process only one asynchronous call at a time.</span></span> <span data-ttu-id="15dc6-119">如果相同或第二個用戶端在 \_ 暫止的非同步呼叫完成之前呼叫 Begin 方法，begin \_ 方法會傳回「RPC \_ E \_ 呼叫擱置」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="15dc6-119">If the same or a second client calls a Begin\_ method before a pending asynchronous call is finished, the Begin\_ method will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="15dc6-120">如果用戶端不需要 Begin 方法的結果 \_ ，它可以在此程式的結尾釋放呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="15dc6-120">If the client does not need the results of the Begin\_ method, it can release the call object at the end of this procedure.</span></span> <span data-ttu-id="15dc6-121">COM 會偵測此狀況，並清除呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc6-121">COM detects this condition and cleans up the call.</span></span> <span data-ttu-id="15dc6-122">\_不會呼叫 Finish 方法，用戶端也不會取得任何 out 參數或傳回值。</span><span class="sxs-lookup"><span data-stu-id="15dc6-122">The Finish\_ method is not called, and the client does not get any out parameters or a return value.</span></span>

<span data-ttu-id="15dc6-123">當伺服器物件已準備好從 Begin 方法傳回時 \_ ，它會對呼叫物件發出信號，表示它已完成。</span><span class="sxs-lookup"><span data-stu-id="15dc6-123">When the server object is ready to return from the Begin\_ method, it signals the call object that it is done.</span></span> <span data-ttu-id="15dc6-124">當用戶端就緒時，它會檢查呼叫物件是否已收到信號。</span><span class="sxs-lookup"><span data-stu-id="15dc6-124">When the client is ready, it checks to see whether the call object has been signaled.</span></span> <span data-ttu-id="15dc6-125">如果是，用戶端可以完成非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc6-125">If so, the client can complete the asynchronous call.</span></span>

<span data-ttu-id="15dc6-126">在用戶端與伺服器之間進行此信號和檢查的機制是呼叫物件上的 [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) 介面。</span><span class="sxs-lookup"><span data-stu-id="15dc6-126">The mechanism for this signaling and checking between client and server is the [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) interface on the call object.</span></span> <span data-ttu-id="15dc6-127">呼叫物件通常會藉由匯總系統提供的同步處理物件來執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="15dc6-127">The call object normally implements this interface by aggregating a system-supplied synchronization object.</span></span> <span data-ttu-id="15dc6-128">同步處理物件會包裝事件控制碼，而伺服器會 \_ 呼叫 [**ISynchronize：：信號**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal)，就會在從 Begin 方法傳回之前發出信號。</span><span class="sxs-lookup"><span data-stu-id="15dc6-128">The synchronization object wraps an event handle, which the server signals just before returning from the Begin\_ method by calling [**ISynchronize::Signal**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-signal).</span></span>

<span data-ttu-id="15dc6-129">**完成非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="15dc6-129">**To complete an asynchronous call**</span></span>

1.  <span data-ttu-id="15dc6-130">查詢 [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) 介面的呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="15dc6-130">Query the call object for the [**ISynchronize**](/windows/win32/api/objidlbase/nn-objidlbase-isynchronize) interface.</span></span>

2.  <span data-ttu-id="15dc6-131">呼叫 [**ISynchronize：： Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait)。</span><span class="sxs-lookup"><span data-stu-id="15dc6-131">Call [**ISynchronize::Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait).</span></span>

3.  <span data-ttu-id="15dc6-132">如果 [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) 傳回 RPC \_ E \_ TIMEOUT，則 Begin \_ 方法未完成處理。</span><span class="sxs-lookup"><span data-stu-id="15dc6-132">If [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) returns RPC\_E\_TIMEOUT, the Begin\_ method is not finished processing.</span></span> <span data-ttu-id="15dc6-133">用戶端可以繼續執行其他工作，稍後再呼叫 **等候** 。</span><span class="sxs-lookup"><span data-stu-id="15dc6-133">The client can continue with other work and call **Wait** again later.</span></span> <span data-ttu-id="15dc6-134">它無法呼叫完成 \_ 方法，直到 **等候** 返回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="15dc6-134">It cannot call the Finish\_ method until **Wait** returns S\_OK.</span></span>

    <span data-ttu-id="15dc6-135">如果 [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) 傳回 S \_ OK，就會 \_ 傳回 Begin 方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-135">If [**Wait**](/windows/win32/api/objidlbase/nf-objidlbase-isynchronize-wait) returns S\_OK, the Begin\_ method has returned.</span></span> <span data-ttu-id="15dc6-136">呼叫適當的完成 \_ 方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-136">Call the appropriate Finish\_ method.</span></span>

<span data-ttu-id="15dc6-137">完成方法會將 \_ 任何 out 參數傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="15dc6-137">The Finish\_ method passes the client any out parameters.</span></span> <span data-ttu-id="15dc6-138">非同步方法的行為（包括完成方法的傳回值 \_ ）應該完全符合對應的同步方法。</span><span class="sxs-lookup"><span data-stu-id="15dc6-138">The behavior of the asynchronous methods, including the return value of the Finish\_ method, should match exactly that of the corresponding synchronous method.</span></span>

<span data-ttu-id="15dc6-139">當完成方法傳回時，用戶端就可以釋出呼叫物件 \_ ，也可以保留呼叫物件的指標以進行其他呼叫。</span><span class="sxs-lookup"><span data-stu-id="15dc6-139">The client can release the call object as soon as the Finish\_ method returns, or it can hold a pointer to the call object to make additional calls.</span></span> <span data-ttu-id="15dc6-140">無論是哪一種情況，當不再需要物件時，用戶端都會負責釋放呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="15dc6-140">In either case, the client is responsible for releasing the call object when the object is no longer needed.</span></span>

<span data-ttu-id="15dc6-141">如果您在 \_ 沒有任何呼叫進行時呼叫 COMPLETE 方法，則方法會傳回 RPC \_ E \_ 呼叫 \_ 完成。</span><span class="sxs-lookup"><span data-stu-id="15dc6-141">If you call a Finish\_ method when no call is in progress, the method will return RPC\_E\_CALL\_COMPLETE.</span></span>

> [!Note]  
> <span data-ttu-id="15dc6-142">如果用戶端和伺服器物件位於相同的單元中，則不保證對 [**ICallFactory：： CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) 的呼叫會成功。</span><span class="sxs-lookup"><span data-stu-id="15dc6-142">If the client and server objects are in the same apartment, calls to [**ICallFactory::CreateCall**](/windows/win32/api/objidlbase/nf-objidlbase-icallfactory-createcall) are not guaranteed to succeed.</span></span> <span data-ttu-id="15dc6-143">如果伺服器物件不支援對特定介面進行非同步呼叫，則嘗試建立呼叫物件將會失敗，而且用戶端必須使用同步介面。</span><span class="sxs-lookup"><span data-stu-id="15dc6-143">If the server object does not support asynchronous calling on a particular interface, the attempt to create a call object will fail and the client must use the synchronous interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="15dc6-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="15dc6-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15dc6-145">取消非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="15dc6-145">Canceling an Asynchronous Call</span></span>](canceling-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="15dc6-146">非同步呼叫期間的用戶端安全性</span><span class="sxs-lookup"><span data-stu-id="15dc6-146">Client Security During an Asynchronous Call</span></span>](client-security-during-an-asynchronous-call.md)
</dt> <dt>

[<span data-ttu-id="15dc6-147">模擬和非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="15dc6-147">Impersonation and Asynchronous Calls</span></span>](impersonation-and-asynchronous-calls.md)
</dt> </dl>

 

 