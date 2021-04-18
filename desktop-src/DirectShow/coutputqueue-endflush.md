---
description: EndFlush 方法會結束清除作業。
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: 'COutputQueue. EndFlush 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976156"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="809a1-103">COutputQueue. EndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="809a1-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="809a1-104">`EndFlush`方法會結束清除作業。</span><span class="sxs-lookup"><span data-stu-id="809a1-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="809a1-105">語法</span><span class="sxs-lookup"><span data-stu-id="809a1-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="809a1-106">參數</span><span class="sxs-lookup"><span data-stu-id="809a1-106">Parameters</span></span>

<span data-ttu-id="809a1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="809a1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="809a1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="809a1-108">Return value</span></span>

<span data-ttu-id="809a1-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="809a1-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="809a1-110">備註</span><span class="sxs-lookup"><span data-stu-id="809a1-110">Remarks</span></span>

<span data-ttu-id="809a1-111">如果物件使用執行緒，這個方法會等候 [**COutputQueue：： m \_ evFlushComplete**](coutputqueue-m-evflushcomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="809a1-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="809a1-112">執行緒釋放任何暫止的樣本之後，會對此事件發出信號。</span><span class="sxs-lookup"><span data-stu-id="809a1-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="809a1-113">如果物件不是使用執行緒，這個方法會呼叫 [**COutputQueue：： FreeSamples**](coutputqueue-freesamples.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="809a1-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="809a1-114">然後， `EndFlush` 方法會在輸入 pin 上呼叫 [**IPin：： EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) 方法。</span><span class="sxs-lookup"><span data-stu-id="809a1-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="809a1-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="809a1-115">Requirements</span></span>



| <span data-ttu-id="809a1-116">需求</span><span class="sxs-lookup"><span data-stu-id="809a1-116">Requirement</span></span> | <span data-ttu-id="809a1-117">值</span><span class="sxs-lookup"><span data-stu-id="809a1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="809a1-118">標頭</span><span class="sxs-lookup"><span data-stu-id="809a1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="809a1-119"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="809a1-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="809a1-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="809a1-120">Library</span></span><br/> | <dl> <span data-ttu-id="809a1-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="809a1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="809a1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="809a1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="809a1-123">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="809a1-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




