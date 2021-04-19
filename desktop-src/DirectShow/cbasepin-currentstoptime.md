---
description: CurrentStopTime 方法會抓取區段停止時間，由 CBasePin：： NewSegment 方法設定。
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: 'CBasePin. CurrentStopTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977523"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="3fb2d-103">CBasePin. CurrentStopTime 方法</span><span class="sxs-lookup"><span data-stu-id="3fb2d-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="3fb2d-104">方法會抓取 `CurrentStopTime` 區段停止時間，由 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法設定。</span><span class="sxs-lookup"><span data-stu-id="3fb2d-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fb2d-105">語法</span><span class="sxs-lookup"><span data-stu-id="3fb2d-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="3fb2d-106">參數</span><span class="sxs-lookup"><span data-stu-id="3fb2d-106">Parameters</span></span>

<span data-ttu-id="3fb2d-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3fb2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3fb2d-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3fb2d-108">Return value</span></span>

<span data-ttu-id="3fb2d-109">傳回 [**CBasePin：： m \_ tStop**](cbasepin-m-tstop.md)的值。</span><span class="sxs-lookup"><span data-stu-id="3fb2d-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3fb2d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="3fb2d-110">Requirements</span></span>



| <span data-ttu-id="3fb2d-111">需求</span><span class="sxs-lookup"><span data-stu-id="3fb2d-111">Requirement</span></span> | <span data-ttu-id="3fb2d-112">值</span><span class="sxs-lookup"><span data-stu-id="3fb2d-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb2d-113">標頭</span><span class="sxs-lookup"><span data-stu-id="3fb2d-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3fb2d-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="3fb2d-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3fb2d-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="3fb2d-115">Library</span></span><br/> | <dl> <span data-ttu-id="3fb2d-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="3fb2d-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb2d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3fb2d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb2d-118">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="3fb2d-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




