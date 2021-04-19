---
description: BeginFlush 方法會開始進行清除作業。
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: 'COutputQueue. BeginFlush 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990699"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="ab71b-103">COutputQueue. BeginFlush 方法</span><span class="sxs-lookup"><span data-stu-id="ab71b-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="ab71b-104">`BeginFlush`方法會開始清除作業。</span><span class="sxs-lookup"><span data-stu-id="ab71b-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab71b-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab71b-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="ab71b-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab71b-106">Parameters</span></span>

<span data-ttu-id="ab71b-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ab71b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab71b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab71b-108">Return value</span></span>

<span data-ttu-id="ab71b-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ab71b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab71b-110">備註</span><span class="sxs-lookup"><span data-stu-id="ab71b-110">Remarks</span></span>

<span data-ttu-id="ab71b-111">這個方法會將 [**COutputQueue：： m \_ bFlushing**](coutputqueue-m-bflushing.md) 成員變數設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="ab71b-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="ab71b-112">如果物件使用執行緒，執行緒會呼叫 [**COutputQueue：： FreeSamples**](coutputqueue-freesamples.md) 方法來釋放任何暫止的樣本。</span><span class="sxs-lookup"><span data-stu-id="ab71b-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="ab71b-113">否則，物件會在 [**COutputQueue：： EndFlush**](coutputqueue-endflush.md)方法期間呼叫 **FreeSamples** 。</span><span class="sxs-lookup"><span data-stu-id="ab71b-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="ab71b-114">這個方法也會將 [**COutputQueue：： m \_ hr**](coutputqueue-m-hr.md) 成員變數設定為 \_ FALSE，這會導致物件捨棄所有新的範例。</span><span class="sxs-lookup"><span data-stu-id="ab71b-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="ab71b-115">物件會在輸入 pin 上呼叫 [**IPin：： BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) 方法，以傳遞排清通知。</span><span class="sxs-lookup"><span data-stu-id="ab71b-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab71b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab71b-116">Requirements</span></span>



| <span data-ttu-id="ab71b-117">需求</span><span class="sxs-lookup"><span data-stu-id="ab71b-117">Requirement</span></span> | <span data-ttu-id="ab71b-118">值</span><span class="sxs-lookup"><span data-stu-id="ab71b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab71b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="ab71b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ab71b-120"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="ab71b-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab71b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab71b-121">Library</span></span><br/> | <dl> <span data-ttu-id="ab71b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="ab71b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab71b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab71b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab71b-124">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="ab71b-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




