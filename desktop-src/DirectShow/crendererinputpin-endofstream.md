---
description: EndOfStream 方法會通知 pin，不需要額外的資料。 這個方法會覆寫 CBasePin：： EndOfStream 方法。
ms.assetid: fb5fd8bb-47be-4df6-b837-2c5ff4347478
title: 'CRendererInputPin. EndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a8f495c87a86efc9d5625868c7f8fd4afd6ff1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991018"
---
# <a name="crendererinputpinendofstream-method"></a><span data-ttu-id="59706-104">CRendererInputPin. EndOfStream 方法</span><span class="sxs-lookup"><span data-stu-id="59706-104">CRendererInputPin.EndOfStream method</span></span>

<span data-ttu-id="59706-105">`EndOfStream`方法會通知 pin，不需要任何其他資料。</span><span class="sxs-lookup"><span data-stu-id="59706-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="59706-106">這個方法會覆寫 [**CBasePin：： EndOfStream**](cbasepin-endofstream.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="59706-106">This method overrides the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="59706-107">語法</span><span class="sxs-lookup"><span data-stu-id="59706-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="59706-108">參數</span><span class="sxs-lookup"><span data-stu-id="59706-108">Parameters</span></span>

<span data-ttu-id="59706-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="59706-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59706-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="59706-110">Return value</span></span>

<span data-ttu-id="59706-111">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="59706-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="59706-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="59706-112">Requirements</span></span>



| <span data-ttu-id="59706-113">需求</span><span class="sxs-lookup"><span data-stu-id="59706-113">Requirement</span></span> | <span data-ttu-id="59706-114">值</span><span class="sxs-lookup"><span data-stu-id="59706-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59706-115">標頭</span><span class="sxs-lookup"><span data-stu-id="59706-115">Header</span></span><br/>  | <dl> <span data-ttu-id="59706-116"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="59706-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59706-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="59706-117">Library</span></span><br/> | <dl> <span data-ttu-id="59706-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="59706-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59706-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59706-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59706-120">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="59706-120">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




