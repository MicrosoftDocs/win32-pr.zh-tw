---
description: FreeSamples 方法會釋出所有暫止的範例。
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: 'COutputQueue. FreeSamples 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993554"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="79315-103">COutputQueue. FreeSamples 方法</span><span class="sxs-lookup"><span data-stu-id="79315-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="79315-104">`FreeSamples`方法會釋出所有暫止的範例。</span><span class="sxs-lookup"><span data-stu-id="79315-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="79315-105">語法</span><span class="sxs-lookup"><span data-stu-id="79315-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="79315-106">參數</span><span class="sxs-lookup"><span data-stu-id="79315-106">Parameters</span></span>

<span data-ttu-id="79315-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="79315-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79315-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="79315-108">Return value</span></span>

<span data-ttu-id="79315-109">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="79315-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79315-110">備註</span><span class="sxs-lookup"><span data-stu-id="79315-110">Remarks</span></span>

<span data-ttu-id="79315-111">這個方法會從佇列和範例陣列移除任何暫止的樣本。</span><span class="sxs-lookup"><span data-stu-id="79315-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="79315-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="79315-112">Requirements</span></span>



| <span data-ttu-id="79315-113">需求</span><span class="sxs-lookup"><span data-stu-id="79315-113">Requirement</span></span> | <span data-ttu-id="79315-114">值</span><span class="sxs-lookup"><span data-stu-id="79315-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79315-115">標頭</span><span class="sxs-lookup"><span data-stu-id="79315-115">Header</span></span><br/>  | <dl> <span data-ttu-id="79315-116"><dt>Outputq (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="79315-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79315-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="79315-117">Library</span></span><br/> | <dl> <span data-ttu-id="79315-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="79315-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79315-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79315-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79315-120">**COutputQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="79315-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




