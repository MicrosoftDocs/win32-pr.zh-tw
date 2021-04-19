---
description: SendAnyway 方法會提供任何暫止的範例。
ms.assetid: b4e3a0c6-0f72-4a00-963e-65ceed265f01
title: 'COutputQueue. SendAnyway 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SendAnyway
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6fa5495371e020310e2367aea7e7bed9ef113f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986174"
---
# <a name="coutputqueuesendanyway-method"></a><span data-ttu-id="be3ff-103">COutputQueue. SendAnyway 方法</span><span class="sxs-lookup"><span data-stu-id="be3ff-103">COutputQueue.SendAnyway method</span></span>

<span data-ttu-id="be3ff-104">`SendAnyway`方法會提供任何暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="be3ff-104">The `SendAnyway` method delivers any pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="be3ff-105">語法</span><span class="sxs-lookup"><span data-stu-id="be3ff-105">Syntax</span></span>


```C++
void SendAnyway();
```



## <a name="parameters"></a><span data-ttu-id="be3ff-106">參數</span><span class="sxs-lookup"><span data-stu-id="be3ff-106">Parameters</span></span>

<span data-ttu-id="be3ff-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="be3ff-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be3ff-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="be3ff-108">Return value</span></span>

<span data-ttu-id="be3ff-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="be3ff-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be3ff-110">備註</span><span class="sxs-lookup"><span data-stu-id="be3ff-110">Remarks</span></span>

<span data-ttu-id="be3ff-111">如果 [**COutputQueue：： m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) 成員變數為 **TRUE**，則物件會先填滿 [**COutputQueue：： m \_ ppSamples**](coutputqueue-m-ppsamples.md) 陣列，然後再傳遞一批樣本。</span><span class="sxs-lookup"><span data-stu-id="be3ff-111">If the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) member variable is **TRUE**, the object fills the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array before it delivers a batch of samples.</span></span> <span data-ttu-id="be3ff-112">呼叫此方法以傳遞部分批次。</span><span class="sxs-lookup"><span data-stu-id="be3ff-112">Call this method to deliver a partial batch.</span></span> <span data-ttu-id="be3ff-113">例如， [**COutputQueue：： EOS**](coutputqueue-eos.md) 方法會呼叫 `SendAnyway` 以序列化資料流程結束的訊息。</span><span class="sxs-lookup"><span data-stu-id="be3ff-113">For example, the [**COutputQueue::EOS**](coutputqueue-eos.md) method calls `SendAnyway` to serialize end-of-stream messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="be3ff-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="be3ff-114">Requirements</span></span>



| <span data-ttu-id="be3ff-115">需求</span><span class="sxs-lookup"><span data-stu-id="be3ff-115">Requirement</span></span> | <span data-ttu-id="be3ff-116">值</span><span class="sxs-lookup"><span data-stu-id="be3ff-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be3ff-117">標頭</span><span class="sxs-lookup"><span data-stu-id="be3ff-117">Header</span></span><br/>  | <dl> <span data-ttu-id="be3ff-118"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="be3ff-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be3ff-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="be3ff-119">Library</span></span><br/> | <dl> <span data-ttu-id="be3ff-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="be3ff-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be3ff-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be3ff-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be3ff-122">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="be3ff-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




