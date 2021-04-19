---
description: SetMediaType 方法會設定連接的媒體類型。 這個方法會覆寫 CBasePin：： SetMediaType 方法。
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: 'CRendererInputPin. SetMediaType 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982696"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="d3fe2-104">CRendererInputPin. SetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="d3fe2-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="d3fe2-105">`SetMediaType`方法會設定連接的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="d3fe2-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="d3fe2-106">這個方法會覆寫 [**CBasePin：： SetMediaType**](cbasepin-setmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d3fe2-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3fe2-107">語法</span><span class="sxs-lookup"><span data-stu-id="d3fe2-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d3fe2-108">參數</span><span class="sxs-lookup"><span data-stu-id="d3fe2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3fe2-109">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="d3fe2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d3fe2-110">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d3fe2-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3fe2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3fe2-111">Return value</span></span>

<span data-ttu-id="d3fe2-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="d3fe2-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3fe2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3fe2-113">Requirements</span></span>



| <span data-ttu-id="d3fe2-114">需求</span><span class="sxs-lookup"><span data-stu-id="d3fe2-114">Requirement</span></span> | <span data-ttu-id="d3fe2-115">值</span><span class="sxs-lookup"><span data-stu-id="d3fe2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3fe2-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d3fe2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d3fe2-117"><dt>Renbase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d3fe2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d3fe2-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3fe2-118">Library</span></span><br/> | <dl> <span data-ttu-id="d3fe2-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d3fe2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3fe2-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3fe2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3fe2-121">**CRendererInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="d3fe2-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




