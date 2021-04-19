---
description: DeliverEndFlush 方法會要求連接的輸入 pin，以結束清除作業。
ms.assetid: e37bf06a-6cdc-4f14-bf2e-7a7d7004cff6
title: 'CDynamicOutputPin. DeliverEndFlush 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2666681dcd5637a8e919ced2c61d6536663d7b30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000375"
---
# <a name="cdynamicoutputpindeliverendflush-method"></a><span data-ttu-id="6df74-103">CDynamicOutputPin. DeliverEndFlush 方法</span><span class="sxs-lookup"><span data-stu-id="6df74-103">CDynamicOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="6df74-104">`DeliverEndFlush`方法會要求連接的輸入 pin 以結束排清作業。</span><span class="sxs-lookup"><span data-stu-id="6df74-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6df74-105">語法</span><span class="sxs-lookup"><span data-stu-id="6df74-105">Syntax</span></span>


```C++
HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="6df74-106">參數</span><span class="sxs-lookup"><span data-stu-id="6df74-106">Parameters</span></span>

<span data-ttu-id="6df74-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6df74-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6df74-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6df74-108">Return value</span></span>

<span data-ttu-id="6df74-109">\_如果成功，則傳回，否則會傳回指出失敗原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6df74-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df74-110">備註</span><span class="sxs-lookup"><span data-stu-id="6df74-110">Remarks</span></span>

<span data-ttu-id="6df74-111">這個方法會覆寫 [**CBaseOutputPin：:D eliverendflush**](cbaseoutputpin-deliverendflush.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6df74-111">This method overrides the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span> <span data-ttu-id="6df74-112">它會重設 [**CDynamicOutputPin：： m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="6df74-112">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df74-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6df74-113">Requirements</span></span>



| <span data-ttu-id="6df74-114">需求</span><span class="sxs-lookup"><span data-stu-id="6df74-114">Requirement</span></span> | <span data-ttu-id="6df74-115">值</span><span class="sxs-lookup"><span data-stu-id="6df74-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6df74-116">標頭</span><span class="sxs-lookup"><span data-stu-id="6df74-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6df74-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="6df74-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6df74-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="6df74-118">Library</span></span><br/> | <dl> <span data-ttu-id="6df74-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="6df74-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6df74-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6df74-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df74-121">**CDynamicOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="6df74-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




