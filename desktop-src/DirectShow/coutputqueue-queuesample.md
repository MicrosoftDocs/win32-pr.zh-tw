---
description: QueueSample 方法會將範例排在佇列中。
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: 'COutputQueue. QueueSample 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8efe0ec3b2326d1af0d0075770bdc6443ab9dcad
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910066"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="5b1cd-103">COutputQueue. QueueSample 方法</span><span class="sxs-lookup"><span data-stu-id="5b1cd-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="5b1cd-104">方法會將 `QueueSample` 範例排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b1cd-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b1cd-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="5b1cd-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b1cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b1cd-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="5b1cd-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5b1cd-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b1cd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b1cd-109">Return value</span></span>

<span data-ttu-id="5b1cd-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b1cd-111">備註</span><span class="sxs-lookup"><span data-stu-id="5b1cd-111">Remarks</span></span>

<span data-ttu-id="5b1cd-112">這個方法會將範例新增至佇列的結尾。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="5b1cd-113">在呼叫這個方法之前，請先保存重要區段，並只在物件使用執行緒來傳遞範例時呼叫它。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="5b1cd-114">若要判斷物件是否使用執行緒，請呼叫 [**COutputQueue：： IsQueued**](coutputqueue-isqueued.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="5b1cd-115">這個方法也可以用來將控制訊息放到佇列上。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="5b1cd-116">控制訊息是已定義的常數 (轉換成長的 \_ PTR 型別) ，指示執行緒執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="5b1cd-117">**COutputQueue** 類別會定義下表中顯示的控制訊息。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



| <span data-ttu-id="5b1cd-118">標籤</span><span class="sxs-lookup"><span data-stu-id="5b1cd-118">Label</span></span> | <span data-ttu-id="5b1cd-119">值</span><span class="sxs-lookup"><span data-stu-id="5b1cd-119">Value</span></span> |
|---------------|----------------------------------------|
| <span data-ttu-id="5b1cd-120">訊息</span><span class="sxs-lookup"><span data-stu-id="5b1cd-120">Message</span></span>       | <span data-ttu-id="5b1cd-121">動作</span><span class="sxs-lookup"><span data-stu-id="5b1cd-121">Action</span></span>                                 |
| <span data-ttu-id="5b1cd-122">EOS 封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="5b1cd-122">EOS\_PACKET</span></span>   | <span data-ttu-id="5b1cd-123">傳遞資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-123">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="5b1cd-124">新 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="5b1cd-124">NEW\_SEGMENT</span></span>  | <span data-ttu-id="5b1cd-125">傳遞新的區段。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-125">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="5b1cd-126">重設封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="5b1cd-126">RESET\_PACKET</span></span> | <span data-ttu-id="5b1cd-127">重設佇列的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-127">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="5b1cd-128">傳送封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="5b1cd-128">SEND\_PACKET</span></span>  | <span data-ttu-id="5b1cd-129">傳送部分範例的批次。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-129">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="5b1cd-130">這是 **COutputQueue** 類別在內部使用的受保護方法。</span><span class="sxs-lookup"><span data-stu-id="5b1cd-130">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b1cd-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b1cd-131">Requirements</span></span>



| <span data-ttu-id="5b1cd-132">需求</span><span class="sxs-lookup"><span data-stu-id="5b1cd-132">Requirement</span></span> | <span data-ttu-id="5b1cd-133">值</span><span class="sxs-lookup"><span data-stu-id="5b1cd-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b1cd-134">標頭</span><span class="sxs-lookup"><span data-stu-id="5b1cd-134">Header</span></span><br/>  | <dl> <span data-ttu-id="5b1cd-135"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5b1cd-135"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5b1cd-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="5b1cd-136">Library</span></span><br/> | <dl> <span data-ttu-id="5b1cd-137"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5b1cd-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b1cd-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b1cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b1cd-139">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="5b1cd-139">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




