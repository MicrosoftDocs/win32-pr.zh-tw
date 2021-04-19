---
description: GetMediaType 方法會依索引值抓取慣用的媒體類型。
ms.assetid: d106e6d1-66ff-4460-9ea2-c93f16116cf4
title: 'CTransformOutputPin. GetMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e52a5bc3b6a2b931a8592372e2ef636863c50ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990739"
---
# <a name="ctransformoutputpingetmediatype-method"></a><span data-ttu-id="73876-103">CTransformOutputPin. GetMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="73876-103">CTransformOutputPin.GetMediaType method</span></span>

<span data-ttu-id="73876-104">`GetMediaType`方法會依索引值抓取慣用的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="73876-104">The `GetMediaType` method retrieves a preferred media type, by index value.</span></span>

## <a name="syntax"></a><span data-ttu-id="73876-105">語法</span><span class="sxs-lookup"><span data-stu-id="73876-105">Syntax</span></span>


```C++
HRESULT GetMediaType(
   int        iPosition,
   CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="73876-106">參數</span><span class="sxs-lookup"><span data-stu-id="73876-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73876-107">*Ipositionsummaryview*</span><span class="sxs-lookup"><span data-stu-id="73876-107">*iPosition*</span></span> 
</dt> <dd>

<span data-ttu-id="73876-108">以零為基底的索引值。</span><span class="sxs-lookup"><span data-stu-id="73876-108">Zero-based index value.</span></span>

</dd> <dt>

<span data-ttu-id="73876-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="73876-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="73876-110">接收媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="73876-110">Pointer to a [**CMediaType**](cmediatype.md) object that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73876-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73876-111">Return value</span></span>

<span data-ttu-id="73876-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="73876-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="73876-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="73876-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="73876-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="73876-114">Return code</span></span>                                                                                            | <span data-ttu-id="73876-115">Description</span><span class="sxs-lookup"><span data-stu-id="73876-115">Description</span></span>                   |
|--------------------------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="73876-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="73876-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="73876-117">Success</span><span class="sxs-lookup"><span data-stu-id="73876-117">Success</span></span><br/>            |
| <dl> <span data-ttu-id="73876-118"><dt>**VFW \_ S \_ 沒有 \_ 其他 \_ 專案**</dt></span><span class="sxs-lookup"><span data-stu-id="73876-118"><dt>**VFW\_S\_NO\_MORE\_ITEMS**</dt></span></span> </dl> | <span data-ttu-id="73876-119">索引超出範圍</span><span class="sxs-lookup"><span data-stu-id="73876-119">Index out of range</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="73876-120">備註</span><span class="sxs-lookup"><span data-stu-id="73876-120">Remarks</span></span>

<span data-ttu-id="73876-121">這個方法會覆寫 [**CBasePin：： GetMediaType**](cbasepin-getmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="73876-121">This method overrides the [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method.</span></span> <span data-ttu-id="73876-122">如果篩選的輸入 pin 未連接，則方法會傳回不再有 \_ 專案的 VFW \_ \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="73876-122">If the filter's input pin is not connected, the method returns VFW\_S\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="73876-123">否則，它會呼叫篩選器的 [**CTransformFilter：： GetMediaType**](ctransformfilter-getmediatype.md) 方法來取得媒體類型。</span><span class="sxs-lookup"><span data-stu-id="73876-123">Otherwise, it calls the filter's [**CTransformFilter::GetMediaType**](ctransformfilter-getmediatype.md) method to retrieve the media type.</span></span> <span data-ttu-id="73876-124">**CTransformFilter：： GetMediaType** 方法是純虛擬的;篩選準則的衍生類別必須覆寫它。</span><span class="sxs-lookup"><span data-stu-id="73876-124">The **CTransformFilter::GetMediaType** method is pure virtual; the filter's derived class must override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="73876-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="73876-125">Requirements</span></span>



| <span data-ttu-id="73876-126">需求</span><span class="sxs-lookup"><span data-stu-id="73876-126">Requirement</span></span> | <span data-ttu-id="73876-127">值</span><span class="sxs-lookup"><span data-stu-id="73876-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73876-128">標頭</span><span class="sxs-lookup"><span data-stu-id="73876-128">Header</span></span><br/>  | <dl> <span data-ttu-id="73876-129"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="73876-129"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73876-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="73876-130">Library</span></span><br/> | <dl> <span data-ttu-id="73876-131"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="73876-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




