---
description: 電話語音的互動式本質需要 TAPI 成為即時操作環境。
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: 同步/非同步模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981567"
---
# <a name="synchronousasynchronous-model"></a><span data-ttu-id="9f312-103">同步/非同步模型</span><span class="sxs-lookup"><span data-stu-id="9f312-103">Synchronous/Asynchronous Model</span></span>

<span data-ttu-id="9f312-104">電話語音的互動式本質需要 TAPI 成為即時操作環境。</span><span class="sxs-lookup"><span data-stu-id="9f312-104">The interactive nature of telephony requires TAPI to be a real-time operating environment.</span></span> <span data-ttu-id="9f312-105">需要許多 TAPI 功能才能快速完成，並以同步方式將其結果傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f312-105">Many of the TAPI functions are required to complete quickly and return their results to the application synchronously.</span></span> <span data-ttu-id="9f312-106">其他函式 (例如撥號) 可能無法快速完成，因此會以非同步方式運作。</span><span class="sxs-lookup"><span data-stu-id="9f312-106">Other functions (such as dialing) may not be able to complete as quickly and therefore operate asynchronously.</span></span>

<span data-ttu-id="9f312-107">電話語音作業會以同步或非同步方式完成。</span><span class="sxs-lookup"><span data-stu-id="9f312-107">Telephony operations complete either synchronously or asynchronously.</span></span> <span data-ttu-id="9f312-108">這兩個模型的差異如下所示。</span><span class="sxs-lookup"><span data-stu-id="9f312-108">These two models differ as follows.</span></span> <span data-ttu-id="9f312-109">*同步* 函式會先執行整個要求，呼叫端的執行緒才能從函式呼叫傳回。</span><span class="sxs-lookup"><span data-stu-id="9f312-109">*Synchronous functions* execute the entire request before the caller's thread is allowed to return from the function call.</span></span> <span data-ttu-id="9f312-110">*非同步* 函式會在要求完整執行之前傳回。</span><span class="sxs-lookup"><span data-stu-id="9f312-110">*Asynchronous functions* return before the request has executed in its entirety.</span></span> <span data-ttu-id="9f312-111">當非同步要求稍後完成時，服務提供者會藉由呼叫 TAPI 最初在初始化順序中提供給它的回呼程式來報告完成。</span><span class="sxs-lookup"><span data-stu-id="9f312-111">When the asynchronous request later completes, the service provider reports the completion by calling a callback procedure that TAPI originally supplied to it early in the initialization sequence.</span></span>

