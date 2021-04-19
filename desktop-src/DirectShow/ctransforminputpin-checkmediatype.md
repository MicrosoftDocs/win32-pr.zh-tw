---
description: CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
ms.assetid: e09a4a3e-ac39-4d0e-9e8c-3e8f18057d0d
title: 'CTransformInputPin. CheckMediaType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6841370795a3131cdbcc95a3bab160be2011c600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984091"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="303ae-103">CTransformInputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="303ae-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="303ae-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="303ae-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="303ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="303ae-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="303ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="303ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="303ae-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="303ae-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="303ae-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="303ae-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="303ae-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="303ae-109">Return value</span></span>

<span data-ttu-id="303ae-110">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="303ae-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="303ae-111">備註</span><span class="sxs-lookup"><span data-stu-id="303ae-111">Remarks</span></span>

<span data-ttu-id="303ae-112">這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="303ae-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="303ae-113">它會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法，這也是純虛擬的方法。</span><span class="sxs-lookup"><span data-stu-id="303ae-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="303ae-114">篩選準則的衍生類別必須執行 **CheckInputType** ，以判斷指定的輸入類型是否可接受。</span><span class="sxs-lookup"><span data-stu-id="303ae-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="303ae-115">如果篩選的輸出連接已連接，這個方法也會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，以判斷輸入類型是否與輸出類型相容。</span><span class="sxs-lookup"><span data-stu-id="303ae-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="303ae-116">**CheckTransform** 方法也是單純的虛擬。</span><span class="sxs-lookup"><span data-stu-id="303ae-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="303ae-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="303ae-117">Requirements</span></span>



| <span data-ttu-id="303ae-118">需求</span><span class="sxs-lookup"><span data-stu-id="303ae-118">Requirement</span></span> | <span data-ttu-id="303ae-119">值</span><span class="sxs-lookup"><span data-stu-id="303ae-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="303ae-120">標頭</span><span class="sxs-lookup"><span data-stu-id="303ae-120">Header</span></span><br/>  | <dl> <span data-ttu-id="303ae-121"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="303ae-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="303ae-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="303ae-122">Library</span></span><br/> | <dl> <span data-ttu-id="303ae-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="303ae-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




