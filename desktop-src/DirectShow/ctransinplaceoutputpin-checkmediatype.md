---
description: CTransInPlaceOutputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: be720021-ef7b-4281-a9f4-93abbdafc75d
title: 'CTransInPlaceOutputPin. CheckMediaType 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 66cd29758e0b2d63db88db8b998cc79ec12efdd9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094716"
---
# <a name="ctransinplaceoutputpincheckmediatype-method"></a><span data-ttu-id="92a60-103">CTransInPlaceOutputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="92a60-103">CTransInPlaceOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="92a60-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="92a60-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a60-105">語法</span><span class="sxs-lookup"><span data-stu-id="92a60-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="92a60-106">參數</span><span class="sxs-lookup"><span data-stu-id="92a60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a60-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="92a60-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="92a60-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="92a60-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a60-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="92a60-109">Return value</span></span>

<span data-ttu-id="92a60-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="92a60-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="92a60-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="92a60-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="92a60-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="92a60-112">Return code</span></span>                                                                                                | <span data-ttu-id="92a60-113">Description</span><span class="sxs-lookup"><span data-stu-id="92a60-113">Description</span></span>                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="92a60-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="92a60-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="92a60-115">成功。</span><span class="sxs-lookup"><span data-stu-id="92a60-115">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="92a60-116"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="92a60-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="92a60-117">媒體類型不被接受。</span><span class="sxs-lookup"><span data-stu-id="92a60-117">Media type not accepted.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="92a60-118">備註</span><span class="sxs-lookup"><span data-stu-id="92a60-118">Remarks</span></span>

<span data-ttu-id="92a60-119">這個方法會覆寫 [**CTransformOutputPin：： CheckMediaType**](ctransformoutputpin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="92a60-119">This method overrides the [**CTransformOutputPin::CheckMediaType**](ctransformoutputpin-checkmediatype.md) method.</span></span>

<span data-ttu-id="92a60-120">如果篩選已經進行串流處理，而且使用兩個配置器，這個方法會拒絕任何格式變更。</span><span class="sxs-lookup"><span data-stu-id="92a60-120">If the filter is already streaming and is using two allocators, this method rejects any format changes.</span></span> <span data-ttu-id="92a60-121">否則，這個方法會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法來檢查媒體類型。</span><span class="sxs-lookup"><span data-stu-id="92a60-121">Otherwise, this method calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method to check the media type.</span></span> <span data-ttu-id="92a60-122">如果輸入連接已連線，它也會在上游輸出 pin 上呼叫 [**IPin：： QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) 方法。</span><span class="sxs-lookup"><span data-stu-id="92a60-122">If the input pin is connected, it also calls the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method on the upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a60-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="92a60-123">Requirements</span></span>



| <span data-ttu-id="92a60-124">需求</span><span class="sxs-lookup"><span data-stu-id="92a60-124">Requirement</span></span> | <span data-ttu-id="92a60-125">值</span><span class="sxs-lookup"><span data-stu-id="92a60-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a60-126">標頭</span><span class="sxs-lookup"><span data-stu-id="92a60-126">Header</span></span><br/>  | <dl> <span data-ttu-id="92a60-127"><dt>Transip (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="92a60-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="92a60-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="92a60-128">Library</span></span><br/> | <dl> <span data-ttu-id="92a60-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="92a60-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a60-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92a60-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a60-131">**CTransInPlaceOutputPin 類別**</span><span class="sxs-lookup"><span data-stu-id="92a60-131">**CTransInPlaceOutputPin Class**</span></span>](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




