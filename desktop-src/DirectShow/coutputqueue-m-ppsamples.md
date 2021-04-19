---
description: 大小為 COutputQueue：： m lBatchSize 的範例陣列 \_ 。
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'COutputQueue：： m_ppSamples 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994760"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="12f20-103">COutputQueue：： m \_ ppSamples 成員</span><span class="sxs-lookup"><span data-stu-id="12f20-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="12f20-104">大小為 [**COutputQueue：： m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)的範例陣列。</span><span class="sxs-lookup"><span data-stu-id="12f20-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="12f20-105">語法</span><span class="sxs-lookup"><span data-stu-id="12f20-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="12f20-106">備註</span><span class="sxs-lookup"><span data-stu-id="12f20-106">Remarks</span></span>

<span data-ttu-id="12f20-107">背景工作執行緒會從佇列提取範例，並將它們放在此陣列中。</span><span class="sxs-lookup"><span data-stu-id="12f20-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="12f20-108">它會將陣列傳遞給 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。</span><span class="sxs-lookup"><span data-stu-id="12f20-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="12f20-109">如果物件不是使用背景工作執行緒，則物件會將範例直接放入這個陣列中。</span><span class="sxs-lookup"><span data-stu-id="12f20-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="12f20-110">[**COutputQueue：： m \_ List**](coutputqueue-m-list.md)成員變數會保存佇列。</span><span class="sxs-lookup"><span data-stu-id="12f20-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="12f20-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="12f20-111">Requirements</span></span>



| <span data-ttu-id="12f20-112">需求</span><span class="sxs-lookup"><span data-stu-id="12f20-112">Requirement</span></span> | <span data-ttu-id="12f20-113">值</span><span class="sxs-lookup"><span data-stu-id="12f20-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f20-114">標頭</span><span class="sxs-lookup"><span data-stu-id="12f20-114">Header</span></span><br/>  | <dl> <span data-ttu-id="12f20-115"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12f20-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12f20-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="12f20-116">Library</span></span><br/> | <dl> <span data-ttu-id="12f20-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12f20-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12f20-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12f20-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12f20-119">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="12f20-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




