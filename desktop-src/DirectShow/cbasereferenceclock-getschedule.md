---
description: GetSchedule 方法會抓取時鐘排程物件的指標。
ms.assetid: ae509f16-d85f-4365-8cf2-c6585cbbdc3d
title: 'CBaseReferenceClock. GetSchedule 方法 (Refclock .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a37cdb3e18f3ab71b144af071233aee5a6a3a93d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000744"
---
# <a name="cbasereferenceclockgetschedule-method"></a><span data-ttu-id="82b10-103">CBaseReferenceClock. GetSchedule 方法</span><span class="sxs-lookup"><span data-stu-id="82b10-103">CBaseReferenceClock.GetSchedule method</span></span>

<span data-ttu-id="82b10-104">方法會抓取 `GetSchedule` 時鐘排程物件的指標。</span><span class="sxs-lookup"><span data-stu-id="82b10-104">The `GetSchedule` method retrieves a pointer to the clock's scheduling object.</span></span>

## <a name="syntax"></a><span data-ttu-id="82b10-105">語法</span><span class="sxs-lookup"><span data-stu-id="82b10-105">Syntax</span></span>


```C++
CAMSchedule* GetSchedule();
```



## <a name="parameters"></a><span data-ttu-id="82b10-106">參數</span><span class="sxs-lookup"><span data-stu-id="82b10-106">Parameters</span></span>

<span data-ttu-id="82b10-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="82b10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82b10-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="82b10-108">Return value</span></span>

<span data-ttu-id="82b10-109">傳回 [**CBaseReferenceClock：： m \_ pSchedule**](cbasereferenceclock-m-pschedule.md) 成員變數。</span><span class="sxs-lookup"><span data-stu-id="82b10-109">Returns the [**CBaseReferenceClock::m\_pSchedule**](cbasereferenceclock-m-pschedule.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="82b10-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b10-110">Requirements</span></span>



| <span data-ttu-id="82b10-111">需求</span><span class="sxs-lookup"><span data-stu-id="82b10-111">Requirement</span></span> | <span data-ttu-id="82b10-112">值</span><span class="sxs-lookup"><span data-stu-id="82b10-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b10-113">標頭</span><span class="sxs-lookup"><span data-stu-id="82b10-113">Header</span></span><br/>  | <dl> <span data-ttu-id="82b10-114"><dt>Refclock (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="82b10-114"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="82b10-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="82b10-115">Library</span></span><br/> | <dl> <span data-ttu-id="82b10-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="82b10-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b10-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82b10-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b10-118">**CBaseReferenceClock 類別**</span><span class="sxs-lookup"><span data-stu-id="82b10-118">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




