---
description: SetDefaultTimerResolution 方法會設定參考時鐘計時器的解析度。
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: 'CBaseReferenceClock. SetDefaultTimerResolution 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991196"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="68c00-103">CBaseReferenceClock. SetDefaultTimerResolution 方法</span><span class="sxs-lookup"><span data-stu-id="68c00-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="68c00-104">`SetDefaultTimerResolution`方法會設定參考時鐘計時器的解析度。</span><span class="sxs-lookup"><span data-stu-id="68c00-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c00-105">語法</span><span class="sxs-lookup"><span data-stu-id="68c00-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="68c00-106">參數</span><span class="sxs-lookup"><span data-stu-id="68c00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68c00-107">*timerResolution*</span><span class="sxs-lookup"><span data-stu-id="68c00-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="68c00-108">最小計時器解析度（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="68c00-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="68c00-109">如果值為零，則參考時鐘會取消其先前的要求。</span><span class="sxs-lookup"><span data-stu-id="68c00-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68c00-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="68c00-110">Return value</span></span>

<span data-ttu-id="68c00-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="68c00-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68c00-112">備註</span><span class="sxs-lookup"><span data-stu-id="68c00-112">Remarks</span></span>

<span data-ttu-id="68c00-113">這個方法會實 [**IReferenceClockTimerControl：： SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) 方法。</span><span class="sxs-lookup"><span data-stu-id="68c00-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c00-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="68c00-114">Requirements</span></span>



| <span data-ttu-id="68c00-115">需求</span><span class="sxs-lookup"><span data-stu-id="68c00-115">Requirement</span></span> | <span data-ttu-id="68c00-116">值</span><span class="sxs-lookup"><span data-stu-id="68c00-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68c00-117">標頭</span><span class="sxs-lookup"><span data-stu-id="68c00-117">Header</span></span><br/>  | <dl> <span data-ttu-id="68c00-118"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="68c00-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="68c00-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="68c00-119">Library</span></span><br/> | <dl> <span data-ttu-id="68c00-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="68c00-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68c00-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c00-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c00-122">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="68c00-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




