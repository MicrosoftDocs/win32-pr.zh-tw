---
description: SetMediaType 方法會設定連接的媒體類型。
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: 'CTransformOutputPin. SetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45bd16f0c0e5ea9cd1e719518fab15180177fd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984444"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="eae44-103">CTransformOutputPin. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="eae44-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="eae44-104">`SetMediaType`方法會設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="eae44-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae44-105">語法</span><span class="sxs-lookup"><span data-stu-id="eae44-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="eae44-106">參數</span><span class="sxs-lookup"><span data-stu-id="eae44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eae44-107">*mt*</span><span class="sxs-lookup"><span data-stu-id="eae44-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="eae44-108">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="eae44-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eae44-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eae44-109">Return value</span></span>

<span data-ttu-id="eae44-110">傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="eae44-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="eae44-111">備註</span><span class="sxs-lookup"><span data-stu-id="eae44-111">Remarks</span></span>

<span data-ttu-id="eae44-112">這個方法會覆寫 [**CBasePin：： SetMediaType**](cbasepin-setmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eae44-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="eae44-113">它會呼叫篩選器的 [**CTransformFilter：： SetMediaType**](ctransformfilter-setmediatype.md) 方法來通知篩選。</span><span class="sxs-lookup"><span data-stu-id="eae44-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="eae44-114">Pin 必須在呼叫這個方法之前，先確認媒體類型是可接受的。</span><span class="sxs-lookup"><span data-stu-id="eae44-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="eae44-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eae44-115">Requirements</span></span>



| <span data-ttu-id="eae44-116">需求</span><span class="sxs-lookup"><span data-stu-id="eae44-116">Requirement</span></span> | <span data-ttu-id="eae44-117">值</span><span class="sxs-lookup"><span data-stu-id="eae44-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eae44-118">標頭</span><span class="sxs-lookup"><span data-stu-id="eae44-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eae44-119"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="eae44-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eae44-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="eae44-120">Library</span></span><br/> | <dl> <span data-ttu-id="eae44-121"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="eae44-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




