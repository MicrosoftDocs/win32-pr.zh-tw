---
description: GetMediaType 方法會抓取輸出圖釘的慣用媒體類型。
ms.assetid: 1bc6c06d-f399-4b8a-81f2-7fffe4630236
title: 'CTransInPlaceFilter. GetMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2347e0466a7df848e0f0b2bccec325eedfefc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990156"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="af853-103">CTransInPlaceFilter. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="af853-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="af853-104">方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="af853-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="af853-105">語法</span><span class="sxs-lookup"><span data-stu-id="af853-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="af853-106">參數</span><span class="sxs-lookup"><span data-stu-id="af853-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af853-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="af853-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="af853-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="af853-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="af853-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="af853-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="af853-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="af853-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af853-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="af853-111">Return value</span></span>

<span data-ttu-id="af853-112">傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="af853-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="af853-113">備註</span><span class="sxs-lookup"><span data-stu-id="af853-113">Remarks</span></span>

<span data-ttu-id="af853-114">這個方法會覆寫 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="af853-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="af853-115">在 **CTransInPlaceFilter** 類別中，每個圖釘都會呼叫相對的連線 pin 來列舉慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="af853-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="af853-116">輸入的 pin 會呼叫下游篩選器的輸入 pin，而且輸出 pin 會呼叫上游篩選器的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="af853-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="af853-117">因此永遠不會呼叫篩選的 `GetMediaType` 方法。</span><span class="sxs-lookup"><span data-stu-id="af853-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="af853-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="af853-118">Requirements</span></span>



| <span data-ttu-id="af853-119">需求</span><span class="sxs-lookup"><span data-stu-id="af853-119">Requirement</span></span> | <span data-ttu-id="af853-120">值</span><span class="sxs-lookup"><span data-stu-id="af853-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af853-121">標頭</span><span class="sxs-lookup"><span data-stu-id="af853-121">Header</span></span><br/>  | <dl> <span data-ttu-id="af853-122"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="af853-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="af853-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="af853-123">Library</span></span><br/> | <dl> <span data-ttu-id="af853-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="af853-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af853-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af853-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af853-126">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="af853-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




