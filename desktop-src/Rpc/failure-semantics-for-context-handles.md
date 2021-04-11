---
title: 內容控制碼的失敗語義
description: 本主題討論內容控制碼的失敗語義。
ms.assetid: fcf28519-39ad-4823-bc27-f3502e4d540c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4528b3f5160b92a4e6f10dbcf877e9fec59f81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021511"
---
# <a name="failure-semantics-for-context-handles"></a><span data-ttu-id="caf3c-103">內容控制碼的失敗語義</span><span class="sxs-lookup"><span data-stu-id="caf3c-103">Failure Semantics for Context Handles</span></span>

<span data-ttu-id="caf3c-104">本主題討論內容控制碼的失敗語義。</span><span class="sxs-lookup"><span data-stu-id="caf3c-104">This topic discusses failure semantics for context handles.</span></span>

## <a name="failure-semantics-when-closing-the-context-handle-fails"></a><span data-ttu-id="caf3c-105">關閉內容控制碼失敗時的失敗語義</span><span class="sxs-lookup"><span data-stu-id="caf3c-105">Failure Semantics when Closing the Context Handle Fails</span></span>

<span data-ttu-id="caf3c-106">假設用戶端應用程式嘗試關閉在伺服器上開啟的內容控制碼，而不關閉用戶端進程。</span><span class="sxs-lookup"><span data-stu-id="caf3c-106">Imagine a client application is attempting to close a context handle it opened on the server, without shutting down the client process.</span></span> <span data-ttu-id="caf3c-107">此外，假設對伺服器的呼叫關閉內容控制碼失敗 (例如，用戶端記憶體不足) 。</span><span class="sxs-lookup"><span data-stu-id="caf3c-107">Also, assume the call to the server to close the context handle fails (for example, the client is out of memory).</span></span> <span data-ttu-id="caf3c-108">處理這種情況的適當方式是呼叫 [**RpcSsDestroyClientCoNtext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) 函數。</span><span class="sxs-lookup"><span data-stu-id="caf3c-108">The proper way to handle this situation is to call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span> <span data-ttu-id="caf3c-109">在這種情況下，用戶端會清除內容控制碼的側邊，而 abortively 會關閉與伺服器的連接。</span><span class="sxs-lookup"><span data-stu-id="caf3c-109">In such a case the client cleans up its side of the context handle, and abortively closes the connection to the server.</span></span> <span data-ttu-id="caf3c-110">由於連接是真正的連接集區 (請參閱 [RPC 和網路](rpc-and-the-network.md)) （參考計數的參考是針對每個開啟的系結或內容控制碼使用一個參考），藉由呼叫 **RpcSsDestroyClientCoNtext** 函式來終結內容控制碼，並不會實際損毀連接。</span><span class="sxs-lookup"><span data-stu-id="caf3c-110">Since the connection is really a connection pool (see [RPC and the Network](rpc-and-the-network.md)), which is reference-counted with one reference for each opened binding or context handle, destroying the context handle by calling the **RpcSsDestroyClientContext** function does not actually destroy the connection.</span></span> <span data-ttu-id="caf3c-111">相反地，它會遞減連接集區的參考計數。</span><span class="sxs-lookup"><span data-stu-id="caf3c-111">Rather, it decrements the reference count for the connection pool.</span></span> <span data-ttu-id="caf3c-112">針對要關閉的集區中的連接，用戶端必須從用戶端進程關閉該伺服器的所有系結控制碼和內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf3c-112">For connections in the pool to be closed, the client needs to close all binding handles and context handles to that server from the client process.</span></span> <span data-ttu-id="caf3c-113">然後，集區中的所有連接都會關閉，然後啟動並清除伺服器的執行機制。</span><span class="sxs-lookup"><span data-stu-id="caf3c-113">Then all connections in the pool are closed, and the server run-down mechanism is initiated and cleans up.</span></span>

## <a name="failure-semantics-during-change-of-state-of-the-context-handle"></a><span data-ttu-id="caf3c-114">變更內容控制碼狀態期間的失敗語義</span><span class="sxs-lookup"><span data-stu-id="caf3c-114">Failure Semantics During Change of State of the Context Handle</span></span>

<span data-ttu-id="caf3c-115">本節中的資訊是指 Windows XP 和更新版本的平臺。</span><span class="sxs-lookup"><span data-stu-id="caf3c-115">The information in this section refers to Windows XP and later platforms.</span></span>

