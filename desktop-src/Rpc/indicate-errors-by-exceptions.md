---
title: 依例外狀況指出錯誤
description: 針對傳統的 C 程式設計人員，通常會透過傳回值傳回錯誤，或使用會傳回錯誤碼的特殊 out 參數。
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842532"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="8be4d-103">依例外狀況指出錯誤</span><span class="sxs-lookup"><span data-stu-id="8be4d-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="8be4d-104">針對傳統的 C 程式設計人員，通常會透過傳回值傳回錯誤，或使用會傳回錯誤碼的特殊 \[ out \] 參數。</span><span class="sxs-lookup"><span data-stu-id="8be4d-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="8be4d-105">這會導致介面實作為下列方法：</span><span class="sxs-lookup"><span data-stu-id="8be4d-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="8be4d-106">這種方法的問題在於，RPC 傳回值只是長整數。</span><span class="sxs-lookup"><span data-stu-id="8be4d-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="8be4d-107">它們沒有任何特殊意義的錯誤 (請注意， [**錯誤 \_ 狀態 \_ t**](/windows/desktop/Midl/error-status-t) 在伺服器) 端沒有特殊的語法，這會帶來重要的影響。</span><span class="sxs-lookup"><span data-stu-id="8be4d-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="8be4d-108">首先，RPC 不會收到作業失敗的警示;它會嘗試 unmarshal 所有 \[ in、out \] 和 \[ out \] 引數。</span><span class="sxs-lookup"><span data-stu-id="8be4d-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="8be4d-109">內容控制碼的失敗語義也不同。</span><span class="sxs-lookup"><span data-stu-id="8be4d-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="8be4d-110">傳回給用戶端的封包基本上是成功封包，且錯誤碼在封包中是深深的。</span><span class="sxs-lookup"><span data-stu-id="8be4d-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="8be4d-111">這也表示 RPC 不會使用延伸的錯誤資訊，因此用戶端軟體通常無法分辨呼叫失敗的位置。</span><span class="sxs-lookup"><span data-stu-id="8be4d-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="8be4d-112">藉由擲回結構化例外狀況處理 (SEH) 例外狀況 (非 c + +) 是更好的方法，來指出 RPC 伺服器常式中的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8be4d-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="8be4d-113">擲回 SEH 例外狀況時，控制項會直接進入 RPC 執行時間。</span><span class="sxs-lookup"><span data-stu-id="8be4d-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="8be4d-114">有時，在無法正常清除的常式中，有時會發生錯誤，而且需要對其呼叫端表示錯誤。</span><span class="sxs-lookup"><span data-stu-id="8be4d-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="8be4d-115">常式應該會將錯誤傳回給它的呼叫者，然後它會將錯誤傳回給其呼叫端等等。</span><span class="sxs-lookup"><span data-stu-id="8be4d-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="8be4d-116">不過，堆疊上的最後一個伺服器常式應該在它回到 RPC 之前擲回例外狀況，以向 RPC 指出發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8be4d-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8be4d-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="8be4d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8be4d-118">例外狀況處理</span><span class="sxs-lookup"><span data-stu-id="8be4d-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 