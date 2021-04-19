---
description: 函式方法。
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: 'COutputQueue. COutputQueue (Outputq. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987857"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="77f34-103">COutputQueue. COutputQueue 函數</span><span class="sxs-lookup"><span data-stu-id="77f34-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="77f34-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="77f34-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="77f34-105">語法</span><span class="sxs-lookup"><span data-stu-id="77f34-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="77f34-106">參數</span><span class="sxs-lookup"><span data-stu-id="77f34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77f34-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="77f34-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-108">輸入釘選的 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="77f34-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="77f34-109">物件將會傳遞範例給此 pin。</span><span class="sxs-lookup"><span data-stu-id="77f34-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="77f34-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-111">**HRESULT** 傳回碼的指標。</span><span class="sxs-lookup"><span data-stu-id="77f34-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="77f34-112">呼叫這個方法之前，請先將值設定為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="77f34-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="77f34-113">傳回時， *phr* 會收到指出方法成功或失敗的值。</span><span class="sxs-lookup"><span data-stu-id="77f34-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="77f34-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-115">旗標，指定物件是否決定建立佇列的時機。</span><span class="sxs-lookup"><span data-stu-id="77f34-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="77f34-116">若 **為 TRUE**，則只有在輸入釘選可能封鎖時，物件才會建立佇列。</span><span class="sxs-lookup"><span data-stu-id="77f34-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="77f34-117">如果為 **FALSE**，則 *bQueue* 參數會指定是否要建立佇列。</span><span class="sxs-lookup"><span data-stu-id="77f34-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="77f34-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-119">如果 *bAuto* 為 **TRUE**，則會忽略此參數。</span><span class="sxs-lookup"><span data-stu-id="77f34-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="77f34-120">如果 *bAuto* 為 **FALSE**，此旗標會指定是否要建立佇列。</span><span class="sxs-lookup"><span data-stu-id="77f34-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="77f34-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-122">要在一個批次中傳遞的最大樣本數。</span><span class="sxs-lookup"><span data-stu-id="77f34-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="77f34-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-124">指定是否使用精確批次大小的旗標。</span><span class="sxs-lookup"><span data-stu-id="77f34-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="77f34-125">若 **為 TRUE**，則物件會等待 *lBatchSize* 範例，再將它們傳遞給輸入釘選。</span><span class="sxs-lookup"><span data-stu-id="77f34-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="77f34-126">如果 **為 FALSE**，則物件會在接收時傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="77f34-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="77f34-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-128">佇列的快取大小。</span><span class="sxs-lookup"><span data-stu-id="77f34-128">Cache size for the queue.</span></span> <span data-ttu-id="77f34-129">預設值為 DEFAULTCACHE 是針對 [**CBaseList**](cbaselist.md) 類別定義的常數。</span><span class="sxs-lookup"><span data-stu-id="77f34-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="77f34-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="77f34-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="77f34-131">傳遞範例之執行緒的優先順序。</span><span class="sxs-lookup"><span data-stu-id="77f34-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77f34-132">備註</span><span class="sxs-lookup"><span data-stu-id="77f34-132">Remarks</span></span>

<span data-ttu-id="77f34-133">如果 *bAuto* 為 **TRUE**，則物件會呼叫下游釘選上的 [**IMemInputPin：： ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) 方法。</span><span class="sxs-lookup"><span data-stu-id="77f34-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="77f34-134">如果 **ReceiveCanBlock** 傳回 S \_ OK (表示 pin 可能會在 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)) 呼叫上封鎖，則物件會建立傳遞範例的執行緒。</span><span class="sxs-lookup"><span data-stu-id="77f34-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="77f34-135">否則，它不會建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="77f34-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="77f34-136">如果 *bAuto* 為 **FALSE**，則 *bQueue* 的值會決定是否要建立執行緒。</span><span class="sxs-lookup"><span data-stu-id="77f34-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="77f34-137">如果物件建立執行緒，則會將執行緒控制碼指派給 [**COutputQueue：： m \_ hThread**](coutputqueue-m-hthread.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="77f34-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="77f34-138">執行緒程式是 [**COutputQueue：： InitialThreadProc**](coutputqueue-initialthreadproc.md)，執行緒參數是指向這個的指標。</span><span class="sxs-lookup"><span data-stu-id="77f34-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="77f34-139">物件也會建立用來保存範例的佇列，這是由 [**COutputQueue：： m \_ List**](coutputqueue-m-list.md) 成員變數提供。</span><span class="sxs-lookup"><span data-stu-id="77f34-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="77f34-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="77f34-140">Requirements</span></span>



| <span data-ttu-id="77f34-141">需求</span><span class="sxs-lookup"><span data-stu-id="77f34-141">Requirement</span></span> | <span data-ttu-id="77f34-142">值</span><span class="sxs-lookup"><span data-stu-id="77f34-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77f34-143">標頭</span><span class="sxs-lookup"><span data-stu-id="77f34-143">Header</span></span><br/>  | <dl> <span data-ttu-id="77f34-144"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="77f34-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77f34-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="77f34-145">Library</span></span><br/> | <dl> <span data-ttu-id="77f34-146"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="77f34-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77f34-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77f34-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77f34-148">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="77f34-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




