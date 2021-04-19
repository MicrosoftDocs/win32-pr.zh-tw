---
description: ThreadProc 方法會從佇列中取出範例，並將其傳遞至輸入釘選。
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: 'COutputQueue. ThreadProc 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988260"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="1eb2c-103">COutputQueue. ThreadProc 方法</span><span class="sxs-lookup"><span data-stu-id="1eb2c-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="1eb2c-104">`ThreadProc`方法會從佇列中取出範例，並將其傳遞至輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eb2c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1eb2c-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="1eb2c-106">參數</span><span class="sxs-lookup"><span data-stu-id="1eb2c-106">Parameters</span></span>

<span data-ttu-id="1eb2c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1eb2c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="1eb2c-108">Return value</span></span>

<span data-ttu-id="1eb2c-109">傳回零。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb2c-110">備註</span><span class="sxs-lookup"><span data-stu-id="1eb2c-110">Remarks</span></span>

<span data-ttu-id="1eb2c-111">[**COutputQueue：： InitialThreadProc**](coutputqueue-initialthreadproc.md)方法會呼叫這個方法，它會執行主執行緒迴圈。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="1eb2c-112">在迴圈中，此方法會執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="1eb2c-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="1eb2c-113">抓取佇列的範例。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="1eb2c-114">如果範例是控制訊息，執行緒就會執行控制項動作。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="1eb2c-115">否則，它會將範例放入 [**COutputQueue：： m \_ ppSamples**](coutputqueue-m-ppsamples.md) 陣列中。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="1eb2c-116">當陣列已滿 (或 [**COutputQueue：： m \_ BBatchExact**](coutputqueue-m-bbatchexact.md) 為 **FALSE**) 時，執行緒會呼叫 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法來傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="1eb2c-117">如果未將任何範例排入佇列，執行緒就會等待 [**COutputQueue：： m \_ hSem**](coutputqueue-m-hsem.md) 信號。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="1eb2c-118">當 [**COutputQueue：： m \_ bTerminate**](coutputqueue-m-bterminate.md) 成員變數變成 **TRUE** 時，執行緒就會終止。</span><span class="sxs-lookup"><span data-stu-id="1eb2c-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eb2c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eb2c-119">Requirements</span></span>



| <span data-ttu-id="1eb2c-120">需求</span><span class="sxs-lookup"><span data-stu-id="1eb2c-120">Requirement</span></span> | <span data-ttu-id="1eb2c-121">值</span><span class="sxs-lookup"><span data-stu-id="1eb2c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb2c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="1eb2c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1eb2c-123"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1eb2c-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1eb2c-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="1eb2c-124">Library</span></span><br/> | <dl> <span data-ttu-id="1eb2c-125"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1eb2c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb2c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eb2c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb2c-127">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="1eb2c-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




