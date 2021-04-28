---
description: CTransformInputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
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
ms.openlocfilehash: c775618c9fe30de6171919d5b8bc8a80ea81d3a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084996"
---
# <a name="ctransforminputpincheckmediatype-method"></a><span data-ttu-id="16b71-103">CTransformInputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="16b71-103">CTransformInputPin.CheckMediaType method</span></span>

<span data-ttu-id="16b71-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="16b71-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b71-105">語法</span><span class="sxs-lookup"><span data-stu-id="16b71-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="16b71-106">參數</span><span class="sxs-lookup"><span data-stu-id="16b71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16b71-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="16b71-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="16b71-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="16b71-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16b71-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="16b71-109">Return value</span></span>

<span data-ttu-id="16b71-110">傳回 S \_ OK 或其他 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="16b71-110">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b71-111">備註</span><span class="sxs-lookup"><span data-stu-id="16b71-111">Remarks</span></span>

<span data-ttu-id="16b71-112">這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="16b71-112">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="16b71-113">它會呼叫篩選器的 [**CTransformFilter：： CheckInputType**](ctransformfilter-checkinputtype.md) 方法，這也是純虛擬的方法。</span><span class="sxs-lookup"><span data-stu-id="16b71-113">It calls the filter's [**CTransformFilter::CheckInputType**](ctransformfilter-checkinputtype.md) method, which is also pure virtual.</span></span> <span data-ttu-id="16b71-114">篩選準則的衍生類別必須執行 **CheckInputType** ，以判斷指定的輸入類型是否可接受。</span><span class="sxs-lookup"><span data-stu-id="16b71-114">The filter's derived class must implement **CheckInputType** to determine whether a given input type is acceptable.</span></span>

<span data-ttu-id="16b71-115">如果篩選的輸出連接已連接，這個方法也會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，以判斷輸入類型是否與輸出類型相容。</span><span class="sxs-lookup"><span data-stu-id="16b71-115">If the filter's output pin is connected, this method also calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method to determine whether the input type is compatible with the output type.</span></span> <span data-ttu-id="16b71-116">**CheckTransform** 方法也是單純的虛擬。</span><span class="sxs-lookup"><span data-stu-id="16b71-116">The **CheckTransform** method is pure virtual as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="16b71-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="16b71-117">Requirements</span></span>



| <span data-ttu-id="16b71-118">需求</span><span class="sxs-lookup"><span data-stu-id="16b71-118">Requirement</span></span> | <span data-ttu-id="16b71-119">值</span><span class="sxs-lookup"><span data-stu-id="16b71-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16b71-120">標頭</span><span class="sxs-lookup"><span data-stu-id="16b71-120">Header</span></span><br/>  | <dl> <span data-ttu-id="16b71-121"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="16b71-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16b71-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="16b71-122">Library</span></span><br/> | <dl> <span data-ttu-id="16b71-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="16b71-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




