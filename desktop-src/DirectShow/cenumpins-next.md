---
description: 下一個方法會抓取列舉序列中指定的 pin 數目。 這個方法會實 IEnumPins：： Next 方法。
ms.assetid: c38fbd32-7d83-43ec-a105-4a7cb515b471
title: 'CEnumPins 下一個方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 612dcd638939b34803b7296babf7445a07cdad22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989879"
---
# <a name="cenumpinsnext-method"></a><span data-ttu-id="aadf8-104">CEnumPins. Next 方法</span><span class="sxs-lookup"><span data-stu-id="aadf8-104">CEnumPins.Next method</span></span>

<span data-ttu-id="aadf8-105">下一個方法會抓取列舉序列中指定的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="aadf8-105">The Next method retrieves a specified number of pins in the enumeration sequence.</span></span> <span data-ttu-id="aadf8-106">這個方法會實 [**IEnumPins：： Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) 方法。</span><span class="sxs-lookup"><span data-stu-id="aadf8-106">This method implements the [**IEnumPins::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aadf8-107">語法</span><span class="sxs-lookup"><span data-stu-id="aadf8-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG cPins,
   IPin  **ppPins,
   ULONG *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="aadf8-108">參數</span><span class="sxs-lookup"><span data-stu-id="aadf8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aadf8-109">*cPins*</span><span class="sxs-lookup"><span data-stu-id="aadf8-109">*cPins*</span></span> 
</dt> <dd>

<span data-ttu-id="aadf8-110">要取出的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="aadf8-110">Number of pins to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="aadf8-111">*ppPins*</span><span class="sxs-lookup"><span data-stu-id="aadf8-111">*ppPins*</span></span> 
</dt> <dd>

<span data-ttu-id="aadf8-112">以 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)指標填滿的大小 *cPins* 陣列。</span><span class="sxs-lookup"><span data-stu-id="aadf8-112">Array of size *cPins* that is filled with [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) pointers.</span></span>

</dd> <dt>

<span data-ttu-id="aadf8-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="aadf8-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="aadf8-114">變數的指標，此變數會接收已抓取的 pin 數目。</span><span class="sxs-lookup"><span data-stu-id="aadf8-114">Pointer to a variable that receives the number of pins retrieved.</span></span> <span data-ttu-id="aadf8-115">如果 *cPins* 是1，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="aadf8-115">Can be **NULL** if *cPins* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aadf8-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="aadf8-116">Return value</span></span>

<span data-ttu-id="aadf8-117">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="aadf8-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="aadf8-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="aadf8-118">Return code</span></span>                                                                                                | <span data-ttu-id="aadf8-119">Description</span><span class="sxs-lookup"><span data-stu-id="aadf8-119">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aadf8-120"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="aadf8-121">未依要求抓取多少 pin。</span><span class="sxs-lookup"><span data-stu-id="aadf8-121">Did not retrieve as many pins as requested.</span></span><br/>                                 |
| <dl> <span data-ttu-id="aadf8-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="aadf8-123">成功。</span><span class="sxs-lookup"><span data-stu-id="aadf8-123">Success.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="aadf8-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="aadf8-125">無效引數。</span><span class="sxs-lookup"><span data-stu-id="aadf8-125">Invalid argument.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="aadf8-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="aadf8-127">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="aadf8-127">**NULL** pointer argument.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="aadf8-128"><dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="aadf8-129">篩選的狀態已變更，且現在與列舉值不一致。</span><span class="sxs-lookup"><span data-stu-id="aadf8-129">The filter's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aadf8-130">備註</span><span class="sxs-lookup"><span data-stu-id="aadf8-130">Remarks</span></span>

<span data-ttu-id="aadf8-131">這個方法會從列舉中的目前位置開始，將指標指向指定數目的釘選，然後將它們放在指定的陣列中。</span><span class="sxs-lookup"><span data-stu-id="aadf8-131">This method retrieves pointers to the specified number of pins, starting at the current position in the enumeration, and places them in the specified array.</span></span>

<span data-ttu-id="aadf8-132">這個方法會呼叫篩選器的 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md) 方法來取出釘選。</span><span class="sxs-lookup"><span data-stu-id="aadf8-132">This method calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to retrieve the pins.</span></span>

<span data-ttu-id="aadf8-133">如果方法成功，則 **IPin** 指標全都具有未完成的參考計數。</span><span class="sxs-lookup"><span data-stu-id="aadf8-133">If the method succeeds, the **IPin** pointers all have outstanding reference counts.</span></span> <span data-ttu-id="aadf8-134">當您完成時，請務必釋放它們。</span><span class="sxs-lookup"><span data-stu-id="aadf8-134">Be sure to release them when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="aadf8-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="aadf8-135">Requirements</span></span>



| <span data-ttu-id="aadf8-136">需求</span><span class="sxs-lookup"><span data-stu-id="aadf8-136">Requirement</span></span> | <span data-ttu-id="aadf8-137">值</span><span class="sxs-lookup"><span data-stu-id="aadf8-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aadf8-138">標頭</span><span class="sxs-lookup"><span data-stu-id="aadf8-138">Header</span></span><br/>  | <dl> <span data-ttu-id="aadf8-139"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="aadf8-140">程式庫</span><span class="sxs-lookup"><span data-stu-id="aadf8-140">Library</span></span><br/> | <dl> <span data-ttu-id="aadf8-141"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aadf8-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aadf8-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aadf8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aadf8-143">**CEnumPins 類別**</span><span class="sxs-lookup"><span data-stu-id="aadf8-143">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




