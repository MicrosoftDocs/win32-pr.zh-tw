---
description: CurrentRate 方法會抓取區段速率（由 CBasePin：： NewSegment 方法所設定）。
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: 'CBasePin. CurrentRate 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995602"
---
# <a name="cbasepincurrentrate-method"></a><span data-ttu-id="50086-103">CBasePin. CurrentRate 方法</span><span class="sxs-lookup"><span data-stu-id="50086-103">CBasePin.CurrentRate method</span></span>

<span data-ttu-id="50086-104">方法會抓取 `CurrentRate` [**CBasePin：： NewSegment**](cbasepin-newsegment.md) 方法所設定的區段速率。</span><span class="sxs-lookup"><span data-stu-id="50086-104">The `CurrentRate` method retrieves the segment rate, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="50086-105">語法</span><span class="sxs-lookup"><span data-stu-id="50086-105">Syntax</span></span>


```C++
double CurrentRate();
```



## <a name="parameters"></a><span data-ttu-id="50086-106">參數</span><span class="sxs-lookup"><span data-stu-id="50086-106">Parameters</span></span>

<span data-ttu-id="50086-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="50086-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50086-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="50086-108">Return value</span></span>

<span data-ttu-id="50086-109">傳回 [**CBasePin：： m \_ dRate**](cbasepin-m-drate.md)的值。</span><span class="sxs-lookup"><span data-stu-id="50086-109">Returns the value of [**CBasePin::m\_dRate**](cbasepin-m-drate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50086-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="50086-110">Requirements</span></span>



| <span data-ttu-id="50086-111">需求</span><span class="sxs-lookup"><span data-stu-id="50086-111">Requirement</span></span> | <span data-ttu-id="50086-112">值</span><span class="sxs-lookup"><span data-stu-id="50086-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50086-113">標頭</span><span class="sxs-lookup"><span data-stu-id="50086-113">Header</span></span><br/>  | <dl> <span data-ttu-id="50086-114"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="50086-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="50086-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="50086-115">Library</span></span><br/> | <dl> <span data-ttu-id="50086-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="50086-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50086-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50086-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50086-118">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="50086-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




