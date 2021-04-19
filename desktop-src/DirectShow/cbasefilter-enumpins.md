---
description: EnumPins 方法會列舉此篩選器上的釘選。 這個方法會實 IBaseFilter：： EnumPins 方法。
ms.assetid: c1015ed3-658f-4f96-a1fb-e04b81a9ddb5
title: 'CBaseFilter. EnumPins 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.EnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66a0f88a9749ba1dabb982e2f275da8a4be2a422
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983121"
---
# <a name="cbasefilterenumpins-method"></a><span data-ttu-id="91b2c-104">CBaseFilter. EnumPins 方法</span><span class="sxs-lookup"><span data-stu-id="91b2c-104">CBaseFilter.EnumPins method</span></span>

<span data-ttu-id="91b2c-105">`EnumPins`方法會列舉此篩選器上的釘選。</span><span class="sxs-lookup"><span data-stu-id="91b2c-105">The `EnumPins` method enumerates the pins on this filter.</span></span> <span data-ttu-id="91b2c-106">這個方法會實 [**IBaseFilter：： EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) 方法。</span><span class="sxs-lookup"><span data-stu-id="91b2c-106">This method implements the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="91b2c-107">語法</span><span class="sxs-lookup"><span data-stu-id="91b2c-107">Syntax</span></span>


```C++
HRESULT EnumPins(
   IEnumPins **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="91b2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="91b2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91b2c-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="91b2c-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="91b2c-110">接收 [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) 介面指標之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="91b2c-110">Address of a variable that receives a pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91b2c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="91b2c-111">Return value</span></span>

<span data-ttu-id="91b2c-112">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="91b2c-112">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="91b2c-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="91b2c-113">Return code</span></span>                                                                                   | <span data-ttu-id="91b2c-114">Description</span><span class="sxs-lookup"><span data-stu-id="91b2c-114">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="91b2c-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="91b2c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="91b2c-116">Success</span><span class="sxs-lookup"><span data-stu-id="91b2c-116">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="91b2c-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="91b2c-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="91b2c-118">記憶體不足</span><span class="sxs-lookup"><span data-stu-id="91b2c-118">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="91b2c-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="91b2c-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="91b2c-120">**Null** 指標引數</span><span class="sxs-lookup"><span data-stu-id="91b2c-120">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91b2c-121">備註</span><span class="sxs-lookup"><span data-stu-id="91b2c-121">Remarks</span></span>

<span data-ttu-id="91b2c-122">這個方法會建立 [**CEnumPins**](cenumpins.md) 基類的實例，並將指標傳回給 **IEnumPins** 類型的物件。</span><span class="sxs-lookup"><span data-stu-id="91b2c-122">This method creates an instance of the [**CEnumPins**](cenumpins.md) base class, and returns a pointer to that object, of type **IEnumPins**.</span></span> <span data-ttu-id="91b2c-123">**CEnumPins** 類別會呼叫篩選準則的 [**CBaseFilter：： GetPin**](cbasefilter-getpin.md)方法，以列舉篩選上的釘選。</span><span class="sxs-lookup"><span data-stu-id="91b2c-123">The **CEnumPins** class calls the filter's [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method to enumerate the pins on the filter.</span></span>

<span data-ttu-id="91b2c-124">如果此方法成功，則 **IEnumPins** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="91b2c-124">If this method succeeds, the **IEnumPins** interface has an outstanding reference count.</span></span> <span data-ttu-id="91b2c-125">呼叫端必須釋放介面。</span><span class="sxs-lookup"><span data-stu-id="91b2c-125">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="91b2c-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="91b2c-126">Requirements</span></span>



| <span data-ttu-id="91b2c-127">需求</span><span class="sxs-lookup"><span data-stu-id="91b2c-127">Requirement</span></span> | <span data-ttu-id="91b2c-128">值</span><span class="sxs-lookup"><span data-stu-id="91b2c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91b2c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="91b2c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="91b2c-130"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="91b2c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="91b2c-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="91b2c-131">Library</span></span><br/> | <dl> <span data-ttu-id="91b2c-132"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="91b2c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91b2c-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91b2c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91b2c-134">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="91b2c-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