-   <span data-ttu-id="9f312-112">非同步作業有一個名為 *dwRequestID* 的參數，其定義的類型 [winspool.drv \_ REQUESTID](./drv-requestid.md) 作為其第一個參數。</span><span class="sxs-lookup"><span data-stu-id="9f312-112">Asynchronous operations have a parameter named *dwRequestID* of the defined type [DRV\_REQUESTID](./drv-requestid.md) as their first parameter.</span></span> <span data-ttu-id="9f312-113">這類作業會在函式呼叫中執行其處理的一部分，並在函式呼叫傳回之後，于獨立的執行執行緒中執行其處理的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="9f312-113">Such an operation performs part of its processing in the function call and the remainder of its processing in an independent execution thread after the function call has returned.</span></span> <span data-ttu-id="9f312-114">當函式傳回時，它會傳回負錯誤結果或在函式呼叫中傳遞的 (正) *dwRequestID* 。</span><span class="sxs-lookup"><span data-stu-id="9f312-114">When the function returns, it returns either a negative error result or the (positive) *dwRequestID* that was passed in the function call.</span></span> <span data-ttu-id="9f312-115">負誤差結果表示作業已完成 (且) 失敗。</span><span class="sxs-lookup"><span data-stu-id="9f312-115">The negative error result indicates that the operation is complete (and failed).</span></span> <span data-ttu-id="9f312-116">傳回的正面 *dwRequestID* 表示作業會繼續在獨立執行緒中執行。</span><span class="sxs-lookup"><span data-stu-id="9f312-116">The positive *dwRequestID* returned indicates that the operation continues in the independent thread.</span></span> <span data-ttu-id="9f312-117">在這種情況下，服務提供者最後會呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 程式，並傳遞 *dwRequestID* 和結果碼來指出作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9f312-117">In such a case, the service provider eventually calls the [**ASYNC\_COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) procedure, passing the *dwRequestID* and a result code to indicate the outcome of the operation.</span></span> <span data-ttu-id="9f312-118">結果碼為零表示成功，或一組相同的 (負) 錯誤結果。</span><span class="sxs-lookup"><span data-stu-id="9f312-118">The result code is zero for success or one of the same set of (negative) error results.</span></span> <span data-ttu-id="9f312-119">在任何情況下，服務提供者絕不能從指定為非同步函式傳回零或 *dwRequestID* 以外的任何正值，因為這樣做可能會產生非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="9f312-119">In any case, the service provider must never return zero or any positive value other than *dwRequestID* from a function designated as asynchronous because doing so can produce unexpected results.</span></span> <span data-ttu-id="9f312-120">服務提供者應該一律將輸入資料從應用程式記憶體複製到服務提供者記憶體中，然後再從非同步函式傳回。</span><span class="sxs-lookup"><span data-stu-id="9f312-120">Service providers should always copy input data from application memory into service provider memory before returning from an asynchronous function.</span></span>
-   <span data-ttu-id="9f312-121">同步作業沒有 *dwRequestID* 作為其第一個參數。</span><span class="sxs-lookup"><span data-stu-id="9f312-121">Synchronous operations do not have *dwRequestID* as their first parameter.</span></span> <span data-ttu-id="9f312-122">這類作業會在呼叫端的執行執行緒中執行其所有處理，並在傳回時傳回最終結果。</span><span class="sxs-lookup"><span data-stu-id="9f312-122">Such an operation performs all of its processing in the caller's execution thread, returning the final result when it returns.</span></span> <span data-ttu-id="9f312-123">結果為零表示成功或負錯誤碼（失敗）。</span><span class="sxs-lookup"><span data-stu-id="9f312-123">The result is zero for success or a negative error code for failure.</span></span> <span data-ttu-id="9f312-124">服務提供者不會針對同步作業呼叫 [**非同步 \_ 完成**](/windows/win32/api/tspi/nc-tspi-async_completion) 。</span><span class="sxs-lookup"><span data-stu-id="9f312-124">The service provider does not call [**ASYNC\_COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) for synchronous operations.</span></span>

<span data-ttu-id="9f312-125">請特別注意，相對於原始要求傳回時的「完成」回呼的時機。</span><span class="sxs-lookup"><span data-stu-id="9f312-125">It is interesting to consider the timing of a "completion" callback relative to when the original request returns.</span></span> <span data-ttu-id="9f312-126">一般的非同步要求會由服務提供者所執行，如下列虛擬程式碼所示：</span><span class="sxs-lookup"><span data-stu-id="9f312-126">A typical asynchronous request would be implemented by the service provider as in the following pseudocode:</span></span>

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

<span data-ttu-id="9f312-127">如果作業順利完成 (或原始要求傳回非常緩慢的) ，則可能會在原始要求回到應用程式之前或甚至是 TAPI 之前，觸發在實體作業完成時執行的中斷處理常式。</span><span class="sxs-lookup"><span data-stu-id="9f312-127">If the operation completes very rapidly (or the original request returns very slowly), it is possible that the interrupt handler that runs when a physical operation completes may be triggered before the original request returns to the application or even to TAPI.</span></span> <span data-ttu-id="9f312-128">這是允許的行為。</span><span class="sxs-lookup"><span data-stu-id="9f312-128">This behavior is allowed.</span></span> <span data-ttu-id="9f312-129">TAPI 保證應用程式的最終完成通知會在原始要求傳回之後傳遞。</span><span class="sxs-lookup"><span data-stu-id="9f312-129">TAPI guarantees that the eventual completion notification to the application is delivered after the original request returns.</span></span>

<span data-ttu-id="9f312-130">**TAPI 2.x：** 列出每個函式是以同步方式完成或以非同步方式出現在 [TAPI 快速函數參考](./tapi-quick-function-reference.md)中的狀態。</span><span class="sxs-lookup"><span data-stu-id="9f312-130">**TAPI 2.x:** Lists which state whether each function completes synchronously or asynchronously appear in [TAPI Quick Function Reference](./tapi-quick-function-reference.md).</span></span>

 

 
