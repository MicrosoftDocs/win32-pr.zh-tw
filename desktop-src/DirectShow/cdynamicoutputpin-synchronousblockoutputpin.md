---
description: SynchronousBlockOutputPin 方法會封鎖釘選;在封鎖 pin 之前，不會返回。
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: 'CDynamicOutputPin. SynchronousBlockOutputPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001206"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="92978-103">CDynamicOutputPin. SynchronousBlockOutputPin 方法</span><span class="sxs-lookup"><span data-stu-id="92978-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="92978-104">`SynchronousBlockOutputPin`方法會封鎖釘選; 在封鎖 pin 之前，不會傳回。</span><span class="sxs-lookup"><span data-stu-id="92978-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="92978-105">語法</span><span class="sxs-lookup"><span data-stu-id="92978-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="92978-106">參數</span><span class="sxs-lookup"><span data-stu-id="92978-106">Parameters</span></span>

<span data-ttu-id="92978-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="92978-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92978-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="92978-108">Return value</span></span>

<span data-ttu-id="92978-109">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="92978-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="92978-110">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="92978-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="92978-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="92978-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="92978-112">Description</span><span class="sxs-lookup"><span data-stu-id="92978-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="92978-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="92978-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="92978-114">成功。</span><span class="sxs-lookup"><span data-stu-id="92978-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="92978-115"><dt>**VFW \_ E \_ PIN \_ 已 \_ 封鎖**</dt></span><span class="sxs-lookup"><span data-stu-id="92978-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="92978-116">Pin 已在另一個執行緒上遭到封鎖。</span><span class="sxs-lookup"><span data-stu-id="92978-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="92978-117"><dt>**\_ \_ \_ \_ \_ \_ 此執行緒上已封鎖 \_ VFW E PIN**</dt></span><span class="sxs-lookup"><span data-stu-id="92978-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="92978-118">呼叫執行緒上已封鎖 Pin。</span><span class="sxs-lookup"><span data-stu-id="92978-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92978-119">備註</span><span class="sxs-lookup"><span data-stu-id="92978-119">Remarks</span></span>

<span data-ttu-id="92978-120">請勿從串流執行緒呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="92978-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="92978-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="92978-121">Requirements</span></span>



| <span data-ttu-id="92978-122">需求</span><span class="sxs-lookup"><span data-stu-id="92978-122">Requirement</span></span> | <span data-ttu-id="92978-123">值</span><span class="sxs-lookup"><span data-stu-id="92978-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92978-124">標頭</span><span class="sxs-lookup"><span data-stu-id="92978-124">Header</span></span><br/>  | <dl> <span data-ttu-id="92978-125"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="92978-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="92978-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="92978-126">Library</span></span><br/> | <dl> <span data-ttu-id="92978-127"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="92978-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92978-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92978-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92978-129">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="92978-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




