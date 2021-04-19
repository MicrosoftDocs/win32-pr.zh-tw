---
description: 當媒體類型是在其中一個篩選器的 pin 上設定時，就會呼叫 SetMediaType 方法。
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: 'CTransformFilter. SetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995024"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="feef2-103">CTransformFilter. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="feef2-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="feef2-104">`SetMediaType`當媒體類型是在其中一個篩選器的釘選上設定時，就會呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="feef2-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="feef2-105">語法</span><span class="sxs-lookup"><span data-stu-id="feef2-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="feef2-106">參數</span><span class="sxs-lookup"><span data-stu-id="feef2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feef2-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="feef2-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="feef2-108">[**釘選 \_ 方向**](/windows/win32/api/strmif/ne-strmif-pin_direction)列舉類型的成員，在篩選上指定釘選 (輸入或輸出) 。</span><span class="sxs-lookup"><span data-stu-id="feef2-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="feef2-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="feef2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="feef2-110">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="feef2-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feef2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="feef2-111">Return value</span></span>

<span data-ttu-id="feef2-112">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="feef2-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="feef2-113">備註</span><span class="sxs-lookup"><span data-stu-id="feef2-113">Remarks</span></span>

<span data-ttu-id="feef2-114">當設定 pin 的媒體類型時， [**CTransformInputPin：： SetMediaType**](ctransforminputpin-setmediatype.md) 和 [**CTransformOutputPin：： SetMediaType**](ctransformoutputpin-setmediatype.md) 方法會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="feef2-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="feef2-115">這個方法不會在基類中執行任何動作，但衍生類別可以覆寫它。</span><span class="sxs-lookup"><span data-stu-id="feef2-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="feef2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="feef2-116">Requirements</span></span>



| <span data-ttu-id="feef2-117">需求</span><span class="sxs-lookup"><span data-stu-id="feef2-117">Requirement</span></span> | <span data-ttu-id="feef2-118">值</span><span class="sxs-lookup"><span data-stu-id="feef2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feef2-119">標頭</span><span class="sxs-lookup"><span data-stu-id="feef2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="feef2-120"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="feef2-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="feef2-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="feef2-121">Library</span></span><br/> | <dl> <span data-ttu-id="feef2-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="feef2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="feef2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feef2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feef2-124">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="feef2-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




