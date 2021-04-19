---
description: FindPin 方法會取得具有指定識別碼的 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: 56ee3e0d-9e3f-4d25-846b-50119b55a122
title: 'CTransformFilter. FindPin 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1631651932d5adbc49fb59d44291dccea55fd41f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995756"
---
# <a name="ctransformfilterfindpin-method"></a><span data-ttu-id="a2486-104">CTransformFilter. FindPin 方法</span><span class="sxs-lookup"><span data-stu-id="a2486-104">CTransformFilter.FindPin method</span></span>

<span data-ttu-id="a2486-105">**FindPin** 方法會取得具有指定識別碼的 pin。</span><span class="sxs-lookup"><span data-stu-id="a2486-105">The **FindPin** method gets the pin with the specified identifier.</span></span> <span data-ttu-id="a2486-106">這個方法會實 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) 方法。</span><span class="sxs-lookup"><span data-stu-id="a2486-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2486-107">語法</span><span class="sxs-lookup"><span data-stu-id="a2486-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="a2486-108">參數</span><span class="sxs-lookup"><span data-stu-id="a2486-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2486-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="a2486-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="a2486-110">包含 pin 識別碼的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="a2486-110">Wide-character string that contains the pin identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a2486-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="a2486-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="a2486-112">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a2486-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="a2486-113">如果方法失敗， `*ppPin` 會設為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a2486-113">If the method fails, `*ppPin` is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2486-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a2486-114">Return value</span></span>

<span data-ttu-id="a2486-115">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a2486-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a2486-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a2486-116">Return code</span></span>                                                                                       | <span data-ttu-id="a2486-117">Description</span><span class="sxs-lookup"><span data-stu-id="a2486-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="a2486-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a2486-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="a2486-119">成功。</span><span class="sxs-lookup"><span data-stu-id="a2486-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a2486-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a2486-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="a2486-121">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="a2486-121">Insufficient memory.</span></span><br/>                       |
| <dl> <span data-ttu-id="a2486-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="a2486-122"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="a2486-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="a2486-123">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="a2486-124"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a2486-124"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a2486-125">找不到具有此識別碼的 pin。</span><span class="sxs-lookup"><span data-stu-id="a2486-125">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2486-126">備註</span><span class="sxs-lookup"><span data-stu-id="a2486-126">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2486-127">此方法的執行不會呼叫 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 來符合 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2486-127">The implementation of this method does not call [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) to match the pin identifier.</span></span> <span data-ttu-id="a2486-128">相反地，此方法會假設輸入的 pin 名為 "In"，且輸出的 pin 名為 "Out"。</span><span class="sxs-lookup"><span data-stu-id="a2486-128">Instead, the method assumes that the input pin is named "In", and the output pin is named "Out".</span></span> <span data-ttu-id="a2486-129">如果您使用一組不同的 pin 識別碼，請覆寫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a2486-129">If you use a different set of pin identifiers, override this method.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2486-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="a2486-130">Requirements</span></span>



| <span data-ttu-id="a2486-131">需求</span><span class="sxs-lookup"><span data-stu-id="a2486-131">Requirement</span></span> | <span data-ttu-id="a2486-132">值</span><span class="sxs-lookup"><span data-stu-id="a2486-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2486-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a2486-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a2486-134"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a2486-134"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a2486-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="a2486-135">Library</span></span><br/> | <dl> <span data-ttu-id="a2486-136"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a2486-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2486-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a2486-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2486-138">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="a2486-138">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




