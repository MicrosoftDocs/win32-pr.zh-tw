---
description: AgreeMediaType 方法會搜尋媒體類型，以建立 pin 連接。
ms.assetid: 545186d2-b5e8-4833-b0ff-11160c1dd53b
title: 'CBasePin. AgreeMediaType 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AgreeMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e5cdea12cb8bca3319f908fe697251a3d4699d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998678"
---
# <a name="cbasepinagreemediatype-method"></a><span data-ttu-id="eaeb6-103">CBasePin. AgreeMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="eaeb6-103">CBasePin.AgreeMediaType method</span></span>

<span data-ttu-id="eaeb6-104">此 `AgreeMediaType` 方法會搜尋媒體類型，以建立 pin 連接。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-104">The `AgreeMediaType` method searches for a media type to make a pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaeb6-105">語法</span><span class="sxs-lookup"><span data-stu-id="eaeb6-105">Syntax</span></span>


```C++
virtual HRESULT AgreeMediaType(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="eaeb6-106">參數</span><span class="sxs-lookup"><span data-stu-id="eaeb6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaeb6-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="eaeb6-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="eaeb6-108">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="eaeb6-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="eaeb6-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="eaeb6-110">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標，或 **為 Null**。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies a media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaeb6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaeb6-111">Return value</span></span>

<span data-ttu-id="eaeb6-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="eaeb6-113">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="eaeb6-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eaeb6-114">Return code</span></span>                                                                                                  | <span data-ttu-id="eaeb6-115">Description</span><span class="sxs-lookup"><span data-stu-id="eaeb6-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="eaeb6-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eaeb6-116"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="eaeb6-117">成功。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="eaeb6-118"><dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="eaeb6-118"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="eaeb6-119">找不到可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-119">No acceptable media type was found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaeb6-120">備註</span><span class="sxs-lookup"><span data-stu-id="eaeb6-120">Remarks</span></span>

<span data-ttu-id="eaeb6-121">如果 *pmt* 參數為非 **Null** ，且完整指定媒體類型，這個方法會嘗試使用該媒體類型的連接。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-121">If the *pmt* parameter is non-**NULL** and fully specifies a media type, this method attempts a connection using that media type.</span></span> <span data-ttu-id="eaeb6-122">如果嘗試失敗，方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-122">If the attempt fails, the method returns an error.</span></span>

<span data-ttu-id="eaeb6-123">如果 *pmt* 參數為 **Null** 或指定部分媒體類型，這個方法會依下列順序嘗試媒體類型：</span><span class="sxs-lookup"><span data-stu-id="eaeb6-123">If the *pmt* parameter is **NULL** or specifies a partial media type, this method tries media types in the following order:</span></span>

1.  <span data-ttu-id="eaeb6-124">接收釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-124">The receiving pin's preferred media types.</span></span>
2.  <span data-ttu-id="eaeb6-125">此 pin 的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-125">This pin's preferred media types.</span></span>

<span data-ttu-id="eaeb6-126">慣用的媒體類型會以 [**CBasePin：： EnumMediaTypes**](cbasepin-enummediatypes.md) 方法列舉，而產生的列舉值會傳遞至 [**CBasePin：： TryMediaTypes**](cbasepin-trymediatypes.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eaeb6-126">Preferred media types are enumerated with the [**CBasePin::EnumMediaTypes**](cbasepin-enummediatypes.md) method, and the resulting enumerator is passed to the [**CBasePin::TryMediaTypes**](cbasepin-trymediatypes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eaeb6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaeb6-127">Requirements</span></span>



| <span data-ttu-id="eaeb6-128">需求</span><span class="sxs-lookup"><span data-stu-id="eaeb6-128">Requirement</span></span> | <span data-ttu-id="eaeb6-129">值</span><span class="sxs-lookup"><span data-stu-id="eaeb6-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaeb6-130">標頭</span><span class="sxs-lookup"><span data-stu-id="eaeb6-130">Header</span></span><br/>  | <dl> <span data-ttu-id="eaeb6-131"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eaeb6-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eaeb6-132">程式庫</span><span class="sxs-lookup"><span data-stu-id="eaeb6-132">Library</span></span><br/> | <dl> <span data-ttu-id="eaeb6-133"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eaeb6-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaeb6-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaeb6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaeb6-135">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="eaeb6-135">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




