---
description: CanReconnectWhenActive 方法會查詢 pin 是否支援動態重新連接。
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: 'CBasePin. CanReconnectWhenActive 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993455"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="5e9e2-103">CBasePin. CanReconnectWhenActive 方法</span><span class="sxs-lookup"><span data-stu-id="5e9e2-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="5e9e2-104">`CanReconnectWhenActive`方法會查詢 pin 是否支援動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="5e9e2-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="5e9e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="5e9e2-106">Parameters</span></span>

<span data-ttu-id="5e9e2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e9e2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e9e2-108">Return value</span></span>

<span data-ttu-id="5e9e2-109">傳回布林值，指定 pin 是否可動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="5e9e2-110">若 **為 TRUE**，則 pin 可以動態重新連接。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e9e2-111">備註</span><span class="sxs-lookup"><span data-stu-id="5e9e2-111">Remarks</span></span>

<span data-ttu-id="5e9e2-112">根據預設，您必須先停止篩選，才能重新連接其任何 pin。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="5e9e2-113">但是，如果 pin 支援動態重新連接，則在篩選作用中時，它可以重新連接。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="5e9e2-114">如需詳細資訊，請參閱 [動態圖形建築物](dynamic-graph-building.md)。</span><span class="sxs-lookup"><span data-stu-id="5e9e2-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9e2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e9e2-115">Requirements</span></span>



| <span data-ttu-id="5e9e2-116">需求</span><span class="sxs-lookup"><span data-stu-id="5e9e2-116">Requirement</span></span> | <span data-ttu-id="5e9e2-117">值</span><span class="sxs-lookup"><span data-stu-id="5e9e2-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9e2-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5e9e2-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5e9e2-119"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5e9e2-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5e9e2-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="5e9e2-120">Library</span></span><br/> | <dl> <span data-ttu-id="5e9e2-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="5e9e2-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9e2-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e9e2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9e2-123">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="5e9e2-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




