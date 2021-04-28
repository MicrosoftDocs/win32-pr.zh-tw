---
description: CTransformOutputPin. CheckMediaType 方法-CheckMediaType 方法會判斷 pin 是否接受特定的媒體類型。
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
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084906"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="239dd-103">CTransformOutputPin. CheckMediaType 方法</span><span class="sxs-lookup"><span data-stu-id="239dd-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="239dd-104">`CheckMediaType`方法會判斷 pin 是否接受特定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="239dd-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="239dd-105">語法</span><span class="sxs-lookup"><span data-stu-id="239dd-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="239dd-106">參數</span><span class="sxs-lookup"><span data-stu-id="239dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239dd-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="239dd-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="239dd-108">[**CMediaType**](cmediatype.md)物件的指標，該物件包含建議的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="239dd-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239dd-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="239dd-109">Return value</span></span>

<span data-ttu-id="239dd-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="239dd-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="239dd-111">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="239dd-111">Possible values include the following.</span></span>



| <span data-ttu-id="239dd-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="239dd-112">Return code</span></span>                                                                                  | <span data-ttu-id="239dd-113">Description</span><span class="sxs-lookup"><span data-stu-id="239dd-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="239dd-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="239dd-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="239dd-115">成功。</span><span class="sxs-lookup"><span data-stu-id="239dd-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="239dd-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="239dd-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="239dd-117">篩選的輸入 pin 未連接。</span><span class="sxs-lookup"><span data-stu-id="239dd-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="239dd-118">備註</span><span class="sxs-lookup"><span data-stu-id="239dd-118">Remarks</span></span>

<span data-ttu-id="239dd-119">這個方法會實作為純虛擬 [**CBasePin：： CheckMediaType**](cbasepin-checkmediatype.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="239dd-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="239dd-120">如果篩選的輸入 pin 未連接，則方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="239dd-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="239dd-121">否則，它會呼叫篩選器的 [**CTransformFilter：： CheckTransform**](ctransformfilter-checktransform.md) 方法，這也是純虛擬的方法。</span><span class="sxs-lookup"><span data-stu-id="239dd-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="239dd-122">篩選準則的衍生類別必須執行 **CheckTransform**，以判斷提議的輸出媒體類型是否與輸入媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="239dd-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="239dd-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="239dd-123">Requirements</span></span>



| <span data-ttu-id="239dd-124">需求</span><span class="sxs-lookup"><span data-stu-id="239dd-124">Requirement</span></span> | <span data-ttu-id="239dd-125">值</span><span class="sxs-lookup"><span data-stu-id="239dd-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239dd-126">標頭</span><span class="sxs-lookup"><span data-stu-id="239dd-126">Header</span></span><br/>  | <dl> <span data-ttu-id="239dd-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="239dd-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="239dd-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="239dd-128">Library</span></span><br/> | <dl> <span data-ttu-id="239dd-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="239dd-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




