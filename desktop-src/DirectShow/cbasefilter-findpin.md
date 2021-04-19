---
description: FindPin 方法會使用指定的識別碼抓取 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: 'CBaseFilter. FindPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98b49c547ec59a74185f7f719da660220de8480f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983120"
---
# <a name="cbasefilterfindpin-method"></a><span data-ttu-id="2cc48-104">CBaseFilter. FindPin 方法</span><span class="sxs-lookup"><span data-stu-id="2cc48-104">CBaseFilter.FindPin method</span></span>

<span data-ttu-id="2cc48-105">`FindPin`方法會使用指定的識別碼抓取 pin。</span><span class="sxs-lookup"><span data-stu-id="2cc48-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="2cc48-106">這個方法會實 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) 方法。</span><span class="sxs-lookup"><span data-stu-id="2cc48-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cc48-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cc48-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="2cc48-108">參數</span><span class="sxs-lookup"><span data-stu-id="2cc48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cc48-109">*識別碼*</span><span class="sxs-lookup"><span data-stu-id="2cc48-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc48-110">常數、以 null 終止的 Unicode 字串的指標，可識別 pin。</span><span class="sxs-lookup"><span data-stu-id="2cc48-110">Pointer to a constant, null-terminated Unicode string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="2cc48-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="2cc48-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2cc48-112">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。</span><span class="sxs-lookup"><span data-stu-id="2cc48-112">Address of a variable that receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cc48-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2cc48-113">Return value</span></span>

<span data-ttu-id="2cc48-114">傳回下列其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2cc48-114">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="2cc48-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2cc48-115">Return code</span></span>                                                                                       | <span data-ttu-id="2cc48-116">Description</span><span class="sxs-lookup"><span data-stu-id="2cc48-116">Description</span></span>                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="2cc48-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2cc48-117"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="2cc48-118">成功。</span><span class="sxs-lookup"><span data-stu-id="2cc48-118">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="2cc48-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="2cc48-119"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="2cc48-120">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="2cc48-120">**NULL** pointer argument.</span></span><br/>     |
| <dl> <span data-ttu-id="2cc48-121"><dt>**\_ \_ 找不到 VFW E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cc48-121"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="2cc48-122">找不到相符的 pin。</span><span class="sxs-lookup"><span data-stu-id="2cc48-122">Could not find a matching pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2cc48-123">備註</span><span class="sxs-lookup"><span data-stu-id="2cc48-123">Remarks</span></span>

<span data-ttu-id="2cc48-124">這個方法會呼叫 [**CBasePin：： Name**](cbasepin-name.md) 方法，以根據 *Id* 參數所指定的字串來比較每個 pin 的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cc48-124">This method calls the [**CBasePin::Name**](cbasepin-name.md) method to compare each pin's name against the string specified by the *Id* parameter.</span></span>

<span data-ttu-id="2cc48-125">如果方法成功，則 **IPin** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="2cc48-125">If the method succeeds, the **IPin** interface has an outstanding reference count.</span></span> <span data-ttu-id="2cc48-126">當您完成時，請務必放開。</span><span class="sxs-lookup"><span data-stu-id="2cc48-126">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cc48-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="2cc48-127">Requirements</span></span>



| <span data-ttu-id="2cc48-128">需求</span><span class="sxs-lookup"><span data-stu-id="2cc48-128">Requirement</span></span> | <span data-ttu-id="2cc48-129">值</span><span class="sxs-lookup"><span data-stu-id="2cc48-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cc48-130">標頭</span><span class="sxs-lookup"><span data-stu-id="2cc48-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2cc48-131"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2cc48-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2cc48-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="2cc48-132">Library</span></span><br/> | <dl> <span data-ttu-id="2cc48-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="2cc48-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cc48-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cc48-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cc48-135">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="2cc48-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




