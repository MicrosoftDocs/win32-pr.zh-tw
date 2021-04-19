---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: 'CTransformOutputPin. CheckMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3c2bc617a5ff56a8b82184700af85e2634960ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997747"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="c868d-103">CTransformOutputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="c868d-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="c868d-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c868d-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c868d-105">語法</span><span class="sxs-lookup"><span data-stu-id="c868d-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="c868d-106">參數</span><span class="sxs-lookup"><span data-stu-id="c868d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c868d-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="c868d-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="c868d-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="c868d-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c868d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c868d-109">Return value</span></span>

<span data-ttu-id="c868d-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="c868d-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c868d-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="c868d-111">Possible values include the following.</span></span>



| <span data-ttu-id="c868d-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c868d-112">Return code</span></span>                                                                                  | <span data-ttu-id="c868d-113">Description</span><span class="sxs-lookup"><span data-stu-id="c868d-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="c868d-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c868d-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c868d-115">成功。</span><span class="sxs-lookup"><span data-stu-id="c868d-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c868d-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c868d-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c868d-117">篩選的輸入 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="c868d-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c868d-118">備註</span><span class="sxs-lookup"><span data-stu-id="c868d-118">Remarks</span></span>

<span data-ttu-id="c868d-119">這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="c868d-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="c868d-120">如果篩選的輸入 pin 未連接，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="c868d-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="c868d-121">否則，它會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，這也是純虛擬的方法。</span><span class="sxs-lookup"><span data-stu-id="c868d-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="c868d-122">篩選準則的衍生類別必須執行 **CheckTransform**，以判斷提議的輸出媒體類型是否與輸入媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="c868d-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c868d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c868d-123">Requirements</span></span>



| <span data-ttu-id="c868d-124">需求</span><span class="sxs-lookup"><span data-stu-id="c868d-124">Requirement</span></span> | <span data-ttu-id="c868d-125">值</span><span class="sxs-lookup"><span data-stu-id="c868d-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c868d-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c868d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c868d-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c868d-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c868d-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="c868d-128">Library</span></span><br/> | <dl> <span data-ttu-id="c868d-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c868d-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




