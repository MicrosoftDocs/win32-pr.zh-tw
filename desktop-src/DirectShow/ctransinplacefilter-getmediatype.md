---
description: CTransInPlaceFilter. GetMediaType 方法-GetMediaType 方法會針對輸出釘選慣用的媒體類型。
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
ms.openlocfilehash: 8678f9b18e40f529da282909015a7c75695770ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094806"
---
# <a name="ctransinplacefiltergetmediatype-method"></a><span data-ttu-id="e06f0-103">CTransInPlaceFilter. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="e06f0-103">CTransInPlaceFilter.GetMediaType method</span></span>

<span data-ttu-id="e06f0-104">方法會抓取 `GetMediaType` 輸出圖釘的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e06f0-104">The `GetMediaType` method retrieves a preferred media type for the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e06f0-105">語法</span><span class="sxs-lookup"><span data-stu-id="e06f0-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e06f0-106">參數</span><span class="sxs-lookup"><span data-stu-id="e06f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e06f0-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="e06f0-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="e06f0-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="e06f0-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="e06f0-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="e06f0-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="e06f0-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e06f0-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e06f0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e06f0-111">Return value</span></span>

<span data-ttu-id="e06f0-112">傳回 E 非 \_ 預期的。</span><span class="sxs-lookup"><span data-stu-id="e06f0-112">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="e06f0-113">備註</span><span class="sxs-lookup"><span data-stu-id="e06f0-113">Remarks</span></span>

<span data-ttu-id="e06f0-114">這個方法會覆寫 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="e06f0-114">This method overrides the [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method.</span></span> <span data-ttu-id="e06f0-115">在 **CTransInPlaceFilter** 類別中，每個圖釘都會呼叫相對的連線 pin 來列舉慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e06f0-115">In the **CTransInPlaceFilter** class, each pin calls the opposite connected pin to enumerate preferred media types.</span></span> <span data-ttu-id="e06f0-116">輸入的 pin 會呼叫下游篩選器的輸入 pin，而且輸出 pin 會呼叫上游篩選器的輸出 pin。</span><span class="sxs-lookup"><span data-stu-id="e06f0-116">The input pin calls the downstream filter's input pin, and the output pin calls the upstream filter's output pin.</span></span> <span data-ttu-id="e06f0-117">因此永遠不會呼叫篩選的 `GetMediaType` 方法。</span><span class="sxs-lookup"><span data-stu-id="e06f0-117">Therefore, the filter's `GetMediaType` method is never called.</span></span>

## <a name="requirements"></a><span data-ttu-id="e06f0-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="e06f0-118">Requirements</span></span>



| <span data-ttu-id="e06f0-119">需求</span><span class="sxs-lookup"><span data-stu-id="e06f0-119">Requirement</span></span> | <span data-ttu-id="e06f0-120">值</span><span class="sxs-lookup"><span data-stu-id="e06f0-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06f0-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e06f0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e06f0-122"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e06f0-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e06f0-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="e06f0-123">Library</span></span><br/> | <dl> <span data-ttu-id="e06f0-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="e06f0-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e06f0-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e06f0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e06f0-126">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="e06f0-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




