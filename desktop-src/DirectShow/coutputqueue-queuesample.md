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
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999992"
---
# <a name="coutputqueuequeuesample-method"></a><span data-ttu-id="e5020-103">COutputQueue. QueueSample 方法</span><span class="sxs-lookup"><span data-stu-id="e5020-103">COutputQueue.QueueSample method</span></span>

<span data-ttu-id="e5020-104">方法會將 `QueueSample` 範例排在佇列中。</span><span class="sxs-lookup"><span data-stu-id="e5020-104">The `QueueSample` method queues a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5020-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5020-105">Syntax</span></span>


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e5020-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5020-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5020-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="e5020-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e5020-108">範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="e5020-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5020-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5020-109">Return value</span></span>

<span data-ttu-id="e5020-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e5020-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5020-111">備註</span><span class="sxs-lookup"><span data-stu-id="e5020-111">Remarks</span></span>

<span data-ttu-id="e5020-112">這個方法會將範例新增至佇列的結尾。</span><span class="sxs-lookup"><span data-stu-id="e5020-112">This method adds a sample to the tail of the queue.</span></span> <span data-ttu-id="e5020-113">在呼叫這個方法之前，請先保存重要區段，並只在物件使用執行緒來傳遞範例時呼叫它。</span><span class="sxs-lookup"><span data-stu-id="e5020-113">Hold the critical section before calling this method, and call it only when the object is using a thread to deliver samples.</span></span> <span data-ttu-id="e5020-114">若要判斷物件是否使用執行緒，請呼叫 [**COutputQueue：： IsQueued**](coutputqueue-isqueued.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e5020-114">To determine if the object is using a thread, call the [**COutputQueue::IsQueued**](coutputqueue-isqueued.md) method.</span></span>

<span data-ttu-id="e5020-115">這個方法也可以用來將控制訊息放到佇列上。</span><span class="sxs-lookup"><span data-stu-id="e5020-115">This method can also be used to put control messages onto the queue.</span></span> <span data-ttu-id="e5020-116">控制訊息是已定義的常數 (轉換成長的 \_ PTR 型別) ，指示執行緒執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="e5020-116">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform some action.</span></span> <span data-ttu-id="e5020-117">**COutputQueue** 類別會定義下表中顯示的控制訊息。</span><span class="sxs-lookup"><span data-stu-id="e5020-117">The **COutputQueue** class defines the control messages shown in the following table.</span></span>



|               |                                        |
|---------------|----------------------------------------|
| <span data-ttu-id="e5020-118">訊息</span><span class="sxs-lookup"><span data-stu-id="e5020-118">Message</span></span>       | <span data-ttu-id="e5020-119">動作</span><span class="sxs-lookup"><span data-stu-id="e5020-119">Action</span></span>                                 |
| <span data-ttu-id="e5020-120">EOS 封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="e5020-120">EOS\_PACKET</span></span>   | <span data-ttu-id="e5020-121">傳遞資料流程結束通知。</span><span class="sxs-lookup"><span data-stu-id="e5020-121">Deliver an end-of-stream notification.</span></span> |
| <span data-ttu-id="e5020-122">新 \_ 區段</span><span class="sxs-lookup"><span data-stu-id="e5020-122">NEW\_SEGMENT</span></span>  | <span data-ttu-id="e5020-123">傳遞新的區段。</span><span class="sxs-lookup"><span data-stu-id="e5020-123">Deliver a new segment.</span></span>                 |
| <span data-ttu-id="e5020-124">重設封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="e5020-124">RESET\_PACKET</span></span> | <span data-ttu-id="e5020-125">重設佇列的狀態。</span><span class="sxs-lookup"><span data-stu-id="e5020-125">Reset the state of the queue.</span></span>          |
| <span data-ttu-id="e5020-126">傳送封 \_ 包</span><span class="sxs-lookup"><span data-stu-id="e5020-126">SEND\_PACKET</span></span>  | <span data-ttu-id="e5020-127">傳送部分範例的批次。</span><span class="sxs-lookup"><span data-stu-id="e5020-127">Send a partial batch of samples.</span></span>       |



 

<span data-ttu-id="e5020-128">這是 **COutputQueue** 類別在內部使用的受保護方法。</span><span class="sxs-lookup"><span data-stu-id="e5020-128">This is a protected method, which the **COutputQueue** class uses internally.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5020-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5020-129">Requirements</span></span>



| <span data-ttu-id="e5020-130">需求</span><span class="sxs-lookup"><span data-stu-id="e5020-130">Requirement</span></span> | <span data-ttu-id="e5020-131">值</span><span class="sxs-lookup"><span data-stu-id="e5020-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5020-132">標頭</span><span class="sxs-lookup"><span data-stu-id="e5020-132">Header</span></span><br/>  | <dl> <span data-ttu-id="e5020-133"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e5020-133"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e5020-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="e5020-134">Library</span></span><br/> | <dl> <span data-ttu-id="e5020-135"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e5020-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5020-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5020-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5020-137">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="e5020-137">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




