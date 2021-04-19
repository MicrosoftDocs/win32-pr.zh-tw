---
description: CheckTransform 方法會檢查輸入媒體類型是否與輸出媒體類型相容。 這個方法會覆寫 CTransformFilter：： CheckTransform 方法。
ms.assetid: d0953014-4a49-4738-a449-c247396a6794
title: 'CTransInPlaceFilter. CheckTransform 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6a80132723be0b70f2c4afe93306d7f581b7734c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993649"
---
# <a name="ctransinplacefilterchecktransform-method"></a><span data-ttu-id="c11f7-104">CTransInPlaceFilter. CheckTransform 方法</span><span class="sxs-lookup"><span data-stu-id="c11f7-104">CTransInPlaceFilter.CheckTransform method</span></span>

<span data-ttu-id="c11f7-105">`CheckTransform`方法會檢查輸入媒體類型是否與輸出媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="c11f7-105">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span> <span data-ttu-id="c11f7-106">這個方法會覆寫 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c11f7-106">This method overrides the [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c11f7-107">語法</span><span class="sxs-lookup"><span data-stu-id="c11f7-107">Syntax</span></span>


```C++
HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
);
```



## <a name="parameters"></a><span data-ttu-id="c11f7-108">參數</span><span class="sxs-lookup"><span data-stu-id="c11f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c11f7-109">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="c11f7-109">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c11f7-110">指定輸入類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c11f7-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="c11f7-111">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="c11f7-111">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="c11f7-112">指定輸出類型之 **CMediaType** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="c11f7-112">Pointer to a **CMediaType** object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c11f7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c11f7-113">Return value</span></span>

<span data-ttu-id="c11f7-114">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="c11f7-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c11f7-115">備註</span><span class="sxs-lookup"><span data-stu-id="c11f7-115">Remarks</span></span>

<span data-ttu-id="c11f7-116">**CTransInPlace** 篩選準則永遠不會呼叫 `CheckTransform` 。</span><span class="sxs-lookup"><span data-stu-id="c11f7-116">The **CTransInPlace** filter never calls `CheckTransform`.</span></span> <span data-ttu-id="c11f7-117">相反地，所有 pin 連接都會使用 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 來檢查媒體類型，並假設輸入和輸出類型一律相符。</span><span class="sxs-lookup"><span data-stu-id="c11f7-117">Instead, all pin connection use [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) to check the media type, with the assumption that the input and output types always match.</span></span>

## <a name="requirements"></a><span data-ttu-id="c11f7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c11f7-118">Requirements</span></span>



| <span data-ttu-id="c11f7-119">需求</span><span class="sxs-lookup"><span data-stu-id="c11f7-119">Requirement</span></span> | <span data-ttu-id="c11f7-120">值</span><span class="sxs-lookup"><span data-stu-id="c11f7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c11f7-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c11f7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c11f7-122"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c11f7-122"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c11f7-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="c11f7-123">Library</span></span><br/> | <dl> <span data-ttu-id="c11f7-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c11f7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c11f7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c11f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c11f7-126">**CTransInPlaceFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="c11f7-126">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




