---
description: IsStopped 方法會判斷是否已停止包含此 pin 的篩選。
ms.assetid: ffeac352-2f9b-44be-a8e8-7e9238d0b18e
title: 'CBasePin. IsStopped 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IsStopped
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4185c02b396f7d0d570081ba1401e0ec9e301d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976245"
---
# <a name="cbasepinisstopped-method"></a><span data-ttu-id="081ea-103">CBasePin. IsStopped 方法</span><span class="sxs-lookup"><span data-stu-id="081ea-103">CBasePin.IsStopped method</span></span>

<span data-ttu-id="081ea-104">`IsStopped`方法會判斷包含此 pin 的篩選是否已停止。</span><span class="sxs-lookup"><span data-stu-id="081ea-104">The `IsStopped` method determines whether the filter containing this pin is stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="081ea-105">語法</span><span class="sxs-lookup"><span data-stu-id="081ea-105">Syntax</span></span>


```C++
BOOL IsStopped();
```



## <a name="parameters"></a><span data-ttu-id="081ea-106">參數</span><span class="sxs-lookup"><span data-stu-id="081ea-106">Parameters</span></span>

<span data-ttu-id="081ea-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="081ea-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="081ea-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="081ea-108">Return value</span></span>

<span data-ttu-id="081ea-109">如果篩選已停止，則傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="081ea-109">Returns **TRUE** if the filter is stopped.</span></span> <span data-ttu-id="081ea-110">否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="081ea-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="081ea-111">備註</span><span class="sxs-lookup"><span data-stu-id="081ea-111">Remarks</span></span>

<span data-ttu-id="081ea-112">請勿在 **CBasePin** 的方法中呼叫這個方法，因為篩選可能尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="081ea-112">Do not call this method from within in the **CBasePin** constructor method, because the filter might not be initialized yet.</span></span>

## <a name="requirements"></a><span data-ttu-id="081ea-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="081ea-113">Requirements</span></span>



| <span data-ttu-id="081ea-114">需求</span><span class="sxs-lookup"><span data-stu-id="081ea-114">Requirement</span></span> | <span data-ttu-id="081ea-115">值</span><span class="sxs-lookup"><span data-stu-id="081ea-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="081ea-116">標頭</span><span class="sxs-lookup"><span data-stu-id="081ea-116">Header</span></span><br/>  | <dl> <span data-ttu-id="081ea-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="081ea-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="081ea-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="081ea-118">Library</span></span><br/> | <dl> <span data-ttu-id="081ea-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="081ea-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="081ea-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="081ea-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="081ea-121">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="081ea-121">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




