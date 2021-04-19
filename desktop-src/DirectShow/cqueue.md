---
description: CQueue 類別範本會執行簡單、靜態大小的佇列。
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: 'CQueue 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979524"
---
# <a name="cqueue-class"></a><span data-ttu-id="4681d-103">CQueue 類別</span><span class="sxs-lookup"><span data-stu-id="4681d-103">CQueue class</span></span>

<span data-ttu-id="4681d-104">**CQueue** 類別範本會執行簡單、靜態大小的佇列。</span><span class="sxs-lookup"><span data-stu-id="4681d-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="4681d-105">公用方法</span><span class="sxs-lookup"><span data-stu-id="4681d-105">Public Methods</span></span>                                  | <span data-ttu-id="4681d-106">Description</span><span class="sxs-lookup"><span data-stu-id="4681d-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="4681d-107">**CQueue**</span><span class="sxs-lookup"><span data-stu-id="4681d-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="4681d-108">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4681d-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="4681d-109">**~ CQueue**</span><span class="sxs-lookup"><span data-stu-id="4681d-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="4681d-110">函式方法。</span><span class="sxs-lookup"><span data-stu-id="4681d-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="4681d-111">**GetQueueObject**</span><span class="sxs-lookup"><span data-stu-id="4681d-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="4681d-112">從佇列中取出下一個專案。</span><span class="sxs-lookup"><span data-stu-id="4681d-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="4681d-113">**PutQueueObject**</span><span class="sxs-lookup"><span data-stu-id="4681d-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="4681d-114">將專案放在佇列上。</span><span class="sxs-lookup"><span data-stu-id="4681d-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="4681d-115">備註</span><span class="sxs-lookup"><span data-stu-id="4681d-115">Remarks</span></span>

<span data-ttu-id="4681d-116">類別的函式會指定佇列的大小。</span><span class="sxs-lookup"><span data-stu-id="4681d-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="4681d-117">使用 [**CQueue：:P utqueueobject**](cqueue-putqueueobject.md) 將專案放在佇列上，並使用 [**CQueue：： GetQueueObject**](cqueue-getqueueobject.md) 方法清除專案。</span><span class="sxs-lookup"><span data-stu-id="4681d-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="4681d-118">如果佇列已滿，則 **PutQueueObject** 方法會封鎖，直到清除某個專案為止。</span><span class="sxs-lookup"><span data-stu-id="4681d-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="4681d-119">如果佇列是空的， **GetQueueObject** 會封鎖，直到某個專案排入佇列為止。</span><span class="sxs-lookup"><span data-stu-id="4681d-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="4681d-120">範本參數會指定專案的類型。</span><span class="sxs-lookup"><span data-stu-id="4681d-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="4681d-121">例如：</span><span class="sxs-lookup"><span data-stu-id="4681d-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="4681d-122">類別會使用兩個信號來控制佇列作業、「取得」信號和「put」信號。</span><span class="sxs-lookup"><span data-stu-id="4681d-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="4681d-123">[**GetQueueObject**](cqueue-getqueueobject.md)方法會使用) **WaitForSingleObject** 函式來等候 "get" 信號 (，並使用 **ReleaseSemaphore** 函數) 釋放「put」信號 (。</span><span class="sxs-lookup"><span data-stu-id="4681d-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="4681d-124">[**PutQueueObject**](cqueue-putqueueobject.md)方法會等候「put」信號，並釋放「get」信號。</span><span class="sxs-lookup"><span data-stu-id="4681d-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="4681d-125">類別會使用重要區段來序列化多個執行緒之間的佇列作業。</span><span class="sxs-lookup"><span data-stu-id="4681d-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="4681d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4681d-126">Requirements</span></span>



| <span data-ttu-id="4681d-127">需求</span><span class="sxs-lookup"><span data-stu-id="4681d-127">Requirement</span></span> | <span data-ttu-id="4681d-128">值</span><span class="sxs-lookup"><span data-stu-id="4681d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4681d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="4681d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4681d-130"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4681d-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4681d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="4681d-131">Library</span></span><br/> | <dl> <span data-ttu-id="4681d-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4681d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




