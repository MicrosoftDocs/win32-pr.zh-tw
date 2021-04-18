---
description: CurrentStartTime 方法會捕獲區段開始時間，由 CBasePin：： NewSegment 方法設定。
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: 'CBasePin. CurrentStartTime 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976270"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="d6acd-103">CBasePin. CurrentStartTime 方法</span><span class="sxs-lookup"><span data-stu-id="d6acd-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="d6acd-104">方法會抓取 `CurrentStartTime` 區段開始時間，由 [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法設定。</span><span class="sxs-lookup"><span data-stu-id="d6acd-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6acd-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6acd-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="d6acd-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6acd-106">Parameters</span></span>

<span data-ttu-id="d6acd-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d6acd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6acd-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6acd-108">Return value</span></span>

<span data-ttu-id="d6acd-109">傳回 [**CBasePin：： m \_ tStart**](cbasepin-m-tstart.md)的值。</span><span class="sxs-lookup"><span data-stu-id="d6acd-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6acd-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6acd-110">Requirements</span></span>



| <span data-ttu-id="d6acd-111">需求</span><span class="sxs-lookup"><span data-stu-id="d6acd-111">Requirement</span></span> | <span data-ttu-id="d6acd-112">值</span><span class="sxs-lookup"><span data-stu-id="d6acd-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6acd-113">標頭</span><span class="sxs-lookup"><span data-stu-id="d6acd-113">Header</span></span><br/>  | <dl> <span data-ttu-id="d6acd-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6acd-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6acd-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6acd-115">Library</span></span><br/> | <dl> <span data-ttu-id="d6acd-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d6acd-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6acd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6acd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6acd-118">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="d6acd-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




