---
description: CDynamicOutputPin. DeliverEndFlush 方法-DeliverEndFlush 方法會要求連接的輸入 pin，以結束清除作業。
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: 'CDynamicOutputPin. DeliverEndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c8b6952ff50dc2266655c58bd5c2e1ed13105598
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095706"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="bb2db-103">CDynamicOutputPin. DeliverEndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="bb2db-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="bb2db-104">`DeliverEndFlush`方法會要求連接的輸入 pin 以結束排清作業。</span><span class="sxs-lookup"><span data-stu-id="bb2db-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2db-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb2db-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="bb2db-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb2db-106">Parameters</span></span>

<span data-ttu-id="bb2db-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bb2db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb2db-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb2db-108">Return value</span></span>

<span data-ttu-id="bb2db-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="bb2db-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2db-110">備註</span><span class="sxs-lookup"><span data-stu-id="bb2db-110">Remarks</span></span>

<span data-ttu-id="bb2db-111">這個方法會覆寫 [**CBaseOutputPin：:D eliverendflush**](cbaseoutputpin-deliverendflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bb2db-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="bb2db-112">它會重設 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="bb2db-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb2db-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb2db-113">Requirements</span></span>



| <span data-ttu-id="bb2db-114">需求</span><span class="sxs-lookup"><span data-stu-id="bb2db-114">Requirement</span></span> | <span data-ttu-id="bb2db-115">值</span><span class="sxs-lookup"><span data-stu-id="bb2db-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2db-116">標頭</span><span class="sxs-lookup"><span data-stu-id="bb2db-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bb2db-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bb2db-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb2db-118">Library</span></span><br/> | <dl> <span data-ttu-id="bb2db-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="bb2db-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2db-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb2db-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2db-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="bb2db-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




