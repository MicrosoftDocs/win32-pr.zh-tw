---
description: 非使用中的方法會通知釘選篩選已停止。
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: 'CDynamicOutputPin：非使用中方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992775"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="980d8-103">CDynamicOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="980d8-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="980d8-104">`Inactive`方法會通知釘選篩選已停止。</span><span class="sxs-lookup"><span data-stu-id="980d8-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="980d8-105">語法</span><span class="sxs-lookup"><span data-stu-id="980d8-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="980d8-106">參數</span><span class="sxs-lookup"><span data-stu-id="980d8-106">Parameters</span></span>

<span data-ttu-id="980d8-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="980d8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="980d8-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="980d8-108">Return value</span></span>

<span data-ttu-id="980d8-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="980d8-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="980d8-110">備註</span><span class="sxs-lookup"><span data-stu-id="980d8-110">Remarks</span></span>

<span data-ttu-id="980d8-111">這個方法會覆寫 [**CBaseOutputPin：：非**](cbaseoutputpin-inactive.md) 使用中的方法。</span><span class="sxs-lookup"><span data-stu-id="980d8-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="980d8-112">它會設定 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="980d8-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="980d8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="980d8-113">Requirements</span></span>



| <span data-ttu-id="980d8-114">需求</span><span class="sxs-lookup"><span data-stu-id="980d8-114">Requirement</span></span> | <span data-ttu-id="980d8-115">值</span><span class="sxs-lookup"><span data-stu-id="980d8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="980d8-116">標頭</span><span class="sxs-lookup"><span data-stu-id="980d8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="980d8-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="980d8-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="980d8-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="980d8-118">Library</span></span><br/> | <dl> <span data-ttu-id="980d8-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="980d8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="980d8-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="980d8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980d8-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="980d8-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




