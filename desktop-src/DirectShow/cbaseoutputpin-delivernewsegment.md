---
description: DeliverNewSegment 方法會將新區段通知傳遞至連接的輸入 pin。
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: 'CBaseOutputPin. DeliverNewSegment 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001930"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="4701b-103">CBaseOutputPin. DeliverNewSegment 方法</span><span class="sxs-lookup"><span data-stu-id="4701b-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="4701b-104">方法會將 `DeliverNewSegment` 新區段通知傳遞至連接的輸入 pin。</span><span class="sxs-lookup"><span data-stu-id="4701b-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="4701b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4701b-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="4701b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4701b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4701b-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="4701b-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="4701b-108">區段的開始媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="4701b-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4701b-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="4701b-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="4701b-110">區段的結束媒體位置，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="4701b-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="4701b-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="4701b-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="4701b-112">此區段的處理速率（以原始費率的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="4701b-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4701b-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4701b-113">Return value</span></span>

<span data-ttu-id="4701b-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4701b-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4701b-115">可能的值包括下表所列的值。</span><span class="sxs-lookup"><span data-stu-id="4701b-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="4701b-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4701b-116">Return code</span></span>                                                                                           | <span data-ttu-id="4701b-117">Description</span><span class="sxs-lookup"><span data-stu-id="4701b-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4701b-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4701b-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="4701b-119">成功。</span><span class="sxs-lookup"><span data-stu-id="4701b-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="4701b-120"><dt>**VFW \_ E \_ 未 \_ 連線**</dt></span><span class="sxs-lookup"><span data-stu-id="4701b-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4701b-121">Pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="4701b-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4701b-122">備註</span><span class="sxs-lookup"><span data-stu-id="4701b-122">Remarks</span></span>

<span data-ttu-id="4701b-123">這個方法會呼叫輸入釘選上的 [**IPin：： NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) 方法。</span><span class="sxs-lookup"><span data-stu-id="4701b-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="4701b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4701b-124">Requirements</span></span>



| <span data-ttu-id="4701b-125">需求</span><span class="sxs-lookup"><span data-stu-id="4701b-125">Requirement</span></span> | <span data-ttu-id="4701b-126">值</span><span class="sxs-lookup"><span data-stu-id="4701b-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4701b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="4701b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4701b-128"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4701b-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4701b-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="4701b-129">Library</span></span><br/> | <dl> <span data-ttu-id="4701b-130"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4701b-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4701b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4701b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4701b-132">**CBaseOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="4701b-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




