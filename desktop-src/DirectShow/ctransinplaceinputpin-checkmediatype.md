---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 2d5f784a-8970-487d-94ef-d96d04f8eb2e
title: 'CTransInPlaceInputPin. CheckMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22f271759bc0ade6b820aed2039bbc16a2cf4a31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998752"
---
# <a name="ctransinplaceinputpincheckmediatype-method"></a><span data-ttu-id="19e9b-103">CTransInPlaceInputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="19e9b-103">CTransInPlaceInputPin.CheckMediaType method</span></span>

<span data-ttu-id="19e9b-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="19e9b-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e9b-105">語法</span><span class="sxs-lookup"><span data-stu-id="19e9b-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="19e9b-106">參數</span><span class="sxs-lookup"><span data-stu-id="19e9b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e9b-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="19e9b-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="19e9b-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="19e9b-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e9b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="19e9b-109">Return value</span></span>

<span data-ttu-id="19e9b-110">\_如果建議的媒體類型是可接受的，則傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="19e9b-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="19e9b-111">否則，會傳回 \_ FALSE 或錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19e9b-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19e9b-112">備註</span><span class="sxs-lookup"><span data-stu-id="19e9b-112">Remarks</span></span>

<span data-ttu-id="19e9b-113">這個方法會覆寫 [**CTransformInputPin：： CheckMediaType**](ctransforminputpin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="19e9b-113">This method overrides the [**CTransformInputPin::CheckMediaType**](ctransforminputpin-checkmediatype.md) method.</span></span> <span data-ttu-id="19e9b-114">它會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查輸入類型。</span><span class="sxs-lookup"><span data-stu-id="19e9b-114">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the input type.</span></span> <span data-ttu-id="19e9b-115">如果輸出連接已連線，此方法也會在下游輸入 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。</span><span class="sxs-lookup"><span data-stu-id="19e9b-115">If the output pin is connected, this method also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e9b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e9b-116">Requirements</span></span>



| <span data-ttu-id="19e9b-117">需求</span><span class="sxs-lookup"><span data-stu-id="19e9b-117">Requirement</span></span> | <span data-ttu-id="19e9b-118">值</span><span class="sxs-lookup"><span data-stu-id="19e9b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e9b-119">標頭</span><span class="sxs-lookup"><span data-stu-id="19e9b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="19e9b-120"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="19e9b-120"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19e9b-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="19e9b-121">Library</span></span><br/> | <dl> <span data-ttu-id="19e9b-122"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="19e9b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e9b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e9b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e9b-124">**CTransInPlaceInputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="19e9b-124">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




