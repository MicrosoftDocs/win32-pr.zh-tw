---
description: 根據媒體類型的清單，TryMediaTypes 方法會嘗試使用這些類型的其中之一來完成連接。
ms.assetid: cc437e44-bc59-494e-8669-7f539353a794
title: 'CBasePin. TryMediaTypes 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.TryMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19b8da39d07b8aae9401bdc6ccf2eecb5d3a1e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994259"
---
# <a name="cbasepintrymediatypes-method"></a><span data-ttu-id="927ad-103">CBasePin. TryMediaTypes 方法</span><span class="sxs-lookup"><span data-stu-id="927ad-103">CBasePin.TryMediaTypes method</span></span>

<span data-ttu-id="927ad-104">根據媒體類型的清單，方法會 `TryMediaTypes` 嘗試使用這些類型的其中之一來完成連接。</span><span class="sxs-lookup"><span data-stu-id="927ad-104">Given a list of media types, the `TryMediaTypes` method tries to complete a connection using one of those types.</span></span>

## <a name="syntax"></a><span data-ttu-id="927ad-105">語法</span><span class="sxs-lookup"><span data-stu-id="927ad-105">Syntax</span></span>


```C++
virtual HRESULT TryMediaTypes(
         IPin            *pReceivePin,
   const CMediaType      *pmt,
         IEnumMediaTypes *pEnum
);
```



## <a name="parameters"></a><span data-ttu-id="927ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="927ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="927ad-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="927ad-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="927ad-108">接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="927ad-108">Pointer to the receiving pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="927ad-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="927ad-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="927ad-110">[**CMediaType**](cmediatype.md)物件的指標，該物件會限制可能的媒體類型或 **Null**。</span><span class="sxs-lookup"><span data-stu-id="927ad-110">Pointer to a [**CMediaType**](cmediatype.md) object that limits the possible media types, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="927ad-111">*pEnum*</span><span class="sxs-lookup"><span data-stu-id="927ad-111">*pEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="927ad-112">[**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes)介面的指標，用來列舉媒體類型的清單。</span><span class="sxs-lookup"><span data-stu-id="927ad-112">Pointer to an [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface, used to enumerate the list of media types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="927ad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="927ad-113">Return value</span></span>

<span data-ttu-id="927ad-114">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="927ad-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="927ad-115">可能的值包括下表中的值。</span><span class="sxs-lookup"><span data-stu-id="927ad-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="927ad-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="927ad-116">Return code</span></span>                                                                                                  | <span data-ttu-id="927ad-117">Description</span><span class="sxs-lookup"><span data-stu-id="927ad-117">Description</span></span>                                       |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="927ad-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="927ad-118"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="927ad-119">成功。</span><span class="sxs-lookup"><span data-stu-id="927ad-119">Success.</span></span><br/>                               |
| <dl> <span data-ttu-id="927ad-120"><dt>**VFW \_ E \_ 沒有 \_ 可接受的 \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="927ad-120"><dt>**VFW\_E\_NO\_ACCEPTABLE\_TYPES**</dt></span></span> </dl> | <span data-ttu-id="927ad-121">找不到可接受的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="927ad-121">Did not find an acceptable media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="927ad-122">備註</span><span class="sxs-lookup"><span data-stu-id="927ad-122">Remarks</span></span>

<span data-ttu-id="927ad-123">針對 **IEnumMediaTypes** 介面所傳回的每個媒體類型，這個方法會呼叫 [**CBasePin：： AttemptConnection**](cbasepin-attemptconnection.md) 方法來嘗試連接。</span><span class="sxs-lookup"><span data-stu-id="927ad-123">For each media type returned by the **IEnumMediaTypes** interface, this method attempts a connection by calling the [**CBasePin::AttemptConnection**](cbasepin-attemptconnection.md) method.</span></span>

<span data-ttu-id="927ad-124">如果 *pmt* 參數為非 **Null**，則 pin 會略過不符合此類型的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="927ad-124">If the *pmt* parameter is non-**NULL**, the pin skips media types that do not match this type.</span></span> <span data-ttu-id="927ad-125">*Pmt* 參數可以指定部分媒體類型。</span><span class="sxs-lookup"><span data-stu-id="927ad-125">The *pmt* parameter can specify a partial media type.</span></span> <span data-ttu-id="927ad-126">部分媒體類型的值為 \_ [主要類型]、[子類型] 或 [格式] 的 GUID Null。</span><span class="sxs-lookup"><span data-stu-id="927ad-126">A partial media type has a value of GUID\_NULL for either the major type, the subtype, or the format.</span></span> <span data-ttu-id="927ad-127">GUID \_ Null 值符合任何類型，類似于 "萬用字元" 值。</span><span class="sxs-lookup"><span data-stu-id="927ad-127">The GUID\_NULL value matches any type, similar to a "wildcard" value.</span></span>

## <a name="requirements"></a><span data-ttu-id="927ad-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="927ad-128">Requirements</span></span>



| <span data-ttu-id="927ad-129">需求</span><span class="sxs-lookup"><span data-stu-id="927ad-129">Requirement</span></span> | <span data-ttu-id="927ad-130">值</span><span class="sxs-lookup"><span data-stu-id="927ad-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="927ad-131">標頭</span><span class="sxs-lookup"><span data-stu-id="927ad-131">Header</span></span><br/>  | <dl> <span data-ttu-id="927ad-132"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="927ad-132"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="927ad-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="927ad-133">Library</span></span><br/> | <dl> <span data-ttu-id="927ad-134"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="927ad-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="927ad-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="927ad-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927ad-136">**CBasePin 類別**</span><span class="sxs-lookup"><span data-stu-id="927ad-136">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




