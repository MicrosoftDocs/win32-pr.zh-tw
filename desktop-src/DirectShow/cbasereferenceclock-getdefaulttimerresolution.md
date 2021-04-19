---
description: GetDefaultTimerResolution 方法會傳回參考時鐘計時器目前的解析度。
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: 'CBaseReferenceClock. GetDefaultTimerResolution 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978706"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="eaa9f-103">CBaseReferenceClock. GetDefaultTimerResolution 方法</span><span class="sxs-lookup"><span data-stu-id="eaa9f-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="eaa9f-104">方法會傳回 `GetDefaultTimerResolution` 目前的參考時鐘計時器解析度。</span><span class="sxs-lookup"><span data-stu-id="eaa9f-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaa9f-105">語法</span><span class="sxs-lookup"><span data-stu-id="eaa9f-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="eaa9f-106">參數</span><span class="sxs-lookup"><span data-stu-id="eaa9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaa9f-107">*pTimerResolution*</span><span class="sxs-lookup"><span data-stu-id="eaa9f-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="eaa9f-108">接收要求的計時器解析度（100-毫微秒單位）。</span><span class="sxs-lookup"><span data-stu-id="eaa9f-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaa9f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaa9f-109">Return value</span></span>

<span data-ttu-id="eaa9f-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eaa9f-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eaa9f-111">備註</span><span class="sxs-lookup"><span data-stu-id="eaa9f-111">Remarks</span></span>

<span data-ttu-id="eaa9f-112">這個方法會實 [**IReferenceClockTimerControl：： GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) 方法。</span><span class="sxs-lookup"><span data-stu-id="eaa9f-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaa9f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaa9f-113">Requirements</span></span>



| <span data-ttu-id="eaa9f-114">需求</span><span class="sxs-lookup"><span data-stu-id="eaa9f-114">Requirement</span></span> | <span data-ttu-id="eaa9f-115">值</span><span class="sxs-lookup"><span data-stu-id="eaa9f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaa9f-116">標頭</span><span class="sxs-lookup"><span data-stu-id="eaa9f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eaa9f-117"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eaa9f-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eaa9f-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="eaa9f-118">Library</span></span><br/> | <dl> <span data-ttu-id="eaa9f-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eaa9f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaa9f-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaa9f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaa9f-121">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="eaa9f-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