<span data-ttu-id="caf3c-116">內容控制碼只是函數的參數。</span><span class="sxs-lookup"><span data-stu-id="caf3c-116">Context handles are simply parameters to a function.</span></span> <span data-ttu-id="caf3c-117">當您封送處理或取消封送處理參數時，會發生內容控制碼狀態中的所有變更。</span><span class="sxs-lookup"><span data-stu-id="caf3c-117">All changes in the state of a context handle happen when parameters are marshaled or unmarshaled.</span></span> <span data-ttu-id="caf3c-118">例如，如果用戶端開啟內容控制碼 (將它從 **Null** 變更為非 **Null**) ，則在封送處理引數以傳送至用戶端之前，RPC 執行時間並不會實際開啟控制碼的 RPC 部分。</span><span class="sxs-lookup"><span data-stu-id="caf3c-118">For example, if a client opens a context handle (changes it from **NULL** to non-**NULL**), the RPC run-time does not actually open the RPC portion of the handle until the arguments are marshaled for sending to the client.</span></span> <span data-ttu-id="caf3c-119">可能會在過渡期間發生失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-119">Failures can occur during the interim.</span></span> <span data-ttu-id="caf3c-120">由於有各種可能的網路或資源不足的狀況，將封包傳輸至用戶端可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-120">Due to a variety of possible network or low resource conditions, transmission of the packet to the client could fail.</span></span> <span data-ttu-id="caf3c-121">或者，伺服器常式可能會在嘗試變更內容控制碼時擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="caf3c-121">Or the server routine may throw an exception while attempting to change a context handle.</span></span> <span data-ttu-id="caf3c-122">在這些或其他失敗情況下，用戶端和伺服器可能會取得內容控制碼不一致的觀點。</span><span class="sxs-lookup"><span data-stu-id="caf3c-122">In these or other failure situations, the client and server may get inconsistent views of the context handle.</span></span> <span data-ttu-id="caf3c-123">本節說明內容控制碼狀態的規則，以及在各種失敗狀況期間的用戶端和伺服器程式碼的責任。</span><span class="sxs-lookup"><span data-stu-id="caf3c-123">This section explains the rule for the state of the context handle, and the responsibility of client and server code during various failure conditions.</span></span>

-   <span data-ttu-id="caf3c-124">**Null** 內容控制碼抵達，但伺服器常式遇到失敗並擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="caf3c-124">A **NULL** context handle arrives, but the server routine encounters a failure and throws an exception.</span></span>

    <span data-ttu-id="caf3c-125">伺服器常式負責清除任何可能已建立的內容控制碼相關狀態。</span><span class="sxs-lookup"><span data-stu-id="caf3c-125">It is the responsibility of the server routine to clean up any context handle–related state it may have created.</span></span> <span data-ttu-id="caf3c-126">RPC 執行時間會清除其狀態。</span><span class="sxs-lookup"><span data-stu-id="caf3c-126">The RPC run time cleans up its state.</span></span>

-   <span data-ttu-id="caf3c-127">非 **Null** 的內容控制碼抵達，但伺服器常式遇到失敗並擲回例外狀況。</span><span class="sxs-lookup"><span data-stu-id="caf3c-127">A non-**NULL** context handles arrives, but the server routine encounters a failure and throws an exception.</span></span>

    <span data-ttu-id="caf3c-128">如果伺服器常式關閉了內容控制碼，用戶端就不會知道它，因為呼叫將不會成功;進一步使用內容控制碼會導致用戶端發生 RPC \_ X \_ SS \_ 內容 \_ 不相符的錯誤。</span><span class="sxs-lookup"><span data-stu-id="caf3c-128">If the server routine closed the context handle, the client will not know about it, since the call will not succeed; further use of the context handle will result in an RPC\_X\_SS\_CONTEXT\_MISMATCH error on the client.</span></span> <span data-ttu-id="caf3c-129">如果伺服器常式未修改內容控制碼，用戶端仍然可以使用它。</span><span class="sxs-lookup"><span data-stu-id="caf3c-129">If the server routine does not modify the context handle, the client can still use it.</span></span> <span data-ttu-id="caf3c-130">如果伺服器常式變更儲存在伺服器內容中的資訊，用戶端的新呼叫將會使用該資訊。</span><span class="sxs-lookup"><span data-stu-id="caf3c-130">If the server routine changes the information stored in the server context, new calls from the client will use that information.</span></span>

-   <span data-ttu-id="caf3c-131">非 **Null** 的內容控制碼抵達，且伺服器常式會關閉控制碼，但在封送處理內容控制碼之後，封送處理失敗，或在封送處理失敗之後處理。</span><span class="sxs-lookup"><span data-stu-id="caf3c-131">A non-**NULL** context handle arrives, and the server routine closes the handle, but either marshaling after the context handle was marshaled failed, or processing after marshaling failed.</span></span>

    <span data-ttu-id="caf3c-132">內容控制碼已關閉，而此用戶端使用此內容控制碼進一步呼叫，會導致 \_ \_ 用戶端上發生 RPC X SS \_ 內容不符的 \_ 錯誤。</span><span class="sxs-lookup"><span data-stu-id="caf3c-132">The context handle is closed, and further calls by this client using this context handle result in an RPC\_X\_SS\_CONTEXT\_MISMATCH error on the client.</span></span>

