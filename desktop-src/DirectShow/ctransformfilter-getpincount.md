---
description: GetPinCount 方法會抓取篩選上的釘選數目。
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: 'CTransformFilter. GetPinCount 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990747"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="dfebf-103">CTransformFilter. GetPinCount 方法</span><span class="sxs-lookup"><span data-stu-id="dfebf-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="dfebf-104">方法會抓取 `GetPinCount` 篩選上的釘選數目。</span><span class="sxs-lookup"><span data-stu-id="dfebf-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfebf-105">語法</span><span class="sxs-lookup"><span data-stu-id="dfebf-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="dfebf-106">參數</span><span class="sxs-lookup"><span data-stu-id="dfebf-106">Parameters</span></span>

<span data-ttu-id="dfebf-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dfebf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfebf-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfebf-108">Return value</span></span>

<span data-ttu-id="dfebf-109">傳回2。</span><span class="sxs-lookup"><span data-stu-id="dfebf-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfebf-110">備註</span><span class="sxs-lookup"><span data-stu-id="dfebf-110">Remarks</span></span>

<span data-ttu-id="dfebf-111">這個方法會覆寫 [**CBaseFilter：： GetPinCount**](cbasefilter-getpincount.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="dfebf-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="dfebf-112">**CTransformFilter** 類別只支援一個輸入 pin 和一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="dfebf-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfebf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfebf-113">Requirements</span></span>



| <span data-ttu-id="dfebf-114">需求</span><span class="sxs-lookup"><span data-stu-id="dfebf-114">Requirement</span></span> | <span data-ttu-id="dfebf-115">值</span><span class="sxs-lookup"><span data-stu-id="dfebf-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfebf-116">標頭</span><span class="sxs-lookup"><span data-stu-id="dfebf-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dfebf-117"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dfebf-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dfebf-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="dfebf-118">Library</span></span><br/> | <dl> <span data-ttu-id="dfebf-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dfebf-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfebf-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfebf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfebf-121">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="dfebf-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




