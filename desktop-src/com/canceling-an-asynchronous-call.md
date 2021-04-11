---
title: 取消非同步呼叫
description: 如果呼叫物件實 ICancelMethodCalls 介面，用戶端可以取消正在進行中的非同步呼叫。
ms.assetid: 30a162f2-ce16-4ee6-8002-59216ac0e59a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775b187f1abd3fca43ba907d92f6eabd926e4608
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093383"
---
# <a name="canceling-an-asynchronous-call"></a><span data-ttu-id="bc63e-103">取消非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="bc63e-103">Canceling an Asynchronous Call</span></span>

<span data-ttu-id="bc63e-104">如果呼叫物件實 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) 介面，用戶端可以取消正在進行中的非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc63e-104">A client can cancel an asynchronous call that is in progress if the call object implements the [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls) interface.</span></span> <span data-ttu-id="bc63e-105">針對使用標準封送處理的物件， **ICancelMethodCalls** 一律可用於封送處理呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc63e-105">For objects that use standard marshaling, **ICancelMethodCalls** is always available for marshaled calls.</span></span> <span data-ttu-id="bc63e-106">針對使用自訂封送處理的物件，或對相同單元內的伺服器物件進行呼叫的物件，只有在呼叫物件執行 **ICancelMethodCalls** 時，才能使用此功能。</span><span class="sxs-lookup"><span data-stu-id="bc63e-106">For objects that use custom marshaling or for calls to server objects within the same apartment, this functionality is available only if the call object implements **ICancelMethodCalls**.</span></span>

<span data-ttu-id="bc63e-107">用戶端可以隨時取消呼叫，從 \_ 呼叫 Begin 方法到完成方法傳回為止 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc63e-107">The client can cancel the call at any time, from when the Begin\_ method is called until the Finish\_ method returns.</span></span> <span data-ttu-id="bc63e-108">如果用戶端在呼叫完成方法之前取消呼叫 \_ ，則必須呼叫完成 \_ 方法來清除呼叫物件的狀態。</span><span class="sxs-lookup"><span data-stu-id="bc63e-108">If the client cancels the call before calling the Finish\_ method, it must call the Finish\_ method to clean up the state of the call object.</span></span> <span data-ttu-id="bc63e-109">在用戶端完成之前，呼叫物件上任何 Begin 方法的任何呼叫 \_ 都會傳回 \_ 擱置中的 RPC E \_ 呼叫 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bc63e-109">Until the client has done so, any calls to any Begin\_ method on the call object will return RPC\_E\_CALL\_PENDING.</span></span>

<span data-ttu-id="bc63e-110">**取消非同步呼叫**</span><span class="sxs-lookup"><span data-stu-id="bc63e-110">**To cancel an asynchronous call**</span></span>

1.  <span data-ttu-id="bc63e-111">查詢 [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls)的呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="bc63e-111">Query the call object for [**ICancelMethodCalls**](/windows/win32/api/objidlbase/nn-objidlbase-icancelmethodcalls).</span></span>

2.  <span data-ttu-id="bc63e-112">呼叫 [**ICancelMethodCalls：： Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel)，然後呼叫 [**release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 以釋放步驟1中 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫所取得的指標。</span><span class="sxs-lookup"><span data-stu-id="bc63e-112">Call [**ICancelMethodCalls::Cancel**](/windows/win32/api/objidlbase/nf-objidlbase-icancelmethodcalls-cancel), and then call [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) to release the pointer obtained by the [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) call in step 1.</span></span>

3.  <span data-ttu-id="bc63e-113">如果用戶端尚未 \_ 呼叫完成方法，請立即呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc63e-113">If the client has not called the Finish\_ method already, call it now.</span></span>

<span data-ttu-id="bc63e-114">不保證伺服器實際上已停止執行呼叫。</span><span class="sxs-lookup"><span data-stu-id="bc63e-114">There is no guarantee that the server actually stopped execution of the call.</span></span> <span data-ttu-id="bc63e-115">如果用戶端的進一步工作取決於呼叫可能或未變更的某些伺服器狀態，用戶端應該在繼續之前判斷該狀態。</span><span class="sxs-lookup"><span data-stu-id="bc63e-115">If the client's further work depends on some server state that the call may or may not have changed, the client should determine that state before proceeding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc63e-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc63e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc63e-117">進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="bc63e-117">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 