---
description: NewSegment 方法會將新的區段傳遞給輸入圖釘。
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: 'COutputQueue. NewSegment 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992972"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="404d6-103">COutputQueue. NewSegment 方法</span><span class="sxs-lookup"><span data-stu-id="404d6-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="404d6-104">方法會將 `NewSegment` 新的區段傳遞給輸入圖釘。</span><span class="sxs-lookup"><span data-stu-id="404d6-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="404d6-105">語法</span><span class="sxs-lookup"><span data-stu-id="404d6-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="404d6-106">參數</span><span class="sxs-lookup"><span data-stu-id="404d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="404d6-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="404d6-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="404d6-108">區段的開始媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="404d6-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="404d6-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="404d6-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="404d6-110">區段的結束媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="404d6-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="404d6-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="404d6-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="404d6-112">此區段的處理速率（以原始費率的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="404d6-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="404d6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="404d6-113">Return value</span></span>

<span data-ttu-id="404d6-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="404d6-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="404d6-115">備註</span><span class="sxs-lookup"><span data-stu-id="404d6-115">Remarks</span></span>

<span data-ttu-id="404d6-116">如果物件使用執行緒，則會依序將下列專案排入佇列：</span><span class="sxs-lookup"><span data-stu-id="404d6-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="404d6-117">新的 \_ 區段控制訊息。</span><span class="sxs-lookup"><span data-stu-id="404d6-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="404d6-118">區段資料。</span><span class="sxs-lookup"><span data-stu-id="404d6-118">The segment data.</span></span>

<span data-ttu-id="404d6-119">新的 \_ 區段訊息會通知執行緒，佇列中的下一個專案將包含區段資料。</span><span class="sxs-lookup"><span data-stu-id="404d6-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="404d6-120">區段資料會組合在結構中，如下所示：</span><span class="sxs-lookup"><span data-stu-id="404d6-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="404d6-121">執行緒會使用結構中指定的資料，在輸入釘選上呼叫 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。</span><span class="sxs-lookup"><span data-stu-id="404d6-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="404d6-122">如果物件未使用執行緒，則會呼叫 [**COutputQueue：： SendAnyway**](coutputqueue-sendanyway.md) 方法來傳遞任何暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="404d6-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="404d6-123">然後，它會在輸入 pin 上呼叫 **IPin：： NewSegment** 。</span><span class="sxs-lookup"><span data-stu-id="404d6-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="404d6-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="404d6-124">Requirements</span></span>



| <span data-ttu-id="404d6-125">需求</span><span class="sxs-lookup"><span data-stu-id="404d6-125">Requirement</span></span> | <span data-ttu-id="404d6-126">值</span><span class="sxs-lookup"><span data-stu-id="404d6-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="404d6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="404d6-127">Header</span></span><br/>  | <dl> <span data-ttu-id="404d6-128"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="404d6-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="404d6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="404d6-129">Library</span></span><br/> | <dl> <span data-ttu-id="404d6-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="404d6-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="404d6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="404d6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="404d6-132">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="404d6-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




