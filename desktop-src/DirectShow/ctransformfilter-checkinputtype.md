---
description: CheckInputType 方法會檢查輸入是否可接受指定的媒體類型。
ms.assetid: 11f156f7-add2-45be-a0d3-05d21f596b89
title: 'CTransformFilter. CheckInputType 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckInputType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63c48a0502ee074b0940f85386dca0619a3ad12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000706"
---
# <a name="ctransformfiltercheckinputtype-method"></a><span data-ttu-id="4b374-103">CTransformFilter. CheckInputType 方法</span><span class="sxs-lookup"><span data-stu-id="4b374-103">CTransformFilter.CheckInputType method</span></span>

<span data-ttu-id="4b374-104">`CheckInputType`方法會檢查輸入是否可接受指定的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4b374-104">The `CheckInputType` method checks whether a specified media type is acceptable for input.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b374-105">語法</span><span class="sxs-lookup"><span data-stu-id="4b374-105">Syntax</span></span>


```C++
virtual HRESULT CheckInputType(
   const CMediaType *mtIn
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4b374-106">參數</span><span class="sxs-lookup"><span data-stu-id="4b374-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b374-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="4b374-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="4b374-108">指定媒體類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4b374-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b374-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b374-109">Return value</span></span>

<span data-ttu-id="4b374-110">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4b374-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4b374-111">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="4b374-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="4b374-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4b374-112">Return code</span></span>                                                                                                | <span data-ttu-id="4b374-113">Description</span><span class="sxs-lookup"><span data-stu-id="4b374-113">Description</span></span>                              |
|------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="4b374-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4b374-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="4b374-115">媒體類型是可接受的。</span><span class="sxs-lookup"><span data-stu-id="4b374-115">Media type is acceptable.</span></span><br/>     |
| <dl> <span data-ttu-id="4b374-116"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="4b374-116"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="4b374-117">媒體類型無法接受。</span><span class="sxs-lookup"><span data-stu-id="4b374-117">Media type is not acceptable.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b374-118">備註</span><span class="sxs-lookup"><span data-stu-id="4b374-118">Remarks</span></span>

<span data-ttu-id="4b374-119">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="4b374-119">The derived class must implement this method.</span></span> <span data-ttu-id="4b374-120">\_如果可接受建議的輸入格式，則傳回 S OK，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4b374-120">Return S\_OK if the proposed input format is acceptable, or an error code otherwise.</span></span>

<span data-ttu-id="4b374-121">如果有任何) ，則這個方法不需要確認輸入格式是否與輸出格式相容 (。</span><span class="sxs-lookup"><span data-stu-id="4b374-121">This method does not need to verify that the input format is compatible with the output format (if any).</span></span> <span data-ttu-id="4b374-122">輸入 pin 會藉由呼叫 [**CheckTransform**](ctransformfilter-checktransform.md) 方法來確認。</span><span class="sxs-lookup"><span data-stu-id="4b374-122">The input pin verifies that by calling the [**CheckTransform**](ctransformfilter-checktransform.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b374-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b374-123">Requirements</span></span>



| <span data-ttu-id="4b374-124">需求</span><span class="sxs-lookup"><span data-stu-id="4b374-124">Requirement</span></span> | <span data-ttu-id="4b374-125">值</span><span class="sxs-lookup"><span data-stu-id="4b374-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b374-126">標頭</span><span class="sxs-lookup"><span data-stu-id="4b374-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4b374-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4b374-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4b374-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="4b374-128">Library</span></span><br/> | <dl> <span data-ttu-id="4b374-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4b374-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b374-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b374-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b374-131">**CTransformFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="4b374-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




