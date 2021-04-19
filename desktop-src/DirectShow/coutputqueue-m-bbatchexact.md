---
description: 旗標，指定物件是否以精確的批次傳遞範例。
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'COutputQueue：： m_bBatchExact 成員 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990075"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="e58e2-103">COutputQueue：： m \_ bBatchExact 成員</span><span class="sxs-lookup"><span data-stu-id="e58e2-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="e58e2-104">旗標，指定物件是否以精確的批次傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="e58e2-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="e58e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="e58e2-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="e58e2-106">備註</span><span class="sxs-lookup"><span data-stu-id="e58e2-106">Remarks</span></span>

<span data-ttu-id="e58e2-107">如果值為 **TRUE**，則物件會等到它擁有完整的媒體樣本批次，再傳遞任何。</span><span class="sxs-lookup"><span data-stu-id="e58e2-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="e58e2-108">否則，它會在抵達時傳遞範例。</span><span class="sxs-lookup"><span data-stu-id="e58e2-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="e58e2-109">[**COutputQueue：： m \_ lBatchSize**](coutputqueue-m-lbatchsize.md)成員變數定義批次大小。</span><span class="sxs-lookup"><span data-stu-id="e58e2-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="e58e2-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="e58e2-110">Requirements</span></span>



| <span data-ttu-id="e58e2-111">需求</span><span class="sxs-lookup"><span data-stu-id="e58e2-111">Requirement</span></span> | <span data-ttu-id="e58e2-112">值</span><span class="sxs-lookup"><span data-stu-id="e58e2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e58e2-113">標頭</span><span class="sxs-lookup"><span data-stu-id="e58e2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e58e2-114"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e58e2-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e58e2-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="e58e2-115">Library</span></span><br/> | <dl> <span data-ttu-id="e58e2-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e58e2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e58e2-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e58e2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e58e2-118">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="e58e2-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




