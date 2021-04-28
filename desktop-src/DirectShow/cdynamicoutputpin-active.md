---
description: CDynamicOutputPin 方法-使用中的方法會通知釘選篩選現在為使用中狀態。
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: 'CDynamicOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099326"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="f83b1-103">CDynamicOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="f83b1-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="f83b1-104">`Active`方法會通知釘選篩選現在已在使用中。</span><span class="sxs-lookup"><span data-stu-id="f83b1-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="f83b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="f83b1-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="f83b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="f83b1-106">Parameters</span></span>

<span data-ttu-id="f83b1-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f83b1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f83b1-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="f83b1-108">Return value</span></span>

<span data-ttu-id="f83b1-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f83b1-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f83b1-110">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="f83b1-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f83b1-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f83b1-111">Return code</span></span>                                                                            | <span data-ttu-id="f83b1-112">Description</span><span class="sxs-lookup"><span data-stu-id="f83b1-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f83b1-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f83b1-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="f83b1-114">成功。</span><span class="sxs-lookup"><span data-stu-id="f83b1-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f83b1-115"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="f83b1-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="f83b1-116">失敗。</span><span class="sxs-lookup"><span data-stu-id="f83b1-116">Failure.</span></span> <span data-ttu-id="f83b1-117">未呼叫 [**CDynamicOutputPin：： SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) 。</span><span class="sxs-lookup"><span data-stu-id="f83b1-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f83b1-118">備註</span><span class="sxs-lookup"><span data-stu-id="f83b1-118">Remarks</span></span>

<span data-ttu-id="f83b1-119">這個方法會覆寫 [**CBaseOutputPin：： Active**](cbaseoutputpin-active.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f83b1-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="f83b1-120">它會重設 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="f83b1-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="f83b1-121">如果擁有篩選準則尚未呼叫 **SetConfigInfo**，這個方法會傳回 E \_ FAIL。</span><span class="sxs-lookup"><span data-stu-id="f83b1-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f83b1-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f83b1-122">Requirements</span></span>



| <span data-ttu-id="f83b1-123">需求</span><span class="sxs-lookup"><span data-stu-id="f83b1-123">Requirement</span></span> | <span data-ttu-id="f83b1-124">值</span><span class="sxs-lookup"><span data-stu-id="f83b1-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f83b1-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f83b1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f83b1-126"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="f83b1-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f83b1-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="f83b1-127">Library</span></span><br/> | <dl> <span data-ttu-id="f83b1-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="f83b1-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f83b1-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f83b1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f83b1-130">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="f83b1-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