-   <span data-ttu-id="caf3c-133">**Null** 內容控制碼抵達，且伺服器會為此控制碼建立其內容，但在封送處理內容控制碼之後，封送處理失敗，或在封送處理失敗之後處理。</span><span class="sxs-lookup"><span data-stu-id="caf3c-133">A **NULL** context handle arrives, and the server creates its context for this handle, but either marshaling after the context handle was marshaled failed, or processing after marshaling failed.</span></span>

    <span data-ttu-id="caf3c-134">在此情況下，RPC 執行時間會叫用此內容控制碼的執行，並清除此內容控制碼的 RPC 狀態。</span><span class="sxs-lookup"><span data-stu-id="caf3c-134">In this case, the RPC run time invokes the run down for this context handle, and cleans up the RPC state for this context handle.</span></span> <span data-ttu-id="caf3c-135">將不會在用戶端上建立內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf3c-135">The context handle will not be created on the client side.</span></span>

-   <span data-ttu-id="caf3c-136">非 **Null** 的內容控制碼會送達，而且伺服器不會變更內容控制碼，也不會變更儲存在伺服器內容中的資訊，而且在封送處理內容控制碼之後，封送處理會失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-136">A non-**NULL** context handle arrives, and the server either does not change the context handle, or it changes the information stored in the server context, and marshaling fails after the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-137">來自用戶端的新呼叫將會使用伺服器所擁有的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf3c-137">New calls from the client will use the context handle that the server has.</span></span>

-   <span data-ttu-id="caf3c-138">**Null** 內容控制碼會送達，而且伺服器不會將它設定為 **null** 以外的任何值，但是在封送處理內容控制碼之前，呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-138">A **NULL** context handle arrives, and the server does not set it to anything other than **NULL**, but the call fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-139">在此情況下，不會在用戶端上建立任何內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf3c-139">In this case, no context handle is created on the client.</span></span>

-   <span data-ttu-id="caf3c-140">非 **Null** 的內容控制碼會抵達，而伺服器會將它設定為 **Null**，但在封送處理內容控制碼之前，封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-140">A non-**NULL** context handle arrives, and the server sets it to **NULL**, but marshaling fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-141">在此情況下，內容控制碼會在伺服器上保持關閉狀態，而客戶 \_ 端 \_ \_ \_ 會在嘗試使用內容控制碼時取得 RPC X SS 內容不符的錯誤。</span><span class="sxs-lookup"><span data-stu-id="caf3c-141">In this case, the context handle remains closed on the server, and the client gets RPC\_X\_SS\_CONTEXT\_MISMATCH errors when it tries to use the context handle.</span></span>

-   <span data-ttu-id="caf3c-142">**Null** 內容控制碼會抵達伺服器，而伺服器會將它設定為非 **Null**，但是在封送處理內容控制碼之前，封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-142">A **NULL** context handle arrives on the server, and the server sets it to non-**NULL**, but marshaling fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-143">將會叫用內容控制碼，讓伺服器能夠清除，而且不會在用戶端上建立任何內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="caf3c-143">The context handle run down is to be invoked so that the server can clean up, and no context handle will be created on the client.</span></span>

-   <span data-ttu-id="caf3c-144">非 **Null** 的內容控制碼會送達，而且伺服器不會變更內容控制碼，也不會變更儲存在伺服器內容中的資訊，而且在封送處理內容控制碼之前，封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-144">A non-**NULL** context handle arrives, and the server either does not change the context handle, or it changes the information stored in the server context, and marshaling fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-145">來自用戶端的新呼叫將使用伺服器上的狀態。</span><span class="sxs-lookup"><span data-stu-id="caf3c-145">New calls from the client will use the state on the server.</span></span>

-   <span data-ttu-id="caf3c-146">內容控制碼宣告為傳回值，而伺服器常式會針對內容控制碼傳回 **Null** ，而在封送處理內容控制碼之前，封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-146">A context handle is declared as a return value, and the server routine returns **NULL** for the context handle and marshaling fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-147">在此情況下，不會在用戶端上建立新的內容。</span><span class="sxs-lookup"><span data-stu-id="caf3c-147">In this case, no new context is created on the client.</span></span>

-   <span data-ttu-id="caf3c-148">內容控制碼宣告為傳回值，而伺服器常式會針對內容控制碼傳回非 **Null** ，並在封送處理內容控制碼之前，封送處理失敗。</span><span class="sxs-lookup"><span data-stu-id="caf3c-148">A context handle is declared as a return value, and the server routine returns non-**NULL** for the context handle and marshaling fails before the context handle is marshaled.</span></span>

    <span data-ttu-id="caf3c-149">RPC 執行時間會呼叫內容處理常式執行時間，讓它有機會清除，而且用戶端上不會建立新的內容。</span><span class="sxs-lookup"><span data-stu-id="caf3c-149">The RPC run time calls the context handle run-down routine to give it a chance to clean up, and no new context is created on the client.</span></span>

 

 




